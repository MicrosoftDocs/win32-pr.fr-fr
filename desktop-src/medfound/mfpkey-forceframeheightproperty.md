---
description: Spécifie une hauteur de frame intermédiaire pour la vidéo encodée.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: MFPKEY_FORCEFRAMEHEIGHT, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202353"
---
# <a name="mfpkey_forceframeheight-property"></a><span data-ttu-id="3bed4-103">MFPKEY \_ propriété FORCEFRAMEHEIGHT</span><span class="sxs-lookup"><span data-stu-id="3bed4-103">MFPKEY\_FORCEFRAMEHEIGHT Property</span></span>

<span data-ttu-id="3bed4-104">Spécifie une hauteur de frame intermédiaire pour la vidéo encodée.</span><span class="sxs-lookup"><span data-stu-id="3bed4-104">Specifies an intermediate frame height for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3bed4-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3bed4-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3bed4-106">\_wszWMVCForceFrameHeight g</span><span class="sxs-lookup"><span data-stu-id="3bed4-106">g\_wszWMVCForceFrameHeight</span></span>

## <a name="data-type"></a><span data-ttu-id="3bed4-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="3bed4-107">Data Type</span></span>

<span data-ttu-id="3bed4-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="3bed4-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="3bed4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3bed4-109">Remarks</span></span>

<span data-ttu-id="3bed4-110">Vous pouvez définir cette valeur et la propriété [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) pour forcer l’encodeur à encoder le flux vidéo avec une taille de frame inférieure aux tailles d’entrée ou de sortie.</span><span class="sxs-lookup"><span data-stu-id="3bed4-110">You can set this value and the [MFPKEY\_FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="3bed4-111">En cas de décodage, la vidéo est redimensionnée à sa résolution d’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="3bed4-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="3bed4-112">Les dimensions de frame valides sur l’un des axes sont commodes de 2 à 8192 pixels.</span><span class="sxs-lookup"><span data-stu-id="3bed4-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="3bed4-113">Les dimensions du frame doivent être divisibles par 2.</span><span class="sxs-lookup"><span data-stu-id="3bed4-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bed4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bed4-114">Requirements</span></span>



| <span data-ttu-id="3bed4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bed4-115">Requirement</span></span> | <span data-ttu-id="3bed4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bed4-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bed4-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bed4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3bed4-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3bed4-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3bed4-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bed4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3bed4-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3bed4-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3bed4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3bed4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bed4-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bed4-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bed4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bed4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bed4-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3bed4-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




