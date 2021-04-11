---
description: Spécifie la catégorie d’appareil pour un périphérique de capture vidéo.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc65af267df38486f6ad7859d16aff4de5973a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113670"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a><span data-ttu-id="8a062-103">Attribut de catégorie de la source de l' \_ attribut DEVSOURCE MF \_ \_ \_ \_ VIDCAP \_</span><span class="sxs-lookup"><span data-stu-id="8a062-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_CATEGORY attribute</span></span>

<span data-ttu-id="8a062-104">Spécifie la catégorie d’appareil pour un périphérique de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="8a062-104">Specifies the device category for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="8a062-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8a062-105">Data type</span></span>

<span data-ttu-id="8a062-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="8a062-106">**GUID**</span></span>

<span data-ttu-id="8a062-107">La valeur suivante est définie.</span><span class="sxs-lookup"><span data-stu-id="8a062-107">The following value is defined.</span></span>



| <span data-ttu-id="8a062-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a062-108">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="8a062-109">Signification</span><span class="sxs-lookup"><span data-stu-id="8a062-109">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <span data-ttu-id="8a062-110"><dt>**CLSID \_ VideoInputDeviceCategory**</dt></span><span class="sxs-lookup"><span data-stu-id="8a062-110"><dt>**CLSID\_VideoInputDeviceCategory**</dt></span></span> </dl> | <span data-ttu-id="8a062-111">Périphérique de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="8a062-111">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="8a062-112">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="8a062-112">Get/set</span></span>

<span data-ttu-id="8a062-113">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="8a062-113">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="8a062-114">Pour définir cet attribut, appelez [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="8a062-114">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a062-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8a062-115">Remarks</span></span>

<span data-ttu-id="8a062-116">Utilisez cet attribut comme entrée pour la fonction [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) lors de l’énumération des périphériques de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="8a062-116">Use this attribute as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function when enumerating video capture devices.</span></span>

<span data-ttu-id="8a062-117">En outre, cet attribut est défini sur les objets d’activation retournés par les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a062-117">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="8a062-118">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="8a062-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="8a062-119">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="8a062-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="8a062-120">L’attribut s’applique uniquement aux périphériques de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="8a062-120">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="8a062-121">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8a062-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a062-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a062-122">Requirements</span></span>



| <span data-ttu-id="8a062-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a062-123">Requirement</span></span> | <span data-ttu-id="8a062-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a062-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a062-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a062-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8a062-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a062-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8a062-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a062-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8a062-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a062-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8a062-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a062-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a062-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a062-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a062-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a062-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a062-132">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8a062-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8a062-133">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="8a062-133">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="8a062-134">Capturer les attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="8a062-134">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




