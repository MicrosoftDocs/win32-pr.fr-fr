---
description: Spécifie la méthode utilisée pour encoder les informations de vecteur de mouvement.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: MFPKEY_DELTAMVRANGEINDEX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528677"
---
# <a name="mfpkey_deltamvrangeindex-property"></a><span data-ttu-id="e20a0-103">MFPKEY \_ propriété DELTAMVRANGEINDEX</span><span class="sxs-lookup"><span data-stu-id="e20a0-103">MFPKEY\_DELTAMVRANGEINDEX Property</span></span>

<span data-ttu-id="e20a0-104">Spécifie la méthode utilisée pour encoder les informations de vecteur de mouvement.</span><span class="sxs-lookup"><span data-stu-id="e20a0-104">Specifies the method used to encode the motion vector information.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e20a0-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e20a0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e20a0-106">\_wszWMVCDeltaMVRangeIndex g</span><span class="sxs-lookup"><span data-stu-id="e20a0-106">g\_wszWMVCDeltaMVRangeIndex</span></span>

## <a name="data-type"></a><span data-ttu-id="e20a0-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="e20a0-107">Data Type</span></span>

<span data-ttu-id="e20a0-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="e20a0-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="e20a0-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e20a0-109">Default Value</span></span>

<span data-ttu-id="e20a0-110">0</span><span class="sxs-lookup"><span data-stu-id="e20a0-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="e20a0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e20a0-111">Remarks</span></span>

<span data-ttu-id="e20a0-112">Si cette propriété est définie, l’encodeur augmente la plage du vecteur de mouvement Delta dans les champs.</span><span class="sxs-lookup"><span data-stu-id="e20a0-112">If this property is set, the encoder increases the delta motion vector range in fields.</span></span> <span data-ttu-id="e20a0-113">Les informations de vecteur de mouvement ne sont valides que pour les champs entrelacés.</span><span class="sxs-lookup"><span data-stu-id="e20a0-113">Motion vector information is valid only for interlaced fields.</span></span>

<span data-ttu-id="e20a0-114">Cette propriété peut être définie sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e20a0-114">This property may be set to one of the following values:</span></span>



| <span data-ttu-id="e20a0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e20a0-115">Value</span></span> | <span data-ttu-id="e20a0-116">Description</span><span class="sxs-lookup"><span data-stu-id="e20a0-116">Description</span></span>                                                                          |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e20a0-117">0</span><span class="sxs-lookup"><span data-stu-id="e20a0-117">0</span></span>     | <span data-ttu-id="e20a0-118">Utilisez la plage de vecteurs de mouvement Delta existante.</span><span class="sxs-lookup"><span data-stu-id="e20a0-118">Use the existing delta motion vector range.</span></span>                                          |
| <span data-ttu-id="e20a0-119">1</span><span class="sxs-lookup"><span data-stu-id="e20a0-119">1</span></span>     | <span data-ttu-id="e20a0-120">Doublez la plage du vecteur de mouvement Delta dans le sens horizontal.</span><span class="sxs-lookup"><span data-stu-id="e20a0-120">Double the delta motion vector range in the horizontal direction.</span></span>                    |
| <span data-ttu-id="e20a0-121">2</span><span class="sxs-lookup"><span data-stu-id="e20a0-121">2</span></span>     | <span data-ttu-id="e20a0-122">Doublez la plage du vecteur de mouvement Delta dans le sens vertical.</span><span class="sxs-lookup"><span data-stu-id="e20a0-122">Double the delta motion vector range in the vertical direction.</span></span>                      |
| <span data-ttu-id="e20a0-123">3</span><span class="sxs-lookup"><span data-stu-id="e20a0-123">3</span></span>     | <span data-ttu-id="e20a0-124">Doublez la plage du vecteur de mouvement Delta dans les directions horizontale et verticale.</span><span class="sxs-lookup"><span data-stu-id="e20a0-124">Double the delta motion vector range in both the horizontal and vertical directions.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e20a0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e20a0-125">Requirements</span></span>



| <span data-ttu-id="e20a0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e20a0-126">Requirement</span></span> | <span data-ttu-id="e20a0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e20a0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e20a0-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e20a0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e20a0-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e20a0-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e20a0-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e20a0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e20a0-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e20a0-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e20a0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e20a0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e20a0-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e20a0-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e20a0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e20a0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20a0-135">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e20a0-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




