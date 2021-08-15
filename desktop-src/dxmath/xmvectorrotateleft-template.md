---
description: Fait pivoter le vecteur vers la gauche d’un nombre donné d’éléments de 32 bits.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Modèle XMVectorRotateLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb3d2a06f775e99b275d7333816307f494c5b2a4a7cc0183eaddc4ee4cd8950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499402"
---
# <a name="xmvectorrotateleft-template"></a>Modèle XMVectorRotateLeft

Fait pivoter le vecteur vers la gauche d’un nombre donné d’éléments de 32 bits.

## <a name="syntax"></a>Syntaxe

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[dans \] Vector pour faire pivoter vers la gauche.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le [**XMVECTOR**](xmvector-data-type.md)pivoté.

## <a name="remarks"></a>Remarques

Cette fonction est une version de modèle de [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) où l’argument *Elements* est une valeur de modèle.

> [!Note]  
> Le `XMVectorRotateLeft` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.

 

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
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
