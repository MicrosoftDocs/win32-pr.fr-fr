---
description: Classe de collection
ms.assetid: 2b2a70ff-2b49-44b2-b506-b0b2cc953ec4
title: Collection (objet)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Collection
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: cf9c5fc6b01574b930b7b8b74186243d00fa5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319217"
---
# <a name="collection-object"></a>Collection (objet)

Classe de collection

## <a name="members"></a>Membres

L’objet **collection** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **collection** possède ces propriétés.



| Propriété                                           | Type d’accès          | Description                                                |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Saut**](-wia-icollection-count.md)<br/> | Lecture seule<br/> | Retourne le nombre de membres de la collection<br/> |
| [**Élément**](-wia-icollection-item.md)<br/>   | Lecture seule<br/> | Retourne l’élément spécifié dans la collection<br/>    |



 

## <a name="remarks"></a>Notes

### <a name="creationaccess-functions"></a>Fonctions d’accès de création \\

Utilisez l’une des méthodes suivantes pour récupérer une référence à l’objet :



[**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md)

[**Children**](-wia-iwiadispatchitem-children.md)

[**Appareils**](-wia-iwia-devices.md)



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




