---
description: Notez qu’au lieu d’utiliser cette fonction héritée, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’API D3DCompile. Compilez un nuanceur ou un effet à partir d’une ressource.
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: D3DX10CompileFromResource, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6b698700804ca767c953343e6d5a5e540ca77555
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922748"
---
# <a name="d3dx10compilefromresource-function"></a>D3DX10CompileFromResource fonction)

> [!Note]  
> Au lieu d’utiliser cette fonction héritée, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .

 

Compilez un nuanceur ou un effet à partir d’une ressource.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSrcModule* \[ dans\]
</dt> <dd>

Type : **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle du module de ressource contenant le nuanceur. HMODULE peut être obtenu avec la [fonction GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pSrcResource* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nom de la ressource contenant le nuanceur. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données est résolu en LPCSTR.

</dd> <dt>

*pSrcFileName* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

facultatif. Nom du fichier d’effet, qui est utilisé pour les messages d’erreur uniquement. Peut avoir la **valeur null**.

</dd> <dt>

*pDefines* \[ dans\]
</dt> <dd>

Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**

facultatif. Pointeur vers un tableau de définitions de macros (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). La dernière structure du tableau sert de terminateur et doit avoir tous les membres définis sur 0. S’il n’est pas utilisé, affectez la valeur **null** à *pDefines* .

</dd> <dt>

*pInclude* \[ dans\]
</dt> <dd>

Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Optionnel. Pointeur vers une interface d' [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) pour la gestion des fichiers include. Si vous affectez la **valeur null** , une erreur de compilation se produira si un nuanceur contient un \# include.

</dd> <dt>

*pFunctionName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur. Quand vous compilez un effet, **D3DX10CompileFromResource** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.

</dd> <dt>

*pProfile* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne qui spécifie le modèle de nuanceur ; peut être n’importe quel profil dans le [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)ou [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).

</dd> <dt>

*Flags1* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

[Indicateurs de compilation du nuanceur](d3d10-shader.md).

</dd> <dt>

*Flags2* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

[Indicateurs de compilation Effect](d3d10-graphics-reference-effect-constants.md). Quand vous compilez un nuanceur et non un fichier Effect, **D3DX10CompileFromResource** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de non-pointeur sur zéro si la fonction appelée ne l’utilise pas.

</dd> <dt>

*pPump* \[ dans\]
</dt> <dd>

Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)). Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.

</dd> <dt>

*ppShader* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Pointeur vers une [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) qui contient le nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.

</dd> <dt>

*ppErrorMsgs* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Pointeur vers une [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) qui contient une liste d’erreurs et d’avertissements qui se sont produits pendant la compilation. Ces erreurs et avertissements sont identiques à la sortie de débogage d’un débogueur.

</dd> <dt>

*pHResult* \[ à\]
</dt> <dd>

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Pointeur vers la valeur de retour. Peut avoir la **valeur null**. Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
