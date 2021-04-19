---
description: Spécifie si une source de périphérique matériel utilise l’heure système pour les horodatages.
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: Attribut MFT_HW_TIMESTAMP_WITH_QPC_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f6f7d50db89e99e76e7b7ea509f444c3998bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520487"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a><span data-ttu-id="20b7a-103">\_Horodateur de la MFT HW \_ \_ avec \_ attribut d' \_ attribut QPC</span><span class="sxs-lookup"><span data-stu-id="20b7a-103">MFT\_HW\_TIMESTAMP\_WITH\_QPC\_Attribute attribute</span></span>

<span data-ttu-id="20b7a-104">Spécifie si une source de périphérique matériel utilise l’heure système pour les horodatages.</span><span class="sxs-lookup"><span data-stu-id="20b7a-104">Specifies whether a hardware device source uses the system time for time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="20b7a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="20b7a-105">Data type</span></span>

<span data-ttu-id="20b7a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="20b7a-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="20b7a-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="20b7a-107">Get/set</span></span>

<span data-ttu-id="20b7a-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="20b7a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="20b7a-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="20b7a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="20b7a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="20b7a-110">Remarks</span></span>

<span data-ttu-id="20b7a-111">Si cet attribut a la **valeur true**, la source de l’appareil utilise l’heure système, telle qu’elle est retournée par le **QueryPerformanceCounter**, pour les horodatages.</span><span class="sxs-lookup"><span data-stu-id="20b7a-111">If this attribute is **TRUE**, the device source uses the system time, as returned by the **QueryPerformanceCounter**, for time stamps.</span></span> <span data-ttu-id="20b7a-112">Dans le cas contraire, la source de l’appareil utilise l’horloge de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="20b7a-112">Otherwise, the device source uses the device's clock.</span></span> <span data-ttu-id="20b7a-113">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="20b7a-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="20b7a-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="20b7a-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="20b7a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20b7a-115">Requirements</span></span>



| <span data-ttu-id="20b7a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20b7a-116">Requirement</span></span> | <span data-ttu-id="20b7a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="20b7a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20b7a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20b7a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="20b7a-119">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="20b7a-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="20b7a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20b7a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="20b7a-121">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="20b7a-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="20b7a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="20b7a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="20b7a-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="20b7a-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20b7a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20b7a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b7a-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20b7a-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="20b7a-126">Capturer les attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="20b7a-126">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




