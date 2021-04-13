---
description: Erreurs de rendu
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Erreurs de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482233"
---
# <a name="rendering-errors"></a><span data-ttu-id="4e2cb-103">Erreurs de rendu</span><span class="sxs-lookup"><span data-stu-id="4e2cb-103">Rendering Errors</span></span>

> [!Note]  
> <span data-ttu-id="4e2cb-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-104">\[Deprecated.</span></span> <span data-ttu-id="4e2cb-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4e2cb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4e2cb-106">Microsoft® DirectShow® Editing services (DES) définit différents codes d’erreur utilisés pour consigner les erreurs de rendu.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-106">Microsoft® DirectShow® Editing Services (DES) defines various error codes used to log rendering errors.</span></span> <span data-ttu-id="4e2cb-107">Si un projet ne s’affiche pas correctement, le moteur de rendu appelle la méthode [**IAMErrorLog :: LogError**](iamerrorlog-logerror.md) .</span><span class="sxs-lookup"><span data-stu-id="4e2cb-107">If a project does not render correctly, the render engine calls the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="4e2cb-108">Le tableau suivant récapitule les paramètres fournis à **LogError**:</span><span class="sxs-lookup"><span data-stu-id="4e2cb-108">The following table summarizes the parameters given to **LogError**:</span></span>

-   <span data-ttu-id="4e2cb-109">Le code d’erreur est contenu dans le paramètre *ErrorCode* .</span><span class="sxs-lookup"><span data-stu-id="4e2cb-109">The error code is contained in the *ErrorCode* parameter.</span></span>
-   <span data-ttu-id="4e2cb-110">La description est contenue dans le paramètre ErrorString.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-110">The description is contained in the ErrorString parameter.</span></span>
-   <span data-ttu-id="4e2cb-111">La description est contenue dans le paramètre *ErrorString* .</span><span class="sxs-lookup"><span data-stu-id="4e2cb-111">The description is contained in the *ErrorString* parameter.</span></span>
-   <span data-ttu-id="4e2cb-112">S’il existe des informations supplémentaires, le type **Variant** est contenu dans le membre **VT** de la **variante** vers laquelle pointe *pExtraInfo*.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-112">If there is extra information, the **VARIANT** type is contained in the **vt** member of the **VARIANT** pointed to by *pExtraInfo*.</span></span>

> [!Note]  
> <span data-ttu-id="4e2cb-113">Les codes d’erreur décrits ici ne sont pas des valeurs **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e2cb-113">The error codes described here are not **HRESULT** values.</span></span> <span data-ttu-id="4e2cb-114">Pour obtenir la liste des valeurs de retour **HRESULT** spécifiques à des, consultez [codes d’erreur et de réussite](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4e2cb-114">For a list of **HRESULT** return values specific to DES, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e2cb-115">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="4e2cb-115">Error code</span></span></th>
<th><span data-ttu-id="4e2cb-116">Description</span><span class="sxs-lookup"><span data-stu-id="4e2cb-116">Description</span></span></th>
<th><span data-ttu-id="4e2cb-117">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4e2cb-117">Extra information</span></span></th>
<th><span data-ttu-id="4e2cb-118">Type de variante</span><span class="sxs-lookup"><span data-stu-id="4e2cb-118">Variant type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e2cb-119">DEX_IDS_BAD_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="4e2cb-119">DEX_IDS_BAD_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="4e2cb-120">Le nom de fichier n’existe pas ou DirectShow ne reconnaît pas l’extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-120">File name doesn't exist, or DirectShow doesn't recognize the file extension.</span></span></td>
<td><span data-ttu-id="4e2cb-121">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="4e2cb-121">File name</span></span></td>
<td><span data-ttu-id="4e2cb-122"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-122"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-123">DEX_IDS_BAD_SOURCE_NAME2</span><span class="sxs-lookup"><span data-stu-id="4e2cb-123">DEX_IDS_BAD_SOURCE_NAME2</span></span></td>
<td><span data-ttu-id="4e2cb-124">Le type de fichier ne correspond pas à l’extension de fichier ou le fichier est endommagé.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-124">File type does not match the file extension or the file is corrupt.</span></span></td>
<td><span data-ttu-id="4e2cb-125">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="4e2cb-125">File name</span></span></td>
<td><span data-ttu-id="4e2cb-126"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-126"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e2cb-127">DEX_IDS_MISSING_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="4e2cb-127">DEX_IDS_MISSING_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="4e2cb-128">Le nom de fichier est requis, mais n’a pas été donné.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-128">File name was required, but wasn't given.</span></span></td>
<td><span data-ttu-id="4e2cb-129">Aucune</span><span class="sxs-lookup"><span data-stu-id="4e2cb-129">None</span></span></td>
<td><span data-ttu-id="4e2cb-130">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e2cb-130">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-131">DEX_IDS_UNKNOWN_SOURCE</span><span class="sxs-lookup"><span data-stu-id="4e2cb-131">DEX_IDS_UNKNOWN_SOURCE</span></span></td>
<td><span data-ttu-id="4e2cb-132">Impossible d’analyser la source de données fournie par cette source.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-132">Cannot parse data source provided by this source.</span></span></td>
<td><span data-ttu-id="4e2cb-133">Aucune</span><span class="sxs-lookup"><span data-stu-id="4e2cb-133">None</span></span></td>
<td><span data-ttu-id="4e2cb-134">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e2cb-134">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e2cb-135">DEX_IDS_INSTALL_PROBLEM</span><span class="sxs-lookup"><span data-stu-id="4e2cb-135">DEX_IDS_INSTALL_PROBLEM</span></span></td>
<td><span data-ttu-id="4e2cb-136">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-136">Unexpected error.</span></span> <span data-ttu-id="4e2cb-137">Certains composants DirectShow ne sont pas installés correctement.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-137">Some DirectShow component is not installed properly.</span></span></td>
<td><span data-ttu-id="4e2cb-138">Aucune</span><span class="sxs-lookup"><span data-stu-id="4e2cb-138">None</span></span></td>
<td><span data-ttu-id="4e2cb-139">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e2cb-139">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-140">DEX_IDS_NO_SOURCE_NAMES</span><span class="sxs-lookup"><span data-stu-id="4e2cb-140">DEX_IDS_NO_SOURCE_NAMES</span></span></td>
<td><span data-ttu-id="4e2cb-141">Le filtre source n’accepte pas les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-141">Source filter does not accept file names.</span></span></td>
<td><span data-ttu-id="4e2cb-142">Aucune</span><span class="sxs-lookup"><span data-stu-id="4e2cb-142">None</span></span></td>
<td><span data-ttu-id="4e2cb-143">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e2cb-143">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e2cb-144">DEX_IDS_BAD_MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="4e2cb-144">DEX_IDS_BAD_MEDIATYPE</span></span></td>
<td><span data-ttu-id="4e2cb-145">Le type de média du groupe n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-145">Group's media type is not supported.</span></span></td>
<td><span data-ttu-id="4e2cb-146">Numéro du groupe</span><span class="sxs-lookup"><span data-stu-id="4e2cb-146">Group number</span></span></td>
<td><span data-ttu-id="4e2cb-147"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-147"><strong>int</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-148">DEX_IDS_STREAM_NUMBER</span><span class="sxs-lookup"><span data-stu-id="4e2cb-148">DEX_IDS_STREAM_NUMBER</span></span></td>
<td><span data-ttu-id="4e2cb-149">Numéro de flux non valide pour cette source.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-149">Invalid stream number for this source.</span></span></td>
<td><span data-ttu-id="4e2cb-150">Numéro de flux</span><span class="sxs-lookup"><span data-stu-id="4e2cb-150">Stream number</span></span></td>
<td><span data-ttu-id="4e2cb-151"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-151"><strong>int</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e2cb-152">DEX_IDS_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="4e2cb-152">DEX_IDS_OUTOFMEMORY</span></span></td>
<td><span data-ttu-id="4e2cb-153">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-153">Out of memory.</span></span></td>
<td><span data-ttu-id="4e2cb-154">Aucune</span><span class="sxs-lookup"><span data-stu-id="4e2cb-154">None</span></span></td>
<td><span data-ttu-id="4e2cb-155">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e2cb-155">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-156">DEX_IDS_DIBSEQ_NOTALLSAME</span><span class="sxs-lookup"><span data-stu-id="4e2cb-156">DEX_IDS_DIBSEQ_NOTALLSAME</span></span></td>
<td><span data-ttu-id="4e2cb-157">Une image bitmap de la séquence n’est pas du même type que les autres.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-157">One bitmap in the sequence was not the same type as the others.</span></span></td>
<td><span data-ttu-id="4e2cb-158">Nom de la bitmap</span><span class="sxs-lookup"><span data-stu-id="4e2cb-158">Bitmap name</span></span></td>
<td><span data-ttu-id="4e2cb-159"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-159"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e2cb-160">DEX_IDS_CLIPTOOSHORT</span><span class="sxs-lookup"><span data-stu-id="4e2cb-160">DEX_IDS_CLIPTOOSHORT</span></span></td>
<td><span data-ttu-id="4e2cb-161">Les heures de média du clip ne sont pas valides ou la séquence de bitmaps indépendantes du périphérique (DIB) est trop petite.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-161">Clip's media times are invalid, or the device-independent bitmap (DIB) sequence is too short.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e2cb-162">Si d’autres erreurs de rendu se produisent, cette erreur peut se produire même si les temps de support sont valides.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-162">If other rendering errors occur, this error might occur even though the media times are valid.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="4e2cb-163">Aucune</span><span class="sxs-lookup"><span data-stu-id="4e2cb-163">None</span></span></td>
<td><span data-ttu-id="4e2cb-164">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e2cb-164">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-165">DEX_IDS_INVALID_DXT</span><span class="sxs-lookup"><span data-stu-id="4e2cb-165">DEX_IDS_INVALID_DXT</span></span></td>
<td><span data-ttu-id="4e2cb-166">L’identificateur de classe (CLSID) de l’effet ou de la transition n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-166">Class identifier (CLSID) of the effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="4e2cb-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="4e2cb-167">CLSID</span></span></td>
<td><span data-ttu-id="4e2cb-168"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-168"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e2cb-169">DEX_IDS_INVALID_DEFAULT_DXT</span><span class="sxs-lookup"><span data-stu-id="4e2cb-169">DEX_IDS_INVALID_DEFAULT_DXT</span></span></td>
<td><span data-ttu-id="4e2cb-170">Le CLSID de l’effet ou de la transition par défaut n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-170">The CLSID of the default effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="4e2cb-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="4e2cb-171">CLSID</span></span></td>
<td><span data-ttu-id="4e2cb-172"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-172"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-173">DEX_IDS_NO_3D</span><span class="sxs-lookup"><span data-stu-id="4e2cb-173">DEX_IDS_NO_3D</span></span></td>
<td><span data-ttu-id="4e2cb-174">Votre version de DirectX ne prend pas en charge les transitions en trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-174">Your version of DirectX does not support three-dimensional transitions.</span></span></td>
<td><span data-ttu-id="4e2cb-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="4e2cb-175">CLSID</span></span></td>
<td><span data-ttu-id="4e2cb-176"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-176"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e2cb-177">DEX_IDS_BROKEN_DXT</span><span class="sxs-lookup"><span data-stu-id="4e2cb-177">DEX_IDS_BROKEN_DXT</span></span></td>
<td><span data-ttu-id="4e2cb-178">Cet effet n’est pas le bon type ou est rompu.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-178">This effect is not the right kind, or is broken.</span></span></td>
<td><span data-ttu-id="4e2cb-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="4e2cb-179">CLSID</span></span></td>
<td><span data-ttu-id="4e2cb-180"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-180"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-181">DEX_IDS_NO_SUCH_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="4e2cb-181">DEX_IDS_NO_SUCH_PROPERTY</span></span></td>
<td><span data-ttu-id="4e2cb-182">Aucune propriété de ce type n’existe sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-182">No such property exists on the object.</span></span></td>
<td><span data-ttu-id="4e2cb-183">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="4e2cb-183">Property name</span></span></td>
<td><span data-ttu-id="4e2cb-184"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-184"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e2cb-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span><span class="sxs-lookup"><span data-stu-id="4e2cb-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span></span></td>
<td><span data-ttu-id="4e2cb-186">Valeur non conforme pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-186">Illegal value for this property.</span></span></td>
<td><span data-ttu-id="4e2cb-187">Valeur spécifiée</span><span class="sxs-lookup"><span data-stu-id="4e2cb-187">Value specified</span></span></td>
<td><span data-ttu-id="4e2cb-188"><strong>DIFFÉRENT</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-188"><strong>VARIANT</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-189">DEX_IDS_INVALID_XML</span><span class="sxs-lookup"><span data-stu-id="4e2cb-189">DEX_IDS_INVALID_XML</span></span></td>
<td><span data-ttu-id="4e2cb-190">Erreur de syntaxe dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-190">Syntax error in XML file.</span></span></td>
<td><span data-ttu-id="4e2cb-191">Numéro de ligne</span><span class="sxs-lookup"><span data-stu-id="4e2cb-191">Line number</span></span></td>
<td><span data-ttu-id="4e2cb-192">VT_I4 (entier sur 4 octets)</span><span class="sxs-lookup"><span data-stu-id="4e2cb-192">VT_I4 (4-byte integer)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e2cb-193">DEX_IDS_CANT_FIND_FILTER</span><span class="sxs-lookup"><span data-stu-id="4e2cb-193">DEX_IDS_CANT_FIND_FILTER</span></span></td>
<td><span data-ttu-id="4e2cb-194">Le filtre spécifié dans XML est introuvable par catégorie et par instance.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-194">Cannot find filter specified in XML by category and instance.</span></span></td>
<td><span data-ttu-id="4e2cb-195">Nom convivial (instance)</span><span class="sxs-lookup"><span data-stu-id="4e2cb-195">Friendly name (instance)</span></span></td>
<td><span data-ttu-id="4e2cb-196"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-196"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-197">DEX_IDS_DISK_WRITE_ERROR</span><span class="sxs-lookup"><span data-stu-id="4e2cb-197">DEX_IDS_DISK_WRITE_ERROR</span></span></td>
<td><span data-ttu-id="4e2cb-198">Erreur lors de l’écriture du fichier XML sur le disque.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-198">Error writing XML file to disk.</span></span></td>
<td><span data-ttu-id="4e2cb-199">Aucune</span><span class="sxs-lookup"><span data-stu-id="4e2cb-199">None</span></span></td>
<td><span data-ttu-id="4e2cb-200">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e2cb-200">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e2cb-201">DEX_IDS_INVALID_AUDIO_FX</span><span class="sxs-lookup"><span data-stu-id="4e2cb-201">DEX_IDS_INVALID_AUDIO_FX</span></span></td>
<td><span data-ttu-id="4e2cb-202">CLSID n’est pas un filtre d’effet audio DirectShow valide.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-202">CLSID not a valid DirectShow audio effect filter.</span></span></td>
<td><span data-ttu-id="4e2cb-203">CLSID</span><span class="sxs-lookup"><span data-stu-id="4e2cb-203">CLSID</span></span></td>
<td><span data-ttu-id="4e2cb-204"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4e2cb-204"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e2cb-205">DEX_IDS_CANT_FIND_COMPRESSOR</span><span class="sxs-lookup"><span data-stu-id="4e2cb-205">DEX_IDS_CANT_FIND_COMPRESSOR</span></span></td>
<td><span data-ttu-id="4e2cb-206">Impossible de trouver un compresseur pour produire le format de compression spécifié.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-206">Cannot find a compressor to produce the specified compression format.</span></span></td>
<td><span data-ttu-id="4e2cb-207">Aucune</span><span class="sxs-lookup"><span data-stu-id="4e2cb-207">None</span></span></td>
<td><span data-ttu-id="4e2cb-208">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4e2cb-208">Not applicable</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4e2cb-209">Les erreurs suivantes ne doivent jamais se produire.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-209">The following errors should never occur.</span></span> <span data-ttu-id="4e2cb-210">Si vous rencontrez l’une de ces erreurs, veuillez envoyer un rapport de bogue à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-210">If you encounter one of these errors, please send a bug report to Microsoft.</span></span>



| <span data-ttu-id="4e2cb-211">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="4e2cb-211">Error code</span></span>                 | <span data-ttu-id="4e2cb-212">Description</span><span class="sxs-lookup"><span data-stu-id="4e2cb-212">Description</span></span>                                 |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="4e2cb-213">analyse de la \_ chronologie des ID DEX \_ \_</span><span class="sxs-lookup"><span data-stu-id="4e2cb-213">DEX\_IDS\_TIMELINE\_PARSE</span></span>  | <span data-ttu-id="4e2cb-214">Erreur inattendue lors de l’analyse de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-214">Unexpected error parsing the timeline.</span></span>      |
| <span data-ttu-id="4e2cb-215">\_Erreur du \_ graphique des ID DEX \_</span><span class="sxs-lookup"><span data-stu-id="4e2cb-215">DEX\_IDS\_GRAPH\_ERROR</span></span>     | <span data-ttu-id="4e2cb-216">Erreur inattendue lors de la génération du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-216">Unexpected error building the filter graph.</span></span> |
| <span data-ttu-id="4e2cb-217">\_erreur de \_ grille \_ ID DEX</span><span class="sxs-lookup"><span data-stu-id="4e2cb-217">DEX\_IDS\_GRID\_ERROR</span></span>      | <span data-ttu-id="4e2cb-218">Erreur inattendue avec la grille interne.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-218">Unexpected error with the internal grid.</span></span>    |
| <span data-ttu-id="4e2cb-219">erreur de l' \_ interface ID DEX \_ \_</span><span class="sxs-lookup"><span data-stu-id="4e2cb-219">DEX\_IDS\_INTERFACE\_ERROR</span></span> | <span data-ttu-id="4e2cb-220">Erreur inattendue lors de l’obtention d’une interface.</span><span class="sxs-lookup"><span data-stu-id="4e2cb-220">Unexpected error getting an interface.</span></span>      |



 

 

 




