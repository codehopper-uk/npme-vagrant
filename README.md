# npme-vagrant

> a vagrant setup for trialing npm Enterprise

Want to use npm, but behind a firewall? npm offers [npm Enterprise] as
a way to replicate the npm Public Registry, run it behind a firewall,
allowing for:

- use/publish private packages
- use/publish public packages
- whitelist/blacklist public packages

## Prerequisites

To get up and running all you'll need is:

- [Vagrant]
- [VirtualBox]
- a FREE [npm Enterprise Trial Key]

## Up and Running

1. Install and/or retrieve all the [Prerequisites]
2. Type `vagrant up` in your terminal
3. Open [`localhost:8800`] in your browser
4. You'll see a screen that looks like this ![not safe](images/1.png)
5. Click `Advanced`. It will show another panel that looks like this ![advanced](images/2.png)
6. Click `Proceed to localhost(unsafe)` (it's safe. i promise :smile:)
7. You'll see a screen that looks like this ![certificate](images/3.png)
   Type `localhost` and then click `Use Self-Signed Certificate`
8. You'll see a screen that asks for your email address and License key, type those in and press the button to continue
9. You'll see a screen that looks like this ![settings](images/4.png)
  Replace what is pre-filled with:
    - Full URL of npm Enterprise registry: `localhost:8080`
    - Full URL of npm Enteprise website: `localhost:8081`
10. Scroll down until you see a section called "Authentication" that looks like the image below. Select `Open`. ![auth](images/5.png)
11. Save. You'll see a dialog to restart your service. Click Restart Now.
12. Visit [`localhost:8081`]. You have the npm website running! You registry is running at [`localhost:8081`]

[npm Enterprise]: https://www.npmjs.com/enterprise
[Vagrant]: https://www.vagrantup.com/
[VirtualBox]: https://www.virtualbox.org/wiki/Downloads
[npm Enterprise Trial Key]: https://www.npmjs.com/enterprise
[Prerequisites]: #Prerequisites
[`localhost:8800`]: http://localhost:8800
[`localhost:8080`]: http://localhost:8080
[`localhost:8081`]: http://localhost:8081
