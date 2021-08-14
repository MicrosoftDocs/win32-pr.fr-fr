---
description: 'Le tableau suivant décrit les threads que les événements d’objet InkOverlay peuvent déclencher. EventThreadsCursorButtonDownFires sur le threadCursorButtonUpFires d’encre de l’encre threadCursorDownFires sur le threadCursorInRangeFires d’encre sur l’encre threadCursorOutOfRangeFires sur l’encre threadDoubleClick (Automation uniquement). Se déclenche sur l’interface utilisateur de l’application threadDoubleClick (bibliothèque managée uniquement). Se déclenche sur l’interface utilisateur threadGestureFires de l’application sur le threadMouseDownFires d’encre sur l’interface utilisateur threadMouseMoveFires de l’application sur le threadMouseUpFires d’interface utilisateur de l’application sur l’interface utilisateur threadMouseWheelFires de l’application sur l’interface utilisateur threadNewInAirPacketsFires de l’application sur le thread d’encre, ou sur le thread qui met à jour l’objet InkOverlay.  Sélection de propertySelectionChangingFires sur le threadSelectionMovedFires d’encre sur l’encre threadSelectionMovingFires sur le threadSelectionResizedFires d’encre sur l’encre threadSelectionResizingFires sur l’encre threadStrokeFires sur l’encre threadStrokesDeletedFires sur l’encre threadStrokesDeletingFires sur l’encre threadSystemGestureFires sur l’encre threadTabletAddedFires sur l’encre threadTabletRemovedFires sur le thread d’encre '
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: Événements de l’objet InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531ee197a14edf3ce0aa8595bdbcdb3ea2937d9cf863dcc6e95690088ed8ee96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218962"
---
# <a name="inkoverlay-object-events"></a>Événements de l’objet InkOverlay

Le tableau suivant décrit les threads que les événements d’objet [**InkOverlay**](inkoverlay-class.md) peuvent déclencher.



| Événement                                                                             | Threads                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkoverlay-cursorbuttondown.md)                           | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**CursorButtonUp**](inkoverlay-cursorbuttonup.md)                               | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**CursorDown**](inkoverlay-cursordown.md)                                       | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**CursorInRange**](inkoverlay-cursorinrange.md)                                 | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**CursorOutOfRange**](inkoverlay-cursoroutofrange.md)                           | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (Automation uniquement).                  | Se déclenche sur le thread d’interface utilisateur de l’application<br/>                                                                                                          |
| [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (bibliothèque managée uniquement). | Se déclenche sur le thread d’interface utilisateur de l’application<br/>                                                                                                                           |
| [**Mouvement**](inkoverlay-gesture.md)                                             | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**MouseDown**](inkoverlay-mousedown.md)                                         | Se déclenche sur le thread d’interface utilisateur de l’application<br/>                                                                                                                           |
| [**MouseMove**](inkoverlay-mousemove.md)                                         | Se déclenche sur le thread d’interface utilisateur de l’application<br/>                                                                                                                           |
| [**Lâché**](inkoverlay-mouseup.md)                                             | Se déclenche sur le thread d’interface utilisateur de l’application<br/>                                                                                                                           |
| [**MouseWheel**](inkoverlay-mousewheel.md)                                       | Se déclenche sur le thread d’interface utilisateur de l’application<br/>                                                                                                                           |
| [**NewInAirPackets**](inkoverlay-newinairpackets.md)                             | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**NewPackets**](inkoverlay-newpackets.md)                                       | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**Toile**](inkoverlay-painted.md)                                             | Se déclenche sur le thread d’interface utilisateur de l’application<br/>                                                                                                                           |
| [**Peinture**](inkoverlay-painting.md)                                           | Se déclenche sur le thread d’interface utilisateur de l’application<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | Se déclenche sur le thread d’encre, ou sur le thread qui met à jour la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) de l’objet [**InkOverlay**](inkoverlay-class.md)<br/> |
| [**SelectionChanging**](inkoverlay-selectionchanging.md)                         | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)                               | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)                             | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**SelectionResized**](inkoverlay-selectionresized.md)                           | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**SelectionResizing**](inkoverlay-selectionresizing.md)                         | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**Stroke**](inkoverlay-stroke.md)                                               | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)                               | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)                             | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**SystemGesture**](inkoverlay-systemgesture.md)                                 | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**TabletAdded**](inkoverlay-tabletadded.md)                                     | Se déclenche sur le thread Ink<br/>                                                                                                                                        |
| [**TabletRemoved**](inkoverlay-tabletremoved.md)                                 | Se déclenche sur le thread Ink<br/>                                                                                                                                        |



 

 

