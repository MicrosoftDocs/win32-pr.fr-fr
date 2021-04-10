---
description: Désactive la conversion de la fréquence des images dans la MFT du processeur vidéo.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: Attribut MF_XVP_DISABLE_FRC (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951390"
---
# <a name="mf_xvp_disable_frc-attribute"></a><span data-ttu-id="a2b9c-103">XVP MF- \_ \_ désactiver l' \_ attribut FRC</span><span class="sxs-lookup"><span data-stu-id="a2b9c-103">MF\_XVP\_DISABLE\_FRC attribute</span></span>

<span data-ttu-id="a2b9c-104">Désactive la conversion de la fréquence des images dans la [**MFT du processeur vidéo**](video-processor-mft.md).</span><span class="sxs-lookup"><span data-stu-id="a2b9c-104">Disables frame-rate conversion in the [**Video Processor MFT**](video-processor-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="a2b9c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a2b9c-105">Data type</span></span>

<span data-ttu-id="a2b9c-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a2b9c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a2b9c-107">Remarks</span></span>

<span data-ttu-id="a2b9c-108">Si cet attribut a la **valeur true**, le processeur vidéo n’effectue pas de conversion de la cadence d’images.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-108">If this attribute is **TRUE**, the video processor will not perform frame-rate conversion.</span></span> <span data-ttu-id="a2b9c-109">Par défaut, le processeur vidéo convertit la fréquence d’images pour qu’elle corresponde au type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-109">By default, the video processor will convert the frame rate to match the output media type.</span></span>

<span data-ttu-id="a2b9c-110">Pour définir cet attribut :</span><span class="sxs-lookup"><span data-stu-id="a2b9c-110">To set this attribute:</span></span>

1.  <span data-ttu-id="a2b9c-111">Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le processeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="a2b9c-112">Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a2b9c-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="a2b9c-113">Définissez l’attribut avant le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b9c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2b9c-114">Requirements</span></span>



| <span data-ttu-id="a2b9c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2b9c-115">Requirement</span></span> | <span data-ttu-id="a2b9c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b9c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b9c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2b9c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b9c-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2b9c-118">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a2b9c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2b9c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b9c-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2b9c-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a2b9c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2b9c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2b9c-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2b9c-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2b9c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2b9c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b9c-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2b9c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




