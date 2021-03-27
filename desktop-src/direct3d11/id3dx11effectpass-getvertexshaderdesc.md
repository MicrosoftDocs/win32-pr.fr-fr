---
title: Méthode ID3DX11EffectPass GetVertexShaderDesc (D3dx11effect. h)
description: Obtenir une description du nuanceur de sommets.
ms.assetid: 7e02a438-2ff4-4e32-bc16-d112aafa57cb
keywords:
- Méthode GetVertexShaderDesc Direct3D 11
- Méthode GetVertexShaderDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode GetVertexShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetVertexShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8c69bab360fa3d12ccfc1a701926183dad7bbe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953960"
---
# <a name="id3dx11effectpassgetvertexshaderdesc-method"></a>ID3DX11EffectPass :: GetVertexShaderDesc, méthode

Obtenir une description du nuanceur de sommets.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVertexShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDesc* 
</dt> <dd>

Type : **[ **D3DX11 \_ passe- \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)\***

Pointeur vers une description du nuanceur de sommets (consultez [**D3DX11 \_ passe \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

Une passe d’effet peut contenir des affectations d’état de rendu et des assignations d’objets Shader.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





