---
title: External. OnChangeViewError, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnChangeViewError, événement
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Événement External. OnChangeViewError lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533173"
---
# <a name="externalonchangeviewerror-event"></a><span data-ttu-id="b1e3c-105">External. OnChangeViewError, événement</span><span class="sxs-lookup"><span data-stu-id="b1e3c-105">External.OnChangeViewError Event</span></span>

> [!Note]  
> <span data-ttu-id="b1e3c-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="b1e3c-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b1e3c-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b1e3c-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b1e3c-108">L’événement **OnChangeViewError** se produit lorsqu’un appel à la méthode [External. changeView](external-changeview.md) génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="b1e3c-108">The **OnChangeViewError** event occurs when a call to the [External.changeView](external-changeview.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="b1e3c-109">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b1e3c-109">Possible Values</span></span>

<span data-ttu-id="b1e3c-110">Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="b1e3c-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1e3c-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1e3c-111">Parameters</span></span>

<span data-ttu-id="b1e3c-112">La fonction qui gère cet événement a les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="b1e3c-112">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="b1e3c-113"><span id="hr"></span><span id="HR"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="b1e3c-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="b1e3c-114">Code d’erreur **HRESULT** indiquant la raison de l’échec.</span><span class="sxs-lookup"><span data-stu-id="b1e3c-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="b1e3c-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span><span class="sxs-lookup"><span data-stu-id="b1e3c-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="b1e3c-116">La même chaîne qui a été passée dans le paramètre **LibraryLocationType** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="b1e3c-116">The same string that was passed in the **LibraryLocationType** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="b1e3c-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span><span class="sxs-lookup"><span data-stu-id="b1e3c-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="b1e3c-118">La même chaîne thatwas transmise dans le paramètre **LibraryLocationID** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="b1e3c-118">The same string thatwas passed in the **LibraryLocationID** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="b1e3c-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filtres*</span><span class="sxs-lookup"><span data-stu-id="b1e3c-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filter*</span></span>
</dt> <dd>

<span data-ttu-id="b1e3c-120">La même chaîne qui a été passée dans le paramètre de **filtre** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="b1e3c-120">The same string that was passed in the **Filter** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="b1e3c-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span><span class="sxs-lookup"><span data-stu-id="b1e3c-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span></span>
</dt> <dd>

<span data-ttu-id="b1e3c-122">La même chaîne qui a été passée dans le paramètre **ViewParams** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="b1e3c-122">The same string that was passed in the **ViewParams** parameter of **changeView**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1e3c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1e3c-123">Requirements</span></span>



| <span data-ttu-id="b1e3c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1e3c-124">Requirement</span></span> | <span data-ttu-id="b1e3c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1e3c-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e3c-126">Version</span><span class="sxs-lookup"><span data-stu-id="b1e3c-126">Version</span></span><br/> | <span data-ttu-id="b1e3c-127">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="b1e3c-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="b1e3c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b1e3c-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="b1e3c-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1e3c-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1e3c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1e3c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e3c-131">**ExternalObject pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="b1e3c-131">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





