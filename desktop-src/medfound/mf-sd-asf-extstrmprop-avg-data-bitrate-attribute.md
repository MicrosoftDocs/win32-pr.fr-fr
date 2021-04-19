---
description: Spécifie la vitesse moyenne de transmission de données, en bits par seconde, d’un flux dans un fichier ASF (Advanced Systems Format).
ms.assetid: 3a0b39ab-e9a9-49df-a321-a88559aec16f
title: Attribut MF_SD_ASF_EXTSTRMPROP_AVG_DATA_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18789fbd18f063c59de712cf1b1b6bdac1c38a5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521278"
---
# <a name="mf_sd_asf_extstrmprop_avg_data_bitrate-attribute"></a><span data-ttu-id="2f147-103">\_Attribut de \_ Vitesse \_ de \_ \_ transmission de données Moy \_ SD ASF EXTSTRMPROP</span><span class="sxs-lookup"><span data-stu-id="2f147-103">MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE attribute</span></span>

<span data-ttu-id="2f147-104">Spécifie la vitesse moyenne de transmission de données, en bits par seconde, d’un flux dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2f147-104">Specifies the average data bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="2f147-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2f147-105">Data type</span></span>

<span data-ttu-id="2f147-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2f147-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2f147-107">Notes</span><span class="sxs-lookup"><span data-stu-id="2f147-107">Remarks</span></span>

<span data-ttu-id="2f147-108">Cet attribut s’applique aux descripteurs de flux pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="2f147-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="2f147-109">Il correspond au champ vitesse de transmission de données dans l’objet de propriétés de flux étendu et définit le taux de fuite utilisé dans le modèle « compartiment perdu ».</span><span class="sxs-lookup"><span data-stu-id="2f147-109">It corresponds to the Data Bit Rate field in the Extended Stream Properties object, and defines the leak rate used in the "leaky bucket" model.</span></span> <span data-ttu-id="2f147-110">Pour plus d’informations, reportez-vous à la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="2f147-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="2f147-111">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="2f147-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="2f147-112">L’application peut créer le descripteur de flux du flux à partir du descripteur de présentation en appelant [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="2f147-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f147-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f147-113">Requirements</span></span>



| <span data-ttu-id="2f147-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f147-114">Requirement</span></span> | <span data-ttu-id="2f147-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f147-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f147-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f147-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2f147-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f147-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2f147-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f147-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2f147-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f147-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2f147-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f147-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f147-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f147-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f147-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f147-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f147-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f147-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f147-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2f147-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2f147-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2f147-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2f147-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2f147-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="2f147-127">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="2f147-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f147-128">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="2f147-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




