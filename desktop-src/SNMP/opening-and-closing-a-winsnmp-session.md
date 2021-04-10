---
title: Ouverture et fermeture d’une session WinSNMP
description: Pour ouvrir une session, une application appelle la fonction SnmpCreateSession.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029534"
---
# <a name="opening-and-closing-a-winsnmp-session"></a>Ouverture et fermeture d’une session WinSNMP

Pour ouvrir une session, une application appelle la fonction [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) . Si la fonction se termine correctement, l’implémentation de l’WinSNMP Microsoft ouvre une session et la fonction retourne un identificateur de session sous la forme d’un descripteur de **\_ session HSNMP** . Toutes les fonctions WinSNMP qui retournent des variables de handle incluent l’identificateur de session en tant que paramètre d’entrée. Cela permet à l’implémentation d’utiliser le handle pour gérer efficacement les ressources au niveau de la session.

Une application peut avoir plusieurs sessions ouvertes simultanément. Plusieurs sessions au sein d’une application peuvent partager des variables de handle.

Si l’implémentation ne peut pas ouvrir une session en raison de limitations de ressources, elle retourne l' \_ échec SNMPAPI quand l’application appelle [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession). Si l’application appelle ensuite la fonction [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) , elle retourne une \_ erreur d’allocation SNMPAPI \_ .

Un appel à la fonction [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) permet à l’implémentation de libérer toutes les ressources restantes et de fermer la session.

Pour plus d’informations, consultez [objets de handle de ressource](resource-handle-objects.md) et [sessions WinSNMP](winsnmp-sessions.md).

 

 




