---
title: Relation contenant-contenu de site à cadre simple
description: Relation contenant-contenu de site à cadre simple
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d356d6cc4993702ac571a800ad2abbfe378e8a8fe06ddc80225d81f0fe21a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129854"
---
# <a name="simple-frame-site-containment"></a>Relation contenant-contenu de site à cadre simple

un contrôle conteneur est un contrôle ActiveX qui est capable de contenir d’autres contrôles. Une zone de groupe qui contient une collection de cases d’option est un exemple de contrôle conteneur. Les contrôles de conteneur doivent définir le \_ bit d’État SIMPLEFRAME OLEMISC et doivent appeler l’implémentation [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) de son conteneur. un conteneur de contrôle ActiveX qui prend en charge les contrôles de conteneur doit implémenter **ISimpleFrameSite**.

CATID-{157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Catégories de composant](component-categories.md)
</dt> </dl>

 

 




