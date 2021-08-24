---
description: D3DXGetVertexShaderProfile fonction-retourne le nom du profil HLSL (High-Level Shader Language) le plus élevé pris en charge par un appareil donné.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: D3DXGetVertexShaderProfile, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5c646fb9779ca923480487cb96f184c76eff9ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473625"
---
# <a name="d3dxgetvertexshaderprofile-function"></a>D3DXGetVertexShaderProfile fonction)

Retourne le nom du profil HLSL (High-Level Shader Language) le plus élevé pris en charge par un appareil donné.

## <a name="syntax"></a>Syntaxe


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers l’appareil. Consultez [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom du profil HLSL.

Si l’appareil ne prend pas en charge les nuanceurs vertex, la fonction retourne la **valeur null**.

## <a name="remarks"></a>Remarques

Un profil de nuanceur spécifie la version du nuanceur d’assembly à utiliser et les fonctionnalités disponibles pour le compilateur HLSL lors de la compilation d’un nuanceur. Le tableau suivant répertorie les profils de nuanceur de sommets pris en charge.




| Profil de nuanceur | Description | 
|----------------|-------------|
| vs_1_1 | Compilez sur vs_1_1 version. | 
| vs_2_0 | Compilez sur vs_2_0 version. | 
| vs_2_a | Identique au profil de vs_2_0, avec les fonctionnalités supplémentaires suivantes disponibles pour que le compilateur cible :<ul><li>Le nombre de registres temporaires (r #) est supérieur ou égal à 13.</li><li>Instruction de contrôle de Flow dynamique.</li><li>Prédication.</li></ul> | 
| vs_3_0 | Compilez sur vs_3_0 version. | 




 

Pour plus d’informations sur les différences entre les versions de nuanceur, consultez [différences de nuanceur de sommets](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
