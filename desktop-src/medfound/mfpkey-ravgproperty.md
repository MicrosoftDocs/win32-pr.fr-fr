---
description: Spécifie la vitesse de transmission moyenne, en bits par seconde, utilisée pour l’encodage à 2 passes, variable-bit-rate (VBR).
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: MFPKEY_RAVG, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519641"
---
# <a name="mfpkey_ravg-property"></a><span data-ttu-id="18f31-103">MFPKEY \_ propriété RAVG</span><span class="sxs-lookup"><span data-stu-id="18f31-103">MFPKEY\_RAVG Property</span></span>

<span data-ttu-id="18f31-104">Spécifie la vitesse de transmission moyenne, en bits par seconde, utilisée pour l’encodage à 2 passes, variable-bit-rate (VBR).</span><span class="sxs-lookup"><span data-stu-id="18f31-104">Specifies the average bit rate, in bits per second, used for 2-pass, variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="18f31-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="18f31-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="18f31-106">\_wszWMVCAvgBitrate g</span><span class="sxs-lookup"><span data-stu-id="18f31-106">g\_wszWMVCAvgBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="18f31-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="18f31-107">Data Type</span></span>

<span data-ttu-id="18f31-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="18f31-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="18f31-109">Notes</span><span class="sxs-lookup"><span data-stu-id="18f31-109">Remarks</span></span>

<span data-ttu-id="18f31-110">Dans les deux cas, cette valeur correspond à la vitesse de transmission moyenne sur toute la durée du contenu.</span><span class="sxs-lookup"><span data-stu-id="18f31-110">In both constrained and unconstrained VBR, this value is the average bit rate across the duration of the content.</span></span>

<span data-ttu-id="18f31-111">Vous devez définir cette valeur pour les deux modes d’encodage VBR en deux passes.</span><span class="sxs-lookup"><span data-stu-id="18f31-111">You must set this value for both modes of two-pass VBR encoding.</span></span> <span data-ttu-id="18f31-112">Une fois que vous avez commencé le traitement des exemples, vous ne devez pas interroger cette valeur tant que vous n’avez pas terminé d’encoder le flux.</span><span class="sxs-lookup"><span data-stu-id="18f31-112">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="18f31-113">L’encodeur interprète une demande pour cette valeur comme un signal indiquant que la session d’encodage est terminée ; l’exemple suivant que vous traitez est traité comme le début d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="18f31-113">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="18f31-114">Cette propriété peut également être lue à la fin d’une session d’encodage VBR à 1 passage.</span><span class="sxs-lookup"><span data-stu-id="18f31-114">This property can also be read at the end of a 1-pass VBR encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="18f31-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18f31-115">Requirements</span></span>



| <span data-ttu-id="18f31-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18f31-116">Requirement</span></span> | <span data-ttu-id="18f31-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="18f31-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18f31-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18f31-118">Minimum supported client</span></span><br/> | <span data-ttu-id="18f31-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18f31-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="18f31-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18f31-120">Minimum supported server</span></span><br/> | <span data-ttu-id="18f31-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18f31-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18f31-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="18f31-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="18f31-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="18f31-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18f31-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18f31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f31-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18f31-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




