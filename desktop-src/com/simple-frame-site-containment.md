---
title: Relation contenant-contenu de site à cadre simple
description: Relation contenant-contenu de site à cadre simple
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939817"
---
# <a name="simple-frame-site-containment"></a>Relation contenant-contenu de site à cadre simple

Un contrôle conteneur est un contrôle ActiveX capable de contenir d’autres contrôles. Une zone de groupe qui contient une collection de cases d’option est un exemple de contrôle conteneur. Les contrôles de conteneur doivent définir le \_ bit d’État SIMPLEFRAME OLEMISC et doivent appeler l’implémentation [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) de son conteneur. Un conteneur de contrôles ActiveX qui prend en charge les contrôles de conteneur doit implémenter **IsimpleFrameSite**.

CATID-{157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Catégories de composant](component-categories.md)
</dt> </dl>

 

 




