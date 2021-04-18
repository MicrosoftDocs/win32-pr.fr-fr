---
description: Retourne le nombre de jeux d’animations actuellement enregistrés dans le contrôleur d’animation.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'ID3DXAnimationController :: GetNumAnimationSets, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522567"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a>ID3DXAnimationController :: GetNumAnimationSets, méthode

Retourne le nombre de jeux d’animations actuellement enregistrés dans le contrôleur d’animation.

## <a name="syntax"></a>Syntaxe


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’ensembles d’animations.

## <a name="remarks"></a>Notes

Le contrôleur contient un nombre quelconque d’animations et de jeux d’animations. Les jeux d’animations peuvent être enregistrés avec [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md). Un contrôleur d’animation créé par un appel à [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) inscrit automatiquement les jeux d’animations chargés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
