---
title: Query. addCondition, méthode
description: La méthode addCondition ajoute une condition à l’objet de requête à l’aide de et de la logique.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- méthode addCondition lecteur Windows Media
- méthode addCondition lecteur Windows Media, classe Query
- Classe de requête lecteur Windows Media, méthode addCondition
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540216"
---
# <a name="queryaddcondition-method"></a><span data-ttu-id="727a2-106">Query. addCondition, méthode</span><span class="sxs-lookup"><span data-stu-id="727a2-106">Query.addCondition method</span></span>

<span data-ttu-id="727a2-107">La méthode **addCondition** ajoute une condition à l’objet de **requête** à l’aide de et de la logique.</span><span class="sxs-lookup"><span data-stu-id="727a2-107">The **addCondition** method adds a condition to the **Query** object using AND logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="727a2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="727a2-108">Syntax</span></span>


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="727a2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="727a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="727a2-110">*attribut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="727a2-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="727a2-111">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="727a2-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="727a2-112">*opérateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="727a2-112">*operator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="727a2-113">**Chaîne** contenant l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="727a2-113">**String** containing the operator.</span></span> <span data-ttu-id="727a2-114">Consultez la section Notes pour connaître les valeurs prises en charge.</span><span class="sxs-lookup"><span data-stu-id="727a2-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="727a2-115">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="727a2-115">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="727a2-116">**Chaîne** contenant la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="727a2-116">**String** containing the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="727a2-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="727a2-117">Return value</span></span>

<span data-ttu-id="727a2-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="727a2-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="727a2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="727a2-119">Remarks</span></span>

