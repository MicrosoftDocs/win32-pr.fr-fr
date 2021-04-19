---
description: Pour les types de média YUV, définit la matrice de conversion de l’espace de couleurs YCbCr sur l’espace de couleurs RVB.
ms.assetid: b268d16d-b4cc-4026-9ba7-805cc5409b95
title: Attribut MF_MT_YUV_MATRIX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c6976e4652c69b3bddc910dcc536a3d07bf39a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536628"
---
# <a name="mf_mt_yuv_matrix-attribute"></a><span data-ttu-id="b7af9-103">\_Attribut de \_ matrice YUV MT \_ MF</span><span class="sxs-lookup"><span data-stu-id="b7af9-103">MF\_MT\_YUV\_MATRIX attribute</span></span>

<span data-ttu-id="b7af9-104">Pour les types de média YUV, définit la matrice de conversion de l’espace de couleurs Y’Cb’Cr sur l’espace de couleurs R’G’B.</span><span class="sxs-lookup"><span data-stu-id="b7af9-104">For YUV media types, defines the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space.</span></span>

## <a name="data-type"></a><span data-ttu-id="b7af9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b7af9-105">Data type</span></span>

<span data-ttu-id="b7af9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b7af9-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b7af9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b7af9-107">Remarks</span></span>

<span data-ttu-id="b7af9-108">La valeur de cet attribut est un membre de l’énumération [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) .</span><span class="sxs-lookup"><span data-stu-id="b7af9-108">The value of this attribute is a member of the [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) enumeration.</span></span>

<span data-ttu-id="b7af9-109">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b7af9-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7af9-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7af9-110">Requirements</span></span>



| <span data-ttu-id="b7af9-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7af9-111">Requirement</span></span> | <span data-ttu-id="b7af9-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7af9-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7af9-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7af9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b7af9-114">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="b7af9-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b7af9-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7af9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b7af9-116">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="b7af9-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b7af9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7af9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7af9-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7af9-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7af9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7af9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7af9-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7af9-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7af9-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b7af9-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b7af9-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b7af9-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b7af9-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b7af9-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="b7af9-124">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="b7af9-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7af9-125">Informations sur les couleurs étendues</span><span class="sxs-lookup"><span data-stu-id="b7af9-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




