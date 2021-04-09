---
description: Définit le mode de traitement de la Stabilisation vidéo MFT.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: Attribut MF_VIDEODSP_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114011"
---
# <a name="mf_videodsp_mode-attribute"></a><span data-ttu-id="f752d-103">\_Attribut de \_ mode VIDEODSP MF</span><span class="sxs-lookup"><span data-stu-id="f752d-103">MF\_VIDEODSP\_MODE attribute</span></span>

<span data-ttu-id="f752d-104">Définit le mode de traitement de la [**stabilisation vidéo MFT**](video-stabilization-mft.md).</span><span class="sxs-lookup"><span data-stu-id="f752d-104">Sets the processing mode of the [**Video Stabilization MFT**](video-stabilization-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="f752d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f752d-105">Data type</span></span>

<span data-ttu-id="f752d-106">**MFVideoDSPMode** stocké en tant que **UIINT32**</span><span class="sxs-lookup"><span data-stu-id="f752d-106">**MFVideoDSPMode** stored as **UIINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f752d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f752d-107">Remarks</span></span>

<span data-ttu-id="f752d-108">La valeur de cet attribut est une valeur d’énumération [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) .</span><span class="sxs-lookup"><span data-stu-id="f752d-108">The value of this attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="f752d-109">Cet attribut peut être utilisé pour activer ou désactiver la stabilisation d’image et peut être mis à jour pour chaque exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="f752d-109">This attribute can be used to enable or disable the image stabilization, and can be updated for each output sample.</span></span>

<span data-ttu-id="f752d-110">Pour définir cet attribut :</span><span class="sxs-lookup"><span data-stu-id="f752d-110">To set this attribute:</span></span>

1.  <span data-ttu-id="f752d-111">Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur la MFT de stabilisation vidéo pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="f752d-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video stabilization MFT to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="f752d-112">Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) pour définir l’attribut.</span><span class="sxs-lookup"><span data-stu-id="f752d-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="f752d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f752d-113">Requirements</span></span>



| <span data-ttu-id="f752d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f752d-114">Requirement</span></span> | <span data-ttu-id="f752d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f752d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f752d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f752d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f752d-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f752d-117">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f752d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f752d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f752d-119">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f752d-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f752d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f752d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f752d-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f752d-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f752d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f752d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f752d-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f752d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f752d-124">**Stabilisation vidéo MFT**</span><span class="sxs-lookup"><span data-stu-id="f752d-124">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




