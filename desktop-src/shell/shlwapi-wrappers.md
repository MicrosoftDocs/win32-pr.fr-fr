---
description: les tables de ce document contiennent des fonctions de wrapper de Shlwapi.dll qui fournissent des fonctionnalités Unicode limitées à Windows 95, Windows 98 et Windows millennium edition (Windows Me).
title: Fonctions de wrapper SHLWAPI
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3c428c89-b650-48c1-9f91-b94f9f8e10e2
api_name:
- SHLWAPI Wrapper Functions
- AppendMenuWrapW
- CallWindowProcWrapW
- CharLowerWrapW
- CharUpperBufWrapW
- CharUpperWrapW
- CompareStringWrapW
- CopyFileWrapW
- CreateEventWrapW
- CreateFileWrapW
- CreateWindowExWrapW
- DefWindowProcWrapW
- DeleteFileWrapW
- DialogBoxParamWrapW
- DispatchMessageWrapW
- DragQueryFileWrapW
- DrawTextExWrapW
- DrawTextWrapW
- ExtTextOutWrapW
- FormatMessageWrapW
- GetClassInfoWrapW
- GetDateFormatW
- GetDateFormatWrapW
- GetDlgItemTextWrapW
- GetFileAttributesWrapW
- GetLocaleInfoWrapW
- GetMenuItemInfoWrapW
- GetModuleFileNameWrapW
- GetModuleHandleWrapW
- GetObjectWrapW
- GetOpenFileNameWrapW
- GetSaveFileNameWrapW
- GetSystemDirectoryWrapW
- GetTimeFormatWrapW
- GetWindowLongWrapW
- GetWindowsDirectoryWrapW
- GetWindowTextLengthWrapW
- GetWindowTextWrapW
- InsertMenuItemWrapW
- IsCharAlphaNumericWrapW
- IsCharAlphaWrapW
- IsCharUpperWrapW
- LoadLibraryWrapW
- LoadStringWrapW
- MessageBoxWrapW
- MLGetUILanguage
- MoveFileWrapW
- OutputDebugStringWrapW
- PeekMessageWrapW
- PostMessageWrapW
- RegCreateKeyExWrapW
- RegisterClassWrapW
- RegOpenKeyExWrapW
- RegQueryValueExW
- RegQueryValueExWrapW
- RegQueryValueWrapW
- RegSetValueExWrapW
- SendMessageWrapW
- SetDlgItemTextWrapW
- SetWindowLongWrapW
- SetWindowTextWrapW
- SHCancelTimerQueueTimer
- SHDeleteTimerQueue
- ShellExecuteExWrapW
- ShellMessageBoxWrapW
- SHGetFileInfoWrapW
- SHGetPathFromIDListWrapW
- SHInterlockedCompareExchange
- SHQueueUserWorkItem
- SHSetTimerQueueTimer
- TranslateAcceleratorWrapW
- UnregisterClassWrapW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2841148c5907375fd653c57a38638b49319ec8fc8ed7bedc121895d142a02736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047091"
---
# <a name="shlwapi-wrapper-functions"></a>Fonctions de wrapper SHLWAPI

\[ces fonctions sont disponibles via Windows XP Service Pack 2 (SP2) et Windows Server 2003. Ils peuvent être modifiés ou non disponibles dans les versions ultérieures de Windows.\]

les tables de ce document contiennent des fonctions de wrapper de Shlwapi.dll qui fournissent des fonctionnalités Unicode limitées à Windows 95, Windows 98 et Windows millennium edition (Windows Me).

