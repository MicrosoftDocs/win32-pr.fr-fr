---
title: Portage des applications du système de fenêtre X
description: Portage des applications du système de fenêtre X
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL sur Windows, Portage
- portage vers OpenGL, système de fenêtre X
- Portage OpenGL, système X Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196871"
---
# <a name="porting-x-window-system-applications"></a>Portage des applications du système de fenêtre X

Comme Windows, le système de fenêtre X est un système de gestion d’événements et de message qui utilise des menus et des contrôles de fenêtre. Le code OpenGL de votre application système X Window est probablement situé dans des zones qui correspondent approximativement à l’emplacement où il apparaîtra lorsque vous le portagerez vers Windows. La majeure partie de votre code OpenGL ne changera pas, mais vous devez réécrire le code qui est spécifique au système X Window.

**Utilisez la procédure générale suivante pour porter les programmes OpenGL du système X Window vers Windows**

1.  Réécrivez le code spécifique au système X Window à l’aide d’un code Windows équivalent. Recherchez le code de création de fenêtre et de gestion d’événements. Le système de fenêtres X et les fenêtres sont des systèmes de gestion d’événements et de fenêtrage basés sur les messages, ce qui facilite la détermination de l’emplacement des modifications appropriées. (Toutefois, en particulier pour les applications volumineuses, la réécriture d’une application d’un système d’exploitation à un autre peut être une entreprise complexe et difficile.)
2.  Localisez tout code qui utilise des fonctions GLX. Il s’agit des fonctions que vous allez traduire en leurs fonctions Windows équivalentes.
3.  Traduisez les fonctions de format de pixel GLX et les fonctions visuelles/Dessinables au format de pixel Windows/OpenGL approprié et aux fonctions de contexte de périphérique.
4.  Traduisez les fonctions de contexte de rendu GLX en fonctions de contexte de rendu Windows/OpenGL.
5.  Traduisez les fonctions GLX pixmap en fonctions Windows équivalentes.
6.  Traduisez GLX trame et d’autres fonctions GLX en fonctions Windows appropriées.

 

 




