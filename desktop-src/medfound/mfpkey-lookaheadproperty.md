---
description: Spécifie le nombre de frames après le frame actuel que le codec évaluera avant d’encoder le frame actuel.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: MFPKEY_LOOKAHEAD, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520510"
---
# <a name="mfpkey_lookahead-property"></a><span data-ttu-id="ff09d-103">\_Propriété de préanalyse MFPKEY</span><span class="sxs-lookup"><span data-stu-id="ff09d-103">MFPKEY\_LOOKAHEAD Property</span></span>

<span data-ttu-id="ff09d-104">Spécifie le nombre de frames après le frame actuel que le codec évaluera avant d’encoder le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="ff09d-104">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ff09d-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ff09d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ff09d-106">\_wszWMVCLookAhead g</span><span class="sxs-lookup"><span data-stu-id="ff09d-106">g\_wszWMVCLookAhead</span></span>

## <a name="data-type"></a><span data-ttu-id="ff09d-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="ff09d-107">Data Type</span></span>

<span data-ttu-id="ff09d-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="ff09d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ff09d-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ff09d-109">Default Value</span></span>

<span data-ttu-id="ff09d-110">0</span><span class="sxs-lookup"><span data-stu-id="ff09d-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="ff09d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ff09d-111">Remarks</span></span>

<span data-ttu-id="ff09d-112">Lorsque le codec utilise la préanalyse, il peut encoder la vidéo plus efficacement.</span><span class="sxs-lookup"><span data-stu-id="ff09d-112">When the codec uses lookahead, it can encode the video more efficiently.</span></span>

<span data-ttu-id="ff09d-113">L’objet Writer du kit de développement logiciel (SDK) Windows Media format s’attend à ce que le codec Encode chaque exemple immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ff09d-113">The writer object of the Windows Media Format SDK expects the codec to encode each sample immediately.</span></span> <span data-ttu-id="ff09d-114">Par conséquent, cette fonctionnalité ne fonctionne pas correctement dans les logiciels qui utilisent l’objet Writer (y compris Windows Media Encoder et Windows Media Player).</span><span class="sxs-lookup"><span data-stu-id="ff09d-114">As a result, this feature does not work properly in software that uses the writer object (including Windows Media Encoder and Windows Media Player).</span></span> <span data-ttu-id="ff09d-115">Toutes les extensions d’unité de données associées aux images vidéo sont attachées à une trame de sortie incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ff09d-115">Any data unit extensions associated with video frames will be attached to the wrong output frame.</span></span> <span data-ttu-id="ff09d-116">Le nombre de frames par lequel les extensions d’unité de données sont mal placées est égal au nombre de trames de la préanalyse utilisées.</span><span class="sxs-lookup"><span data-stu-id="ff09d-116">The number of frames by which the data unit extensions are misplaced is equal to the number of frames of lookahead that are used.</span></span>

<span data-ttu-id="ff09d-117">Les valeurs de préanalyse valides sont comprises entre 0 et 16 frames.</span><span class="sxs-lookup"><span data-stu-id="ff09d-117">Valid lookahead values range from 0 to 16 frames.</span></span> <span data-ttu-id="ff09d-118">La valeur recommandée est 16.</span><span class="sxs-lookup"><span data-stu-id="ff09d-118">The recommended value is 16.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff09d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff09d-119">Requirements</span></span>



| <span data-ttu-id="ff09d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff09d-120">Requirement</span></span> | <span data-ttu-id="ff09d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff09d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff09d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff09d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ff09d-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff09d-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ff09d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff09d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ff09d-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff09d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff09d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff09d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff09d-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff09d-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff09d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff09d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff09d-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ff09d-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




