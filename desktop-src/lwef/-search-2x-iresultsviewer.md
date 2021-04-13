---
title: Interface IResultsViewer (WdsSharedIDL. h)
description: Expose les méthodes et les propriétés de la vue résultats.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IResultsViewer
- Fonctionnalités d’environnement Windows héritées de l’interface IResultsViewer, Description
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508806"
---
# <a name="iresultsviewer-interface"></a><span data-ttu-id="b0e3c-105">Interface IResultsViewer</span><span class="sxs-lookup"><span data-stu-id="b0e3c-105">IResultsViewer interface</span></span>

> [!NOTE]
> <span data-ttu-id="b0e3c-106">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b0e3c-107">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e3c-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="b0e3c-108">Expose les méthodes et les propriétés de la vue résultats.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-108">Exposes methods and properties for the results view.</span></span>

## <a name="members"></a><span data-ttu-id="b0e3c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b0e3c-109">Members</span></span>

<span data-ttu-id="b0e3c-110">L’interface **IResultsViewer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b0e3c-110">The **IResultsViewer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b0e3c-111">**IResultsViewer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b0e3c-111">**IResultsViewer** also has these types of members:</span></span>

-   [<span data-ttu-id="b0e3c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b0e3c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b0e3c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b0e3c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b0e3c-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b0e3c-114">Methods</span></span>

<span data-ttu-id="b0e3c-115">L’interface **IResultsViewer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-115">The **IResultsViewer** interface has these methods.</span></span>



| <span data-ttu-id="b0e3c-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="b0e3c-116">Method</span></span>                                                   | <span data-ttu-id="b0e3c-117">Description</span><span class="sxs-lookup"><span data-stu-id="b0e3c-117">Description</span></span>                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0e3c-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-118">**GoBack**</span></span>](-search-2x-iresultsviewer-goback.md)       | <span data-ttu-id="b0e3c-119">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-119">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="b0e3c-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-120">**GoForward**</span></span>](-search-2x-iresultsviewer-goforward.md) | <span data-ttu-id="b0e3c-121">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-121">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="b0e3c-122">**Générer**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-122">**Refresh**</span></span>](-search-2x-iresultsviewer-refresh.md)     | <span data-ttu-id="b0e3c-123">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-123">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="b0e3c-124">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-124">**Stop**</span></span>](-search-2x-iresultsviewer-stop.md)           | <span data-ttu-id="b0e3c-125">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-125">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="b0e3c-126">**Mise à jour**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-126">**Update**</span></span>](-search-2x-iresultsviewer-update.md)       | <span data-ttu-id="b0e3c-127">Applique les modifications de requête et parcourt la vue jusqu’au nouvel ensemble de résultats.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-127">Applies any query changes and navigates the view to the new set of results.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b0e3c-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b0e3c-128">Properties</span></span>

<span data-ttu-id="b0e3c-129">L’interface **IResultsViewer** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-129">The **IResultsViewer** interface has these properties.</span></span>



