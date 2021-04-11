---
title: Ouverture et fermeture d’une application WinSNMP
description: L’application WinSNMP doit appeler la fonction SnmpStartup avec succès avant d’appeler une autre fonction WinSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029536"
---
# <a name="opening-and-closing-a-winsnmp-application"></a><span data-ttu-id="68dc6-103">Ouverture et fermeture d’une application WinSNMP</span><span class="sxs-lookup"><span data-stu-id="68dc6-103">Opening and Closing a WinSNMP Application</span></span>

<span data-ttu-id="68dc6-104">L’application WinSNMP doit appeler la fonction [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) avec succès avant d’appeler une autre fonction winsnmp.</span><span class="sxs-lookup"><span data-stu-id="68dc6-104">The WinSNMP application must call the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function successfully before it calls any other WinSNMP function.</span></span> <span data-ttu-id="68dc6-105">La fonction **SnmpStartup** permet à l’implémentation de Microsoft WinSNMP d’effectuer des procédures d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="68dc6-105">The **SnmpStartup** function enables the Microsoft WinSNMP implementation to perform initialization procedures.</span></span> <span data-ttu-id="68dc6-106">La fonction retourne également à l’application la version de l’API WinSNMP prise en charge par l’implémentation, le niveau de communications SNMP qu’elle prend en charge, ainsi que les modes de traduction et de retransmission par défaut de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="68dc6-106">The function also returns to the application the version of the WinSNMP API that the implementation supports, the level of SNMP communications it supports, and the implementation's default translation and retransmission modes.</span></span>

<span data-ttu-id="68dc6-107">L’application WinSNMP doit appeler la fonction [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) lorsque l’application n’a plus besoin des services de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="68dc6-107">The WinSNMP application must call the [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) function when the application no longer requires the implementation's services.</span></span> <span data-ttu-id="68dc6-108">Même si **SnmpCleanup** permet à l’implémentation de libérer toutes les ressources allouées à l’application, il est recommandé que l’application appelle d’abord la fonction [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) une fois pour chaque session WinSNMP ouverte, afin d’optimiser les performances de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="68dc6-108">Even though **SnmpCleanup** enables the implementation to deallocate all resources allocated to the application, it is recommended that the application first call the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function once for each open WinSNMP session, to maximize the implementation's performance.</span></span> <span data-ttu-id="68dc6-109">L’application WinSNMP doit appeler [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) comme dernière fonction WinSNMP avant qu’elle ne se termine.</span><span class="sxs-lookup"><span data-stu-id="68dc6-109">The WinSNMP application must call [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) as the last WinSNMP function before it terminates.</span></span>

 

 




