---
title: Interface ID3DX11EffectRasterizerVariable (D3dx11effect. h)
description: Une interface de la variable rastériseur accède à l’état du rastériseur.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- Interface ID3DX11EffectRasterizerVariable Direct3D 11
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4653936edc3fd2181f875b3a848e401b8fa24d318a1e48df4fa06e462ae3cf19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534185"
---
# <a name="id3dx11effectrasterizervariable-interface"></a>Interface ID3DX11EffectRasterizerVariable

Une interface de la variable rastériseur accède à l’état du rastériseur.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectRasterizerVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectRasterizerVariable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectRasterizerVariable** possède ces méthodes.



| Méthode                                                                                   | Description                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectrasterizervariable-getbackingstore.md)               | Obtient un pointeur vers une variable qui contient l’État rasteriser.<br/> |
| [**GetRasterizerState**](id3dx11effectrasterizervariable-getrasterizerstate.md)         | Obtient un pointeur vers une interface de rastérisation.<br/>                    |
| [**SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)         | Définit l’état du rastériseur.<br/>                                  |
| [**UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | Restaure un état de rastériseur précédemment défini.<br/>                  |



 

## <a name="remarks"></a>Remarques

Une interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) est créée lorsqu’un effet est lu dans la mémoire.

Les variables d’effet sont enregistrées en mémoire dans le magasin de stockage ; Quand une technique est appliquée, les valeurs du magasin de stockage sont copiées sur l’appareil. Vous pouvez utiliser l’une ou l’autre de ces méthodes pour retourner l’État.

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

 

 





