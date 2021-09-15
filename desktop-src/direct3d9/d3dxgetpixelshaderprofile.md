---
description: D3DXGetPixelShaderProfile fonction-retourne le nom du profil HLSL (High-Level Shader Language) le plus élevé pris en charge par un appareil donné.
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: D3DXGetPixelShaderProfile, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc609e742a4f780f3cb8c34e4dbc4cc40842ee51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518733"
---
# <a name="d3dxgetpixelshaderprofile-function"></a>D3DXGetPixelShaderProfile fonction)

Retourne le nom du profil HLSL (High-Level Shader Language) le plus élevé pris en charge par un appareil donné.

## <a name="syntax"></a>Syntaxe


```C++
LPCSTR D3DXGetPixelShaderProfile(
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

Si l’appareil ne prend pas en charge les nuanceurs de pixels, la fonction retourne la **valeur null**.

## <a name="remarks"></a>Remarques

Un profil de nuanceur spécifie la version du nuanceur d’assembly à utiliser et les fonctionnalités disponibles pour le compilateur HLSL lors de la compilation d’un nuanceur. Le tableau suivant répertorie les profils de nuanceur de pixels pris en charge.




| Profil de nuanceur | Description | 
|----------------|-------------|
| ps_1_1 | Compilez sur ps_1_1 version. | 
| ps_1_2 | Compilez sur ps_1_2 version. | 
| ps_1_3 | Compilez sur ps_1_3 version. | 
| ps_1_4 | Compilez sur ps_1_4 version. | 
| ps_2_0 | Compilez sur ps_2_0 version. | 
| ps_2_a | Identique au profil de ps_2_0, avec les fonctionnalités supplémentaires suivantes disponibles pour que le compilateur cible :<ul><li>Le nombre de registres temporaires (r #) est supérieur ou égal à 22.</li><li>Swizzle source arbitraire.</li><li>Instructions de dégradé : DSX, DSY.</li><li>Prédication.</li><li>Aucune limite de lecture de texture dépendante.</li><li>Aucune limite pour le nombre d’instructions de texture.</li></ul> | 
| ps_2_b | Identique au profil de ps_2_0, avec les fonctionnalités supplémentaires suivantes disponibles pour que le compilateur cible :<ul><li>Le nombre de registres temporaires (r #) est supérieur ou égal à 32.</li><li>Aucune limite pour le nombre d’instructions de texture.</li></ul> | 
| ps_3_0 | Compilez sur ps_3_0 version. | 




 

Pour plus d’informations sur les différences entre les versions de nuanceur, consultez [différences de nuanceur de pixels](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
