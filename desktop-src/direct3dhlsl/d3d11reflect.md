---
title: D3D11Reflect fonction)
description: Obtient un pointeur vers une interface de réflexion.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- D3D11Reflect fonction HLSL
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116282"
---
# <a name="d3d11reflect-function"></a>D3D11Reflect fonction)

Obtient un pointeur vers une interface de réflexion.

## <a name="syntax"></a>Syntaxe

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrcData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Pointeur vers les données sources comme code HLSL compilé.

</dd> <dt>

*SrcDataSize* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**

Longueur de *pSrcData*.

</dd> <dt>

*ppReflector* \[ à\]
</dt> <dd>

Type : **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***

Adresse d’un pointeur vers l’interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

Retourne l’un des codes de retour décrits dans la rubrique [codes de retour Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).

## <a name="remarks"></a>Notes

La fonction de compilateur inline **D3D11Reflect** est un wrapper pour la fonction de compilateur [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) . **D3D11Reflect** peut récupérer uniquement une interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) à partir d’un nuanceur. **D3DReflect** peut récupérer une interface **ID3D11ShaderReflection** ou une interface de réflexion direct3d 10 ou Direct3D 10,1, par exemple, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).

Le code du nuanceur contient des métadonnées qui peuvent être inspectées à l’aide des API de réflexion.

Le code suivant montre comment récupérer une interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) à partir d’un nuanceur.


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DCompiler. inl</dt> </dl>     |
| Bibliothèque<br/> | <dl> <dt>D3dcompiler \_ 47. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dcompiler \_47.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

