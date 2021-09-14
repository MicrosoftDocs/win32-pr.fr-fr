---
title: Fonction de type Rect (D2d1helper. h)
description: Crée une structure rectangle qui stocke ses coordonnées à l’aide du type de données spécifié.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Fonction de type Rect Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5f56fd9cbcfd576a441d9199e7ec1114cfb9f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112566"
---
# <a name="rectlttypegt-function"></a>Rect &lt; , &gt; fonction de type

Crée une structure rectangle qui stocke ses coordonnées à l’aide du type de données spécifié.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a>Paramètres de modèle



| Paramètre | Description                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| Type      | Type de données utilisé pour stocker les dimensions du rectangle. Les valeurs possibles sont **float** et **UInt32**. |



 

## <a name="parameters"></a>Paramètres



| Paramètre | Description                                             |
|-----------|---------------------------------------------------------|
| gauche      | Coordonnée x de l’angle supérieur gauche du rectangle.  |
| top       | Coordonnée y de l’angle supérieur gauche du rectangle.  |
| droite     | Coordonnée x du coin inférieur droit du rectangle. |
| bottom    | Coordonnée y du coin inférieur droit du rectangle. |



 

## <a name="return-value"></a>Valeur renvoyée

Structure rectangle qui contient les coordonnées spécifiées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ desktop apps \|\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[ desktop apps \|\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Bibliothèque<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





