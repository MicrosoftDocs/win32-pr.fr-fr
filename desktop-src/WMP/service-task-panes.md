---
title: Volets de tâches du service
description: Volets de tâches du service
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Magasins en ligne du lecteur Windows Media, volets des tâches du service
- magasins en ligne, volets des tâches de service
- types 2 magasins en ligne, volets de tâches de service
- Windows Media Player Online stores, volets des tâches
- magasins en ligne, volets des tâches
- tapez 2 magasins en ligne, volets des tâches
- Windows Media Player, service, volets Office
- Windows Media Player, volets des tâches
- volets de tâches du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029356"
---
# <a name="service-task-panes"></a><span data-ttu-id="c735c-112">Volets de tâches du service</span><span class="sxs-lookup"><span data-stu-id="c735c-112">Service Task Panes</span></span>

<span data-ttu-id="c735c-113">Dans le lecteur Windows Media 10, les fournisseurs de magasins en ligne peuvent configurer le lecteur Windows Media pour qu’ils affichent jusqu’à trois volets de tâches, appelés volets de tâches de service.</span><span class="sxs-lookup"><span data-stu-id="c735c-113">In Windows Media Player 10, online store providers can configure Windows Media Player to display as many as three task panes, called service task panes.</span></span> <span data-ttu-id="c735c-114">Chaque volet de tâches de service est représenté par un bouton personnalisable que le lecteur Windows Media affiche sur le côté droit de la barre des tâches fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c735c-114">Each service task pane is represented by a customizable button that Windows Media Player displays on the right side of the Features taskbar.</span></span>

<span data-ttu-id="c735c-115">Chaque volet de tâches de service héberge une page Web qui est l’interface utilisateur d’une fonctionnalité de magasin en ligne particulière. L’apparence des volets de tâches du service est définie par le document XML ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="c735c-115">Each service task pane hosts a webpage that is the user interface for a particular online store feature.The appearance of the service task panes is defined by the ServiceInfo XML document.</span></span> <span data-ttu-id="c735c-116">Dans ce document, les volets Office de service sont représentés par trois éléments : **ServiceTask1**, **ServiceTask2** et **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="c735c-116">In this document, the service task panes are represented by three elements: **ServiceTask1**, **ServiceTask2**, and **ServiceTask3**.</span></span> <span data-ttu-id="c735c-117">Ces volets de tâches de service sont conçus pour fournir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c735c-117">These service task panes are intended to provide the following:</span></span>

-   <span data-ttu-id="c735c-118">Un service musical.</span><span class="sxs-lookup"><span data-stu-id="c735c-118">A music service.</span></span>
-   <span data-ttu-id="c735c-119">Service vidéo.</span><span class="sxs-lookup"><span data-stu-id="c735c-119">A video service.</span></span>
-   <span data-ttu-id="c735c-120">Un service radio.</span><span class="sxs-lookup"><span data-stu-id="c735c-120">A radio service.</span></span>

<span data-ttu-id="c735c-121">Vous pouvez positionner ces fonctionnalités dans le lecteur Windows Media dans n’importe quel ordre, mais **ServiceTask1** doit être le volet principal des tâches pour engager des activités commerciales.</span><span class="sxs-lookup"><span data-stu-id="c735c-121">You can position these features in Windows Media Player in any order you like, but **ServiceTask1** must be the primary task pane for engaging in commercial activity.</span></span>

<span data-ttu-id="c735c-122">La page Web hébergée dans chaque volet de tâches du service a accès à l’objet **externe** .</span><span class="sxs-lookup"><span data-stu-id="c735c-122">The webpage hosted in each service task pane has access to the **External** object.</span></span> <span data-ttu-id="c735c-123">Cet objet fournit des méthodes, des propriétés et un événement qui fournissent des fonctionnalités spéciales pour les pages Web dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c735c-123">This object provides methods, properties, and an event that provide special functionality for webpages in Windows Media Player.</span></span> <span data-ttu-id="c735c-124">Par exemple, vous pouvez utiliser l’événement et les propriétés de **externe** pour que l’apparence de votre page Web corresponde au modèle de couleurs choisi par l’utilisateur pour le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c735c-124">For instance, you can use the event and properties from **External** to make the appearance of your webpage match the color scheme that the user has chosen for Windows Media Player.</span></span>

<span data-ttu-id="c735c-125">Dans le lecteur Windows Media 11, il n’existe aucun volet Office de service.</span><span class="sxs-lookup"><span data-stu-id="c735c-125">In Windows Media Player 11, there are no service task panes.</span></span> <span data-ttu-id="c735c-126">Au lieu de cela, il existe un onglet **magasins en ligne** unique, qui héberge la page Web principale du magasin en ligne actif.</span><span class="sxs-lookup"><span data-stu-id="c735c-126">Instead, there is a single **Online Stores** tab, which hosts the main webpage for the active online store.</span></span> <span data-ttu-id="c735c-127">Dans le document ServiceInfo, l’onglet **magasins en ligne** est représenté par l’élément **ServiceTask1** ; les éléments **ServiceTask2** et **ServiceTask3** sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="c735c-127">In the ServiceInfo document, the **Online Stores** tab is represented by the **ServiceTask1** element; the **ServiceTask2** and **ServiceTask3** elements are ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c735c-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c735c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c735c-129">**À propos des magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="c735c-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c735c-130">**Objet externe pour les magasins de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="c735c-130">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c735c-131">**Document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="c735c-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




