---
title: Constructeur Matrix5x4F Matrix5x4F (FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT) (D2d1 \_ Helper. h)
description: Instancie une nouvelle instance d’une classe Matrix5x4F qui est initialisée avec toutes les valeurs de la matrice à virgule flottante.
ms.assetid: 46C2741F-9E49-4ABD-9DA5-D4E6D3CA2B09
keywords:
- Matrix5x4F, constructeur Direct2D
- Matrix5x4F, constructeur Direct2D, interface Matrix5x4F
- Matrix5x4F, interface Direct2D, constructeur Matrix5x4F
topic_type:
- apiref
api_name:
- Matrix5x4F.Matrix5x4F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2582e58f535ddf4f87d54e16dd2edaec2aa37e91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112633"
---
# <a name="matrix5x4fmatrix5x4ffloat-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-constructor"></a>Matrix5x4F :: Matrix5x4F (FLOAT, float, float, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT), constructeur

Instancie une nouvelle instance d’une classe [**Matrix5x4F**](matrix5x4f.md) qui est initialisée avec toutes les valeurs de la matrice à virgule flottante.

## <a name="syntax"></a>Syntaxe


```C++
inline Matrix5x4F(
   FLOAT m11,
   FLOAT m12,
   FLOAT m13,
   FLOAT m14,
   FLOAT m21,
   FLOAT m22,
   FLOAT m23,
   FLOAT m24,
   FLOAT m31,
   FLOAT m32,
   FLOAT m33,
   FLOAT m34,
   FLOAT m41,
   FLOAT m42,
   FLOAT m43,
   FLOAT m44,
   FLOAT m51,
   FLOAT m52,
   FLOAT m53,
   FLOAT m54
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*m11* 
</dt> <dd>

Type : **float**

Valeur de la première ligne et de la première colonne de la matrice.

</dd> <dt>

*M12* 
</dt> <dd>

Type : **float**

Valeur de la première ligne et de la deuxième colonne de la matrice.

</dd> <dt>

*m13* 
</dt> <dd>

Type : **float**

Valeur de la première ligne et de la troisième colonne de la matrice.

</dd> <dt>

*m14* 
</dt> <dd>

Type : **float**

Valeur dans la première ligne et la quatrième colonne de la matrice.

</dd> <dt>

*m21* 
</dt> <dd>

Type : **float**

Valeur de la deuxième ligne et de la première colonne de la matrice.

</dd> <dt>

*m22* 
</dt> <dd>

Type : **float**

Valeur de la deuxième ligne et de la deuxième colonne de la matrice.

</dd> <dt>

*m23* 
</dt> <dd>

Type : **float**

Valeur de la deuxième ligne et de la troisième colonne de la matrice.

</dd> <dt>

*m24* 
</dt> <dd>

Type : **float**

Valeur de la deuxième ligne et de la quatrième colonne de la matrice.

</dd> <dt>

*m31* 
</dt> <dd>

Type : **float**

Valeur de la troisième ligne et de la première colonne de la matrice.

</dd> <dt>

*m32* 
</dt> <dd>

Type : **float**

Valeur de la troisième ligne et de la deuxième colonne de la matrice.

</dd> <dt>

*m33* 
</dt> <dd>

Type : **float**

Valeur de la troisième ligne et de la troisième colonne de la matrice.

</dd> <dt>

*m34* 
</dt> <dd>

Type : **float**

Valeur de la troisième ligne et de la quatrième colonne de la matrice.

</dd> <dt>

*m41* 
</dt> <dd>

Type : **float**

Valeur de la quatrième ligne et de la première colonne de la matrice.

</dd> <dt>

*m42* 
</dt> <dd>

Type : **float**

Valeur de la quatrième ligne et de la deuxième colonne de la matrice.

</dd> <dt>

*m43* 
</dt> <dd>

Type : **float**

Valeur de la quatrième ligne et de la troisième colonne de la matrice.

</dd> <dt>

*m44* 
</dt> <dd>

Type : **float**

Valeur de la quatrième ligne et de la quatrième colonne de la matrice.

</dd> <dt>

*m51* 
</dt> <dd>

Type : **float**

Valeur de la cinquième ligne et de la première colonne de la matrice.

</dd> <dt>

*m52* 
</dt> <dd>

Type : **float**

Valeur de la cinquième ligne et de la deuxième colonne de la matrice.

</dd> <dt>

*m53* 
</dt> <dd>

Type : **float**

Valeur de la cinquième ligne et de la troisième colonne de la matrice.

</dd> <dt>

*m54* 
</dt> <dd>

Type : **float**

Valeur dans la cinquième ligne et la quatrième colonne de la matrice.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows Vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                           |
| Espace de noms<br/>                | D2D1<br/>                                                                                                                   |
| En-tête<br/>                   | <dl> <dt>D2d1 \_ Helper. h</dt> </dl>                                         |
| Bibliothèque<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                               |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Matrix5x4F**](matrix5x4f.md)
</dt> </dl>

 

 





