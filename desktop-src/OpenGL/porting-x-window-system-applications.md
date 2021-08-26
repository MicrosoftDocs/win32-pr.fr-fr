---
title: Portage des applications du système de fenêtre X
description: Portage des applications du système de fenêtre X
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL sur Windows, portage
- portage vers OpenGL, système de fenêtre X
- Portage OpenGL, système X Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07a20de68df3806da40629252246f176beece0a4c3951180d484d9fadc6b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034759"
---
# <a name="porting-x-window-system-applications"></a>Portage des applications du système de fenêtre X

comme Windows, le système de fenêtre X est un système de gestion d’événements et de message qui utilise des menus et des contrôles de fenêtre. Le code OpenGL de votre application système X Window est probablement situé dans des zones qui correspondent approximativement à l’emplacement où il apparaîtra lorsque vous le passerez à Windows. La majeure partie de votre code OpenGL ne changera pas, mais vous devez réécrire le code qui est spécifique au système X Window.

**Utilisez la procédure générale suivante pour déplacer les programmes OpenGL du système X Window vers Windows**

1.  réécrivez le code spécifique au système X Window en utilisant un code d’Windows équivalent. Recherchez le code de création de fenêtre et de gestion d’événements. le système de fenêtres X et les Windows sont des systèmes de gestion d’événements et de fenêtrage basés sur les messages, ce qui facilite la détermination de l’emplacement des modifications appropriées. (Toutefois, en particulier pour les applications volumineuses, la réécriture d’une application d’un système d’exploitation à un autre peut être une entreprise complexe et difficile.)
2.  Localisez tout code qui utilise des fonctions GLX. il s’agit des fonctions que vous allez traduire en leurs fonctions Windows équivalentes.
3.  traduisez les fonctions de format de pixel GLX et les fonctions visuelles/dessinées en fonction appropriée Windows format de pixel/OpenGL et de contexte de périphérique.
4.  traduisez les fonctions de contexte de rendu GLX pour Windows fonctions de contexte de rendu/OpenGL.
5.  traduisez les fonctions GLX Pixmap en fonctions Windows équivalentes.
6.  traduisez GLX trame et d’autres fonctions GLX en fonctions Windows appropriées.

 

 




