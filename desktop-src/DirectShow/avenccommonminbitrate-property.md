---
description: Spécifie la vitesse de transmission minimale, en bits par seconde. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: Propriété AVEncCommonMinBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c9b6e84675994d2aca7548f6c13d6558ebc020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519196"
---
# <a name="avenccommonminbitrate-property"></a><span data-ttu-id="a3f0e-104">Propriété AVEncCommonMinBitRate</span><span class="sxs-lookup"><span data-stu-id="a3f0e-104">AVEncCommonMinBitRate property</span></span>

<span data-ttu-id="a3f0e-105">Spécifie la vitesse de transmission minimale, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-105">Specifies the minimum bit rate, in bits per second.</span></span> <span data-ttu-id="a3f0e-106">Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="a3f0e-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="a3f0e-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a3f0e-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="a3f0e-108">Data type</span></span>

<span data-ttu-id="a3f0e-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a3f0e-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a3f0e-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="a3f0e-110">Property GUID</span></span>

<span data-ttu-id="a3f0e-111">**CODECAPI \_ AVEncCommonMinBitRate**</span><span class="sxs-lookup"><span data-stu-id="a3f0e-111">**CODECAPI\_AVEncCommonMinBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="a3f0e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a3f0e-112">Property value</span></span>

<span data-ttu-id="a3f0e-113">Cette propriété a une plage de valeurs linéaire.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-113">This property has a linear range of values.</span></span> <span data-ttu-id="a3f0e-114">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="a3f0e-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f0e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a3f0e-115">Remarks</span></span>

<span data-ttu-id="a3f0e-116">L’encodeur applique la vitesse de transmission minimale en renforçant la qualité d’encodage en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-116">The encoder enforces the minimum bit rate by increasing the encoding quality as necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f0e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3f0e-117">Requirements</span></span>



| <span data-ttu-id="a3f0e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3f0e-118">Requirement</span></span> | <span data-ttu-id="a3f0e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3f0e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f0e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3f0e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f0e-121">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a3f0e-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a3f0e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3f0e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f0e-123">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a3f0e-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a3f0e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3f0e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3f0e-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f0e-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f0e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3f0e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f0e-127">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="a3f0e-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a3f0e-128">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a3f0e-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




