---
description: Le kit de développement logiciel (SDK) Moniteur réseau comprend les fonctions et les exemples de code dont vous avez besoin pour créer des experts. Toutefois, vous pouvez également utiliser des outils existants, y compris un éditeur de boîtes de dialogue.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programmation d’un expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115346"
---
# <a name="programming-an-expert"></a><span data-ttu-id="9ed8a-104">Programmation d’un expert</span><span class="sxs-lookup"><span data-stu-id="9ed8a-104">Programming an Expert</span></span>

<span data-ttu-id="9ed8a-105">Le kit de développement logiciel (SDK) Moniteur réseau comprend les fonctions et les exemples de code dont vous avez besoin pour créer des experts.</span><span class="sxs-lookup"><span data-stu-id="9ed8a-105">The Network Monitor SDK includes the functions and sample code you need to build experts.</span></span> <span data-ttu-id="9ed8a-106">Toutefois, vous pouvez également utiliser des outils existants, y compris un éditeur de boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9ed8a-106">However, you can also use existing tools, including a dialog editor.</span></span>

## <a name="minimum-requirements-to-run-an-expert"></a><span data-ttu-id="9ed8a-107">Configuration minimale requise pour exécuter un expert</span><span class="sxs-lookup"><span data-stu-id="9ed8a-107">Minimum Requirements to Run an Expert</span></span>

<span data-ttu-id="9ed8a-108">Le tableau suivant répertorie les points d’entrée de DLL et les fonctions d’experts que vous devez utiliser pour créer un expert.</span><span class="sxs-lookup"><span data-stu-id="9ed8a-108">The following table lists the DLL entry points and expert functions you must use to build an expert.</span></span>



| <span data-ttu-id="9ed8a-109">Nom</span><span class="sxs-lookup"><span data-stu-id="9ed8a-109">Name</span></span>                                                 | <span data-ttu-id="9ed8a-110">Type</span><span class="sxs-lookup"><span data-stu-id="9ed8a-110">Type</span></span>               | <span data-ttu-id="9ed8a-111">Requis ?</span><span class="sxs-lookup"><span data-stu-id="9ed8a-111">Required?</span></span>                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [<span data-ttu-id="9ed8a-112">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="9ed8a-112">**DllMain**</span></span>](dllmain-expert.md)                    | <span data-ttu-id="9ed8a-113">Fonction d’entrée de DLL</span><span class="sxs-lookup"><span data-stu-id="9ed8a-113">DLL entry function</span></span> | <span data-ttu-id="9ed8a-114">Oui</span><span class="sxs-lookup"><span data-stu-id="9ed8a-114">Yes</span></span>                                             |
| [<span data-ttu-id="9ed8a-115">**Inscrire un expert**</span><span class="sxs-lookup"><span data-stu-id="9ed8a-115">**Register Expert**</span></span>](register-expert.md)           | <span data-ttu-id="9ed8a-116">Fonction d’entrée de DLL</span><span class="sxs-lookup"><span data-stu-id="9ed8a-116">DLL entry function</span></span> | <span data-ttu-id="9ed8a-117">Oui</span><span class="sxs-lookup"><span data-stu-id="9ed8a-117">Yes</span></span>                                             |
| [<span data-ttu-id="9ed8a-118">**Utilisez**</span><span class="sxs-lookup"><span data-stu-id="9ed8a-118">**Run**</span></span>](run.md)                                   | <span data-ttu-id="9ed8a-119">Fonction d’entrée de DLL</span><span class="sxs-lookup"><span data-stu-id="9ed8a-119">DLL entry function</span></span> | <span data-ttu-id="9ed8a-120">Oui</span><span class="sxs-lookup"><span data-stu-id="9ed8a-120">Yes</span></span>                                             |
| [<span data-ttu-id="9ed8a-121">**Configurer**</span><span class="sxs-lookup"><span data-stu-id="9ed8a-121">**Configure**</span></span>](configure.md)                       | <span data-ttu-id="9ed8a-122">Fonction d’entrée de DLL</span><span class="sxs-lookup"><span data-stu-id="9ed8a-122">DLL entry function</span></span> | <span data-ttu-id="9ed8a-123">Uniquement si l’expert fournit la configuration utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9ed8a-123">Only if the expert provides user configuration.</span></span> |
| [<span data-ttu-id="9ed8a-124">**ExpertIndicateStatus**</span><span class="sxs-lookup"><span data-stu-id="9ed8a-124">**ExpertIndicateStatus**</span></span>](expertindicatestatus.md) | <span data-ttu-id="9ed8a-125">Fonction expert</span><span class="sxs-lookup"><span data-stu-id="9ed8a-125">Expert function</span></span>    | <span data-ttu-id="9ed8a-126">Oui</span><span class="sxs-lookup"><span data-stu-id="9ed8a-126">Yes</span></span>                                             |
| [<span data-ttu-id="9ed8a-127">**ExpertSubmitEvent**</span><span class="sxs-lookup"><span data-stu-id="9ed8a-127">**ExpertSubmitEvent**</span></span>](expertsubmitevent.md)       | <span data-ttu-id="9ed8a-128">Fonction expert</span><span class="sxs-lookup"><span data-stu-id="9ed8a-128">Expert function</span></span>    | <span data-ttu-id="9ed8a-129">Oui</span><span class="sxs-lookup"><span data-stu-id="9ed8a-129">Yes</span></span>                                             |



 

