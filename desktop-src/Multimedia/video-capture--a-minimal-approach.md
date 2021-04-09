---
title: Vidéo capture une approche minime
description: Vidéo capture une approche minime
ms.assetid: e39ff590-69c0-4927-90c2-786c6082068f
keywords:
- Video for Windows (VFW), capture vidéo
- VFW (vidéo pour Windows), capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a65d5d5bbdc00dfd947c5d917e514d72e3ac069
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842173"
---
# <a name="video-capture-a-minimal-approach"></a>Capture vidéo : approche minimale

La capture vidéo numérise un flux de données vidéo et audio, et la stocke sur un disque dur ou tout autre type de dispositif de stockage persistant. Cette section décrit comment ajouter une forme simple de capture vidéo à une application à l’aide de trois instructions de code. Elle explique également comment arrêter ou abandonner une session de capture en envoyant des messages à la fenêtre de capture.

Une fenêtre de capture AVICap gère les détails de la capture audio et vidéo en continu dans les fichiers AVI. Cela permet de libérer votre application de l’implication au format de fichier AVI, à la gestion des mémoires tampons audio et vidéo, ainsi qu’à l’accès de bas niveau des pilotes de périphériques vidéo et audio. AVICap fournit une interface flexible pour les applications. Vous pouvez ajouter la capture vidéo à votre application, en utilisant uniquement les lignes de code suivantes :


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



Une interface de macro est également disponible et offre une alternative à l’utilisation de la fonction [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) et améliore la lisibilité d’une application. L’exemple suivant utilise l’interface de macro pour ajouter la capture vidéo à une application.


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



Une fois que votre application a créé une fenêtre de capture de la classe de fenêtre AVICap et que vous l’avez connectée à un pilote vidéo, la fenêtre de capture est prête à capturer les données. À ce stade, votre application peut simplement envoyer le message de séquence de l' [**\_ embout \_ WM**](wm-cap-sequence.md) (ou la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) ) pour commencer la capture.

À l’aide des paramètres par défaut, \_ \_ la séquence de l’embout WM lance la capture de l’entrée vidéo et audio dans un fichier nommé CAPTURE.AVI. La capture se poursuit jusqu’à ce que l’un des événements suivants se produise :

-   L’utilisateur appuie sur la touche Échap ou sur le bouton de la souris.
-   Votre application s’arrête ou abandonne l’opération de capture.
-   Le disque est saturé.

Dans une application, vous pouvez arrêter la diffusion en continu de données capturées dans un fichier en envoyant le message [**WM \_ Cap \_ Stop**](wm-cap-stop.md) (ou macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) ) à une fenêtre de capture. Vous pouvez également abandonner l’opération de capture en envoyant le message [**WM \_ Cap \_ Abort**](wm-cap-abort.md) (ou la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) ) à une fenêtre de capture.

 

 