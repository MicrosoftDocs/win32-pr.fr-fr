---
description: Contient l’horodatage de décodage (DTS) pour l’exemple.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: Attribut MFSampleExtension_DecodeTimestamp (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517582"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a><span data-ttu-id="37221-103">\_Attribut MFSampleExtension DecodeTimestamp</span><span class="sxs-lookup"><span data-stu-id="37221-103">MFSampleExtension\_DecodeTimestamp attribute</span></span>

<span data-ttu-id="37221-104">Contient l’horodatage de décodage (DTS) pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="37221-104">Contains the decode time stamp (DTS) for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="37221-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="37221-105">Data type</span></span>

<span data-ttu-id="37221-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="37221-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="37221-107">Notes</span><span class="sxs-lookup"><span data-stu-id="37221-107">Remarks</span></span>

<span data-ttu-id="37221-108">La valeur de l’attribut est le DTS en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="37221-108">The value of the attribute is the DTS in 100-nanosecond units.</span></span> <span data-ttu-id="37221-109">Le DTS est défini dans certaines normes d’encodage, y compris MPEG.</span><span class="sxs-lookup"><span data-stu-id="37221-109">The DTS is defined in some encoding standards, including MPEG.</span></span> <span data-ttu-id="37221-110">Le DTS spécifie le moment où l’image encodée doit être décodée.</span><span class="sxs-lookup"><span data-stu-id="37221-110">The DTS specifies when the encoded picture should be decoded.</span></span> <span data-ttu-id="37221-111">Si la vidéo encodée contient des frames B, les DTS peuvent différer de l’heure de la présentation, car les images B apparaissent hors de l’ordre temporel dans le flux binaire.</span><span class="sxs-lookup"><span data-stu-id="37221-111">If the encoded video contains B frames, the DTS can differ from the presentation time, because B pictures appear out of temporal order in the bitstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="37221-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37221-112">Requirements</span></span>



| <span data-ttu-id="37221-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37221-113">Requirement</span></span> | <span data-ttu-id="37221-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="37221-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37221-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37221-115">Minimum supported client</span></span><br/> | <span data-ttu-id="37221-116">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="37221-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="37221-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37221-117">Minimum supported server</span></span><br/> | <span data-ttu-id="37221-118">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="37221-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="37221-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="37221-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="37221-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="37221-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37221-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37221-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37221-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37221-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="37221-123">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="37221-123">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




