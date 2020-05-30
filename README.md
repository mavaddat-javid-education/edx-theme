### How to install a theme

In order to install a theme to your Open edX you need to do the
following:

1.  Choose a theme and copy-paste its branch name. You are going to put
    theme branch name into the script.

2.  Go to your Open edX server via WSL2 or SSH. Make sure you
    use fullstack version. 

3.  Run the script 

4.  Enjoy the new awesome look of your Open edX 😎

Everything else the script will do for you.

#### Now let's do it step by step.

------------------------------------------------------------------------

##### <a name="#step-1"></a>Step \#1

Choose a theme. You can try the themes on the @raccoongang 
[themex.io](https://themex.io/) page. Or you can find the available themes
and their Open edX version from the list below:

-   Open edX Dogwood fullstack version

    -   [Marvel](https://themex.io/theme/marvel/)
        - `marvel-theme-dogwood`

    -   [Marvel Yellow](https://themex.io/theme/marvel-yellow/)
        - `marvel-yellow-theme-dogwood`

    -   [Marvel Blue](https://themex.io/theme/marvel-blue/)
        - `marvel-blue-theme-dogwood`

-   Open edX Eucalyptus fullstack version

    -   [Marvel](https://themex.io/theme/marvel/)
        - `marvel-theme-eucalyptus`

    -   [Marvel Yellow](https://themex.io/theme/marvel-yellow/)
        - `marvel-yellow-theme-eucalyptus`

    -   [Marvel Blue](https://themex.io/theme/marvel-blue/)
        - `marvel-blue-theme-eucalyptus`

##### <a name="#step-2"></a>Step \#2

Open [WSL2](https://github.com/microsoft/WSL2-Linux-Kernel) shell and start your local Open edX instance. For example, when using  @Docker for [Windows](https://docs.docker.com/docker-for-windows/wsl/) and [Tutor](https://github.com/overhangio/tutor) by @OverhangIO, you can start the system by `tutor local start`

If you need to connect remotely (pretend server resides at `edx-marvel.raccoongang.com` and you can connect username `ubuntu`), open Terminal and go to your Open edX server via SSH by running a
command:  `ssh ubuntu@edx-marvel.raccoongang.com`


### <a name="#step-3"></a>Step \#3

Assuming you chose the theme branch `marvel-yellow-theme-eucalyptus` in [Step \#1](#step1), run these commands one by one:

`git clone https://github.com/mavaddat-javid-education/edx-theme.git`

`cd edx-theme`

`./update_theme.sh marvel-yellow-theme-eucalyptus`

### <a name="#step-4"></a>[Step \#4]

Now's the time to enjoy! Go and check how awesome your Open edX looks like. Please feel free to customize your
theme.

------------------------------------------------------------------------

Please note:  Your edx-platform repository
should not have any uncommitted changes for updating a theme. 

### How to compile SASS:

 1. Start build platform static `paver devstack lms`
 2. Go to theme folder `ficus/themes/edx-theme/`
 3. For start local compile sass run command `sh static-compile.sh start`
 4. For end local compile sass and remove time files run command `sh static-compile.sh stop`
