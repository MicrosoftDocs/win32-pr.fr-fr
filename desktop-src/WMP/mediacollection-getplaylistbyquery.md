---
title: Méthode MediaCollection. getPlaylistByQuery
description: La méthode getPlaylistByQuery récupère un objet de sélection contenant des objets multimédias qui correspondent aux conditions de requête.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- méthode getPlaylistByQuery lecteur Windows Media
- méthode getPlaylistByQuery lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getPlaylistByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537466"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a><span data-ttu-id="6ad48-106">Méthode MediaCollection. getPlaylistByQuery</span><span class="sxs-lookup"><span data-stu-id="6ad48-106">MediaCollection.getPlaylistByQuery method</span></span>

<span data-ttu-id="6ad48-107">La méthode **getPlaylistByQuery** récupère un objet de **sélection** contenant des objets **multimédias** qui correspondent aux conditions de requête.</span><span class="sxs-lookup"><span data-stu-id="6ad48-107">The **getPlaylistByQuery** method retrieves a **Playlist** object containing **Media** objects that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad48-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ad48-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="6ad48-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ad48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ad48-110">*requête* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ad48-110">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad48-111">Objet de **requête** qui définit les conditions utilisées pour créer la sélection.</span><span class="sxs-lookup"><span data-stu-id="6ad48-111">**Query** object that defines the conditions used to create the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="6ad48-112">*MediaType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ad48-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad48-113">**Chaîne** contenant le type de média.</span><span class="sxs-lookup"><span data-stu-id="6ad48-113">**String** containing the media type.</span></span> <span data-ttu-id="6ad48-114">Doit contenir l’une des valeurs suivantes : « audio », « Video », « photo », « playlist » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="6ad48-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="6ad48-115">*sortAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ad48-115">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad48-116">**Chaîne** contenant le nom d’attribut utilisé pour le tri.</span><span class="sxs-lookup"><span data-stu-id="6ad48-116">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="6ad48-117">Une chaîne vide ("") signifie qu’aucun tri n’est appliqué.</span><span class="sxs-lookup"><span data-stu-id="6ad48-117">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="6ad48-118">*sortAscending* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ad48-118">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad48-119">Valeur **booléenne** qui indique que la sélection doit être triée dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="6ad48-119">**Boolean**, true indicating that the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ad48-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ad48-120">Return value</span></span>

<span data-ttu-id="6ad48-121">Cette méthode retourne un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="6ad48-121">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ad48-122">Notes</span><span class="sxs-lookup"><span data-stu-id="6ad48-122">Remarks</span></span>

<span data-ttu-id="6ad48-123">Les requêtes composées à l’aide de la **requête** ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="6ad48-123">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="6ad48-124">Lorsque la requête composée spécifiée par le paramètre de *requête* contient une condition construite sur l’attribut **MediaType** , cette condition est ignorée.</span><span class="sxs-lookup"><span data-stu-id="6ad48-124">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="6ad48-125">La valeur du paramètre *MediaType* est toujours utilisée.</span><span class="sxs-lookup"><span data-stu-id="6ad48-125">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="6ad48-126">Par exemple, si la requête composée contient la condition « MediaType est égal à audio » et que la valeur du paramètre *MediaType* est « Video », la sélection résultante contient uniquement les éléments vidéo.</span><span class="sxs-lookup"><span data-stu-id="6ad48-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad48-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ad48-127">Requirements</span></span>



| <span data-ttu-id="6ad48-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ad48-128">Requirement</span></span> | <span data-ttu-id="6ad48-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ad48-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad48-130">Version</span><span class="sxs-lookup"><span data-stu-id="6ad48-130">Version</span></span><br/> | <span data-ttu-id="6ad48-131">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="6ad48-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="6ad48-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6ad48-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="6ad48-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ad48-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ad48-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ad48-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad48-135">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="6ad48-135">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="6ad48-136">**MediaType (attribut)**</span><span class="sxs-lookup"><span data-stu-id="6ad48-136">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="6ad48-137">**Objet Query**</span><span class="sxs-lookup"><span data-stu-id="6ad48-137">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





