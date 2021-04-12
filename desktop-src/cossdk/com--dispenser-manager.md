---
description: Le gestionnaire de distribution fournit la mise en pool des ressources pour les distributeurs de ressources et garantit qu’une ressource fournie par un distributeur de ressources est correctement inscrite dans la transaction des objets d’application.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Gestionnaire de distributeur COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523580"
---
# <a name="com-dispenser-manager"></a><span data-ttu-id="599e0-103">Gestionnaire de distributeur COM+</span><span class="sxs-lookup"><span data-stu-id="599e0-103">COM+ Dispenser Manager</span></span>

<span data-ttu-id="599e0-104">Le gestionnaire de distribution fournit la mise en pool des ressources pour les distributeurs de ressources et garantit qu’une ressource fournie par un distributeur de ressources est correctement inscrite dans la transaction de l’objet d’application.</span><span class="sxs-lookup"><span data-stu-id="599e0-104">The dispenser manager provides resource pooling for the resource dispensers and ensures that a resource supplied by a resource dispenser is correctly enlisted in the application object's transaction.</span></span> <span data-ttu-id="599e0-105">Le gestionnaire de distribution récupère automatiquement les ressources qui sont toujours réservées à la fin de la durée de vie d’un objet, ce qui élimine le risque de fuites de ressources.</span><span class="sxs-lookup"><span data-stu-id="599e0-105">The dispenser manager automatically reclaims resources that are still reserved at the end of an object's lifetime, eliminating the possibility of resource "leaks."</span></span> <span data-ttu-id="599e0-106">Le gestionnaire de distribution peut demander à un distributeur de ressources de créer une ressource ou de détruire des ressources inactives si nécessaire pour ajuster les niveaux d’inventaire, plutôt que d’utiliser des paramètres statiques.</span><span class="sxs-lookup"><span data-stu-id="599e0-106">The dispenser manager can ask a resource dispenser to create a new resource or to destroy idle resources when necessary to adjust inventory levels, rather than using static settings.</span></span>

> [!Note]  
> <span data-ttu-id="599e0-107">Étant donné que les interfaces de distributeur de ressources exposées à l’application ne doivent pas nécessairement être des interfaces COM, le gestionnaire de distribution peut être utilisé dans un processus sans initialiser COM, par exemple pour prendre en charge le distributeur de ressources ODBC.</span><span class="sxs-lookup"><span data-stu-id="599e0-107">Because resource dispenser interfaces exposed to the application are not required to be COM interfaces, the dispenser manager can be used in a process without initializing COM, for example, to support the ODBC resource dispenser.</span></span>

 

<span data-ttu-id="599e0-108">Lors de la création d’une ressource, le distributeur de ressources peut spécifier la durée pendant laquelle une ressource inactive est autorisée à rester dans le pool avant sa destruction.</span><span class="sxs-lookup"><span data-stu-id="599e0-108">Upon resource creation, the resource dispenser may specify how long an idle resource is allowed to remain in the pool before it's destroyed.</span></span> <span data-ttu-id="599e0-109">Un thread qui s’exécute dans le gestionnaire de distribution recherche toujours ces ressources inactives.</span><span class="sxs-lookup"><span data-stu-id="599e0-109">A thread that runs in the dispenser manager is always looking for these idle resources.</span></span>

## <a name="the-inventory-statistics-manager"></a><span data-ttu-id="599e0-110">Gestionnaire des statistiques d’inventaire</span><span class="sxs-lookup"><span data-stu-id="599e0-110">The Inventory Statistics Manager</span></span>

<span data-ttu-id="599e0-111">Le gestionnaire de distribution utilise le *Gestionnaire de statistiques d’inventaire* pour gérer les niveaux d’inventaire des ressources de pool.</span><span class="sxs-lookup"><span data-stu-id="599e0-111">The dispenser manager uses the *inventory statistics manager* to manage pool resource inventory levels.</span></span> <span data-ttu-id="599e0-112">Le gestionnaire des statistiques d’inventaire conserve un enregistrement de lorsque chaque ressource a été utilisée et supprime les ressources de l’inventaire lorsqu’elles n’ont pas été utilisées pendant *x* secondes, où la valeur de *x* est définie par ressource lors de la création de la ressource.</span><span class="sxs-lookup"><span data-stu-id="599e0-112">The inventory statistics manager maintains a record of when each resource was used and removes resources from inventory when they have not been used for *x* seconds, where the value of *x* is set per resource when the resource is created.</span></span>

## <a name="the-holder-component"></a><span data-ttu-id="599e0-113">Composant du détenteur</span><span class="sxs-lookup"><span data-stu-id="599e0-113">The Holder Component</span></span>

<span data-ttu-id="599e0-114">Le gestionnaire du distributeur interroge chaque *détenteur*, un composant créé par le gestionnaire du distributeur, qui répertorie l’inventaire des ressources pour chaque distributeur de ressources, toutes les 10 secondes pour lui permettre de réajuster son inventaire des ressources.</span><span class="sxs-lookup"><span data-stu-id="599e0-114">The dispenser manager polls each *holder*, a component created by the dispenser manager that lists the resource inventory for each resource dispenser, every 10 seconds to allow it to readjust its resource inventory.</span></span> <span data-ttu-id="599e0-115">Chaque détenteur appelle le gestionnaire de statistiques d’inventaire pour suggérer des niveaux de stock pour chaque type de ressource.</span><span class="sxs-lookup"><span data-stu-id="599e0-115">Each holder calls the inventory statistics manager to suggest inventory levels for each type of resource.</span></span> <span data-ttu-id="599e0-116">Par conséquent, le détenteur peut demander au distributeur de ressources de créer ou de détruire un inventaire.</span><span class="sxs-lookup"><span data-stu-id="599e0-116">As a result, the holder may ask the resource dispenser to either create or destroy some inventory.</span></span>

<span data-ttu-id="599e0-117">Le détenteur et le distributeur de ressources communiquent pour demander des ressources d’un type particulier.</span><span class="sxs-lookup"><span data-stu-id="599e0-117">The holder and resource dispenser communicate to request resources of a particular type.</span></span> <span data-ttu-id="599e0-118">Les relations suivantes existent entre le conteneur et le distributeur de ressources :</span><span class="sxs-lookup"><span data-stu-id="599e0-118">The following relationships exist between the holder and resource dispenser:</span></span>

-   <span data-ttu-id="599e0-119">Le détenteur peut demander une ressource à partir du distributeur de ressources.</span><span class="sxs-lookup"><span data-stu-id="599e0-119">The holder can request a resource from the resource dispenser.</span></span> <span data-ttu-id="599e0-120">Le distributeur de ressources retourne une ressource disponible ou en crée une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="599e0-120">The resource dispenser either returns an available resource or creates a new one.</span></span>
-   <span data-ttu-id="599e0-121">Le détenteur peut notifier au distributeur de ressources qu’une application n’a plus besoin d’une ressource, puis la renvoyer au pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="599e0-121">The holder can notify the resource dispenser that an application no longer needs a resource and then return it to the resource pool.</span></span>
-   <span data-ttu-id="599e0-122">Le détenteur et le distributeur de ressources fonctionnent ensemble pour conserver la taille du pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="599e0-122">The holder and the resource dispenser work together to maintain the size of the resource pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="599e0-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="599e0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="599e0-124">Concepts du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="599e0-124">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



