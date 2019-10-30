---
title: Skonfiguruj środowisko programistyczne
typora-copy-images-to: ./
disableTableOfContents: true
---

Before you start building your first Gatsby site, you’ll need to familiarize yourself with some core web technologies and make sure that you have installed all required software tools.

Zanim zaczniesz budować swoją pierwszą strone Gatsby, musisz zapoznać się z niektórymi podstawowymi internetowymi technologiami i upewnić się, że zainstalowałeś wszystkie wymagane narzędzia oraz programy.

## Zapoznaj się z wierzem poleceń

Wiersz poleceń to interfejs tekstowy służący do uruchamiania poleceń na komputerze. Często występuje pod nazwą terminal. W tym samouczku będziemy używać obu określeń zamiennie. Uźywanie terminala przypomina używanie Findera na komputerach Mac lub Eksploratora w systemie Windows. Finder i Explorer to przykłady graficznych interfejsów użytkownika (GUI). Wiersz poleceń to potężny, tekstowy sposób interakcji z komputerem.

Poświęć chwilę, aby zlokalizować i otworzyć interfejs wiersza poleceń (CLI) dla swojego komputera. W zależności od używanego systemu operacyjnego zobacz [**instrukcje dla komputerów Mac**](https://www.imymac.com/pl/mac-cleaner/how-to-open-terminal-on-mac.html), [**instrukcje dla systemu Windows**](https://www.download.net.pl/10-sposobow-na-uruchomienie-wiersza-polecenia-w-windows-10/n/7949/) or [**instrukcje dla systemu Linux**](https://pl.wikibooks.org/wiki/Ubuntu/Podstawowe_polecenia).

## Zainstaluj Homebrew dla Node.js

To install Gatsby and Node.js, it is recommended to use [Homebrew](https://brew.sh/). Trochę konfiguracji na początku może uchronić Cię przed niektórymi bolączkami w późniejszych krokach!

Jak zainstalować lub zweryfikować Homebrew na komputerze:

1.  Otwórz Terminal.
2.  Sprawdź czy Homebrew jest zainstalowane uruchamiając komendę `brew -v`. Powinieneś zobaczyć "Homebrew" oraz numer wersji.
3.  Jeśli nie, pobierz i zainstaluj [Homebrew wraz z instrukcją](https://docs.brew.sh/Installation) dla swojego systemu operacyjnego (Mac, Linux lub Windows).
4.  Po zainstalowaniu Homebrew powtórz krok 2, aby zweryfikować.

### Użytkownicy komputerów Mac: zainstaluj Xcode Command Line Tools

1.  Otwórz Terminal.
2.  Na Macu, zainstaluj Xcode Command Line Tools uruchamiając komendę `xcode-select --install`.
3.  Jeśli ten sposób zawiedzie, pobierz [bezpośrednio ze strony Apple](https://developer.apple.com/download/more/), po zalogowaniu się za pomocą konta programisty Apple.
4.  Po wyświetleniu monitu o rozpoczęcie instalacji ponownie pojawi się monit o zaakceptowanie licencji na oprogramowanie do pobrania narzędzi.

## ⌚ Zainstaluj Node.js oraz npm

Node.js to środowisko, które może uruchamiać kod JavaScript poza przeglądarką internetową. Gatsby jest napisane w Node.js. Aby rozpocząć pracę z Gatsby, musisz mieć najnowszą wersję zainstalowaną na komputerze.

_Note: Minimalna wersja Node wspierana przez Gatsby to wersja 8, ale możesz teź użyć nowszej wersji._

1.  Otwórz Terminal.
2.  Uruchom komendę `brew update` aby upewnić się, że masz najnowszą wersję Homebrew.
3.  Uruchom tę komendę, aby zainstalować Node i npm naraz: `brew install node`

Po wykonaniu wszystkich kroków upewnij się, że wszystko zostało poprawnie zainstalowane:

### Sprawdź czy Node.js jest zainstalowane poprawnie

1.  Otwórz Terminal.
2.  Uruchom komendę `node --version`. (Jeśli dopiero zaczynasz korzystać z terminala, “uruchom `komendę`” oznacza “wpisz `node -version` w wierszu polecenia i naciśnij klawisz Enter”. Od tego momentu właśnie to rozumiemy jako "Uruchom `komendę`”)
3.  Uruchom komendę `npm --version`.

The output of each of those commands should be a version number. Your versions may not be the same as those shown below! If entering those commands doesn’t show you a version number, go back and make sure you have installed Node.js.

![Check node and npm versions in terminal](01-node-npm-versions.png)

## Install Git

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. When you install a Gatsby "starter" site, Gatsby uses Git behind the scenes to download and install the required files for your starter. You will need to have Git installed to set up your first Gatsby site.

The steps to download and install Git depend on your operating system. Follow the guide for your system:

- [Install Git on macOS](https://www.atlassian.com/git/tutorials/install-git#mac-os-x)
- [Install Git on Windows](https://www.atlassian.com/git/tutorials/install-git#windows)
- [Install Git on Linux](https://www.atlassian.com/git/tutorials/install-git#linux)

## Using the Gatsby CLI

The Gatsby CLI tool lets you quickly create new Gatsby-powered sites and run commands for developing Gatsby sites. It is a published npm package.

The Gatsby CLI is available via npm and should be installed globally by running `npm install -g gatsby-cli`.

_**Note**: when you install Gatsby and run it for the first time, you'll see a short message notifying you about anonymous usage data that is being collected for Gatsby commands, you can read more about how that data is pulled out and used in the [telemetry doc](/docs/telemetry)._

To see the commands available, run `gatsby --help`.

![Check gatsby commands in terminal](05-gatsby-help.png)

> 💡 If you are unable to successfully run the Gatsby CLI due to a permissions issue, you may want to check out the [npm docs on fixing permissions](https://docs.npmjs.com/getting-started/fixing-npm-permissions), or [this guide](https://github.com/sindresorhus/guides/blob/master/npm-global-without-sudo.md).

## Create a Gatsby site

Now you are ready to use the Gatsby CLI tool to create your first Gatsby site. Using the tool, you can download “starters” (partially built sites with some default configuration) to help you get moving faster on creating a certain type of site. The “Hello World” starter you’ll be using here is a starter with the bare essentials needed for a Gatsby site.

1.  Open up your terminal.
2.  Run `gatsby new hello-world https://github.com/gatsbyjs/gatsby-starter-hello-world`. (_Note: Depending on your download speed, the amount of time this takes will vary. For brevity's sake, the gif below was paused during part of the install_).
3.  Run `cd hello-world`.
4.  Run `gatsby develop`.

<video controls="controls" autoplay="true" loop="true">
  <source type="video/mp4" src="./03-create-site.mp4" />
  <p>Sorry! You browser doesn't support this video.</p>
</video>

What just happened?

```shell
gatsby new hello-world https://github.com/gatsbyjs/gatsby-starter-hello-world
```

- `new` is a gatsby command to create a new Gatsby project.
- Here, `hello-world` is an arbitrary title — you could pick anything. The CLI tool will place the code for your new site in a new folder called “hello-world”.
- Lastly, the GitHub URL specified points to a code repository that holds the starter code you want to use.

```shell
cd hello-world
```

- This says 'I want to change directories (`cd`) to the “hello-world” subfolder'. Whenever you want to run any commands for your site, you need to be in the context for that site (aka, your terminal needs to be pointed at the directory where your site code lives).

```shell
gatsby develop
```

- This command starts a development server. You will be able to see and interact with your new site in a development environment — local (on your computer, not published to the internet).

### View your site locally

Open up a new tab in your browser and navigate to [**http://localhost:8000**](http://localhost:8000/).

![Check homepage](04-home-page.png)

Congrats! This is the beginning of your very first Gatsby site! 🎉

You’ll be able to visit the site locally at [**_http://localhost:8000_**](http://localhost:8000/) for as long as your development server is running. That’s the process you started by running the `gatsby develop` command. To stop running that process (or to “stop running the development server”), go back to your terminal window, hold down the “control” key, and then hit “c” (ctrl-c). To start it again, run `gatsby develop` again!

**Note:** If you are using VM setup like `vagrant` and/or would like to listen on your local IP address, run `gatsby develop -- --host=0.0.0.0`. Now, the development server listens on both 'localhost' and your local IP.

## Set up a code editor

A code editor is a program designed specifically for editing computer code. There are many great ones out there.

### Download VS Code

Gatsby documentation sometimes includes screenshots that were taken in VS Code, so if you don't have a preferred code editor yet, using VS Code will make sure that your screen looks just like the screenshots in the tutorial and docs. If you choose to use VS Code, visit the [VS Code site](https://code.visualstudio.com/#alt-downloads) and download the version appropriate for your platform.

### Install the Prettier plugin

We also recommend using [Prettier](https://github.com/prettier/prettier), a tool that helps format your code to avoid errors.

You can use Prettier directly in your editor using the [Prettier VS Code plugin](https://github.com/prettier/prettier-vscode):

1.  Open the extensions view on VS Code (View => Extensions).
2.  Search for "Prettier - Code formatter".
3.  Click "Install". (After installation you'll be prompted to restart VS Code to enable the extension. Newer versions of VS Code will automatically enable the extension after download.)

> 💡 If you're not using VS Code, check out the Prettier docs for [install instructions](https://prettier.io/docs/en/install.html) or [other editor integrations](https://prettier.io/docs/en/editors.html).

## ➡️ What’s Next?

To summarize, in this section you:

- Learned about the command line and how to use it
- Installed and learned about Node.js and the npm CLI tool, the version control system Git, and the Gatsby CLI tool
- Generated a new Gatsby site using the Gatsby CLI tool
- Ran the Gatsby development server and visited your site locally
- Downloaded a code editor
- Installed a code formatter called Prettier

Now, move on to [**getting to know Gatsby building blocks**](/tutorial/part-one/).

## References

### Overview of core technologies

It’s not necessary to be an expert with these already — if you’re not, don’t worry! You’ll pick up a lot through the course of this tutorial series. These are some of the main web technologies you’ll use when building a Gatsby site:

- **HTML**: A markup language that every web browser is able to understand. It stands for HyperText Markup Language. HTML gives your web content a universal informational structure, defining things like headings, paragraphs, and more.
- **CSS**: A presentational language used to style the appearance of your web content (fonts, colors, layout, etc). It stands for Cascading Style Sheets.
- **JavaScript**: A programming language that helps us make the web dynamic and interactive.
- **React**: A code library (built with JavaScript) for building user interfaces. It’s the framework that Gatsby uses to build pages and structure content.
- **GraphQL**: A query language that allows you to pull data into your website. It’s the interface that Gatsby uses for managing site data.

### What is a website?

For a comprehensive introduction to what a website is--including an intro to HTML and CSS--check out “[**Building your first web page**](https://learn.shayhowe.com/html-css/building-your-first-web-page/)”. It’s a great place to start learning about the web. For a more hands-on introduction to [**HTML**](https://www.codecademy.com/learn/learn-html), [**CSS**](https://www.codecademy.com/learn/learn-css), and [**JavaScript**](https://www.codecademy.com/learn/introduction-to-javascript), check out the tutorials from Codecademy. [**React**](https://reactjs.org/tutorial/tutorial.html) and [**GraphQL**](http://graphql.org/graphql-js/) also have their own introductory tutorials.

### Learn more about the command line

For a great introduction to using the command line, check out [**Codecademy’s Command Line tutorial**](https://www.codecademy.com/courses/learn-the-command-line/lessons/navigation/exercises/your-first-command) for Mac and Linux users, and [**this tutorial**](https://www.computerhope.com/issues/chusedos.htm) for Windows users. Even if you are a Windows user, the first page of the Codecademy tutorial is a valuable read. It explains what the command line is, not just how to interface with it.

### Learn more about npm

npm is a JavaScript package manager. A package is a module of code that you can choose to include in your projects. If you just downloaded and installed Node.js, npm was installed with it!

npm has three distinct components: the npm website, the npm registry, and the npm command line interface (CLI).

- On the npm website, you can browse what JavaScript packages are available in the npm registry.
- The npm registry is a large database of information about JavaScript packages available on npm.
- Once you’ve identified a package you want, you can use the npm CLI to install it in your project or globally (like other CLI tools). The npm CLI is what talks to the registry — you generally only interact with the npm website or the npm CLI.

> 💡 Check out npm’s introduction, “[**What is npm?**](https://docs.npmjs.com/getting-started/what-is-npm)”.

### Learn more about Git

You will not need to know Git to complete this tutorial, but it is a very useful tool. If you are interested in learning more about version control, Git, and GitHub, check out GitHub's [Git Handbook](https://guides.github.com/introduction/git-handbook/).