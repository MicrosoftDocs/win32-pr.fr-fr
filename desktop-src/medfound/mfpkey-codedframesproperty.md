---
description: Spécifie le nombre de trames vidéo encodées par le codec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: MFPKEY_CODEDFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530596"
---
# <a name="mfpkey_codedframes-property"></a><span data-ttu-id="0acfd-103">MFPKEY \_ propriété CODEDFRAMES</span><span class="sxs-lookup"><span data-stu-id="0acfd-103">MFPKEY\_CODEDFRAMES Property</span></span>

<span data-ttu-id="0acfd-104">Spécifie le nombre de trames vidéo encodées par le codec.</span><span class="sxs-lookup"><span data-stu-id="0acfd-104">Specifies the number of video frames encoded by the codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0acfd-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0acfd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0acfd-106">\_wszWMVCCodedFrames g</span><span class="sxs-lookup"><span data-stu-id="0acfd-106">g\_wszWMVCCodedFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="0acfd-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="0acfd-107">Data Type</span></span>

<span data-ttu-id="0acfd-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="0acfd-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="0acfd-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0acfd-109">Remarks</span></span>

<span data-ttu-id="0acfd-110">Cette valeur est égale à [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) moins les images qui ont été supprimées en raison de contraintes de vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="0acfd-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints.</span></span> <span data-ttu-id="0acfd-111">Vous pouvez récupérer cette valeur une fois que vous avez terminé de passer des exemples.</span><span class="sxs-lookup"><span data-stu-id="0acfd-111">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="0acfd-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0acfd-112">Requirements</span></span>



| <span data-ttu-id="0acfd-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0acfd-113">Requirement</span></span> | <span data-ttu-id="0acfd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0acfd-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0acfd-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0acfd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0acfd-116">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0acfd-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0acfd-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0acfd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0acfd-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0acfd-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0acfd-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="0acfd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0acfd-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0acfd-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0acfd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0acfd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0acfd-122">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0acfd-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




