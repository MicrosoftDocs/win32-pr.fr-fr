---
description: Spécifie la taille moyenne de la mémoire tampon, en octets, nécessaire pour un flux dans un fichier ASF (Advanced Systems Format).
ms.assetid: 9e9259a2-6fb7-4a24-8d14-841f2cc8c3ef
title: Attribut MF_SD_ASF_EXTSTRMPROP_AVG_BUFFERSIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c3fc186c2c07ccff1993f1db07d89150a98541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866185"
---
# <a name="mf_sd_asf_extstrmprop_avg_buffersize-attribute"></a><span data-ttu-id="bc487-103">MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Moy \_ attribut de tampon</span><span class="sxs-lookup"><span data-stu-id="bc487-103">MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE attribute</span></span>

<span data-ttu-id="bc487-104">Spécifie la taille moyenne de la mémoire tampon, en octets, nécessaire pour un flux dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="bc487-104">Specifies the average buffer size, in bytes, needed for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="bc487-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="bc487-105">Data type</span></span>

<span data-ttu-id="bc487-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bc487-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bc487-107">Notes</span><span class="sxs-lookup"><span data-stu-id="bc487-107">Remarks</span></span>

<span data-ttu-id="bc487-108">Cet attribut s’applique aux descripteurs de flux pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="bc487-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="bc487-109">Il correspond au champ Taille de la mémoire tampon de l’objet propriétés de flux étendus et définit la taille de compartiment utilisée dans le modèle « compartiment perdu ».</span><span class="sxs-lookup"><span data-stu-id="bc487-109">It corresponds to the Buffer Size field in the Extended Stream Properties object, and defines the bucket size used in the "leaky bucket" model.</span></span> <span data-ttu-id="bc487-110">Pour plus d’informations, reportez-vous à la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="bc487-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="bc487-111">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="bc487-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="bc487-112">L’application peut créer le descripteur de flux du flux à partir du descripteur de présentation en appelant [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="bc487-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc487-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc487-113">Requirements</span></span>



| <span data-ttu-id="bc487-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc487-114">Requirement</span></span> | <span data-ttu-id="bc487-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc487-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc487-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc487-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc487-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc487-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bc487-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc487-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc487-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc487-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bc487-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc487-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc487-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc487-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc487-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc487-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc487-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bc487-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bc487-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bc487-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="bc487-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bc487-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="bc487-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="bc487-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="bc487-127">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="bc487-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="bc487-128">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="bc487-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




