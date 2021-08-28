---
description: Permute les composants de deux vecteurs pour créer un nouveau vecteur.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Modèle XMVectorPermute (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd3f7071edaf659991c1294d29a154d3a319d5faee982537025e107cf9621f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978669"
---
# <a name="xmvectorpermute-template"></a>Modèle XMVectorPermute

Permute les composants de deux vecteurs pour créer un nouveau vecteur.

## <a name="syntax"></a>Syntaxe

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[dans le \] premier vecteur.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*MIME*
</dt> <dd>

\[dans le \] second vecteur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le vecteur permuté qui résulte de la combinaison des vecteurs sources.

## <a name="remarks"></a>Remarques

Si les 4 index ne référencent qu’un seul vecteur (c’est-à-dire qu’ils se trouvent tous dans la plage 0-3 ou dans la plage 4-7), utilisez [**XMVectorSwizzle**](xmvectorswizzle-template.md) à la place pour obtenir de meilleures performances.

Notez que la bibliothèque utilise des spécialisations de modèle sur certaines plateformes pour améliorer les performances. Tous les cas de mise en miroir possibles ne sont pas implémentés pour ces cas spéciaux. par conséquent, il est préférable de faire en sorte que l’élément X du vecteur résultant provient du paramètre v1 plutôt que du paramètre v2. Par exemple, préférez utiliser `XMVectorPermute<0,1,4,5>(A,B);` à `XMVectorPermute(4,5,0,1)(B,A);` .

Cette fonction est une version de modèle de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) où les arguments *permute \** sont des valeurs de modèle.

Les constantes [XM \_ permute \_](ovw-xnamath-reference-constants.md) sont fournies pour une utilisation en tant que valeurs d’entrée pour *permutex*,*permute*,*PermuteZ* et *PermuteW*.

> [!Note]  
> Le `XMVectorPermute` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.

 

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

[**XMVectorSwizzle**](xmvectorswizzle-template.md)
</dt> </dl>

 

 
