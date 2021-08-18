---
title: Ajout de User-Controlled lecture
description: Ajout de User-Controlled lecture
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- MCIWndCreate fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62d4e4af43be9877ec5bf3fae452e44ae415bc47047448cb65b64ad3446e0b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941817"
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

 

 




