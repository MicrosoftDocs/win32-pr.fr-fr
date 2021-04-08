---
description: Spécifie si l’encodeur produit des groupes d’images ouverts (GOP secondes) ou des GOP secondes fermés. Cette propriété s’applique aux encodeurs vidéo MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Propriété AVEncMPVGOPOpen (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746925"
---
# <a name="avencmpvgopopen-property"></a><span data-ttu-id="86e10-104">Propriété AVEncMPVGOPOpen</span><span class="sxs-lookup"><span data-stu-id="86e10-104">AVEncMPVGOPOpen property</span></span>

<span data-ttu-id="86e10-105">Spécifie si l’encodeur produit des groupes d’images ouverts (GOP secondes) ou des GOP secondes fermés.</span><span class="sxs-lookup"><span data-stu-id="86e10-105">Specifies whether the encoder produces open groups of pictures (GOPs) or closed GOPs.</span></span> <span data-ttu-id="86e10-106">Cette propriété s’applique aux encodeurs vidéo MPEG.</span><span class="sxs-lookup"><span data-stu-id="86e10-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="86e10-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="86e10-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="86e10-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="86e10-108">Data type</span></span>

<span data-ttu-id="86e10-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="86e10-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="86e10-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="86e10-110">Property GUID</span></span>

<span data-ttu-id="86e10-111">**CODECAPI \_ AVEncMPVGOPOpen**</span><span class="sxs-lookup"><span data-stu-id="86e10-111">**CODECAPI\_AVEncMPVGOPOpen**</span></span>

## <a name="property-value"></a><span data-ttu-id="86e10-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="86e10-112">Property value</span></span>



| <span data-ttu-id="86e10-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="86e10-113">Value</span></span>          | <span data-ttu-id="86e10-114">Description</span><span class="sxs-lookup"><span data-stu-id="86e10-114">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="86e10-115">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="86e10-115">VARIANT\_FALSE</span></span> | <span data-ttu-id="86e10-116">GOP secondes fermé</span><span class="sxs-lookup"><span data-stu-id="86e10-116">Closed GOPs</span></span> |
| <span data-ttu-id="86e10-117">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="86e10-117">VARIANT\_TRUE</span></span>  | <span data-ttu-id="86e10-118">Ouvrir GOP secondes</span><span class="sxs-lookup"><span data-stu-id="86e10-118">Open GOPs</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="86e10-119">Notes</span><span class="sxs-lookup"><span data-stu-id="86e10-119">Remarks</span></span>

<span data-ttu-id="86e10-120">Un groupe d’images ouvert contient des frames Delta qui référencent des frames du groupe d’images précédent.</span><span class="sxs-lookup"><span data-stu-id="86e10-120">An open GOP contains delta frames that reference frames from the previous GOP.</span></span> <span data-ttu-id="86e10-121">Un groupe d’images fermé ne contient pas de frame Delta qui référencent le groupe d’images précédent.</span><span class="sxs-lookup"><span data-stu-id="86e10-121">A closed GOP does not contain any delta frames that reference the previous GOP.</span></span>

## <a name="requirements"></a><span data-ttu-id="86e10-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86e10-122">Requirements</span></span>



| <span data-ttu-id="86e10-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86e10-123">Requirement</span></span> | <span data-ttu-id="86e10-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="86e10-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86e10-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86e10-125">Minimum supported client</span></span><br/> | <span data-ttu-id="86e10-126">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="86e10-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="86e10-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86e10-127">Minimum supported server</span></span><br/> | <span data-ttu-id="86e10-128">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="86e10-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="86e10-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="86e10-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="86e10-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="86e10-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e10-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86e10-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e10-132">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="86e10-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="86e10-133">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="86e10-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




