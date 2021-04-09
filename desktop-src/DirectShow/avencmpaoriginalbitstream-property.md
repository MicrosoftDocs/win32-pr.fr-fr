---
description: Spécifie le paramètre par défaut du bit d’origine dans le flux audio MPEG-1. Cette propriété s’applique aux encodeurs audio MPEG.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Propriété AVEncMPAOriginalBitstream (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a49fda5bb605ac8735ebac4be758e7f73efb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846546"
---
# <a name="avencmpaoriginalbitstream-property"></a><span data-ttu-id="f5cf0-104">Propriété AVEncMPAOriginalBitstream</span><span class="sxs-lookup"><span data-stu-id="f5cf0-104">AVEncMPAOriginalBitstream property</span></span>

<span data-ttu-id="f5cf0-105">Spécifie le paramètre par défaut du bit d’origine dans le flux audio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="f5cf0-105">Specifies the default setting for the original bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="f5cf0-106">Cette propriété s’applique aux encodeurs audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="f5cf0-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="f5cf0-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f5cf0-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="f5cf0-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="f5cf0-108">Data type</span></span>

<span data-ttu-id="f5cf0-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="f5cf0-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f5cf0-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="f5cf0-110">Property GUID</span></span>

<span data-ttu-id="f5cf0-111">**CODECAPI \_ AVEncMPAOriginalBitstream**</span><span class="sxs-lookup"><span data-stu-id="f5cf0-111">**CODECAPI\_AVEncMPAOriginalBitstream**</span></span>

## <a name="property-value"></a><span data-ttu-id="f5cf0-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f5cf0-112">Property value</span></span>

<span data-ttu-id="f5cf0-113">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f5cf0-113">This property can have the following values.</span></span>



| <span data-ttu-id="f5cf0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5cf0-114">Value</span></span>          | <span data-ttu-id="f5cf0-115">Description</span><span class="sxs-lookup"><span data-stu-id="f5cf0-115">Description</span></span>          |
|----------------|----------------------|
| <span data-ttu-id="f5cf0-116">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="f5cf0-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="f5cf0-117">Le bit d’origine est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f5cf0-117">Original bit is off.</span></span> |
| <span data-ttu-id="f5cf0-118">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="f5cf0-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="f5cf0-119">Le bit d’origine est activé.</span><span class="sxs-lookup"><span data-stu-id="f5cf0-119">Original bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="f5cf0-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f5cf0-120">Remarks</span></span>

<span data-ttu-id="f5cf0-121">L’encodeur peut remplacer ce paramètre en fonction du contenu du flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f5cf0-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5cf0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5cf0-122">Requirements</span></span>



| <span data-ttu-id="f5cf0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5cf0-123">Requirement</span></span> | <span data-ttu-id="f5cf0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5cf0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5cf0-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5cf0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f5cf0-126">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="f5cf0-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f5cf0-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5cf0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f5cf0-128">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="f5cf0-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f5cf0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5cf0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5cf0-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5cf0-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5cf0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5cf0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5cf0-132">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="f5cf0-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="f5cf0-133">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="f5cf0-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




