---
description: 'ID3DXEffectStateManager :: SetVertexShaderConstantF, méthode-fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes à virgule flottante de nuanceur de sommets.'
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: 'ID3DXEffectStateManager :: SetVertexShaderConstantF, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aecc510a01bbb461f9f8742f2125b39913335c2ff9b135083f0f59f3f6544b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748559"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a>ID3DXEffectStateManager :: SetVertexShaderConstantF, méthode

Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes à virgule flottante de vertex shader.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartRegister* \[ à\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de base zéro du premier registre constant.

</dd> <dt>

*pConstantData* \[ à\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Tableau de constantes à virgule flottante.

</dd> <dt>

*RegisterCount* \[ à\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de registres dans pConstantData.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :

-   L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
