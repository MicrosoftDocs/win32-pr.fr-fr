---
description: Spécifie le nombre de passes d’encodage pris en charge par l’encodeur.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Propriété AVEncCommonMultipassMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846669"
---
# <a name="avenccommonmultipassmode-property"></a><span data-ttu-id="c49bc-103">Propriété AVEncCommonMultipassMode</span><span class="sxs-lookup"><span data-stu-id="c49bc-103">AVEncCommonMultipassMode property</span></span>

<span data-ttu-id="c49bc-104">Spécifie le nombre de passes d’encodage pris en charge par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="c49bc-104">Specifies the number of encoding passes that the encoder supports.</span></span>

<span data-ttu-id="c49bc-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c49bc-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="c49bc-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="c49bc-106">Data type</span></span>

<span data-ttu-id="c49bc-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="c49bc-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c49bc-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="c49bc-108">Property GUID</span></span>

<span data-ttu-id="c49bc-109">**CODECAPI \_ AVEncCommonMultipassMode**</span><span class="sxs-lookup"><span data-stu-id="c49bc-109">**CODECAPI\_AVEncCommonMultipassMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="c49bc-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c49bc-110">Property value</span></span>

<span data-ttu-id="c49bc-111">Cette propriété est retournée sous la forme d’une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="c49bc-111">This property is returned as a range of values.</span></span> <span data-ttu-id="c49bc-112">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="c49bc-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="c49bc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c49bc-113">Remarks</span></span>

<span data-ttu-id="c49bc-114">La latence du décodage est définie comme la quantité de données que le décodeur doit mettre en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c49bc-114">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="c49bc-115">Par exemple, la définition de cette propriété sur la **\_ valeur variant true** sur un encodeur vidéo MPEG limite les types de structures GOP que l’encodeur peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="c49bc-115">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

<span data-ttu-id="c49bc-116">Pour définir l’étape d’encodage actuelle, définissez la propriété [**AVEncCommonPassStart**](avenccommonpassstart-property.md) .</span><span class="sxs-lookup"><span data-stu-id="c49bc-116">To set the current encoding pass, set the [**AVEncCommonPassStart**](avenccommonpassstart-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c49bc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c49bc-117">Requirements</span></span>



| <span data-ttu-id="c49bc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c49bc-118">Requirement</span></span> | <span data-ttu-id="c49bc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c49bc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c49bc-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c49bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c49bc-121">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="c49bc-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c49bc-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c49bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c49bc-123">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="c49bc-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c49bc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c49bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c49bc-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c49bc-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c49bc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c49bc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c49bc-127">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="c49bc-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c49bc-128">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="c49bc-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




