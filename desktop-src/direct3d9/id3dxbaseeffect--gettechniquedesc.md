---
description: Obtient une description de technique.
ms.assetid: 12122858-1e54-446c-8f12-20cc62499d74
title: 'ID3DXBaseEffect :: GetTechniqueDesc, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6027cf24576a29a1f447e5c20f99634c42adf00d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531481"
---
# <a name="id3dxbaseeffectgettechniquedesc-method"></a>ID3DXBaseEffect :: GetTechniqueDesc, méthode

Obtient une description de technique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTechniqueDesc(
  [in]  D3DXHANDLE         hTechnique,
  [out] D3DXTECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hTechnique* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle de technique. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ à\]
</dt> <dd>

Type : **[ **D3DXTECHNIQUE \_ desc**](d3dxtechnique-desc.md)\***

Retourne une description de la technique. Consultez [**D3DXTECHNIQUE \_ desc**](d3dxtechnique-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




