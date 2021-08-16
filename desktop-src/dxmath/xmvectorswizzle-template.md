---
description: Swizzles un vecteur.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Modèle XMVectorSwizzle (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 800d976d63480f88defea7f1db07651563df44e8985ae5925810617b44302e87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984479"
---
# <a name="xmvectorswizzle-template"></a>Modèle XMVectorSwizzle

Swizzles un vecteur.

## <a name="syntax"></a>Syntaxe

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[dans \] vector to Swizzle.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le [**XMVECTOR**](xmvector-data-type.md)swizzled.

## <a name="remarks"></a>Remarques

Cette fonction est une version de modèle de [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) où les arguments *Swizzle \** sont des valeurs de modèle.

`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` et `XM_SWIZZLE_W` sont des constantes qui prennent respectivement la valeur 0, 1, 2 et 3 pour une utilisation avec `XMVectorSwizzle` . Identique à,, `XM_PERMUTE_0X` `XM_PERMUTE_0Y` `XM_PERMUTE_0Z` et `XM_PERMUTE_0W` .

> [!Note]  
> Le `XMVectorSwizzle` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.

 

**Espace de noms**: utiliser DirectX

### <a name="platform-requirements"></a>Conditions requises par la plateforme

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8. pris en charge pour les applications de bureau Win32, les applications de Windows Store et les applications Windows Phone 8.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de modèle de bibliothèque DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> </dl>

 

 
