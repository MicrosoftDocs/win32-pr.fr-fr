---
description: Active le mode faible latence dans un codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826903"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="a0a8e-103">CODECAPI \_ propriété AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="a0a8e-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="a0a8e-104">Active le mode faible latence dans un codec.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="a0a8e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a0a8e-105">Data type</span></span>

<span data-ttu-id="a0a8e-106">**ULong** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="a0a8e-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a0a8e-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="a0a8e-107">Property GUID</span></span>

<span data-ttu-id="a0a8e-108">**CODECAPI \_ AVLowLatencyMode**</span><span class="sxs-lookup"><span data-stu-id="a0a8e-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="a0a8e-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a0a8e-109">Property value</span></span>

<span data-ttu-id="a0a8e-110">Si la valeur est différente de zéro, le mode faible latence est activé.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="a0a8e-111">Si la valeur est égale à zéro, le mode de latence faible est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a8e-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="a0a8e-112">Remarks</span></span>

<span data-ttu-id="a0a8e-113">Cette propriété s’applique aux encodeurs et aux décodeurs.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="a0a8e-114">Le mode de faible latence est utile pour les communications en temps réel ou la capture en direct, lorsque la latence doit être réduite.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="a0a8e-115">Toutefois, le mode à faible latence peut également réduire la qualité du décodage ou du codage.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="a0a8e-116">L’encodeur est supposé ne pas ajouter de délai d’échantillonnage en raison de la réorganisation des frames dans le processus d’encodage, et un exemple d’entrée produira un échantillon de sortie.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="a0a8e-117">Les secteurs/frames B peuvent être présents tant qu’ils n’introduisent pas de réordonnancement de frame dans l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

> [!WARNING] 
> <span data-ttu-id="a0a8e-118">Dans l’implémentation actuelle, le Media Foundation décodeur H. 264 utilise le type **VT_UI4** pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-118">In the current implementation, the Media Foundation H.264 decoder uses the type **VT_UI4** for this property.</span></span> <span data-ttu-id="a0a8e-119">Toutes les autres implémentations, y compris l’encodeur H. 264, utilisent le type **VT_BOOL**.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-119">All other implementations, including the H.264 encoder, use the type **VT_BOOL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0a8e-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a0a8e-120">Requirements</span></span>



| <span data-ttu-id="a0a8e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0a8e-121">Requirement</span></span> | <span data-ttu-id="a0a8e-122">Value</span><span class="sxs-lookup"><span data-stu-id="a0a8e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a8e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0a8e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a8e-124">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a0a8e-124">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="a0a8e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0a8e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a8e-126">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="a0a8e-126">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a0a8e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0a8e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0a8e-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0a8e-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0a8e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0a8e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a8e-130">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a0a8e-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a0a8e-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a0a8e-131">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

