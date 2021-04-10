---
description: .
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Meilleures pratiques pour réduire les services qui ne répondent pas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e1fbad7fe60c4165ebb97847c303482314f68e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868594"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a><span data-ttu-id="7372a-103">Meilleures pratiques pour réduire les services qui ne répondent pas</span><span class="sxs-lookup"><span data-stu-id="7372a-103">Best Practices for Minimizing Unresponsive Services</span></span>

## <a name="affected-platform"></a><span data-ttu-id="7372a-104">Plateforme affectée</span><span class="sxs-lookup"><span data-stu-id="7372a-104">Affected Platform</span></span>

 <span data-ttu-id="7372a-105">**Clients** – Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="7372a-105">**Clients** – Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="7372a-106">Description</span><span class="sxs-lookup"><span data-stu-id="7372a-106">Description</span></span>

<span data-ttu-id="7372a-107">Les services qui ne répondent pas peuvent entraîner des délais d’attente, des sessions terminées et même des données perdues.</span><span class="sxs-lookup"><span data-stu-id="7372a-107">Unresponsive services can result in timeouts, terminated sessions, and even lost data.</span></span> <span data-ttu-id="7372a-108">L’utilisation des meilleures pratiques peut réduire de manière considérable l’occurrence de services qui ne répondent pas.</span><span class="sxs-lookup"><span data-stu-id="7372a-108">Employing best practices can greatly reduce the occurrence of unresponsive services.</span></span>

## <a name="best-practices"></a><span data-ttu-id="7372a-109">Bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="7372a-109">Best Practices</span></span>

<span data-ttu-id="7372a-110">Assurez-vous que vos applications et tous leurs services et pilotes dépendants répondent aux notifications d’arrêt et de puissance système.</span><span class="sxs-lookup"><span data-stu-id="7372a-110">Make sure your applications and all of their dependent services and drivers respond to system power and shutdown notifications.</span></span>

-   <span data-ttu-id="7372a-111">Toutes les applications doivent répondre rapidement et de manière appropriée aux messages d’arrêt tels que WM \_ QUERYENDSESSION et WM \_ ENDSESSION qui indiquent un arrêt en cours.</span><span class="sxs-lookup"><span data-stu-id="7372a-111">All applications should respond promptly and appropriately to shutdown messages such as WM\_QUERYENDSESSION and WM\_ENDSESSION that indicate a shutdown is in progress.</span></span>
-   <span data-ttu-id="7372a-112">Tous les services doivent répondre rapidement aux notifications d’arrêt SCM.</span><span class="sxs-lookup"><span data-stu-id="7372a-112">All services should promptly respond to SCM shutdown notifications.</span></span> <span data-ttu-id="7372a-113">S’ils ne parviennent pas à le faire, l’ordinateur les traite comme ne répondant pas et démarre un délai de 20 secondes et les arrête, ce qui permet d’éviter la perte de données.</span><span class="sxs-lookup"><span data-stu-id="7372a-113">If they fail to do so, the machine treats them as unresponsive and initiates a 20-second time-out and stops them, opening up the possibility of lost data.</span></span> <span data-ttu-id="7372a-114">Cela ajoute également 20 secondes à l’heure d’arrêt d’un arrêt de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7372a-114">This also adds 20 seconds to the shutdown time of a machine shutdown.</span></span>
-   <span data-ttu-id="7372a-115">Tous les services qui ont des dépendances de pilote de périphérique en mode noyau doivent répondre rapidement et de manière appropriée à \_ la notification d’arrêt d’IRP MJ \_ dans leurs routines DispatchShutdown.</span><span class="sxs-lookup"><span data-stu-id="7372a-115">All services that have kernel device driver dependencies should respond promptly and appropriately to IRP\_MJ\_SHUTDOWN notification in their DispatchShutdown routines.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="7372a-116">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="7372a-116">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="7372a-117">Windows Performance Toolkit</span><span class="sxs-lookup"><span data-stu-id="7372a-117">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



