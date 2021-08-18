---
description: Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger des valeurs à virgule flottante dans une instance de type XMVECTOR.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Type de données XMVECTORF32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1a39de246e3e0e4ab9a96197dbe4a286cb6ecabe327d60e5c506795af79dd11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739779"
---
# <a name="xmvectorf32-data-type"></a>Type de données XMVECTORF32

Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger des valeurs à virgule flottante dans une instance de type [**XMVECTOR**](xmvector-data-type.md) .


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a>Remarques

Pour obtenir la liste des fonctionnalités supplémentaires, telles que les constructeurs et les opérateurs, disponibles à l’aide `XMVECTORF32` de lors de la programmation en C++, consultez [Extensions XMVECTORF32](ovw-xmvectorf32-extensions.md).

Les structures **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)et [**XMVECTORU8**](xmvectoru8-data-type.md) sont fournies en tant que mécanisme pour créer des [**XMVECTOR**](xmvector-data-type.md) à partir de différents types de données constantes (virgule flottante, entier non signé, entier et octet) à l’aide d’initialiseurs.

Cela est nécessaire pour prendre en charge [**XMVECTOR**](xmvector-data-type.md), car il ne prend pas en charge les initialiseurs, pour des raisons de portabilité et d’optimisation.

Par exemple :


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
```



**Espace de noms**: utiliser DirectX

### <a name="platform-requirements"></a>Conditions requises par la plateforme

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8. pris en charge pour les applications de bureau Win32, les applications de Windows Store et les applications Windows Phone 8.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de bibliothèque DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Type de données XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Type de données XMVECTOR**](xmvector-data-type.md)
</dt> <dt>

[**Type de données XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Type de données XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Type de données XMVECTORF32**](xmvectorf32-data-type.md)
</dt> </dl>

 

 




