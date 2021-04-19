---
title: Méthodes de plug-in d’autorisation
description: Tous les points d’entrée de plug-in d’autorisation ont un mécanisme de rappel pour signaler la réussite ou l’échec de l’appel. Certains mécanismes de rappel sont appelés plusieurs fois jusqu’à ce que tous les résultats soient signalés.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510826"
---
# <a name="authorization-plug-in-methods"></a><span data-ttu-id="4461b-104">Méthodes de plug-in d’autorisation</span><span class="sxs-lookup"><span data-stu-id="4461b-104">Authorization Plug-in Methods</span></span>

<span data-ttu-id="4461b-105">Tous les points d’entrée de plug-in d’autorisation ont un mécanisme de rappel pour signaler la réussite ou l’échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="4461b-105">All authorization plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="4461b-106">Certains mécanismes de rappel sont appelés plusieurs fois jusqu’à ce que tous les résultats soient signalés.</span><span class="sxs-lookup"><span data-stu-id="4461b-106">Some callback mechanisms are called multiple times until all of the results are reported.</span></span>

<span data-ttu-id="4461b-107">Le tableau suivant fournit une vue d’ensemble des méthodes de rappel d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="4461b-107">The following table provides an overview of the authorization callback methods.</span></span>



| <span data-ttu-id="4461b-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="4461b-108">Method</span></span>                                                                           | <span data-ttu-id="4461b-109">Description</span><span class="sxs-lookup"><span data-stu-id="4461b-109">Description</span></span>                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="4461b-110">**WSManPluginAuthzOperationComplete**</span><span class="sxs-lookup"><span data-stu-id="4461b-110">**WSManPluginAuthzOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | <span data-ttu-id="4461b-111">Signale la réussite ou l’échec d’une opération utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4461b-111">Reports either a successful or failed user operation.</span></span>                |
| [<span data-ttu-id="4461b-112">**WSManPluginAuthzQueryQuotaComplete**</span><span class="sxs-lookup"><span data-stu-id="4461b-112">**WSManPluginAuthzQueryQuotaComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | <span data-ttu-id="4461b-113">Signale les détails de quota pertinents pour l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="4461b-113">Reports quota details that are relevant for the specified user.</span></span>      |
| [<span data-ttu-id="4461b-114">**WSManPluginAuthzUserComplete**</span><span class="sxs-lookup"><span data-stu-id="4461b-114">**WSManPluginAuthzUserComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | <span data-ttu-id="4461b-115">Signale une autorisation de connexion utilisateur ayant réussi ou échoué.</span><span class="sxs-lookup"><span data-stu-id="4461b-115">Reports either a successful or failed user connection authorization.</span></span> |



 

 

 




