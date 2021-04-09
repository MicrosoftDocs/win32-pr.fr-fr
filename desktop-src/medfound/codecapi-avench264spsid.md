---
description: Définit l’identificateur de l’ensemble de paramètres de séquence (SPS) dans l’unité de couche d’abstraction de réseau (NAL) SPS du flux de bits H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: CODECAPI_AVEncH264SPSID, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111866"
---
# <a name="codecapi_avench264spsid-property"></a><span data-ttu-id="a21bf-103">CODECAPI \_ propriété AVEncH264SPSID</span><span class="sxs-lookup"><span data-stu-id="a21bf-103">CODECAPI\_AVEncH264SPSID property</span></span>

<span data-ttu-id="a21bf-104">Définit l’identificateur de l’ensemble de paramètres de séquence (SPS) dans l’unité de couche d’abstraction de réseau (NAL) SPS du flux de bits H. 264.</span><span class="sxs-lookup"><span data-stu-id="a21bf-104">Sets the sequence parameter set (SPS) identifier in the SPS network abstraction layer (NAL) unit of the H.264 bit stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="a21bf-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a21bf-105">Data type</span></span>

<span data-ttu-id="a21bf-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="a21bf-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a21bf-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="a21bf-107">Property GUID</span></span>

<span data-ttu-id="a21bf-108">**CODECAPI \_ AVEncH264SPSID**</span><span class="sxs-lookup"><span data-stu-id="a21bf-108">**CODECAPI\_AVEncH264SPSID**</span></span>

## <a name="property-value"></a><span data-ttu-id="a21bf-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a21bf-109">Property value</span></span>

<span data-ttu-id="a21bf-110">Spécifie la valeur de l' **\_ ID du \_ jeu \_ de paramètres SEQ** dans l’unité de SPS nal.</span><span class="sxs-lookup"><span data-stu-id="a21bf-110">Specifies the value of **seq\_parameter\_set\_id** in the SPS NAL unit.</span></span> <span data-ttu-id="a21bf-111">L’élément de syntaxe de l’ID de l' **\_ ensemble de paramètres \_ \_ Seq** identifie le jeu de paramètres de séquence.</span><span class="sxs-lookup"><span data-stu-id="a21bf-111">The **seq\_parameter\_set\_id** syntax element identifies the sequence parameter set.</span></span> <span data-ttu-id="a21bf-112">Le flux de bits résultant peut être concaténé avec d’autres flux de bits, afin de produire un flux de bits plus long qui contient plusieurs jeux de paramètres de séquence avec différents identificateurs SPS.</span><span class="sxs-lookup"><span data-stu-id="a21bf-112">The resulting bit stream can be concatenated with other bit streams, to produce a longer bit stream that contains multiple sequence parameter sets with different SPS identifiers.</span></span>

<span data-ttu-id="a21bf-113">La plage valide est 0 31, comme indiqué dans la spécification H. 264/AVC.</span><span class="sxs-lookup"><span data-stu-id="a21bf-113">The valid range is 0 31, as specified in the H.264/AVC specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="a21bf-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a21bf-114">Requirements</span></span>



| <span data-ttu-id="a21bf-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a21bf-115">Requirement</span></span> | <span data-ttu-id="a21bf-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a21bf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a21bf-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a21bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a21bf-118">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a21bf-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="a21bf-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a21bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a21bf-120">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="a21bf-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a21bf-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a21bf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a21bf-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a21bf-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a21bf-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a21bf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a21bf-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a21bf-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a21bf-125">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a21bf-125">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

