---
description: Constantes utilisées pour définir la priorité d’une ressource dans SetPriority.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 367d50292b283cc7a0dcdef42b2e2c270099e314dc61c8d590e7ef2a1091a4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751329"
---
# <a name="d3d9_resource_priority"></a>Priorité de la \_ ressource d3d9 \_

Constantes utilisées pour définir la priorité d’une ressource dans [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).



| Constante/valeur                                                                                                                                                                                                                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <dt>**D3d9 \_ 0x28000000 \_ \_ minimale**</dt> de la priorité de ressource <dt></dt> </dl> | La ressource a la priorité la plus faible possible. Cette constante marque la ressource comme inutilisée et pour l’éviction. La ressource doit être supprimée dès qu’une autre ressource requiert l’espace mémoire occupé par la ressource.<br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <dt>**D3d9 \_ Priorité de ressource \_ \_ basse**</dt> <dt>0x50000000</dt> </dl>             | La ressource est planifiée avec une priorité basse. Le placement de la ressource n’est pas critique et le système d’exploitation effectue un travail minimal pour rechercher un emplacement pour la ressource. Le marquage d’une ressource en basse priorité permet d’autres ressources plus critiques d’occuper la mémoire la plus rapide.<br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <dt>**D3d9 \_ 0x78000000 \_ \_ normale de priorité de ressource**</dt> <dt></dt> </dl>    | La ressource est planifiée avec une priorité normale. La position de la ressource est importante pour les performances, mais elle n’est pas critique. Le système d’exploitation doit tenter de placer la ressource qui est marquée comme normale à l’emplacement préféré de la ressource au lieu d’une ressource de faible priorité. En règle générale, les textures sont marquées comme normales.<br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <dt>**D3d9 \_ Priorité de ressource \_ \_ élevée**</dt> <dt>0xA0000000</dt> </dl>          | La ressource est planifiée avec une priorité élevée. Le positionnement de la ressource est essentiel pour les performances. Le système d’exploitation tente toujours de placer la ressource marquée comme haute dans l’emplacement préféré de la ressource au lieu d’une ressource de priorité basse ou normale. En général, les cibles de rendu sont marquées comme étant élevées.<br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <dt>**D3d9 \_ 0xc8000000 \_ \_ maximale**</dt> de la priorité de ressource <dt></dt> </dl> | La ressource a la priorité maximale possible. Cette constante marque la priorité de la ressource comme étant épinglée de manière réversible. Une ressource épinglée n’est supprimée de la mémoire que s’il n’existe aucune autre façon de résoudre la mémoire requise d’une mémoire tampon DMA. Le système d’exploitation tente de fractionner une mémoire tampon DMA à sa taille minimale et supprime toutes les autres ressources qui ne sont pas épinglées et qui ne sont pas épinglées de manière réversible avant de supprimer une ressource épinglée. <br/> |



## <a name="remarks"></a>Remarques

Les valeurs autres que la priorité de **\_ ressource d3d9 \_ \_ minimale** et la **priorité de \_ ressource d3d9 \_ \_ maximale** sont traitées comme des indicateurs par le planificateur.

Vous pouvez utiliser des niveaux de priorité autres que les valeurs définies précédemment dans cette rubrique. Par exemple, le marquage d’une ressource avec un niveau de priorité de 0x78000001 indique que la priorité de la ressource est légèrement supérieure à la normale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
