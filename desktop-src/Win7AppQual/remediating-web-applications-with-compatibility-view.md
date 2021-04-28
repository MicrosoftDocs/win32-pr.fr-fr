---
description: Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116357"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a><span data-ttu-id="3b0f3-103">Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité</span><span class="sxs-lookup"><span data-stu-id="3b0f3-103">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>

<span data-ttu-id="3b0f3-104">Cette section décrit les étapes de base de la prévention et la planification de la prochaine compatibilité des applications pendant que vous résolvez les problèmes maintenant.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-104">This section describes basic mitigation steps and how to plan for future application compatibility while you are addressing any issues now.</span></span>

<span data-ttu-id="3b0f3-105">Dans la mesure du possible, Windows Internet Explorer prend en charge les modèles Internet Explorer hérités afin que les sites que vous développez continuent de se comporter comme prévu dans les versions plus récentes d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-105">Windows Internet Explorer supports the legacy Internet Explorer models whenever feasible so that sites that you develop to them continue to behave as expected in newer versions of Internet Explorer.</span></span> <span data-ttu-id="3b0f3-106">À compter de Windows Internet Explorer 8, vous pouvez choisir de prendre en charge les comportements hérités en sélectionnant le mode de rendu page par page.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-106">Starting with Windows Internet Explorer 8, you can choose to support legacy behaviors by selecting the rendering mode on a page-by-page basis.</span></span>

<span data-ttu-id="3b0f3-107">Internet Explorer 8 comprend les modes de rendu suivants que vous pouvez définir à l’aide de l’en-tête X-UA-compatible.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-107">Internet Explorer 8 includes the following rendering modes that you can set by using the X-UA-Compatible header.</span></span>



| <span data-ttu-id="3b0f3-108">Valeur content</span><span class="sxs-lookup"><span data-stu-id="3b0f3-108">Content value</span></span> | <span data-ttu-id="3b0f3-109">Description</span><span class="sxs-lookup"><span data-stu-id="3b0f3-109">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0f3-110">IE=5</span><span class="sxs-lookup"><span data-stu-id="3b0f3-110">IE=5</span></span>          | <span data-ttu-id="3b0f3-111">Utilisez le mode Quirks.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-111">Use quirks mode.</span></span>                                                                      |
| <span data-ttu-id="3b0f3-112">IE = 7</span><span class="sxs-lookup"><span data-stu-id="3b0f3-112">IE=7</span></span>          | <span data-ttu-id="3b0f3-113">Utilisez toujours le mode Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-113">Always use Windows Internet Explorer 7 mode.</span></span>                                          |
| <span data-ttu-id="3b0f3-114">IE=EmulateIE7</span><span class="sxs-lookup"><span data-stu-id="3b0f3-114">IE=EmulateIE7</span></span> | <span data-ttu-id="3b0f3-115">Affichez en mode Internet Explorer 7, sauf si le site contient le DOCTYPE excentrique.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-115">Display in Internet Explorer 7 mode unless the site has the quirks DOCTYPE.</span></span>           |
| <span data-ttu-id="3b0f3-116">IE = 8</span><span class="sxs-lookup"><span data-stu-id="3b0f3-116">IE=8</span></span>          | <span data-ttu-id="3b0f3-117">Utilisez toujours le mode Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-117">Always use Internet Explorer 8 mode.</span></span>                                                  |
| <span data-ttu-id="3b0f3-118">IE=EmulateIE8</span><span class="sxs-lookup"><span data-stu-id="3b0f3-118">IE=EmulateIE8</span></span> | <span data-ttu-id="3b0f3-119">Remplacez l’affichage de compatibilité sur les ordinateurs clients et utilisez le mode Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-119">Override Compatibility View on client machines and use Internet Explorer 8 mode.</span></span>      |
| <span data-ttu-id="3b0f3-120">IE=Edge</span><span class="sxs-lookup"><span data-stu-id="3b0f3-120">IE=Edge</span></span>       | <span data-ttu-id="3b0f3-121">Affichez dans le dernier mode.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-121">Display in the latest mode.</span></span> <span data-ttu-id="3b0f3-122">Dans Internet Explorer 8, cette valeur est équivalente à IE = 8.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-122">In Internet Explorer 8, this value is equivalent to IE=8.</span></span> |



 

<span data-ttu-id="3b0f3-123">Les rubriques suivantes expliquent comment mettre à jour des applications Web à l’aide de l’affichage de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-123">The following topics describe how to update web applications by using Compatibility View.</span></span>



| <span data-ttu-id="3b0f3-124">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3b0f3-124">Topic</span></span>                                                                                                  | <span data-ttu-id="3b0f3-125">Description</span><span class="sxs-lookup"><span data-stu-id="3b0f3-125">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="3b0f3-126">Qu’est-ce que l’affichage de compatibilité ?</span><span class="sxs-lookup"><span data-stu-id="3b0f3-126">What Is Compatibility View</span></span>](what-is-compatibility-view-.md)                                          | <span data-ttu-id="3b0f3-127">Décrit l’affichage de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-127">Describes Compatibility View.</span></span>                                                  |
| [<span data-ttu-id="3b0f3-128">Pourquoi avez-vous besoin d’un affichage de compatibilité ?</span><span class="sxs-lookup"><span data-stu-id="3b0f3-128">Why Do You Need Compatibility View?</span></span>](why-do-you-need-compatibility-view-.md)                         | <span data-ttu-id="3b0f3-129">Explique pourquoi vous devez utiliser l’affichage de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-129">Describes why you should use Compatibility View.</span></span>                               |
| [<span data-ttu-id="3b0f3-130">Utiliser la balise meta pour garantir la compatibilité future</span><span class="sxs-lookup"><span data-stu-id="3b0f3-130">Use the Meta Tag to Ensure Future Compatibility</span></span>](use-the-meta-tag-to-ensure-future-compatibility.md) | <span data-ttu-id="3b0f3-131">Décrit comment vous pouvez utiliser l’élément **meta** pour garantir la compatibilité future.</span><span class="sxs-lookup"><span data-stu-id="3b0f3-131">Describes how you can use the **meta** element to ensure future compatibility.</span></span> |



 

 

 



