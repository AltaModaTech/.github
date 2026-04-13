# AltaModaTech Journal

## 04/12/2026

- Abandoned AMT.Extensions.System.IO in netcore-extensions.
  - .NET's System.IO is too rigid for multi-platform
    - Doesn't support filesystem concept, maybe due to history of being tied to NTFS/Windows.
    - Extending is not a problem, but testing across multiple platforms (filesytems) inverts cost:benefit.
  - TestableIO/Testably, a replacement to System.IO
    - supports filesystems (including mock filesystems)
    - but doesn't play well with extensions for System.IO (API matches, but extensions must be TestableIO/Testably types)
