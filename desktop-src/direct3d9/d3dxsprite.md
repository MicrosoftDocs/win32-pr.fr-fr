---
description: 'Les indicateurs suivants sont utilisés pour spécifier les options de rendu Sprite dans le paramètre flags de la méthode Begin :'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4dbf3e80e7cf6f7884d778860f9de61f5193f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997316"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

Les indicateurs suivants sont utilisés pour spécifier les options de rendu Sprite dans le paramètre flags de la méthode [**Begin**](id3dxsprite--begin.md) :



| \#définition                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXSPRITE \_ DONOTSAVESTATE           | L’état de l’appareil ne doit pas être enregistré ou restauré lorsque [**Begin**](id3dxsprite--begin.md) ou [**end**](id3dxsprite--end.md) est appelé.                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | L’état de rendu de l’appareil ne doit pas être modifié lorsque [**Begin**](id3dxsprite--begin.md) est appelé. L’appareil est supposé être dans un état valide pour dessiner les vertex contenant UsageIndex = 0 dans la \_ position D3DDECLUSAGE, D3DDECLUSAGE \_ texcoord et les \_ données de couleur D3DDECLUSAGE.                                                                                                                                                     |
| D3DXSPRITE \_ OBJECTSPACE              | Les transformations de projection, de vue et de projection ne sont pas modifiées. Les transformations actuellement définies sur l’appareil sont utilisées pour transformer les sprites lorsque les sprites traités par lot sont dessinés (lorsque le [**vidage**](id3dxsprite--flush.md) ou la [**fin**](id3dxsprite--end.md) est appelé). Si cet indicateur n’est pas spécifié, les transformations universelles, de vue et de projection sont modifiées afin que les sprites soient dessinés en coordonnées d’espace d’écran.              |
| \_Panneau D3DXSPRITE                | Chaque sprite est pivoté sur son centre afin d’être orienté vers la visionneuse. [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) ou [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) doit être appelé en premier.                                                                                                                                                                                                                |
| D3DXSPRITE \_ ALPHABLEND               | Active la fusion alpha avec D3DRS \_ ALPHATESTENABLE défini sur **true** (pour une valeur alpha différente de zéro). D3DBLEND \_ SRCALPHA correspond à l’état de Blend source et D3DBLEND \_ INVSRCALPHA correspond à l’État Blend de destination dans les appels à [**SetRenderState**](/windows/desktop/api). Consultez [État de la fusion alpha (Direct3D 9)](alpha-blending-state.md). [**ID3DXFont**](id3dxfont.md) s’attend à ce que cet indicateur soit défini lors du dessin de texte. |
| \_Texture de tri D3DXSPRITE \_            | Triez les sprites par texture avant le dessin. Cela peut améliorer les performances lors du dessin de sprites de profondeur uniforme qui ne se chevauchent pas. Vous pouvez également combiner la \_ \_ texture de tri D3DXSPRITE avec D3DXSPRITE \_ sort \_ Depth \_ FRONTTOBACK ou D3DXSPRITE \_ sort \_ Depth \_ BACKTOFRONT. Cela permet de trier la liste des sprites par profondeur en premier et texture seconde.<br/>                                                                           |
| D3DXSPRITE \_ profondeur de tri \_ \_ FRONTTOBACK | Les sprites sont triés par profondeur dans l’ordre avant-arrière avant le dessin. Cette procédure est recommandée lors du dessin de sprites opaques de profondeurs variables. Vous pouvez combiner D3DXSPRITE \_ de \_ profondeur de tri \_ FRONTTOBACK avec la \_ \_ texture de tri D3DXSPRITE pour trier d’abord par profondeur, et seconde par texture.<br/>                                                                                                                                   |
| D3DXSPRITE \_ profondeur de tri \_ \_ BACKTOFRONT | Les sprites sont triés par profondeur dans le sens de l’arrière-plan avant le dessin. Cette procédure est recommandée lors du dessin de sprites transparents de profondeurs variables. Vous pouvez combiner D3DXSPRITE \_ de \_ profondeur de tri \_ BACKTOFRONT avec la \_ \_ texture de tri D3DXSPRITE pour trier d’abord par profondeur, et seconde par texture.<br/>                                                                                                                              |
| D3DXSPRITE \_ do \_ not \_ ADDREF \_ texture | Désactive l’appel de AddRef () sur chaque dessin, et Release () sur Flush () pour obtenir de meilleures performances.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Informations constantes



|                          |             |
|--------------------------|-------------|
| En-tête                   | d3dx9core. h |
| Système d’exploitation minimal | Windows 98  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




