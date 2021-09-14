---
title: Interface ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Une interface d’échantillonneur accède à l’état de l’échantillonneur.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Interface ID3DX11EffectSamplerVariable Direct3D 11
- Interface ID3DX11EffectSamplerVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095374"
---
# <a name="id3dx11effectsamplervariable-interface"></a>Interface ID3DX11EffectSamplerVariable

Une interface d’échantillonneur accède à l’état de l’échantillonneur.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectSamplerVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectSamplerVariable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectSamplerVariable** possède ces méthodes.



| Méthode                                                                  | Description                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectsamplervariable-getbackingstore.md) | Obtient un pointeur vers une variable qui contient l’état de l’échantillonneur.<br/> |
| [**GetSampler**](id3dx11effectsamplervariable-getsampler.md)           | Obtient un pointeur vers une interface d’échantillonneur.<br/>                    |
| [**SetSampler**](id3dx11effectsamplervariable-setsampler.md)           | Définissez l’état de l’échantillonneur.<br/>                                       |
| [**UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)   | Rétablir un état d’échantillonneur précédemment défini.<br/>                   |



 

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

 

 





