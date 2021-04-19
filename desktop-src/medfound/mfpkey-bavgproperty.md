---
description: Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) contraints à sa vitesse de transmission moyenne (spécifiée par MFPKEY \_ RAVG).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: MFPKEY_BAVG, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518228"
---
# <a name="mfpkey_bavg-property"></a><span data-ttu-id="d9f7c-103">MFPKEY \_ propriété BAVG</span><span class="sxs-lookup"><span data-stu-id="d9f7c-103">MFPKEY\_BAVG Property</span></span>

<span data-ttu-id="d9f7c-104">Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) contraints à sa vitesse de transmission moyenne (spécifiée par [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="d9f7c-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by [MFPKEY\_RAVG](mfpkey-ravgproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d9f7c-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d9f7c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d9f7c-106">\_wszWMVCBAvg g</span><span class="sxs-lookup"><span data-stu-id="d9f7c-106">g\_wszWMVCBAvg</span></span>

## <a name="data-type"></a><span data-ttu-id="d9f7c-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="d9f7c-107">Data Type</span></span>

<span data-ttu-id="d9f7c-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="d9f7c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d9f7c-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="d9f7c-109">Default Value</span></span>

<span data-ttu-id="d9f7c-110">Aucune valeur par défaut, mais le codec calcule une valeur appropriée en fonction des autres paramètres VBR restreints.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-110">No default value, but the codec will compute an appropriate value based on the other constrained VBR settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f7c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d9f7c-111">Remarks</span></span>

<span data-ttu-id="d9f7c-112">Cette valeur est calculée par le codec après l’étape d’encodage finale.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-112">This value is computed by the codec after the final encoding pass.</span></span> <span data-ttu-id="d9f7c-113">Vous ne devez pas interroger cette valeur tant que l’encodage n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-113">You should not query for this value until after encoding is complete.</span></span> <span data-ttu-id="d9f7c-114">Le codec interprète une demande pour cette valeur comme un signal indiquant que la session d’encodage est terminée ; l’exemple suivant que vous traitez est traité comme le début d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f7c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9f7c-115">Requirements</span></span>



| <span data-ttu-id="d9f7c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9f7c-116">Requirement</span></span> | <span data-ttu-id="d9f7c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9f7c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f7c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9f7c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d9f7c-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9f7c-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d9f7c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9f7c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d9f7c-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9f7c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9f7c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9f7c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9f7c-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9f7c-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f7c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9f7c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f7c-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d9f7c-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




