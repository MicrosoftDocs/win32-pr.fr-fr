---
description: Spécifie le rôle d’appareil pour un périphérique de capture audio.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034212"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a><span data-ttu-id="711f3-103">Attribut \_ de \_ \_ \_ \_ rôle AUDCAP du type de source de l’attribut DEVSOURCE \_ MF</span><span class="sxs-lookup"><span data-stu-id="711f3-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ROLE attribute</span></span>

<span data-ttu-id="711f3-104">Spécifie le rôle d’appareil pour un périphérique de capture audio.</span><span class="sxs-lookup"><span data-stu-id="711f3-104">Specifies the device role for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="711f3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="711f3-105">Data type</span></span>

<span data-ttu-id="711f3-106">**ERole** stocké en tant que **UInt32**</span><span class="sxs-lookup"><span data-stu-id="711f3-106">**ERole** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="711f3-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="711f3-107">Get/set</span></span>

<span data-ttu-id="711f3-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="711f3-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="711f3-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="711f3-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="711f3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="711f3-110">Remarks</span></span>

<span data-ttu-id="711f3-111">Le type d’énumération **eRole** est documenté dans la documentation de l’API audio principale.</span><span class="sxs-lookup"><span data-stu-id="711f3-111">The **eRole** enumeration type is documented in the Core Audio API documentation.</span></span>

<span data-ttu-id="711f3-112">La valeur de l’attribut spécifie un rôle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="711f3-112">The value of the attribute specifies a device role.</span></span> <span data-ttu-id="711f3-113">Cet attribut est utilisé avec les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="711f3-113">This attribute is used with the following functions.</span></span>

<span data-ttu-id="711f3-114">Cet attribut peut être utilisé comme entrée pour les fonctions [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) et [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="711f3-114">This attribute can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="711f3-115">Si l’attribut est spécifié, la fonction crée une source de média qui utilise le périphérique de capture audio par défaut pour le rôle d’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="711f3-115">If the attribute is specified, the function creates a media source that uses the default audio capture device for the specified device role.</span></span>

<span data-ttu-id="711f3-116">Cet attribut peut également être utilisé comme entrée de la fonction [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="711f3-116">This attribute can also be used as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="711f3-117">Si l’attribut est spécifié, l’énumération est limitée au rôle d’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="711f3-117">If the attribute is specified, the enumeration is restricted to the specified device role.</span></span> <span data-ttu-id="711f3-118">En outre, chaque objet d’activation retourné par la fonction **MFEnumDeviceSources** contient cet attribut.</span><span class="sxs-lookup"><span data-stu-id="711f3-118">In addition, each activation object returned by the **MFEnumDeviceSources** function contains this attribute.</span></span> <span data-ttu-id="711f3-119">L’attribut est ensuite utilisé en interne par l’objet d’activation lorsqu’il crée la source du média.</span><span class="sxs-lookup"><span data-stu-id="711f3-119">The attribute is then used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="711f3-120">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="711f3-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="711f3-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="711f3-121">Requirements</span></span>



| <span data-ttu-id="711f3-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="711f3-122">Requirement</span></span> | <span data-ttu-id="711f3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="711f3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="711f3-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="711f3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="711f3-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="711f3-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="711f3-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="711f3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="711f3-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="711f3-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="711f3-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="711f3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="711f3-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="711f3-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="711f3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="711f3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711f3-131">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="711f3-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="711f3-132">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="711f3-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="711f3-133">Capturer les attributs de l’appareil</span><span class="sxs-lookup"><span data-stu-id="711f3-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




