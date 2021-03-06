# F# .NET Core MonoGame template with CoreRT

A very basic, running MonoGame starter, using F#, .NET Core and CoreRT. These three things are not standard for MonoGame, so figuring out how to combine them requires a bit of research across a few sources. Here is the result.

Tested on windows 10 only, but there is nothing windows specific so in theory should be fine on Linux/OSX. In order to run you need the .NET Core SDK (2.0+). To compile the CoreRT executable, on windows you need the C++ linker; one of the ways in which this can be obtained is by installing VS Community and specifying C++ dev and/or the Win 10 SDK. Trying to compile on other platforms will result in CoreRT providing instructions on what you need - issues with CoreRT should be investigated with them (https://github.com/dotnet/corert)

The command to build the exe on windows is 'dotnet publish -r win-x64'; Note the win-x64 as opposed to win10-x64: the latter at time of writing causes CoreRT to fail with an unfixable message.
