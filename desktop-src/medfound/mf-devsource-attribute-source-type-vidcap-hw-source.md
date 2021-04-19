---
description: Spécifie si une source de capture vidéo est un périphérique matériel ou un périphérique logiciel.
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e816e668267a23e67e7450b81a32cde454315bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544250"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a><span data-ttu-id="a512d-103">TYPE de source de l' \_ attribut MF DEVSOURCE VIDCAP de l' \_ \_ \_ \_ \_ \_ attribut source HW</span><span class="sxs-lookup"><span data-stu-id="a512d-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_HW\_SOURCE attribute</span></span>

<span data-ttu-id="a512d-104">Spécifie si une source de capture vidéo est un périphérique matériel ou un périphérique logiciel.</span><span class="sxs-lookup"><span data-stu-id="a512d-104">Specifies whether a video capture source is a hardware device or a software device.</span></span>

## <a name="data-type"></a><span data-ttu-id="a512d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a512d-105">Data type</span></span>

<span data-ttu-id="a512d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a512d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a512d-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="a512d-107">Get/set</span></span>

<span data-ttu-id="a512d-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a512d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a512d-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a512d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="a512d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a512d-110">Remarks</span></span>

<span data-ttu-id="a512d-111">Si la valeur est **true**, la source de capture est un périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="a512d-111">If the value is **TRUE**, the capture source is a hardware device.</span></span> <span data-ttu-id="a512d-112">Si la valeur est **false**, il s’agit d’un périphérique logiciel.</span><span class="sxs-lookup"><span data-stu-id="a512d-112">If the value is **FALSE**, it is a software device.</span></span> <span data-ttu-id="a512d-113">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a512d-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="a512d-114">Cet attribut est défini sur les objets d’activation retournés par les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a512d-114">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="a512d-115">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="a512d-115">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="a512d-116">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="a512d-116">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="a512d-117">L’attribut s’applique uniquement aux périphériques de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="a512d-117">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="a512d-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a512d-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a512d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a512d-119">Requirements</span></span>



| <span data-ttu-id="a512d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a512d-120">Requirement</span></span> | <span data-ttu-id="a512d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a512d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a512d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a512d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a512d-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a512d-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a512d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a512d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a512d-125">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a512d-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a512d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a512d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a512d-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a512d-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a512d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a512d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a512d-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a512d-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a512d-130">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="a512d-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="a512d-131">Capturer les attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a512d-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




