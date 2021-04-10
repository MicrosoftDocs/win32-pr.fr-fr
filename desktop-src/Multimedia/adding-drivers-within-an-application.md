---
title: Ajout de pilotes dans une application
description: Ajout de pilotes dans une application
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Audio Compression Manager (ACM), ajout de pilotes
- ACM (gestionnaire de compression audio), ajout de pilotes
- Exemples ACM, ajout de pilotes
- ajout de pilotes
- acmDriverAdd fonction)
- pilotes globaux
- pilotes locaux
- Audio Compression Manager (ACM), pilotes globaux
- ACM (gestionnaire de compression audio), pilotes globaux
- Audio Compression Manager (ACM), pilotes locaux
- ACM (gestionnaire de compression audio), pilotes locaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029226"
---
# <a name="adding-drivers-within-an-application"></a><span data-ttu-id="b69a6-114">Ajout de pilotes dans une application</span><span class="sxs-lookup"><span data-stu-id="b69a6-114">Adding Drivers Within an Application</span></span>

<span data-ttu-id="b69a6-115">Si vous avez besoin que votre application implémente ses propres routines de compression en interne, l’application peut ajouter des pilotes à l’ACM en appelant la fonction [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .</span><span class="sxs-lookup"><span data-stu-id="b69a6-115">If you need your application to implement its own compression routines internally, the application can add drivers to the ACM by calling the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span> <span data-ttu-id="b69a6-116">L’application implémente le pilote en fournissant une fonction conforme au prototype [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="b69a6-116">The application implements the driver by providing a function that conforms to the [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) prototype.</span></span> <span data-ttu-id="b69a6-117">Une fois que l’application a ajouté le pilote, l’application peut utiliser le pilote à l’aide de l’ACM comme tout autre pilote.</span><span class="sxs-lookup"><span data-stu-id="b69a6-117">After the application has added the driver, the application can use the driver through the ACM as it would use any other driver.</span></span>

<span data-ttu-id="b69a6-118">L’ACM traite les pilotes comme des pilotes globaux ou locaux.</span><span class="sxs-lookup"><span data-stu-id="b69a6-118">The ACM treats drivers as either global or local.</span></span> <span data-ttu-id="b69a6-119">Une application spécifie si un pilote doit être ajouté comme global ou local lorsqu’il appelle **acmDriverAdd**.</span><span class="sxs-lookup"><span data-stu-id="b69a6-119">An application specifies whether a driver should be added as global or local when it calls **acmDriverAdd**.</span></span> <span data-ttu-id="b69a6-120">Il existe deux différences entre les pilotes globaux et les pilotes locaux :</span><span class="sxs-lookup"><span data-stu-id="b69a6-120">There are two differences between global and local drivers:</span></span>

-   <span data-ttu-id="b69a6-121">Les pilotes ajoutés en tant que pilotes globaux ne sont pas partagés avec d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="b69a6-121">Drivers added as global drivers are not shared with other applications.</span></span>
-   <span data-ttu-id="b69a6-122">Une application peut modifier directement la priorité d’un pilote global (mais pas un pilote local) en appelant la fonction [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) .</span><span class="sxs-lookup"><span data-stu-id="b69a6-122">An application can directly alter the priority of a global driver (but not a local driver) by calling the [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) function.</span></span> <span data-ttu-id="b69a6-123">L’ACM effectue une recherche prioritaire lors de la recherche d’un pilote approprié pour fournir une implémentation d’un appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="b69a6-123">The ACM conducts a prioritized search when seeking an appropriate driver to provide an implementation of a function call.</span></span> <span data-ttu-id="b69a6-124">L’ACM donne toujours aux pilotes locaux une priorité plus élevée que les pilotes globaux.</span><span class="sxs-lookup"><span data-stu-id="b69a6-124">The ACM always gives local drivers higher priority than global drivers.</span></span> <span data-ttu-id="b69a6-125">Le pilote local le plus récemment ajouté a la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="b69a6-125">The most recently added local driver has highest priority.</span></span>

 

 




