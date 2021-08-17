---
title: Ouverture et fermeture d’une session WinSNMP
description: Pour ouvrir une session, une application appelle la fonction SnmpCreateSession.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41871c9adc2f7fcefc04b5816b29685ad6b1516a6238c1855ed41e878d5b2736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009197"
---
# <a name="opening-and-closing-a-winsnmp-session"></a>Ouverture et fermeture d’une session WinSNMP

Pour ouvrir une session, une application appelle la fonction [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) . Si la fonction se termine correctement, l’implémentation de l’WinSNMP Microsoft ouvre une session et la fonction retourne un identificateur de session sous la forme d’un descripteur de **\_ session HSNMP** . Toutes les fonctions WinSNMP qui retournent des variables de handle incluent l’identificateur de session en tant que paramètre d’entrée. Cela permet à l’implémentation d’utiliser le handle pour gérer efficacement les ressources au niveau de la session.

Une application peut avoir plusieurs sessions ouvertes simultanément. Plusieurs sessions au sein d’une application peuvent partager des variables de handle.

Si l’implémentation ne peut pas ouvrir une session en raison de limitations de ressources, elle retourne l' \_ échec SNMPAPI quand l’application appelle [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession). Si l’application appelle ensuite la fonction [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) , elle retourne une \_ erreur d’allocation SNMPAPI \_ .

Un appel à la fonction [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) permet à l’implémentation de libérer toutes les ressources restantes et de fermer la session.

Pour plus d’informations, consultez [objets de handle de ressource](resource-handle-objects.md) et [sessions WinSNMP](winsnmp-sessions.md).

 

 




