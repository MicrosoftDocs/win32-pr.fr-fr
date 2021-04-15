---
title: Jeux de propriétés DocumentSummaryInformation et UserDefined
description: Un jeu de propriétés DocumentSummaryInformation et UserDefined est une extension du jeu de propriétés d’informations de résumé. Les deux jeux de propriétés peuvent exister simultanément.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- Jeux de propriétés UserDefined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507203"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a><span data-ttu-id="2b500-106">Jeux de propriétés DocumentSummaryInformation et UserDefined</span><span class="sxs-lookup"><span data-stu-id="2b500-106">The DocumentSummaryInformation and UserDefined Property Sets</span></span>

<span data-ttu-id="2b500-107">Un jeu de propriétés **DocumentSummaryInformation** et **UserDefined** est une extension [du jeu de propriétés d’informations de résumé](the-summary-information-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="2b500-107">A **DocumentSummaryInformation** and **UserDefined** property set is an extension to [the Summary Information property set](the-summary-information-property-set.md).</span></span> <span data-ttu-id="2b500-108">Les deux jeux de propriétés peuvent exister simultanément.</span><span class="sxs-lookup"><span data-stu-id="2b500-108">Both property sets can exist simultaneously.</span></span>

<span data-ttu-id="2b500-109">Le nom du flux qui contient le jeu de propriétés **DocumentSummaryInformation** est **« \\ 005DocumentSummaryInformation »**.</span><span class="sxs-lookup"><span data-stu-id="2b500-109">The name of the stream that contains the **DocumentSummaryInformation** property set is **"\\005DocumentSummaryInformation"**.</span></span> <span data-ttu-id="2b500-110">L’identificateur de format (FMTID) pour le jeu de propriétés **DocumentSummaryInformation** est **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="2b500-110">The format identifier (FMTID) for the **DocumentSummaryInformation** property set is **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="2b500-111">La déclaration de cette valeur est disponible dans les fichiers d’en-tête fournis sous la forme **fmtid \_ DocSummaryInformation**.</span><span class="sxs-lookup"><span data-stu-id="2b500-111">The declaration for this value is available in the provided header files as **FMTID\_DocSummaryInformation**.</span></span> <span data-ttu-id="2b500-112">Pour plus d’informations, consultez [noms dans IStorage](names-in-istorage.md), [propriété informations de synthèse définie](the-summary-information-property-set.md), [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) et [format identificateurs](format-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="2b500-112">For more information, see [Names in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [Format Identifiers](format-identifiers.md).</span></span>

<span data-ttu-id="2b500-113">Ce flux comporte également une section distincte pour les propriétés personnalisées définies par l’utilisateur, comme dans les jeux de propriétés **DocumentSummaryInformation** et **UserDefined** .</span><span class="sxs-lookup"><span data-stu-id="2b500-113">This stream also has a separate section for the custom-user-defined properties as in the **DocumentSummaryInformation** and **UserDefined** property sets.</span></span> <span data-ttu-id="2b500-114">Cette section apparaît dans l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) en tant que jeu de propriétés distinct, avec le fmtid suivant (disponible en tant que **fmtid \_ UserDefinedProperties**) : **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="2b500-114">This section appears in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface as a separate property set, with the following FMTID (available as **FMTID\_UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="2b500-115">Ces deux jeux de propriétés sont les seuls pour lesquels un seul flux peut contenir plusieurs jeux de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b500-115">These two property sets are the only ones for which a single stream can hold multiple property sets.</span></span> <span data-ttu-id="2b500-116">Le fait que ces deux jeux de propriétés se trouvent dans un seul flux affecte le comportement de l’interface **IPropertySetStorage** .</span><span class="sxs-lookup"><span data-stu-id="2b500-116">The fact that these two property sets are in a single stream affects the behavior of the **IPropertySetStorage** interface.</span></span> <span data-ttu-id="2b500-117">Pour plus d’informations, consultez [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span><span class="sxs-lookup"><span data-stu-id="2b500-117">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span></span>

<span data-ttu-id="2b500-118">Le tableau suivant répertorie les propriétés ajoutées au jeu de propriétés **DocumentSummaryInformation** et **UserDefined** .</span><span class="sxs-lookup"><span data-stu-id="2b500-118">The following table lists the added properties to the **DocumentSummaryInformation** and **UserDefined** property set.</span></span> <span data-ttu-id="2b500-119">Comme dans le jeu de propriétés **SummaryInformation** , les noms ne sont généralement pas stockés dans le jeu de propriétés, mais sont déduits à partir de l’identificateur de propriété.</span><span class="sxs-lookup"><span data-stu-id="2b500-119">As in the **SummaryInformation** property set, the names are not typically stored in the property set, but are inferred from the property identifier.</span></span>



| <span data-ttu-id="2b500-120">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="2b500-120">Property name</span></span>      | <span data-ttu-id="2b500-121">Identificateur de propriété</span><span class="sxs-lookup"><span data-stu-id="2b500-121">Property identifier</span></span>     | <span data-ttu-id="2b500-122">Valeur de l’identificateur de propriété</span><span class="sxs-lookup"><span data-stu-id="2b500-122">Property identifier value</span></span> | <span data-ttu-id="2b500-123">Type VARIANT</span><span class="sxs-lookup"><span data-stu-id="2b500-123">VARIANT type</span></span>                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| <span data-ttu-id="2b500-124">Category</span><span class="sxs-lookup"><span data-stu-id="2b500-124">Category</span></span>           | <span data-ttu-id="2b500-125">**\_catégorie PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="2b500-125">**PIDDSI\_CATEGORY**</span></span>    | <span data-ttu-id="2b500-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2b500-126">0x00000002</span></span>                | <span data-ttu-id="2b500-127">**VT- \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="2b500-127">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="2b500-128">PresentationTarget</span><span class="sxs-lookup"><span data-stu-id="2b500-128">PresentationTarget</span></span> | <span data-ttu-id="2b500-129">**PIDDSI \_ PRESFORMAT**</span><span class="sxs-lookup"><span data-stu-id="2b500-129">**PIDDSI\_PRESFORMAT**</span></span>  | <span data-ttu-id="2b500-130">0x00000003</span><span class="sxs-lookup"><span data-stu-id="2b500-130">0x00000003</span></span>                | <span data-ttu-id="2b500-131">**VT- \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="2b500-131">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="2b500-132">Octets</span><span class="sxs-lookup"><span data-stu-id="2b500-132">Bytes</span></span>              | <span data-ttu-id="2b500-133">**PIDDSI \_ BYTECOUNT**</span><span class="sxs-lookup"><span data-stu-id="2b500-133">**PIDDSI\_BYTECOUNT**</span></span>   | <span data-ttu-id="2b500-134">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2b500-134">0x00000004</span></span>                | <span data-ttu-id="2b500-135">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="2b500-135">**VT\_I4**</span></span>                        |
| <span data-ttu-id="2b500-136">Lignes</span><span class="sxs-lookup"><span data-stu-id="2b500-136">Lines</span></span>              | <span data-ttu-id="2b500-137">**PIDDSI \_ LINECOUNT**</span><span class="sxs-lookup"><span data-stu-id="2b500-137">**PIDDSI\_LINECOUNT**</span></span>   | <span data-ttu-id="2b500-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="2b500-138">0x00000005</span></span>                | <span data-ttu-id="2b500-139">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="2b500-139">**VT\_I4**</span></span>                        |
| <span data-ttu-id="2b500-140">Paragraphes</span><span class="sxs-lookup"><span data-stu-id="2b500-140">Paragraphs</span></span>         | <span data-ttu-id="2b500-141">**PIDDSI \_ PARCOUNT**</span><span class="sxs-lookup"><span data-stu-id="2b500-141">**PIDDSI\_PARCOUNT**</span></span>    | <span data-ttu-id="2b500-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="2b500-142">0x00000006</span></span>                | <span data-ttu-id="2b500-143">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="2b500-143">**VT\_I4**</span></span>                        |
| <span data-ttu-id="2b500-144">Diapositives</span><span class="sxs-lookup"><span data-stu-id="2b500-144">Slides</span></span>             | <span data-ttu-id="2b500-145">**PIDDSI \_ SLIDECOUNT**</span><span class="sxs-lookup"><span data-stu-id="2b500-145">**PIDDSI\_SLIDECOUNT**</span></span>  | <span data-ttu-id="2b500-146">0x00000007</span><span class="sxs-lookup"><span data-stu-id="2b500-146">0x00000007</span></span>                | <span data-ttu-id="2b500-147">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="2b500-147">**VT\_I4**</span></span>                        |
| <span data-ttu-id="2b500-148">Notes</span><span class="sxs-lookup"><span data-stu-id="2b500-148">Notes</span></span>              | <span data-ttu-id="2b500-149">**PIDDSI \_ NOTECOUNT**</span><span class="sxs-lookup"><span data-stu-id="2b500-149">**PIDDSI\_NOTECOUNT**</span></span>   | <span data-ttu-id="2b500-150">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2b500-150">0x00000008</span></span>                | <span data-ttu-id="2b500-151">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="2b500-151">**VT\_I4**</span></span>                        |
| <span data-ttu-id="2b500-152">HiddenSlides</span><span class="sxs-lookup"><span data-stu-id="2b500-152">HiddenSlides</span></span>       | <span data-ttu-id="2b500-153">**PIDDSI \_ HIDDENCOUNT**</span><span class="sxs-lookup"><span data-stu-id="2b500-153">**PIDDSI\_HIDDENCOUNT**</span></span> | <span data-ttu-id="2b500-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="2b500-154">0x00000009</span></span>                | <span data-ttu-id="2b500-155">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="2b500-155">**VT\_I4**</span></span>                        |
| <span data-ttu-id="2b500-156">MMClips</span><span class="sxs-lookup"><span data-stu-id="2b500-156">MMClips</span></span>            | <span data-ttu-id="2b500-157">**PIDDSI \_ MMCLIPCOUNT**</span><span class="sxs-lookup"><span data-stu-id="2b500-157">**PIDDSI\_MMCLIPCOUNT**</span></span> | <span data-ttu-id="2b500-158">Stop</span><span class="sxs-lookup"><span data-stu-id="2b500-158">0x0000000A</span></span>                | <span data-ttu-id="2b500-159">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="2b500-159">**VT\_I4**</span></span>                        |
| <span data-ttu-id="2b500-160">ScaleCrop</span><span class="sxs-lookup"><span data-stu-id="2b500-160">ScaleCrop</span></span>          | <span data-ttu-id="2b500-161">**\_échelle PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="2b500-161">**PIDDSI\_SCALE**</span></span>       | <span data-ttu-id="2b500-162">0x0000000B</span><span class="sxs-lookup"><span data-stu-id="2b500-162">0x0000000B</span></span>                | <span data-ttu-id="2b500-163">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="2b500-163">**VT\_BOOL**</span></span>                      |
| <span data-ttu-id="2b500-164">HeadingPairs</span><span class="sxs-lookup"><span data-stu-id="2b500-164">HeadingPairs</span></span>       | <span data-ttu-id="2b500-165">**PIDDSI \_ HEADINGPAIR**</span><span class="sxs-lookup"><span data-stu-id="2b500-165">**PIDDSI\_HEADINGPAIR**</span></span> | <span data-ttu-id="2b500-166">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="2b500-166">0x0000000C</span></span>                | <span data-ttu-id="2b500-167">**VT \_** \| **\_ vecteur VT** de variante</span><span class="sxs-lookup"><span data-stu-id="2b500-167">**VT\_VARIANT** \| **VT\_VECTOR**</span></span> |
| <span data-ttu-id="2b500-168">TitlesofParts</span><span class="sxs-lookup"><span data-stu-id="2b500-168">TitlesofParts</span></span>      | <span data-ttu-id="2b500-169">**PIDDSI \_ DOCPARTS**</span><span class="sxs-lookup"><span data-stu-id="2b500-169">**PIDDSI\_DOCPARTS**</span></span>    | <span data-ttu-id="2b500-170">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="2b500-170">0x0000000D</span></span>                | <span data-ttu-id="2b500-171">**VT \_ vecteur** \| **VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="2b500-171">**VT\_VECTOR** \| **VT\_LPSTR**</span></span>   |
| <span data-ttu-id="2b500-172">Manager</span><span class="sxs-lookup"><span data-stu-id="2b500-172">Manager</span></span>            | <span data-ttu-id="2b500-173">**\_Gestionnaire PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="2b500-173">**PIDDSI\_MANAGER**</span></span>     | <span data-ttu-id="2b500-174">0x0000000E</span><span class="sxs-lookup"><span data-stu-id="2b500-174">0x0000000E</span></span>                | <span data-ttu-id="2b500-175">**VT- \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="2b500-175">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="2b500-176">Company</span><span class="sxs-lookup"><span data-stu-id="2b500-176">Company</span></span>            | <span data-ttu-id="2b500-177">**\_entreprise PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="2b500-177">**PIDDSI\_COMPANY**</span></span>     | <span data-ttu-id="2b500-178">0x0000000F</span><span class="sxs-lookup"><span data-stu-id="2b500-178">0x0000000F</span></span>                | <span data-ttu-id="2b500-179">**VT- \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="2b500-179">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="2b500-180">LinksUpToDate</span><span class="sxs-lookup"><span data-stu-id="2b500-180">LinksUpToDate</span></span>      | <span data-ttu-id="2b500-181">**PIDDSI \_ LINKSDIRTY**</span><span class="sxs-lookup"><span data-stu-id="2b500-181">**PIDDSI\_LINKSDIRTY**</span></span>  | <span data-ttu-id="2b500-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b500-182">0x00000010</span></span>                | <span data-ttu-id="2b500-183">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="2b500-183">**VT\_BOOL**</span></span>                      |



 

<span data-ttu-id="2b500-184">Ces propriétés ont les utilisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2b500-184">These properties have the following uses:</span></span>

<dl> <dt>

<span data-ttu-id="2b500-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Catégorie</span><span class="sxs-lookup"><span data-stu-id="2b500-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="2b500-186">Chaîne de texte tapée par l’utilisateur qui indique la catégorie à laquelle le fichier appartient (Mémo, proposition, etc.).</span><span class="sxs-lookup"><span data-stu-id="2b500-186">A text string typed by the user that indicates what category the file belongs to (memo, proposal, and so on).</span></span> <span data-ttu-id="2b500-187">Il est utile pour rechercher des fichiers du même type.</span><span class="sxs-lookup"><span data-stu-id="2b500-187">It is useful for finding files of same type.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span><span class="sxs-lookup"><span data-stu-id="2b500-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span></span>
</dt> <dd>

<span data-ttu-id="2b500-189">Format cible pour la présentation (35mm, imprimante, vidéo, etc.).</span><span class="sxs-lookup"><span data-stu-id="2b500-189">Target format for presentation (35mm, printer, video, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="2b500-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bits</span><span class="sxs-lookup"><span data-stu-id="2b500-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes</span></span>
</dt> <dd>

<span data-ttu-id="2b500-191">Nombre d'octets.</span><span class="sxs-lookup"><span data-stu-id="2b500-191">Number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Courbes</span><span class="sxs-lookup"><span data-stu-id="2b500-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Lines</span></span>
</dt> <dd>

<span data-ttu-id="2b500-193">Nombre de lignes.</span><span class="sxs-lookup"><span data-stu-id="2b500-193">Number of lines.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Suivants</span><span class="sxs-lookup"><span data-stu-id="2b500-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Paragraphs</span></span>
</dt> <dd>

<span data-ttu-id="2b500-195">Nombre de paragraphes.</span><span class="sxs-lookup"><span data-stu-id="2b500-195">Number of paragraphs.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Suivantes</span><span class="sxs-lookup"><span data-stu-id="2b500-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Slides</span></span>
</dt> <dd>

<span data-ttu-id="2b500-197">Nombre de diapositives.</span><span class="sxs-lookup"><span data-stu-id="2b500-197">Number of slides.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notes</span><span class="sxs-lookup"><span data-stu-id="2b500-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notes</span></span>
</dt> <dd>

<span data-ttu-id="2b500-199">Nombre de pages qui contiennent des remarques.</span><span class="sxs-lookup"><span data-stu-id="2b500-199">Number of pages that contain notes.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span><span class="sxs-lookup"><span data-stu-id="2b500-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span></span>
</dt> <dd>

<span data-ttu-id="2b500-201">Nombre de diapositives masquées.</span><span class="sxs-lookup"><span data-stu-id="2b500-201">Number of slides that are hidden.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span><span class="sxs-lookup"><span data-stu-id="2b500-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span></span>
</dt> <dd>

<span data-ttu-id="2b500-203">Nombre de clips audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="2b500-203">Number of sound or video clips.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span><span class="sxs-lookup"><span data-stu-id="2b500-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span></span>
</dt> <dd>

<span data-ttu-id="2b500-205">Affectez la valeur true (-1) lorsque la mise à l’échelle de la miniature est souhaitée.</span><span class="sxs-lookup"><span data-stu-id="2b500-205">Set to True (-1) when scaling of the thumbnail is desired.</span></span> <span data-ttu-id="2b500-206">Si la valeur n’est pas définie, le rognage est souhaité.</span><span class="sxs-lookup"><span data-stu-id="2b500-206">If not set, cropping is desired.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span><span class="sxs-lookup"><span data-stu-id="2b500-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span></span>
</dt> <dd>

<span data-ttu-id="2b500-208">Propriété utilisée en interne indiquant le regroupement de différentes parties de document et le nombre d’éléments dans chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="2b500-208">Internally used property indicating the grouping of different document parts and the number of items in each group.</span></span> <span data-ttu-id="2b500-209">Les titres des parties de document sont stockés dans la propriété **TitlesofParts** .</span><span class="sxs-lookup"><span data-stu-id="2b500-209">The titles of the document parts are stored in the **TitlesofParts** property.</span></span> <span data-ttu-id="2b500-210">La propriété **HeadingPairs** est stockée sous la forme d’un vecteur de variantes, dans des paires répétées de valeurs **VT \_ LPSTR** (ou **VT \_ LPWStr**) et **VT \_ I4** .</span><span class="sxs-lookup"><span data-stu-id="2b500-210">The **HeadingPairs** property is stored as a vector of variants, in repeating pairs of **VT\_LPSTR** (or **VT\_LPWSTR**) and **VT\_I4** values.</span></span> <span data-ttu-id="2b500-211">La valeur de **VT \_ LPSTR** représente un nom de titre et la valeur **VT \_ I4** indique le nombre de parties de document sous cet en-tête.</span><span class="sxs-lookup"><span data-stu-id="2b500-211">The **VT\_LPSTR** value represents a heading name, and the **VT\_I4** value indicates the count of document parts under that heading.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span><span class="sxs-lookup"><span data-stu-id="2b500-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span></span>
</dt> <dd>

<span data-ttu-id="2b500-213">Noms des parties de document.</span><span class="sxs-lookup"><span data-stu-id="2b500-213">Names of document parts.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Gestion</span><span class="sxs-lookup"><span data-stu-id="2b500-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager</span></span>
</dt> <dd>

<span data-ttu-id="2b500-215">Gestionnaire du projet.</span><span class="sxs-lookup"><span data-stu-id="2b500-215">Manager of the project.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Entreprise</span><span class="sxs-lookup"><span data-stu-id="2b500-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="2b500-217">Nom de la société</span><span class="sxs-lookup"><span data-stu-id="2b500-217">Company name.</span></span>

</dd> <dt>

<span data-ttu-id="2b500-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span><span class="sxs-lookup"><span data-stu-id="2b500-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span></span>
</dt> <dd>

<span data-ttu-id="2b500-219">Valeur booléenne pour indiquer si les liens personnalisés sont gênés par un bruit excessif, pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="2b500-219">Boolean value to indicate whether the custom links are hampered by excessive noise, for all applications.</span></span>

> [!Note]  
> <span data-ttu-id="2b500-220">Comme décrit dans 12,3.</span><span class="sxs-lookup"><span data-stu-id="2b500-220">As described in 12.3.</span></span> <span data-ttu-id="2b500-221">Format sérialisé pour les jeux de propriétés de la spécification de conception OLE 2,0, les éléments vectoriels dans les propriétés **HeadingPairs** et **TitlesofParts** doivent être alignés sur des limites de 32 bits dans le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b500-221">Serialized Format for Property Sets of the OLE 2.0 Design Specification, vector elements in the **HeadingPairs** and **TitlesofParts** properties should be aligned on 32 bit boundaries within the property set.</span></span> <span data-ttu-id="2b500-222">Toutefois, dans les jeux de propriétés **DocumentSummaryInformation** et **UserDefined** , lorsque la page de codes du jeu de propriétés n’est pas Unicode, ces éléments doivent être empaquetés.</span><span class="sxs-lookup"><span data-stu-id="2b500-222">However, in the **DocumentSummaryInformation** and **UserDefined** property sets, when the code page of the property set is not Unicode, these elements must be packed.</span></span>

 

</dd> </dl>

<span data-ttu-id="2b500-223">La propriété **UserDefined** définie peut être utilisée pour contenir toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b500-223">The **UserDefined** property set can be used to hold any properties.</span></span> <span data-ttu-id="2b500-224">En règle générale, il est utilisé pour stocker les propriétés nommées créées par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2b500-224">Typically, it is used to store named properties created by a user.</span></span>

 

 




