---
description: Taux d’erreur de données, en erreurs de bits par seconde, pour un type de média vidéo.
ms.assetid: 90433ff4-a563-4751-86d9-caac0cc58194
title: Attribut MF_MT_AVG_BIT_ERROR_RATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21eb33d1bc1636dd047dbd56ce6b7ad3a683f356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201981"
---
# <a name="mf_mt_avg_bit_error_rate-attribute"></a><span data-ttu-id="a500c-103">\_Attribut de \_ taux d’erreur moyen des \_ bits \_ \_ MF</span><span class="sxs-lookup"><span data-stu-id="a500c-103">MF\_MT\_AVG\_BIT\_ERROR\_RATE attribute</span></span>

<span data-ttu-id="a500c-104">Taux d’erreur de données, en erreurs de bits par seconde, pour un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="a500c-104">Data error rate, in bit errors per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a500c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a500c-105">Data type</span></span>

<span data-ttu-id="a500c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a500c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a500c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a500c-107">Remarks</span></span>

<span data-ttu-id="a500c-108">Cet attribut correspond au membre **dwBitErrorRate** des structures [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) et [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="a500c-108">This attribute corresponds to the **dwBitErrorRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="a500c-109">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a500c-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a500c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a500c-110">Requirements</span></span>



| <span data-ttu-id="a500c-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a500c-111">Requirement</span></span> | <span data-ttu-id="a500c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a500c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a500c-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a500c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a500c-114">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a500c-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a500c-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a500c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a500c-116">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="a500c-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a500c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="a500c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a500c-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a500c-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a500c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a500c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a500c-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a500c-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a500c-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a500c-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a500c-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a500c-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a500c-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a500c-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a500c-124">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="a500c-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
