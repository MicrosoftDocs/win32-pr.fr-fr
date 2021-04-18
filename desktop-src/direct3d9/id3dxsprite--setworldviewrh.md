---
description: Définit la transformation de la vue universelle droitier pour un sprite. Un appel à cette méthode est requis avant d’effectuer un billboarding ou de trier des sprites.
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: 'ID3DXSprite :: SetWorldViewRH, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewRH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7521f60f819829fc72ba907b57d4e4eb13682a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527118"
---
# <a name="id3dxspritesetworldviewrh-method"></a>ID3DXSprite :: SetWorldViewRH, méthode

Définit la transformation de la vue universelle droitier pour un sprite. Un appel à cette méthode est requis avant d’effectuer un billboarding ou de trier des sprites.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetWorldViewRH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWorld* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers un [**D3DXMATRIX**](d3dxmatrix.md) qui contient une transformation universelle. Si la **valeur est null**, la matrice d’identité est utilisée pour la transformation universelle.

</dd> <dt>

*pview* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers un [**D3DXMATRIX**](d3dxmatrix.md) qui contient une transformation de vue. Si la **valeur est null**, la matrice d’identité est utilisée pour la transformation de vue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Notes

Un appel à cette méthode (ou à [**ID3DXSprite :: SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) est requis si le sprite est rendu avec la valeur de l’indicateur de [D3DXSprite du \_ \_ panneau](d3dxsprite.md), du D3DXSprite \_ \_ \_ \_ de profondeur de tri FRONTTOBACK ou \_ \_ de la profondeur de tri D3DXSprite BACKTOFRONT \_ \_ [**:: Begin**](id3dxsprite--begin.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




