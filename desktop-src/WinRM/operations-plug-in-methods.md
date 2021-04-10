---
title: Méthodes de plug-in Operations
description: Méthodes de plug-in Operations
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939540"
---
# <a name="operations-plug-in-methods"></a><span data-ttu-id="6a805-103">Méthodes de plug-in Operations</span><span class="sxs-lookup"><span data-stu-id="6a805-103">Operations Plug-in Methods</span></span>

<span data-ttu-id="6a805-104">Tous les points d’entrée de plug-in d’opérations ont un mécanisme de rappel pour signaler la réussite ou l’échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="6a805-104">All operations plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="6a805-105">Certains mécanismes de rappel sont appelés plusieurs fois, jusqu’à ce que tous les résultats soient signalés.</span><span class="sxs-lookup"><span data-stu-id="6a805-105">Some callback mechanisms are called multiple times, until all of the results are reported.</span></span>

<span data-ttu-id="6a805-106">Le tableau suivant fournit une vue d’ensemble des méthodes de rappel d’opérations.</span><span class="sxs-lookup"><span data-stu-id="6a805-106">The following table provides an overview of the operations callback methods.</span></span>



| <span data-ttu-id="6a805-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="6a805-107">Method</span></span>                                                                         | <span data-ttu-id="6a805-108">Description</span><span class="sxs-lookup"><span data-stu-id="6a805-108">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a805-109">**WSManPluginFreeRequestDetails**</span><span class="sxs-lookup"><span data-stu-id="6a805-109">**WSManPluginFreeRequestDetails**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | <span data-ttu-id="6a805-110">Libère la mémoire allouée pour la structure de [**\_ \_ demande de plug-in WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) .</span><span class="sxs-lookup"><span data-stu-id="6a805-110">Releases memory that is allocated for the [**WSMAN\_PLUGIN\_REQUEST**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) structure.</span></span>                                          |
| [<span data-ttu-id="6a805-111">**WSManPluginGetOperationParameters**</span><span class="sxs-lookup"><span data-stu-id="6a805-111">**WSManPluginGetOperationParameters**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | <span data-ttu-id="6a805-112">Obtient des informations opérationnelles, telles que les délais d’attente et les restrictions de données associées à une opération.</span><span class="sxs-lookup"><span data-stu-id="6a805-112">Gets operational information, such as time-outs and data restrictions that are associated with an operation.</span></span>                                         |
| [<span data-ttu-id="6a805-113">**WSManPluginOperationComplete**</span><span class="sxs-lookup"><span data-stu-id="6a805-113">**WSManPluginOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | <span data-ttu-id="6a805-114">Enregistre l’achèvement d’une opération.</span><span class="sxs-lookup"><span data-stu-id="6a805-114">Records the completion of an operation.</span></span>                                                                                                              |
| [<span data-ttu-id="6a805-115">**WSManPluginReceiveResult**</span><span class="sxs-lookup"><span data-stu-id="6a805-115">**WSManPluginReceiveResult**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | <span data-ttu-id="6a805-116">Signale les résultats aux plug-ins de Windows Remote Management (WinRM).</span><span class="sxs-lookup"><span data-stu-id="6a805-116">Reports results to Windows Remote Management (WinRM) plug-ins.</span></span>                                                                                       |
| [<span data-ttu-id="6a805-117">**WSManPluginReportContext**</span><span class="sxs-lookup"><span data-stu-id="6a805-117">**WSManPluginReportContext**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | <span data-ttu-id="6a805-118">Signale l’interpréteur de commandes et le contexte de commande à l’infrastructure WinRM afin que d’autres opérations puissent être effectuées sur l’interpréteur de commandes et/ou la commande.</span><span class="sxs-lookup"><span data-stu-id="6a805-118">Reports the shell and command context back to the WinRM infrastructure so that further operations can be performed against the shell and/or command.</span></span> |



 

 

 




