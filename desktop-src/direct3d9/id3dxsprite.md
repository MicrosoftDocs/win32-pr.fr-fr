---
description: L’interface ID3DXSprite fournit un ensemble de méthodes qui simplifient le processus de dessin de sprites à l’aide de Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Interface ID3DXSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d5786096fb9c38188d73d613fd11efd97c2401e9f8ae9c7eb4a05dfe1dc1e6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729245"
---
# <a name="id3dxsprite-interface"></a>Interface ID3DXSprite

L’interface ID3DXSprite fournit un ensemble de méthodes qui simplifient le processus de dessin de sprites à l’aide de Microsoft Direct3D.

## <a name="members"></a>Membres

L’interface **ID3DXSprite** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSprite** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXSprite** possède ces méthodes.



| Méthode                                                | Description                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Début**](id3dxsprite--begin.md)                   | Prépare un appareil pour le dessin des sprites.<br/>                                                                                                                                                                            |
| [**Dessin**](id3dxsprite--draw.md)                     | Ajoute un sprite à la liste des sprites regroupés par lots.<br/>                                                                                                                                                                     |
| [**End**](id3dxsprite--end.md)                       | Appelle [**ID3DXSprite :: Flush**](id3dxsprite--flush.md) et restaure l’état de l’appareil pour qu’il se trouvait avant l’appel de [**ID3DXSprite :: Begin**](id3dxsprite--begin.md) .<br/>                                            |
| [**Purge**](id3dxsprite--flush.md)                   | Force tous les sprites regroupés par lot à être envoyés à l’appareil. Les États des appareils restent tels qu’ils étaient après le dernier appel à [**ID3DXSprite :: Begin**](id3dxsprite--begin.md). La liste des sprites regroupés par lot est alors effacée.<br/> |
| [**GetDevice**](id3dxsprite--getdevice.md)           | Récupère l’appareil associé à l’objet Sprite.<br/>                                                                                                                                                           |
| [**GetTransform**](id3dxsprite--gettransform.md)     | Obtient la transformation de sprite.<br/>                                                                                                                                                                                        |
| [**OnLostDevice**](id3dxsprite--onlostdevice.md)     | Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu ou avant de réinitialiser un appareil.<br/>                              |
| [**OnResetDevice**](id3dxsprite--onresetdevice.md)   | Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.<br/>                                                                                                                                                   |
| [**SetTransform**](id3dxsprite--settransform.md)     | Définit la transformation Sprite.<br/>                                                                                                                                                                                        |
| [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) | Définit la transformation de vue universelle de gauche pour un sprite. Un appel à cette méthode est requis avant d’effectuer un billboarding ou de trier des sprites.<br/>                                                                                 |
| [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) | Définit la transformation de la vue universelle droitier pour un sprite. Un appel à cette méthode est requis avant d’effectuer un billboarding ou de trier des sprites.<br/>                                                                                |



 

## <a name="remarks"></a>Remarques

L’interface **ID3DXSprite** est obtenue en appelant la fonction [**D3DXCreateSprite**](d3dxcreatesprite.md) .

L’application appelle généralement en premier [**ID3DXSprite :: Begin**](id3dxsprite--begin.md), qui permet de contrôler l’état de rendu de l’appareil, la fusion alpha, la transformation et le tri des sprites. Ensuite, pour chaque sprite à afficher, appelez [**ID3DXSprite ::D RAW**](id3dxsprite--draw.md). **ID3DXSprite ::D RAW** peut être appelé à plusieurs reprises pour stocker un nombre quelconque de sprites. Pour afficher les sprites regroupés par lot sur l’appareil, appelez [**ID3DXSprite :: end**](id3dxsprite--end.md) ou [**ID3DXSprite :: Flush**](id3dxsprite--flush.md).

Le type LPD3DXSPRITE est défini comme un pointeur vers l’interface **ID3DXSprite** .


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
