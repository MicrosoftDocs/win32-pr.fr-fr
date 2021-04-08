---
title: Modification de la stratégie de retransmission
description: L’implémentation de l’WinSNMP de Microsoft fournit une prise en charge de la stratégie de retransmission en stockant une valeur de délai d’attente et un nombre de tentatives pour l’application WinSNMP dans une base de données.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840073"
---
# <a name="changing-the-retransmission-policy"></a><span data-ttu-id="73123-103">Modification de la stratégie de retransmission</span><span class="sxs-lookup"><span data-stu-id="73123-103">Changing the Retransmission Policy</span></span>

<span data-ttu-id="73123-104">L’implémentation de l’WinSNMP de Microsoft fournit une prise en charge de la stratégie de retransmission en stockant une valeur de délai d’attente et un nombre de tentatives pour l’application WinSNMP dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="73123-104">The Microsoft WinSNMP implementation provides retransmission policy support by storing a time-out value and a retry count for the WinSNMP application in a database.</span></span> <span data-ttu-id="73123-105">L’implémentation stocke des valeurs pour des entités de destination individuelles.</span><span class="sxs-lookup"><span data-stu-id="73123-105">The implementation stores values for individual destination entities.</span></span> <span data-ttu-id="73123-106">L’implémentation fournit initialement des valeurs par défaut pour ces éléments, mais une application peut ajouter ou modifier des valeurs pour des entités individuelles.</span><span class="sxs-lookup"><span data-stu-id="73123-106">The implementation initially supplies default values for these elements, but an application can add or modify values for individual entities.</span></span>

<span data-ttu-id="73123-107">Un appel aux fonctions [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) et [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) retourne les valeurs de délai d’attente et de nombre de tentatives pour une entité de destination spécifique.</span><span class="sxs-lookup"><span data-stu-id="73123-107">A call to the [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) and [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) functions returns the time-out and retry count values for a specific destination entity.</span></span> <span data-ttu-id="73123-108">Pour modifier la valeur du délai d’attente, une application WinSNMP doit appeler la fonction [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) .</span><span class="sxs-lookup"><span data-stu-id="73123-108">To change the time-out value, a WinSNMP application must call the [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) function.</span></span> <span data-ttu-id="73123-109">Pour modifier la valeur du nombre de tentatives, l’application doit appeler la fonction [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) .</span><span class="sxs-lookup"><span data-stu-id="73123-109">To change the retry count value the application must call the [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) function.</span></span> <span data-ttu-id="73123-110">Les paramètres mis à jour affectent les nouvelles demandes de message SNMP à l’entité de destination.</span><span class="sxs-lookup"><span data-stu-id="73123-110">The updated settings affect new SNMP message requests to the destination entity.</span></span>

 

 




