---
title: Générer des fonctions de rappel
description: Générer des fonctions de rappel
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Fonctions de rappel AVICap, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e87a3c986378bee05078b8cab28a0647827a1102ef1809558a47dcd5123af2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369133"
---
# <a name="yield-callback-functions"></a>Générer des fonctions de rappel

Les applications peuvent utiliser les fonctions de rappel yield pendant la capture en continu. (Une fonction de rappel yield se compose généralement d’une boucle de message qui appelle [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)et [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage).) La fenêtre de capture appelle la fonction de rappel yield au moins une fois pour chaque trame vidéo capturée, mais le taux exact dépend de la fréquence d’images et de la surcharge du pilote de capture et du disque.

 

 