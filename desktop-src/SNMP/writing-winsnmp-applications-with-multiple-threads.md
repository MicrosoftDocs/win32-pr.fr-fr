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
# <a name="writing-winsnmp-applications-with-multiple-threads"></a><span data-ttu-id="c317e-103">Écriture d’applications WinSNMP avec plusieurs threads</span><span class="sxs-lookup"><span data-stu-id="c317e-103">Writing WinSNMP Applications with Multiple Threads</span></span>

<span data-ttu-id="c317e-104">L’implémentation de l’WinSNMP de Microsoft garantit que les opérations WinSNMP d’un processus ne modifient pas les paramètres WinSNMP d’un autre processus.</span><span class="sxs-lookup"><span data-stu-id="c317e-104">The Microsoft WinSNMP implementation ensures that the WinSNMP operations of one process do not modify the WinSNMP settings of another process.</span></span>

<span data-ttu-id="c317e-105">Une application WinSNMP avec plusieurs threads doit s’assurer que les opérations WinSNMP qui définissent des paramètres au niveau de l’application sont thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c317e-105">A WinSNMP application with multiple threads must ensure that WinSNMP operations that set application-level parameters are thread-safe.</span></span> <span data-ttu-id="c317e-106">Les fonctions qui définissent les paramètres au niveau de l’application sont [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) et [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode).</span><span class="sxs-lookup"><span data-stu-id="c317e-106">The functions that set application-level parameters are [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) and [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode).</span></span> <span data-ttu-id="c317e-107">Ces fonctions modifient les paramètres pour l’entité et le mode de traduction du contexte et le mode de retransmission.</span><span class="sxs-lookup"><span data-stu-id="c317e-107">These functions modify settings for the entity and context translation mode and the retransmission mode.</span></span>

<span data-ttu-id="c317e-108">Pour plus d’informations, consultez [threads multiples](/windows/desktop/ProcThread/multiple-threads) et [sécurité des threads et droits d’accès](/windows/desktop/ProcThread/thread-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="c317e-108">For more information, see [Multiple Threads](/windows/desktop/ProcThread/multiple-threads) and [Thread Security and Access Rights](/windows/desktop/ProcThread/thread-security-and-access-rights).</span></span>

 

 