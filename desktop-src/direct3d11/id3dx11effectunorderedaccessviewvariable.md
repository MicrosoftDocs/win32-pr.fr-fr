---
title: Interface ID3DX11EffectUnorderedAccessViewVariable (D3dx11effect. h)
description: Accède à une vue d’accès non ordonnée.
ms.assetid: f78dc8c5-c85a-48cf-b579-f2937aa5ce2a
keywords:
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d48161ad4d9fc1773889fab0e8a0fd9a21ec793e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992141"
---
# <a name="id3dx11effectunorderedaccessviewvariable-interface"></a>Interface ID3DX11EffectUnorderedAccessViewVariable

Accède à une vue d’accès non ordonnée.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectUnorderedAccessViewVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectUnorderedAccessViewVariable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectUnorderedAccessViewVariable** possède ces méthodes.



| Méthode                                                                                                      | Description                                        |
|:------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetUnorderedAccessView**](id3dx11effectunorderedaccessviewvariable-getunorderedaccessview.md)           | Obtenir un mode d’accès non ordonné.<br/>           |
| [**GetUnorderedAccessViewArray**](id3dx11effectunorderedaccessviewvariable-getunorderedaccessviewarray.md) | Obtient un tableau de vues d’accès non ordonnées.<br/> |
| [**SetUnorderedAccessView**](id3dx11effectunorderedaccessviewvariable-setunorderedaccessview.md)           | Définissez un mode d’accès non ordonné.<br/>           |
| [**SetUnorderedAccessViewArray**](id3dx11effectunorderedaccessviewvariable-setunorderedaccessviewarray.md) | Définissez un tableau de vues d’accès non ordonnées.<br/> |



 

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

 

 





