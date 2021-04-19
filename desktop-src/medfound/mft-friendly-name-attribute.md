---
description: Contient le nom complet d’une transformation de Media Foundation matérielle (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: Attribut MFT_FRIENDLY_NAME_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33417fd30f4d856ce7306fbbbd492fa29575f7ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520488"
---
# <a name="mft_friendly_name_attribute-attribute"></a><span data-ttu-id="5e611-103">\_Attribut de \_ nom \_ convivial de la MFT</span><span class="sxs-lookup"><span data-stu-id="5e611-103">MFT\_FRIENDLY\_NAME\_Attribute attribute</span></span>

<span data-ttu-id="5e611-104">Contient le nom complet d’une transformation de Media Foundation matérielle (MFT).</span><span class="sxs-lookup"><span data-stu-id="5e611-104">Contains the display name for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="5e611-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5e611-105">Data type</span></span>

<span data-ttu-id="5e611-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="5e611-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="5e611-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="5e611-107">Get/set</span></span>

<span data-ttu-id="5e611-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="5e611-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="5e611-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="5e611-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e611-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5e611-110">Remarks</span></span>

<span data-ttu-id="5e611-111">Cet attribut est pris en charge par les MFTs basés sur le matériel.</span><span class="sxs-lookup"><span data-stu-id="5e611-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="5e611-112">Elle est également définie sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) alloués par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , lorsque ces pointeurs représentent des MFTS matériels.</span><span class="sxs-lookup"><span data-stu-id="5e611-112">It is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="5e611-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5e611-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e611-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e611-114">Requirements</span></span>



| <span data-ttu-id="5e611-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e611-115">Requirement</span></span> | <span data-ttu-id="5e611-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e611-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e611-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e611-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e611-118">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5e611-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="5e611-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e611-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5e611-120">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5e611-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5e611-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e611-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e611-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e611-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e611-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e611-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e611-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e611-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e611-125">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="5e611-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




