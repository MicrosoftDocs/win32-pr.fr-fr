---
title: IDCompositionMatrixTransform SetMatrixElement (int, int, IDCompositionAnimation), méthode
description: Anime la valeur d’un élément de la matrice de cette transformation 2D.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Méthode SetMatrixElement DirectComposition
- SetMatrixElement, méthode DirectComposition, IDCompositionMatrixTransform, interface
- IDCompositionMatrixTransform interface DirectComposition, méthode SetMatrixElement
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382389"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a>IDCompositionMatrixTransform :: SetMatrixElement (int, int, IDCompositionAnimation \* ), méthode

Anime la valeur d’un élément de la matrice de cette transformation 2D.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ligne* \[ dans\]
</dt> <dd>

Index de ligne de l’élément à modifier. Cette valeur doit être comprise entre 0 et 2 inclus.

</dd> <dt>

*colonne* \[ dans\]
</dt> <dd>

Index de colonne de l’élément à modifier. Cette valeur doit être comprise entre 0 et 1, inclus.

</dd> <dt>

*animation* \[ dans\]
</dt> <dd>

Animation qui représente la façon dont la valeur de l’élément spécifié change au fil du temps. Ce paramètre ne doit pas avoir la valeur NULL.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne la valeur \_ OK. Sinon, elle retourne un code d’erreur **HRESULT** . Pour obtenir la liste des codes d’erreur, consultez [codes d’erreur DirectComposition](directcomposition-error-codes.md) .

## <a name="remarks"></a>Notes

Cette méthode effectue une copie de l’animation spécifiée. Si l’objet référencé par le paramètre d' *animation* est modifié après l’appel de cette méthode, la modification n’affecte pas l’élément à moins que cette méthode ne soit appelée à nouveau. Si l’élément a été précédemment animé, l’appel de cette méthode remplace l’animation précédente par la nouvelle animation.

Cette méthode échoue si l' *animation* est un pointeur non valide ou si elle n’a pas été créée par la même interface [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) que la transformation affectée. L’interface ne peut pas être une implémentation personnalisée ; seules les interfaces créées par Microsoft DirectComposition peuvent être utilisées avec cette méthode.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 