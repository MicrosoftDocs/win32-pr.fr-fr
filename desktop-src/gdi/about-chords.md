---
description: Une corde est une région délimitée par l’intersection d’une ellipse et un segment de ligne appelé sécante. L’illustration suivante montre une corde dessinée à l’aide de la fonction corde.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: À propos des cordes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3bad0d17d34386ada7c7c3b46bb1bcc4db5f9a2ce572ce78c33f8f4b6af909
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400529"
---
# <a name="about-chords"></a>À propos des cordes

Une *corde* est une région délimitée par l’intersection d’une ellipse et un segment de ligne appelé *sécante*. L’illustration suivante montre une corde dessinée à l’aide de la fonction [**corde**](/windows/desktop/api/Wingdi/nf-wingdi-chord) .

![illustration d’un Elipse, montrant deux radials, une sécante et une corde](images/csfsh-02.png)

Lors de l’appel de [**corde**](/windows/win32/api/wingdi/nf-wingdi-chord), une application fournit les coordonnées des angles supérieur gauche et inférieur droit du rectangle englobant de l’ellipse, ainsi que les coordonnées de deux points définissant deux radiales. Un radial est une ligne dessinée du centre du rectangle englobant d’une ellipse à un point sur l’ellipse.

Lorsque le système dessine la partie courbée du cordon, il le fait en utilisant la direction d’arc actuelle pour le contexte de périphérique spécifié. La direction de l’arc par défaut est dans le sens inverse des aiguilles. Vous pouvez demander à votre application de réinitialiser la direction de l’arc en appelant la fonction [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .

 

 
