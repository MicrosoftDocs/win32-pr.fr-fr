---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir une transformation.
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: 'ID3DXEffectStateManager :: SetTransform, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b19a060cfeb09d5d1a92e5e7a1a1f25b58e64f4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953912"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a>ID3DXEffectStateManager :: SetTransform, méthode

Fonction de rappel qui doit être implémentée par un utilisateur pour définir une transformation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*État* \[ dans\]
</dt> <dd>

Type : **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**

Type de transformation à appliquer à la matrice. Consultez [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).

</dd> <dt>

*pMatrix* \[ dans\]
</dt> <dd>

Type : **const [**D3DMATRIX**](d3dmatrix.md) \***

Matrice de transformation. Consultez [**D3DMATRIX**](d3dmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :

-   L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
