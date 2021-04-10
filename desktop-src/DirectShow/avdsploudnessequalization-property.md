---
description: Active ou désactive l’égalisation sonore dans un décodeur audio ou un processeur de signal numérique (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Propriété AVDSPLoudnessEqualization (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a2fc09077c114ab18f2626b333cfe4c87c97d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950317"
---
# <a name="avdsploudnessequalization-property"></a><span data-ttu-id="4755f-103">Propriété AVDSPLoudnessEqualization</span><span class="sxs-lookup"><span data-stu-id="4755f-103">AVDSPLoudnessEqualization property</span></span>

<span data-ttu-id="4755f-104">Active ou désactive l’égalisation sonore dans un décodeur audio ou un processeur de signal numérique (DSP).</span><span class="sxs-lookup"><span data-stu-id="4755f-104">Enables or disables loudness equalization in an audio decoder or digital signal processor (DSP).</span></span>

<span data-ttu-id="4755f-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4755f-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="4755f-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="4755f-106">Data type</span></span>

<span data-ttu-id="4755f-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="4755f-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4755f-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="4755f-108">Property GUID</span></span>

<span data-ttu-id="4755f-109">**CODECAPI \_ AVDSPLoudnessEqualization**</span><span class="sxs-lookup"><span data-stu-id="4755f-109">**CODECAPI\_AVDSPLoudnessEqualization**</span></span>

## <a name="property-value"></a><span data-ttu-id="4755f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4755f-110">Property value</span></span>

<span data-ttu-id="4755f-111">La valeur de cette propriété est un membre de l’énumération [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) .</span><span class="sxs-lookup"><span data-stu-id="4755f-111">The value of this property is a member of the [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="4755f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4755f-112">Remarks</span></span>

<span data-ttu-id="4755f-113">L’égalisation sonore est un processus DSP qui maintient un niveau de volume cohérent lorsque le flux audio change.</span><span class="sxs-lookup"><span data-stu-id="4755f-113">Loudness equalization is a DSP process that maintains a consistent volume level when the audio stream changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="4755f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4755f-114">Requirements</span></span>



| <span data-ttu-id="4755f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4755f-115">Requirement</span></span> | <span data-ttu-id="4755f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4755f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4755f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4755f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4755f-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="4755f-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4755f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4755f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4755f-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="4755f-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4755f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="4755f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4755f-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4755f-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4755f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4755f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4755f-124">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="4755f-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4755f-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="4755f-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




