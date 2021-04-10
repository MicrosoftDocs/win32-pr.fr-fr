---
description: Spécifie si l’encodeur effectue un télécinéma inverse.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Propriété AVEncVideoInverseTelecineEnable (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109498"
---
# <a name="avencvideoinversetelecineenable-property"></a><span data-ttu-id="080e4-103">Propriété AVEncVideoInverseTelecineEnable</span><span class="sxs-lookup"><span data-stu-id="080e4-103">AVEncVideoInverseTelecineEnable property</span></span>

<span data-ttu-id="080e4-104">Spécifie si l’encodeur effectue un télécinéma inverse.</span><span class="sxs-lookup"><span data-stu-id="080e4-104">Specifies whether the encoder performs inverse telecine.</span></span>

<span data-ttu-id="080e4-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="080e4-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="080e4-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="080e4-106">Data type</span></span>

<span data-ttu-id="080e4-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="080e4-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="080e4-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="080e4-108">Property GUID</span></span>

<span data-ttu-id="080e4-109">**CODECAPI \_ AVEncVideoInverseTelecineEnable**</span><span class="sxs-lookup"><span data-stu-id="080e4-109">**CODECAPI\_AVEncVideoInverseTelecineEnable**</span></span>

## <a name="remarks"></a><span data-ttu-id="080e4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="080e4-110">Remarks</span></span>

<span data-ttu-id="080e4-111">Si la valeur est **\_ true**, l’encodeur effectue un télécinéma inverse.</span><span class="sxs-lookup"><span data-stu-id="080e4-111">If the value is **VARIANT\_TRUE**, the encoder performs inverse telecine.</span></span> <span data-ttu-id="080e4-112">Si vous n’avez pas besoin de télécinéma inverse, affectez la valeur **\_ false** à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="080e4-112">If inverse telecine is not required, set this property to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="080e4-113">Pour effectuer un télécinéma inverse en dehors de l’encodeur, affectez la valeur **\_ false** à cette propriété et affectez à la propriété [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) la valeur eAVEncVideoOutputScan \_ SameAsInput.</span><span class="sxs-lookup"><span data-stu-id="080e4-113">To perform inverse telecine outside of the encoder, set this property to **VARIANT\_FALSE** and set the [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) property to eAVEncVideoOutputScan\_SameAsInput.</span></span>

## <a name="requirements"></a><span data-ttu-id="080e4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="080e4-114">Requirements</span></span>



| <span data-ttu-id="080e4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="080e4-115">Requirement</span></span> | <span data-ttu-id="080e4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="080e4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="080e4-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="080e4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="080e4-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="080e4-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="080e4-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="080e4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="080e4-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="080e4-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="080e4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="080e4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="080e4-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="080e4-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="080e4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="080e4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="080e4-124">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="080e4-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="080e4-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="080e4-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




