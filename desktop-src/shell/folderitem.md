---
description: Représente un élément dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur l’élément.
title: Objet FolderItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a1c66c594a60682ad359ffbcdcd0bf045601051d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484025"
---
# <a name="folderitem-object"></a>Objet FolderItem

Représente un élément dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur l’élément.

## <a name="members"></a>Membres

L’objet **FolderItem** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **FolderItem** a ces méthodes.



| Méthode                                      | Description                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InvokeVerb**](folderitem-invokeverb.md) | Exécute un verbe sur l’élément.<br/>                                                                                                                     |
| [**Verbes et adverbes**](folderitem-verbs.md)           | Récupère l’objet [**FolderItemVerbs**](folderitemverbs.md) de l’élément. Cet objet est la collection de verbes qui peuvent être exécutés sur l’élément.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **FolderItem** a ces propriétés.



| Propriété                                                   | Type d’accès           | Description                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitem-application.md)<br/>   | Lecture seule<br/>  | Contient l’objet d' [**application**](folderitem-application.md) de l’élément de dossier.<br/>                                                                                                                   |
| [**GetFolder ITaskService**](folderitem-getfolder.md)<br/>       | Lecture seule<br/>  | Contient l’objet [**dossier**](folder.md) de l’élément, si l’élément est un dossier.<br/>                                                                                                                           |
| [**GetLink**](folderitem-getlink.md)<br/>           | Lecture seule<br/>  | Contient l’objet [**ShellLinkObject**](shelllinkobject-object.md) de l’élément, si l’élément est un raccourci.<br/>                                                                                                |
| [**IsBrowsable**](folderitem-isbrowsable.md)<br/>   | Lecture seule<br/>  | Indique si l’élément peut être hébergé à l’intérieur d’un navigateur ou d’un frame de l’Explorateur Windows.<br/>                                                                                                                         |
| [**IsFileSystem**](folderitem-isfilesystem.md)<br/> | Lecture seule<br/>  | Indique si l’élément fait partie du système de fichiers.<br/>                                                                                                                                                       |
| [**IsFolder**](folderitem-isfolder.md)<br/>         | Lecture seule<br/>  | Indique si l’élément est un dossier.<br/>                                                                                                                                                                      |
| [**IsLink**](folderitem-islink.md)<br/>             | Lecture seule<br/>  | Indique si l’élément est un raccourci.<br/>                                                                                                                                                               |
| [**ModifyDate**](folderitem-modifydate.md)<br/>     | Lecture/écriture<br/> | Définit ou obtient la date et l’heure de la dernière modification d’un fichier. [**ModifyDate**](folderitem-modifydate.md) peut être utilisé pour récupérer la date et l’heure de la dernière modification d’un dossier, mais ne peut pas le définir.<br/> |
| [**Nom**](folderitem-name.md)<br/>                 | Lecture/écriture<br/> | Définit ou obtient le nom de l’élément.<br/>                                                                                                                                                                           |
| [**Parent**](folderitem-parent.md)<br/>             | Lecture seule<br/>  | Obtient un objet qui représente le parent de l’élément.<br/>                                                                                                                                                  |
| [**Path**](folderitem-path.md)<br/>                 | Lecture seule<br/>  | Contient le chemin d’accès complet et le nom de l’élément.<br/>                                                                                                                                                                 |
| [**Corps**](folderitem-size.md)<br/>                 | Lecture seule<br/>  | Contient la taille de l’élément.<br/>                                                                                                                                                                               |
| [**Type**](folderitem-type.md)<br/>                 | Lecture seule<br/>  | Contient une représentation sous forme de chaîne du type de l’élément.<br/>                                                                                                                                                    |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




