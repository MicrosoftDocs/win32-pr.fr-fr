---
description: Créer un processeur de données asynchrones pour un nuanceur.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: D3DX10CreateAsyncCompilerProcessor, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: f5e7011d868b46196293f441d76d182156fb0ba1431227d6bf01212f8c809249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303464"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a>D3DX10CreateAsyncCompilerProcessor fonction)

Créer un processeur de données asynchrones pour un nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFileName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne qui contient le nom de fichier du nuanceur.

</dd> <dt>

*pDefines* \[ dans\]
</dt> <dd>

Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**

Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.

</dd> <dt>

*pInclude* \[ dans\]
</dt> <dd>

Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))). Ce paramètre peut être **NULL**.

</dd> <dt>

*pFunctionName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur. Quand vous compilez un effet, **D3DX10CreateAsyncCompilerProcessor** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.

</dd> <dt>

*pProfile* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md) ou le modèle de nuanceur.

</dd> <dt>

*Flags1* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

[Indicateurs de compilation du nuanceur](d3d10-shader.md).

</dd> <dt>

*Flags2* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

[Indicateurs de compilation Effect](d3d10-graphics-reference-effect-constants.md). Quand vous compilez un nuanceur et non un fichier Effect, **D3DX10CreateAsyncCompilerProcessor** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.

</dd> <dt>

*ppCompiledShader* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Adresse d’un pointeur vers l’effet compilé (consultez [**ID3D10Blob interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppErrorBuffer* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Adresse d’un pointeur vers des erreurs de compilation (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppDataProcessor* \[ à\]
</dt> <dd>

Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

 

 
