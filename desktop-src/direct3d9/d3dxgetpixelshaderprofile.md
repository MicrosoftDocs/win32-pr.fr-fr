---
description: Retourne le nom du profil HLSL (High-Level Shader Language) le plus élevé pris en charge par un appareil donné.
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
ms.openlocfilehash: ad1f430a95b1ff2173dceb1e0561dccf3d0ee88d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953848"
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

## <a name="return-value"></a>Valeur retournée

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom du profil HLSL.

Si l’appareil ne prend pas en charge les nuanceurs de pixels, la fonction retourne la **valeur null**.

## <a name="remarks"></a>Notes

Un profil de nuanceur spécifie la version du nuanceur d’assembly à utiliser et les fonctionnalités disponibles pour le compilateur HLSL lors de la compilation d’un nuanceur. Le tableau suivant répertorie les profils de nuanceur de pixels pris en charge.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Profil de nuanceur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ps_1_1</td>
<td>Compilez sur ps_1_1 version.</td>
</tr>
<tr class="even">
<td>ps_1_2</td>
<td>Compilez sur ps_1_2 version.</td>
</tr>
<tr class="odd">
<td>ps_1_3</td>
<td>Compilez sur ps_1_3 version.</td>
</tr>
<tr class="even">
<td>ps_1_4</td>
<td>Compilez sur ps_1_4 version.</td>
</tr>
<tr class="odd">
<td>ps_2_0</td>
<td>Compilez sur ps_2_0 version.</td>
</tr>
<tr class="even">
<td>ps_2_a</td>
<td>Identique au profil de ps_2_0, avec les fonctionnalités supplémentaires suivantes disponibles pour que le compilateur cible :
<ul>
<li>Le nombre de registres temporaires (r #) est supérieur ou égal à 22.</li>
<li>Swizzle source arbitraire.</li>
<li>Instructions de dégradé : DSX, DSY.</li>
<li>Prédication.</li>
<li>Aucune limite de lecture de texture dépendante.</li>
<li>Aucune limite pour le nombre d’instructions de texture.</li>
</ul></td>
</tr>
<tr class="odd">
<td>ps_2_b</td>
<td>Identique au profil de ps_2_0, avec les fonctionnalités supplémentaires suivantes disponibles pour que le compilateur cible :
<ul>
<li>Le nombre de registres temporaires (r #) est supérieur ou égal à 32.</li>
<li>Aucune limite pour le nombre d’instructions de texture.</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_3_0</td>
<td>Compilez sur ps_3_0 version.</td>
</tr>
</tbody>
</table>



 

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

 

 
