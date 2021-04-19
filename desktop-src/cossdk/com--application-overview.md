---
description: Une application COM+ est l’unité principale d’administration et de sécurité pour les services de composants et se compose d’un groupe de composants COM qui exécutent généralement des fonctions associées.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Vue d’ensemble de l’application COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "106522483"
---
# <a name="com-application-overview"></a><span data-ttu-id="5a256-103">Vue d’ensemble de l’application COM+</span><span class="sxs-lookup"><span data-stu-id="5a256-103">COM+ Application Overview</span></span>

<span data-ttu-id="5a256-104">Une application COM+ est l’unité principale d’administration et de sécurité pour les services de composants et se compose d’un groupe de composants COM qui exécutent généralement des fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="5a256-104">A COM+ application is the primary unit of administration and security for Component Services and consists of a group of COM components that generally perform related functions.</span></span> <span data-ttu-id="5a256-105">Ces composants se composent davantage d’interfaces et de méthodes, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="5a256-105">These components further consist of interfaces and methods, as shown in the following illustration.</span></span>

![Diagramme qui affiche des interfaces et des méthodes à l’intérieur des zones, par ordre de méthode dans une interface à l’intérieur d’une application COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

<span data-ttu-id="5a256-107">Vous pouvez utiliser l’outil d’administration Services de composants pour créer des applications COM+, ajouter des composants aux applications et définir les attributs d’une application et de ses composants.</span><span class="sxs-lookup"><span data-stu-id="5a256-107">You can use the Component Services administrative tool to create new COM+ applications, add components to applications, and set the attributes for an application and its components.</span></span>

<span data-ttu-id="5a256-108">En créant des groupes logiques de composants COM en tant qu’applications COM+, vous pouvez tirer parti des avantages suivants de COM+ :</span><span class="sxs-lookup"><span data-stu-id="5a256-108">By creating logical groups of COM components as COM+ applications, you can take advantage of the following benefits of COM+:</span></span>

-   <span data-ttu-id="5a256-109">Une étendue de déploiement pour les composants COM.</span><span class="sxs-lookup"><span data-stu-id="5a256-109">A deployment scope for COM components.</span></span>
-   <span data-ttu-id="5a256-110">Étendue de configuration commune pour les composants COM, y compris les limites de sécurité et la mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="5a256-110">A common configuration scope for COM components, including security boundaries and queuing.</span></span>
-   <span data-ttu-id="5a256-111">Stockage des attributs de composant non fournis par le développeur de composants (par exemple, transactions et synchronisation).</span><span class="sxs-lookup"><span data-stu-id="5a256-111">Storage of component attributes not provided by the component developer (for example, transactions and synchronization).</span></span>
-   <span data-ttu-id="5a256-112">Les bibliothèques de liens dynamiques (dll) du composant sont chargées dans des processus (DLLHost.exe) à la demande.</span><span class="sxs-lookup"><span data-stu-id="5a256-112">Component dynamic-link libraries (DLLs) loaded into processes (DLLHost.exe) on demand.</span></span>
-   <span data-ttu-id="5a256-113">Processus serveur managés pour héberger des composants.</span><span class="sxs-lookup"><span data-stu-id="5a256-113">Managed server processes to host components.</span></span>
-   <span data-ttu-id="5a256-114">Création et gestion des threads utilisés par les composants.</span><span class="sxs-lookup"><span data-stu-id="5a256-114">Creation and management of threads used by components.</span></span>
-   <span data-ttu-id="5a256-115">Accès à l’objet de contexte pour les distributeurs de ressources, ce qui permet aux ressources acquises d’être automatiquement associées au contexte.</span><span class="sxs-lookup"><span data-stu-id="5a256-115">Access to the context object for resource dispensers, allowing acquired resources to be automatically associated with the context.</span></span> <span data-ttu-id="5a256-116">(Pour plus d’informations sur les composants COM et les contextes, consultez [contextes com+](com--contexts.md).)</span><span class="sxs-lookup"><span data-stu-id="5a256-116">(For more information on COM components and contexts, see [COM+ Contexts](com--contexts.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a256-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a256-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a256-118">Développement d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="5a256-118">Developing COM+ Applications</span></span>](developing-com--applications.md)
</dt> <dt>

[<span data-ttu-id="5a256-119">Parties d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="5a256-119">Parts of a COM+ Application</span></span>](parts-of-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="5a256-120">Types d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="5a256-120">Types of COM+ Applications</span></span>](types-of-com--applications.md)
</dt> </dl>

 

 



