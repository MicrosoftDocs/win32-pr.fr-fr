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
ms.openlocfilehash: 63f2d1be37ae244eee5960feb8d5eae22ce379a8567bd782c3b0c3e43eabb53b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593339"
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
| [**Count**](-wia-icollection-count.md)<br/> | Lecture seule<br/> | Retourne le nombre de membres de la collection<br/> |
| [**Élément**](-wia-icollection-item.md)<br/>   | Lecture seule<br/> | Retourne l’élément spécifié dans la collection<br/>    |



 

## <a name="remarks"></a>Remarques

### <a name="creationaccess-functions"></a>Fonctions d’accès de création \\

Utilisez l’une des méthodes suivantes pour récupérer une référence à l’objet :



[**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md)

[**Children**](-wia-iwiadispatchitem-children.md)

[**Appareils**](-wia-iwia-devices.md)



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




