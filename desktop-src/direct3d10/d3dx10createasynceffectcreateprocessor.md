---
description: Créer un pool d’effets de manière asynchrone.
ms.assetid: 50c55751-26de-4002-9a89-8e5ab59dda79
title: D3DX10CreateAsyncEffectCreateProcessor, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 573efc51214031afe66f6cfd552bbda634d15142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522344"
---
# <a name="d3dx10createasynceffectcreateprocessor-function"></a>D3DX10CreateAsyncEffectCreateProcessor fonction)

Créer un pool d’effets de manière asynchrone.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateAsyncEffectCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _In_        ID3D10EffectPool     *pPool,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppProcessor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFileName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne qui contient le nom de fichier de l’effet.

</dd> <dt>

*pDefines* \[ dans\]
</dt> <dd>

Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**

Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.

</dd> <dt>

*pInclude* \[ dans\]
</dt> <dd>

Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.

</dd> <dt>

*pProfile* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md) ou le modèle de nuanceur.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Options de compilation HLSL (voir [indicateurs de nuanceur](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*FXFlags* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Appliquer des options de compilation (voir [indicateurs de compilation et d’effet](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) qui utilisera les ressources.

</dd> <dt>

*pPool* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***

Pointeur vers un pool d’effets (voir [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) pour le partage de variables entre les effets.

</dd> <dt>

*ppErrorBuffer* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Adresse d’un pointeur vers la mémoire (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient des erreurs d’effet de compilation, le cas échéant.

</dd> <dt>

*ppProcessor* \[ à\]
</dt> <dd>

Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Adresse d’un pointeur vers le processeur de données asynchrones (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