<span data-ttu-id="9ed8a-130">Consultez les rubriques de référence de l’expert et de l’analyseur dans le kit de développement logiciel (SDK) Moniteur réseau pour mettre à jour votre code source, puis utilisez l’exemple de code et les procédures fournis dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ed8a-130">Review the expert and parser reference topics in the Network Monitor SDK to update your source code and then use the sample code and procedures provided in these topics:</span></span>

-   [<span data-ttu-id="9ed8a-131">Création d’un expert</span><span class="sxs-lookup"><span data-stu-id="9ed8a-131">Building an Expert</span></span>](building-an-expert.md)
-   [<span data-ttu-id="9ed8a-132">Installation d’un expert</span><span class="sxs-lookup"><span data-stu-id="9ed8a-132">Installing an Expert</span></span>](installing-an-expert-to-network-monitor-2-1.md)
-   [<span data-ttu-id="9ed8a-133">Débogage d’un expert</span><span class="sxs-lookup"><span data-stu-id="9ed8a-133">Debugging an Expert</span></span>](debugging-an-expert.md)

<span data-ttu-id="9ed8a-134">Les dll d’experts requièrent le C, et non la Convention d’appel C++, car les fonctions sont appelées par le biais de pointeurs de fonction à l’aide d’une superposition.</span><span class="sxs-lookup"><span data-stu-id="9ed8a-134">Expert DLLs require the C, not the C++, calling convention because functions are called through function pointers by using an overlay.</span></span> <span data-ttu-id="9ed8a-135">Grâce à un ensemble de fonctions d’experts spécialisées, l’expert a accès aux frames de la capture.</span><span class="sxs-lookup"><span data-stu-id="9ed8a-135">Through a set of specialized expert functions, the expert has access to the frames in the capture.</span></span> <span data-ttu-id="9ed8a-136">L’expert peut utiliser la plupart des Moniteur réseau API pour manipuler les données renvoyées.</span><span class="sxs-lookup"><span data-stu-id="9ed8a-136">The expert can use most of the Network Monitor API to manipulate the returned data.</span></span> <span data-ttu-id="9ed8a-137">Lorsqu’un expert trouve des informations à envoyer à l’utilisateur, il reporte les informations dans une structure de données d’événement et les soumet à Moniteur réseau, qui affiche ensuite les informations dans une fenêtre de sortie d’expert.</span><span class="sxs-lookup"><span data-stu-id="9ed8a-137">When an expert finds information to send to the user, it packages the information in an event data structure and submits it to Network Monitor, which then displays the information in an expert output window.</span></span> <span data-ttu-id="9ed8a-138">L’expert doit régulièrement mettre à jour Moniteur réseau avec des informations d’état d’achèvement de pourcentage, qui sont fournies par la fonction [**ExpertIndicateStatus**](expertindicatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="9ed8a-138">The expert must periodically update Network Monitor with percentage-completion status information, which is provided by the [**ExpertIndicateStatus**](expertindicatestatus.md) function.</span></span>

<span data-ttu-id="9ed8a-139">Les fonctions exportées par l’expert sont appelées comme suit :</span><span class="sxs-lookup"><span data-stu-id="9ed8a-139">The expert's exported functions are called as follows:</span></span>

-   <span data-ttu-id="9ed8a-140">Lorsque Moniteur réseau crée la liste d’experts à présenter à l’utilisateur, Moniteur réseau appelle la fonction d' [**expert d’inscription**](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="9ed8a-140">When Network Monitor is creating the list of experts to present to the user, Network Monitor calls the [**Register Expert**](register-expert.md) function.</span></span>
-   <span data-ttu-id="9ed8a-141">Après l’appel à **Register**, si l’expert est configurable, moniteur réseau appelle la fonction [**configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="9ed8a-141">After the call to **Register**, if the expert is configurable, Network Monitor calls the [**Configure**](configure.md) function.</span></span>
-   <span data-ttu-id="9ed8a-142">Lorsque l’utilisateur Moniteur réseau clique sur **exécuter expert**, moniteur réseau appelle la fonction [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="9ed8a-142">When the Network Monitor user clicks **Run Expert**, Network Monitor calls the [**Run**](run.md) function.</span></span>

<span data-ttu-id="9ed8a-143">Quand les experts analysent les trames demandées et trouvent un problème, ils utilisent [**ExpertSubmitEvent**](expertsubmitevent.md) pour envoyer un événement qui contient des informations sur le problème.</span><span class="sxs-lookup"><span data-stu-id="9ed8a-143">When experts analyze the requested frames and find a problem, they use [**ExpertSubmitEvent**](expertsubmitevent.md) to submit an event that contains information about the problem.</span></span> <span data-ttu-id="9ed8a-144">Moniteur réseau distribue l’événement au observateur d’événements standard (partagé) ou (si l’expert s’inscrit pour lui) sur un observateur d’événements privé.</span><span class="sxs-lookup"><span data-stu-id="9ed8a-144">Network Monitor distributes the event to either the standard (shared) Event Viewer or (if the expert registers for it) to a private Event Viewer.</span></span>

 

 