| <span data-ttu-id="b0e3c-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="b0e3c-130">Property</span></span>                                                                            | <span data-ttu-id="b0e3c-131">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b0e3c-131">Access type</span></span>           | <span data-ttu-id="b0e3c-132">Description</span><span class="sxs-lookup"><span data-stu-id="b0e3c-132">Description</span></span>                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0e3c-133">**Contenu**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-133">**Contents**</span></span>](-search-2x-iresultsviewer-contents.md)<br/>                   | <span data-ttu-id="b0e3c-134">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="b0e3c-134">Write-only</span></span><br/> | <span data-ttu-id="b0e3c-135">Cette propriété effectue le suivi du type de contenu affiché dans l’affichage des résultats.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-135">This property tracks the type of the content being displayed in the results view.</span></span> <br/>    |
| [<span data-ttu-id="b0e3c-136">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-136">**DisplayName**</span></span>](-search-2x-iresultsviewer-displayname.md)<br/>             | <span data-ttu-id="b0e3c-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b0e3c-137">Read-only</span></span><br/>  | <span data-ttu-id="b0e3c-138">Nom complet localisé du type.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-138">Localized display name of the type.</span></span><br/>                                                   |
| [<span data-ttu-id="b0e3c-139">**EnumSelectedItems**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-139">**EnumSelectedItems**</span></span>](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | <span data-ttu-id="b0e3c-140">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="b0e3c-140">Write-only</span></span><br/> | <span data-ttu-id="b0e3c-141">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-141">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="b0e3c-142">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-142">**FilterType**</span></span>](-search-2x-iresultsviewer-filtertype.md)<br/>               | <span data-ttu-id="b0e3c-143">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b0e3c-143">Read/write</span></span><br/> | <span data-ttu-id="b0e3c-144">Cette propriété définit ou retourne le nom du type preceived pour filtrer les résultats par.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-144">This property will set or return the name of the preceived type to filter results by.</span></span><br/> |
| [<span data-ttu-id="b0e3c-145">**HeaderStyle**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-145">**HeaderStyle**</span></span>](-search-2x-iresultsviewer-headerstyle.md)<br/>             | <span data-ttu-id="b0e3c-146">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b0e3c-146">Read/write</span></span><br/> | <span data-ttu-id="b0e3c-147">Style de l’en-tête affiché dans la vue.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-147">The style of header displayed in the view.</span></span><br/>                                            |
| [<span data-ttu-id="b0e3c-148">**IsUpdateNeeded**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-148">**IsUpdateNeeded**</span></span>](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | <span data-ttu-id="b0e3c-149">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="b0e3c-149">Write-only</span></span><br/> | <span data-ttu-id="b0e3c-150">La valeur TRUE est retournée si la requête views a été modifiée et doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-150">This returns TRUE if the views query has been modified and needs updating.</span></span> <br/>           |
| [<span data-ttu-id="b0e3c-151">**ItemStore**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-151">**ItemStore**</span></span>](-search-2x-iresultsviewer-itemstore.md)<br/>                 | <span data-ttu-id="b0e3c-152">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b0e3c-152">Read/write</span></span><br/> | <span data-ttu-id="b0e3c-153">Cette propriété définit ou retourne le nom du magasin sur lequel filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-153">This property will set or return the name of the store to filter results by.</span></span><br/>          |
| [<span data-ttu-id="b0e3c-154">**PreviewStyle**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-154">**PreviewStyle**</span></span>](-search-2x-iresultsviewer-previewstyle.md)<br/>           | <span data-ttu-id="b0e3c-155">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b0e3c-155">Read/write</span></span><br/> | <span data-ttu-id="b0e3c-156">Contrôle le mode d’affichage du volet de visualisation.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-156">Controls the preview pane's display mode.</span></span><br/>                                             |
| [<span data-ttu-id="b0e3c-157">**Le propertyFilters**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-157">**PropertyFilters**</span></span>](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | <span data-ttu-id="b0e3c-158">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="b0e3c-158">Write-only</span></span><br/> | <span data-ttu-id="b0e3c-159">Lors de l’appel de la collection de filtres de propriétés, elle retourne ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b0e3c-159">When calling the property filter collection it will return the following:</span></span><br/>             |
| [<span data-ttu-id="b0e3c-160">**QueryText**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-160">**QueryText**</span></span>](-search-2x-iresultsviewer-querytext.md)<br/>                 | <span data-ttu-id="b0e3c-161">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b0e3c-161">Read/write</span></span><br/> | <span data-ttu-id="b0e3c-162">Obtient ou définit le texte de la requête actuelle.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-162">Gets or sets the current query text.</span></span><br/>                                                  |
| [<span data-ttu-id="b0e3c-163">**ResultsStyle**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-163">**ResultsStyle**</span></span>](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | <span data-ttu-id="b0e3c-164">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="b0e3c-164">Write-only</span></span><br/> | <span data-ttu-id="b0e3c-165">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-165">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="b0e3c-166">**SortOrderProperty**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-166">**SortOrderProperty**</span></span>](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | <span data-ttu-id="b0e3c-167">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b0e3c-167">Read/write</span></span><br/> | <span data-ttu-id="b0e3c-168">Cette propriété définit ou retourne l’ordre des colonnes de tri des résultats.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-168">This property will set or return the order of columns to sort results by.</span></span> <br/>            |
| [<span data-ttu-id="b0e3c-169">**SortProperty**</span><span class="sxs-lookup"><span data-stu-id="b0e3c-169">**SortProperty**</span></span>](-search-2x-iresultsviewer-sortproperty.md)<br/>           | <span data-ttu-id="b0e3c-170">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b0e3c-170">Read/write</span></span><br/> | <span data-ttu-id="b0e3c-171">Cette propriété définit ou retourne le IndexColumn de la propriété selon laquelle trier les résultats.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-171">This property will set or return the IndexColumn of the property to sort results by.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0e3c-172">Notes</span><span class="sxs-lookup"><span data-stu-id="b0e3c-172">Remarks</span></span>

<span data-ttu-id="b0e3c-173">Ces méthodes et propriétés sont utilisées pour manipuler les informations affichées.</span><span class="sxs-lookup"><span data-stu-id="b0e3c-173">These methods and properties are used to manipulate the information viewed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e3c-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0e3c-174">Requirements</span></span>



| <span data-ttu-id="b0e3c-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0e3c-175">Requirement</span></span> | <span data-ttu-id="b0e3c-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0e3c-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e3c-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e3c-177">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e3c-178">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0e3c-178">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b0e3c-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e3c-179">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e3c-180">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0e3c-180">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b0e3c-181">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b0e3c-181">Redistributable</span></span><br/>          | <span data-ttu-id="b0e3c-182">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="b0e3c-182">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="b0e3c-183">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0e3c-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e3c-184"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e3c-184"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

