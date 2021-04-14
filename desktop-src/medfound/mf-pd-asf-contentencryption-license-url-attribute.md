---
description: Spécifie l’URL d’acquisition de licence pour un fichier ASF (Advanced Systems Format) chiffré. Cet attribut correspond au champ URL de licence de l’en-tête de chiffrement de contenu, défini dans la spécification ASF.
ms.assetid: fe431c38-8227-4385-ac6f-72b9982cde62
title: Attribut MF_PD_ASF_CONTENTENCRYPTION_LICENSE_URL (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5245ebbc5bfeac8b363898b4913c82b94990fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484817"
---
# <a name="mf_pd_asf_contentencryption_license_url-attribute"></a><span data-ttu-id="ebf6b-104">\_Attribut d' \_ \_ URL de \_ licence CONTENTENCRYPTION pour MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="ebf6b-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_LICENSE\_URL attribute</span></span>

<span data-ttu-id="ebf6b-105">Spécifie l’URL d’acquisition de licence pour un fichier ASF (Advanced Systems Format) chiffré.</span><span class="sxs-lookup"><span data-stu-id="ebf6b-105">Specifies the license acquisition URL for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="ebf6b-106">Cet attribut correspond au champ URL de licence de l’en-tête de chiffrement de contenu, défini dans la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="ebf6b-106">This attribute corresponds to the License URL field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="ebf6b-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="ebf6b-107">Data type</span></span>

<span data-ttu-id="ebf6b-108">Chaîne de caractères larges</span><span class="sxs-lookup"><span data-stu-id="ebf6b-108">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf6b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ebf6b-109">Remarks</span></span>

<span data-ttu-id="ebf6b-110">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="ebf6b-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="ebf6b-111">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) récupère le champ URL de licence, le convertit en une chaîne de caractères larges, puis remplit un tableau de **WCHAR** qui se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="ebf6b-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the License URL field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="ebf6b-112">La taille du tableau est égale au champ longueur de l’URL de licence de l’en-tête de chiffrement de contenu.</span><span class="sxs-lookup"><span data-stu-id="ebf6b-112">The size of the array equals the License URL Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf6b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebf6b-113">Requirements</span></span>



| <span data-ttu-id="ebf6b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebf6b-114">Requirement</span></span> | <span data-ttu-id="ebf6b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf6b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf6b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf6b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf6b-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebf6b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ebf6b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf6b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf6b-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebf6b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ebf6b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebf6b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebf6b-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebf6b-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebf6b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf6b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf6b-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ebf6b-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ebf6b-124">**IMFAttributes :: GetString**</span><span class="sxs-lookup"><span data-stu-id="ebf6b-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="ebf6b-125">**IMFAttributes :: SetString**</span><span class="sxs-lookup"><span data-stu-id="ebf6b-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="ebf6b-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ebf6b-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ebf6b-127">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="ebf6b-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="ebf6b-128">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="ebf6b-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="ebf6b-129">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="ebf6b-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




