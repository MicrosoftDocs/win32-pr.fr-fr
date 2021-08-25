---
description: 'Fonction D3DXCheckVersion : Vérifiez que la version de D3DX avec laquelle vous avez compilé est la version que vous exécutez.'
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: D3DXCheckVersion, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26831f3a1a5f08494a7382cd412c30dcd24c1482c01dca684962a580068d380d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894119"
---
# <a name="d3dxcheckversion-function"></a>D3DXCheckVersion fonction)

Vérifiez que la version de D3DX que vous avez compilée est la version que vous exécutez.

## <a name="syntax"></a>Syntaxe


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*D3DSDKVersion* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Utilisez la \_ version du kit de développement logiciel D3D \_ . Consultez la section Remarques.

</dd> <dt>

*D3DXSDKVersion* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Utilisez la \_ version du kit de développement logiciel D3DX \_ . Consultez la section Remarques.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

Retourne la **valeur true** si la version de D3DX avec laquelle vous avez compilé est la version avec laquelle vous exécutez. Sinon, la **valeur false** est retournée.

## <a name="remarks"></a>Remarques

Utilisez cette fonction pendant l’initialisation de votre application comme suit :


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



Utilisez [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) pour vérifier que le runtime approprié est installé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
