# Install Dependencies

The design of Scenic goes to great lengths to minimize its dependencies to just
the minimum. Namely, it needs Erlang/Elixir and OpenGL.

Rendering your application into a window on your local computer (MacOS, Ubuntu
and others) is done by the
[`scenic_driver_local`](https://github.com/ScenicFramework/scenic_driver_local)
driver. It uses the GLFW and GLEW libraries to connect to OpenGL.

The instructions below assume you have already installed Elixir/Erlang. If you
need to install Elixir/Erlang there are instructions on the [elixir-lang
website](https://elixir-lang.org/install.html).

## On MacOS

The easiest way to install on MacOS is to use Homebrew. Just run the following
in a terminal:

```bash
brew update
brew install glfw3 glew pkg-config
```

Once these components have been installed, you should be able to build the
`scenic_driver_local` driver.

## On Windows

Some initial setup is required for windows. You'll need windows services for
linux (WSL) and VcXsrv, [Jeffrey Borchert's article details these
steps.](https://medium.com/@jeffborch/running-the-scenic-elixir-gui-framework-on-windows-10-using-wsl-f9c01fd276f6)

## On Ubuntu 24

The easiest way to install on Ubuntu is to use apt-get. Just run the following:

```bash
sudo apt-get update
sudo apt-get install pkgconf libgtk-3-0 libgtk-3-dev libsystemd-dev libwebp-dev libzstd-dev
```

Once these components have been installed, you should be able to build the
`scenic_driver_local` driver.

## On Fedora

The easiest way to install on Fedora is to use dnf. Just run the following:

```bash
dnf install glfw glfw-devel pkgconf glew glew-devel
```

Once these components have been installed, you should be able to build the
`scenic_driver_glfw` driver.

## On Archlinux

The easiest way to install on Archlinux is to use pacman. Just run the
following:

```bash
sudo pacman -S glfw-x11 glew
```

If you're using wayland, you'll probably need `glfw-wayland` instead of
`glfw-x11` and `glew-wayland` instead of `glew`

## What to read next?

Next, you should read about [General Overview](overview_general.html).
