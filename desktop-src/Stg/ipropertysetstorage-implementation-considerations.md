---
title: Considérations relatives à l’implémentation de IPropertySetStorage
description: Plusieurs problèmes surviennent lors de l’étude de la façon de fournir une implémentation de l’interface IPropertySetStorage qui lit et écrit le format du jeu de propriétés COM. qui sont décrites dans les sections suivantes.
ms.assetid: 055da516-ed42-49ec-b20c-a5e98718bea8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7532211668fa1ecf290484a707b19e1c263b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674693"
---
# <a name="ipropertysetstorage-implementation-considerations"></a><span data-ttu-id="a7a9c-104">Considérations relatives à l’implémentation de IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="a7a9c-104">IPropertySetStorage Implementation Considerations</span></span>

<span data-ttu-id="a7a9c-105">Plusieurs problèmes surviennent lors de l’étude de la façon de fournir une implémentation de l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) qui lit et écrit le format du jeu de propriétés com.</span><span class="sxs-lookup"><span data-stu-id="a7a9c-105">Several issues arise when considering how to provide an implementation of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface that reads and writes the COM property set format.</span></span> <span data-ttu-id="a7a9c-106">qui sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="a7a9c-106">The following sections describe these considerations.</span></span>

-   [<span data-ttu-id="a7a9c-107">Noms dans IStorage</span><span class="sxs-lookup"><span data-stu-id="a7a9c-107">Names in IStorage</span></span>](names-in-istorage.md)
-   [<span data-ttu-id="a7a9c-108">Objets de stockage et de flux pour un jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="a7a9c-108">Storage and Stream Objects for a Property Set</span></span>](storage-vs--stream-for-a-property-set.md)
-   [<span data-ttu-id="a7a9c-109">Définition de l’identificateur de classe du jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="a7a9c-109">Setting the Property Set Class Identifier</span></span>](setting-the-property-set-class-identifier.md)
-   [<span data-ttu-id="a7a9c-110">Points de synchronisation</span><span class="sxs-lookup"><span data-stu-id="a7a9c-110">Synchronization Points</span></span>](synchronization-points.md)
-   [<span data-ttu-id="a7a9c-111">Pages de codes et chaînes Unicode</span><span class="sxs-lookup"><span data-stu-id="a7a9c-111">Code Pages and Unicode Strings</span></span>](code-pages-and-unicode-strings.md)
-   [<span data-ttu-id="a7a9c-112">Dictionnaire</span><span class="sxs-lookup"><span data-stu-id="a7a9c-112">Dictionary</span></span>](dictionary.md)
-   [<span data-ttu-id="a7a9c-113">Extensions</span><span class="sxs-lookup"><span data-stu-id="a7a9c-113">Extensions</span></span>](extensions.md)
-   [<span data-ttu-id="a7a9c-114">Sérialisation du jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="a7a9c-114">Property Set Serialization</span></span>](version-0-vs--version-1-property-set-serialization.md)

<span data-ttu-id="a7a9c-115">Pour plus d’informations, consultez [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) dans la section de référence sous interfaces.</span><span class="sxs-lookup"><span data-stu-id="a7a9c-115">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) in the Reference section under Interfaces.</span></span>

 

 




