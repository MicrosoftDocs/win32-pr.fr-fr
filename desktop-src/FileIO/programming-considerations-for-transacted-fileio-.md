---
description: Décrit les différentes considérations en matière de programmation pour le NTFS transactionnel.
ms.assetid: a1ef1ce1-42f6-4627-ab64-e7f41fa23e94
title: Considérations relatives à la programmation pour NTFS transactionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd3150746b1cb34495178cc8318805587f3d08f17e04cb8227e95a9c52ddce3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047939"
---
# <a name="programming-considerations-for-transactional-ntfs"></a>Considérations relatives à la programmation pour NTFS transactionnel

Pour obtenir une description des différentes considérations relatives à la programmation pour NTFS transactionnel, consultez les sections suivantes :

-   [Les modifications de fichiers qui sont traitées](#which-file-changes-are-transacted)
-   [Compression](#compression)
-   [Création d’un fichier ou d’un répertoire](#creating-a-file-or-directory)
-   [Suppression d’un fichier](#deleting-a-file)
-   [Suppression d’un répertoire](#deleting-a-directory)
-   [Problèmes de verrouillage de répertoire](#directory-locking-issues)
-   [Énumération de répertoire](#directory-enumeration)
-   [Fichiers mappés en mémoire](#memory-mapped-files)
-   [Flux nommés](#named-streams)
-   [Attribution d’un nouveau nom à un fichier ou à un répertoire](#renaming-a-file-or-directory)
-   [Points d'analyse](#reparse-points)
-   [Codes d’erreur](#error-codes)
-   [Système de fichiers chiffré](#encrypted-file-system)
-   [Fonctions d’e/s de fichier et NTFS transactionnel](#file-io-functions-and-transactional-ntfs)
    -   [Fonctions traitées](#transacted-functions)
    -   [Les fonctions d’e/s de fichier ont changé par TxF](#file-io-functions-changed-by-txf)

## <a name="which-file-changes-are-transacted"></a>Les modifications de fichiers qui sont traitées

La plupart des modifications de fichier, telles que les modifications apportées au contenu des fichiers, aux flux, aux points d’analyse, aux attributs et à l’espace de noms du système de fichiers, sont traitées. Quand l’une de ces modifications est effectuée sur un descripteur de fichier transactionnel, la modification est isolée des autres transactions, et la modification est annulée si la transaction est restaurée.

Les modifications qui n’affectent pas le contenu du fichier, les métadonnées ou l’espace de noms du système de fichiers, telles que les modifications de compression ou de défragmentation, ne sont pas traitées. Ces modifications ne sont pas isolées des autres transactions, et elles ne sont pas annulées si la transaction est restaurée.

## <a name="compression"></a>Compression

L’état de compression d’un fichier ouvert dans une transaction ne peut pas être modifié.

## <a name="creating-a-file-or-directory"></a>Création d’un fichier ou d’un répertoire

Un fichier ou un répertoire créé dans une transaction n’est pas visible à l’extérieur de la transaction actuelle. En dehors de cette transaction, toute tentative de création d’un fichier portant le même nom échoue avec l’erreur erreur de **\_ \_ conflit transactionnel**, en réservant efficacement le nom de fichier lorsque la transaction est validée ou annulée.

## <a name="deleting-a-file"></a>Suppression d’un fichier

Un fichier ou un répertoire qui est supprimé en appelant la fonction [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) reste visible pour tous les lecteurs externes.

> [!Note]  
> Tous les descripteurs traités dans le fichier doivent être fermés avant la fin de la transaction. Si les descripteurs ne sont pas correctement fermés, la suppression n’a pas lieu. Tous les descripteurs ouverts dans le fichier doivent être fermés avant d’effectuer la validation pour que l’opération de suppression soit considérée comme faisant partie de la transaction. cela est dû au fait que le système ne supprime pas réellement un fichier tant que le dernier descripteur n’est pas fermé, même lorsque l’opération n’est pas traitée, dans le cadre du sous-système d’e/s de fichier Windows.

 

## <a name="deleting-a-directory"></a>Suppression d’un répertoire

Un répertoire qui est supprimé en appelant la fonction [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) reste visible pour tous les lecteurs externes.

> [!Note]  
> Les mêmes contraintes existent pour les handles ouverts sur les opérations de répertoire traitées que sur les fichiers. Pour plus d’informations, consultez [Suppression d’un fichier](#deleting-a-file).

 

## <a name="directory-locking-issues"></a>Problèmes de verrouillage de répertoire

Si un fichier est modifié dans une transaction, tous les composants de répertoire du chemin d’accès au fichier sont appelés *épinglés par rapport à renommer* jusqu’à la fin de la transaction. Autrement dit, le système vous empêche de le renommer jusqu’à ce que la transaction soit validée ou restaurée. Une tentative de changement de nom d’un répertoire qui est un ancêtre en fichier modifié dans une transaction en cours échouera avec l’erreur erreur **\_ Impossible de \_ débloquer la \_ \_ dépendance transactionnelle**.

## <a name="directory-enumeration"></a>Énumération de répertoire

Le contenu d’un répertoire peut être modifié lorsqu’une énumération est en cours à la suite de l’utilisation d’API qui énumèrent, par exemple les fonctions [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) et [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) .

Les modifications apportées à un répertoire en dehors d’une transaction ne sont pas isolées de la transaction et sont immédiatement visibles dans la transaction. Par exemple, si un rédacteur non transactionnel ajoute un fichier à un répertoire, le nouveau fichier est immédiatement visible à l’intérieur de la transaction de telle sorte que l’appel de la fonction [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) ou [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) retourne le nouveau fichier.

Les modifications apportées à un répertoire à l’intérieur d’une transaction sont isolées jusqu’à ce que la transaction soit validée. Par exemple, un fichier créé dans le répertoire dans le cadre de la transaction. Un lecteur non transactionnel appelant la fonction [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) ou [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) ne voit pas le fichier nouvellement créé tant que la transaction n’est pas validée.

## <a name="memory-mapped-files"></a>Fichiers mappés en mémoire

Le client doit appeler la fonction [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile) , fermer l’objet de mappage de fichiers et fermer le descripteur de fichier avant de valider la transaction associée sur un fichier mappé en mémoire.

## <a name="named-streams"></a>Flux nommés

Les flux nommés sont entièrement transactionnels, mais le verrouillage est effectué au niveau du fichier, et non au niveau du flux. Les rédacteurs à l’extérieur d’une transaction qui tente de modifier un flux dans un fichier verrouillé reçoivent la **\_ \_ violation de partage des erreurs** d’erreur.

Vous ne pouvez pas renommer un flux secondaire dans une transaction.

## <a name="renaming-a-file-or-directory"></a>Attribution d’un nouveau nom à un fichier ou à un répertoire

Pour renommer un fichier en tant qu’opération traitée par transaction, appelez [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) pour déplacer le fichier.

## <a name="reparse-points"></a>Points d'analyse

Les modifications apportées aux points d’analyse sont transactionnelles, ce qui signifie que si un nouveau point d’analyse est assigné à un fichier dans une transaction, il n’est pas visible pour les autres transactions. De même, les modifications ou la suppression d’un point d’analyse existant ne sont pas visibles tant que la validation n’est pas effectuée.

## <a name="error-codes"></a>Codes d’erreur

Le gestionnaire de transactions KTM (Kernel Transaction Manager) utilise les codes d’erreur système dans la plage comprise entre 6700 et 6799. NTFS transactionnel (TxF) utilise Windows codes d’erreur dans la plage comprise entre 6800 et 6899. Pour plus d’informations, consultez WinError. h et codes d’erreur système (6000-8199).

## <a name="encrypted-file-system"></a>Système de fichiers chiffré

TxF ne prend pas en charge les opérations sur les fichiers EFS. Vous ne pouvez pas ouvrir un fichier chiffré EFS pour les transactions. L’appel de la fonction [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) sur un fichier EFS échoue avec l’erreur erreur **\_ EFS \_ non \_ autorisée \_ dans la \_ transaction**. De même, l’appel de la fonction [**EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) sur un fichier dans une transaction échoue avec l’erreur erreur **\_ EFS \_ non \_ autorisée \_ dans la \_ transaction**.

## <a name="file-io-functions-and-transactional-ntfs"></a>Fonctions d’e/s de fichier et NTFS transactionnel

TxF fournit de nouvelles fonctions transactionnelles qui prennent un nom de fichier et modifie le comportement des fonctions d’API d’e/s de fichier existantes qui prennent un handle de fichier.

### <a name="transacted-functions"></a>Fonctions traitées

Si vous n’appelez pas l’une des fonctions transactionnelles suivantes à la place de sa version non traitée, l’opération ne sera pas traitée :

-   [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
-   [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)
-   [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
-   [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
-   [**CreateSymbolicLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinktransacteda)
-   [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
-   [**FindFirstFileNameTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirstfilenametransactedw)
-   [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
-   [**FindFirstStreamTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirststreamtransactedw)
-   [**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
-   [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
-   [**GetFullPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfullpathnametransacteda)
-   [**GetLongPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getlongpathnametransacteda)
-   [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)
-   [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)
-   [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)

Par exemple, la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) a maintenant une version traitée : [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).

### <a name="file-io-functions-changed-by-txf"></a>Les fonctions d’e/s de fichier ont changé par TxF

Le tableau suivant répertorie les fonctions dont le comportement est affecté par le NTFS transactionnel. Par exemple, le comportement de la fonction [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) varie selon que le paramètre *hFile* a été créé par la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ou la fonction [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) .



| Fonction                                                                                                                                                                                                                                                                                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CloseHandle"></span><span id="closehandle"></span><span id="CLOSEHANDLE"></span>[**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)<br/>                                                                                                                                                                                                                                                                                                             | Les applications doivent fermer tous les descripteurs liés à une transaction avant la validation de la transaction. Une application doit fermer un handle transactionnel ouvert avec l' **\_ indicateur \_ de fichier supprimer \_ lors de la \_ fermeture** avant de valider la transaction pour que l’opération de suppression se produise.<br/>                                                                                                                                     |
| <span id="CreateFileMapping"></span><span id="createfilemapping"></span><span id="CREATEFILEMAPPING"></span>[**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                 | Si une transaction est associée à *hFile*, l’objet de mappage de fichiers créé par cette fonction sera associé à la même transaction. Les modifications apportées via les vues de cet objet de mappage de fichier sont traitées. Les applications doivent appeler [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), annuler le mappage de toutes les vues et fermer tous les descripteurs de l’objet de mappage de fichiers avant de valider les modifications traitées.<br/> |
| <span id="FindNextFile"></span><span id="findnextfile"></span><span id="FINDNEXTFILE"></span>[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)<br/>                                                                                                                                                                                                                                                                                                         | Si une transaction est liée au descripteur d’énumération de fichiers, les fichiers retournés sont soumis aux règles d’isolation des transactions.<br/>                                                                                                                                                                                                                                                                    |
| <span id="FSCTL_SET_COMPRESSION"></span><span id="fsctl_set_compression"></span>[**FSCTL \_ définir la \_ compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                                                                                                                                                                                                                                                                                                  | Vous ne pouvez pas modifier l’état de compression d’un fichier ouvert par [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).<br/>                                                                                                                                                                                                                                                                                               |
| <span id="GetFileInformationByHandle__________and__________GetFileInformationByHandleEx"></span><span id="getfileinformationbyhandle__________and__________getfileinformationbyhandleex"></span><span id="GETFILEINFORMATIONBYHANDLE__________AND__________GETFILEINFORMATIONBYHANDLEEX"></span>[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) et [ **GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)<br/> | Si une transaction est liée au descripteur de fichier, la fonction retourne des informations pour la vue de fichier isolé.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetFileSize_and__________GetFileSizeEx"></span><span id="getfilesize_and__________getfilesizeex"></span><span id="GETFILESIZE_AND__________GETFILESIZEEX"></span>[**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) et [ **GetFileSizeEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesizeex)<br/>                                                                                                                                                                                  | Si une transaction est liée au descripteur de fichier, la fonction retourne des informations pour la vue de fichier isolé.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetVolumeInformation"></span><span id="getvolumeinformation"></span><span id="GETVOLUMEINFORMATION"></span>[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                                                                                                                                                                                                                 | Si le volume prend en charge les transactions de système de fichiers, la fonction retourne le **fichier \_ prend en charge les \_ transactions** dans *lpFileSystemFlags*.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="MapViewOfFile_and__________MapViewOfFileEx"></span><span id="mapviewoffile_and__________mapviewoffileex"></span><span id="MAPVIEWOFFILE_AND__________MAPVIEWOFFILEEX"></span>[**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) et [ **MapViewOfFileEx**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex)<br/>                                                                                                                                                                | Si une transaction est associée au descripteur de fichier utilisé pour créer l’objet de mappage de fichiers qui est mappé, la vue associée est traitée. Si la vue est utilisée pour effectuer des modifications transactionnelles dans un fichier, l’utilisateur doit appeler [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), fermer l’objet de mappage de fichiers et fermer le descripteur de fichier avant de valider la transaction associée.<br/>              |
| <span id="ReadDirectoryChangesW"></span><span id="readdirectorychangesw"></span><span id="READDIRECTORYCHANGESW"></span>[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>                                                                                                                                                                                                                                                            | Si une transaction est liée au handle de répertoire, les notifications reflètent la vue isolée de l’annuaire. Les modifications apportées aux fichiers en dehors de la vue traitée dans le répertoire ne sont pas incluses dans les notifications.<br/>                                                                                                                                                                                |
| <span id="ReadFile___________ReadFileEx__and__________ReadFileScatter"></span><span id="readfile___________readfileex__and__________readfilescatter"></span><span id="READFILE___________READFILEEX__AND__________READFILESCATTER"></span>[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)et [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter)<br/>                                                                                  | Si une transaction est liée au descripteur de fichier, la fonction retourne les données à partir de la vue traitée du fichier. Un handle de lecture traité est garanti pour afficher la même vue d’un fichier pendant la durée du descripteur.<br/>                                                                                                                                                                                 |
| <span id="SetEndOfFile"></span><span id="setendoffile"></span><span id="SETENDOFFILE"></span>[**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                                                                                                                                                                                                                                                                                                         | Si une transaction est liée au descripteur, la modification de la position de fin de fichier est traitée.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="SetFileInformationByHandle"></span><span id="setfileinformationbyhandle"></span><span id="SETFILEINFORMATIONBYHANDLE"></span>[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)<br/>                                                                                                                                                                                                                                   | Si une transaction est liée au descripteur, les modifications apportées seront traitées pour les classes d’informations **FileBasicInfo**, **FileRenameInfo**, **FileAllocationInfo**, **FileEndOfFileInfo** et **FileDispositionInfo**.<br/>                                                                                                                                                                          |
| <span id="SetFileShortName"></span><span id="setfileshortname"></span><span id="SETFILESHORTNAME"></span>[**SetFileShortName**](/windows/desktop/api/WinBase/nf-winbase-setfileshortnamea)<br/>                                                                                                                                                                                                                                                                                     | Si une transaction est liée au descripteur, la modification du nom abrégé du fichier est traitée.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="SetFileTime"></span><span id="setfiletime"></span><span id="SETFILETIME"></span>[**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)<br/>                                                                                                                                                                                                                                                                                                             | Si une transaction est liée au descripteur, la modification de l’heure du fichier est traitée.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="WriteFile__________WriteFileEx__and_________WriteFileGather"></span><span id="writefile__________writefileex__and_________writefilegather"></span><span id="WRITEFILE__________WRITEFILEEX__AND_________WRITEFILEGATHER"></span>[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)et [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)<br/>                                                                              | Si une transaction est liée au descripteur de fichier, l’écriture du fichier est traitée.<br/>                                                                                                                                                                                                                                                                                                                          |



 

 

