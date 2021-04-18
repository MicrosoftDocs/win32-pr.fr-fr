---
title: Ajout de User-Controlled lecture
description: Ajout de User-Controlled lecture
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- MCIWndCreate fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511829"
---
# <a name="adding-user-controlled-playback"></a>Ajout de User-Controlled lecture

Vous pouvez ajouter une lecture contrôlée par l’utilisateur à une application existante en appelant la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) comme suit :


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



Les paramètres [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identifient les descripteurs de la fenêtre parente et de l’instance de module associée à la fenêtre MCIWnd. Ils spécifient également les styles de fenêtre et le nom de fichier (ou nom de périphérique) à associer à la fenêtre MCIWnd.

**MCIWndCreate** effectue automatiquement les étapes suivantes, pour les autres classes de fenêtres, vous devez implémenter vous-même dans votre code :

1.  Inscrivez la classe de fenêtre MCIWnd.
2.  Créez la fenêtre MCIWnd.
3.  Charge le contenu spécifié.
4.  Établissez la position de lecture actuelle au début du contenu.
5.  Affichez le contrôle de l’appareil.
6.  Affichez la zone de lecture de la fenêtre, si nécessaire.

 

 




