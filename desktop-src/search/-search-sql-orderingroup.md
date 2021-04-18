---
description: La clause ORDER IN GROUP est utilisée conjointement avec l’instruction GROUP ON, qui retourne des jeux de résultats dans des groupes.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: COMMANDE dans la clause GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318157"
---
# <a name="order-in-group-clause"></a><span data-ttu-id="f005d-103">COMMANDE dans la clause GROUP</span><span class="sxs-lookup"><span data-stu-id="f005d-103">ORDER IN GROUP Clause</span></span>

<span data-ttu-id="f005d-104">La clause ORDER IN GROUP est utilisée conjointement avec l’instruction [Group on](-search-sql-group-on-over.md) , qui retourne des jeux de résultats dans des groupes.</span><span class="sxs-lookup"><span data-stu-id="f005d-104">The ORDER IN GROUP clause is used in conjunction with the [GROUP ON](-search-sql-group-on-over.md) statement, which returns result sets in groups.</span></span> <span data-ttu-id="f005d-105">La clause ORDER IN GROUP vous permet de trier chaque groupe retourné d’une manière différente.</span><span class="sxs-lookup"><span data-stu-id="f005d-105">The ORDER IN GROUP clause enables you to sort each returned group in a different way.</span></span> <span data-ttu-id="f005d-106">Si vous regroupez sur System. genre, par exemple, vous pouvez trier tous les documents en System.Document. LastAuthor, tous les fichiers musicaux par System. Music. AlbumArtist et tous les messages électroniques par System. message. FromName.</span><span class="sxs-lookup"><span data-stu-id="f005d-106">If you group on System.Kind, for example, you can then sort all documents by System.Document.LastAuthor, all music files by System.Music.AlbumArtist, and all emails by System.Message.FromName.</span></span>

## <a name="syntax"></a><span data-ttu-id="f005d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f005d-107">Syntax</span></span>

<span data-ttu-id="f005d-108">Voici la syntaxe de la clause ORDER dans le groupe :</span><span class="sxs-lookup"><span data-stu-id="f005d-108">The following is the syntax of the ORDER IN GROUP clause:</span></span>


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



<span data-ttu-id="f005d-109">Le spécificateur de nom de groupe est une plage ou une valeur connue de la colonne de groupe, comme spécifié dans l’instruction GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="f005d-109">The group name specifier is a range or known value from the group column, as specified in the GROUP ON statement.</span></span> <span data-ttu-id="f005d-110">Par exemple, les valeurs connues pour System. photo. ISOSpeed incluent « ISO-100 », « ISO-200 », et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="f005d-110">For example, known values for System.Photo.ISOSpeed would include 'ISO-100', 'ISO-200', and so on.</span></span> <span data-ttu-id="f005d-111">Une plage pour System. photo. DateTaken inclut « 2006-1-1 » et « 2007-1-1 » pour une instruction comme GROUP sur System. ItemDate \[ « 2006-1-1 », « 2007-1-1 » \] .</span><span class="sxs-lookup"><span data-stu-id="f005d-111">A range for System.Photo.DateTaken would include '2006-1-1' and '2007-1-1' for a statement like GROUP ON System.ItemDate \['2006-1-1', '2007-1-1'\].</span></span>

<span data-ttu-id="f005d-112">Le spécificateur de colonne doit être une colonne valide spécifiée dans l’instruction GROUP ON ou SELECT.</span><span class="sxs-lookup"><span data-stu-id="f005d-112">The column specifier must be a valid column specified in either the GROUP ON or the SELECT statement.</span></span> <span data-ttu-id="f005d-113">Vous pouvez inclure plusieurs colonnes, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="f005d-113">You can include more than one column, separated by commas.</span></span> <span data-ttu-id="f005d-114">Par exemple, si vous regroupez sur System. photo. ISOSpeed, vous pouvez trier toutes les photos ISO-100, d’abord par System. photo. ShutterSpeed, puis par System. photo. ouverture.</span><span class="sxs-lookup"><span data-stu-id="f005d-114">For example, if you group on System.Photo.ISOSpeed, you can sort all ISO-100 photos, first by System.Photo.ShutterSpeed, and then by System.Photo.Aperture.</span></span>

<span data-ttu-id="f005d-115">Le spécificateur de direction facultatif peut être ASC pour l’ordre croissant (de faible à élevé) ou DESC pour l’ordre décroissant (de haut en bas).</span><span class="sxs-lookup"><span data-stu-id="f005d-115">The optional direction specifier can be either ASC for ascending (low to high) or DESC for descending (high to low).</span></span> <span data-ttu-id="f005d-116">Si vous ne fournissez pas de spécificateur de direction, la valeur par défaut, par ordre croissant, est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f005d-116">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="f005d-117">Si vous spécifiez plusieurs colonnes, mais que vous ne spécifiez pas toutes les directions, la direction que vous spécifiez en dernier est appliquée à chaque colonne consécutive jusqu’à ce que vous modifiiez explicitement la direction.</span><span class="sxs-lookup"><span data-stu-id="f005d-117">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each successive column until you explicitly change the direction.</span></span>

<span data-ttu-id="f005d-118">Les plages ou valeurs qui ne sont pas explicitement spécifiées dans une clause ORDER GROUP IN sont triées dans l’ordre croissant en fonction des valeurs de la colonne GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="f005d-118">Ranges or values that are not explicitly specified in an ORDER GROUP IN clause are sorted in ascending order by the values in the GROUP ON column.</span></span>

