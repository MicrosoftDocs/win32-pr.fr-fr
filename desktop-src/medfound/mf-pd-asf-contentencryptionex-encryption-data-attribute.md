---
description: Contient des données de chiffrement pour un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de chiffrement de contenu étendu dans l’en-tête ASF, défini dans la spécification ASF.
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: Attribut MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550e75f50a7f09556cd9dd89239b3f33fb74d289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318801"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a><span data-ttu-id="f1119-104">\_Attribut de \_ \_ données de \_ chiffrement CONTENTENCRYPTIONEX \_ pour MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="f1119-104">MF\_PD\_ASF\_CONTENTENCRYPTIONEX\_ENCRYPTION\_DATA attribute</span></span>

<span data-ttu-id="f1119-105">Contient des données de chiffrement pour un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="f1119-105">Contains encryption data for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="f1119-106">Cet attribut correspond à l’objet de chiffrement de contenu étendu dans l’en-tête ASF, défini dans la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="f1119-106">This attribute corresponds to the Extended Content Encryption Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="f1119-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="f1119-107">Data type</span></span>

<span data-ttu-id="f1119-108">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="f1119-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="f1119-109">Notes</span><span class="sxs-lookup"><span data-stu-id="f1119-109">Remarks</span></span>

<span data-ttu-id="f1119-110">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="f1119-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="f1119-111">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crée le descripteur de présentation et génère cet attribut à partir de l’en-tête d’objet de chiffrement de contenu étendu.</span><span class="sxs-lookup"><span data-stu-id="f1119-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Extended Content Encryption Object header.</span></span> <span data-ttu-id="f1119-112">La taille de l’objet blob est égale au champ de la taille des données.</span><span class="sxs-lookup"><span data-stu-id="f1119-112">The size of the blob equals the Data Size field.</span></span> <span data-ttu-id="f1119-113">Le tableau d’octets contenu dans l’objet blob est égal au champ de données de l’objet de chiffrement de contenu étendu de l’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="f1119-113">The byte array contained in the blob equals the Data field in the Extended Content Encryption object of the ASF header.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1119-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1119-114">Requirements</span></span>



| <span data-ttu-id="f1119-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1119-115">Requirement</span></span> | <span data-ttu-id="f1119-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1119-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1119-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1119-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f1119-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1119-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f1119-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1119-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f1119-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1119-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f1119-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1119-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1119-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1119-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1119-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1119-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1119-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1119-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f1119-125">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="f1119-125">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="f1119-126">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="f1119-126">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="f1119-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f1119-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f1119-128">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="f1119-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f1119-129">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="f1119-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f1119-130">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="f1119-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




