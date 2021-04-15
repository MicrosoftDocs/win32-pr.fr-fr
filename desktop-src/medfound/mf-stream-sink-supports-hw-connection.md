---
description: Indique si un récepteur multimédia prend en charge le workflow de données matérielles.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: Attribut MF_STREAM_SINK_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485208"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a><span data-ttu-id="5721a-103">Le \_ récepteur de flux MF \_ \_ prend en charge l' \_ attribut de \_ connexion matérielle</span><span class="sxs-lookup"><span data-stu-id="5721a-103">MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="5721a-104">Indique si un récepteur multimédia prend en charge le workflow de données matérielles.</span><span class="sxs-lookup"><span data-stu-id="5721a-104">Indicates whether a media sink supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="5721a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5721a-105">Data type</span></span>

<span data-ttu-id="5721a-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5721a-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5721a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5721a-107">Remarks</span></span>

<span data-ttu-id="5721a-108">Cet attribut est utilisé lorsqu’un récepteur multimédia transmet un périphérique matériel et est en mesure de recevoir des données sur un bus matériel.</span><span class="sxs-lookup"><span data-stu-id="5721a-108">This attribute is used when a media sink proxies a hardware device and is able to receive data over a hardware bus.</span></span> <span data-ttu-id="5721a-109">Par exemple, un décodeur audio matériel peut envoyer des données audio directement au matériel de rendu audio.</span><span class="sxs-lookup"><span data-stu-id="5721a-109">For example, a hardware audio decoder might send audio data directly to the audio rendering hardware.</span></span>

<span data-ttu-id="5721a-110">Dans ce scénario, le décodeur et le récepteur sont toujours représentés dans le Microsoft Media Foundation par une [transformation de Media Foundation](media-foundation-transforms.md) (MFT) et un récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="5721a-110">In this scenario, the decoder and the sink are still represented in the Microsoft Media Foundation by a [Media Foundation transform](media-foundation-transforms.md) (MFT) and a media sink.</span></span> <span data-ttu-id="5721a-111">Toutefois, il n’y a pas de flux de données entre ces deux objets au niveau de la couche de pipeline, uniquement au niveau de la couche matérielle, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="5721a-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![diagramme qui montre une source de proxy matériel.](images/proxy-mft4.png)

<span data-ttu-id="5721a-113">La connexion entre la table MFT et le récepteur multimédia est négociée comme suit.</span><span class="sxs-lookup"><span data-stu-id="5721a-113">The connection between the MFT and the media sink is negotiated as follows.</span></span>

1.  <span data-ttu-id="5721a-114">Le pipeline vérifie si la MFT est un proxy matériel, en vérifiant l’attribut d' [ \_ \_ \_ \_ attribut d’URL matériel de l’énumération MFT](mft-enum-hardware-url-attribute.md) sur la table MFT.</span><span class="sxs-lookup"><span data-stu-id="5721a-114">The pipeline checks if the MFT is a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="5721a-115">Pour plus d’informations, consultez [Hardware MFTS](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="5721a-115">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="5721a-116">Le pipeline obtient un pointeur vers l’interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) du récepteur de flux sur le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="5721a-116">The pipeline gets a pointer to the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface of the stream sink on the media sink.</span></span>
3.  <span data-ttu-id="5721a-117">Le pipeline utilise le pointeur [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pour interroger le \_ récepteur de flux MF \_ \_ prend en charge l' \_ attribut de \_ connexion matérielle.</span><span class="sxs-lookup"><span data-stu-id="5721a-117">The pipeline uses the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer to query for the MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="5721a-118">Si cet attribut est présent et qu’il est égal à **true**, la source du média prend en charge les connexions matérielles.</span><span class="sxs-lookup"><span data-stu-id="5721a-118">If this attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="5721a-119">Le pipeline définit l’attribut d' [ \_ \_ \_ attribut de flux connecté MFT](mft-connected-stream-attribute.md) sur le récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="5721a-119">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the stream sink.</span></span> <span data-ttu-id="5721a-120">La valeur de cet attribut est le pointeur [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) à partir de la table MFT.</span><span class="sxs-lookup"><span data-stu-id="5721a-120">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer from the MFT.</span></span>
5.  <span data-ttu-id="5721a-121">Le pipeline affecte la **valeur true** à l’attribut [MFT \_ Connected \_ to \_ HW \_ Stream](mft-connected-to-hw-stream.md) à la fois dans le récepteur de flux et dans la table MFT.</span><span class="sxs-lookup"><span data-stu-id="5721a-121">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the stream sink and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="5721a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5721a-122">Requirements</span></span>



| <span data-ttu-id="5721a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5721a-123">Requirement</span></span> | <span data-ttu-id="5721a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5721a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5721a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5721a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5721a-126">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5721a-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="5721a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5721a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5721a-128">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="5721a-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5721a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5721a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5721a-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5721a-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5721a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5721a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5721a-132">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5721a-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




