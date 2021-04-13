---
description: Contient des données secrètes pour un fichier ASF (Advanced Systems Format) chiffré. Cet attribut correspond au champ de données secrètes de l’en-tête de chiffrement de contenu, défini dans la spécification ASF.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: Attribut MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28c960131e61e539fa417e1068b45974a24c42a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526001"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a><span data-ttu-id="a5e9b-104">\_Attribut de \_ \_ données de \_ secret CONTENTENCRYPTION pour MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="a5e9b-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_SECRET\_DATA attribute</span></span>

<span data-ttu-id="a5e9b-105">Contient des données secrètes pour un fichier ASF (Advanced Systems Format) chiffré.</span><span class="sxs-lookup"><span data-stu-id="a5e9b-105">Contains secret data for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="a5e9b-106">Cet attribut correspond au champ de données secrètes de l’en-tête de chiffrement de contenu, défini dans la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="a5e9b-106">This attribute corresponds to the Secret Data field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5e9b-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="a5e9b-107">Data type</span></span>

<span data-ttu-id="a5e9b-108">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="a5e9b-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="a5e9b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a5e9b-109">Remarks</span></span>

<span data-ttu-id="a5e9b-110">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="a5e9b-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="a5e9b-111">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) remplit un tableau d’octets avec le champ de données de secret.</span><span class="sxs-lookup"><span data-stu-id="a5e9b-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method populates a byte array with the Secret Data field.</span></span> <span data-ttu-id="a5e9b-112">La taille du tableau est égale au champ de la longueur des données secrètes de l’en-tête de chiffrement du contenu.</span><span class="sxs-lookup"><span data-stu-id="a5e9b-112">The size of the array equals the Secret Data Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5e9b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5e9b-113">Requirements</span></span>



| <span data-ttu-id="a5e9b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5e9b-114">Requirement</span></span> | <span data-ttu-id="a5e9b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5e9b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e9b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5e9b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e9b-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5e9b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a5e9b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5e9b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a5e9b-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5e9b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a5e9b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5e9b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5e9b-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5e9b-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5e9b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5e9b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e9b-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5e9b-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5e9b-124">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="a5e9b-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a5e9b-125">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="a5e9b-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="a5e9b-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a5e9b-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a5e9b-127">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="a5e9b-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5e9b-128">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="a5e9b-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="a5e9b-129">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="a5e9b-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




