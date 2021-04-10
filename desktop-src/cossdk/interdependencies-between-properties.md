---
description: Interdépendances entre les propriétés
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Interdépendances entre les propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950668"
---
# <a name="interdependencies-between-properties"></a><span data-ttu-id="bdc92-103">Interdépendances entre les propriétés</span><span class="sxs-lookup"><span data-stu-id="bdc92-103">Interdependencies Between Properties</span></span>

<span data-ttu-id="bdc92-104">Lorsque vous définissez des propriétés, le catalogue COM+ met en œuvre une logique de cohérence pour vous assurer que vous configurez les éléments de manière raisonnable.</span><span class="sxs-lookup"><span data-stu-id="bdc92-104">When you set properties, the COM+ catalog enforces some coherency logic to ensure that you configure elements in a reasonable way.</span></span> <span data-ttu-id="bdc92-105">Cette logique peut être implémentée de deux manières, comme suit :</span><span class="sxs-lookup"><span data-stu-id="bdc92-105">This logic can be implemented in two ways, as follows:</span></span>

-   <span data-ttu-id="bdc92-106">**Dépendances.**</span><span class="sxs-lookup"><span data-stu-id="bdc92-106">**Dependencies.**</span></span> <span data-ttu-id="bdc92-107">Vous risquez de ne pas pouvoir apporter des modifications, car une autre propriété dépend d’un paramètre particulier pour une propriété que vous essayez de définir.</span><span class="sxs-lookup"><span data-stu-id="bdc92-107">You might be blocked from making some changes because another property depends on a particular setting for a property you attempt to set.</span></span> <span data-ttu-id="bdc92-108">Par exemple, si un composant est défini avec les transactions d’attribut requises et si vous tentez ensuite de modifier le paramètre de synchronisation sur aucun, une erreur est générée lorsque vous tentez d’appeler [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) , car les transactions dépendent de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="bdc92-108">For example, if a component is set with the attribute Transactions Required and if you then attempt to change the Synchronization setting to None, an error is generated when you attempt to call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) because transactions depend on synchronization.</span></span>
-   <span data-ttu-id="bdc92-109">**Effets secondaires.**</span><span class="sxs-lookup"><span data-stu-id="bdc92-109">**Side effects.**</span></span> <span data-ttu-id="bdc92-110">Certaines propriétés peuvent être modifiées pour vous si vous ne les définissez pas explicitement.</span><span class="sxs-lookup"><span data-stu-id="bdc92-110">Some properties might be changed for you without your explicitly setting them.</span></span> <span data-ttu-id="bdc92-111">Par exemple, si vous définissez un composant avec l’attribut transactions requis, la synchronisation est définie sur obligatoire.</span><span class="sxs-lookup"><span data-stu-id="bdc92-111">For example, if you set a component with the attribute Transactions Required, Synchronization will be set to Required as well.</span></span> <span data-ttu-id="bdc92-112">C’est vraiment le côté inverse des dépendances : une propriété est prioritaire sur une autre, et sa dépendance est exprimée par la première définition de la propriété secondaire, puis par le blocage des modifications.</span><span class="sxs-lookup"><span data-stu-id="bdc92-112">This is really the flip side of dependencies—one property takes precedence over another, and its dependency is expressed through first setting the secondary property and then blocking changes to it.</span></span>

<span data-ttu-id="bdc92-113">Dans la liste des propriétés exposées par les éléments d’une collection, tous les éléments répertoriés dans les [collections d’administration com+](com--administration-collections.md), les dépendances et les effets secondaires sont indiqués pour chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="bdc92-113">In the list of properties exposed by items in a collection, all listed in [COM+ Administration Collections](com--administration-collections.md), the dependencies and side effects are stated for each property.</span></span> <span data-ttu-id="bdc92-114">Quand vous configurez des applications et des composants COM+, vous devez connaître les contraintes imposées aux configurations.</span><span class="sxs-lookup"><span data-stu-id="bdc92-114">When you configure COM+ applications and components, you should be aware of what constraints are imposed on configurations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdc92-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bdc92-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc92-116">Obtention et définition des propriétés</span><span class="sxs-lookup"><span data-stu-id="bdc92-116">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="bdc92-117">Interrogation des propriétés disponibles</span><span class="sxs-lookup"><span data-stu-id="bdc92-117">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="bdc92-118">Enregistrement ou rejet des modifications</span><span class="sxs-lookup"><span data-stu-id="bdc92-118">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



