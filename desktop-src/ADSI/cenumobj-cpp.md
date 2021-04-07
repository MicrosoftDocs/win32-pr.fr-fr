---
title: CENUMOBJ. COTISATIONS
description: Dans l’exemple de composant fournisseur, l’énumération d’un objet conteneur utilise les routines de cenumobj. cpp, énumérées dans le tableau suivant.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730196"
---
# <a name="cenumobjcpp"></a><span data-ttu-id="bb8d4-103">CENUMOBJ. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="bb8d4-103">CENUMOBJ.CPP</span></span>

<span data-ttu-id="bb8d4-104">Dans l’exemple de composant fournisseur, l’énumération d’un objet conteneur utilise les routines de cenumobj. cpp, énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-104">In the example provider component, the enumeration of a container object uses the routines, from cenumobj.cpp, listed in the following table.</span></span>



| <span data-ttu-id="bb8d4-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="bb8d4-105">Method</span></span>                                                 | <span data-ttu-id="bb8d4-106">Description</span><span class="sxs-lookup"><span data-stu-id="bb8d4-106">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb8d4-107">**CSampleDSGenObjectEnum :: Create**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-107">**CSampleDSGenObjectEnum::Create**</span></span>                     | <span data-ttu-id="bb8d4-108">Créez un objet pour permettre l’énumération des objets Active Directory génériques.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-108">Create an object to enable enumeration of generic Active Directory objects.</span></span>                                                                                           |
| <span data-ttu-id="bb8d4-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span></span>     | <span data-ttu-id="bb8d4-110">Initialisation.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-110">Initialization.</span></span>                                                                                                                                                       |
| <span data-ttu-id="bb8d4-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="bb8d4-112">Gérer la récupération d’objets.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-112">Manage retrieval of objects.</span></span>                                                                                                                                          |
| <span data-ttu-id="bb8d4-113">**CSampleDSGenObjectEnum::FetchObjects**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-113">**CSampleDSGenObjectEnum::FetchObjects**</span></span>               | <span data-ttu-id="bb8d4-114">Récupérez l’ensemble de pointeurs [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui correspondent au filtre.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-114">Retrieve the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers that match the filter.</span></span>                                                             |
| <span data-ttu-id="bb8d4-115">**CSampleDSGenObjectEnum::FetchNextObject**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-115">**CSampleDSGenObjectEnum::FetchNextObject**</span></span>            | <span data-ttu-id="bb8d4-116">Récupérez un objet et comparez-le au filtre.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-116">Retrieve an object and match against the filter.</span></span> <span data-ttu-id="bb8d4-117">Si elle correspond, encapsulez-la dans l’objet générique et retournez un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="bb8d4-117">If it matches, wrap it in generic object and return a [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |
| <span data-ttu-id="bb8d4-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="bb8d4-119">Gérer la récupération des objets.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-119">Manage retrieving the objects.</span></span>                                                                                                                                        |
| <span data-ttu-id="bb8d4-120">**CSampleDSGenObjectEnum :: suivant**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-120">**CSampleDSGenObjectEnum::Next**</span></span>                       | <span data-ttu-id="bb8d4-121">Récupère le nombre spécifié d’éléments de l’objet d’énumération indiqué.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-121">Retrieve the specified number of elements from the enumeration object indicated.</span></span>                                                                                      |
| <span data-ttu-id="bb8d4-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span></span>            | <span data-ttu-id="bb8d4-123">Vérifiez que la classe d’objet en trouve une dans la liste de filtres.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-123">Verify that object class matches one in the filter list.</span></span>                                                                                                              |
| <span data-ttu-id="bb8d4-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span></span>         | <span data-ttu-id="bb8d4-125">Gérez le tableau de filtres.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-125">Manage the filter array.</span></span>                                                                                                                                              |
| <span data-ttu-id="bb8d4-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span></span> | <span data-ttu-id="bb8d4-127">Ajoutez une nouvelle classe d’objet au filtre et définissez le filtre comme étant contigu.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-127">Add a new object class to the filter and set the filter as contiguous.</span></span>                                                                                                |
| <span data-ttu-id="bb8d4-128">**FreeFilterList**</span><span class="sxs-lookup"><span data-stu-id="bb8d4-128">**FreeFilterList**</span></span>                                     | <span data-ttu-id="bb8d4-129">Libérez le filtre.</span><span class="sxs-lookup"><span data-stu-id="bb8d4-129">Free the filter.</span></span>                                                                                                                                                      |



 

 

 