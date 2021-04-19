---
description: Le gestionnaire de contrôle des services (SCM) contrôle un service en envoyant des événements de contrôle de service à la routine du gestionnaire de contrôle des services.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Services multithread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5795a170f912050d115537407fcb491305a35ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518845"
---
# <a name="multithreaded-services"></a><span data-ttu-id="43689-103">Services multithread</span><span class="sxs-lookup"><span data-stu-id="43689-103">Multithreaded Services</span></span>

<span data-ttu-id="43689-104">Le gestionnaire de contrôle des services (SCM) contrôle un service en envoyant des événements de contrôle de service à la routine du gestionnaire de contrôle du service.</span><span class="sxs-lookup"><span data-stu-id="43689-104">The service control manager (SCM) controls a service by sending service control events to the service's control handler routine.</span></span> <span data-ttu-id="43689-105">Le service doit répondre en temps utile aux événements de contrôle afin que le SCM puisse effectuer le suivi de l’état du service.</span><span class="sxs-lookup"><span data-stu-id="43689-105">The service must respond to control events in a timely manner so that the SCM can keep track of the state of the service.</span></span> <span data-ttu-id="43689-106">En outre, l’état du service doit correspondre à la description de l’état que le SCM reçoit.</span><span class="sxs-lookup"><span data-stu-id="43689-106">Also, the state of the service must match the description of its state that the SCM receives.</span></span>

<span data-ttu-id="43689-107">En raison de ce mécanisme de communication entre un service et le SCM, vous devez être prudent lorsque vous utilisez plusieurs threads dans un service.</span><span class="sxs-lookup"><span data-stu-id="43689-107">Due to this communication mechanism between a service and the SCM, you must be careful when using multiple threads in a service.</span></span> <span data-ttu-id="43689-108">Lorsqu’un service est invité à s’arrêter par le SCM, il doit attendre la fin de tous les threads avant de signaler au SCM que le service est arrêté.</span><span class="sxs-lookup"><span data-stu-id="43689-108">When a service is instructed to stop by the SCM, it must wait for all the threads to exit before reporting to the SCM that the service is stopped.</span></span> <span data-ttu-id="43689-109">Dans le cas contraire, le SCM peut être perturbé par l’état du service et risque de ne pas s’arrêter correctement.</span><span class="sxs-lookup"><span data-stu-id="43689-109">Otherwise, the SCM can become confused about the state of the service and might fail to shut down correctly.</span></span>

<span data-ttu-id="43689-110">Le SCM doit être informé que le service répond à l’événement de contrôle d’arrêt et que la progression de l’arrêt du service est en cours.</span><span class="sxs-lookup"><span data-stu-id="43689-110">The SCM needs to be notified that the service is responding to the stop control event and that progress is being made in stopping the service.</span></span> <span data-ttu-id="43689-111">Le SCM part du principe que le service est en cours de progression si le service répond (via [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) au cours de la période (indicateur d’attente) spécifiée dans l’appel précédent à **SetServiceStatus**, et que le point de contrôle est mis à jour pour être plus grand que le point de contrôle spécifié dans l’appel précédent à **SetServiceStatus**.</span><span class="sxs-lookup"><span data-stu-id="43689-111">The SCM will assume the service is making progress if the service responds (through [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) within the time (wait hint) specified in the previous call to **SetServiceStatus**, and the check point is updated to be greater than the checkpoint specified in the previous call to **SetServiceStatus**.</span></span>

<span data-ttu-id="43689-112">Si le service signale au SCM que le service s’est arrêté avant la sortie de tous les threads, il est possible que le SCM interprète cela comme une contradiction.</span><span class="sxs-lookup"><span data-stu-id="43689-112">If the service reports to the SCM that the service has stopped before all threads have exited, it is possible that the SCM will interpret this as a contradiction.</span></span> <span data-ttu-id="43689-113">Cela peut aboutir à un État dans lequel le service ne peut pas être arrêté ou redémarré.</span><span class="sxs-lookup"><span data-stu-id="43689-113">This might result in a state where the service cannot be stopped or restarted.</span></span>

 

 



