---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir le nombre de segments de la sous-division pour N-patchs.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: 'ID3DXEffectStateManager :: SetNPatchMode, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetNPatchMode
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9b8725a0482b6945b04013df43d34a502f25b7b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954000"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a>ID3DXEffectStateManager :: SetNPatchMode, méthode

Fonction de rappel qui doit être implémentée par un utilisateur pour définir le nombre de segments de la sous-division pour N-patchs.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nSegments* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Scinder la surface en ce nombre de sous-divisions. Il s’agit du même numéro que celui utilisé par [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :

-   L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
