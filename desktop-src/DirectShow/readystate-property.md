---
description: La propriété ReadyState récupère l’ReadyState de l’objet MSWebDVD.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Propriété ReadyState (ocidl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520872"
---
# <a name="readystate-property"></a>Propriété ReadyState

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `ReadyState` propriété récupère l’readyState de l’objet **mswebdvd** .

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant l’ReadyState du contrôle.



| Code de retour | Description                                               |
|-------------|-----------------------------------------------------------|
| 0           | État d’initialisation par défaut.                             |
| 1           | L’objet charge ses propriétés.                         |
| 2           | L’objet a été initialisé.                              |
| 3           | L’objet est interactif, mais les données ne sont pas toutes disponibles. |
| 4           | L’objet a reçu toutes ses données.                         |



 

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut.

Tout objet incorporé dans une page Web expose la `ReadyState` propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Ocidl. h</dt> </dl> |



 

 




