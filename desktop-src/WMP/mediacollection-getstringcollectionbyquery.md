---
title: Méthode MediaCollection. getStringCollectionByQuery
description: La méthode getStringCollectionByQuery récupère un objet StringCollection contenant toutes les chaînes qui correspondent aux conditions de la requête.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- méthode getStringCollectionByQuery lecteur Windows Media
- méthode getStringCollectionByQuery lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getStringCollectionByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545437"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a><span data-ttu-id="ee069-106">Méthode MediaCollection. getStringCollectionByQuery</span><span class="sxs-lookup"><span data-stu-id="ee069-106">MediaCollection.getStringCollectionByQuery method</span></span>

<span data-ttu-id="ee069-107">La méthode **getStringCollectionByQuery** récupère un objet **StringCollection** contenant toutes les chaînes qui correspondent aux conditions de la requête.</span><span class="sxs-lookup"><span data-stu-id="ee069-107">The **getStringCollectionByQuery** method retrieves a **StringCollection** object containing all strings that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee069-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee069-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="ee069-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee069-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee069-110">*attribut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee069-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee069-111">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="ee069-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="ee069-112">*requête* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee069-112">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee069-113">Objet de **requête** .</span><span class="sxs-lookup"><span data-stu-id="ee069-113">**Query** object.</span></span>

</dd> <dt>

<span data-ttu-id="ee069-114">*MediaType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee069-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee069-115">**Chaîne** contenant le type de média.</span><span class="sxs-lookup"><span data-stu-id="ee069-115">**String** containing the media type.</span></span> <span data-ttu-id="ee069-116">Doit contenir l’une des valeurs suivantes : « audio », « Video », « photo », « playlist » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="ee069-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="ee069-117">*sortAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee069-117">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee069-118">**Chaîne** contenant le nom d’attribut utilisé pour le tri.</span><span class="sxs-lookup"><span data-stu-id="ee069-118">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="ee069-119">Une chaîne vide ("") signifie qu’aucun tri n’est appliqué.</span><span class="sxs-lookup"><span data-stu-id="ee069-119">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="ee069-120">*sortAscending* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee069-120">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee069-121">**Boolean**, true indiquant que **StringCollection** doit être trié dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="ee069-121">**Boolean**, true indicating that the **StringCollection** must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee069-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee069-122">Return value</span></span>

<span data-ttu-id="ee069-123">Cette méthode retourne un objet **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="ee069-123">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee069-124">Notes</span><span class="sxs-lookup"><span data-stu-id="ee069-124">Remarks</span></span>

<span data-ttu-id="ee069-125">Les requêtes composées à l’aide de la **requête** ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="ee069-125">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="ee069-126">Lorsque la requête composée spécifiée par le paramètre de *requête* contient une condition construite sur l’attribut **MediaType** , cette condition est ignorée.</span><span class="sxs-lookup"><span data-stu-id="ee069-126">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="ee069-127">La valeur du paramètre *MediaType* est toujours utilisée.</span><span class="sxs-lookup"><span data-stu-id="ee069-127">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="ee069-128">Par exemple, si la requête composée contient la condition « MediaType est égal à audio » et que la valeur du paramètre *MediaType* est « Video », la sélection résultante contient uniquement les éléments vidéo.</span><span class="sxs-lookup"><span data-stu-id="ee069-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee069-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee069-129">Requirements</span></span>



| <span data-ttu-id="ee069-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee069-130">Requirement</span></span> | <span data-ttu-id="ee069-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee069-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee069-132">Version</span><span class="sxs-lookup"><span data-stu-id="ee069-132">Version</span></span><br/> | <span data-ttu-id="ee069-133">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="ee069-133">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="ee069-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ee069-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="ee069-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee069-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee069-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee069-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee069-137">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="ee069-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="ee069-138">**MediaType (attribut)**</span><span class="sxs-lookup"><span data-stu-id="ee069-138">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="ee069-139">**Objet Query**</span><span class="sxs-lookup"><span data-stu-id="ee069-139">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





