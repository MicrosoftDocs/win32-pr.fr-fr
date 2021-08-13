---
title: Interface ID3DX11EffectGroup (D3dx11effect. h)
description: L’interface ID3DX11EffectGroup accède à un groupe d’effets. La durée de vie d’un objet ID3DX11EffectGroup est égale à la durée de vie de son objet ID3DX11Effect parent.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Interface ID3DX11EffectGroup Direct3D 11
- Interface ID3DX11EffectGroup Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa42a884be0abd15f0d16403a95d859d89cd472fc630b51ffe586e703e1a8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046227"
---
# <a name="id3dx11effectgroup-interface"></a>Interface ID3DX11EffectGroup

L’interface **ID3DX11EffectGroup** accède à un groupe d’effets.

La durée de vie d’un objet **ID3DX11EffectGroup** est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectGroup** possède ces méthodes.



| Méthode                                                                  | Description                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetAnnotationByIndex**](id3dx11effectgroup-getannotationbyindex.md) | Obtient une annotation par index.<br/>                        |
| [**GetAnnotationByName**](id3dx11effectgroup-getannotationbyname.md)   | Obtient une annotation par nom.<br/>                         |
| [**GetDesc**](id3dx11effectgroup-getdesc.md)                           | Obtient une description de groupe.<br/>                          |
| [**GetTechniqueByIndex**](id3dx11effectgroup-gettechniquebyindex.md)   | Obtient une technique par index.<br/>                          |
| [**GetTechniqueByName**](id3dx11effectgroup-gettechniquebyname.md)     | Obtient une technique par nom.<br/>                           |
| [**IsValid**](id3dx11effectgroup-isvalid.md)                           | Testez un effet pour voir s’il contient une syntaxe valide.<br/> |



 

## <a name="remarks"></a>Remarques

Pour obtenir une interface **ID3DX11EffectGroup** , appelez une méthode comme [**ID3DX11Effect :: GetGroupByName**](id3dx11effect-getgroupbyname.md).

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





