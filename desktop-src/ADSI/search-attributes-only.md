---
title: Rechercher des attributs uniquement
description: Parfois, vous effectuez une recherche pour déterminer le type de données disponibles pour un objet.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Attributs de recherche uniquement ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939579"
---
# <a name="search-attributes-only"></a><span data-ttu-id="32329-104">Rechercher des attributs uniquement</span><span class="sxs-lookup"><span data-stu-id="32329-104">Search Attributes Only</span></span>

<span data-ttu-id="32329-105">Parfois, vous effectuez une recherche pour déterminer le type de données disponibles pour un objet.</span><span class="sxs-lookup"><span data-stu-id="32329-105">Sometimes you perform a search to determine what type of data is available for an object.</span></span> <span data-ttu-id="32329-106">Dans ce cas, vous vous intéressez uniquement aux attributs, et non aux valeurs, de l’objet.</span><span class="sxs-lookup"><span data-stu-id="32329-106">In this case, you are interested only in the attributes, and not the values, of the object.</span></span> <span data-ttu-id="32329-107">Pour ce faire, vous devez définir l’option « Rechercher les attributs uniquement ».</span><span class="sxs-lookup"><span data-stu-id="32329-107">To accomplish this, you set the "search attributes only" option.</span></span> <span data-ttu-id="32329-108">La spécification de cette option retourne les noms des attributs sans leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="32329-108">Specifying this option returns the attribute names without their values.</span></span> <span data-ttu-id="32329-109">Toutefois, le jeu de résultats comprend uniquement les attributs qui ont des valeurs affectées.</span><span class="sxs-lookup"><span data-stu-id="32329-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="32329-110">Par exemple, considérez un objet avec les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="32329-110">For example, consider an object with the following attributes:</span></span>

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

<span data-ttu-id="32329-111">Lorsque l’option Rechercher uniquement les attributs est définie, le jeu de résultats comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="32329-111">When the search attributes only option is set, the result set includes:</span></span>

``` syntax
First Name
Last Name
Phone Number
```

<span data-ttu-id="32329-112">Pour plus d’informations sur l’utilisation de l’option Rechercher des attributs uniquement avec une interface de recherche spécifique, consultez :</span><span class="sxs-lookup"><span data-stu-id="32329-112">For more information about using the search attributes only option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="32329-113">Retour uniquement des noms d’attributs avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="32329-113">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)
-   [<span data-ttu-id="32329-114">Recherche avec ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="32329-114">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="32329-115">Recherche avec OLE DB</span><span class="sxs-lookup"><span data-stu-id="32329-115">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




