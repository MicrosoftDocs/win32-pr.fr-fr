---
description: Indique si une source de média prend en charge le workflow de données matérielles.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: Attribut MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539121"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a><span data-ttu-id="2bcb3-103">Le \_ flux source MF \_ \_ prend en charge l' \_ attribut de \_ connexion HW</span><span class="sxs-lookup"><span data-stu-id="2bcb3-103">MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="2bcb3-104">Indique si une source de média prend en charge le workflow de données matérielles.</span><span class="sxs-lookup"><span data-stu-id="2bcb3-104">Indicates whether a media source supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="2bcb3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2bcb3-105">Data type</span></span>

<span data-ttu-id="2bcb3-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bcb3-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2bcb3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="2bcb3-107">Remarks</span></span>

<span data-ttu-id="2bcb3-108">Cet attribut est utilisé quand une source de média transmet un périphérique matériel et est en mesure de transférer des données en aval sur un bus matériel, sans envoyer de données jusqu’au processeur.</span><span class="sxs-lookup"><span data-stu-id="2bcb3-108">This attribute is used when a media source proxies a hardware device and is able to transfer data downstream over a hardware bus, without sending data up to the CPU.</span></span> <span data-ttu-id="2bcb3-109">Par exemple, une webcam peut fournir une vidéo encodée H. 264 directement à un décodeur matériel intégré.</span><span class="sxs-lookup"><span data-stu-id="2bcb3-109">For example, a webcam might deliver H.264-encoded video directly to an integrated hardware decoder.</span></span>

<span data-ttu-id="2bcb3-110">Dans ce scénario, la source et le décodeur sont toujours représentés dans le Microsoft Media Foundation par un objet de [source multimédia](media-sources.md) et une table de [Media Foundation de transformation](media-foundation-transforms.md) (MFT).</span><span class="sxs-lookup"><span data-stu-id="2bcb3-110">In this scenario, the source and decoder are still represented in the Microsoft Media Foundation by a [media source](media-sources.md) object and a [Media Foundation transform](media-foundation-transforms.md) (MFT).</span></span> <span data-ttu-id="2bcb3-111">Toutefois, il n’y a pas de flux de données entre ces deux objets au niveau de la couche de pipeline, uniquement au niveau de la couche matérielle, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="2bcb3-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![diagramme qui montre une source de proxy matériel.](images/proxy-mft3.png)

<span data-ttu-id="2bcb3-113">La connexion entre la source du média et la table MFT est négociée comme suit.</span><span class="sxs-lookup"><span data-stu-id="2bcb3-113">The connection between the media source and the MFT is negotiated as follows.</span></span>

1.  <span data-ttu-id="2bcb3-114">Le pipeline interroge la source du média pour l’interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="2bcb3-114">The pipeline queries the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span> <span data-ttu-id="2bcb3-115">(Cette interface est facultative pour la prise en charge des sources multimédias.)</span><span class="sxs-lookup"><span data-stu-id="2bcb3-115">(This interface is optional for media sources to support.)</span></span>
2.  <span data-ttu-id="2bcb3-116">Le pipeline appelle [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="2bcb3-116">The pipeline calls [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
3.  <span data-ttu-id="2bcb3-117">Les requêtes de pipeline pour \_ le \_ flux source MF \_ prennent en charge l' \_ attribut de connexion HW \_ .</span><span class="sxs-lookup"><span data-stu-id="2bcb3-117">The pipeline queries for the MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="2bcb3-118">Si l’attribut est présent et qu’il est égal à **true**, la source du média prend en charge les connexions matérielles.</span><span class="sxs-lookup"><span data-stu-id="2bcb3-118">If the attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="2bcb3-119">Le pipeline vérifie si la MFT est également un proxy matériel, en vérifiant l’attribut d' [ \_ \_ \_ \_ attribut d’URL matériel de l’énumération MFT](mft-enum-hardware-url-attribute.md) sur la table MFT.</span><span class="sxs-lookup"><span data-stu-id="2bcb3-119">The pipeline checks if the MFT is also a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="2bcb3-120">Pour plus d’informations, consultez [Hardware MFTS](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="2bcb3-120">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
5.  <span data-ttu-id="2bcb3-121">Le pipeline définit l’attribut d' [ \_ \_ \_ attribut de flux connecté MFT](mft-connected-stream-attribute.md) sur la table MFT.</span><span class="sxs-lookup"><span data-stu-id="2bcb3-121">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="2bcb3-122">La valeur de cet attribut est le pointeur [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) obtenu à partir de la source du média à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="2bcb3-122">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer obtained from the media source in step 2.</span></span>
6.  <span data-ttu-id="2bcb3-123">Le pipeline affecte la **valeur true** à la [table MFT \_ connectée à l’attribut de \_ \_ \_ flux matériel](mft-connected-to-hw-stream.md) à la fois à la source du média et à la table MFT.</span><span class="sxs-lookup"><span data-stu-id="2bcb3-123">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the media source and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bcb3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bcb3-124">Requirements</span></span>



| <span data-ttu-id="2bcb3-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bcb3-125">Requirement</span></span> | <span data-ttu-id="2bcb3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bcb3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2bcb3-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bcb3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2bcb3-128">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2bcb3-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2bcb3-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bcb3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2bcb3-130">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="2bcb3-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2bcb3-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="2bcb3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bcb3-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bcb3-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bcb3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bcb3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bcb3-134">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2bcb3-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2bcb3-135">Matériel MFTs</span><span class="sxs-lookup"><span data-stu-id="2bcb3-135">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> </dl>

 

 




