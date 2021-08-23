---
title: D3DX11CompileFromFile, fonction (D3DX11async. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API D3DCompileFromFile. Compilez un nuanceur ou un effet à partir d’un fichier.'
ms.assetid: 91a1a339-50da-4f86-9b55-6af246a60482
keywords:
- Fonction D3DX11CompileFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a62a5a3d60dc62317fdd6f08e99faea025a172f77af7f10fd48e6752fb1b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989869"
---
# <a name="d3dx11compilefromfile-function"></a>D3DX11CompileFromFile fonction)

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’une des API de compilation HLSL, comme l’API [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) .

 

Compilez un nuanceur ou un effet à partir d’un fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrcFile* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom du fichier qui contient le code du nuanceur. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données est résolu en LPCSTR.

</dd> <dt>

*pDefines* \[ dans\]
</dt> <dd>

Type : **const [**D3D10 \_ Shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Facultatif. Pointeur vers un tableau de définitions de macros (consultez la [**\_ \_ macro de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). La dernière structure du tableau sert de terminateur et doit avoir tous les membres définis sur 0. S’il n’est pas utilisé, affectez la valeur **null** à *pDefines* .

</dd> <dt>

*pInclude* \[ dans\]
</dt> <dd>

Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Facultatif. Pointeur vers une interface pour la gestion des fichiers include. Si vous affectez la **valeur null** , une erreur de compilation se produira si un nuanceur contient un \# include.

</dd> <dt>

*pFunctionName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur. Quand vous compilez un effet, **D3DX11CompileFromFile** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.

</dd> <dt>

*pProfile* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Chaîne qui spécifie le modèle de nuanceur ; peut être n’importe quel profil dans le nuancier Model 2, Shader Model 3, Shader Model 4 ou Shader Model 5. Le profil peut également être pour le type d’effet (par exemple, FX \_ 4 \_ 1).

</dd> <dt>

*Flags1* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

[**Indicateurs de compilation**](/windows/desktop/direct3dhlsl/d3dcompile-constants)du nuanceur.

</dd> <dt>

*Flags2* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

[**Indicateurs de compilation**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)Effect. Quand vous compilez un nuanceur et non un fichier Effect, **D3DX11CompileFromFile** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de non-pointeur sur zéro si la fonction appelée ne l’utilise pas.

</dd> <dt>

*pPump* \[ dans\]
</dt> <dd>

Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Pointeur vers une interface de pompage de thread (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)). Utilisez **null** pour spécifier que cette fonction ne doit pas être retournée tant qu’elle n’est pas terminée.

</dd> <dt>

*ppShader* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Pointeur vers la mémoire qui contient le nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.

</dd> <dt>

*ppErrorMsgs* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Pointeur vers la mémoire qui contient une liste d’erreurs et d’avertissements qui se sont produits pendant la compilation. Ces erreurs et avertissements sont identiques à la sortie de débogage d’un débogueur.

</dd> <dt>

*pHResult* \[ à\]
</dt> <dd>

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Pointeur vers la valeur de retour. Peut avoir la **valeur null**. Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

**D3DX11CompileFromFile** retourne E \_ INVALIDARG si vous fournissez une valeur non **null** au paramètre *pHResult* lorsque vous fournissez la valeur **null** au paramètre *pPump* . Pour plus d’informations sur cette situation, consultez la section Notes.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur **D3DX11CompileFromFile**, consultez [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).

Vous devez fournir la **valeur null** au paramètre *pHResult* si vous fournissez également la **valeur null** au paramètre *pPump* . Dans le cas contraire, vous ne pouvez pas créer de nuanceur à l’aide du code de nuanceur compilé que **D3DX11CompileFromFile** retourne dans la mémoire vers laquelle pointe le paramètre *ppShader* . Pour créer un nuanceur à partir d’un code de nuanceur conforme, vous appelez l’une des méthodes d’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) suivantes :

-   [**CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**CreatePixelShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

En outre, si vous fournissez une valeur non **null** à *pHResult* lorsque vous fournissez la valeur **null** à *pPump*, **D3DX11CompileFromFile** retourne le code d’erreur de l’E \_ INVALIDARG.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