Windows 95, Windows 98 et Windows Millennium edition (Windows Me) sont désignés ici comme « plateformes ANSI natives ». Sur les plateformes ANSI natives, ces fonctions wrapper convertissent les paramètres de chaîne d’entrée Unicode en ANSI et appellent les versions ANSI des fonctions dans la colonne **transferts vers** . Par exemple, **AppendMenuWrapW** appelle **AppendMenuA**, qui est la version ANSI de [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Les autres fonctions suivent le même modèle. Toute chaîne retournée par la fonction ANSI est convertie en Unicode et retournée à l’application appelante. Hormis les exceptions notées dans la colonne **Remarques** , la fonction wrapper a la même syntaxe et fournit les mêmes fonctionnalités que la fonction dans la colonne **transférer vers** . Pour plus d’informations sur l’utilisation, reportez-vous à cette page de référence.

**Avertissement de sécurité :** Plusieurs chaînes Unicode peuvent être converties en une même chaîne ANSI. Des collisions inattendues après la conversion peuvent entraîner un comportement inattendu. Par exemple, si **CreateEventWrapW** est utilisé pour créer deux événements de nom différent dont les noms correspondent après la conversion d’Unicode en ANSI, le deuxième appel renverra un handle au même événement que le premier appel, même si les chaînes Unicode d’origine étaient différentes.

les systèmes d’exploitation Microsoft Windows NT, Windows 2000, Windows XP, Windows Server 2003 et versions ultérieures sont appelés « plateformes Unicode natives ». Pour l’essentiel, sur les plateformes Unicode natives, ces fonctions wrapper transfèrent simplement des paramètres de chaîne d’entrée à la version Unicode de la fonction dans la colonne **forwards to** . Par exemple, **AppendMenuWrapW** est transféré à **AppendMenuW**, qui est la version Unicode de [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Les autres fonctions suivent le même modèle. Toutes les chaînes retournées par la fonction Unicode sont retournées à l’application appelante. Hormis les exceptions notées dans la colonne **Remarques** , la fonction wrapper a la même syntaxe et fournit les mêmes fonctionnalités que la fonction dans la colonne **transférer vers** . Pour plus d’informations sur l’utilisation, reportez-vous à cette page de référence.

**Avertissement de sécurité :** Les problèmes de sécurité signalés pour les fonctions de la colonne **transferts vers** s’appliquent également aux fonctions wrapper correspondantes. Pour plus d’informations, consultez la documentation de référence pour la fonction dans la colonne **transfert vers** .

Les fonctions wrapper dans ce tableau sont toutes contenues dans Shlwapi.dll. Pour les appeler, vous devez utiliser l’ordinal indiqué dans le tableau.

> [!Note]  
> ces fonctions wrapper sont disponibles sur Windows xp, mais ne fournissent pas de fonctionnalité de wrapper dans Windows xp Service Pack 2 (SP2) et versions ultérieures. ils ne fournissent pas non plus de fonctionnalité de wrapper dans Windows Server 2003. Vous devez utiliser les fonctions indiquées dans la colonne **transférer vers à** la place.

 



| Fonction                  | Ordinal | Transférer à                                             | DLL      | Remarques                                                                                                                             |
|---------------------------|---------|---------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| AppendMenuWrapW           | 36      | [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)                     | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(menu)](#menu)                                                           |
| CallWindowProcWrapW       | 37      | [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)             | USER32   | [cliqu](#shlwapi-wrapper-functions)                                                                                                   |
| CharLowerWrapW            | 38      | [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)                       | KERNEL32 | [Envoyer](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperBufWrapW         | 44      | [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)               | KERNEL32 | [Envoyer](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperWrapW            | 43      | [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)                       | KERNEL32 | [Envoyer](#shlwapi-wrapper-functions)                                                                                                   |
| CompareStringWrapW        | 45      | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                 | KERNEL32 | [CompareString](#comparestring)                                                                                                   |
| CopyFileWrapW             | 112     | [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateEventWrapW          | 51      | [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)                     | KERNEL32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| CreateFileWrapW           | 52      | [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateWindowExWrapW       | 55      | [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)             | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| DefWindowProcWrapW        | 56      | [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)               | USER32   | [cliqu](#shlwapi-wrapper-functions)                                                                                                   |
| DeleteFileWrapW           | 57      | [**DeleteFile**](/windows/win32/api/fileapi/nf-fileapi-deletefilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| DialogBoxParamWrapW       | 59      | [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)             | USER32   | [(f)](#dragqueryfile), [(i)](#shlwapi-wrapper-functions), [(DialogBoxParam)](#dialogboxparam)                                       |
| DispatchMessageWrapW      | 60      | [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)           | USER32   | [cliqu](#shlwapi-wrapper-functions)                                                                                                   |
| DragQueryFileWrapW        | 318     | [**DragQueryFile**](/windows/win32/api/Shellapi/nf-shellapi-dragqueryfilea)                  | SHELL32  | [(b)](#dialogboxparam), [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DragQueryFile)](#dragqueryfile)               |
| DrawTextExWrapW           | 301     | [**DrawTextEx**](/windows/win32/api/winuser/nf-winuser-drawtextexa)                        | USER32   | [(a)](#shlwapi-wrapper-functions), [(d)](#shlwapi-wrapper-functions)                                                                |
| DrawTextWrapW             | 61      | [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)                            | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| ExtTextOutWrapW           | 299     | [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)                        | GDI32    | [(d)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(ExtTextOut)](#exttextout)                                               |
| FormatMessageWrapW        | 68      | [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(FormatMessage)](#formatmessage)                                       |
| GetClassInfoWrapW         | 69      | [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)                 | USER32   | [GetClassinfo](#getclassinfo)                                                                                                     |
| GetDateFormatWrapW        | 311     | [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetDlgItemTextWrapW       | 74      | [**GetDlgItemText**](/windows/win32/api/winuser/nf-winuser-getdlgitemtexta)             | USER32   | [activée](#compareexchange)                                                                                                             |
| GetFileAttributesWrapW    | 75      | [**GetFileAttributes**](/windows/win32/api/fileapi/nf-fileapi-getfileattributesa)           | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| GetLocaleInfoWrapW        | 77      | [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)                 | KERNEL32 | [activée](#compareexchange)                                                                                                             |
| GetMenuItemInfoWrapW      | 302     | [**GetMenuItemInfo**](/windows/win32/api/winuser/nf-winuser-getmenuiteminfoa)           | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange), [(MenuItemInfo)](#menuiteminfo)                                                     |
| GetModuleFileNameWrapW    | 80      | [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)         | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetModuleHandleWrapW      | 83      | [**Échec GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)             | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetObjectWrapW            | 84      | [**GetObject**](/windows/win32/api/wingdi/nf-wingdi-getobject)                          | GDI32    | [activée](#compareexchange)                                                                                                             |
| GetOpenFileNameWrapW      | 403     | [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OpenFileName)](#openfilename)                 |
| GetSaveFileNameWrapW      | 389     | [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OpenFileName)](#openfilename)                 |
| GetSystemDirectoryWrapW   | 81      | [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)       | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetTimeFormatWrapW        | 310     | [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetWindowLongWrapW        | 94      | [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| GetWindowsDirectoryWrapW  | 97      | [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)     | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetWindowTextLengthWrapW  | 96      | [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)   | USER32   | [j](#j)                                                                                                                           |
| GetWindowTextWrapW        | 95      | [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)               | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange)                                                                                      |
| InsertMenuItemWrapW       | 98      | [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema)             | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(menu)](#menu), [(MenuItemInfo)](#menuiteminfo)                          |
| IsCharAlphaWrapW          | 25      | [**IsCharAlpha**](/windows/win32/api/winuser/nf-winuser-ischaralphaa)                   | USER32   | [Envoyer](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharAlphaNumericWrapW   | 28      | [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)     | KERNEL32 | [Envoyer](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharUpperWrapW          | 26      | [**IsCharUpper**](/windows/win32/api/winuser/nf-winuser-ischaruppera)                   | USER32   | [Envoyer](#shlwapi-wrapper-functions)                                                                                                   |
| LoadLibraryWrapW          | 105     | [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                     | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| LoadStringWrapW           | 107     | [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)                     | KERNEL32 | [Envoyer](#shlwapi-wrapper-functions)                                                                                                   |
| MessageBoxWrapW           | 340     | [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)                     | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| MoveFileWrapW             | 113     | [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| OutputDebugStringWrapW    | 115     | [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)         | KERNEL32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| PeekMessageWrapW          | 116     | [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)                   | USER32   | [(PeekMessage et PostMessage)](#peekmessage-and-postmessage)                                                                       |
| PostMessageWrapW          | 117     | [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)                   | USER32   | [(PeekMessage et PostMessage)](#peekmessage-and-postmessage)                                                                       |
| RegCreateKeyExWrapW       | 120     | [**RegCreateKeyEx**](/windows/win32/api/winreg/nf-winreg-regcreatekeyexa)               | ADVAPI32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| RegisterClassWrapW        | 131     | [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)               | USER32   | [(a)](#shlwapi-wrapper-functions), [(registerClass)](#registerclass)                                                                |
| RegOpenKeyExWrapW         | 125     | [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)                   | ADVAPI32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| RegQueryValueExWrapW      | 128     | [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa)             | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(ValueEx)](#regqueryvalueexw), [(RegQueryValueExW)](#regqueryvalueexw) |
| RegQueryValueWrapW        | 127     | [**RegQueryValue**](/windows/win32/api/winreg/nf-winreg-regqueryvaluea)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| RegSetValueExWrapW        | 130     | [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvalueexa)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(ValueEx)](#regqueryvalueexw)                                                                   |
| SendMessageWrapW          | 136     | [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)                   | USER32   | [SendMessage](#sendmessage)                                                                                                       |
| SetDlgItemTextWrapW       | 138     | [**SetDlgItemText**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)             | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| SetWindowLongWrapW        | 141     | [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| SetWindowTextWrapW        | 143     | [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)               | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| ShellExecuteExWrapW       | 35      | [**ShellExecuteEx**](/windows/win32/api/Shellapi/nf-shellapi-shellexecuteexa)                | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(ShellExecuteEx)](#shellexecuteex)                                      |
| ShellMessageBoxWrapW      | 388     | [**ShellMessageBox**](/windows/win32/api/Shellapi/nf-shellapi-shellmessageboxa)              | SHLWAPI  | [(a)](#shlwapi-wrapper-functions), [(FormatMessage)](#formatmessage)                                                                |
| SHGetFileInfoWrapW        | 313     | [**SHGetFileInfo**](/windows/win32/api/Shellapi/nf-shellapi-shgetfileinfoa)                  | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange)                                                  |
| SHGetPathFromIDListWrapW  | 334     | [**SHGetPathFromIDList**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)      | USER32   | [activée](#compareexchange)                                                                                                             |
| TranslateAcceleratorWrapW | 146     | [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) | USER32   | [cliqu](#shlwapi-wrapper-functions)                                                                                                   |
| UnregisterClassWrapW      | 147     | [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)           | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |



 

Les fonctions wrapper dans le tableau suivant n’effectuent pas de conversion de jeu de caractères. Au lieu de cela, ils offrent une prise en charge limitée des fonctionnalités du système d’exploitation qui ne sont pas disponibles sur les plateformes précédentes.



| Fonction                     | Ordinal | Transférer à                                                                     | DLL      | Remarques                                                                        |
|------------------------------|---------|---------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------|
| MLGetUILanguage              | 376     | [**GetUserDefaultUILanguage**](/windows/win32/api/winnls/nf-winnls-getuserdefaultuilanguage)                   | KERNEL32 | [manutention](#shlwapi-wrapper-functions)                                              |
| SHCancelTimerQueueTimer      | 265     | [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)                         | KERNEL32 | [manutention](#shlwapi-wrapper-functions)                                              |
| SHDeleteTimerQueue           | 262     | [**DeleteTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue)                                   | KERNEL32 | [manutention](#shlwapi-wrapper-functions)                                              |
| SHInterlockedCompareExchange | 342     | [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) | KERNEL32 | [CompareExchange](#compareexchange)                                          |
| SHQueueUserWorkItem          | 260     | [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                                 | KERNEL32 | [(QueueUserWorkItem)](#queueuserworkitem), [(h)](#shlwapi-wrapper-functions)   |
| SHSetTimerQueueTimer         | 263     | [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)                         | KERNEL32 | [(SetTimerQueueTimer)](#settimerqueuetimer), [(h)](#shlwapi-wrapper-functions) |



 

## <a name="remarks"></a>Remarques

### <a name="a"></a>un

Si une conversion de chaîne est nécessaire, toutes les chaînes sont converties via la \_ page de codes CP ACP.

Ces fonctions utilisent les caractères les mieux adaptés et n’effectuent pas de vérification par défaut lors de la conversion d’Unicode en ANSI. En outre, si la chaîne ne peut pas être convertie d’Unicode en ANSI, la fonction wrapper passe une chaîne **null** à la fonction ANSI sous-jacente. Cela peut se produire, par exemple, lorsque la mémoire est insuffisante. Le passage d’une chaîne **null** peut entraîner l’échec de certaines fonctions avec une erreur de paramètre non valide, mais d’autres fonctions acceptent la chaîne **null** et la considèrent comme le paramètre prévu. Par exemple, une erreur se produit lorsque la fonction **CreateWindowExWrapW** tente de convertir le paramètre *lpWindowName* en ANSI, et que [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) crée une fenêtre avec une légende vide. Le wrapper ne vous avertit pas lorsque ces problèmes se sont produits.

La couche Microsoft pour Unicode (MSLU) recherche des erreurs lors de la conversion d’Unicode en ANSI et retourne les valeurs d’erreur appropriées. Par exemple, la fonction wrapper [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) dans le MSLU retourne 0 si l’élément n’a pas été correctement ajouté.

### <a name="b"></a>p

Ces fonctions utilisent un lien à chargement différé vers la fonction appropriée. Cela signifie que la DLL qui contient la fonction dans la colonne « Forwarders to » n’est pas chargée par le Shlwapi.dll jusqu’à ce qu’une fonction de cette DLL soit appelée. l’éditeur de liens Microsoft Visual C++ prend en charge cette fonctionnalité plus généralement via l’option/delayload.

### <a name="c"></a>secteur

Cette fonction manipule les noms de fichiers. Comme indiqué dans [(a)](#shlwapi-wrapper-functions), les fonctions convertissent toutes les chaînes via la \_ page de codes CP ACP. Ils ne vérifient pas si les fonctions d’e/s de fichier ont été définies en mode ANSI. Si les fonctions d’e/s de fichier sont en mode OEM, les chaînes sont converties vers et à partir d’un jeu de caractères incorrect. Une application peut définir explicitement les fonctions d’e/s de fichier en mode OEM en appelant la fonction [**SetFileApisToOEM**](/windows/win32/api/fileapi/nf-fileapi-setfileapistooem) .

* * Avertissement de sécurité : * * l’utilisation de ces fonctions wrapper pour les noms de fichiers peut compromettre la sécurité de votre application. Étant donné qu’aucune vérification par défaut n’est effectuée et que les caractères les mieux adaptés sont utilisés, les caractères de nom de fichier peuvent être convertis de manière inattendue. Cela peut entraîner des attaques d’usurpation du système de fichiers. En outre, une perte de données silencieuse peut se produire lors de la conversion d’Unicode en ANSI.

Le MSLU n’a pas ces limitations.

### <a name="d"></a>e

Si la chaîne en cours de dessin requiert un jeu de caractères qui n’est pas disponible dans la police sélectionnée dans le contexte de périphérique, ces fonctions wrapper utilisent la fonctionnalité de [liaison de police](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767872(v=vs.85)) de la bibliothèque [mlang](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767865(v=vs.85)) pour restituer chaque caractère dans une police appropriée. Contrairement à la plupart des autres fonctions wrapper, celles-ci sont fonctionnelles sur Microsoft Windows NT 4,0 en plus des plateformes ANSI natives.

### <a name="e"></a>Envoyer

Les implémentations Unicode complètes de ces fonctions sont disponibles sur les plateformes ANSI native. Ces fonctions n’appellent pas la fonction ANSI associée.

### <a name="f"></a>FA

Si la langue de l’interface utilisateur par défaut de l’utilisateur utilise un autre jeu de caractères que la langue de l’interface utilisateur par défaut du système, le système tente de réécrire les contrôles des modèles et des sous-classes de boîtes de dialogue et de convertir les éléments de menu en owner-draw, afin que les chaînes de la langue de l’interface utilisateur par défaut continuent à s’afficher correctement Les seuls contrôles pris en charge par les règles de réécriture du modèle de boîte de dialogue sont les contrôles static, Button, ListBox et ComboBox. Ces contrôles sont sous-classés de sorte que la fonction **SendMessageWrapW** peut obtenir la chaîne Unicode d’origine sans être traduite par le jeu de caractères ANSI. Contrairement à la plupart des autres fonctions wrapper, celles-ci sont fonctionnelles sur Microsoft Windows NT 4,0 et les plateformes ANSI natives. Consultez les notes dans la documentation de la fonction [**MLLoadLibrary**](./callbacks.md) pour plus d’informations sur la façon dont la langue de l’interface utilisateur par défaut de l’utilisateur et la langue de l’interface utilisateur par défaut du système sont déterminées.

### <a name="g"></a>activée

Si une conversion de chaîne est nécessaire, toutes les chaînes sont converties via la \_ page de codes CP ACP.

Lors de la conversion d’ANSI en Unicode pour la sortie, si la chaîne retournée ne tient pas dans la mémoire tampon qui a été fournie, les fonctions wrapper tronquent la chaîne. Les fonctions qui retournent le nombre de caractères copiés dans la mémoire tampon ou le nombre de caractères nécessaires pour éviter la troncation ne retournent pas le nombre de caractères Unicode copiés dans la mémoire tampon fournie par ou requis par l’appelant de la fonction wrapper. Elles retournent le nombre de caractères ANSI copiés dans la mémoire tampon ou requis par la fonction ANSI sous-jacente. Le MSLU n’a pas ces limitations.

### <a name="h"></a>manutention

sur les systèmes antérieurs à Windows XP, ces fonctions implémentent un pool de threads simplifié et une file d’attente du minuteur. sur Windows XP et versions ultérieures, ces fonctions utilisent le pool de threads système et la file d’attente du minuteur système. Pour les fonctions de file d’attente du minuteur, le paramètre *hQueue* doit avoir la valeur **null** pour indiquer que l’opération doit être effectuée sur la file d’attente du minuteur par défaut.

### <a name="i"></a>cliqu

Sur les plateformes Unicode, ces fonctions traduisent le message Unicode en ANSI si la fenêtre de destination est ANSI. Ces fonctions n’effectuent pas de traduction de message sur les plateformes ANSI natives. Par conséquent, l’appel d’applications qui appellent cette fonction doit garantir que le message est au format Unicode sur les plateformes Unicode et au format ANSI sur les plateformes ANSI. Par exemple, dans l’appel de fonction suivant, *wParam* doit être un point de code Unicode si le programme s’exécute sur une plateforme Unicode et doit être un caractère ANSI si le programme s’exécute sur une plateforme ANSI.

``` syntax
CallWindowProcWrapW(prevWndProc, hwnd, WM_CHAR, wParam, lParam);
```

Le MSLU suit le jeu de caractères de la procédure de fenêtre de destination et convertit le message en fonction des besoins.

### <a name="j"></a>j

Sur les plateformes ANSI, ces fonctions retournent la longueur de la chaîne ANSI sous-jacente, et non la longueur de la chaîne Unicode convertie. Le MSLU n’a pas ces limitations.

### <a name="compareexchange"></a>CompareExchange

La syntaxe de **SHInterlockedCompareExchange** est légèrement différente de celle de [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer), mais elle fonctionne de façon identique.

``` syntax
void* SHInterlockedCompareExchange(void **ppDest, void *pExch, void *pComp);
```

### <a name="comparestring"></a>CompareString

N’oubliez pas que sur les plateformes ANSI natives, les deux chaînes sont converties en ANSI et comparées en tant que chaînes ANSI. Si les chaînes Unicode contiennent des caractères qui ne peuvent pas être représentés en ANSI, les résultats peuvent être inattendus. Par exemple, si la page de codes ANSI par défaut ne prend pas en charge les caractères CJK, les chaînes L « \\ x66F0 » et l « \\ x6708 » sont considérées comme égales sur les plateformes ANSI natives, car elles sont toutes deux mappées à la chaîne ANSI «  ? ».

### <a name="datetime"></a>(DateTime)

sur Shlwapi.dll version 5,0, fournie avec Windows 2000, la page de codes de l’identificateur de paramètres régionaux que vous transmettez comme premier paramètre de **GetDateFormatWrapW** et de **GetTimeFormatWrapW** doit correspondre à la page de codes ANSI actuelle. Dans le cas contraire, la chaîne retournée peut être convertie de manière incorrecte. Cette limitation ne s’applique pas à Shlwapi.dll versions 5,5 ou ultérieures. cela signifie que les systèmes Windows XP et versions ultérieures ne sont pas soumis à cette limitation. Le MSLU n’a pas cette limitation.

### <a name="dialogboxparam"></a>(DialogBoxParam)

Le paramètre *lpTemplateName* de la fonction **DialogBoxParamWrapW** ne peut pas être une chaîne. Il doit s’agir d’un nombre ordinal créé par la macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) . La procédure de dialogue spécifiée par le paramètre *lpDialogFunc* reçoit des messages ANSI sur les plateformes ANSI natives et les messages Unicode sur les plateformes Unicode natives. La procédure de dialogue doit être préparée à gérer les deux cas. Le MSLU n’a pas ces limitations.

### <a name="exttextout"></a>(ExtTextOut)

Les plateformes ANSI natives implémentent la fonction [**ExtTextOutW**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) , ainsi que les plateformes Unicode natives. L’objectif de **ExtTextOutWrapW** est de procéder à la liaison des polices, comme décrit dans une remarque distincte.

### <a name="dragqueryfile"></a>(DragQueryFile)

La fonction **DragQueryFileWrapW** ne vous permet pas de rechercher la longueur d’un fichier dans la poignée de suppression en passant **null** comme paramètre *lpszFile* . Le MSLU n’a pas ces limitations.

### <a name="formatmessage"></a>FormatMessage

Sur les plateformes ANSI natives, les formats de la chaîne ne sont pas convertis de Unicode en ANSI. Par exemple, l’exemple de code suivant est erroné.


```
WCHAR szBuffer[MAX_PATH];
DWORD_PTR Arguments[2] = { L"String1", L"String2" };

FormatMessageWrapW(FORMAT_MESSAGE_FROM_STRING, 
               L"%1!s! %2", 
               0, 0, 
               szBuffer, 
               MAX_PATH, 
               (va_list*)Arguments);
```



Cet exemple de code utilise «  ! s ! » HH:MM:SS. Sur les plateformes ANSI natives, cette chaîne est transmise à la version ANSI de la fonction [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) . Par conséquent, une chaîne ANSI est attendue au lieu d’une chaîne Unicode. De même, le format « %2 » implique un argument de chaîne. Lorsqu’elle est transmise à la fonction ANSI **FormatMessage** , elle est interprétée comme une chaîne ANSI et non comme une chaîne Unicode. La chaîne de format correcte est L "%1 ! ws ! %2 ! WS !». Cela imprime les chaînes correctement sur les plateformes ANSI et Unicode.

La fonction ne prend pas en charge la chaîne de format spéciale "%0".

Le MSLU n’a pas ces limitations.

### <a name="getclassinfo"></a>GetClassinfo

Sur les plateformes ANSI natives, les membres **lpszMenuName** et **lpszClassName** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ne sont pas convertis en Unicode et ont toujours la valeur **null**. En outre, la procédure de fenêtre retournée dans le membre **lpfnWndProc** de la structure **WNDCLASS** n’est pas convertie en Unicode et fait référence à une procédure de fenêtre ANSI. Le MSLU n’a pas ces limitations.

### <a name="menu"></a>Menus

sur Shlwapi.dll version 5,0, fournie avec Windows 2000, les chaînes d’élément de menu qui contiennent des caractères de tabulation ( \\ t) peuvent ne pas s’afficher correctement. Cette limitation ne s’applique pas à Shlwapi.dll versions 5,5 ou ultérieures. cela signifie que les systèmes Windows XP et versions ultérieures ne sont pas soumis à cette limitation. Le MSLU n’a pas cette limitation.

### <a name="menuiteminfo"></a>MenuItemInfo

Cette fonction ne prend en charge que la version Microsoft Windows NT 4,0 de la structure [**MENUITEMINFOW**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Cette structure n’a pas de membre **hbmpItem** . En outre, la fonction ne prend pas en charge l' \_ indicateur miim bitmap. Le MSLU n’a pas ces limitations.

### <a name="openfilename"></a>OpenFileName

Le membre **cbSize** de la structure [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) doit avoir la valeur sizeof (OpenFileName \_ NT4W).

Le membre **lpstrCustomFilter** de la structure [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) doit avoir la valeur **null**.

Les valeurs des membres **nMaxFile** et **nMaxFileTitle** de la structure [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) ne doivent pas dépasser le \_ chemin d’accès maximal.

Si le membre **lpfnHook** de la structure [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) n’a pas la **valeur null**, il doit faire référence à une procédure de raccordement ANSI sur les plateformes ANSI native et une procédure de hook Unicode sur les plateformes Unicode natives.

Le MSLU n’a pas ces limitations.

### <a name="peekmessage-and-postmessage"></a>(PeekMessage et PostMessage)

Sur les plateformes ANSI natives, aucune traduction n’est effectuée sur le message transmis ou récupéré. Le message transmis/récupéré est ANSI sur les plateformes ANSI natives et Unicode sur les plateformes Unicode natives. L’application appelante doit être préparée à gérer les deux cas. Par exemple, si le message récupéré est WM \_ Char, le *wParam* est un code de caractère ANSI sur les plateformes ANSI native, mais il s’agit d’un point de code Unicode sur les plateformes Unicode natives. Le MSLU n’a pas ces limitations.

### <a name="queueuserworkitem"></a>QueueUserWorkItem

La fonction **SHQueueUserWorkItem** est légèrement différente de la fonction [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) correspondante. La syntaxe de **SHQueueUserWorkItem** est présentée ici.

``` syntax
BOOL SHQueueUserWorkItem(LPTHREAD_START_ROUTINE pfnCallback,
                     LPVOID pContext,
                     LONG lPriority,
                     DWORD_PTR dwTag,
                     DWORD_PTR * pdwId,
                     LPCSTR pszModule,
                     DWORD dwFlags);
```

Les paramètres doivent être définis comme suit :

-   Les paramètres *pfnCallback* et *pContext* ont les mêmes significations que les paramètres de *fonction* et de *contexte* , respectivement, de [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem).
-   Le paramètre *dwTag* est inutilisé et doit avoir la valeur 0.
-   Le paramètre *pdwld* est inutilisé et doit avoir la valeur **null**.
-   Le paramètre *pszModule* pointe vers une chaîne ANSI facultative se terminant par un caractère null qui spécifie le nom d’une bibliothèque à charger avant le début et le déchargement de l’élément de travail une fois l’élément de travail terminé. Ce paramètre peut être **NULL**.
-   Le paramètre *dwFlags* ne prend en charge qu’un sous-ensemble des valeurs prises en charge par [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem). Les indicateurs suivants sont reconnus.

    

    | Name              | Valeur      | Signification                          |
    |-------------------|------------|----------------------------------|
    | TPS \_ EXECUTEIO    | 0x00000001 | Identique à WT \_ EXECUTEINIOTHREAD.   |
    | TPS \_ LONGEXECTIME | 0x00000008 | Identique à WT \_ EXECUTELONGFUNCTION. |

    

     

    > [!Note]  
    > L' \_ indicateur LONGEXECTIME TPS n’a pas la même valeur numérique que l' \_ indicateur WT EXECUTELONGFUNCTION. Lors de l’utilisation de **SHQueueUserWorkItem**, le paramètre dwFlags doit être une combinaison de \_ \* valeurs TPS, et non de \_ \* valeurs WT.

     

**SHQueueUserWorkItem** retourne une valeur différente de zéro si l’élément de travail a été mis en file d’attente avec succès et 0 dans le cas contraire. Si la fonction échoue, vous pouvez utiliser [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir des informations supplémentaires.

### <a name="registerclass"></a>RegisterClass

Sur les plateformes ANSI natives, aucune traduction n’est effectuée sur le membre **lpfnWndProc** de la structure [**WNDCLASSW**](/windows/win32/api/winuser/ns-winuser-wndclassa) . La fenêtre reçoit les messages de fenêtre ANSI sur les plateformes ANSI natives et les messages de fenêtre Unicode sur les plateformes Unicode natives. La procédure de fenêtre doit être préparée pour gérer les deux cas. Le MSLU n’a pas ces limitations.

### <a name="regqueryvalueexw"></a>(RegQueryValueExW)

**RegQueryValueExWrapW** a également été appelé sous le nom **RegQueryValueExW**. Comme avec toute fonction sans nom exportée de façon stricte par ordinal, vous pouvez choisir le nom de la fonction dans votre code.

### <a name="sendmessage"></a>SendMessage

Sur les plates-formes Unicode natives, la fonction **SendMessageWrapW** est transférée à la fonction [**SendMessageW**](/windows/win32/api/winuser/nf-winuser-sendmessage) . Sur les plateformes ANSI natives, **SendMessageWrapW** offre une prise en charge limitée de la conversion des messages Unicode en ANSI. La liste des messages pris en charge est indiquée dans le tableau suivant. La fonction ne traduit pas les autres messages.

Le MSLU n’a pas ces limitations.



| Message              | Description                                                                                               |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| $ \_ ADDSTRING        | (b) (f) (c)                                                                                               |
| \_FindString CB       | (b) (f) (c)                                                                                               |
| \_FINDEXACTSTRING CB  | (a) (f) (c)                                                                                               |
| \_GETLBTEXT CB        | (b) (f) (c) (o) la mémoire tampon transmise dans le paramètre *lParam* doit avoir un espace pour au moins 256 caractères.   |
| \_GETLBTEXTLEN CB     | un                                                                                                       |
| \_INSERTSTRING CB     | (b) (f) (c)                                                                                               |
| \_SELECTSTRING CB     | (b) (f) (c)                                                                                               |
| \_CHARFROMPOS em      |                                                                                                           |
| \_GETLINE em          | (e) la valeur de retour est le nombre de caractères ANSI copiés.                                             |
| \_GETSEL em           |                                                                                                           |
| \_REPLACESEL em       | (b) (f)                                                                                                   |
| \_SETPASSWORDCHAR em  | un                                                                                                       |
| \_SETSEL em           |                                                                                                           |
| \_SETWORDBREAKPROC em | Ce message n’a aucun effet. La procédure d’arrêt de mot n’est pas définie.                                          |
| LB \_ ADDSTRING        | (b) (f) (d)                                                                                               |
| \_FindString lb       | (b) (f) (d)                                                                                               |
| \_FINDEXACTSTRING lb  | (b) (f) (lbs)                                                                                             |
| LB, \_ GETTEXT          | (b) (f) (lb) (o) la mémoire tampon transmise dans le paramètre *lParam* doit avoir un espace pour au moins 256 caractères. |
| \_GETTEXTLEN lb       | un                                                                                                       |
| \_INSERTSTRING lb     | (b) (f) (d)                                                                                               |
| \_SELECTSTRING lb     | (b) (f) (d)                                                                                               |
| WM \_ GETTEXT          | (b) (f)                                                                                                   |
| \_GETTEXTLENGTH WM    | un                                                                                                       |
| WM, \_ SETTEXT          | (b) (f)                                                                                                   |
| \_SETTINGCHANGE WM    | (a) le message est envoyé avec un délai d’expiration de trois secondes.                                                  |



 


-   (a) la chaîne ANSI en cours de mesure ou de récupération doit répondre à la condition suivante : la longueur de la version Unicode correspondante de la chaîne ne peut pas dépasser la longueur de la version ANSI de la chaîne. Si cette condition n’est pas remplie, la longueur retournée est short. Si la mémoire est insuffisante pour déterminer la longueur de la chaîne Unicode, la fonction retourne zéro, non LB \_ Err ou CB \_ Err comme prévu.
-   (b) si une conversion de chaîne est nécessaire, toutes les chaînes sont converties via la \_ page de codes CP ACP.

    Cette fonction utilise les caractères les mieux adaptés et n’effectue pas de vérification par défaut lors de la conversion d’Unicode en ANSI. En outre, si la chaîne ne peut pas être convertie d’Unicode en ANSI, la fonction passe une chaîne NULL à la fonction ANSI sous-jacente. Cela peut se produire, par exemple, lorsque la mémoire est insuffisante. Le passage d’une chaîne NULL peut entraîner l’échec de certaines fonctions avec une erreur de paramètre non valide, mais d’autres fonctions acceptent la chaîne NULL et la considèrent comme le paramètre prévu. Par exemple, si une erreur se produit lorsque le \_ Wrapper WM SETTEXT tente de convertir le titre de la fenêtre en ANSI, la fenêtre aura une légende vide. La fonction ne vous avertit pas lorsque ces problèmes se produisent. Le MSLU n’a pas ces limitations.

-   (c) le handle de fenêtre spécifié doit être le handle d’un contrôle [ComboBox](../controls/combo-boxes.md) ou [ComboBoxEx](../controls/comboboxex-controls.md) . Si le handle est un contrôle de zone de liste déroulante owner-draw et n’a pas été créé avec le style de style de [zone de liste](../controls/list-box-styles.md) , la traduction de ce message échoue et peut même se bloquer.
-   (d) le handle de fenêtre spécifié doit être le handle d’un contrôle ListBox. Si la zone de liste est owner-draw et n’a pas été créée avec le style de [styles de zone de liste](../controls/list-box-styles.md) , la traduction de ce message échoue et peut même se bloquer.
-   (e) si une conversion de chaîne est nécessaire, toutes les chaînes sont converties via la \_ page de codes CP ACP.

    Lors de la conversion d’ANSI en Unicode pour la sortie, les fonctions wrapper tronquent la chaîne retournée si elle ne tient pas dans la mémoire tampon fournie. La valeur de retour pour les fonctions qui retournent le nombre de caractères copiés dans la mémoire tampon ou le nombre de caractères nécessaires pour éviter la troncation fait référence au nombre de caractères ANSI copiés dans la mémoire tampon ou requis par la fonction ANSI sous-jacente, et non au nombre de caractères Unicode copiés dans la mémoire tampon fournie par ou requis par l’application appelante appelée. Le MSLU n’a pas cette limitation. pour plus d’informations, consultez [Microsoft Layer pour Unicode sur les systèmes Windows 95/98/Me](/previous-versions/ms812865(v=msdn.10)).

### <a name="settimerqueuetimer"></a>(SetTimerQueueTimer)

La fonction **SHSetTimerQueueTimer** est légèrement différente de la fonction [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) correspondante. Sa syntaxe est comme suit :

``` syntax
HANDLE SHSetTimerQueueTimer(HANDLE hQueue,
                        WAITORTIMERCALLBACK pfnCallback,
                        LPVOID pContext,
                        DWORD dwDueTime,
                        DWORD dwPeriod,
                        LPCSTR lpszLibrary,
                        DWORD dwFlags);
```

Les paramètres doivent être définis comme suit :

-   Le paramètre *hQueue* doit avoir la valeur **null**, ce qui spécifie la file d’attente du minuteur par défaut.
-   Les paramètres *pfnCallback*, *pContext*, *dwDueTime* et *dwPeriod* ont les mêmes significations que les paramètres de *rappel*, de *paramètre*, de *DueTime* et de *point* , respectivement, de [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).
-   Le paramètre *lpszLibrary* est inutilisé et doit avoir la valeur **null**.
-   Le paramètre *Flags* prend en charge uniquement un sous-ensemble des valeurs prises en charge par [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).

    

    | Name              | Valeur      | Signification                         |
    |-------------------|------------|---------------------------------|
    | TPS \_ EXECUTEIO    | 0x00000001 | Identique à WT \_ EXECUTEINIOTHREAD   |
    | TPS \_ LONGEXECTIME | 0x00000008 | Identique à WT \_ EXECUTELONGFUNCTION |

    

     

    > [!Note]  
    > L' \_ indicateur LONGEXECTIME TPS n’a pas la même valeur numérique que l' \_ indicateur WT EXECUTELONGFUNCTION. Lors de l’utilisation de **SHSetTimerQueueTimer**, le paramètre *dwFlags* doit être une combinaison de \_ \* valeurs TPS, et non de \_ \* valeurs WT.

     

**SHSetTimerQueueTimer** retourne le handle de la minuterie créée en cas de réussite et **null** dans le cas contraire.

### <a name="shellexecuteex"></a>(ShellExecuteEx)

Le membre **lpFile** de la structure [**SHELLEXECUTEINFO**](/windows/win32/api/Shellapi/ns-shellapi-shellexecuteinfoa) passé dans le seul paramètre de cette fonction ne peut pas dépasser la \_ longueur maximale des URL Internet \_ \_ . Si l' \_ indicateur voir Mask \_ className est omis, le membre **lpClass** doit être initialisé avec la **valeur null**.

### <a name="valueex"></a>(ValueEx)

Seuls les types de données de registre suivants sont pris en charge : REG \_ SZ, reg \_ expand \_ SZ, REG \_ Binary et reg \_ DWORD. Contrairement à ces fonctions wrapper, MSLU prend également en charge REG \_ multi \_ expand \_ sz.

### <a name="windowlong"></a>(WindowLong)

Sur les plateformes ANSI natives, la fonction n’effectue aucune conversion sur l’une des fenêtres de type long. Par exemple, si vous transmettez GWLP \_ WNDPROC, la fonction retourne la procédure de fenêtre ANSI, pas un thunk. Le MSLU n’a pas ces limitations.

 

 
