---
title: D3DX11CreateAsyncCompilerProcessor, fonction (D3DX11async. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes. Créer un processeur de données asynchrones pour un nuanceur.'
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- Fonction D3DX11CreateAsyncCompilerProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5d3767bafda4f1914d37b7baacf599335877c30de216282f172ebe55739920
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124904"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a>D3DX11CreateAsyncCompilerProcessor fonction)

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.

 

Créer un processeur de données asynchrones pour un nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFileName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Chaîne qui contient le nom de fichier du nuanceur.

</dd> <dt>

*pDefines* \[ dans\]
</dt> <dd>

Type : **const d3d11 \_ Shader \_ macro \***

Tableau de macros de nuanceur se terminant par un caractère NULL ; Affectez-lui la valeur **null** pour ne spécifier aucune macro.

</dd> <dt>

*pInclude* \[ dans\]
</dt> <dd>

Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Pointeur vers une interface include. Ce paramètre peut être **NULL**.

</dd> <dt>

*pFunctionName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur. Quand vous compilez un effet, **D3DX11CreateAsyncCompilerProcessor** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas..

</dd> <dt>

*pProfile* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Chaîne qui spécifie le profil de nuanceur ou le modèle de nuanceur ; peut être n’importe quel profil dans le nuancier Model 2, Shader Model 3, Shader Model 4 ou Shader Model 5. Le profil peut également être pour le type d’effet (par exemple, FX \_ 4 \_ 1).

</dd> <dt>

*Flags1* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indicateurs de compilation du nuanceur.

</dd> <dt>

*Flags2* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indicateurs de compilation Effect. Quand vous compilez un nuanceur et non un fichier Effect, **D3DX11CreateAsyncCompilerProcessor** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de non-pointeur sur zéro si la fonction appelée ne l’utilise pas.

</dd> <dt>

*ppCompiledShader* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Adresse d’un pointeur vers l’effet compilé.

</dd> <dt>

*ppErrorBuffer* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Adresse d’un pointeur vers des erreurs de compilation.

</dd> <dt>

*ppDataProcessor* \[ à\]
</dt> <dd>

Type : **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarques

Il n’y a aucune implémentation du chargeur asynchrone en dehors de D3DX 10 et D3DX 11.

pour les applications Windows store, les exemples DirectX (par exemple, l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluent le module **BasicLoader** qui utilise le Windows Runtime modèle de programmation asynchrone ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

pour les applications de bureau Win32, vous pouvez utiliser le [runtime d’accès concurrentiel](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) pour implémenter un modèle semblable au Windows Runtime modèle de programmation asynchrone.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

