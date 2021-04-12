---
title: Écriture d’applications WinSNMP avec plusieurs threads
description: L’implémentation de l’WinSNMP de Microsoft garantit que les opérations WinSNMP d’un processus ne modifient pas les paramètres WinSNMP d’un autre processus.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6b7991968c5c5efafa898758c3c60cad1abb2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382262"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Écriture d’applications WinSNMP avec plusieurs threads

L’implémentation de l’WinSNMP de Microsoft garantit que les opérations WinSNMP d’un processus ne modifient pas les paramètres WinSNMP d’un autre processus.

Une application WinSNMP avec plusieurs threads doit s’assurer que les opérations WinSNMP qui définissent des paramètres au niveau de l’application sont thread-safe. Les fonctions qui définissent les paramètres au niveau de l’application sont [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) et [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode). Ces fonctions modifient les paramètres pour l’entité et le mode de traduction du contexte et le mode de retransmission.

Pour plus d’informations, consultez [threads multiples](/windows/desktop/ProcThread/multiple-threads) et [sécurité des threads et droits d’accès](/windows/desktop/ProcThread/thread-security-and-access-rights).

 

 