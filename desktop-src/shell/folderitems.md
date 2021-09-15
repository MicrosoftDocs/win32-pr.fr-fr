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
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412509"
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
| [**Nombre**](folderitems-count.md)<br/>             | Lecture seule<br/> | Contient le nombre d’éléments de la collection.<br/>                                                    |
| [**Parent**](folderitems-parent.md)<br/>           | Lecture seule<br/> | Non implémenté.<br/>                                                                                   |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




