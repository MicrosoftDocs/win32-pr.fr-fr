---
description: La façon dont les liens symboliques affectent les fonctions de fichier standard qui utilisent des noms de chemin d’accès pour spécifier un ou plusieurs fichiers.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Effets de liens symboliques sur les fonctions des systèmes de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1c5d140dc70de8ebc255b779b226b6da156aa2b8961c49d86f466ac01b26ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078453"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a>Effets de liens symboliques sur les fonctions des systèmes de fichiers

Plusieurs fonctions de fichier standard qui utilisent des noms de chemin d’accès pour spécifier un ou plusieurs fichiers sont affectées par l’utilisation de liens symboliques. Cette rubrique répertorie ces fonctions et décrit les modifications de comportement :

-   [CopyFile et CopyFileTransacted](#copyfile-and-copyfiletransacted)
-   [CopyFileEx](#copyfileex)
-   [CreateFile et CreateFileTransacted](#createfile-and-createfiletransacted)
-   [CreateHardLink et CreateHardLinkTransacted](#createhardlink-and-createhardlinktransacted)
-   [DeleteFile et DeleteFileTransacted](#deletefile-and-deletefiletransacted)
-   [FindFirstChangeNotification](#findfirstchangenotification)
-   [FindFirstFile et FindFirstFileTransacted](#findfirstfile-and-findfirstfiletransacted)
-   [FindFirstFileEx](#findfirstfileex)
-   [FindNextFile](#findnextfile)
-   [GetBinaryType](#getbinarytype)
-   [GetCompressedFileSize et GetCompressedFileSizeTransacted](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [GetDiskFreeSpace](#getdiskfreespaceex)
-   [GetDiskFreeSpaceEx](#getdiskfreespaceex)
-   [GetFileAttributes](#getfileattributesex)
-   [GetFileAttributesEx](#getfileattributesex)
-   [GetFileSecurity](#getfilesecurity)
-   [GetTempPath](#gettemppath)
-   [GetVolumeInformation](#getvolumeinformation)
-   [SetFileAttributes](#setfileattributes)
-   [SetFileSecurity](#setfilesecurity)
-   [Rubriques connexes](#related-topics)

Dans les descriptions ci-dessous, les termes suivants sont utilisés :

-   Fichier source : fichier d’origine à copier.
-   Fichier de destination : copie nouvellement créée du fichier.
-   Cible : entité vers laquelle pointe un lien symbolique.

> [!Note]  
> Le comportement des fonctions qui acceptent un descripteur créé à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , telle que la fonction [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) , varie selon que la fonction **CreateFile** a été appelée ou non à l’aide de l’indicateur de fichier ouvrir l’indicateur de **\_ \_ \_ \_ point d’analyse** . Pour plus d’informations, consultez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) et les sections [CreateFile et CreateFileTransacted](#createfile-and-createfiletransacted) suivantes.

 

## <a name="copyfile-and-copyfiletransacted"></a>CopyFile et CopyFileTransacted

Si le fichier source est un lien symbolique, le fichier copié réel est la cible du lien symbolique.

Si le fichier de destination existe déjà et qu’il s’agit d’un lien symbolique, le lien symbolique est remplacé par le fichier source.

## <a name="copyfileex"></a>CopyFileEx

Si **la \_ \_ copie du \_ lien symbolique** de copie de fichier est spécifiée et :

-   Si le fichier source est un lien symbolique, le lien symbolique est copié, et non le fichier cible.
-   Si le fichier source n’est pas un lien symbolique, le comportement n’est pas modifié.
-   Si le fichier de destination est un lien symbolique existant, le lien symbolique est remplacé, et non le fichier cible.
-   Si **le \_ fichier de copie \_ échoue \_ si \_ Exists** est également spécifié et que le fichier de destination est un lien symbolique existant, l’opération échoue dans tous les cas.

Si **le \_ \_ \_ lien symbolique** copie du fichier de copie n’est pas spécifié et :

-   Si **le \_ fichier de copie \_ échoue \_ si \_ Exists** est également spécifié et que le fichier de destination est un lien symbolique existant, l’opération échoue uniquement si la cible du lien symbolique existe.
-   Si **le \_ fichier de copie \_ échoue \_ si \_ Exists** n’est pas spécifié, le comportement n’est pas modifié.

**Windows Server 2003 et Windows XP :** L' **indicateur \_ \_ \_ symlink de copie** de copie de fichier n’est pas pris en charge. Si le fichier source est un lien symbolique, le fichier copié réel est la cible du lien symbolique.

## <a name="createfile-and-createfiletransacted"></a>CreateFile et CreateFileTransacted

Si l’appel à cette fonction crée un nouveau fichier, le comportement n’est pas modifié.

Si **l' \_ indicateur de fichier ouvrir le \_ \_ \_ point d’analyse** est spécifié et :

-   Si un fichier existant est ouvert et qu’il s’agit d’un lien symbolique, le handle retourné est un handle vers le lien symbolique.
-   Si l’option **créer \_ toujours**, **tronquer le fichier \_ existant** ou **Supprimer l' \_ indicateur de fichier \_ \_ lors de la \_ fermeture** est spécifiée, le fichier affecté est un lien symbolique.

Si aucun indicateur de fichier n’est ouvert, le **\_ \_ \_ \_ point d’analyse** n’est pas spécifié et :

-   Si un fichier existant est ouvert et qu’il s’agit d’un lien symbolique, le handle retourné est un handle vers la cible.
-   Si l’option **créer \_ toujours**, **tronquer le fichier \_ existant** ou **Supprimer l' \_ indicateur de fichier \_ \_ lors de la \_ fermeture** est spécifiée, le fichier affecté est la cible.

## <a name="createhardlink-and-createhardlinktransacted"></a>CreateHardLink et CreateHardLinkTransacted

Si le chemin d’accès pointe vers un lien symbolique, la fonction crée un lien physique vers la cible.

## <a name="deletefile-and-deletefiletransacted"></a>DeleteFile et DeleteFileTransacted

Si le chemin d’accès pointe vers un lien symbolique, le lien symbolique est supprimé, et non pas la cible. Pour supprimer une cible, vous devez appeler [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) et spécifier **l' \_ indicateur \_ de fichier supprimer \_ lors de la \_ fermeture**.

## <a name="findfirstchangenotification"></a>FindFirstChangeNotification

Si le chemin d’accès pointe vers un lien symbolique, le descripteur de notification est créé pour la cible. Si une application s’est inscrite pour recevoir des notifications de modification pour un répertoire qui contient des liens symboliques, l’application est notifiée uniquement lorsque les liens symboliques ont été modifiés, et non les fichiers cibles.

## <a name="findfirstfile-and-findfirstfiletransacted"></a>FindFirstFile et FindFirstFileTransacted

Si le chemin d’accès pointe vers un lien symbolique, le tampon de [**\_ \_ données de recherche Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contient des informations sur le lien symbolique, et non sur la cible.

## <a name="findfirstfileex"></a>FindFirstFileEx

Si le chemin d’accès pointe vers un lien symbolique, le tampon de [**\_ \_ données de recherche Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contient des informations sur le lien symbolique, et non sur la cible.

## <a name="findnextfile"></a>FindNextFile

Si le chemin d’accès pointe vers un lien symbolique, le tampon de [**\_ \_ données de recherche Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contient des informations sur le lien symbolique, et non sur la cible.

## <a name="getbinarytype"></a>GetBinaryType

Si le chemin d’accès pointe vers un lien symbolique, le fichier cible est utilisé.

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a>GetCompressedFileSize et GetCompressedFileSizeTransacted

Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne la taille de fichier de la cible.

## <a name="getdiskfreespace"></a>GetDiskFreeSpace

Si le chemin d’accès pointe vers un lien symbolique, l’opération est effectuée sur la cible.

## <a name="getdiskfreespaceex"></a>GetDiskFreeSpaceEx

Si le chemin d’accès pointe vers un lien symbolique, l’opération est effectuée sur la cible.

## <a name="getfileattributes"></a>GetFileAttributes

Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne les attributs du lien symbolique.

## <a name="getfileattributesex"></a>GetFileAttributesEx

Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne les attributs du lien symbolique.

## <a name="getfilesecurity"></a>GetFileSecurity

Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne les attributs du lien symbolique.

## <a name="gettemppath"></a>GetTempPath

Si le chemin d’accès pointe vers un lien symbolique, le nom du chemin d’accès temporaire conserve les liens symboliques.

## <a name="getvolumeinformation"></a>GetVolumeInformation

Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne les informations de volume de la cible.

## <a name="setfileattributes"></a>SetFileAttributes

Si le chemin d’accès pointe vers un lien symbolique, la fonction récupère les attributs du lien symbolique.

## <a name="setfilesecurity"></a>SetFileSecurity

Si le chemin d’accès pointe vers un lien symbolique, la fonction retourne les attributs du lien symbolique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[**GetBinaryType**](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
