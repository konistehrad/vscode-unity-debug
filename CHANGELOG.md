# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Security

- Updated npm package versions.

### Changed

- Updated LICENSE and CHANGELOG.

## [3.0.11]

- Attempt to fix error during processing `stackTrace` (<https://github.com/Unity-Technologies/vscode-unity-debug/issues/183>)

## [3.0.10]

- Fix launch.json creation when there is no configuration (<https://github.com/Unity-Technologies/vscode-unity-debug/issues/194>)

## [3.0.9]

- Fix extension entry point after moving to webpack

## [3.0.8]

- Use webpack to bundle extension

## [3.0.7]

- Fix Changelog not appearing in the extension

## [3.0.6]

- Attempt to fix "Could not find target name ..." for specific cases (<https://github.com/Unity-Technologies/vscode-unity-debug/issues/193>)

## [3.0.5]

- Attempt to fix path issue on Linux (<https://github.com/Unity-Technologies/vscode-unity-debug/issues/195>)

## [3.0.4]

- Minor changes in exception handling to track down <https://github.com/Unity-Technologies/vscode-unity-debug/issues/183>
- More graceful debugger stop by supporting `terminate` request

## [3.0.3]

- Activate extension only on specific events

## [3.0.2]

- Update vscode dependencies

## [3.0.1]

- Improve stability with latest VS Code

## [3.0.0]

- Update debugger libraries. Fixes added Roslyn to evaluate certain expressions sent to the debugger.

## [2.7.0]

- Update debugger libs. This patch includes sending the absolute file path to the debugger agent on native.

## [2.6.7]

- Fix launch settings configuration through resolve.

## [2.6.6]

- Fix duplicate line removing breakpoints.

## [2.6.5]

- Initialize commands on vs code start up time.

## [2.6.4]

- Improve attaching to unity processes. Added support for PS4, Xbox One, and Switch.

## [2.6.3]

- Fix regression within attach unity debugger. This is necessary when EditorInstance.json does not exist.

## [2.6.2]

- Missing EditorInstance.json file will no longer crash the program, instead it will terminated and report steps the user should take.

## [2.6.1]

- Updated debugger-libs to stop hovering from stack overflowing, due to miss use of NRefactory.

## [2.6.0]

- Multithreaded stack trace unwrapping is now enabled. Making it possible to switch context.

## [2.5.0]

- New support for halt on exception. In debug view a list of exceptions control which to break on.

## [2.4.2]

- Added support for Library/EditorInstance.json. The correct process is attached and multiple editors are running.

## [2.4.1]

- Fix modification exception when setting breakpoints.

## [2.4.0]

- Added support for attaching individual unity processes by use of commands.

## [2.3.0]

- Added support for conditional breakpoints.

## [2.2.0]

- Added support for setValue. This makes it possible to modify variables at runtime.

## [2.1.0]

- Added support for circumventing string truncation by disabling ellipsing on strings in watch field.

## [2.0.1]

- Fix duplicate key exception when assigning breakpoints.

## [2.0.0]

- Updated packages to support .NET 4.6 runtime in Unity.
- Fix issue with being able to detach from Unity, which would cause the Unity Editor to hang.
- Various instabilities fixes, such as LINQ debugging for .NET 4.6 runtime, hovering variables, complex class debugging etc.

## [1.3.0]

- Fix "Error: command 'vscode.startDebug' not found" error when using "Unity Attach Debugger" command.
- Fix issue with being unable to attach to Unity Editor because of "UnityCrashHandler64" and "Unity Hub" processes.

## [1.2.1]

- Fix issue with "Unity Attach Debugger" not working due to missing attach.js file.

## [1.2.0]

- Add support for hovering on variables. Patch contributed by JohnPoison.
- Update debugger client library to latest version. Fixes debugging issues in Unity 5.5 and above.
- Fix issue with not being able to attach if unityiproxy (Unity Remote) process is running.
- Added MIT LICENSE.txt

## [1.1.0]

- Added "Unity Attach Debugger" to command palette. Patch contributed by Dominick.
- Fixed issue with being unable to attach to Linux Player.

## [1.0.4]

- Fixed issue with case sensitive path compare.
  (<https://github.com/Unity-Technologies/vscode-unity-debug/issues/14>)

## [1.0.3]

- Improved logging when multiple Unity processes are found.

## [1.0.2]

- Improved support for expressions added with "Add Watch"

- Fixed issue with being unable to attach to Unity editor on Ubuntu, when
  using Unity graphical shell.

- Attaching to the Unity Editor is faster.

- Update debugger protocol to latest version.

## [1.0.1]

- Fixed issue with using "Add Watch" not generating valid expressions.

## [1.0.0]

- Fixed issue with being unable to add a watch.

## [0.5.0]

- Added support for attaching to Windows, OSX, Linux, Android and iOS players

- Added log file
  OSX/Linux: ${HOME}/.vscode/extensions/Unity.unity-debug-x.y.z/bin/UnityDebug-log.txt
  Windows: %USERPROFILE%\.vscode\extensions\Unity.unity-debug-x.y.z\bin\UnityDebug-log.txt

- Fix issue with "unity" being marked as unknown "type" in launch.json

## [0.1.0]

- Initial release.
- Only attaching to Unity editor is supported.
