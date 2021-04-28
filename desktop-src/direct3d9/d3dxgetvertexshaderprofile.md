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
ms.openlocfilehash: 70d6cdf79fdd91e819d54702682515aa3e4810b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114457"
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

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom du profil HLSL.

Si l’appareil ne prend pas en charge les nuanceurs vertex, la fonction retourne la **valeur null**.

## <a name="remarks"></a>Notes 

Un profil de nuanceur spécifie la version du nuanceur d’assembly à utiliser et les fonctionnalités disponibles pour le compilateur HLSL lors de la compilation d’un nuanceur. Le tableau suivant répertorie les profils de nuanceur de sommets pris en charge.



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
<td>vs_1_1</td>
<td>Compilez sur vs_1_1 version.</td>
</tr>
<tr class="even">
<td>vs_2_0</td>
<td>Compilez sur vs_2_0 version.</td>
</tr>
<tr class="odd">
<td>vs_2_a</td>
<td>Identique au profil de vs_2_0, avec les fonctionnalités supplémentaires suivantes disponibles pour que le compilateur cible :
<ul>
<li>Le nombre de registres temporaires (r #) est supérieur ou égal à 13.</li>
<li>Instruction de contrôle de Flow dynamique.</li>
<li>Prédication.</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_3_0</td>
<td>Compilez sur vs_3_0 version.</td>
</tr>
</tbody>
</table>



 

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

 

 
