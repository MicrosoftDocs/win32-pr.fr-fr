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
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511160"
---
# <a name="recttype-function"></a>Rect, <Type> fonction

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Bibliothèque<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





