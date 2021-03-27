---
title: Interface ID3DX11EffectBlendVariable (D3dx11effect. h)
description: L’interface de variable Blend accède à l’État Blend.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- Interface ID3DX11EffectBlendVariable Direct3D 11
- Interface ID3DX11EffectBlendVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954009"
---
# <a name="id3dx11effectblendvariable-interface"></a>Interface ID3DX11EffectBlendVariable

L’interface de variable Blend accède à l’État Blend.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectBlendVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectBlendVariable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectBlendVariable** possède ces méthodes.



| Méthode                                                                    | Description                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBackingStore**](id3dx11effectblendvariable-getbackingstore.md)     | Obtient un pointeur vers une variable d’état de fusion.<br/>  |
| [**GetBlendState**](id3dx11effectblendvariable-getblendstate.md)         | Obtient un pointeur vers une interface d’état de fusion.<br/> |
| [**SetBlendState**](id3dx11effectblendvariable-setblendstate.md)         | Définit l’état de fusion d’un effet.<br/>             |
| [**UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md) | Restaure un état de fusion précédemment défini.<br/>     |



 

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

 

 





