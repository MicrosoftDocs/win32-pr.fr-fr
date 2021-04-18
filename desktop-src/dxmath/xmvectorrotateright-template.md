---
description: Fait pivoter le vecteur vers la droite d’un nombre donné d’éléments de 32 bits.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Modèle XMVectorRotateRight (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2c4e623a75015e8051a5a9ccf32f4715016b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526470"
---
# <a name="xmvectorrotateright-template"></a>Modèle XMVectorRotateRight

Fait pivoter le vecteur vers la droite d’un nombre donné d’éléments de 32 bits.

## <a name="syntax"></a>Syntaxe

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[dans \] Vector pour faire pivoter vers la droite.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le [**XMVECTOR**](xmvector-data-type.md)pivoté.

## <a name="remarks"></a>Notes

Cette fonction est une version de modèle de [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) où l’argument *Elements* est une valeur de modèle.

> [!Note]  
> Le `XMVectorRotateRight` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.

 

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

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
