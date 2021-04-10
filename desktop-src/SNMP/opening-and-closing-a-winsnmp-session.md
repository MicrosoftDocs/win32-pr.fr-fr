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
# <a name="opening-and-closing-a-winsnmp-session"></a><span data-ttu-id="8b913-103">Ouverture et fermeture d’une session WinSNMP</span><span class="sxs-lookup"><span data-stu-id="8b913-103">Opening and Closing a WinSNMP Session</span></span>

<span data-ttu-id="8b913-104">Pour ouvrir une session, une application appelle la fonction [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .</span><span class="sxs-lookup"><span data-stu-id="8b913-104">To open a session, an application calls the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span> <span data-ttu-id="8b913-105">Si la fonction se termine correctement, l’implémentation de l’WinSNMP Microsoft ouvre une session et la fonction retourne un identificateur de session sous la forme d’un descripteur de **\_ session HSNMP** .</span><span class="sxs-lookup"><span data-stu-id="8b913-105">If the function completes successfully, the Microsoft WinSNMP implementation opens a session, and the function returns a session identifier in the form of an **HSNMP\_SESSION** handle.</span></span> <span data-ttu-id="8b913-106">Toutes les fonctions WinSNMP qui retournent des variables de handle incluent l’identificateur de session en tant que paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8b913-106">All WinSNMP functions that return handle variables include the session identifier as an input parameter.</span></span> <span data-ttu-id="8b913-107">Cela permet à l’implémentation d’utiliser le handle pour gérer efficacement les ressources au niveau de la session.</span><span class="sxs-lookup"><span data-stu-id="8b913-107">This enables the implementation to use the handle to efficiently manage resources at the session level.</span></span>

<span data-ttu-id="8b913-108">Une application peut avoir plusieurs sessions ouvertes simultanément.</span><span class="sxs-lookup"><span data-stu-id="8b913-108">An application can have multiple sessions open at one time.</span></span> <span data-ttu-id="8b913-109">Plusieurs sessions au sein d’une application peuvent partager des variables de handle.</span><span class="sxs-lookup"><span data-stu-id="8b913-109">Multiple sessions within an application can share handle variables.</span></span>

<span data-ttu-id="8b913-110">Si l’implémentation ne peut pas ouvrir une session en raison de limitations de ressources, elle retourne l' \_ échec SNMPAPI quand l’application appelle [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span><span class="sxs-lookup"><span data-stu-id="8b913-110">If the implementation cannot open a session because of resource limitations, it returns SNMPAPI\_FAILURE when the application calls [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span> <span data-ttu-id="8b913-111">Si l’application appelle ensuite la fonction [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) , elle retourne une \_ erreur d’allocation SNMPAPI \_ .</span><span class="sxs-lookup"><span data-stu-id="8b913-111">If the application then calls the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function, it returns SNMPAPI\_ALLOC\_ERROR.</span></span>

<span data-ttu-id="8b913-112">Un appel à la fonction [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) permet à l’implémentation de libérer toutes les ressources restantes et de fermer la session.</span><span class="sxs-lookup"><span data-stu-id="8b913-112">A call to the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function enables the implementation to free any remaining resources and to close the session.</span></span>

<span data-ttu-id="8b913-113">Pour plus d’informations, consultez [objets de handle de ressource](resource-handle-objects.md) et [sessions WinSNMP](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="8b913-113">For more information, see [Resource Handle Objects](resource-handle-objects.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




