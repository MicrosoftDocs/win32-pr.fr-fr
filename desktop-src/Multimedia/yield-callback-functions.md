---
title: Générer des fonctions de rappel
description: Générer des fonctions de rappel
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Fonctions de rappel AVICap, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3666ea24a1d37402ffc13c09ca8ab95fcd19e1f7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369415"
---
# <a name="yield-callback-functions"></a>Générer des fonctions de rappel

Les applications peuvent utiliser les fonctions de rappel yield pendant la capture en continu. (Une fonction de rappel yield se compose généralement d’une boucle de message qui appelle [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)et [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage).) La fenêtre de capture appelle la fonction de rappel yield au moins une fois pour chaque trame vidéo capturée, mais le taux exact dépend de la fréquence d’images et de la surcharge du pilote de capture et du disque.

 

 