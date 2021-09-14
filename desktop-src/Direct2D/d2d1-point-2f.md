---
title: D2D1_POINT_2F (D2DBaseTypes. h)
description: Représente une paire de coordonnées x et y dans l’espace à deux dimensions. | D2D1_POINT_2F (D2DBaseTypes. h)
ms.assetid: b317ae75-d738-4e1a-bcd1-adf3e95b197e
keywords:
- D2D1_POINT_2F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f93bf4a0d1a1b3f988f1c6d168388e9910080dcb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113453"
---
# <a name="d2d1_point_2f"></a>D2D1 \_ point \_ 2F

Représente une paire de coordonnées x et y dans l’espace à deux dimensions.


```C++
typedef D2D_POINT_2F D2D1_POINT_2F;
```



## <a name="remarks"></a>Notes

Les points dans Direct2D sont représentés par les structures **d2d1 \_ point \_ 2F** ou [**d2d1 \_ point \_ 2U**](d2d1-point-2u.md) . Tous deux contiennent une paire de coordonnées x et y dans l’espace à deux dimensions. La **structure \_ d2d1 point \_ 2F** stocke les coordonnées en tant que valeurs **float** , et la structure de **point d2d1 \_ \_ 2U** les stocke en tant que valeurs **UInt32** .

**D2d1 \_ Le POINT \_ 2F** est un nouveau nom pour le type déjà défini du [**\_ point D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ desktop apps \|\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[ desktop apps \|\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2DBaseTypes. h (inclure D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Point d2d1 \_ 2U**](/windows/desktop/Direct2D/d2d1-point-2u)
</dt> <dt>

[**\_Point D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

