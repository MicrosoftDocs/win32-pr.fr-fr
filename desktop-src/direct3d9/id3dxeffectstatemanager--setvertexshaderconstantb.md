---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes booléennes de nuanceur de sommets.
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: 'ID3DXEffectStateManager :: SetVertexShaderConstantB, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1eaf68f27d477aee36bd7773488f34bad29db61d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535186"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a>ID3DXEffectStateManager :: SetVertexShaderConstantB, méthode

Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes booléennes de nuanceur de sommets.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
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

Type : **const [**bool**](../winprog/windows-data-types.md) \***

Tableau de constantes booléennes.

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
-   L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
