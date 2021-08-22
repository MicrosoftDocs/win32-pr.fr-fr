---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état du matériau.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'ID3DXEffectStateManager :: SetMaterial, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 67e8b1ad498b5aacbae7aaad2d6b63fa406d54d6315a4e75b3028efe3107eaf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802873"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a>ID3DXEffectStateManager :: SetMaterial, méthode

Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état du matériau.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMaterial* \[ dans\]
</dt> <dd>

Type : **const [**D3DMATERIAL9**](d3dmaterial9.md) \***

Pointeur vers l’état du matériau. Consultez [**D3DMATERIAL9**](d3dmaterial9.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :

-   L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
