---
description: Spécifie si les flux audio d’une présentation ont une vitesse de transmission variable.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: Attribut MF_PD_AUDIO_ISVARIABLEBITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a34d3dd64f9100050dc9aae37e811d00c9d58af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203717"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a><span data-ttu-id="d2647-103">\_Attribut ISVARIABLEBITRATE de l’audio MF PD \_ \_</span><span class="sxs-lookup"><span data-stu-id="d2647-103">MF\_PD\_AUDIO\_ISVARIABLEBITRATE attribute</span></span>

<span data-ttu-id="d2647-104">Spécifie si les flux audio d’une présentation ont une vitesse de transmission variable.</span><span class="sxs-lookup"><span data-stu-id="d2647-104">Specifies whether the audio streams in a presentation have a variable bit rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="d2647-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d2647-105">Data type</span></span>

<span data-ttu-id="d2647-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d2647-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d2647-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="d2647-107">Get/set</span></span>

<span data-ttu-id="d2647-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d2647-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d2647-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="d2647-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d2647-110">S'applique à</span><span class="sxs-lookup"><span data-stu-id="d2647-110">Applies To</span></span>

[<span data-ttu-id="d2647-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d2647-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="d2647-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d2647-112">Remarks</span></span>

<span data-ttu-id="d2647-113">Il s’agit d’un attribut facultatif pour les descripteurs de présentation.</span><span class="sxs-lookup"><span data-stu-id="d2647-113">This is an optional attribute for presentation descriptors.</span></span> <span data-ttu-id="d2647-114">Si l’attribut a la **valeur true** (différente de zéro), la présentation contient au moins un flux audio VBR (variable-bit-rate).</span><span class="sxs-lookup"><span data-stu-id="d2647-114">If the attribute is **TRUE** (nonzero), the presentation contains at least one variable-bit-rate (VBR) audio stream.</span></span> <span data-ttu-id="d2647-115">Si l’attribut a la **valeur false**, tous les flux audio ont une vitesse de transmission constante.</span><span class="sxs-lookup"><span data-stu-id="d2647-115">If the attribute is **FALSE**, all of the audio streams have a constant bit rate.</span></span>

<span data-ttu-id="d2647-116">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d2647-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2647-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2647-117">Requirements</span></span>



| <span data-ttu-id="d2647-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2647-118">Requirement</span></span> | <span data-ttu-id="d2647-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2647-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2647-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2647-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d2647-121">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d2647-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d2647-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2647-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d2647-123">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d2647-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d2647-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2647-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2647-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2647-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2647-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2647-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2647-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2647-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d2647-128">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="d2647-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




