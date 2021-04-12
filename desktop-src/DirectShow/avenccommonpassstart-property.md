---
description: Démarre la première passe d’encodage.
ms.assetid: a062be3f-7806-4f1c-b98e-2c9ed31f010c
title: Propriété AVEncCommonPassStart (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d5be37fc4866aea6f442d4d8a2c0f74c6609cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392800"
---
# <a name="avenccommonpassstart-property"></a><span data-ttu-id="90edf-103">Propriété AVEncCommonPassStart</span><span class="sxs-lookup"><span data-stu-id="90edf-103">AVEncCommonPassStart property</span></span>

<span data-ttu-id="90edf-104">Démarre la première passe d’encodage.</span><span class="sxs-lookup"><span data-stu-id="90edf-104">Starts the first encoding pass.</span></span>

<span data-ttu-id="90edf-105">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="90edf-105">This property is write-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="90edf-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="90edf-106">Data type</span></span>

<span data-ttu-id="90edf-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="90edf-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="90edf-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="90edf-108">Property GUID</span></span>

<span data-ttu-id="90edf-109">**CODECAPI \_ AVEncCommonPassStart**</span><span class="sxs-lookup"><span data-stu-id="90edf-109">**CODECAPI\_AVEncCommonPassStart**</span></span>

## <a name="property-value"></a><span data-ttu-id="90edf-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="90edf-110">Property value</span></span>

<span data-ttu-id="90edf-111">La valeur de cette propriété est l’étape d’encodage à démarrer.</span><span class="sxs-lookup"><span data-stu-id="90edf-111">The value of this property is the encoding pass to start.</span></span> <span data-ttu-id="90edf-112">Pour obtenir la plage des valeurs prises en charge, interrogez la propriété [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md) de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="90edf-112">To get the range of supported values, query the encoder's [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="90edf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90edf-113">Requirements</span></span>



| <span data-ttu-id="90edf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90edf-114">Requirement</span></span> | <span data-ttu-id="90edf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="90edf-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90edf-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90edf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="90edf-117">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="90edf-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="90edf-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90edf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="90edf-119">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="90edf-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="90edf-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="90edf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="90edf-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="90edf-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90edf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90edf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90edf-123">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="90edf-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="90edf-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="90edf-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