<span data-ttu-id="727a2-120">Les requêtes composées à l’aide de la **requête** ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="727a2-120">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="727a2-121">Vous trouverez une liste de valeurs pour le paramètre *attribut* dans la section [référence des attributs alphabétiques](alphabetical-attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="727a2-121">A list of values for the *attribute* parameter can be found in the [Alphabetical Attribute Reference](alphabetical-attribute-reference.md) section.</span></span>

<span data-ttu-id="727a2-122">Les conditions contenues dans un objet de **requête** sont organisées en groupes de conditions.</span><span class="sxs-lookup"><span data-stu-id="727a2-122">Conditions contained in a **Query** object are organized into condition groups.</span></span> <span data-ttu-id="727a2-123">Plusieurs conditions au sein d’un groupe de conditions sont toujours concaténées à l’aide de et de la logique.</span><span class="sxs-lookup"><span data-stu-id="727a2-123">Multiple conditions within a condition group are always concatenated using AND logic.</span></span> <span data-ttu-id="727a2-124">Les groupes de conditions sont toujours concaténés entre eux à l’aide de ou logique.</span><span class="sxs-lookup"><span data-stu-id="727a2-124">Condition groups are always concatenated to each other using OR logic.</span></span> <span data-ttu-id="727a2-125">Pour démarrer un nouveau groupe de conditions, appelez **query. beginNextGroup**.</span><span class="sxs-lookup"><span data-stu-id="727a2-125">To start a new condition group, call **Query.beginNextGroup**.</span></span>

<span data-ttu-id="727a2-126">Le tableau suivant répertorie les valeurs prises en charge pour l' *opérateur*.</span><span class="sxs-lookup"><span data-stu-id="727a2-126">The following table lists the supported values for *operator*.</span></span>



| <span data-ttu-id="727a2-127">Opérateur</span><span class="sxs-lookup"><span data-stu-id="727a2-127">Operator</span></span>            | <span data-ttu-id="727a2-128">S’applique à</span><span class="sxs-lookup"><span data-stu-id="727a2-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="727a2-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="727a2-129">BeginsWith</span></span>          | <span data-ttu-id="727a2-130">Chaînes</span><span class="sxs-lookup"><span data-stu-id="727a2-130">Strings</span></span>        |
| <span data-ttu-id="727a2-131">Contient</span><span class="sxs-lookup"><span data-stu-id="727a2-131">Contains</span></span>            | <span data-ttu-id="727a2-132">Chaînes</span><span class="sxs-lookup"><span data-stu-id="727a2-132">Strings</span></span>        |
| <span data-ttu-id="727a2-133">Égal à</span><span class="sxs-lookup"><span data-stu-id="727a2-133">Equals</span></span>              | <span data-ttu-id="727a2-134">Tous les types</span><span class="sxs-lookup"><span data-stu-id="727a2-134">All types</span></span>      |
| <span data-ttu-id="727a2-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="727a2-135">GreaterThan</span></span>         | <span data-ttu-id="727a2-136">Nombres, dates</span><span class="sxs-lookup"><span data-stu-id="727a2-136">Numbers, Dates</span></span> |
| <span data-ttu-id="727a2-137">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="727a2-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="727a2-138">Nombres, dates</span><span class="sxs-lookup"><span data-stu-id="727a2-138">Numbers, Dates</span></span> |
| <span data-ttu-id="727a2-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="727a2-139">LessThan</span></span>            | <span data-ttu-id="727a2-140">Nombres, dates</span><span class="sxs-lookup"><span data-stu-id="727a2-140">Numbers, Dates</span></span> |
| <span data-ttu-id="727a2-141">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="727a2-141">LessThanOrEquals</span></span>    | <span data-ttu-id="727a2-142">Nombres, dates</span><span class="sxs-lookup"><span data-stu-id="727a2-142">Numbers, Dates</span></span> |
| <span data-ttu-id="727a2-143">NotBeginsWith</span><span class="sxs-lookup"><span data-stu-id="727a2-143">NotBeginsWith</span></span>       | <span data-ttu-id="727a2-144">Chaînes</span><span class="sxs-lookup"><span data-stu-id="727a2-144">Strings</span></span>        |
| <span data-ttu-id="727a2-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="727a2-145">NotContains</span></span>         | <span data-ttu-id="727a2-146">Chaînes</span><span class="sxs-lookup"><span data-stu-id="727a2-146">Strings</span></span>        |
| <span data-ttu-id="727a2-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="727a2-147">NotEquals</span></span>           | <span data-ttu-id="727a2-148">Tous les types</span><span class="sxs-lookup"><span data-stu-id="727a2-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="727a2-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="727a2-149">Examples</span></span>

<span data-ttu-id="727a2-150">L’exemple JScript suivant utilise **query. addCondition** et **query. beginNextGroup** pour exécuter un exemple de requête.</span><span class="sxs-lookup"><span data-stu-id="727a2-150">The following JScript example uses **Query.addCondition** and **Query.beginNextGroup** to perform an example query.</span></span>


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a><span data-ttu-id="727a2-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="727a2-151">Requirements</span></span>



| <span data-ttu-id="727a2-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="727a2-152">Requirement</span></span> | <span data-ttu-id="727a2-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="727a2-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="727a2-154">Version</span><span class="sxs-lookup"><span data-stu-id="727a2-154">Version</span></span><br/> | <span data-ttu-id="727a2-155">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="727a2-155">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="727a2-156">DLL</span><span class="sxs-lookup"><span data-stu-id="727a2-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="727a2-157"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="727a2-157"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="727a2-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="727a2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="727a2-159">**MediaCollection. createQuery**</span><span class="sxs-lookup"><span data-stu-id="727a2-159">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="727a2-160">**MediaCollection.getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="727a2-160">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="727a2-161">**MediaCollection.getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="727a2-161">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="727a2-162">**Objet Query**</span><span class="sxs-lookup"><span data-stu-id="727a2-162">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="727a2-163">**Query. beginNextGroup**</span><span class="sxs-lookup"><span data-stu-id="727a2-163">**Query.beginNextGroup**</span></span>](query-beginnextgroup.md)
</dt> </dl>

 

 





