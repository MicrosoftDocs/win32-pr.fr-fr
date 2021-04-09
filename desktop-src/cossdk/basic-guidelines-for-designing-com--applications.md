---
description: Instructions de base pour la conception d’applications COM+
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Instructions de base pour la conception d’applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111046"
---
# <a name="basic-guidelines-for-designing-com-applications"></a><span data-ttu-id="66913-103">Instructions de base pour la conception d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="66913-103">Basic Guidelines for Designing COM+ Applications</span></span>

<span data-ttu-id="66913-104">Pour tirer pleinement parti de COM+, vous pouvez utiliser quelques recommandations de base lors de la création d’une application :</span><span class="sxs-lookup"><span data-stu-id="66913-104">To take full advantage of COM+, there are a few basic guidelines you can use when creating an application:</span></span>

-   <span data-ttu-id="66913-105">**Modélisez votre état durable comme un schéma de base de données, à l’aide de l’outil de base de données de votre choix.**</span><span class="sxs-lookup"><span data-stu-id="66913-105">**Model your durable state as a database schema, using your database tool of choice.**</span></span> <span data-ttu-id="66913-106">Presque toutes les applications doivent maintenir un État durable.</span><span class="sxs-lookup"><span data-stu-id="66913-106">Almost every application needs to maintain durable state.</span></span> <span data-ttu-id="66913-107">Les bases de données fournissent les services nécessaires pour créer un stockage durable et évolutif de l’État.</span><span class="sxs-lookup"><span data-stu-id="66913-107">Databases provide the services needed to create durable and scalable storage of state.</span></span> <span data-ttu-id="66913-108">Par conséquent, la première étape de la création d’une application COM+ consiste à modéliser l’État durable de votre application en tant que schéma de base de données.</span><span class="sxs-lookup"><span data-stu-id="66913-108">Therefore, the first step in creating a COM+ application is to model the durable state of your application as some sort of database schema.</span></span> <span data-ttu-id="66913-109">La base de données que vous utilisez n’a pas vraiment d’importance. la plupart des bases de données commerciales sont compatibles avec COM+.</span><span class="sxs-lookup"><span data-stu-id="66913-109">It doesn't really matter what database you use; most commercial databases are compatible with COM+.</span></span> <span data-ttu-id="66913-110">Microsoft SQL Server est un bon exemple d’une solution que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="66913-110">Microsoft SQL Server is a good example of one solution you could use.</span></span>

-   <span data-ttu-id="66913-111">**Modélisez la logique de votre application COM+ sous la forme d’un ensemble d’interfaces COM.**</span><span class="sxs-lookup"><span data-stu-id="66913-111">**Model the logic of your COM+ application as a set of COM interfaces.**</span></span> <span data-ttu-id="66913-112">Une fois que vous avez un schéma qui représente les informations d’état de l’application, modélisez les échanges qui se produisent dans l’application en tant qu’interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="66913-112">Once you have a schema that represents the state information of the application, model the interchanges that happen in the application as COM interfaces.</span></span> <span data-ttu-id="66913-113">Ces interfaces modéliseront le comportement de l’application.</span><span class="sxs-lookup"><span data-stu-id="66913-113">These interfaces will model the behavior of the application.</span></span> <span data-ttu-id="66913-114">Il s’agit également de la phase de développement lorsque vous devez déterminer les services COM+ qui conviennent le mieux à votre application.</span><span class="sxs-lookup"><span data-stu-id="66913-114">This is also the development stage when you should determine which COM+ services work best for your application.</span></span>

-   <span data-ttu-id="66913-115">**Générez des dll de composant qui contiennent des composants qui utilisent le schéma de données physique et exposent une vue logique des données à d’autres composants (le premier élément de cette liste), ainsi que des composants implémentés en termes de modèle de données logique (le deuxième élément de cette liste).**</span><span class="sxs-lookup"><span data-stu-id="66913-115">**Build component DLLs that contain components that use the physical data schema and expose a logical view of the data to other components (the first item in this list), as well as components that are implemented in terms of the logical data model (the second item in this list).**</span></span> <span data-ttu-id="66913-116">Une fois que vous disposez de la structure de la logique et des informations d’État, vous pouvez commencer à écrire du code et vous pouvez maintenant écrire des composants COM basés sur des DLL qui implémentent les interfaces en termes de schéma défini.</span><span class="sxs-lookup"><span data-stu-id="66913-116">Once you have the structure of the logic and the state information, you can begin to write code and can now write DLL-based COM components that implement the interfaces in terms of the defined schema.</span></span> <span data-ttu-id="66913-117">Vos composants agissent simplement comme manipulateurs pour l’utilisation de vos informations de base de données, et vos dll de composant vous permettent de créer une application COM+ qui fonctionne et dont l’échelle est correcte.</span><span class="sxs-lookup"><span data-stu-id="66913-117">Your components simply act as manipulators for working with your database information, and your component DLLs enable you build a COM+ application that works and that scales successfully.</span></span>

-   <span data-ttu-id="66913-118">**Déployez les composants dans l’environnement COM+ à l’aide des services COM+ que vous avez sélectionnés.**</span><span class="sxs-lookup"><span data-stu-id="66913-118">**Deploy the components in the COM+ environment using the COM+ services you've selected.**</span></span> <span data-ttu-id="66913-119">Une fois que vous avez créé l’application, vous pouvez déployer l’application sur un réseau ou un cluster de serveurs.</span><span class="sxs-lookup"><span data-stu-id="66913-119">Once you have built the application, you can then deploy the application across a network or server cluster.</span></span> <span data-ttu-id="66913-120">Vous pouvez désormais prendre des décisions en fonction des ressources disponibles, et vous pouvez adapter chaque composant pour obtenir des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="66913-120">You can now make decisions based on resources available, and you can tailor each component for maximum performance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66913-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66913-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66913-122">Hypothèses et principes de conception de COM+</span><span class="sxs-lookup"><span data-stu-id="66913-122">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="66913-123">Conception de l’application COM+ à l’aide d’UML</span><span class="sxs-lookup"><span data-stu-id="66913-123">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="66913-124">Conseils de conception générale pour l’utilisation de COM+</span><span class="sxs-lookup"><span data-stu-id="66913-124">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="66913-125">Optimisation des interactions avec le niveau de logique métier COM+</span><span class="sxs-lookup"><span data-stu-id="66913-125">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="66913-126">Autres outils Microsoft pour la création d’applications distribuées</span><span class="sxs-lookup"><span data-stu-id="66913-126">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



