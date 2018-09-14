
# olock — seamless auth ui

olock is an authentication user interface contained within a modal, for your single-page application

**"seamless auth"** — *authentication which operates entirely from a modal, no page refreshes or redirects for login/logout/password-reset routines*

- built to interoperate with [ooth](https://github.com/nmaro/ooth)
- inspired by the [staart](https://github.com/nmaro/staart) ui project (which isn't seamless)

----

# chase's dev diary

## 2018-09-13 'olock' project begins

i recently came across nick redmark's [ooth](https://github.com/nmaro/ooth) project, and thought this might be a good option to build new user accounting systems

so i reached out to nick on his [ooth slack channel](https://ooth.slack.com/), to ask him about achieving what i'm starting to call a "seamless" authentication experience

auth0 uses the term "embedded", but i think i prefer "seamless"

**chase-moskal:**

> Hello @nmaro! Really impressed with what you've done with ooth! I've got an idea, a question, and I'm looking for some pointers:
>
> *How can I create an "embedded" authentication UI for ooth?*
>
> I'm hoping to create a "completely seamlesss" clientside experience for single-page applications
>
> I'm thinking of an experience where the user can login, logout, reset password, etc — all from within a modal dialog — without any page refreshes, reloads, or redirects
>
> Is this feasible?
>
> If so, I would like to build an ooth-compatible UI library for the purpose (with `typescript`, `preact`, and `mobx`)
>
> I currently understand that staart is build in a more traditional way, with a dedicated `/login` page and such
>
> @nmaro, if an "embedded" UI was created, how would you imagine it should differ from staart? And how might somebody like myself best get started? What limitations or drawbacks might I face?
>
> Thanks!

**nmaro:**

> hey @chase-moskal I think what you are aiming at should be entirely possible.
>
> in fact it should be even easier than what staart is aiming to accomplish
>
> the first step is to bootstrap a single-page application - for example using create-react-app
>
> I don't know what's out there for preact
>
> but the next step would be to create the ui components (i'd advise you to use the staart components as inspiration)
>
> the thing you need to do, really, is to create some forms and then call the appropriate ooth-client methods on submit
>
> then, if you want to display or hide things based on whether the user is logged in you can subscribe to changes to the ooht-client user event (as described here: https://nmaro.github.io/ooth/#subscribe-to-the-user-object)

so, i'm getting started on this project, playing around, we'll see where it goes
