# Shaiya Episode 6

## Environment

Windows 10

Visual Studio 2022

C++ 23

## Prerequisites

[Microsoft Visual C++ Redistributable](https://aka.ms/vs/17/release/vc_redist.x86.exe)

## Injection

Cheat Engine isn't guaranteed to work for everyone. It's not an issue with the application or the libraries. The libraries have an export defined in the main headers.

## Data Execution Prevention (DEP)

Intermittent access violations have been reported on Windows Server 2022. The issue is related to [Data Execution Prevention](https://learn.microsoft.com/en-us/windows/win32/memory/data-execution-prevention). The following command will output the DEP support policy:

```
wmic OS Get DataExecutionPrevention_SupportPolicy
```

According to the [GetSystemDEPPolicy](https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-getsystemdeppolicy) documentation, Windows Server defaults to 3 (OptOut). The libraries will attempt to disable DEP for the process. Another option is to add the executable(s) to the exclusion list.

## Inspiration

[Cups](https://www.elitepvpers.com/forum/shaiya-pserver-guides-releases/4653021-shaiya-library.html)

[EricDutra-16](https://www.elitepvpers.com/forum/shaiya-pserver-guides-releases/4189218-release-wip-ep6-source-code.html)

[shen1l](https://www.elitepvpers.com/forum/shaiya-pserver-guides-releases/3669922-release-ep6-itemmall-fixed.html)

## References

[Eden](https://github.com/tristonplummer/Eden)

[Teos](https://github.com/ShaiyaTeos/Teos)

[Parsec](https://github.com/matigramirez/Parsec)

## Pull Requests

Pull requests are not welcome. GitHub doesn't allow the pull requests tab to be disabled.

## Configuration

### Episode 5.4

```cpp
// shaiya\include\common.h
//#define SHAIYA_EP6_4_PT
```

### Episode 6.4

```cpp
// shaiya\include\common.h
#define SHAIYA_EP6_4_PT
```
