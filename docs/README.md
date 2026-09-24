## KnownFolders.h from the Windows SDK


The [Known Folder Table on MSDN](https://learn.microsoft.com/en-us/windows/win32/shell/knownfolderid) shows 100+ vertical tables of 7 items (Constant, Display Name, Folder Type, Default Path, CSIDL Equivalent, Legacy Display Name, Legacy Default Path)) for each of the 100+ Folder ID's. That can be viewed here in a [single  markdown table transposed](MsdnKnownFoldFormatted.md) with some help from Gemini.

[KnownFolders.h](KnownFolders_SDK_81.h) defines the ID's for use with this kind of code on 2 lines with a `\\comment` then macro with the GUID:

```cpp
// {D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}
DEFINE_KNOWN_FOLDER(FOLDERID_NetworkFolder, 0xD20BEEC4, 0x5CA8, 0x4905, 0xAE, 0x3B, 0xBF, 0x25, 0x1E, 0xA0, 0x9B, 0x53);

// {0AC0837C-BBF8-452A-850D-79D08E667CA7}
DEFINE_KNOWN_FOLDER(FOLDERID_ComputerFolder,   0x0AC0837C, 0xBBF8, 0x452A, 0x85, 0x0D, 0x79, 0xD0, 0x8E, 0x66, 0x7C, 0xA7);
```
 To make that easier to review the [KnownFolders_ID_Guid.md](KnownFolders_ID_Guid.md) markdown file organizes that into a single row.

Finnaly check out the mapping of the old CSIDL to Known Folders (and the opposite) made by Gemini theh editted in [CSIDL_to_KnownFolders.md](CSIDL_to_KnownFolders.md)

