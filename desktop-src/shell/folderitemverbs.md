---
description: Représente la collection de verbes pour un élément dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur la collection.
title: Objet FolderItemVerbs (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 31badb4b-b89e-4294-9dd7-bda716e163b2
ms.openlocfilehash: a710f8a1362ea54e98d76056b3b911ef4882cf522d200626e3479baf6d770af9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593259"
---
# <a name="folderitemverbs-object"></a>Objet FolderItemVerbs

Représente la collection de verbes pour un élément dans un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur la collection.

## <a name="members"></a>Membres

L’objet **FolderItemVerbs** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **FolderItemVerbs** a ces méthodes.



| Méthode                                        | Description                                                                                                      |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitemverbs--newenum.md) | Crée et retourne un nouvel objet **FolderItemVerbs** qui est une copie de cet objet FolderItemVerbs.<br/>   |
| [**Élément**](folderitemverbs-item.md)          | Récupère l’objet [**FolderItemVerb**](folderitemverb.md) pour un élément spécifié dans la collection.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **FolderItemVerbs** a ces propriétés.



| Propriété                                                      | Type d’accès          | Description                                                |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Application**](folderitemverbs-application.md)<br/> | Lecture seule<br/> | Non implémenté.<br/>                                |
| [**Count**](folderitemverbs-count.md)<br/>             | Lecture seule<br/> | Contient le nombre d’éléments de la collection.<br/> |
| [**Parent**](folderitemverbs-parent.md)<br/>           | Lecture seule<br/> | Non implémenté.<br/>                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




