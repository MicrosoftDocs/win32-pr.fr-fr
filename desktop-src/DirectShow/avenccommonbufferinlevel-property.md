---
description: Spécifie le niveau initial de la mémoire tampon d’encodage, en bits. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: Propriété AVEncCommonBufferInLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109670"
---
# <a name="avenccommonbufferinlevel-property"></a><span data-ttu-id="d8c4e-104">Propriété AVEncCommonBufferInLevel</span><span class="sxs-lookup"><span data-stu-id="d8c4e-104">AVEncCommonBufferInLevel property</span></span>

<span data-ttu-id="d8c4e-105">Spécifie le niveau initial de la mémoire tampon d’encodage, en bits.</span><span class="sxs-lookup"><span data-stu-id="d8c4e-105">Specifies the initial level of the encoding buffer, in bits.</span></span> <span data-ttu-id="d8c4e-106">Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="d8c4e-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="d8c4e-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d8c4e-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d8c4e-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="d8c4e-108">Data type</span></span>

<span data-ttu-id="d8c4e-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d8c4e-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d8c4e-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="d8c4e-110">Property GUID</span></span>

<span data-ttu-id="d8c4e-111">**CODECAPI \_ AVEncCommonBufferInLevel**</span><span class="sxs-lookup"><span data-stu-id="d8c4e-111">**CODECAPI\_AVEncCommonBufferInLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="d8c4e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d8c4e-112">Property value</span></span>

<span data-ttu-id="d8c4e-113">Cette propriété a une plage de valeurs linéaire.</span><span class="sxs-lookup"><span data-stu-id="d8c4e-113">This property has a linear range of values.</span></span> <span data-ttu-id="d8c4e-114">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="d8c4e-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8c4e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d8c4e-115">Remarks</span></span>

<span data-ttu-id="d8c4e-116">Pour la vidéo MPEG, cette propriété définit la saturation de la mémoire tampon vidéo (VBV) initiale.</span><span class="sxs-lookup"><span data-stu-id="d8c4e-116">For MPEG video, this property defines the initial video buffer verifier (VBV) fullness.</span></span> <span data-ttu-id="d8c4e-117">Il prend en charge la concaténation de flux pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="d8c4e-117">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8c4e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8c4e-118">Requirements</span></span>



| <span data-ttu-id="d8c4e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8c4e-119">Requirement</span></span> | <span data-ttu-id="d8c4e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8c4e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c4e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8c4e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d8c4e-122">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d8c4e-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d8c4e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8c4e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d8c4e-124">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d8c4e-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d8c4e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8c4e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8c4e-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8c4e-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8c4e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8c4e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c4e-128">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="d8c4e-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d8c4e-129">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d8c4e-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




