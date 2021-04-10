---
title: Ouverture et fermeture des appareils de mixage
description: Ouverture et fermeture des appareils de mixage
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- audio multimédia, ouverture des appareils de mixage
- audio, ouverture des appareils de mixage
- mixages audio, ouverture
- mixages, ouverture
- audio multimédia, fermeture des appareils de mixage
- audio, fermeture des appareils de mixage
- mixages audio, fermeture
- mixageeurs, fermeture
- ouverture des appareils de mixage
- fermeture des appareils de mixage
- identificateurs d’appareil et descripteurs d’appareil
- mixages audio, identificateurs d’appareil et descripteurs d’appareil
- mélangeurs, identificateurs d’appareil et descripteurs d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031088"
---
# <a name="opening-and-closing-mixer-devices"></a>Ouverture et fermeture des appareils de mixage

Lorsque vous souhaitez utiliser un appareil de mixage, vous pouvez commencer à l’utiliser, ou vous pouvez ouvrir explicitement l’appareil avant de l’utiliser. L’ouverture explicite d’un appareil de mixage offre deux avantages principaux :

-   Cela garantit l’existence continue de cet appareil de mixage.
-   Elle vous permet de recevoir des notifications de changement de ligne et de contrôle audio.

Vous pouvez utiliser la fonction [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) pour ouvrir explicitement un appareil de mixage. Cette fonction prend comme paramètres un identificateur de périphérique, un pointeur vers un emplacement de mémoire et d’autres valeurs propres à chaque type d’appareil. L’emplacement de la mémoire est rempli avec un handle d’appareil. Utilisez ce handle d’appareil pour identifier l’appareil mixer ouvert lors de l’appel d’autres fonctions de mixage audio. Tant qu’il existe un handle de périphérique de mixage, l’appareil continue à exister dans le système. Si une modification de configuration se produit sur le périphérique de mixage et qu’elle n’a pas été explicitement ouverte, votre application risque de ne pas pouvoir y accéder.

> [!Note]  
> La différence entre les identificateurs d’appareil et les descripteurs d’appareil est importante. Des descripteurs d’appareil sont retournés lorsque vous ouvrez un pilote de périphérique à l’aide de **mixerOpen**. Les identificateurs d’appareil sont déterminés implicitement à partir du nombre d’appareils présents dans un système. ce nombre est obtenu à l’aide de la fonction [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) .

 

Vous pouvez utiliser la fonction [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) pour fermer un appareil de mixage. Vous devez fermer l’appareil une fois que vous avez fini de l’utiliser.

 

 