---
title: Interface ID3DX11EffectDepthStencilVariable (D3dx11effect. h)
description: Une interface à profondeur variable de gabarit accède à l’état de gabarit de profondeur.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953965"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a>Interface ID3DX11EffectDepthStencilVariable

Une interface à profondeur variable de gabarit accède à l’état de gabarit de profondeur.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectDepthStencilVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilVariable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectDepthStencilVariable** possède ces méthodes.



| Méthode                                                                                         | Description                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | Obtient un pointeur vers une variable qui contient l’état du gabarit de profondeur.<br/> |
| [**GetDepthStencilState**](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | Obtient un pointeur vers une interface de stencil de profondeur.<br/>                    |
| [**SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | Définit l’état du stencil de profondeur.<br/>                                  |
| [**UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | Rétablit un État du stencil de profondeur précédemment défini.<br/>                  |



 

## <a name="remarks"></a>Notes

Une interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) est créée lorsqu’un effet est lu dans la mémoire.

Les variables d’effet sont enregistrées en mémoire dans le magasin de stockage ; Quand une technique est appliquée, les valeurs du magasin de stockage sont copiées sur l’appareil. Vous pouvez utiliser l’une ou l’autre de ces méthodes pour retourner l’État.

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

 

 





