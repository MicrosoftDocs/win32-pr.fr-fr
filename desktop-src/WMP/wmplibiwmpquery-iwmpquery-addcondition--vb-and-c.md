---
title: Méthode IWMPQuery addCondition
description: La méthode addCondition ajoute une condition à la requête composée à l’aide de et de la logique.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- méthode addCondition lecteur Windows Media
- méthode addCondition lecteur Windows Media, interface IWMPQuery
- Interface IWMPQuery lecteur Windows Media, méthode addCondition
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525546"
---
# <a name="iwmpqueryaddcondition-method"></a><span data-ttu-id="8028c-106">IWMPQuery :: addCondition, méthode</span><span class="sxs-lookup"><span data-stu-id="8028c-106">IWMPQuery::addCondition method</span></span>

<span data-ttu-id="8028c-107">La méthode **addCondition** ajoute une condition à la requête composée à l’aide **de et** de la logique.</span><span class="sxs-lookup"><span data-stu-id="8028c-107">The **addCondition** method adds a condition to the compound query using **AND** logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="8028c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8028c-108">Syntax</span></span>


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a><span data-ttu-id="8028c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8028c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8028c-110">*bstrAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8028c-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8028c-111">**System. String** qui est le nom de l’attribut à ajouter à la requête.</span><span class="sxs-lookup"><span data-stu-id="8028c-111">A **System.String** that is the name of the attribute to be added to the query.</span></span>

</dd> <dt>

<span data-ttu-id="8028c-112">*bstrOperator* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8028c-112">*bstrOperator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8028c-113">**System. String** qui est l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="8028c-113">A **System.String** that is the operator.</span></span> <span data-ttu-id="8028c-114">Consultez la section Notes pour connaître les valeurs prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8028c-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="8028c-115">*bstrValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8028c-115">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8028c-116">**System. String** qui est la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="8028c-116">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8028c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8028c-117">Return value</span></span>

<span data-ttu-id="8028c-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8028c-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8028c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8028c-119">Remarks</span></span>

