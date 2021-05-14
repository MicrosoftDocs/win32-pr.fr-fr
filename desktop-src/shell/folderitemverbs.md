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
ms.openlocfilehash: 8206c2113e2fa60abef41e43e4739b6eefd77dd4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840603"
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



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




