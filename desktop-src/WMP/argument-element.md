---
title: argument, élément
description: L’élément argument contient une partie d’une chaîne de condition.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Élément argument Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528770"
---
# <a name="argument-element"></a><span data-ttu-id="0b368-104">argument, élément</span><span class="sxs-lookup"><span data-stu-id="0b368-104">argument Element</span></span>

<span data-ttu-id="0b368-105">L’élément **argument** contient une partie d’une chaîne de condition.</span><span class="sxs-lookup"><span data-stu-id="0b368-105">The **argument** element contains one portion of a condition string.</span></span> <span data-ttu-id="0b368-106">Une chaîne de condition comporte généralement une partie condition et une partie valeur.</span><span class="sxs-lookup"><span data-stu-id="0b368-106">A condition string typically has a condition portion and a value portion.</span></span> <span data-ttu-id="0b368-107">Par exemple, dans la chaîne de condition « artiste est égal à Joe », la partie condition est « égal à » et la partie valeur est « Joe ».</span><span class="sxs-lookup"><span data-stu-id="0b368-107">For example, in the condition string "Artist Equals Joe", the condition portion is "Equals" and the value portion is "Joe".</span></span>

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a><span data-ttu-id="0b368-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="0b368-108">Attributes</span></span>

<span data-ttu-id="0b368-109">**nom** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="0b368-109">**name** (required)</span></span>

<span data-ttu-id="0b368-110">Nom d’une partie de la chaîne de condition.</span><span class="sxs-lookup"><span data-stu-id="0b368-110">The name of one portion of the condition string.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="0b368-111">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="0b368-111">Parent/Child Elements</span></span>



| <span data-ttu-id="0b368-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="0b368-112">Hierarchy</span></span> | <span data-ttu-id="0b368-113">Éléments</span><span class="sxs-lookup"><span data-stu-id="0b368-113">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="0b368-114">Parent</span><span class="sxs-lookup"><span data-stu-id="0b368-114">Parent</span></span>    | [<span data-ttu-id="0b368-115">échantillon</span><span class="sxs-lookup"><span data-stu-id="0b368-115">fragment</span></span>](fragment-element.md) |
| <span data-ttu-id="0b368-116">Enfant</span><span class="sxs-lookup"><span data-stu-id="0b368-116">Child</span></span>     | <span data-ttu-id="0b368-117">Aucune</span><span class="sxs-lookup"><span data-stu-id="0b368-117">None</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="0b368-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0b368-118">Remarks</span></span>

