---
description: Spécifie si le récepteur de fichiers MPEG-4 filtre le jeu de paramètres de séquence (SPS) et le jeu de paramètres d’image (PPS) NALUs.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: Attribut MF_MPEG4SINK_SPSPPS_PASSTHROUGH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754276"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a><span data-ttu-id="0217a-103">\_ \_ Attribut passthrough MPEG4SINK SPSPPS MF \_</span><span class="sxs-lookup"><span data-stu-id="0217a-103">MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute</span></span>

<span data-ttu-id="0217a-104">Spécifie si le [**récepteur de fichiers MPEG-4**](mpeg-4-file-sink.md) filtre le jeu de paramètres de séquence (SPS) et le jeu de paramètres d’image (PPS) NALUs.</span><span class="sxs-lookup"><span data-stu-id="0217a-104">Specifies whether the [**MPEG-4 File Sink**](mpeg-4-file-sink.md) filters out sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

## <a name="data-type"></a><span data-ttu-id="0217a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0217a-105">Data type</span></span>

<span data-ttu-id="0217a-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0217a-106">**BOOL** stored as **UINT32**</span></span>

## <a name="applies-to"></a><span data-ttu-id="0217a-107">S’applique à</span><span class="sxs-lookup"><span data-stu-id="0217a-107">Applies to</span></span>

[<span data-ttu-id="0217a-108">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="0217a-108">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a><span data-ttu-id="0217a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0217a-109">Remarks</span></span>

<span data-ttu-id="0217a-110">Le [**récepteur de fichiers MPEG-4**](mpeg-4-file-sink.md) écrit les paramètres SPS et PPS dans la zone de description de l’exemple du fichier MP4.</span><span class="sxs-lookup"><span data-stu-id="0217a-110">The [**MPEG-4 File Sink**](mpeg-4-file-sink.md) writes the SPS and PPS parameters into the sample description box of the MP4 file.</span></span> <span data-ttu-id="0217a-111">Par défaut, il élimine les NALUs SPS et PPS du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="0217a-111">By default, it filters out the SPS and PPS NALUs from the video stream.</span></span> <span data-ttu-id="0217a-112">Pour remplacer ce comportement, affectez la valeur \_ \_ \_ **true** à l’attribut passthrough MPEG4SINK SPSPPS MF.</span><span class="sxs-lookup"><span data-stu-id="0217a-112">To override this behavior, set the MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0217a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0217a-113">Requirements</span></span>



| <span data-ttu-id="0217a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0217a-114">Requirement</span></span> | <span data-ttu-id="0217a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0217a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0217a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0217a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0217a-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0217a-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0217a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0217a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0217a-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="0217a-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0217a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0217a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0217a-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0217a-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0217a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0217a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0217a-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0217a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




