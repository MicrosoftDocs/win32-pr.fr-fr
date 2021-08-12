---
description: Définit la transformation de vue universelle de gauche pour un sprite. Un appel à cette méthode est requis avant d’effectuer un billboarding ou de trier des sprites.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: 'ID3DXSprite :: SetWorldViewLH, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 67ee276b90629a18f93bd9a26879e8a7ad62d71ae46baf2d2c0a6bfba82a53a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292571"
---
# <a name="id3dxspritesetworldviewlh-method"></a>ID3DXSprite :: SetWorldViewLH, méthode

Définit la transformation de vue universelle de gauche pour un sprite. Un appel à cette méthode est requis avant d’effectuer un billboarding ou de trier des sprites.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetWorldViewLH(
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

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Notes

Un appel à cette méthode (ou à [**ID3DXSprite :: SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) est requis si le sprite est rendu avec la valeur de l’indicateur de [D3DXSprite du \_ \_ panneau](d3dxsprite.md), du D3DXSprite \_ \_ \_ \_ de profondeur de tri FRONTTOBACK ou \_ \_ de la profondeur de tri D3DXSprite BACKTOFRONT \_ \_ [**:: Begin**](id3dxsprite--begin.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




