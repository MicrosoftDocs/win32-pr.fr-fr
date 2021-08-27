---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Stocke une paire ordonnée de nombres à virgule flottante, en général la largeur et la hauteur d’un rectangle.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7068319c161d7d6b288da6d3a451d8cdfdda715b9890160d17cc7fe872322381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087759"
---
# <a name="d2d1_size_f"></a>D2D1 \_ taille \_ F

Stocke une paire ordonnée de nombres à virgule flottante, en général la largeur et la hauteur d’un rectangle.


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a>Remarques

Comme les points, les tailles sont un autre concept graphique important. Dans Direct2D, les tailles sont représentées par les structures **d2d1 \_ size \_ F** ou [**d2d1 \_ size \_ U**](d2d1-size-u.md) . Tous deux contiennent une paire ordonnée de nombres, en général la largeur et la hauteur d’un rectangle. La **structure d2d1 \_ size \_ F** contient une paire ordonnée de valeurs **float** et la structure **d2d1 \_ size \_ U** contient une paire ordonnée de valeurs **UInt32** .

**D2d1 \_ La taille \_ f** est un nouveau nom pour un type déjà défini ( **\_ taille D2D \_**). Pour obtenir la liste des champs fournis par **d2d1 \_ size \_ f**, consultez **D2D \_ size \_ f**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ desktop apps \|\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[ desktop apps \|\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2DBaseTypes. h (inclure D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Taille ( \_ F) D2D**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[**Taille de D2D1 \_ \_ U**](d2d1-size-u.md)
</dt> <dt>

[**D2D1 \_ point \_ 2F**](d2d1-point-2f.md)
</dt> </dl>

 

