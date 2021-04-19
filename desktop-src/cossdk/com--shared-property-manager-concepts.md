---
description: Dans COM+, l’état transitoire partagé pour les objets est géré à l’aide du gestionnaire de propriétés partagées (SPM). Le SPM est un distributeur de ressources que vous pouvez utiliser pour partager l’état entre plusieurs objets au sein d’un processus serveur.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Concepts de Gestionnaire de propriétés partagés COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514129"
---
# <a name="com-shared-property-manager-concepts"></a><span data-ttu-id="d8229-104">Concepts de Gestionnaire de propriétés partagés COM+</span><span class="sxs-lookup"><span data-stu-id="d8229-104">COM+ Shared Property Manager Concepts</span></span>

<span data-ttu-id="d8229-105">Dans COM+, l’état transitoire partagé pour les objets est géré à l’aide du gestionnaire de propriétés partagées (SPM).</span><span class="sxs-lookup"><span data-stu-id="d8229-105">In COM+, shared transient state for objects is managed by using the shared property manager (SPM).</span></span> <span data-ttu-id="d8229-106">Le SPM est un distributeur de ressources que vous pouvez utiliser pour partager l’état entre plusieurs objets au sein d’un processus serveur.</span><span class="sxs-lookup"><span data-stu-id="d8229-106">The SPM is a resource dispenser that you can use to share state among multiple objects within a server process.</span></span>

<span data-ttu-id="d8229-107">Vous ne pouvez pas utiliser de variables globales dans un environnement distribué en raison de problèmes de concurrence et de collision de noms.</span><span class="sxs-lookup"><span data-stu-id="d8229-107">You cannot use global variables in a distributed environment because of concurrency and name collision issues.</span></span> <span data-ttu-id="d8229-108">Le gestionnaire de propriétés partagées élimine les conflits de noms en fournissant des groupes de propriétés partagés, qui établissent des espaces de noms uniques pour les propriétés partagées qu’ils contiennent.</span><span class="sxs-lookup"><span data-stu-id="d8229-108">The shared property manager eliminates name collisions by providing shared property groups, which establish unique namespaces for the shared properties they contain.</span></span> <span data-ttu-id="d8229-109">Le SPM implémente également des verrous et des sémaphores pour aider à protéger les propriétés partagées de l’accès simultané, ce qui peut entraîner la perte de mises à jour et le fait de conserver les propriétés dans un État imprévisible.</span><span class="sxs-lookup"><span data-stu-id="d8229-109">The SPM also implements locks and semaphores to help protect shared properties from simultaneous access, which could result in lost updates and leave properties in an unpredictable state.</span></span>

> [!Note]  
> <span data-ttu-id="d8229-110">L’état transitoire partagé est des informations d’État conservées en mémoire qui ne survivent pas aux défaillances du système.</span><span class="sxs-lookup"><span data-stu-id="d8229-110">Shared transient state is state information kept in memory that does not survive system failures.</span></span> <span data-ttu-id="d8229-111">Les informations sont conçues pour être partagées par plusieurs objets entre les limites des transactions (mais pas entre les processus).</span><span class="sxs-lookup"><span data-stu-id="d8229-111">The information is designed to be shared by multiple objects across transaction (but not across process) boundaries.</span></span>

 

<span data-ttu-id="d8229-112">Les propriétés partagées stockées dans le SPM sont uniquement disponibles pour les objets qui s’exécutent dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="d8229-112">Shared properties stored in the SPM are available only to objects running in the same process.</span></span> <span data-ttu-id="d8229-113">Cela signifie que les objets qui utiliseront le SPM pour le stockage des valeurs et qui devront avoir accès à ces valeurs doivent être installés dans le cadre de la même application COM+.</span><span class="sxs-lookup"><span data-stu-id="d8229-113">This means that the objects that will use the SPM for storing values and that will need to have access to these values must be installed as part of the same COM+ application.</span></span> <span data-ttu-id="d8229-114">Il est possible pour les administrateurs système de déplacer des classes COM+ d’un package à un autre après le déploiement de votre application COM+.</span><span class="sxs-lookup"><span data-stu-id="d8229-114">It is possible for system administrators to move COM+ classes from one package to another after your COM+ application has been deployed.</span></span> <span data-ttu-id="d8229-115">Si vous vous fiez à plusieurs objets qui partagent des propriétés via le SPM, vous devez clairement documenter qu’ils doivent être installés dans la même application COM+.</span><span class="sxs-lookup"><span data-stu-id="d8229-115">If you rely on several objects sharing properties through the SPM, you should clearly document that they must be installed in the same COM+ application.</span></span>

<span data-ttu-id="d8229-116">Il est également important que les composants partageant des propriétés aient le même attribut d’activation.</span><span class="sxs-lookup"><span data-stu-id="d8229-116">It's also important for components sharing properties to have the same activation attribute.</span></span> <span data-ttu-id="d8229-117">Si deux composants dans le même package ont des attributs d’activation différents, ils ne peuvent généralement pas partager de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d8229-117">If two components in the same package have different activation attributes, they generally won't be able to share properties.</span></span> <span data-ttu-id="d8229-118">Par exemple, si un composant est configuré pour s’exécuter dans un processus client et que l’autre est configuré pour s’exécuter dans un processus serveur, ses objets s’exécutent généralement dans des processus différents même s’ils se trouvent dans le même package.</span><span class="sxs-lookup"><span data-stu-id="d8229-118">For example, if one component is configured to run in a client process and the other is configured to run in a server process, their objects will usually run in different processes even though they're in the same package.</span></span>

<span data-ttu-id="d8229-119">Vous devez toujours instancier les objets [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)et [**SHAREDPROPERTY**](sharedproperty.md) à partir de composants com+ plutôt qu’à partir d’un client de base.</span><span class="sxs-lookup"><span data-stu-id="d8229-119">You should always instantiate the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md), and [**SharedProperty**](sharedproperty.md) objects from COM+ components rather than from a base client.</span></span> <span data-ttu-id="d8229-120">Si un client de base crée des groupes de propriétés et des propriétés partagés, les propriétés partagées se trouvent à l’intérieur du processus client de base, et non dans un processus serveur.</span><span class="sxs-lookup"><span data-stu-id="d8229-120">If a base client creates shared property groups and properties, the shared properties are inside the base-client process, not in a server process.</span></span> <span data-ttu-id="d8229-121">Cela signifie que les objets COM+ ne peuvent pas partager les propriétés, à moins que les objets ne s’exécutent également dans le processus client (ce qui n’est généralement pas une bonne idée).</span><span class="sxs-lookup"><span data-stu-id="d8229-121">This means the COM+ objects cannot share the properties unless the objects are also running in the client process (which is generally not a good idea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8229-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d8229-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8229-123">Gestionnaire de propriétés partagé COM+</span><span class="sxs-lookup"><span data-stu-id="d8229-123">COM+ Shared Property Manager</span></span>](com--shared-property-manager.md)
</dt> <dt>

[<span data-ttu-id="d8229-124">Groupes de propriétés partagées</span><span class="sxs-lookup"><span data-stu-id="d8229-124">Shared Property Groups</span></span>](shared-property-groups.md)
</dt> </dl>

 

 



