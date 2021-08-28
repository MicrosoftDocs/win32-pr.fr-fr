---
description: Le rectangle englobant cumulé est le plus petit rectangle englobant la partie d’une fenêtre ou d’une zone client affectée par les opérations de dessin récentes.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Rectangle englobant cumulé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d90b2f92b50dbaede477c0a712be970bf0af46b25c5e5edd956fe428d46559
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779349"
---
# <a name="accumulated-bounding-rectangle"></a>Rectangle englobant cumulé

Le *rectangle englobant cumulé* est le plus petit rectangle englobant la partie d’une fenêtre ou d’une zone client affectée par les opérations de dessin récentes. Une application peut utiliser ce rectangle pour déterminer facilement l’étendue des modifications provoquées par les opérations de dessin. Il est parfois utilisé conjointement avec [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) pour déterminer la partie de la zone cliente qui doit être redessinée après l’effacement du verrou de mise à jour.

Une application utilise la fonction [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (en spécifiant l' \_ activation de DCB) pour commencer à accumuler le rectangle englobant. Le système accumule ensuite les points pour le rectangle englobant lorsque l’application utilise le contexte de périphérique d’affichage spécifié. L’application peut récupérer le rectangle englobant actuel à tout moment à l’aide de la fonction [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) . L’application arrête l’accumulation en appelant à nouveau **SetBoundsRect** , en spécifiant la \_ valeur de désactivation de DCB.

 

 



