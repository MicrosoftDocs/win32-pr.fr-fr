---
description: L’objet InkOverlay peut être attaché à un contrôle de fenêtre et utilisé pour activer la fonctionnalité d’encre de base.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Effacement à l’aide de l’objet InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6d95e7939bc53c534d3bfc9a542e40b95fbce05234000e24b107f0f2625eae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110939"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a>Effacement à l’aide de l’objet InkOverlay

L’objet [**InkOverlay**](inkoverlay-class.md) peut être attaché à un contrôle de fenêtre et utilisé pour activer la fonctionnalité d’encre de base. Vous pouvez utiliser l’objet **InkOverlay** pour effacer l’encre en affectant à la propriété [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) la valeur **Delete**. Vous pouvez ensuite définir la propriété [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) sur les membres **Stroke** ou **point** de [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode). La définition de la propriété **EraserMode** sur **Stroke** efface les traits entiers. La définition de la propriété **EraserMode** sur **point** efface l’encre sur laquelle le curseur passe.

 

 



