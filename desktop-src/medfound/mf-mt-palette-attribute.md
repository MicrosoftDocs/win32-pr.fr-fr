---
description: Contient les entrées de palette pour un type de média vidéo. Utilisez cet attribut pour les formats vidéo en palette, tels que RVB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: Attribut MF_MT_PALETTE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dcfc596ae463cf642cc462da1c73dc641356d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529791"
---
# <a name="mf_mt_palette-attribute"></a><span data-ttu-id="6fb31-104">\_Attribut de \_ palette MF MT</span><span class="sxs-lookup"><span data-stu-id="6fb31-104">MF\_MT\_PALETTE attribute</span></span>

<span data-ttu-id="6fb31-105">Contient les entrées de palette pour un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="6fb31-105">Contains the palette entries for a video media type.</span></span> <span data-ttu-id="6fb31-106">Utilisez cet attribut pour les formats vidéo en palette, tels que RVB 8.</span><span class="sxs-lookup"><span data-stu-id="6fb31-106">Use this attribute for palettized video formats, such as RGB 8.</span></span>

## <a name="data-type"></a><span data-ttu-id="6fb31-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="6fb31-107">Data type</span></span>

<span data-ttu-id="6fb31-108">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="6fb31-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="6fb31-109">Notes</span><span class="sxs-lookup"><span data-stu-id="6fb31-109">Remarks</span></span>

<span data-ttu-id="6fb31-110">Les données d’attribut sont un tableau d’unions [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) .</span><span class="sxs-lookup"><span data-stu-id="6fb31-110">The attribute data is an array of [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) unions.</span></span>

<span data-ttu-id="6fb31-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6fb31-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fb31-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fb31-112">Requirements</span></span>



| <span data-ttu-id="6fb31-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fb31-113">Requirement</span></span> | <span data-ttu-id="6fb31-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fb31-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb31-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fb31-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb31-116">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="6fb31-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6fb31-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fb31-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb31-118">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="6fb31-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6fb31-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fb31-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fb31-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fb31-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fb31-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fb31-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb31-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6fb31-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6fb31-123">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="6fb31-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="6fb31-124">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="6fb31-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="6fb31-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6fb31-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6fb31-126">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="6fb31-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




