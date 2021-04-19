---
description: Pour envoyer des demandes de contrôle à un service en cours d’exécution, un programme de contrôle de service utilise la fonction ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Demandes de contrôle de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543655"
---
# <a name="service-control-requests"></a><span data-ttu-id="70ccc-103">Demandes de contrôle de service</span><span class="sxs-lookup"><span data-stu-id="70ccc-103">Service Control Requests</span></span>

<span data-ttu-id="70ccc-104">Pour envoyer des demandes de contrôle à un service en cours d’exécution, un programme de contrôle de service utilise la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) .</span><span class="sxs-lookup"><span data-stu-id="70ccc-104">To send control requests to a running service, a service control program uses the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="70ccc-105">Cette fonction spécifie une valeur de contrôle qui est passée à la fonction [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) du service spécifié.</span><span class="sxs-lookup"><span data-stu-id="70ccc-105">This function specifies a control value that is passed to the [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) function of the specified service.</span></span> <span data-ttu-id="70ccc-106">Cette valeur de contrôle peut être un code défini par l’utilisateur, ou il peut s’agir de l’un des codes standard qui permettent au programme appelant d’effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="70ccc-106">This control value can be a user-defined code, or it can be one of the standard codes that enable the calling program to perform the following actions:</span></span>

-   <span data-ttu-id="70ccc-107">Arrêter un service (arrêt du contrôle de SERVICE \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="70ccc-107">Stop a service (SERVICE\_CONTROL\_STOP).</span></span>
-   <span data-ttu-id="70ccc-108">Suspendre un service ( \_ suspendre le contrôle de service \_ ).</span><span class="sxs-lookup"><span data-stu-id="70ccc-108">Pause a service (SERVICE\_CONTROL\_PAUSE).</span></span>
-   <span data-ttu-id="70ccc-109">Reprendre l’exécution d’un service suspendu ( \_ le contrôle du service \_ continue).</span><span class="sxs-lookup"><span data-stu-id="70ccc-109">Resume executing a paused service (SERVICE\_CONTROL\_CONTINUE).</span></span>
-   <span data-ttu-id="70ccc-110">Récupérer les informations d’État mises à jour à partir d’un service (interrogation du SERVICE de \_ contrôle \_ ).</span><span class="sxs-lookup"><span data-stu-id="70ccc-110">Retrieve updated status information from a service (SERVICE\_CONTROL\_INTERROGATE).</span></span>

<span data-ttu-id="70ccc-111">Chaque service spécifie les valeurs de contrôle qu’il acceptera et traitera.</span><span class="sxs-lookup"><span data-stu-id="70ccc-111">Each service specifies the control values that it will accept and process.</span></span> <span data-ttu-id="70ccc-112">Pour déterminer les valeurs de contrôle standard acceptées par un service, utilisez la fonction [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) ou spécifiez la valeur de \_ \_ contrôle d’interrogation du contrôle de service dans un appel à la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) .</span><span class="sxs-lookup"><span data-stu-id="70ccc-112">To determine which of the standard control values are accepted by a service, use the [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function or specify the SERVICE\_CONTROL\_INTERROGATE control value in a call to the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="70ccc-113">Le membre **dwControlsAccepted** de la structure d' [**\_ État de service**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) retourné par ces fonctions indique si le service peut être arrêté, suspendu ou repris.</span><span class="sxs-lookup"><span data-stu-id="70ccc-113">The **dwControlsAccepted** member of the [**SERVICE\_STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) structure returned by these functions indicates whether the service can be stopped, paused, or resumed.</span></span> <span data-ttu-id="70ccc-114">Tous les services acceptent la \_ valeur de contrôle d’interrogation du contrôle des services \_ .</span><span class="sxs-lookup"><span data-stu-id="70ccc-114">All services accept the SERVICE\_CONTROL\_INTERROGATE control value.</span></span>

<span data-ttu-id="70ccc-115">La fonction [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) signale l’état le plus récent pour un service spécifié, mais n’obtient pas d’État mis à jour à partir du service lui-même.</span><span class="sxs-lookup"><span data-stu-id="70ccc-115">The [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function reports the most recent status for a specified service, but does not get an updated status from the service itself.</span></span> <span data-ttu-id="70ccc-116">L’utilisation de \_ la \_ valeur de contrôle d’interrogation du contrôle de service dans un appel à [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) garantit que les informations d’état retournées sont actuelles.</span><span class="sxs-lookup"><span data-stu-id="70ccc-116">Using the SERVICE\_CONTROL\_INTERROGATE control value in a call to [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) ensures that the status information returned is current.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70ccc-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="70ccc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70ccc-118">Contrôle d’un service à l’aide de SC</span><span class="sxs-lookup"><span data-stu-id="70ccc-118">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



