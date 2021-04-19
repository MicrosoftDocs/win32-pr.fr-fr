---
description: Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale (spécifiée par MFPKEY \_ rmax).
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: MFPKEY_BMAX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526943"
---
# <a name="mfpkey_bmax-property"></a><span data-ttu-id="aa10f-103">MFPKEY \_ propriété BMAX</span><span class="sxs-lookup"><span data-stu-id="aa10f-103">MFPKEY\_BMAX Property</span></span>

<span data-ttu-id="aa10f-104">Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale (spécifiée par [MFPKEY \_ Rmax](mfpkey-rmaxproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="aa10f-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by [MFPKEY\_RMAX](mfpkey-rmaxproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="aa10f-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="aa10f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="aa10f-106">\_wszWMVCBMax g</span><span class="sxs-lookup"><span data-stu-id="aa10f-106">g\_wszWMVCBMax</span></span>

## <a name="data-type"></a><span data-ttu-id="aa10f-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="aa10f-107">Data Type</span></span>

<span data-ttu-id="aa10f-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="aa10f-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="aa10f-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="aa10f-109">Default Value</span></span>

<span data-ttu-id="aa10f-110">Aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="aa10f-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa10f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="aa10f-111">Remarks</span></span>

<span data-ttu-id="aa10f-112">Vous devez définir cette valeur pour l’encodage VBR à limitation maximale.</span><span class="sxs-lookup"><span data-stu-id="aa10f-112">You must set this value for peak-constrained VBR encoding.</span></span> <span data-ttu-id="aa10f-113">Une fois que vous avez commencé le traitement des exemples, vous ne devez pas interroger cette valeur tant que vous n’avez pas terminé d’encoder le flux.</span><span class="sxs-lookup"><span data-stu-id="aa10f-113">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="aa10f-114">Le codec interprète une demande pour cette valeur comme un signal indiquant que la session d’encodage est terminée ; l’exemple suivant que vous traitez est traité comme le début d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="aa10f-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa10f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa10f-115">Requirements</span></span>



| <span data-ttu-id="aa10f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa10f-116">Requirement</span></span> | <span data-ttu-id="aa10f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa10f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa10f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa10f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aa10f-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa10f-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aa10f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa10f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aa10f-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa10f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa10f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa10f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa10f-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa10f-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa10f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa10f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa10f-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aa10f-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




