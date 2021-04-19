---
description: Spécifie l’ID de fournisseur pour une Microsoft Media Foundation matérielle.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: Attribut MFT_ENUM_HARDWARE_VENDOR_ID_Attribute
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4d92585936e52cbb0b9b65201a5de0d3a02b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533781"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a><span data-ttu-id="7ea6c-103">\_Attribut d' \_ \_ attribut d’ID de fournisseur de matériel d' \_ énumération MFT \_</span><span class="sxs-lookup"><span data-stu-id="7ea6c-103">MFT\_ENUM\_HARDWARE\_VENDOR\_ID\_Attribute attribute</span></span>

<span data-ttu-id="7ea6c-104">Spécifie l’ID de fournisseur pour une transformation de Microsoft Media Foundation matérielle (MFT).</span><span class="sxs-lookup"><span data-stu-id="7ea6c-104">Specifies the vendor ID for a hardware-based Microsoft Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="7ea6c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7ea6c-105">Data type</span></span>

<span data-ttu-id="7ea6c-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="7ea6c-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="7ea6c-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="7ea6c-107">Get/set</span></span>

<span data-ttu-id="7ea6c-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="7ea6c-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="7ea6c-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="7ea6c-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ea6c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7ea6c-110">Remarks</span></span>

<span data-ttu-id="7ea6c-111">Cet attribut est à titre d’information et est facultatif.</span><span class="sxs-lookup"><span data-stu-id="7ea6c-111">This attribute is informational and optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ea6c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ea6c-112">Requirements</span></span>



| <span data-ttu-id="7ea6c-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ea6c-113">Requirement</span></span> | <span data-ttu-id="7ea6c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ea6c-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea6c-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ea6c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7ea6c-116">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7ea6c-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="7ea6c-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ea6c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7ea6c-118">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="7ea6c-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="7ea6c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ea6c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ea6c-120"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ea6c-120"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ea6c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ea6c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea6c-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7ea6c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7ea6c-123">Matériel MFTs</span><span class="sxs-lookup"><span data-stu-id="7ea6c-123">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="7ea6c-124">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="7ea6c-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




