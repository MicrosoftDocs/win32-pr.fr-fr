---
description: Spécifie la fonction de conversion de RVB en RVB pour un type de média vidéo.
ms.assetid: c64c2135-f588-4d7a-9ca8-ae4f7b290572
title: Attribut MF_MT_TRANSFER_FUNCTION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d175a0e40d0aba45b4ec664d71e236e077e09a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521217"
---
# <a name="mf_mt_transfer_function-attribute"></a><span data-ttu-id="7b26e-103">MF \_ - \_ attribut de fonction de transfert MT \_</span><span class="sxs-lookup"><span data-stu-id="7b26e-103">MF\_MT\_TRANSFER\_FUNCTION attribute</span></span>

<span data-ttu-id="7b26e-104">Spécifie la fonction de conversion de RGB en R’G’B’pour un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="7b26e-104">Specifies the conversion function from RGB to R'G'B' for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="7b26e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7b26e-105">Data type</span></span>

<span data-ttu-id="7b26e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7b26e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7b26e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="7b26e-107">Remarks</span></span>

<span data-ttu-id="7b26e-108">La valeur de cet attribut est un membre de l’énumération [**MFVideoTransferFunction**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransferfunction) .</span><span class="sxs-lookup"><span data-stu-id="7b26e-108">The value of this attribute is a member of the [**MFVideoTransferFunction**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransferfunction) enumeration.</span></span>

<span data-ttu-id="7b26e-109">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7b26e-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b26e-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b26e-110">Requirements</span></span>



| <span data-ttu-id="7b26e-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b26e-111">Requirement</span></span> | <span data-ttu-id="7b26e-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b26e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b26e-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b26e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7b26e-114">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="7b26e-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7b26e-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b26e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7b26e-116">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="7b26e-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7b26e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b26e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b26e-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b26e-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b26e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b26e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b26e-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b26e-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7b26e-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7b26e-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7b26e-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7b26e-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7b26e-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="7b26e-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7b26e-124">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="7b26e-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="7b26e-125">Informations sur les couleurs étendues</span><span class="sxs-lookup"><span data-stu-id="7b26e-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




