---
title: Méthode ID3DX11EffectShaderVariable GetHullShader (D3dx11effect. h)
description: Obtenir un nuanceur de coque.
ms.assetid: 18b2a8fc-2c53-4858-9aaa-00d0dc86adee
keywords:
- Méthode GetHullShader Direct3D 11
- Méthode GetHullShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, méthode GetHullShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetHullShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534e29d68402cba797a44d060782fe7a362fef6dfd01388902b7617d31f5c7fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533275"
---
# <a name="id3dx11effectshadervariablegethullshader-method"></a>ID3DX11EffectShaderVariable :: GetHullShader, méthode

Obtenir un nuanceur de coque.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetHullShader(
   UINT             ShaderIndex,
   ID3D11HullShader **ppPS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index du nuanceur.

</dd> <dt>

*ppPS* 
</dt> <dd>

Type : **[ **ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***

Pointeur vers un pointeur [**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader) qui sera défini sur le nuanceur de coque lors du retour.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Remarques

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

