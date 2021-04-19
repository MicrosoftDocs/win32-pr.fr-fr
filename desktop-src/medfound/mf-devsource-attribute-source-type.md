---
description: Spécifie un type d’appareil, tel que la capture audio ou la capture vidéo.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524897"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a><span data-ttu-id="cf1af-103">Attribut de type de source de l' \_ attribut DEVSOURCE MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="cf1af-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE attribute</span></span>

<span data-ttu-id="cf1af-104">Spécifie le type d’un appareil, tel que la capture audio ou la capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="cf1af-104">Specifies a device's type, such as audio capture or video capture.</span></span>

## <a name="data-type"></a><span data-ttu-id="cf1af-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="cf1af-105">Data type</span></span>

<span data-ttu-id="cf1af-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="cf1af-106">**GUID**</span></span>

<span data-ttu-id="cf1af-107">Les valeurs suivantes sont définies pour cet attribut :</span><span class="sxs-lookup"><span data-stu-id="cf1af-107">The following values are defined for this attribute:</span></span>



| <span data-ttu-id="cf1af-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf1af-108">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="cf1af-109">Signification</span><span class="sxs-lookup"><span data-stu-id="cf1af-109">Meaning</span></span>                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <span data-ttu-id="cf1af-110"><dt>**TYPE de source de l' \_ attribut DEVSOURCE MF \_ \_ \_ \_ AUDCAP \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="cf1af-110"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="cf1af-111">Périphérique de capture audio.</span><span class="sxs-lookup"><span data-stu-id="cf1af-111">Audio capture device.</span></span><br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <span data-ttu-id="cf1af-112"><dt>**TYPE de source de l' \_ attribut DEVSOURCE MF \_ \_ \_ \_ VIDCAP \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="cf1af-112"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="cf1af-113">Périphérique de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="cf1af-113">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="cf1af-114">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="cf1af-114">Get/set</span></span>

<span data-ttu-id="cf1af-115">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="cf1af-115">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="cf1af-116">Pour définir cet attribut, appelez [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="cf1af-116">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf1af-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cf1af-117">Remarks</span></span>

<span data-ttu-id="cf1af-118">Utilisez cet attribut comme entrée pour les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf1af-118">Use this attribute as input to the following functions:</span></span>

-   [<span data-ttu-id="cf1af-119">**MFCreateDeviceSource**</span><span class="sxs-lookup"><span data-stu-id="cf1af-119">**MFCreateDeviceSource**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [<span data-ttu-id="cf1af-120">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="cf1af-120">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="cf1af-121">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="cf1af-121">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="cf1af-122">En outre, cet attribut est défini sur les objets d’activation retournés par la fonction [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="cf1af-122">In addition, this attribute is set on the activation objects returned by the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span>

<span data-ttu-id="cf1af-123">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cf1af-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf1af-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf1af-124">Requirements</span></span>



| <span data-ttu-id="cf1af-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf1af-125">Requirement</span></span> | <span data-ttu-id="cf1af-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf1af-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1af-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf1af-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cf1af-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf1af-128">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cf1af-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf1af-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cf1af-130">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf1af-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cf1af-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf1af-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf1af-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf1af-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf1af-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf1af-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf1af-134">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cf1af-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cf1af-135">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="cf1af-135">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="cf1af-136">Capturer les attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="cf1af-136">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




