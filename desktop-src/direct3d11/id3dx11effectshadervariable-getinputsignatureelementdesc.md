---
title: Méthode ID3DX11EffectShaderVariable GetInputSignatureElementDesc (D3dx11effect. h)
description: Obtient une description de la signature d’entrée.
ms.assetid: 45b1fd25-1005-48fd-8a61-561ea2c273e5
keywords:
- Méthode GetInputSignatureElementDesc Direct3D 11
- Méthode GetInputSignatureElementDesc Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, méthode GetInputSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetInputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf788370c26da1ba773d797de544b1a64750d90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116306"
---
# <a name="id3dx11effectshadervariablegetinputsignatureelementdesc-method"></a>ID3DX11EffectShaderVariable :: GetInputSignatureElementDesc, méthode

Obtient une description de la signature d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetInputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index de nuanceur de base zéro.

</dd> <dt>

*Element* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index d’élément de nuanceur de base zéro.

</dd> <dt>

*pDesc* 
</dt> <dd>

Type : **[ **\_ paramètre de signature d3d11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

Pointeur vers une description de paramètre (consultez [**d3d11 \_ signature \_ Parameter \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

Un effet contient un ou plusieurs nuanceurs ; chaque nuanceur a une signature d’entrée et de sortie ; chaque signature contient un ou plusieurs éléments (ou paramètres). L’index du nuanceur identifie le nuanceur et l’index de l’élément identifie l’élément (ou le paramètre) dans la signature du nuanceur.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

