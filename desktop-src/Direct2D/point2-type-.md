---
title: Fonction de type point2 (D2d1helper. h)
description: Crée un point qui stocke ses coordonnées à l’aide du type de données spécifié.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Fonction de type point2 Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d925cc5676e6f0c9a8fb27a3ba2a12591ee87a5a72d5937e365fa57179e47ce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160375"
---
# <a name="point2type-function"></a>Point2, <Type> fonction

Crée un point qui stocke ses coordonnées à l’aide du type de données spécifié.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a>Paramètres de modèle



| Paramètre | Description                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| Type      | Type de données utilisé pour stocker les coordonnées x et y du point. Les valeurs possibles sont FLOAT et UINT32. |



 

## <a name="parameters"></a>Paramètres



| Paramètre | Description                    |
|-----------|--------------------------------|
| x         | Coordonnée X du point. |
| y         | Coordonnée Y du point. |



 

## <a name="return-value"></a>Valeur renvoyée

Point qui contient les coordonnées x et y spécifiées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ desktop apps \|\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[ desktop apps \|\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Bibliothèque<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





