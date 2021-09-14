---
title: Relation contenant-contenu de site à cadre simple
description: Relation contenant-contenu de site à cadre simple
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095505"
---
# <a name="simple-frame-site-containment"></a>Relation contenant-contenu de site à cadre simple

un contrôle conteneur est un contrôle ActiveX qui est capable de contenir d’autres contrôles. Une zone de groupe qui contient une collection de cases d’option est un exemple de contrôle conteneur. Les contrôles de conteneur doivent définir le \_ bit d’État SIMPLEFRAME OLEMISC et doivent appeler l’implémentation [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) de son conteneur. un conteneur de contrôle ActiveX qui prend en charge les contrôles de conteneur doit implémenter **ISimpleFrameSite**.

CATID-{157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Catégories de composant](component-categories.md)
</dt> </dl>

 

 




