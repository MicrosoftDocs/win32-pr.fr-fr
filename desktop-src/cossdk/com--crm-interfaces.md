---
description: Les interfaces CRM sont requises pour assurer la prise en charge des travailleurs CRM et des compensateurs CRM développés à l’aide de Visual Basic et Visual C++.
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Interfaces CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749005"
---
# <a name="com-crm-interfaces"></a><span data-ttu-id="45e15-103">Interfaces CRM COM+</span><span class="sxs-lookup"><span data-stu-id="45e15-103">COM+ CRM Interfaces</span></span>

<span data-ttu-id="45e15-104">Les interfaces CRM sont requises pour assurer la prise en charge des travailleurs CRM et des compensateurs CRM développés à l’aide de Visual Basic et Visual C++.</span><span class="sxs-lookup"><span data-stu-id="45e15-104">The CRM interfaces are required to provide support for CRM Workers and CRM Compensators developed using Visual Basic and Visual C++.</span></span>

<span data-ttu-id="45e15-105">Vous pouvez utiliser le Gestionnaire des ressources CRM (Compensating Compensating) pour intégrer rapidement et facilement des ressources d’application à des transactions Microsoft Distributed Transaction Coordinator (DTC).</span><span class="sxs-lookup"><span data-stu-id="45e15-105">You can use the COM+ Compensating Resource Manager (CRM) to quickly and easily integrate application resources with Microsoft Distributed Transaction Coordinator (DTC) transactions.</span></span>

<span data-ttu-id="45e15-106">Il est plus facile pour les composants écrits avec Visual Basic de créer un enregistrement de journal sous la forme d’une collection de variantes.</span><span class="sxs-lookup"><span data-stu-id="45e15-106">It is easier for components written with Visual Basic to build up a log record as a collection of Variants.</span></span> <span data-ttu-id="45e15-107">En outre, les composants Visual Basic sont des threads cloisonnés, ce qui signifie qu’il doit être possible de marshaler les interfaces du cloisonnement multithread à un cloisonnement à thread unique.</span><span class="sxs-lookup"><span data-stu-id="45e15-107">Also, Visual Basic components are apartment threaded, which implies that it must be possible to marshal the interfaces from the multithreaded apartment to a single-threaded apartment.</span></span> <span data-ttu-id="45e15-108">Les composants CRM développés avec Visual C++ pouvaient également utiliser le modèle de thread cloisonné, bien qu’il soit recommandé d’utiliser à la place le modèle de thread à la fois.</span><span class="sxs-lookup"><span data-stu-id="45e15-108">CRM components developed with Visual C++ could also use the Apartment threading model, although it is recommended that these use the Both threading model instead.</span></span>

<span data-ttu-id="45e15-109">Les interfaces décrites dans le tableau suivant fournissent des informations de référence détaillées pour les développeurs de données CRM COM+.</span><span class="sxs-lookup"><span data-stu-id="45e15-109">The interfaces described in the following table provide detailed reference information for developers of COM+ CRMs.</span></span>



| <span data-ttu-id="45e15-110">Interfaces CRM</span><span class="sxs-lookup"><span data-stu-id="45e15-110">CRM interfaces</span></span>                                             | <span data-ttu-id="45e15-111">Description</span><span class="sxs-lookup"><span data-stu-id="45e15-111">Description</span></span>                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45e15-112">**ICrmCompensator**</span><span class="sxs-lookup"><span data-stu-id="45e15-112">**ICrmCompensator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | <span data-ttu-id="45e15-113">Cette interface fournit des enregistrements de journal non structurés dans Visual C++.</span><span class="sxs-lookup"><span data-stu-id="45e15-113">This interface delivers unstructured log records in Visual C++.</span></span>                                                           |
| [<span data-ttu-id="45e15-114">**ICrmCompensatorVariants**</span><span class="sxs-lookup"><span data-stu-id="45e15-114">**ICrmCompensatorVariants**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | <span data-ttu-id="45e15-115">Cette interface fournit des enregistrements de journal structurés au compensateur CRM lors de l’utilisation de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="45e15-115">This interface delivers structured log records to the CRM Compensator when using Visual Basic.</span></span>                            |
| [<span data-ttu-id="45e15-116">**ICrmFormatLogRecords**</span><span class="sxs-lookup"><span data-stu-id="45e15-116">**ICrmFormatLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | <span data-ttu-id="45e15-117">Cette interface convertit les enregistrements de journal au format affichable afin qu’ils puissent être présentés à l’aide d’un outil d’analyse générique.</span><span class="sxs-lookup"><span data-stu-id="45e15-117">This interface converts the log records to viewable format so that they can be presented using a generic monitoring tool.</span></span> |
| [<span data-ttu-id="45e15-118">**ICrmLogControl**</span><span class="sxs-lookup"><span data-stu-id="45e15-118">**ICrmLogControl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | <span data-ttu-id="45e15-119">Cette interface est utilisée par le processus de travail CRM et le compensateur CRM pour écrire des enregistrements dans le journal et les rendre durables.</span><span class="sxs-lookup"><span data-stu-id="45e15-119">This interface is used by the CRM Worker and CRM Compensator to write records to the log and make them durable.</span></span>           |
| [<span data-ttu-id="45e15-120">**ICrmMonitor**</span><span class="sxs-lookup"><span data-stu-id="45e15-120">**ICrmMonitor**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | <span data-ttu-id="45e15-121">Cette interface capture un instantané de l’état actuel d’un CRM et contient un Clerk CRM spécifique.</span><span class="sxs-lookup"><span data-stu-id="45e15-121">This interface captures a snapshot of the current state of a CRM and holds a specific CRM clerk.</span></span>                          |
| [<span data-ttu-id="45e15-122">**ICrmMonitorClerks**</span><span class="sxs-lookup"><span data-stu-id="45e15-122">**ICrmMonitorClerks**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | <span data-ttu-id="45e15-123">Cette interface obtient des informations sur l’état des Clerk.</span><span class="sxs-lookup"><span data-stu-id="45e15-123">This interface obtains information about the state of clerks.</span></span>                                                             |
| [<span data-ttu-id="45e15-124">**ICrmMonitorLogRecords**</span><span class="sxs-lookup"><span data-stu-id="45e15-124">**ICrmMonitorLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | <span data-ttu-id="45e15-125">Cette interface analyse les enregistrements de journal individuels gérés par un Clerk CRM spécifique pour une transaction donnée.</span><span class="sxs-lookup"><span data-stu-id="45e15-125">This interface monitors the individual log records maintained by a specific CRM clerk for a given transaction.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="45e15-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45e15-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45e15-127">Concepts de Gestionnaire des ressources de compensation COM+</span><span class="sxs-lookup"><span data-stu-id="45e15-127">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



