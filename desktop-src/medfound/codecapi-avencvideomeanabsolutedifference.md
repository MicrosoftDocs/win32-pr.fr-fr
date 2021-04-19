---
description: Contrôle la signalisation de MFSampleExtension \_ MeanAbsoluteDifference par le biais de IMFAttribute sur chaque échantillon de sortie.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: CODECAPI_AVEncVideoMeanAbsoluteDifference, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516199"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a><span data-ttu-id="ebe9f-103">CODECAPI \_ propriété AVEncVideoMeanAbsoluteDifference</span><span class="sxs-lookup"><span data-stu-id="ebe9f-103">CODECAPI\_AVEncVideoMeanAbsoluteDifference property</span></span>

<span data-ttu-id="ebe9f-104">Contrôle la signalisation de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) par le biais de [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) sur chaque échantillon de sortie.</span><span class="sxs-lookup"><span data-stu-id="ebe9f-104">Controls the signaling of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) through [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) on each output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="ebe9f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ebe9f-105">Data type</span></span>

<span data-ttu-id="ebe9f-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="ebe9f-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ebe9f-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="ebe9f-107">Property GUID</span></span>

<span data-ttu-id="ebe9f-108">**CODECAPI \_ AVEncVideoMeanAbsoluteDifference**</span><span class="sxs-lookup"><span data-stu-id="ebe9f-108">**CODECAPI\_AVEncVideoMeanAbsoluteDifference**</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe9f-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ebe9f-109">Remarks</span></span>

<span data-ttu-id="ebe9f-110">Si l’application définit une valeur différente de zéro, l’encodeur doit ajouter l’exemple d’attribut [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) à chaque exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="ebe9f-110">If the application sets a non-zero value then the encoder should add the [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sample attribute to each output sample.</span></span> <span data-ttu-id="ebe9f-111">L' \_ attribut MFSampleExtension MeanAbsoluteDifference indique la différence absolue moyenne entre les échantillons source et les échantillons prédits dans le plan Y.</span><span class="sxs-lookup"><span data-stu-id="ebe9f-111">The MFSampleExtension\_MeanAbsoluteDifference attribute indicates the mean absolute difference between the source samples and the predicted samples in the Y plane.</span></span>

<span data-ttu-id="ebe9f-112">Si l’encodeur retourne 0 pour **GetParameterRange**, l’encodeur ne prend pas en charge la sortie de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sur les exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="ebe9f-112">If the encoder returns 0 for **GetParameterRange**, then the encoder does not support the output of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) on the output samples.</span></span>

<span data-ttu-id="ebe9f-113">La valeur par défaut doit être 0.</span><span class="sxs-lookup"><span data-stu-id="ebe9f-113">The default value should be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe9f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebe9f-114">Requirements</span></span>



| <span data-ttu-id="ebe9f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebe9f-115">Requirement</span></span> | <span data-ttu-id="ebe9f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebe9f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe9f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebe9f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ebe9f-118">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebe9f-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ebe9f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebe9f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ebe9f-120">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebe9f-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ebe9f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebe9f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebe9f-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebe9f-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe9f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebe9f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe9f-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ebe9f-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




