---
description: Spécifie le type de mécanisme de protection utilisé dans un fichier ASF (Advanced Systems Format).
ms.assetid: 91ceb610-6ff4-4133-beab-6debb94eec2c
title: Attribut MF_PD_ASF_CONTENTENCRYPTION_TYPE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9131b24138edf6e85fc0e264bdcdd028f2eb0538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862501"
---
# <a name="mf_pd_asf_contentencryption_type-attribute"></a><span data-ttu-id="1325c-103">\_Attribut de \_ \_ type CONTENTENCRYPTION \_ pour MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="1325c-103">MF\_PD\_ASF\_CONTENTENCRYPTION\_TYPE attribute</span></span>

<span data-ttu-id="1325c-104">Spécifie le type de mécanisme de protection utilisé dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="1325c-104">Specifies the type of protection mechanism used in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="1325c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1325c-105">Data type</span></span>

<span data-ttu-id="1325c-106">Chaîne de caractères larges</span><span class="sxs-lookup"><span data-stu-id="1325c-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="1325c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1325c-107">Remarks</span></span>

<span data-ttu-id="1325c-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="1325c-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="1325c-109">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) récupère le champ type de protection, le convertit en une chaîne de caractères larges, puis remplit un tableau de **WCHAR** qui se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="1325c-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Protection Type field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="1325c-110">S’il est présent, la valeur doit être « DRM ».</span><span class="sxs-lookup"><span data-stu-id="1325c-110">If present, the value must be "DRM".</span></span> <span data-ttu-id="1325c-111">La taille du tableau est égale au champ de longueur du champ de type de protection de l’en-tête de chiffrement de contenu.</span><span class="sxs-lookup"><span data-stu-id="1325c-111">The size of the array equals the Protection Type Field Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="1325c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1325c-112">Requirements</span></span>



| <span data-ttu-id="1325c-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1325c-113">Requirement</span></span> | <span data-ttu-id="1325c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1325c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1325c-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1325c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1325c-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1325c-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1325c-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1325c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1325c-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1325c-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1325c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1325c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1325c-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="1325c-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1325c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1325c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1325c-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1325c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1325c-123">**IMFAttributes :: GetString**</span><span class="sxs-lookup"><span data-stu-id="1325c-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="1325c-124">**IMFAttributes :: SetString**</span><span class="sxs-lookup"><span data-stu-id="1325c-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="1325c-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1325c-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="1325c-126">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="1325c-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="1325c-127">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="1325c-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="1325c-128">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="1325c-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




