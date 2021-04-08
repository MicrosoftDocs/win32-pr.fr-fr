---
description: Spécifie la vitesse de transmission moyenne du flux audio encodé, en bits par seconde. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).
ms.assetid: 9513ad64-2de9-497d-86ce-46cfdf87e0f8
title: Propriété AVEncAudioMeanBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e311686e6113003593c8a6dbe02a9fca1f30b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033540"
---
# <a name="avencaudiomeanbitrate-property"></a><span data-ttu-id="b46bd-104">Propriété AVEncAudioMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="b46bd-104">AVEncAudioMeanBitRate property</span></span>

<span data-ttu-id="b46bd-105">Spécifie la vitesse de transmission moyenne du flux audio encodé, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="b46bd-105">Specifies the average bit rate of the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="b46bd-106">Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="b46bd-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="b46bd-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b46bd-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b46bd-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="b46bd-108">Data type</span></span>

<span data-ttu-id="b46bd-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b46bd-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b46bd-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="b46bd-110">Property GUID</span></span>

<span data-ttu-id="b46bd-111">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="b46bd-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="b46bd-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b46bd-112">Property value</span></span>

<span data-ttu-id="b46bd-113">Les encodeurs peuvent implémenter cette propriété en tant que jeu énuméré ou en tant que plage linéaire.</span><span class="sxs-lookup"><span data-stu-id="b46bd-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="requirements"></a><span data-ttu-id="b46bd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b46bd-114">Requirements</span></span>



| <span data-ttu-id="b46bd-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b46bd-115">Requirement</span></span> | <span data-ttu-id="b46bd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b46bd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b46bd-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b46bd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b46bd-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="b46bd-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b46bd-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b46bd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b46bd-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="b46bd-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b46bd-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b46bd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b46bd-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b46bd-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b46bd-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b46bd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b46bd-124">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="b46bd-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b46bd-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b46bd-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




