---
title: Redirecteur de système de fichiers
description: Le \\ répertoire windir system32 est réservé aux applications 64 bits sur Windows 64 bits.
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- redirecteur du système de fichiers 64 bits, programmation Windows
- Guide de programmation Windows 64 bits-programmation Windows 64 bits, redirecteur de système de fichiers
- WOW64 64 bits Windows, redirecteur de système de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568ddde85d18f90b951051251774c3509081dfdd
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443630"
---
# <a name="file-system-redirector"></a>Redirecteur de système de fichiers

Le répertoire% windir% \\ system32 est réservé aux applications 64 bits sur Windows 64 bits. La plupart des noms de fichiers DLL n’ont pas été modifiés lors de la création de versions 64 bits des dll. par conséquent, les versions 32 bits des dll sont stockées dans un répertoire différent. WOW64 masque cette différence à l’aide d’un *redirecteur de système de fichiers*.

Dans la plupart des cas, chaque fois qu’une application 32 bits tente d’accéder à% windir% \\ system32,% windir% \\ LastGood \\ system32 ou% windir% \\regedit.exe, l’accès est redirigé vers un chemin d’accès spécifique à l’architecture.

> [!Note]  
> Ces chemins d’accès sont fournis à des fins de référence uniquement. Pour des fins de compatibilité, les applications ne doivent pas utiliser ces chemins directement. Au lieu de cela, ils doivent appeler les API décrites ci-dessous.

 



| Chemin d’accès d’origine                | Chemin Redirigé pour les processus x86 32 bits | Chemin Redirigé pour les processus ARM 32 bits |
|------------------------------|------------------------------------------|------------------------------------------|
| % windir% \\ system32           | % windir% \\ SysWOW64                       | % windir% \\ SysArm32                       |
| % windir% \\ LastGood \\ system32 | % windir% \\ LastGood \\ SysWOW64             | % windir% \\ LastGood \\ SysArm32             |
| % windir% \\regedit.exe        | % windir% \\ SysWOW64 \\regedit.exe          | % windir% \\ SysArm32 \\regedit.exe         |



 

Si l’accès amène le système à afficher l’invite du contrôle de compte d’utilisateur, la redirection n’a pas lieu. Au lieu de cela, la version 64 bits du fichier demandé est lancée. Pour éviter ce problème, spécifiez le répertoire SysWOW64 pour éviter la redirection et assurez-vous d’accéder à la version 32 bits du fichier, ou exécutez l’application 32 bits avec des privilèges d’administrateur pour que l’invite UAC ne s’affiche pas.

* * Windows Server 2003 et Windows XP : * * le contrôle de compte d’utilisateur n’est pas pris en charge.

Certains sous-répertoires sont exempts de redirection. L’accès à ces sous-répertoires n’est pas redirigé vers% windir% \\ SysWOW64 : <dl> % windir% \\ system32 \\ CatRoot  
% windir% \\ system32 \\ Catroot2  
% windir% \\ system32 \\ DriverStore  
% windir% \\ system32 \\ drivers, \\ etc.  
% windir% \\ system32 \\ LogFiles  
% windir% \\ system32 \\ spool  
</dl>

* * Windows Server 2008, Windows Vista, Windows Server 2003 et Windows XP : * *% windir% \\ system32 \\ DriverStore est redirigé.

Pour récupérer le nom du répertoire système 32 bits, les applications 64 bits doivent utiliser la fonction [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) (Windows 10, version 1511) ou la fonction [**GetSystemWow64Directory**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .

Les applications doivent utiliser la fonction [**SHGetKnownFolderPath**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) pour déterminer le nom du répertoire% ProgramFiles%.

**Windows Server 2003 et Windows XP :** Les applications doivent utiliser la fonction [**SHGetSpecialFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) pour déterminer le nom du répertoire% ProgramFiles%.

Les applications peuvent contrôler le redirecteur du système de fichiers WOW64 à l’aide des fonctions [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection), [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)et [**Wow64RevertWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) . La désactivation de la redirection du système de fichiers affecte toutes les opérations de fichier effectuées par le thread appelant, donc elle doit être désactivée uniquement lorsqu’elle est nécessaire pour un seul appel [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) et réactivée immédiatement après le retour de la fonction. La désactivation de la redirection du système de fichiers pour des périodes plus longues peut empêcher des applications 32 bits de charger des DLL système, provoquant ainsi l’échec des applications.

les applications 32 bits peuvent accéder au répertoire système natif en remplaçant% windir% \\ SysNative pour% windir% \\ system32. WOW64 reconnaît SysNative comme un alias spécial utilisé pour indiquer que le système de fichiers ne doit pas rediriger l’accès. Ce mécanisme est flexible et facile à utiliser. c’est pourquoi il est recommandé de contourner la redirection du système de fichiers. Notez que les applications 64 bits ne peuvent pas utiliser l’alias SysNative, car il s’agit d’un répertoire virtuel qui n’est pas un réel.

**Windows Server 2003 et Windows XP :** L’alias SysNative a été ajouté à partir de Windows Vista.

 

 