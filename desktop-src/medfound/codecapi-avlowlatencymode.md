---
description: Active le mode faible latence dans un codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f159045f6b40d531495338b1598c214926a59612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517211"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="c870f-103">CODECAPI \_ propriété AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="c870f-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="c870f-104">Active le mode faible latence dans un codec.</span><span class="sxs-lookup"><span data-stu-id="c870f-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="c870f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="c870f-105">Data type</span></span>

<span data-ttu-id="c870f-106">**ULong** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="c870f-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c870f-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="c870f-107">Property GUID</span></span>

<span data-ttu-id="c870f-108">**CODECAPI \_ AVLowLatencyMode**</span><span class="sxs-lookup"><span data-stu-id="c870f-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="c870f-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c870f-109">Property value</span></span>

<span data-ttu-id="c870f-110">Si la valeur est différente de zéro, le mode faible latence est activé.</span><span class="sxs-lookup"><span data-stu-id="c870f-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="c870f-111">Si la valeur est égale à zéro, le mode de latence faible est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c870f-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="c870f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c870f-112">Remarks</span></span>

<span data-ttu-id="c870f-113">Cette propriété s’applique aux encodeurs et aux décodeurs.</span><span class="sxs-lookup"><span data-stu-id="c870f-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="c870f-114">Le mode de faible latence est utile pour les communications en temps réel ou la capture en direct, lorsque la latence doit être réduite.</span><span class="sxs-lookup"><span data-stu-id="c870f-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="c870f-115">Toutefois, le mode à faible latence peut également réduire la qualité du décodage ou du codage.</span><span class="sxs-lookup"><span data-stu-id="c870f-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="c870f-116">L’encodeur est supposé ne pas ajouter de délai d’échantillonnage en raison de la réorganisation des frames dans le processus d’encodage, et un exemple d’entrée produira un échantillon de sortie.</span><span class="sxs-lookup"><span data-stu-id="c870f-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="c870f-117">Les secteurs/frames B peuvent être présents tant qu’ils n’introduisent pas de réordonnancement de frame dans l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="c870f-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="c870f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c870f-118">Requirements</span></span>



| <span data-ttu-id="c870f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c870f-119">Requirement</span></span> | <span data-ttu-id="c870f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c870f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c870f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c870f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c870f-122">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c870f-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="c870f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c870f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c870f-124">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="c870f-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c870f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c870f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c870f-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c870f-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c870f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c870f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c870f-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c870f-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c870f-129">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="c870f-129">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

