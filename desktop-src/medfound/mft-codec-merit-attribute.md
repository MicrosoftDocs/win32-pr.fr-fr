---
description: Contient la valeur mérite d’un codec matériel.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: Attribut MFT_CODEC_MERIT_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542912"
---
# <a name="mft_codec_merit_attribute-attribute"></a><span data-ttu-id="f47bc-103">\_Attribut de \_ mérite du codec MFT \_</span><span class="sxs-lookup"><span data-stu-id="f47bc-103">MFT\_CODEC\_MERIT\_Attribute attribute</span></span>

<span data-ttu-id="f47bc-104">Contient la valeur mérite d’un codec matériel.</span><span class="sxs-lookup"><span data-stu-id="f47bc-104">Contains the merit value of a hardware codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="f47bc-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f47bc-105">Data type</span></span>

<span data-ttu-id="f47bc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f47bc-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f47bc-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="f47bc-107">Get/set</span></span>

<span data-ttu-id="f47bc-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f47bc-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f47bc-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f47bc-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f47bc-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f47bc-110">Remarks</span></span>

<span data-ttu-id="f47bc-111">Cet attribut est défini sur l’objet d’activation d’une Media Foundation transformation (MFT) qui représente un codec matériel.</span><span class="sxs-lookup"><span data-stu-id="f47bc-111">This attribute is set on the activation object for a Media Foundation transform (MFT) that represents a hardware codec.</span></span> <span data-ttu-id="f47bc-112">La valeur de l’attribut est la valeur mérite du codec.</span><span class="sxs-lookup"><span data-stu-id="f47bc-112">The value of the attribute is the codec's merit value.</span></span>

<span data-ttu-id="f47bc-113">Cet attribut contrôle l’ordre dans lequel la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) énumère les codecs, si l’indicateur d' **\_ énumération MFT \_ \_ SORTANDFILTER** est défini.</span><span class="sxs-lookup"><span data-stu-id="f47bc-113">This attribute controls the order in which the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function enumerates codecs, if the **MFT\_ENUM\_FLAG\_SORTANDFILTER** flag is set.</span></span> <span data-ttu-id="f47bc-114">MFTs avec une valeur mérite apparaît plus haut dans la liste que les autres MFTs.</span><span class="sxs-lookup"><span data-stu-id="f47bc-114">MFTs with a merit value appear higher in the list than other MFTs.</span></span>

<span data-ttu-id="f47bc-115">Cet attribut ne contient pas de valeur approuvée.</span><span class="sxs-lookup"><span data-stu-id="f47bc-115">This attribute does not contain a trusted value.</span></span> <span data-ttu-id="f47bc-116">Pour vérifier la valeur réelle de mérite du codec, appelez la fonction [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .</span><span class="sxs-lookup"><span data-stu-id="f47bc-116">To verify the codec's actual merit value, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span>

<span data-ttu-id="f47bc-117">Si la valeur de l' \_ attribut d' \_ attribut mérite du codec MFT \_ ne correspond pas à la valeur mérite récupérée par [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) échoue et retourne **MF \_ E \_ non valide \_ codec \_ mérite**.</span><span class="sxs-lookup"><span data-stu-id="f47bc-117">If the value of the MFT\_CODEC\_MERIT\_Attribute attribute does not match the merit value retrieved by [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails and returns **MF\_E\_INVALID\_CODEC\_MERIT**.</span></span>

<span data-ttu-id="f47bc-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f47bc-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f47bc-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f47bc-119">Requirements</span></span>



| <span data-ttu-id="f47bc-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f47bc-120">Requirement</span></span> | <span data-ttu-id="f47bc-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f47bc-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f47bc-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f47bc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f47bc-123">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f47bc-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f47bc-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f47bc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f47bc-125">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f47bc-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f47bc-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f47bc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f47bc-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="f47bc-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f47bc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f47bc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47bc-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f47bc-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f47bc-130">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="f47bc-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




