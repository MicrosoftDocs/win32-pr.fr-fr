---
description: Cet attribut spécifie une protection supplémentaire offerte par une autorité d’approbation de sortie vidéo (OTA) lorsqu’un connecteur n’offre pas de protection de sortie.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: Attribut MFPROTECTION_CONSTRICTVIDEO_NOOPM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951489"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a><span data-ttu-id="23fd9-103">MFPROTECTION \_ CONSTRICTVIDEO \_ NOOPM, attribut</span><span class="sxs-lookup"><span data-stu-id="23fd9-103">MFPROTECTION\_CONSTRICTVIDEO\_NOOPM attribute</span></span>

<span data-ttu-id="23fd9-104">Cet attribut spécifie une protection supplémentaire offerte par une autorité d’approbation de sortie vidéo (OTA) lorsqu’un connecteur n’offre pas de protection de sortie.</span><span class="sxs-lookup"><span data-stu-id="23fd9-104">This attribute specifies additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="23fd9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="23fd9-105">Data type</span></span>

<span data-ttu-id="23fd9-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="23fd9-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="23fd9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="23fd9-107">Remarks</span></span>

<span data-ttu-id="23fd9-108">Il s’agit d’une protection supplémentaire offerte par une autorité d’approbation de sortie vidéo (OTA) lorsqu’un connecteur n’offre pas de protection de sortie (voir [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span><span class="sxs-lookup"><span data-stu-id="23fd9-108">This is an additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection (see [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span></span> <span data-ttu-id="23fd9-109">Dans ce cas, le OTA peut proposer cette protection dont l’effet est identique à la protection [MFPROTECTION \_ CONSTRICTVIDEO](mfprotection-constrictvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="23fd9-109">In this case the OTA may offer this protection whose effect is the same as the [MFPROTECTION\_CONSTRICTVIDEO](mfprotection-constrictvideo.md) protection.</span></span> <span data-ttu-id="23fd9-110">Cela est défini pour éviter toute confusion avec les appels précédents à [**IMFOutputPolicy :: GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interactions où la présence de la \_ protection MFPROTECTION CONSTRICTVIDEO a été utilisée pour aider à identifier le Pseudo-connecteur du gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="23fd9-110">This is defined to avoid confusion with previous calls to [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interactions where the presence of MFPROTECTION\_CONSTRICTVIDEO protection was used to help identify the desktop window manager pseudo-connector.</span></span>

## <a name="requirements"></a><span data-ttu-id="23fd9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23fd9-111">Requirements</span></span>



| <span data-ttu-id="23fd9-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23fd9-112">Requirement</span></span> | <span data-ttu-id="23fd9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="23fd9-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23fd9-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23fd9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="23fd9-115">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23fd9-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="23fd9-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23fd9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="23fd9-117">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23fd9-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="23fd9-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="23fd9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="23fd9-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="23fd9-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23fd9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23fd9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23fd9-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23fd9-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




