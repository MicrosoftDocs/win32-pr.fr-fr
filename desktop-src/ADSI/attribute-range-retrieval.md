---
title: Récupération de plage d’attributs
description: Un attribut à valeurs multiples peut avoir presque n’importe quel nombre de valeurs. Dans de nombreux cas, il peut être avantageux, voire nécessaire, de limiter la plage de valeurs récupérées par une requête.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- ADSI-récupération de plage d’attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939607"
---
# <a name="attribute-range-retrieval"></a><span data-ttu-id="84db6-105">Récupération de plage d’attributs</span><span class="sxs-lookup"><span data-stu-id="84db6-105">Attribute Range Retrieval</span></span>

<span data-ttu-id="84db6-106">Un attribut à valeurs multiples peut avoir presque n’importe quel nombre de valeurs.</span><span class="sxs-lookup"><span data-stu-id="84db6-106">A multi-valued attribute can have almost any number of values.</span></span> <span data-ttu-id="84db6-107">Dans de nombreux cas, il peut être avantageux, voire nécessaire, de limiter la plage de valeurs récupérées par une requête.</span><span class="sxs-lookup"><span data-stu-id="84db6-107">In many cases, it may be advantageous, or even necessary, to limit the range of values that are retrieved by a query.</span></span>

<span data-ttu-id="84db6-108">La récupération de plage implique de demander un nombre limité de valeurs d’attribut dans une seule requête.</span><span class="sxs-lookup"><span data-stu-id="84db6-108">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="84db6-109">Le nombre de valeurs demandé doit être inférieur ou égal au nombre maximal de valeurs prises en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="84db6-109">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="84db6-110">Pour réduire le nombre de fois que la requête doit contacter le serveur, le nombre de valeurs demandé doit être aussi proche que possible de cette valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="84db6-110">To reduce the number of times the query must contact the server, the number of values requested should be as close to this maximum as possible.</span></span> <span data-ttu-id="84db6-111">Pour permettre à une application de fonctionner correctement avec tous les serveurs Windows, un nombre maximal de 1000 doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="84db6-111">To enable an application to work correctly with all Windows servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="84db6-112">Les spécificateurs de plage pour une requête de propriété requièrent la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="84db6-112">The range specifiers for a property query require the following form:</span></span>


```C++
range=<low range>-<high range>
```



<span data-ttu-id="84db6-113">où « &lt; Low Range &gt; » est l’index de base zéro de la première valeur de propriété à récupérer et « &lt; High range &gt; » est l’index de base zéro de la dernière valeur de propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="84db6-113">where "&lt;low range&gt;" is the zero-based index of the first property value to retrieve and "&lt;high range&gt;" is the zero-based index of the last property value to retrieve.</span></span> <span data-ttu-id="84db6-114">La valeur zéro est utilisée pour &lt; la « plage inférieure &gt; » pour spécifier la première entrée.</span><span class="sxs-lookup"><span data-stu-id="84db6-114">Zero is used for "&lt;low range&gt;" to specify the first entry.</span></span> <span data-ttu-id="84db6-115">Le caractère générique ( \* ) peut être utilisé pour la « &lt; plage supérieure &gt; » afin de spécifier toutes les entrées restantes.</span><span class="sxs-lookup"><span data-stu-id="84db6-115">The wildcard character (\*) can be used for "&lt;high range&gt;" to specify all remaining entries.</span></span>

<span data-ttu-id="84db6-116">Le tableau suivant répertorie des exemples de spécificateurs de plage.</span><span class="sxs-lookup"><span data-stu-id="84db6-116">The following table lists examples of range specifiers.</span></span>



