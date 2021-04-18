---
description: Fait pivoter un vecteur vers la gauche d’un nombre donné de composants 32 bits et insérer les éléments sélectionnés de ce résultat dans un autre vecteur.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Modèle XMVectorInsert (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526319"
---
# <a name="xmvectorinsert-template"></a>Modèle XMVectorInsert

Fait pivoter un vecteur vers la gauche d’un nombre donné de composants 32 bits et insérer les éléments sélectionnés de ce résultat dans un autre vecteur.

## <a name="syntax"></a>Syntaxe

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="VD"></span><span id="vd"></span>*VD*
</dt> <dd>

\[dans \] Vector à insérer dans.

</dd> <dt>

<span id="VS"></span><span id="vs"></span>*COMPARATIF*
</dt> <dd>

\[dans \] Vector pour faire pivoter vers la gauche.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le [**XMVECTOR**](xmvector-data-type.md) qui résulte de la rotation et de l’insertion.

## <a name="remarks"></a>Notes

Cette fonction est une version de modèle de [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) où les arguments *Select \** sont des valeurs de modèle.

Pour des performances optimales, le résultat de `XMVectorInsert` doit être attribué à *VD*.

> [!Note]  
> Le `XMVectorInsert` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x.

 

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
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
