---
title: Générer des fonctions de rappel
description: Générer des fonctions de rappel
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Fonctions de rappel AVICap, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3666ea24a1d37402ffc13c09ca8ab95fcd19e1f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725853"
---
# <a name="yield-callback-functions"></a><span data-ttu-id="1658b-104">Générer des fonctions de rappel</span><span class="sxs-lookup"><span data-stu-id="1658b-104">Yield Callback Functions</span></span>

<span data-ttu-id="1658b-105">Les applications peuvent utiliser les fonctions de rappel yield pendant la capture en continu.</span><span class="sxs-lookup"><span data-stu-id="1658b-105">Applications can use yield callback functions during streaming capture.</span></span> <span data-ttu-id="1658b-106">(Une fonction de rappel yield se compose généralement d’une boucle de message qui appelle [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)et [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage).) La fenêtre de capture appelle la fonction de rappel yield au moins une fois pour chaque trame vidéo capturée, mais le taux exact dépend de la fréquence d’images et de la surcharge du pilote de capture et du disque.</span><span class="sxs-lookup"><span data-stu-id="1658b-106">(A yield callback function typically consists of a message loop that calls [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), and [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage).) The capture window calls the yield callback function at least once for every captured video frame, but the exact rate depends on the frame rate and the overhead of the capture driver and disk.</span></span>

 

 