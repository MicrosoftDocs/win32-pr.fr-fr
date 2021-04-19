---
description: Spécifie le nombre maximal d’échantillons PCM supplémentaires qui peuvent être retournés à la fin de après le décodage d’un fichier.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518194"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a><span data-ttu-id="921d3-103">\_Propriété MaxNumPCMSamplesWithPaddedSilence du décodeur MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="921d3-103">MFPKEY\_Decoder\_MaxNumPCMSamplesWithPaddedSilence Property</span></span>

<span data-ttu-id="921d3-104">Spécifie le nombre maximal d’échantillons PCM supplémentaires qui peuvent être retournés à la fin de après le décodage d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="921d3-104">Specifies the maximum number of additional PCM samples that might be returned at the end of after decoding a file.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="921d3-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="921d3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="921d3-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="921d3-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="921d3-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="921d3-107">Data Type</span></span>

<span data-ttu-id="921d3-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="921d3-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="921d3-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="921d3-109">Default Value</span></span>

<span data-ttu-id="921d3-110">2 048</span><span class="sxs-lookup"><span data-stu-id="921d3-110">2048</span></span>

## <a name="remarks"></a><span data-ttu-id="921d3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="921d3-111">Remarks</span></span>

<span data-ttu-id="921d3-112">Cette propriété peut être utilisée pour estimer le silence artificiel qui est inséré entre les chansons au fur et à mesure qu’elles sont chargées dans le décodeur l’une après l’autre.</span><span class="sxs-lookup"><span data-stu-id="921d3-112">This property can be used to estimate artificial silence that gets is inserted between songs as they are fed to the decoder one after another.</span></span>

<span data-ttu-id="921d3-113">Pour les décodeurs Windows Media Audio 10 Professional et Windows Media Audio 9 Lossless, cette propriété est toujours égale à 0.</span><span class="sxs-lookup"><span data-stu-id="921d3-113">For the Windows Media Audio 10 Professional and Windows Media Audio 9 Lossless decoders, this property is always equal to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="921d3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="921d3-114">Requirements</span></span>



| <span data-ttu-id="921d3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="921d3-115">Requirement</span></span> | <span data-ttu-id="921d3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="921d3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="921d3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="921d3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="921d3-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="921d3-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="921d3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="921d3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="921d3-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="921d3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="921d3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="921d3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="921d3-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="921d3-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="921d3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="921d3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921d3-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="921d3-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