## <a name="examples"></a><span data-ttu-id="f005d-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="f005d-119">Examples</span></span>

<span data-ttu-id="f005d-120">L’exemple suivant regroupe les résultats par la propriété System. Kind.</span><span class="sxs-lookup"><span data-stu-id="f005d-120">The following example groups results by the System.Kind property.</span></span> <span data-ttu-id="f005d-121">La requête commanderait le groupe « Program » par le nom de l’application et le groupe « Music » par titre d’album et par numéro de suivi.</span><span class="sxs-lookup"><span data-stu-id="f005d-121">The query would order the 'program' group by the application name and the 'music' group by album title and track number.</span></span> <span data-ttu-id="f005d-122">Le groupe **null** serait classé par le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f005d-122">The **NULL** group would be ordered by the item name.</span></span> <span data-ttu-id="f005d-123">Tous les autres groupes seraient triés par date d’élément.</span><span class="sxs-lookup"><span data-stu-id="f005d-123">All other groups would by ordered by the item date.</span></span>


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



<span data-ttu-id="f005d-124">L’exemple suivant regroupe les résultats par la propriété System. ItemDate, puis trie chaque URL de groupe par élément, type ou nom.</span><span class="sxs-lookup"><span data-stu-id="f005d-124">The following example groups results by the System.ItemDate property, and then sorts each group by item URL, kind, or name.</span></span>


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



<span data-ttu-id="f005d-125">Les résultats de la requête précédente sont retournés dans cinq groupes et triés comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f005d-125">The results of the preceding query would be returned in five groups and sorted as described in the following table.</span></span>



| <span data-ttu-id="f005d-126">Groupe</span><span class="sxs-lookup"><span data-stu-id="f005d-126">Group</span></span>    | <span data-ttu-id="f005d-127">Description</span><span class="sxs-lookup"><span data-stu-id="f005d-127">Description</span></span>                                               | <span data-ttu-id="f005d-128">Trié par</span><span class="sxs-lookup"><span data-stu-id="f005d-128">Sorted by</span></span>                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="f005d-129">MINVALUE</span><span class="sxs-lookup"><span data-stu-id="f005d-129">MINVALUE</span></span> | <span data-ttu-id="f005d-130">Éléments dont la date est antérieure à 2006-1-1</span><span class="sxs-lookup"><span data-stu-id="f005d-130">Items with dates before 2006-1-1</span></span>                          | <span data-ttu-id="f005d-131">Trié par l’URL de l’élément, dans l’ordre croissant</span><span class="sxs-lookup"><span data-stu-id="f005d-131">Sorted by the item's URL, in ascending order</span></span> |
| <span data-ttu-id="f005d-132">2006-1-1</span><span class="sxs-lookup"><span data-stu-id="f005d-132">2006-1-1</span></span> | <span data-ttu-id="f005d-133">Éléments dont la date est le ou après le 2006-1-1 mais avant 2007-1-1</span><span class="sxs-lookup"><span data-stu-id="f005d-133">Items with dates on or after 2006-1-1 but before 2007-1-1</span></span> | <span data-ttu-id="f005d-134">Trié par date de l’élément, dans l’ordre croissant</span><span class="sxs-lookup"><span data-stu-id="f005d-134">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="f005d-135">2007-1-1</span><span class="sxs-lookup"><span data-stu-id="f005d-135">2007-1-1</span></span> | <span data-ttu-id="f005d-136">Éléments dont la date est le ou après le 2007-1-1 mais avant 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="f005d-136">Items with dates on or after 2007-1-1 but before 2008-1-1</span></span> | <span data-ttu-id="f005d-137">Trié par valeur de genre, dans l’ordre croissant</span><span class="sxs-lookup"><span data-stu-id="f005d-137">Sorted by kind value, in ascending order</span></span>     |
| <span data-ttu-id="f005d-138">2008-1-1</span><span class="sxs-lookup"><span data-stu-id="f005d-138">2008-1-1</span></span> | <span data-ttu-id="f005d-139">Éléments dont la date est le ou après le 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="f005d-139">Items with dates on or after 2008-1-1</span></span>                     | <span data-ttu-id="f005d-140">Trié par date de l’élément, dans l’ordre croissant</span><span class="sxs-lookup"><span data-stu-id="f005d-140">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="f005d-141">**NULL**</span><span class="sxs-lookup"><span data-stu-id="f005d-141">**NULL**</span></span> | <span data-ttu-id="f005d-142">Éléments sans valeur dans la colonne System. ItemDate</span><span class="sxs-lookup"><span data-stu-id="f005d-142">Items with no value in the System.ItemDate column</span></span>         | <span data-ttu-id="f005d-143">Trié par nom d’élément, dans l’ordre croissant</span><span class="sxs-lookup"><span data-stu-id="f005d-143">Sorted by item name, in ascending order</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="f005d-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f005d-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f005d-145">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="f005d-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f005d-146">REGROUPER... ... Gestion</span><span class="sxs-lookup"><span data-stu-id="f005d-146">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
</dt> <dt>

[<span data-ttu-id="f005d-147">Clause ORDER BY</span><span class="sxs-lookup"><span data-stu-id="f005d-147">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> </dl>

 

 