<span data-ttu-id="0b368-119">Lorsque l’attribut **Name** d’un élément **fragment** est une caractéristique d’élément multimédia telle que l’artiste de l’album ou le genre, l’élément **fragment** doit contenir deux éléments **argument** : un qui spécifie une condition et un autre qui spécifie une valeur.</span><span class="sxs-lookup"><span data-stu-id="0b368-119">When the **name** attribute of a **fragment** element is a media item characteristic such as Album Artist, or Genre, the **fragment** element must contain two **argument** elements: one that specifies a condition and another that specifies a value.</span></span> <span data-ttu-id="0b368-120">Le tableau suivant présente deux valeurs possibles pour l’attribut **Name** et la façon dont les éléments **argument** sont utilisés pour spécifier des conditions et des valeurs.</span><span class="sxs-lookup"><span data-stu-id="0b368-120">The following table shows two possible values for the **name** attribute and how **argument** elements are used to specify conditions and values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b368-121">Valeur d'attribut</span><span class="sxs-lookup"><span data-stu-id="0b368-121">Attribute value</span></span></th>
<th><span data-ttu-id="0b368-122">Description</span><span class="sxs-lookup"><span data-stu-id="0b368-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b368-123">Condition</span><span class="sxs-lookup"><span data-stu-id="0b368-123">Condition</span></span></td>
<td><span data-ttu-id="0b368-124">Le contenu de l’élément <strong>argument</strong> est la partie condition d’une chaîne de condition.</span><span class="sxs-lookup"><span data-stu-id="0b368-124">The content of the <strong>argument</strong> element is the condition portion of a condition string.</span></span> <span data-ttu-id="0b368-125">Par exemple, dans la condition la chaîne &quot; Artist est égale à Jean &quot; , la partie condition est &quot; égale à &quot; .</span><span class="sxs-lookup"><span data-stu-id="0b368-125">For example, in the condition string &quot;Artist Equals Joe&quot;, the condition portion is &quot;Equals&quot;.</span></span> <span data-ttu-id="0b368-126">La partie de condition d’une chaîne de condition doit être l’une des suivantes : Equals, n’est pas égal à, contient, ne contient pas, est inférieur à, est supérieur à, est, n’est pas, est antérieur à, est plus récent que, plus récent, en dessous, croissant, décroissant, aléatoire, est au moins égal à.</span><span class="sxs-lookup"><span data-stu-id="0b368-126">The condition portion of a condition string must be one of the following: Equals, Does Not Equal, Contains, Does Not Contain, Is Less Than, Is Greater Than, Is, Is Not, Is Before, Is Later Than, Is More Recent Than, Above, Below, Ascending, Descending, Random, Is At Least, Is No More Than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b368-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b368-127">Value</span></span></td>
<td><span data-ttu-id="0b368-128">Le contenu de l’élément <strong>argument</strong> est la partie valeur d’une chaîne de condition.</span><span class="sxs-lookup"><span data-stu-id="0b368-128">The content of the <strong>argument</strong> element is the value portion of a condition string.</span></span> <span data-ttu-id="0b368-129">Par exemple, dans la condition chaîne &quot; Artist est égal à Jean &quot; , la partie valeur est &quot; Joe &quot; . Tels</span><span class="sxs-lookup"><span data-stu-id="0b368-129">For example, in the condition string &quot;Artist Equals Joe&quot;, the value portion is &quot;Joe&quot;.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0b368-130">Lorsque l’attribut **Name** d’un élément **fragment** est « limiter la taille totale à » ou « limiter la durée totale à », l’élément **fragment** doit contenir deux éléments **argument** : un qui spécifie un format et un qui spécifie un nombre.</span><span class="sxs-lookup"><span data-stu-id="0b368-130">When the **name** attribute of a **fragment** element is "Limit Total Size To" or "Limit Total Duration To", the **fragment** element must contain two **argument** elements: one that specifies a format and one that specifies a number.</span></span> <span data-ttu-id="0b368-131">Le tableau suivant présente deux valeurs possibles pour l’attribut **Name** et la façon dont les éléments **argument** sont utilisés pour limiter la taille ou la durée d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="0b368-131">The following table shows two possible values for the **name** attribute and how **argument** elements are used to limit the size or duration of a playlist.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b368-132">Valeur d'attribut</span><span class="sxs-lookup"><span data-stu-id="0b368-132">Attribute value</span></span></th>
<th><span data-ttu-id="0b368-133">Description</span><span class="sxs-lookup"><span data-stu-id="0b368-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b368-134">Format</span><span class="sxs-lookup"><span data-stu-id="0b368-134">Format</span></span></td>
<td><span data-ttu-id="0b368-135">Lorsque l’attribut <strong>Name</strong> de l' <strong>élément fragment</strong> est &quot; limiter la taille totale à &quot; , le contenu de l’élément <strong>argument</strong> doit être l’un des suivants : kilo-octets, mégaoctets ou gigaoctets. lorsque l’attribut <strong>Name</strong> de l’élément <strong>fragment</strong> est limiter la &quot; durée totale à &quot; , le contenu de l’élément <strong>argument</strong> doit être l’un des suivants : secondes, minutes, heures ou jours.</span><span class="sxs-lookup"><span data-stu-id="0b368-135">When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Size To&quot;, the content of the <strong>argument</strong> element must be one of the following: Kilobytes, Megabytes, or Gigabytes.When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Duration To&quot;, the content of the <strong>argument</strong> element must be one of the following: Seconds, Minutes, Hours, or Days.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b368-136">Number</span><span class="sxs-lookup"><span data-stu-id="0b368-136">Number</span></span></td>
<td><span data-ttu-id="0b368-137">Le contenu de l’élément <strong>argument</strong> est un nombre qui limite la taille ou la durée de la sélection. Illustre</span><span class="sxs-lookup"><span data-stu-id="0b368-137">The content of the <strong>argument</strong> element is a number that limits the size or duration of the playlist.Examples:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0b368-138">Lorsque l’attribut **Name** d’un élément **fragment** est « Limit Number of items », l’élément **fragment** doit contenir un élément **argument** qui spécifie le nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="0b368-138">When the **name** attribute of a **fragment** element is "Limit Number of Items", the **fragment** element must contain one **argument** element that specifies the number of items.</span></span> <span data-ttu-id="0b368-139">Le tableau suivant indique comment utiliser la valeur numérique de l’attribut **Name** .</span><span class="sxs-lookup"><span data-stu-id="0b368-139">The following table shows how to use the Number value of the **name** attribute.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b368-140">Valeur d'attribut</span><span class="sxs-lookup"><span data-stu-id="0b368-140">Attribute value</span></span></th>
<th><span data-ttu-id="0b368-141">Description</span><span class="sxs-lookup"><span data-stu-id="0b368-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b368-142">Number</span><span class="sxs-lookup"><span data-stu-id="0b368-142">Number</span></span></td>
<td><span data-ttu-id="0b368-143">Le contenu de l’élément <strong>argument</strong> est un nombre qui limite le nombre d’éléments dans une sélection. Tels</span><span class="sxs-lookup"><span data-stu-id="0b368-143">The content of the <strong>argument</strong> element is a number that limits the number of items in a playlist.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="0b368-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b368-144">Requirements</span></span>



| <span data-ttu-id="0b368-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b368-145">Requirement</span></span> | <span data-ttu-id="0b368-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b368-146">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="0b368-147">Version</span><span class="sxs-lookup"><span data-stu-id="0b368-147">Version</span></span><br/> | <span data-ttu-id="0b368-148">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0b368-148">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b368-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b368-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b368-150">**fragment, élément**</span><span class="sxs-lookup"><span data-stu-id="0b368-150">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="0b368-151">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0b368-151">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





