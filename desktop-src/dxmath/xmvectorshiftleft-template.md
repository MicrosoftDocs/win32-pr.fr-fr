---
description: Déplace un vecteur vers la gauche d’un nombre donné d’éléments 32 bits, en remplissant les éléments libérés avec les éléments d’un second vecteur.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Modèle XMVectorShiftLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544449"
---
# <a name="xmvectorshiftleft-template"></a>Modèle XMVectorShiftLeft

Déplace un vecteur vers la gauche d’un nombre donné d’éléments 32 bits, en remplissant les éléments libérés avec les éléments d’un second vecteur.

## <a name="syntax"></a>Syntaxe

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[dans \] Vector, déplacer vers la gauche.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*MIME*
</dt> <dd>

\[dans \] Vector utilisé pour remplir les composants libérés de V1 après leur décalage vers la gauche.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le décalage et le remplissage de [**XMVECTOR**](xmvector-data-type.md).

## <a name="remarks"></a>Notes

Cette fonction est une version de modèle de [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) où l’argument *Elements* est une valeur de modèle.

> [!Note]  
> Le `XMVectorShiftLeft` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.

 

**Espace de noms**: utiliser DirectX

### <a name="platform-requirements"></a>Conditions requises par la plateforme

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8. Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de modèle de bibliothèque DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> </dl>

 

 
