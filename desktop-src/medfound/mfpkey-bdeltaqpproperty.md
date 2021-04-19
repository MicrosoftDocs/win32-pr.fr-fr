---
description: Spécifie l’augmentation Delta entre le quantificateur d’image du frame d’ancrage et le quantificateur d’image du cadre B.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: MFPKEY_BDELTAQP, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106537012"
---
# <a name="mfpkey_bdeltaqp-property"></a><span data-ttu-id="f0885-103">MFPKEY \_ propriété BDELTAQP</span><span class="sxs-lookup"><span data-stu-id="f0885-103">MFPKEY\_BDELTAQP Property</span></span>

<span data-ttu-id="f0885-104">Spécifie l’augmentation Delta entre le quantificateur d’image du frame d’ancrage et le quantificateur d’image du cadre B.</span><span class="sxs-lookup"><span data-stu-id="f0885-104">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f0885-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f0885-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f0885-106">\_wszWMVCBDeltaQP g</span><span class="sxs-lookup"><span data-stu-id="f0885-106">g\_wszWMVCBDeltaQP</span></span>

## <a name="data-type"></a><span data-ttu-id="f0885-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="f0885-107">Data Type</span></span>

<span data-ttu-id="f0885-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="f0885-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f0885-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f0885-109">Default Value</span></span>

<span data-ttu-id="f0885-110">0</span><span class="sxs-lookup"><span data-stu-id="f0885-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="f0885-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f0885-111">Remarks</span></span>

<span data-ttu-id="f0885-112">Le quantificateur d’image (QP) est une mesure de la compression d’un cadre.</span><span class="sxs-lookup"><span data-stu-id="f0885-112">Picture quantizer (QP) is a measurement of how compressed a frame is.</span></span> <span data-ttu-id="f0885-113">Des valeurs plus élevées représentent des taux de compression plus élevés.</span><span class="sxs-lookup"><span data-stu-id="f0885-113">Higher values represent higher compression ratios.</span></span> <span data-ttu-id="f0885-114">Le QP peut être défini par incréments de demi-point.</span><span class="sxs-lookup"><span data-stu-id="f0885-114">The QP can be set in half-point increments.</span></span> <span data-ttu-id="f0885-115">Un frame B est généralement compressé à un QP de la même façon que ou 0,5 plus haut que le QP du frame d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="f0885-115">A B-frame is typically compressed at a QP the same as or 0.5 higher than the anchor frame's QP.</span></span> <span data-ttu-id="f0885-116">En spécifiant un delta de trame de B-Frame supérieur à 0, il est possible de compresser les images B à un taux de compression encore plus élevé.</span><span class="sxs-lookup"><span data-stu-id="f0885-116">By specifying a B-frame QP delta higher than 0, it is possible to compress B-frames at an even higher compression ratio.</span></span>

<span data-ttu-id="f0885-117">Le delta du frame B ne peut être défini que dans des incréments de point entier.</span><span class="sxs-lookup"><span data-stu-id="f0885-117">The B-frame delta QP can be set only in whole-point increments.</span></span> <span data-ttu-id="f0885-118">Cette propriété doit être définie sur une valeur entière comprise entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="f0885-118">This property must be set to an integer value from 0 to 31.</span></span> <span data-ttu-id="f0885-119">La valeur recommandée est 1.</span><span class="sxs-lookup"><span data-stu-id="f0885-119">The recommended value is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0885-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0885-120">Requirements</span></span>



| <span data-ttu-id="f0885-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0885-121">Requirement</span></span> | <span data-ttu-id="f0885-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0885-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0885-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0885-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f0885-124">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0885-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f0885-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0885-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f0885-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0885-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0885-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0885-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0885-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0885-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0885-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0885-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0885-130">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0885-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




