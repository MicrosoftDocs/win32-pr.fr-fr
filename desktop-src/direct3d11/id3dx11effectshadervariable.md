---
title: Interface ID3DX11EffectShaderVariable (D3dx11effect. h)
description: Une interface de variable de nuanceur accède à une variable de nuanceur.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- Interface ID3DX11EffectShaderVariable Direct3D 11
- Interface ID3DX11EffectShaderVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992221"
---
# <a name="id3dx11effectshadervariable-interface"></a>Interface ID3DX11EffectShaderVariable

Une interface de variable de nuanceur accède à une variable de nuanceur.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectShaderVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderVariable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectShaderVariable** possède ces méthodes.



| Méthode                                                                                                           | Description                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**GetComputeShader**](id3dx11effectshadervariable-getcomputeshader.md)                                         | Obtenir un nuanceur de calcul.<br/>                       |
| [**GetDomainShader**](id3dx11effectshadervariable-getdomainshader.md)                                           | Obtenir un nuanceur de domaine.<br/>                        |
| [**GetGeometryShader**](id3dx11effectshadervariable-getgeometryshader.md)                                       | Obtenir un nuanceur Geometry.<br/>                      |
| [**GetHullShader**](id3dx11effectshadervariable-gethullshader.md)                                               | Obtenir un nuanceur de coque.<br/>                          |
| [**GetInputSignatureElementDesc**](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | Obtient une description de la signature d’entrée.<br/>         |
| [**GetOutputSignatureElementDesc**](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | Obtient une description de la signature de sortie.<br/>        |
| [**GetPatchConstantSignatureElementDesc**](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | Obtenir une description de la signature constante de patch.<br/> |
| [**GetPixelShader**](id3dx11effectshadervariable-getpixelshader.md)                                             | Obtenir un nuanceur de pixels.<br/>                         |
| [**GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md)                                               | Obtenir une description du nuanceur.<br/>                   |
| [**GetVertexShader**](id3dx11effectshadervariable-getvertexshader.md)                                           | Obtenir un nuanceur de sommets.<br/>                        |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effets 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





