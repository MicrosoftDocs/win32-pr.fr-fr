---
description: Obtient une description de l’étape.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'ID3DXBaseEffect :: GetPassDesc, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74106bc38367e13cd70af94d0ad12016165aaae24693f19386e69ebe1d7a5cb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987749"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a>ID3DXBaseEffect :: GetPassDesc, méthode

Obtient une description de l’étape.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPass* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle de réussite. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ à\]
</dt> <dd>

Type : **[ **D3DXPASS \_ desc**](d3dxpass-desc.md)\***

Retourne une description de la passe spécifiée. Consultez [**D3DXPASS \_ desc**](d3dxpass-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

> [!Note]  
> Si un effet est créé avec [D3DXFX qui \_ ne peut pas être \_ cloné](d3dxfx.md), cette méthode retournera les pointeurs **null** (dans [**D3DXPASS \_ desc**](d3dxpass-desc.md)) aux fonctions de nuanceur.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




