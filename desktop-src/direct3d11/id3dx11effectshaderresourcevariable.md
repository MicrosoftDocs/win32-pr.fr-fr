---
title: Interface ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Une interface de nuanceur-ressource accède à une ressource de nuanceur.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- Interface ID3DX11EffectShaderResourceVariable Direct3D 11
- Interface ID3DX11EffectShaderResourceVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996296"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a>Interface ID3DX11EffectShaderResourceVariable

Une interface de nuanceur-ressource accède à une ressource de nuanceur.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectShaderResourceVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderResourceVariable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectShaderResourceVariable** possède ces méthodes.



| Méthode                                                                           | Description                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [**GetResource**](id3dx11effectshaderresourcevariable-getresource.md)           | Obtenir une ressource de nuanceur.<br/>            |
| [**GetResourceArray**](id3dx11effectshaderresourcevariable-getresourcearray.md) | Obtient un tableau de ressources de nuanceur.<br/> |
| [**SetResource**](id3dx11effectshaderresourcevariable-setresource.md)           | Définissez une ressource de nuanceur.<br/>            |
| [**SetResourceArray**](id3dx11effectshaderresourcevariable-setresourcearray.md) | Définir un tableau de ressources de nuanceur.<br/> |



 

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

 

 





