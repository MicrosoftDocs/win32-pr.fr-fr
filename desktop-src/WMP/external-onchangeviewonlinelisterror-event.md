---
title: External. OnChangeViewOnlineListError, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnChangeViewOnlineListError, événement
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Événement External. OnChangeViewOnlineListError lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529950"
---
# <a name="externalonchangeviewonlinelisterror-event"></a><span data-ttu-id="82131-105">External. OnChangeViewOnlineListError, événement</span><span class="sxs-lookup"><span data-stu-id="82131-105">External.OnChangeViewOnlineListError Event</span></span>

> [!Note]  
> <span data-ttu-id="82131-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="82131-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="82131-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="82131-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="82131-108">L’événement **OnChangeViewOnlineListError** se produit lorsqu’un appel à la méthode [External. changeViewOnlineList](external-changeviewonlinelist.md) génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="82131-108">The **OnChangeViewOnlineListError** event occurs when a call to the [External.changeViewOnlineList](external-changeviewonlinelist.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a><span data-ttu-id="82131-109">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="82131-109">Possible Values</span></span>

<span data-ttu-id="82131-110">Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="82131-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="82131-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82131-111">Parameters</span></span>

<span data-ttu-id="82131-112">La fonction qui gère cette erreur a les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="82131-112">The function that handles this error has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="82131-113"><span id="hr"></span><span id="HR"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="82131-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="82131-114">Code d’erreur **HRESULT** indiquant la raison de l’échec.</span><span class="sxs-lookup"><span data-stu-id="82131-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="82131-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span><span class="sxs-lookup"><span data-stu-id="82131-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="82131-116">La même chaîne qui a été passée dans le paramètre **LibraryLocationType** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="82131-116">The same string that was passed in the **LibraryLocationType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="82131-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span><span class="sxs-lookup"><span data-stu-id="82131-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="82131-118">La même chaîne qui a été passée dans le paramètre **LibraryLocationID** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="82131-118">The same string that was passed in the **LibraryLocationID** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="82131-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span><span class="sxs-lookup"><span data-stu-id="82131-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span></span>
</dt> <dd>

<span data-ttu-id="82131-120">La même chaîne qui a été passée dans le paramètre **params** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="82131-120">The same string that was passed in the **Params** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="82131-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*Convivial*</span><span class="sxs-lookup"><span data-stu-id="82131-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span></span>
</dt> <dd>

<span data-ttu-id="82131-122">La même chaîne qui a été passée dans le paramètre **FriendlyName** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="82131-122">The same string that was passed in the **FriendlyName** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="82131-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*Type*</span><span class="sxs-lookup"><span data-stu-id="82131-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span></span>
</dt> <dd>

<span data-ttu-id="82131-124">La même chaîne qui a été passée dans le paramètre **ListType** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="82131-124">The same string that was passed in the **ListType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="82131-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span><span class="sxs-lookup"><span data-stu-id="82131-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span></span>
</dt> <dd>

<span data-ttu-id="82131-126">La même chaîne qui a été passée dans le paramètre **ViewMode** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="82131-126">The same string that was passed in the **ViewMode** parameter of **changeViewOnlineList**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82131-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82131-127">Requirements</span></span>



| <span data-ttu-id="82131-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82131-128">Requirement</span></span> | <span data-ttu-id="82131-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="82131-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82131-130">Version</span><span class="sxs-lookup"><span data-stu-id="82131-130">Version</span></span><br/> | <span data-ttu-id="82131-131">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="82131-131">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="82131-132">DLL</span><span class="sxs-lookup"><span data-stu-id="82131-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="82131-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82131-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82131-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82131-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82131-135">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="82131-135">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





