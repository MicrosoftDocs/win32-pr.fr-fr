---
description: Contient un pointeur vers les attributs de flux du flux connecté sur une table de Media Foundation matérielle (MFT).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: Attribut MFT_CONNECTED_STREAM_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863962"
---
# <a name="mft_connected_stream_attribute-attribute"></a><span data-ttu-id="a562f-103">Attribut de l' \_ \_ attribut de flux connecté MFT \_</span><span class="sxs-lookup"><span data-stu-id="a562f-103">MFT\_CONNECTED\_STREAM\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="a562f-104">Contient un pointeur vers les attributs de flux du flux connecté sur une table de Media Foundation matérielle (MFT).</span><span class="sxs-lookup"><span data-stu-id="a562f-104">Contains a pointer to the stream attributes of the connected stream on a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="a562f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a562f-105">Data type</span></span>

<span data-ttu-id="a562f-106">**IMFAttributes \** _ stocké en tant que _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="a562f-106">**IMFAttributes\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="a562f-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="a562f-107">Get/set</span></span>

<span data-ttu-id="a562f-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="a562f-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="a562f-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="a562f-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="a562f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a562f-110">Remarks</span></span>

<span data-ttu-id="a562f-111">En général, les applications n’utilisent pas cet attribut.</span><span class="sxs-lookup"><span data-stu-id="a562f-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="a562f-112">Cet attribut est utilisé pour les MFTs qui agissent en tant que proxys sur un périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="a562f-112">This attribute is used for MFTs that act as proxies to a hardware device.</span></span> <span data-ttu-id="a562f-113">Pour plus d’informations, consultez [Hardware MFTS](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="a562f-113">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>

<span data-ttu-id="a562f-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a562f-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a562f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a562f-115">Requirements</span></span>



| <span data-ttu-id="a562f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a562f-116">Requirement</span></span> | <span data-ttu-id="a562f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a562f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a562f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a562f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a562f-119">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a562f-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a562f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a562f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a562f-121">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a562f-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a562f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a562f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a562f-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="a562f-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a562f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a562f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a562f-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a562f-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a562f-126">MFT \_ connecté \_ au \_ flux de matériel \_</span><span class="sxs-lookup"><span data-stu-id="a562f-126">MFT\_CONNECTED\_TO\_HW\_STREAM</span></span>](mft-connected-to-hw-stream.md)
</dt> <dt>

[<span data-ttu-id="a562f-127">Matériel MFTs</span><span class="sxs-lookup"><span data-stu-id="a562f-127">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="a562f-128">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="a562f-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