| <span data-ttu-id="84db6-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="84db6-117">Example</span></span>      | <span data-ttu-id="84db6-118">Description</span><span class="sxs-lookup"><span data-stu-id="84db6-118">Description</span></span>                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="84db6-119">plage = 0-\*</span><span class="sxs-lookup"><span data-stu-id="84db6-119">range=0-\*</span></span>   | <span data-ttu-id="84db6-120">Récupérez toutes les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="84db6-120">Retrieve all property values.</span></span> <span data-ttu-id="84db6-121">Cela est soumis à des limites imposées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="84db6-121">This is subject to limits imposed by the server.</span></span>                |
| <span data-ttu-id="84db6-122">plage = 0-500</span><span class="sxs-lookup"><span data-stu-id="84db6-122">range=0-500</span></span>  | <span data-ttu-id="84db6-123">Récupérer des valeurs de 1er à 501st inclusivement.</span><span class="sxs-lookup"><span data-stu-id="84db6-123">Retrieve from 1st to 501st values inclusively.</span></span>                                                |
| <span data-ttu-id="84db6-124">plage = 2-3</span><span class="sxs-lookup"><span data-stu-id="84db6-124">range=2-3</span></span>    | <span data-ttu-id="84db6-125">Récupérez les 3e et 4e valeurs.</span><span class="sxs-lookup"><span data-stu-id="84db6-125">Retrieve 3rd and 4th values.</span></span>                                                                  |
| <span data-ttu-id="84db6-126">plage = 501-\*</span><span class="sxs-lookup"><span data-stu-id="84db6-126">range=501-\*</span></span> | <span data-ttu-id="84db6-127">Récupérez le 502nd et toutes les valeurs restantes.</span><span class="sxs-lookup"><span data-stu-id="84db6-127">Retrieve the 502nd and all remaining values.</span></span> <span data-ttu-id="84db6-128">Cela est soumis à des limites imposées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="84db6-128">This is subject to limits imposed by the server.</span></span> |



 

<span data-ttu-id="84db6-129">Il existe plusieurs façons de récupérer une plage de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="84db6-129">There are several different ways to retrieve a range of property values.</span></span> <span data-ttu-id="84db6-130">La méthode [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) peut être utilisée dans un langage Automation ou C++.</span><span class="sxs-lookup"><span data-stu-id="84db6-130">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method can be used in either an automation language or C++.</span></span> <span data-ttu-id="84db6-131">La méthode **IADs. GetInfoEx** est la méthode recommandée pour effectuer une récupération de plage.</span><span class="sxs-lookup"><span data-stu-id="84db6-131">The **IADs.GetInfoEx** method is the preferred method of performing range retrieval.</span></span> <span data-ttu-id="84db6-132">Pour plus d’informations sur l’utilisation de **IADs. GetInfoEx** pour la récupération de plages, consultez [utilisation de IADs :: GetInfoEx pour la récupération de plages](using-iads--getinfoex-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="84db6-132">For more information about using **IADs.GetInfoEx** for range retrieval, see [Using IADs::GetInfoEx for Range Retrieval](using-iads--getinfoex-for-range-retrieval.md).</span></span>

<span data-ttu-id="84db6-133">Si un langage Automation est utilisé, les objets d’annuaire ActiveX (ADO) peuvent être utilisés pour récupérer une plage de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="84db6-133">If an automation language is used, the ActiveX Directory Objects (ADO) can be used to retrieve a range of property values.</span></span> <span data-ttu-id="84db6-134">Pour plus d’informations sur l’utilisation d’ADO pour la récupération de plages, consultez [utilisation d’ADO pour la récupération de plages](using-ado-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="84db6-134">For more information about using ADO for range retrieval, see [Using ADO for Range Retrieval](using-ado-for-range-retrieval.md).</span></span>

<span data-ttu-id="84db6-135">Si vous utilisez C++, les interfaces [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) et [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) peuvent être utilisées pour récupérer une plage de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="84db6-135">If C++ is used, the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) and [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="84db6-136">Pour plus d’informations sur l’utilisation de **IDirectorySearch** et **IDirectoryObject** pour la récupération de plages, consultez [utilisation de IDirectorySearch et IDirectoryObject pour la récupération de plages](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="84db6-136">For more information about using **IDirectorySearch** and **IDirectoryObject** for range retrieval, see [Using IDirectorySearch and IDirectoryObject for Range Retrieval](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span></span>

 

 




