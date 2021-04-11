---
description: Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour la lecture VBR (variable-bit-rate) avec restriction à 2 passes.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: MFPKEY_RMAX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202321"
---
# <a name="mfpkey_rmax-property"></a><span data-ttu-id="079b0-103">MFPKEY \_ propriété Rmax</span><span class="sxs-lookup"><span data-stu-id="079b0-103">MFPKEY\_RMAX Property</span></span>

<span data-ttu-id="079b0-104">Spécifie le taux de bits de pointe, en bits par seconde, utilisé pour la lecture VBR (variable-bit-rate) avec restriction à 2 passes.</span><span class="sxs-lookup"><span data-stu-id="079b0-104">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) playback.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="079b0-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="079b0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="079b0-106">\_wszWMVCMaxBitrate g</span><span class="sxs-lookup"><span data-stu-id="079b0-106">g\_wszWMVCMaxBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="079b0-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="079b0-107">Data Type</span></span>

<span data-ttu-id="079b0-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="079b0-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="079b0-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="079b0-109">Default Value</span></span>

<span data-ttu-id="079b0-110">Aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="079b0-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="079b0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="079b0-111">Remarks</span></span>

<span data-ttu-id="079b0-112">Cette valeur représente le taux binaire de pointe pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="079b0-112">This value represents the peak bit rate for playback.</span></span> <span data-ttu-id="079b0-113">La valeur de [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) est utilisée pour décrire la mémoire tampon en termes de vitesse de transmission ; en effet, le VBR restreint est semblable au taux binaire constant (CBR) qui utilise cette valeur comme vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="079b0-113">The value of [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is used to describe the buffer in terms of this bit rate; in effect, constrained VBR is similar to constant bit rate (CBR) using this value as the bit rate.</span></span> <span data-ttu-id="079b0-114">Toutefois, un flux VBR restreint peut être lu à une vitesse de transmission inférieure, à condition que la mémoire tampon soit augmentée.</span><span class="sxs-lookup"><span data-stu-id="079b0-114">However, a constrained VBR stream can be played back at a lower bit rate, as long as the buffer is increased.</span></span>

<span data-ttu-id="079b0-115">Vous devez définir cette valeur pour l’encodage VBR à double passage restreint.</span><span class="sxs-lookup"><span data-stu-id="079b0-115">You must set this value for peak-constrained two-pass VBR encoding.</span></span> <span data-ttu-id="079b0-116">Une fois que vous avez commencé le traitement des exemples, vous ne devez pas interroger cette valeur tant que vous n’avez pas terminé d’encoder le flux.</span><span class="sxs-lookup"><span data-stu-id="079b0-116">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="079b0-117">L’encodeur interprète une demande pour cette valeur comme un signal indiquant que la session d’encodage est terminée ; l’exemple suivant que vous traitez est traité comme le début d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="079b0-117">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="079b0-118">En général, cette valeur est deux à trois fois supérieure à la valeur de [MFPKEY \_ RAVG](mfpkey-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="079b0-118">Typically, this value is two to three times greater than the value of [MFPKEY\_RAVG](mfpkey-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="079b0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="079b0-119">Requirements</span></span>



| <span data-ttu-id="079b0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="079b0-120">Requirement</span></span> | <span data-ttu-id="079b0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="079b0-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="079b0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="079b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="079b0-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="079b0-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="079b0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="079b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="079b0-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="079b0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="079b0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="079b0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="079b0-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="079b0-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="079b0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="079b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="079b0-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="079b0-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




