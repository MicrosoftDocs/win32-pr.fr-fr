---
title: Fonction de type de taille (D2d1helper. h)
description: Crée une structure de taille qui stocke sa largeur et sa hauteur à l’aide du type de données spécifié.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Fonction de type de taille Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465002"
---
# <a name="sizetype-function"></a>Size, <Type> fonction

Crée une structure de taille qui stocke sa largeur et sa hauteur à l’aide du type de données spécifié.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a>Paramètres de modèle



| Paramètre | Description                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| Type      | Type de données utilisé pour stocker la largeur et la hauteur de la taille. Les valeurs possibles sont FLOAT et UINT32. |



 

## <a name="parameters"></a>Paramètres



| Paramètre | Description        |
|-----------|--------------------|
| width     | Largeur de la taille.  |
| height    | Hauteur de la taille. |



 

## <a name="return-value"></a>Valeur renvoyée

Taille qui contient la largeur et la hauteur spécifiées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Bibliothèque<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





