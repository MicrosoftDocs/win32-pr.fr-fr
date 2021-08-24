---
title: Écriture d’applications WinSNMP avec plusieurs threads
description: L’implémentation de l’WinSNMP de Microsoft garantit que les opérations WinSNMP d’un processus ne modifient pas les paramètres WinSNMP d’un autre processus.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33ee400009204a1117eb54b8166ade2c10f3d1dd3317a8316d70fc8c2d606d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142732"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Écriture d’applications WinSNMP avec plusieurs threads

L’implémentation de l’WinSNMP de Microsoft garantit que les opérations WinSNMP d’un processus ne modifient pas les paramètres WinSNMP d’un autre processus.

Une application WinSNMP avec plusieurs threads doit s’assurer que les opérations WinSNMP qui définissent des paramètres au niveau de l’application sont thread-safe. Les fonctions qui définissent les paramètres au niveau de l’application sont [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) et [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode). Ces fonctions modifient les paramètres pour l’entité et le mode de traduction du contexte et le mode de retransmission.

Pour plus d’informations, consultez [threads multiples](/windows/desktop/ProcThread/multiple-threads) et [sécurité des threads et droits d’accès](/windows/desktop/ProcThread/thread-security-and-access-rights).

 

 