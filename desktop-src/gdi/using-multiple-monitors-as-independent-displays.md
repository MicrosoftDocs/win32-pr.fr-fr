---
description: Lorsque vous utilisez plusieurs écrans comme des affichages indépendants, le bureau contient un affichage ou un ensemble d’affichages.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Utilisation de plusieurs moniteurs comme affichages indépendants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710672e02e8ea7244e09c21b876197033e5f17144433b8f530ad8e52cd6806e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468249"
---
# <a name="using-multiple-monitors-as-independent-displays"></a>Utilisation de plusieurs moniteurs comme affichages indépendants

Lorsque vous utilisez plusieurs écrans comme des affichages indépendants, le bureau contient un affichage ou un ensemble d’affichages. Cet ensemble d’affichages comprend toujours l’analyse principale et se comporte comme indiqué dans les autres sections de cette rubrique. Une application peut utiliser n’importe quelle autre analyse comme un affichage indépendant.

> [!Note]  
> l’utilisation d’autres moniteurs comme des affichages indépendants n’est pas prise en charge sur les pilotes qui sont implémentés sur le modèle WDDM (Windows Display Driver Model).

 

Le gestionnaire de fenêtres ne sait rien des affichages indépendants. Ils sont entièrement contrôlés par l’application et aucune fonction du gestionnaire de fenêtrage n’est disponible pour l’application (tous les appels du gestionnaire de fenêtres passent automatiquement à l’affichage principal). Chaque affichage indépendant a sa propre origine et ses coordonnées horizontales et verticales, et est accessible via les fonctions GDI telles que [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) ou les fonctions DirectX telles que **DirectDrawCreate**.

Pour localiser les affichages indépendants, appelez [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) et recherchez les affichages qui n’ont pas de \_ périphérique d’affichage \_ attaché \_ à \_ l’indicateur de bureau dans la structure du [**\_ périphérique d’affichage**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .

Une application peut ouvrir un affichage en appelant


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



Dans cet appel, le paramètre *lpszDisplayName* est l’un des noms d’appareil retournés par [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) et *lpDevMode* est une description du mode graphique de cet appareil. Le HDC qui en résulte peut être utilisé pour effectuer une opération graphique sur l’appareil.

 

 



