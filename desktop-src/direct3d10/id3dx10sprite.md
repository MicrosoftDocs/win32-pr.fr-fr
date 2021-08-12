---
description: L’interface ID3DX10Sprite fournit un ensemble de méthodes qui simplifient le processus de dessin de sprites à l’aide de Microsoft Direct3D. Cette interface peut fonctionner sur un ensemble de plusieurs sprites.
ms.assetid: 3703f272-f631-41c0-a0d5-e7cf2d4ae145
title: Interface ID3DX10Sprite (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8495d967d0f512e16a06506e73ac1a35bf5fa380924cdbe6513b06a43502b137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301927"
---
# <a name="id3dx10sprite-interface"></a>Interface ID3DX10Sprite

L’interface ID3DX10Sprite fournit un ensemble de méthodes qui simplifient le processus de dessin de sprites à l’aide de Microsoft Direct3D. Cette interface peut fonctionner sur un ensemble de plusieurs sprites.

## <a name="members"></a>Membres

L’interface **ID3DX10Sprite** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10Sprite** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX10Sprite** possède ces méthodes.



| Méthode                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Début**](id3dx10sprite-begin.md)                                   | Préparez un appareil pour dessiner des sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md)       | Ajoutez un tableau de sprites au lot de sprites à restituer. Elle doit être appelée entre les appels à [**ID3DX10Sprite :: Begin**](id3dx10sprite-begin.md) et [**ID3DX10Sprite :: end**](id3dx10sprite-end.md), et [**ID3DX10Sprite :: Flush**](id3dx10sprite-flush.md) doit être appelé avant end pour envoyer tous les sprites traités par lot à l’appareil pour le rendu. Cette méthode de dessin est particulièrement utile lorsque vous dessinez un petit nombre de sprites que vous souhaitez mettre en mémoire tampon dans un grand lot, tel que des polices.<br/>                                                                                                                                                                              |
| [**DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md)     | Dessinez un tableau de sprites. Cela envoie immédiatement les sprites à l’appareil pour le rendu, ce qui est différent de [**ID3DX10Sprite ::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) qui ajoute uniquement un tableau de sprites à un lot de sprites à restituer lorsque [**ID3DX10Sprite :: Flush**](id3dx10sprite-flush.md) est appelé. Cette méthode de dessin est particulièrement utile lors du dessin d’un grand nombre de sprites qui ont déjà été triés sur l’UC (ou qui n’ont pas besoin d’être triés), comme dans un système de particules. Elle doit être appelée entre les appels à [**ID3DX10Sprite :: Begin**](id3dx10sprite-begin.md) et [**ID3DX10Sprite :: end**](id3dx10sprite-end.md).<br/> |
| [**End**](id3dx10sprite-end.md)                                       | Appelez-le après ID3DX10Sprite :: Flush. Si \_ \_ \_ l’état de l’enregistrement d3dx10 Sprite a été spécifié lors de l’appel de ID3DX10Sprite :: Begin, cette API restaure l’état de l’appareil sur la manière dont il se trouvait avant l’appel de ID3DX10Sprite :: Begin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Purge**](id3dx10sprite-flush.md)                                   | Forcer l’envoi de tous les sprites par lot à l’appareil. Les États des appareils restent tels qu’ils étaient après le dernier appel à ID3DX10Sprite :: Begin. La liste des sprites regroupés par lot est alors effacée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**GetDevice**](id3dx10sprite-getdevice.md)                           | Récupérez l’appareil associé à l’objet Sprite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**GetProjectionTransform**](id3dx10sprite-getprojectiontransform.md) | Obtient la matrice de projection Sprite qui est appliquée à tous les sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**GetViewTransform**](id3dx10sprite-getviewtransform.md)             | Obtient la transformation de vue qui s’applique à tous les sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SetProjectionTransform**](id3dx10sprite-setprojectiontransform.md) | Définissez la matrice de projection pour tous les sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**SetViewTransform**](id3dx10sprite-setviewtransform.md)             | Définissez la transformation de vue qui s’applique à tous les sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Notes

L’interface ID3DX10Sprite est obtenue en appelant la fonction [**D3DX10CreateSprite**](d3dx10createsprite.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
