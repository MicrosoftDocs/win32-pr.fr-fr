---
description: Traitement des In-Place
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: Traitement des In-Place
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514091"
---
# <a name="in-place-processing"></a><span data-ttu-id="8e146-103">Traitement des In-Place</span><span class="sxs-lookup"><span data-stu-id="8e146-103">In-Place Processing</span></span>

<span data-ttu-id="8e146-104">Certaines transformations de données peuvent être effectuées en modifiant directement les données.</span><span class="sxs-lookup"><span data-stu-id="8e146-104">Certain data transformations can be accomplished by directly modifying the data.</span></span> <span data-ttu-id="8e146-105">C’est ce que l’on appelle le traitement *sur place* .</span><span class="sxs-lookup"><span data-stu-id="8e146-105">This is called *in-place* processing.</span></span> <span data-ttu-id="8e146-106">De nombreux effets audio et vidéo peuvent être effectués de cette manière.</span><span class="sxs-lookup"><span data-stu-id="8e146-106">Many audio and video effects can be done in this manner.</span></span> <span data-ttu-id="8e146-107">Si un module DMO prend en charge le traitement sur place, il expose l’interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) .</span><span class="sxs-lookup"><span data-stu-id="8e146-107">If a DMO supports in-place processing, it exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="8e146-108">Le traitement sur place est généralement plus efficace que l’utilisation de mémoires tampons distinctes pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="8e146-108">In-place processing is generally more efficient than using separate buffers for the output.</span></span> <span data-ttu-id="8e146-109">(Une exception majeure se présente lorsque la mémoire tampon réside dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="8e146-109">(One major exception is when the buffer resides in video memory.</span></span> <span data-ttu-id="8e146-110">Dans ce cas, les opérations de lecture sont beaucoup plus lentes que les opérations d’écriture. par conséquent, le traitement sur place n’est pas recommandé.)</span><span class="sxs-lookup"><span data-stu-id="8e146-110">In that situation, read operations are much slower than write operations, so in-place processing is not recommended.)</span></span>

<span data-ttu-id="8e146-111">Pour traiter les données en place, le client effectue un appel unique à la méthode [**IMediaObjectInPlace ::P tionnaire**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) , plutôt qu’à des appels distincts à **ProcessInput** et **ProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="8e146-111">To process data in place, the client makes a single call to the [**IMediaObjectInPlace::Process**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) method, rather than separate calls to **ProcessInput** and **ProcessOutput**.</span></span> <span data-ttu-id="8e146-112">La méthode **Process** est synchrone ; tout le traitement se produit à l’intérieur de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8e146-112">The **Process** method is synchronous; all processing occurs inside the call.</span></span> <span data-ttu-id="8e146-113">En outre, le traitement sur place n’utilise pas d’objets **IMediaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="8e146-113">Also, in-place processing does not use **IMediaBuffer** objects.</span></span> <span data-ttu-id="8e146-114">La méthode **Process** prend un pointeur directement vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8e146-114">The **Process** method takes a pointer directly to the memory buffer.</span></span>

<span data-ttu-id="8e146-115">Un DMO qui prend en charge le traitement sur place doit toujours implémenter l’interface **IMediaObject** , y compris les méthodes **ProcessInput** et **ProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="8e146-115">A DMO that supports in-place processing still must implement the **IMediaObject** interface, including the **ProcessInput** and **ProcessOutput** methods.</span></span> <span data-ttu-id="8e146-116">Le client peut choisir s’il faut utiliser le traitement sur place ou utiliser des mémoires tampons distinctes.</span><span class="sxs-lookup"><span data-stu-id="8e146-116">The client can choose whether to use in-place processing or use separate buffers.</span></span> <span data-ttu-id="8e146-117">Toutefois, ne mélangez pas les deux types de traitement.</span><span class="sxs-lookup"><span data-stu-id="8e146-117">However, do not mix the two types of processing.</span></span> <span data-ttu-id="8e146-118">Si vous appelez le **processus**, n’appelez pas **ProcessInput** ou **ProcessOutput**, et vice-versa.</span><span class="sxs-lookup"><span data-stu-id="8e146-118">If you call **Process**, do not call **ProcessInput** or **ProcessOutput**, and vice-versa.</span></span>

<span data-ttu-id="8e146-119">**Fin des effets**</span><span class="sxs-lookup"><span data-stu-id="8e146-119">**Effect Tails**</span></span>

<span data-ttu-id="8e146-120">Un DMO sur place peut créer une sortie supplémentaire après l’arrêt de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="8e146-120">An in-place DMO might create some additional output after the input stops.</span></span> <span data-ttu-id="8e146-121">C’est ce qu’on appelle une *fin d’effet*.</span><span class="sxs-lookup"><span data-stu-id="8e146-121">This is called an *effect tail*.</span></span> <span data-ttu-id="8e146-122">Par exemple, un effet de réverbération se poursuit une fois que l’entrée atteint le silence.</span><span class="sxs-lookup"><span data-stu-id="8e146-122">For example, a reverb effect continues after the input reaches silence.</span></span> <span data-ttu-id="8e146-123">En cas de fin d’effet, la méthode **Process** retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="8e146-123">If there is an effect tail, the **Process** method returns S\_FALSE.</span></span> <span data-ttu-id="8e146-124">Une fois que l’application a traité toutes ses données, elle peut générer la fin de l’effet en envoyant des tampons vides à la méthode de **processus** .</span><span class="sxs-lookup"><span data-stu-id="8e146-124">Once the application has processed all of its data, it can generate the effect tail by sending empty buffers to the **Process** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e146-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e146-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e146-126">Hébergement direct d’un DMO</span><span class="sxs-lookup"><span data-stu-id="8e146-126">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



