---
description: Disposition des clés de Registre
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Disposition des clés de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514904"
---
# <a name="layout-of-the-registry-keys"></a><span data-ttu-id="ee982-103">Disposition des clés de Registre</span><span class="sxs-lookup"><span data-stu-id="ee982-103">Layout of the Registry Keys</span></span>

<span data-ttu-id="ee982-104">Les filtres DirectShow sont enregistrés à deux emplacements :</span><span class="sxs-lookup"><span data-stu-id="ee982-104">DirectShow filters are registered in two places:</span></span>

-   <span data-ttu-id="ee982-105">La DLL qui contient le filtre est inscrite en tant que serveur COM du filtre.</span><span class="sxs-lookup"><span data-stu-id="ee982-105">The DLL that contains the filter is registered as the filter's COM server.</span></span> <span data-ttu-id="ee982-106">Quand une application appelle **CoCreateInstance** pour créer le filtre, la bibliothèque COM Microsoft Windows utilise cette entrée de Registre pour localiser la dll.</span><span class="sxs-lookup"><span data-stu-id="ee982-106">When an application calls **CoCreateInstance** to create the filter, the Microsoft Windows COM library uses this registry entry to locate the DLL.</span></span>
-   <span data-ttu-id="ee982-107">Des informations supplémentaires sur le filtre peuvent être inscrites dans une catégorie de filtre.</span><span class="sxs-lookup"><span data-stu-id="ee982-107">Additional information about the filter can be registered within a filter category.</span></span> <span data-ttu-id="ee982-108">Ces informations permettent à l' [énumérateur de périphérique système](system-device-enumerator.md) et au [Mappeur de filtre](filter-mapper.md) de localiser le filtre.</span><span class="sxs-lookup"><span data-stu-id="ee982-108">This information enables the [System Device Enumerator](system-device-enumerator.md) and the [Filter Mapper](filter-mapper.md) to locate the filter.</span></span>

<span data-ttu-id="ee982-109">Les filtres ne sont pas requis pour enregistrer les informations de filtre supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ee982-109">Filters are not required to register the additional filter information.</span></span> <span data-ttu-id="ee982-110">Tant que la DLL est inscrite en tant que serveur COM, une application peut créer le filtre et l’ajouter à un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="ee982-110">As long as the DLL is registered as the COM server, an application can create the filter and add it to a filter graph.</span></span> <span data-ttu-id="ee982-111">Toutefois, si vous souhaitez que votre filtre soit détectable par l’énumérateur du périphérique système ou le mappeur de filtre, vous devez enregistrer les informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ee982-111">However, if you want your filter to be discoverable by the System Device Enumerator or the Filter Mapper, you must register the additional information.</span></span>

<span data-ttu-id="ee982-112">L’entrée de Registre pour la DLL a les clés suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee982-112">The registry entry for the DLL has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



<span data-ttu-id="ee982-113">L’entrée de Registre pour les informations de filtre a les clés suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee982-113">The registry entry for the filter information has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



<span data-ttu-id="ee982-114">GUID d’une catégorie de filtre.</span><span class="sxs-lookup"><span data-stu-id="ee982-114">is the GUID of a filter category.</span></span> <span data-ttu-id="ee982-115">(Voir les [catégories de filtre](filter-categories.md).) Les informations de filtre sont compressées dans un format binaire.</span><span class="sxs-lookup"><span data-stu-id="ee982-115">(See [Filter Categories](filter-categories.md).) The filter information is packed into a binary format.</span></span> <span data-ttu-id="ee982-116">L’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) décompresse ces données lors de la recherche d’un filtre dans le registre.</span><span class="sxs-lookup"><span data-stu-id="ee982-116">The [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface unpacks this data when it searches the registry for a filter.</span></span>

<span data-ttu-id="ee982-117">Tous les GUID de catégorie de filtre sont répertoriés dans le Registre sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="ee982-117">All of the filter category GUIDs are listed in the registry under the following key:</span></span>


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



