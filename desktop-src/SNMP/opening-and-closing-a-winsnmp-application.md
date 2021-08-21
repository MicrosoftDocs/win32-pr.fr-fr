---
title: Ouverture et fermeture d’une application WinSNMP
description: L’application WinSNMP doit appeler la fonction SnmpStartup avec succès avant d’appeler une autre fonction WinSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aa18f437f8b1a430ad27b40b838859d2e00641bcb4532602715548b370acce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009247"
---
# <a name="opening-and-closing-a-winsnmp-application"></a>Ouverture et fermeture d’une application WinSNMP

L’application WinSNMP doit appeler la fonction [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) avec succès avant d’appeler une autre fonction winsnmp. La fonction **SnmpStartup** permet à l’implémentation de Microsoft WinSNMP d’effectuer des procédures d’initialisation. La fonction retourne également à l’application la version de l’API WinSNMP prise en charge par l’implémentation, le niveau de communications SNMP qu’elle prend en charge, ainsi que les modes de traduction et de retransmission par défaut de l’implémentation.

L’application WinSNMP doit appeler la fonction [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) lorsque l’application n’a plus besoin des services de l’implémentation. Même si **SnmpCleanup** permet à l’implémentation de libérer toutes les ressources allouées à l’application, il est recommandé que l’application appelle d’abord la fonction [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) une fois pour chaque session WinSNMP ouverte, afin d’optimiser les performances de l’implémentation. L’application WinSNMP doit appeler [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) comme dernière fonction WinSNMP avant qu’elle ne se termine.

 

 




