---
description: Contient la liste des langages RFC 1766 utilisés dans la présentation actuelle.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: Attribut MF_PD_ASF_LANGLIST_LEGACYORDER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24abc714a7605800faa8ad66f8c0b888fba6f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530108"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a><span data-ttu-id="6fb90-103">MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER (attribut)</span><span class="sxs-lookup"><span data-stu-id="6fb90-103">MF\_PD\_ASF\_LANGLIST\_LEGACYORDER attribute</span></span>

<span data-ttu-id="6fb90-104">Contient la liste des langages RFC 1766 utilisés dans la présentation actuelle.</span><span class="sxs-lookup"><span data-stu-id="6fb90-104">Contains a list of RFC 1766 languages used in the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="6fb90-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="6fb90-105">Data type</span></span>

<span data-ttu-id="6fb90-106">**POIDS \[\]**</span><span class="sxs-lookup"><span data-stu-id="6fb90-106">**BYTE \[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="6fb90-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="6fb90-107">Get/set</span></span>

<span data-ttu-id="6fb90-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="6fb90-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="6fb90-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="6fb90-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6fb90-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="6fb90-110">Applies to</span></span>

[<span data-ttu-id="6fb90-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="6fb90-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="6fb90-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6fb90-112">Remarks</span></span>

<span data-ttu-id="6fb90-113">Cet attribut s’applique aux descripteurs de présentation générés à partir de l' [objet ASF ContentInfo](asf-contentinfo-object.md) par un appel à [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="6fb90-113">This attribute applies to presentation descriptors that were generated from the [ASF ContentInfo Object](asf-contentinfo-object.md) by a call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="6fb90-114">Le format du tableau d’octets est le suivant :</span><span class="sxs-lookup"><span data-stu-id="6fb90-114">The format of the byte array is as follows:</span></span>



| <span data-ttu-id="6fb90-115">Champ de l’objet de liste de langues</span><span class="sxs-lookup"><span data-stu-id="6fb90-115">Language List Object field</span></span> | <span data-ttu-id="6fb90-116">Type de données</span><span class="sxs-lookup"><span data-stu-id="6fb90-116">Data type</span></span>    | <span data-ttu-id="6fb90-117">Taille</span><span class="sxs-lookup"><span data-stu-id="6fb90-117">Size</span></span>    | <span data-ttu-id="6fb90-118">Description</span><span class="sxs-lookup"><span data-stu-id="6fb90-118">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="6fb90-119">Nombre d’enregistrements de l’ID de langue</span><span class="sxs-lookup"><span data-stu-id="6fb90-119">Language ID Records Count</span></span>  | <span data-ttu-id="6fb90-120">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="6fb90-120">**DWORD**</span></span>    | <span data-ttu-id="6fb90-121">4 octets</span><span class="sxs-lookup"><span data-stu-id="6fb90-121">4 bytes</span></span> | <span data-ttu-id="6fb90-122">Nombre de langues</span><span class="sxs-lookup"><span data-stu-id="6fb90-122">Number of languages</span></span>                    |
| <span data-ttu-id="6fb90-123">Enregistrements d’ID de langue</span><span class="sxs-lookup"><span data-stu-id="6fb90-123">Language ID Records</span></span>        | <span data-ttu-id="6fb90-124">**POIDS**\[\]</span><span class="sxs-lookup"><span data-stu-id="6fb90-124">**BYTE**\[\]</span></span> | <span data-ttu-id="6fb90-125">Variable</span><span class="sxs-lookup"><span data-stu-id="6fb90-125">Varies</span></span>  | <span data-ttu-id="6fb90-126">Tableau de chaînes de langage (voir ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="6fb90-126">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="6fb90-127">Le premier **DWORD** est le nombre de langages, suivi d’un tableau de chaînes d’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="6fb90-127">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="6fb90-128">Chaque chaîne a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="6fb90-128">Each string has the following format:</span></span>



| <span data-ttu-id="6fb90-129">Champ de l’objet de liste de langues</span><span class="sxs-lookup"><span data-stu-id="6fb90-129">Language List Object field</span></span> | <span data-ttu-id="6fb90-130">Type de données</span><span class="sxs-lookup"><span data-stu-id="6fb90-130">Data type</span></span>     | <span data-ttu-id="6fb90-131">Taille</span><span class="sxs-lookup"><span data-stu-id="6fb90-131">Size</span></span>    | <span data-ttu-id="6fb90-132">Description</span><span class="sxs-lookup"><span data-stu-id="6fb90-132">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb90-133">Longueur de l’ID de langue</span><span class="sxs-lookup"><span data-stu-id="6fb90-133">Language ID Length</span></span>         | <span data-ttu-id="6fb90-134">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="6fb90-134">**DWORD**</span></span>     | <span data-ttu-id="6fb90-135">4 octets</span><span class="sxs-lookup"><span data-stu-id="6fb90-135">4 bytes</span></span> | <span data-ttu-id="6fb90-136">Longueur de la chaîne en octets, y compris la taille du caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="6fb90-136">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="6fb90-137">ID de langue</span><span class="sxs-lookup"><span data-stu-id="6fb90-137">Language ID</span></span>                | <span data-ttu-id="6fb90-138">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="6fb90-138">**WCHAR**\[\]</span></span> | <span data-ttu-id="6fb90-139">Variable</span><span class="sxs-lookup"><span data-stu-id="6fb90-139">Varies</span></span>  | <span data-ttu-id="6fb90-140">Chaîne terminée par le caractère null qui contient le nom du langage RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="6fb90-140">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="6fb90-141">Chaque chaîne est une balise de langue conforme à la norme RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="6fb90-141">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="6fb90-142">Utilisez cet attribut uniquement pour la compatibilité descendante avec l’ordre d’énumération de l’interface [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6fb90-142">Use this attribute only for backward compatibility with the enumeration order of the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface in the Windows Media Format SDK.</span></span> <span data-ttu-id="6fb90-143">Les chaînes de langue sont stockées dans un ordre différent dans l’attribut [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6fb90-143">The language strings are stored in a different order in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fb90-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fb90-144">Requirements</span></span>



| <span data-ttu-id="6fb90-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fb90-145">Requirement</span></span> | <span data-ttu-id="6fb90-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fb90-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb90-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fb90-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb90-148">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fb90-148">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6fb90-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fb90-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb90-150">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fb90-150">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6fb90-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fb90-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fb90-152"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fb90-152"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fb90-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fb90-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb90-154">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6fb90-154">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6fb90-155">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="6fb90-155">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
