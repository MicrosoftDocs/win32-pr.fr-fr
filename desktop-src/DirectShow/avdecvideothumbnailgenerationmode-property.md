---
description: Active ou désactive le mode de génération de miniatures dans un décodeur vidéo.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Propriété AVDecVideoThumbnailGenerationMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950321"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a><span data-ttu-id="db7b0-103">Propriété AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="db7b0-103">AVDecVideoThumbnailGenerationMode property</span></span>

<span data-ttu-id="db7b0-104">Active ou désactive le mode de génération de miniatures dans un décodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="db7b0-104">Enables or disables thumbnail generation mode in a video decoder.</span></span>

<span data-ttu-id="db7b0-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="db7b0-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="db7b0-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="db7b0-106">Data type</span></span>

<span data-ttu-id="db7b0-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="db7b0-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="db7b0-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="db7b0-108">Property GUID</span></span>

<span data-ttu-id="db7b0-109">**CODECAPI \_ AVDecVideoThumbnailGenerationMode**</span><span class="sxs-lookup"><span data-stu-id="db7b0-109">**CODECAPI\_AVDecVideoThumbnailGenerationMode**</span></span>

## <a name="remarks"></a><span data-ttu-id="db7b0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="db7b0-110">Remarks</span></span>

<span data-ttu-id="db7b0-111">Si la valeur est **\_ true**, le décodeur utilise un paramètre optimisé pour générer rapidement des images miniatures.</span><span class="sxs-lookup"><span data-stu-id="db7b0-111">If the value is **VARIANT\_TRUE**, the decoder uses a setting that is optimized to generate thumbnail images quickly.</span></span> <span data-ttu-id="db7b0-112">(Par exemple, il peut ignorer des frames B ou P.) Dans le cas contraire, si la valeur est **\_ false**, le décodeur utilise ses paramètres de décodage normaux.</span><span class="sxs-lookup"><span data-stu-id="db7b0-112">(For example, it might skip B or P frames.) Otherwise, if the value is **VARIANT\_FALSE**, the decoder uses its normal decoding settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="db7b0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db7b0-113">Requirements</span></span>



| <span data-ttu-id="db7b0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db7b0-114">Requirement</span></span> | <span data-ttu-id="db7b0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="db7b0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db7b0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db7b0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db7b0-117">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="db7b0-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="db7b0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db7b0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db7b0-119">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="db7b0-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="db7b0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="db7b0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="db7b0-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="db7b0-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db7b0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db7b0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db7b0-123">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="db7b0-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="db7b0-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="db7b0-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




