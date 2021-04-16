---
description: Spécifie une largeur de frame intermédiaire pour la vidéo encodée.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: MFPKEY_FORCEFRAMEWIDTH, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea4c8c7ac025de1c089c592a591136df966797d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528671"
---
# <a name="mfpkey_forceframewidth-property"></a><span data-ttu-id="bb1ac-103">MFPKEY \_ propriété FORCEFRAMEWIDTH</span><span class="sxs-lookup"><span data-stu-id="bb1ac-103">MFPKEY\_FORCEFRAMEWIDTH Property</span></span>

<span data-ttu-id="bb1ac-104">Spécifie une largeur de frame intermédiaire pour la vidéo encodée.</span><span class="sxs-lookup"><span data-stu-id="bb1ac-104">Specifies an intermediate frame width for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="bb1ac-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="bb1ac-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="bb1ac-106">\_wszWMVCForceFrameWidth g</span><span class="sxs-lookup"><span data-stu-id="bb1ac-106">g\_wszWMVCForceFrameWidth</span></span>

## <a name="data-type"></a><span data-ttu-id="bb1ac-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="bb1ac-107">Data Type</span></span>

<span data-ttu-id="bb1ac-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="bb1ac-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="bb1ac-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bb1ac-109">Remarks</span></span>

<span data-ttu-id="bb1ac-110">Vous pouvez définir cette valeur et la propriété [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) pour forcer l’encodeur à encoder le flux vidéo avec une taille de frame inférieure aux tailles d’entrée ou de sortie.</span><span class="sxs-lookup"><span data-stu-id="bb1ac-110">You can set this value and the [MFPKEY\_FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="bb1ac-111">En cas de décodage, la vidéo est redimensionnée à sa résolution d’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="bb1ac-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="bb1ac-112">Les dimensions de frame valides sur l’un des axes sont commodes de 2 à 8192 pixels.</span><span class="sxs-lookup"><span data-stu-id="bb1ac-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="bb1ac-113">Les dimensions du frame doivent être divisibles par 2.</span><span class="sxs-lookup"><span data-stu-id="bb1ac-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb1ac-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb1ac-114">Requirements</span></span>



| <span data-ttu-id="bb1ac-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb1ac-115">Requirement</span></span> | <span data-ttu-id="bb1ac-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb1ac-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb1ac-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb1ac-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bb1ac-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb1ac-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bb1ac-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb1ac-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bb1ac-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb1ac-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb1ac-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb1ac-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb1ac-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb1ac-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb1ac-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb1ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb1ac-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bb1ac-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




