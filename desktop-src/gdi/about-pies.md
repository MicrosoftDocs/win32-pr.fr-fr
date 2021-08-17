---
description: Un secteur est une région délimitée par l’intersection d’une courbe ellipse et deux radiales. L’illustration suivante montre un graphique à secteurs dessiné à l’aide de la fonction Pie.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: À propos des secteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e447e313a3088bbf9a72c790115fb3bb25770017cf13ce7922685fd18ccfe671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966459"
---
# <a name="about-pies"></a>À propos des secteurs

Un *secteur* est une région délimitée par l’intersection d’une courbe ellipse et deux radiales. L’illustration suivante montre un graphique à secteurs dessiné à l’aide de la fonction [**Pie**](/windows/desktop/api/Wingdi/nf-wingdi-pie) .

![Illustration montrant une ellipse avec un graphique en secteurs ombré](images/csfsh-03.png)

Lors de l’appel de [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), une application fournit les coordonnées des angles supérieur gauche et inférieur droit du rectangle englobant de l’ellipse, ainsi que les coordonnées de deux points définissant deux radiales.

Lorsque le système dessine la partie courbée du graphique, il utilise la direction d’arc actuelle pour le contexte de périphérique donné. La direction de l’arc par défaut est dans le sens inverse des aiguilles. Une application peut réinitialiser la direction de l’arc en appelant la fonction [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .

 

 
