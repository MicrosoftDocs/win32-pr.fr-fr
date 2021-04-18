---
description: Spécifie une liste de commandes de script et les paramètres d’un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de commande de script dans l’en-tête ASF, défini dans la spécification ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: Attribut MF_PD_ASF_SCRIPT (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519396"
---
# <a name="mf_pd_asf_script-attribute"></a><span data-ttu-id="04520-104">\_Attribut de script MF PD \_ ASF \_</span><span class="sxs-lookup"><span data-stu-id="04520-104">MF\_PD\_ASF\_SCRIPT attribute</span></span>

<span data-ttu-id="04520-105">Spécifie une liste de commandes de script et les paramètres d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="04520-105">Specifies a list of script commands and the parameters for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="04520-106">Cet attribut correspond à l’objet de commande de script dans l’en-tête ASF, défini dans la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="04520-106">This attribute corresponds to the Script Command Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="04520-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="04520-107">Data type</span></span>

<span data-ttu-id="04520-108">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="04520-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="04520-109">Notes</span><span class="sxs-lookup"><span data-stu-id="04520-109">Remarks</span></span>

<span data-ttu-id="04520-110">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="04520-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="04520-111">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crée le descripteur de présentation et génère cet attribut à partir de l’en-tête de l’objet de commande de script.</span><span class="sxs-lookup"><span data-stu-id="04520-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Script Command Object header.</span></span> <span data-ttu-id="04520-112">Le tableau suivant indique le format de l’objet BLOB :</span><span class="sxs-lookup"><span data-stu-id="04520-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="04520-113">Champ de l’objet de commande de script</span><span class="sxs-lookup"><span data-stu-id="04520-113">Script Command Object field</span></span> | <span data-ttu-id="04520-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="04520-114">Data type</span></span>    | <span data-ttu-id="04520-115">Taille</span><span class="sxs-lookup"><span data-stu-id="04520-115">Size</span></span>    | <span data-ttu-id="04520-116">Description</span><span class="sxs-lookup"><span data-stu-id="04520-116">Description</span></span>               |
|-----------------------------|--------------|---------|---------------------------|
| <span data-ttu-id="04520-117">Nombre de commandes</span><span class="sxs-lookup"><span data-stu-id="04520-117">Commands Count</span></span>              | <span data-ttu-id="04520-118">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="04520-118">**DWORD**</span></span>    | <span data-ttu-id="04520-119">4 octets</span><span class="sxs-lookup"><span data-stu-id="04520-119">4 bytes</span></span> | <span data-ttu-id="04520-120">Nombre de commandes de script</span><span class="sxs-lookup"><span data-stu-id="04520-120">Number of script commands</span></span> |
| <span data-ttu-id="04520-121">Type de commande, commandes</span><span class="sxs-lookup"><span data-stu-id="04520-121">Command Type, Commands</span></span>      | <span data-ttu-id="04520-122">**POIDS**\[\]</span><span class="sxs-lookup"><span data-stu-id="04520-122">**BYTE**\[\]</span></span> | <span data-ttu-id="04520-123">Variable</span><span class="sxs-lookup"><span data-stu-id="04520-123">Varies</span></span>  | <span data-ttu-id="04520-124">Tableau de commandes de script</span><span class="sxs-lookup"><span data-stu-id="04520-124">Array of script commands</span></span>  |



 

<span data-ttu-id="04520-125">Le premier **DWORD** est le nombre de commandes de script, suivi d’un tableau de commandes.</span><span class="sxs-lookup"><span data-stu-id="04520-125">The first **DWORD** is the number of script commands, followed by an array of commands.</span></span> <span data-ttu-id="04520-126">Chaque commande de script a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="04520-126">Each script command has the following format:</span></span>



| <span data-ttu-id="04520-127">Champ de l’objet de commande de script</span><span class="sxs-lookup"><span data-stu-id="04520-127">Script Command Object field</span></span> | <span data-ttu-id="04520-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="04520-128">Data type</span></span>     | <span data-ttu-id="04520-129">Taille</span><span class="sxs-lookup"><span data-stu-id="04520-129">Size</span></span>    | <span data-ttu-id="04520-130">Description</span><span class="sxs-lookup"><span data-stu-id="04520-130">Description</span></span>                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| <span data-ttu-id="04520-131">Longueur du nom de la commande</span><span class="sxs-lookup"><span data-stu-id="04520-131">Command Name Length</span></span>         | <span data-ttu-id="04520-132">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="04520-132">**DWORD**</span></span>     | <span data-ttu-id="04520-133">4 octets</span><span class="sxs-lookup"><span data-stu-id="04520-133">4 bytes</span></span> | <span data-ttu-id="04520-134">Taille de la chaîne de commande en octets, y compris le caractère NULL.</span><span class="sxs-lookup"><span data-stu-id="04520-134">Size of the command string, in bytes, including the NULL character.</span></span>      |
| <span data-ttu-id="04520-135">Nom de la commande</span><span class="sxs-lookup"><span data-stu-id="04520-135">Command Name</span></span>                | <span data-ttu-id="04520-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="04520-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="04520-137">Variable</span><span class="sxs-lookup"><span data-stu-id="04520-137">Varies</span></span>  | <span data-ttu-id="04520-138">Chaîne terminée par le caractère null qui contient la commande de script.</span><span class="sxs-lookup"><span data-stu-id="04520-138">Null-terminated string that contains the script command.</span></span>                 |
| <span data-ttu-id="04520-139">Longueur du nom du type de commande</span><span class="sxs-lookup"><span data-stu-id="04520-139">Command Type Name Length</span></span>    | <span data-ttu-id="04520-140">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="04520-140">**DWORD**</span></span>     | <span data-ttu-id="04520-141">4 octets</span><span class="sxs-lookup"><span data-stu-id="04520-141">4 bytes</span></span> | <span data-ttu-id="04520-142">Taille de la chaîne de type de commande, en octets, y compris le caractère NULL.</span><span class="sxs-lookup"><span data-stu-id="04520-142">Size of the command type string, in bytes, including the NULL character.</span></span> |
| <span data-ttu-id="04520-143">Nom du type de commande</span><span class="sxs-lookup"><span data-stu-id="04520-143">Command Type Name</span></span>           | <span data-ttu-id="04520-144">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="04520-144">**WCHAR**\[\]</span></span> | <span data-ttu-id="04520-145">Variable</span><span class="sxs-lookup"><span data-stu-id="04520-145">Varies</span></span>  | <span data-ttu-id="04520-146">Chaîne terminée par le caractère null qui contient le type de commande.</span><span class="sxs-lookup"><span data-stu-id="04520-146">Null-terminated string that contains the command type.</span></span>                   |
| <span data-ttu-id="04520-147">Heure de présentation</span><span class="sxs-lookup"><span data-stu-id="04520-147">Presentation Time</span></span>           | <span data-ttu-id="04520-148">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="04520-148">**DWORD**</span></span>     | <span data-ttu-id="04520-149">4 octets</span><span class="sxs-lookup"><span data-stu-id="04520-149">4 bytes</span></span> | <span data-ttu-id="04520-150">Durée de présentation de la commande, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="04520-150">Presentation time of the command in milliseconds.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="04520-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04520-151">Requirements</span></span>



| <span data-ttu-id="04520-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04520-152">Requirement</span></span> | <span data-ttu-id="04520-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="04520-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04520-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04520-154">Minimum supported client</span></span><br/> | <span data-ttu-id="04520-155">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04520-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="04520-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04520-156">Minimum supported server</span></span><br/> | <span data-ttu-id="04520-157">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04520-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="04520-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="04520-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="04520-159"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="04520-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04520-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04520-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04520-161">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04520-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="04520-162">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="04520-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="04520-163">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="04520-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="04520-164">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="04520-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="04520-165">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="04520-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="04520-166">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="04520-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="04520-167">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="04520-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




