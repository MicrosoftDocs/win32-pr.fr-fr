---
description: Spécifie si le flux de sortie doit être structuré afin que le flux encodé ait une latence de décodage faible.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Propriété AVEncCommonLowLatency (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200825"
---
# <a name="avenccommonlowlatency-property"></a><span data-ttu-id="47afd-103">Propriété AVEncCommonLowLatency</span><span class="sxs-lookup"><span data-stu-id="47afd-103">AVEncCommonLowLatency property</span></span>

<span data-ttu-id="47afd-104">Spécifie si le flux de sortie doit être structuré afin que le flux encodé ait une latence de décodage faible.</span><span class="sxs-lookup"><span data-stu-id="47afd-104">Specifies whether the output stream should be structured so that the encoded stream has a low decoding latency.</span></span>

<span data-ttu-id="47afd-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="47afd-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="47afd-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="47afd-106">Data type</span></span>

<span data-ttu-id="47afd-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="47afd-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="47afd-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="47afd-108">Property GUID</span></span>

<span data-ttu-id="47afd-109">**CODECAPI \_ AVEncCommonLowLatency**</span><span class="sxs-lookup"><span data-stu-id="47afd-109">**CODECAPI\_AVEncCommonLowLatency**</span></span>

## <a name="remarks"></a><span data-ttu-id="47afd-110">Notes</span><span class="sxs-lookup"><span data-stu-id="47afd-110">Remarks</span></span>

<span data-ttu-id="47afd-111">La latence du décodage est définie comme la quantité de données que le décodeur doit mettre en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="47afd-111">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="47afd-112">Par exemple, la définition de cette propriété sur la **\_ valeur variant true** sur un encodeur vidéo MPEG limite les types de structures GOP que l’encodeur peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="47afd-112">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

## <a name="requirements"></a><span data-ttu-id="47afd-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47afd-113">Requirements</span></span>



| <span data-ttu-id="47afd-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47afd-114">Requirement</span></span> | <span data-ttu-id="47afd-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="47afd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47afd-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47afd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="47afd-117">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="47afd-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="47afd-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47afd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="47afd-119">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="47afd-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="47afd-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="47afd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="47afd-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="47afd-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47afd-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47afd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47afd-123">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="47afd-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="47afd-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="47afd-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




