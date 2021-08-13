---
title: Interface ID3DX11EffectDepthStencilViewVariable (D3dx11effect. h)
description: Une interface à profondeur variable de vue de gabarit accède à une vue de stencil de profondeur.
ms.assetid: 316bf0cc-a7cd-4a40-932a-d566e3c2001e
keywords:
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d445f2250ec29dbc4b964fecf538a4272985d2396c3cd0e605ca751aa810b3d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535917"
---
# <a name="id3dx11effectdepthstencilviewvariable-interface"></a>Interface ID3DX11EffectDepthStencilViewVariable

Une interface à profondeur variable de vue de gabarit accède à une vue de stencil de profondeur.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectDepthStencilViewVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilViewVariable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectDepthStencilViewVariable** possède ces méthodes.



| Méthode                                                                                     | Description                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**GetDepthStencil**](id3dx11effectdepthstencilviewvariable-getdepthstencil.md)           | Obtenir une ressource de vue de gabarit de profondeur.<br/>            |
| [**GetDepthStencilArray**](id3dx11effectdepthstencilviewvariable-getdepthstencilarray.md) | Obtenir un tableau de ressources de profondeur-stencil-vue.<br/> |
| [**SetDepthStencil**](id3dx11effectdepthstencilviewvariable-setdepthstencil.md)           | Définissez une ressource de vue de gabarit de profondeur.<br/>            |
| [**SetDepthStencilArray**](id3dx11effectdepthstencilviewvariable-setdepthstencilarray.md) | Définir un tableau de ressources de profondeur-stencil-affichage.<br/> |



 

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

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effets 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





