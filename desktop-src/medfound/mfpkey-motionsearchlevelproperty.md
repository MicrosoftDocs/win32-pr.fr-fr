---
description: Spécifie comment les informations de couleur sont utilisées dans les opérations de recherche de mouvement.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: MFPKEY_MOTIONSEARCHLEVEL, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034334"
---
# <a name="mfpkey_motionsearchlevel-property"></a><span data-ttu-id="13952-103">MFPKEY \_ propriété MOTIONSEARCHLEVEL</span><span class="sxs-lookup"><span data-stu-id="13952-103">MFPKEY\_MOTIONSEARCHLEVEL Property</span></span>

<span data-ttu-id="13952-104">Spécifie comment les informations de couleur sont utilisées dans les opérations de recherche de mouvement.</span><span class="sxs-lookup"><span data-stu-id="13952-104">Specifies how color information is used in motion search operations.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="13952-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="13952-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="13952-106">\_wszWMVCMotionSearchLevel g</span><span class="sxs-lookup"><span data-stu-id="13952-106">g\_wszWMVCMotionSearchLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="13952-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="13952-107">Data Type</span></span>

<span data-ttu-id="13952-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="13952-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="13952-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="13952-109">Default Value</span></span>

<span data-ttu-id="13952-110">0</span><span class="sxs-lookup"><span data-stu-id="13952-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="13952-111">Notes</span><span class="sxs-lookup"><span data-stu-id="13952-111">Remarks</span></span>

<span data-ttu-id="13952-112">Cette propriété peut être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="13952-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="13952-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="13952-113">Value</span></span> | <span data-ttu-id="13952-114">Informations vidéo utilisées</span><span class="sxs-lookup"><span data-stu-id="13952-114">Video information used</span></span>                           |
|-------|--------------------------------------------------|
| <span data-ttu-id="13952-115">0</span><span class="sxs-lookup"><span data-stu-id="13952-115">0</span></span>     | <span data-ttu-id="13952-116">Luminance uniquement.</span><span class="sxs-lookup"><span data-stu-id="13952-116">Luma only.</span></span>                                       |
| <span data-ttu-id="13952-117">1</span><span class="sxs-lookup"><span data-stu-id="13952-117">1</span></span>     | <span data-ttu-id="13952-118">Luminance avec Chroma entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="13952-118">Luma with nearest-integer chroma.</span></span>                |
| <span data-ttu-id="13952-119">2</span><span class="sxs-lookup"><span data-stu-id="13952-119">2</span></span>     | <span data-ttu-id="13952-120">Luminance avec chroma vrai.</span><span class="sxs-lookup"><span data-stu-id="13952-120">Luma with true chroma.</span></span>                           |
| <span data-ttu-id="13952-121">-1</span><span class="sxs-lookup"><span data-stu-id="13952-121">-1</span></span>    | <span data-ttu-id="13952-122">Bloc macro-adaptative avec vrai Chroma.</span><span class="sxs-lookup"><span data-stu-id="13952-122">Macroblock-adaptive with true chroma.</span></span>            |
| <span data-ttu-id="13952-123">-2</span><span class="sxs-lookup"><span data-stu-id="13952-123">-2</span></span>    | <span data-ttu-id="13952-124">Bloc macro-adaptative avec Chroma d’entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="13952-124">Macroblock-adaptive with nearest-integer chroma.</span></span> |



 

<span data-ttu-id="13952-125">Par défaut, le codec effectue une recherche de mouvement uniquement dans le canal de luminance.</span><span class="sxs-lookup"><span data-stu-id="13952-125">By default, the codec performs motion search only in the luma channel.</span></span> <span data-ttu-id="13952-126">L’inclusion d’informations Chroma dans l’estimation de mouvement peut améliorer considérablement la qualité de la vidéo encodée.</span><span class="sxs-lookup"><span data-stu-id="13952-126">Including chroma information in motion estimation can significantly improve the quality of encoded video.</span></span> <span data-ttu-id="13952-127">La recherche de mouvement avec la luminance et la chrominance réelle produira la meilleure qualité vidéo, mais à un coût de performances optimal.</span><span class="sxs-lookup"><span data-stu-id="13952-127">Motion search with luma and true chroma will yield the best video quality, but at the highest performance cost.</span></span> <span data-ttu-id="13952-128">Les deux modes dynamiques (-1 et-2) et la luminance avec le mode Chroma entier le plus proche fournissent des compromis raisonnables entre qualité et performances.</span><span class="sxs-lookup"><span data-stu-id="13952-128">The two dynamic modes (-1 and -2) and the luma with nearest-integer chroma mode will provide reasonable compromises between quality and performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="13952-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13952-129">Requirements</span></span>



| <span data-ttu-id="13952-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13952-130">Requirement</span></span> | <span data-ttu-id="13952-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="13952-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13952-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13952-132">Minimum supported client</span></span><br/> | <span data-ttu-id="13952-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13952-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="13952-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13952-134">Minimum supported server</span></span><br/> | <span data-ttu-id="13952-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13952-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13952-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="13952-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="13952-137"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="13952-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13952-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13952-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13952-139">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="13952-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




