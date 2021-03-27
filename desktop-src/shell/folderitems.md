---
description: Représente la collection d’éléments dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur la collection.
title: Objet FolderItems (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 6f9a6fa978c64c788cbd224cf3a39454c644a57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749156"
---
# <a name="folderitems-object"></a>Objet FolderItems

Représente la collection d’éléments dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur la collection.

## <a name="members"></a>Membres

L’objet **FolderItems** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **FolderItems** a ces méthodes.



| Méthode                                    | Description                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitems--newenum.md) | Non implémenté.<br/>                                                                              |
| [**Élément**](folderitems-item.md)          | Récupère l’objet [**FolderItem**](folderitem.md) pour un élément spécifié dans la collection.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **FolderItems** a ces propriétés.



| Propriété                                                  | Type d’accès          | Description                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitems-application.md)<br/> | Lecture seule<br/> | Contient l’objet [**application**](folderitems-application.md) de la collection d’éléments Folder.<br/> |
| [**Count**](folderitems-count.md)<br/>             | Lecture seule<br/> | Contient le nombre d’éléments de la collection.<br/>                                                    |
| [**Parent**](folderitems-parent.md)<br/>           | Lecture seule<br/> | Non implémenté.<br/>                                                                                   |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




