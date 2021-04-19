---
description: Obtient la taille de l’image décodée, en pixels.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Propriété AVDecVideoImageSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe8fc3e77de920588ca1f0ee31d86f19c7e667
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515758"
---
# <a name="avdecvideoimagesize-property"></a><span data-ttu-id="9eae6-103">Propriété AVDecVideoImageSize</span><span class="sxs-lookup"><span data-stu-id="9eae6-103">AVDecVideoImageSize property</span></span>

<span data-ttu-id="9eae6-104">Obtient la taille de l’image décodée, en pixels.</span><span class="sxs-lookup"><span data-stu-id="9eae6-104">Gets the size of the decoded image, in pixels.</span></span>

<span data-ttu-id="9eae6-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9eae6-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="9eae6-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="9eae6-106">Data type</span></span>

<span data-ttu-id="9eae6-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="9eae6-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9eae6-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="9eae6-108">Property GUID</span></span>

<span data-ttu-id="9eae6-109">**CODECAPI \_ AVDecVideoImageSize**</span><span class="sxs-lookup"><span data-stu-id="9eae6-109">**CODECAPI\_AVDecVideoImageSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="9eae6-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9eae6-110">Property value</span></span>

<span data-ttu-id="9eae6-111">Les 16 bits de poids fort contiennent la largeur, tandis que les 16 bits de poids faible contiennent la hauteur.</span><span class="sxs-lookup"><span data-stu-id="9eae6-111">The high 16 bits contain the width, and the low 16 bits contain the height.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eae6-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9eae6-112">Remarks</span></span>

<span data-ttu-id="9eae6-113">Le nombre de canaux comprend le canal de l’effet de fréquence faible (LFE), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9eae6-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eae6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9eae6-114">Requirements</span></span>



| <span data-ttu-id="9eae6-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9eae6-115">Requirement</span></span> | <span data-ttu-id="9eae6-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9eae6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9eae6-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eae6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9eae6-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="9eae6-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9eae6-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eae6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9eae6-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="9eae6-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9eae6-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9eae6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eae6-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eae6-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eae6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9eae6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eae6-124">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="9eae6-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9eae6-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="9eae6-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




