---
description: Le \_ mutex MSIExecute est défini uniquement lors du traitement de la table InstallExecuteSequence, de la table AdminExecuteSequence ou de la table AdvtExecuteSequence.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: Mutex _MSIExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864554"
---
# <a name="_msiexecute-mutex"></a><span data-ttu-id="cb494-103">\_Mutex MSIExecute</span><span class="sxs-lookup"><span data-stu-id="cb494-103">\_MSIExecute Mutex</span></span>

<span data-ttu-id="cb494-104">Le \_ mutex MSIExecute est défini uniquement lors du traitement de la table [InstallExecuteSequence](installexecutesequence-table.md), de la table [AdminExecuteSequence](adminexecutesequence-table.md)ou de la table [AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="cb494-104">The \_MSIExecute Mutex is set only while processing the [InstallExecuteSequence table](installexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

<span data-ttu-id="cb494-105">Étant donné que deux installations ne peuvent pas être exécutées dans le même processus, une tentative d’appel de l’interface de programmation d’applications (API) du programme d’installation retourne une erreur d' \_ installation \_ déjà \_ en cours d’exécution (1618) dans deux cas :</span><span class="sxs-lookup"><span data-stu-id="cb494-105">Because two installations cannot be run in the same process, an attempt to call the installer's application programming interface (API) returns ERROR\_INSTALL\_ALREADY\_RUNNING (1618) in two cases:</span></span>

-   <span data-ttu-id="cb494-106">Pendant que le \_ mutex MSIExecute est défini.</span><span class="sxs-lookup"><span data-stu-id="cb494-106">While the \_MSIExecute Mutex is set.</span></span>
-   <span data-ttu-id="cb494-107">Pendant que le processus en cours traite la table [InstallUISequence](installuisequence-table.md) ou la [table AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="cb494-107">While the current process is processing the [InstallUISequence table](installuisequence-table.md) or [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="cb494-108">Pour plus d’informations sur l’application en cours d’installation, consultez les messages de [journalisation des événements](event-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="cb494-108">See the [Event Logging](event-logging.md) messages for information about what application is being installed.</span></span>

<span data-ttu-id="cb494-109">Dans les cas où il n’est pas pratique de retourner une erreur d' \_ installation \_ déjà en \_ cours d’exécution, vous pouvez récupérer l’état actuel du service Windows Installer avant de tenter de démarrer l’installation à l’aide de la fonction [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) .</span><span class="sxs-lookup"><span data-stu-id="cb494-109">In cases where it is impractical to return an ERROR\_INSTALL\_ALREADY\_RUNNING error, you can retrieve the current status of the Windows Installer service before attempting to start the installation by using the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function.</span></span> <span data-ttu-id="cb494-110">Le service Windows Installer est en cours d’exécution si la valeur du membre **dwControlsAccepted** de la structure du [**processus d' \_ état \_ du service**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) retourné est arrêt de l' **\_ acceptation \_ du service**.</span><span class="sxs-lookup"><span data-stu-id="cb494-110">The Windows Installer service is currently running if the value of the **dwControlsAccepted** member of the returned [**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) structure is **SERVICE\_ACCEPT\_SHUTDOWN**.</span></span>

<span data-ttu-id="cb494-111">**Windows Installer 2,0 :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cb494-111">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="cb494-112">L’utilisation de la fonction [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) pour récupérer l’état actuel du service Windows Installer requiert Windows Installer version 3,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cb494-112">The use of the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function to retrieve the current status of the Windows Installer service requires Windows Installer version 3.0 or greater.</span></span>

 

 
