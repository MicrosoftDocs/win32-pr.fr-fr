---
description: Contient le lien symbolique pour une transformation de Media Foundation matérielle (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: Attribut MFT_ENUM_HARDWARE_URL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202255"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a><span data-ttu-id="71750-103">\_Attribut d' \_ \_ attribut d’URL matériel de l’énumération MFT \_</span><span class="sxs-lookup"><span data-stu-id="71750-103">MFT\_ENUM\_HARDWARE\_URL\_Attribute attribute</span></span>

<span data-ttu-id="71750-104">Contient le lien symbolique pour une transformation de Media Foundation matérielle (MFT).</span><span class="sxs-lookup"><span data-stu-id="71750-104">Contains the symbolic link for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="71750-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="71750-105">Data type</span></span>

<span data-ttu-id="71750-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="71750-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="71750-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="71750-107">Get/set</span></span>

<span data-ttu-id="71750-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="71750-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="71750-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="71750-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="71750-110">Notes</span><span class="sxs-lookup"><span data-stu-id="71750-110">Remarks</span></span>

<span data-ttu-id="71750-111">Cet attribut est pris en charge par les MFTs basés sur le matériel.</span><span class="sxs-lookup"><span data-stu-id="71750-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="71750-112">La valeur de l’attribut est le lien symbolique pour le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="71750-112">The value of the attribute is the symbolic link for the device driver.</span></span> <span data-ttu-id="71750-113">Cet attribut est également défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) alloués par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , lorsque ces pointeurs représentent des MFTS basées sur le matériel.</span><span class="sxs-lookup"><span data-stu-id="71750-113">This attribute is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="71750-114">Le lien symbolique doit être considéré comme une chaîne opaque.</span><span class="sxs-lookup"><span data-stu-id="71750-114">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="71750-115">Pour obtenir le nom complet d’un appareil, interrogez l’attribut [ \_ \_ nom convivial](mft-friendly-name-attribute.md) de la MFT.</span><span class="sxs-lookup"><span data-stu-id="71750-115">To get the display name for a device, query the [MFT\_FRIENDLY\_NAME](mft-friendly-name-attribute.md) attribute.</span></span>

<span data-ttu-id="71750-116">Cet attribut n’est pas défini pour le MFTs logiciel.</span><span class="sxs-lookup"><span data-stu-id="71750-116">Software MFTs should not have this attribute set.</span></span>

<span data-ttu-id="71750-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="71750-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="71750-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71750-118">Requirements</span></span>



| <span data-ttu-id="71750-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71750-119">Requirement</span></span> | <span data-ttu-id="71750-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="71750-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71750-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71750-121">Minimum supported client</span></span><br/> | <span data-ttu-id="71750-122">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="71750-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="71750-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71750-123">Minimum supported server</span></span><br/> | <span data-ttu-id="71750-124">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="71750-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="71750-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="71750-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="71750-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="71750-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71750-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71750-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71750-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="71750-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="71750-129">Matériel MFTs</span><span class="sxs-lookup"><span data-stu-id="71750-129">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="71750-130">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="71750-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




