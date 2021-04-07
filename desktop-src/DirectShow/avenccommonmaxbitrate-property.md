---
description: Spécifie la vitesse de transmission maximale, en bits par seconde. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).
ms.assetid: 053fdad0-dc5f-4af1-84a6-bb7c0dac7e79
title: Propriété AVEncCommonMaxBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03844935e909591b2fe3c7244db79e77e7936f1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846670"
---
# <a name="avenccommonmaxbitrate-property"></a><span data-ttu-id="e523d-104">Propriété AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="e523d-104">AVEncCommonMaxBitRate property</span></span>

<span data-ttu-id="e523d-105">Spécifie la vitesse de transmission maximale, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="e523d-105">Specifies the maximum bit rate, in bits per second.</span></span> <span data-ttu-id="e523d-106">Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="e523d-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="e523d-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e523d-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="e523d-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="e523d-108">Data type</span></span>

<span data-ttu-id="e523d-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="e523d-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e523d-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="e523d-110">Property GUID</span></span>

<span data-ttu-id="e523d-111">**CODECAPI \_ AVEncCommonMaxBitRate**</span><span class="sxs-lookup"><span data-stu-id="e523d-111">**CODECAPI\_AVEncCommonMaxBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="e523d-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e523d-112">Property value</span></span>

<span data-ttu-id="e523d-113">Cette propriété a une plage de valeurs linéaire.</span><span class="sxs-lookup"><span data-stu-id="e523d-113">This property has a linear range of values.</span></span> <span data-ttu-id="e523d-114">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="e523d-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="e523d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e523d-115">Requirements</span></span>



| <span data-ttu-id="e523d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e523d-116">Requirement</span></span> | <span data-ttu-id="e523d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e523d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e523d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e523d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e523d-119">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="e523d-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e523d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e523d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e523d-121">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="e523d-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e523d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e523d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e523d-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e523d-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e523d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e523d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e523d-125">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="e523d-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="e523d-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="e523d-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