<span data-ttu-id="8028c-120">Les conditions contenues dans une requête composée sont organisées en groupes de conditions.</span><span class="sxs-lookup"><span data-stu-id="8028c-120">Conditions contained in a compound query are organized into condition groups.</span></span> <span data-ttu-id="8028c-121">Plusieurs conditions au sein d’un groupe de conditions sont toujours concaténées à l’aide de la logique **et** .</span><span class="sxs-lookup"><span data-stu-id="8028c-121">Multiple conditions within a condition group are always concatenated by using **AND** logic.</span></span> <span data-ttu-id="8028c-122">Les groupes de conditions sont toujours concaténés les uns aux autres à l’aide de **ou** logique.</span><span class="sxs-lookup"><span data-stu-id="8028c-122">Condition groups are always concatenated to each other by using **OR** logic.</span></span> <span data-ttu-id="8028c-123">Pour démarrer un nouveau groupe de conditions, appelez [IWMPQuery. beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="8028c-123">To start a new condition group, call [IWMPQuery.beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span></span>

<span data-ttu-id="8028c-124">Les requêtes composées utilisant **IWMPQuery** ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="8028c-124">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="8028c-125">Une liste de valeurs pour le paramètre *bstrAttribute* se trouve dans la [référence d’attribut alphabétique](alphabetical-attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8028c-125">A list of values for the *bstrAttribute* parameter can be found in [Alphabetical Attribute Reference](alphabetical-attribute-reference.md).</span></span>

<span data-ttu-id="8028c-126">Le tableau suivant répertorie les valeurs prises en charge pour *bstrOperator*.</span><span class="sxs-lookup"><span data-stu-id="8028c-126">The following table lists the supported values for *bstrOperator*.</span></span>



| <span data-ttu-id="8028c-127">String</span><span class="sxs-lookup"><span data-stu-id="8028c-127">String</span></span>              | <span data-ttu-id="8028c-128">S’applique à</span><span class="sxs-lookup"><span data-stu-id="8028c-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="8028c-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="8028c-129">BeginsWith</span></span>          | <span data-ttu-id="8028c-130">Chaînes</span><span class="sxs-lookup"><span data-stu-id="8028c-130">Strings</span></span>        |
| <span data-ttu-id="8028c-131">Contient</span><span class="sxs-lookup"><span data-stu-id="8028c-131">Contains</span></span>            | <span data-ttu-id="8028c-132">Chaînes</span><span class="sxs-lookup"><span data-stu-id="8028c-132">Strings</span></span>        |
| <span data-ttu-id="8028c-133">Égal à</span><span class="sxs-lookup"><span data-stu-id="8028c-133">Equals</span></span>              | <span data-ttu-id="8028c-134">Tous les types</span><span class="sxs-lookup"><span data-stu-id="8028c-134">All types</span></span>      |
| <span data-ttu-id="8028c-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="8028c-135">GreaterThan</span></span>         | <span data-ttu-id="8028c-136">Nombres, dates</span><span class="sxs-lookup"><span data-stu-id="8028c-136">Numbers, Dates</span></span> |
| <span data-ttu-id="8028c-137">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="8028c-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="8028c-138">Nombres, dates</span><span class="sxs-lookup"><span data-stu-id="8028c-138">Numbers, Dates</span></span> |
| <span data-ttu-id="8028c-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="8028c-139">LessThan</span></span>            | <span data-ttu-id="8028c-140">Nombres, dates</span><span class="sxs-lookup"><span data-stu-id="8028c-140">Numbers, Dates</span></span> |
| <span data-ttu-id="8028c-141">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="8028c-141">LessThanOrEquals</span></span>    | <span data-ttu-id="8028c-142">Nombres, dates</span><span class="sxs-lookup"><span data-stu-id="8028c-142">Numbers, Dates</span></span> |
| <span data-ttu-id="8028c-143">NotBeginsWith</span><span class="sxs-lookup"><span data-stu-id="8028c-143">NotBeginsWith</span></span>       | <span data-ttu-id="8028c-144">Chaînes</span><span class="sxs-lookup"><span data-stu-id="8028c-144">Strings</span></span>        |
| <span data-ttu-id="8028c-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="8028c-145">NotContains</span></span>         | <span data-ttu-id="8028c-146">Chaînes</span><span class="sxs-lookup"><span data-stu-id="8028c-146">Strings</span></span>        |
| <span data-ttu-id="8028c-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="8028c-147">NotEquals</span></span>           | <span data-ttu-id="8028c-148">Tous les types</span><span class="sxs-lookup"><span data-stu-id="8028c-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="8028c-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="8028c-149">Examples</span></span>

<span data-ttu-id="8028c-150">L’exemple suivant crée une requête, y ajoute deux conditions et utilise cette requête pour extraire les résultats de la requête sous la forme d’une collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="8028c-150">The following example creates a query, adds two conditions to it, and uses that query to extract the results of the query as a string collection.</span></span> <span data-ttu-id="8028c-151">Les résultats sont ensuite affichés dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="8028c-151">The results are then displayed in a list box.</span></span> <span data-ttu-id="8028c-152">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="8028c-152">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="8028c-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8028c-153">Requirements</span></span>



| <span data-ttu-id="8028c-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8028c-154">Requirement</span></span> | <span data-ttu-id="8028c-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="8028c-155">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8028c-156">Version</span><span class="sxs-lookup"><span data-stu-id="8028c-156">Version</span></span><br/>   | <span data-ttu-id="8028c-157">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="8028c-157">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="8028c-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8028c-158">Namespace</span></span><br/> | <span data-ttu-id="8028c-159">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8028c-159">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8028c-160">Assembly</span><span class="sxs-lookup"><span data-stu-id="8028c-160">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8028c-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8028c-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8028c-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8028c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8028c-163">**Référence d’attribut alphabétique**</span><span class="sxs-lookup"><span data-stu-id="8028c-163">**Alphabetical Attribute Reference**</span></span>](alphabetical-attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="8028c-164">**IWMPMediaCollection2. createQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8028c-164">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8028c-165">**IWMPMediaCollection2. getPlaylistByQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8028c-165">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8028c-166">**IWMPMediaCollection2. getStringCollectionByQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8028c-166">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8028c-167">**Interface IWMPQuery**</span><span class="sxs-lookup"><span data-stu-id="8028c-167">**IWMPQuery Interface**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





