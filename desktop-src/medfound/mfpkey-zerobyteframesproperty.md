---
description: Spécifie le nombre de trames vidéo ignorées, car il s’agit de doublons de trames précédentes.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: MFPKEY_ZEROBYTEFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863433"
---
# <a name="mfpkey_zerobyteframes-property"></a><span data-ttu-id="88cbe-103">MFPKEY \_ propriété ZEROBYTEFRAMES</span><span class="sxs-lookup"><span data-stu-id="88cbe-103">MFPKEY\_ZEROBYTEFRAMES Property</span></span>

<span data-ttu-id="88cbe-104">Spécifie le nombre de trames vidéo ignorées, car il s’agit de doublons de trames précédentes.</span><span class="sxs-lookup"><span data-stu-id="88cbe-104">Specifies the number of video frames that are skipped because they were duplicates of previous frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="88cbe-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="88cbe-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="88cbe-106">\_wszWMVCZeroByteFrames g</span><span class="sxs-lookup"><span data-stu-id="88cbe-106">g\_wszWMVCZeroByteFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="88cbe-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="88cbe-107">Data Type</span></span>

<span data-ttu-id="88cbe-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="88cbe-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="88cbe-109">Notes</span><span class="sxs-lookup"><span data-stu-id="88cbe-109">Remarks</span></span>

<span data-ttu-id="88cbe-110">Cette valeur n’est pas soustraite du nombre total de frames transmis ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) lors du calcul du nombre de frames encodés ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="88cbe-110">This value is not subtracted from the total number of frames passed ([MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md)) when calculating the number of encoded frames ([MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md)).</span></span>

<span data-ttu-id="88cbe-111">Vous pouvez empêcher le codec d’ignorer les images dupliquées en définissant [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) sur variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="88cbe-111">You can stop the codec from skipping duplicate frames by setting [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) to VARIANT\_TRUE.</span></span>

<span data-ttu-id="88cbe-112">Vous pouvez récupérer cette valeur une fois que vous avez terminé de passer des exemples.</span><span class="sxs-lookup"><span data-stu-id="88cbe-112">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="88cbe-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88cbe-113">Requirements</span></span>



| <span data-ttu-id="88cbe-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88cbe-114">Requirement</span></span> | <span data-ttu-id="88cbe-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="88cbe-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88cbe-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88cbe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="88cbe-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88cbe-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="88cbe-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88cbe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="88cbe-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88cbe-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="88cbe-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="88cbe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="88cbe-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="88cbe-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88cbe-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88cbe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88cbe-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="88cbe-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




