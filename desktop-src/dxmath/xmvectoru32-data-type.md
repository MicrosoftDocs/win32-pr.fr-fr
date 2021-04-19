---
description: Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger les \_ valeurs UInt32 t dans une instance de type XMVECTOR.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: Type de données XMVECTORU32 (Directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c7a64d42bc4638573b987642c0cd77c37cc12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542406"
---
# <a name="xmvectoru32-data-type"></a>Type de données XMVECTORU32

Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger les \_ valeurs UInt32 t dans une instance de type [**XMVECTOR**](xmvector-data-type.md) .


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a>Notes

Pour obtenir la liste des fonctionnalités supplémentaires, telles que les constructeurs et les opérateurs, disponibles à l’aide de XMVECTORU32 lors de la programmation en C++, consultez [Extensions XMVECTORU32](ovw-xmvectoru32-extensions.md).

Les structures [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md)et [**XMVECTORU8**](xmvectoru8-data-type.md) sont fournies en tant que mécanisme pour créer des [**XMVECTOR**](xmvector-data-type.md) à partir de différents types de données constantes (virgule flottante, entier non signé, entier et octet) à l’aide d’initialiseurs.

Cela est nécessaire pour prendre en charge [**XMVECTOR**](xmvector-data-type.md), car il ne prend pas en charge les initialiseurs, pour des raisons de portabilité et d’optimisation.

Par exemple :

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

**Espace de noms**: utiliser DirectX

### <a name="platform-requirements"></a>Conditions requises par la plateforme

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8. Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Directxmath. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de bibliothèque DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Type de données XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Type de données XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Type de données XMVECTOR**](xmvector-data-type.md)
</dt> <dt>

[**Type de données XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[Extensions XMVECTORU32](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




