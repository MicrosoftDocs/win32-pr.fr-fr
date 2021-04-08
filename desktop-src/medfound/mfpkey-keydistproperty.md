---
description: Spécifie la durée maximale, en millisecondes, entre les images clés de la sortie du codec.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: MFPKEY_KEYDIST, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864153"
---
# <a name="mfpkey_keydist-property"></a><span data-ttu-id="1df34-103">MFPKEY, \_ propriété de KEYdist</span><span class="sxs-lookup"><span data-stu-id="1df34-103">MFPKEY\_KEYDIST Property</span></span>

<span data-ttu-id="1df34-104">Spécifie la durée maximale, en millisecondes, entre les images clés de la sortie du codec.</span><span class="sxs-lookup"><span data-stu-id="1df34-104">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1df34-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1df34-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1df34-106">\_wszWMVCKeyframeDistance g</span><span class="sxs-lookup"><span data-stu-id="1df34-106">g\_wszWMVCKeyframeDistance</span></span>

## <a name="data-type"></a><span data-ttu-id="1df34-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="1df34-107">Data Type</span></span>

<span data-ttu-id="1df34-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="1df34-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1df34-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="1df34-109">Default Value</span></span>

<span data-ttu-id="1df34-110">La valeur par défaut dépend de la version de Windows en cours d’exécution, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1df34-110">The default value depends on which version of Windows is running, as shown in the following table.</span></span>



| <span data-ttu-id="1df34-111">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="1df34-111">Operating system</span></span> | <span data-ttu-id="1df34-112">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="1df34-112">Default value</span></span> |
|------------------|---------------|
| <span data-ttu-id="1df34-113">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1df34-113">Windows XP</span></span>       | <span data-ttu-id="1df34-114">8000</span><span class="sxs-lookup"><span data-stu-id="1df34-114">8000</span></span>          |
| <span data-ttu-id="1df34-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1df34-115">Windows Vista</span></span>    | <span data-ttu-id="1df34-116">8000</span><span class="sxs-lookup"><span data-stu-id="1df34-116">8000</span></span>          |
| <span data-ttu-id="1df34-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1df34-117">Windows 7</span></span>        | <span data-ttu-id="1df34-118">2000</span><span class="sxs-lookup"><span data-stu-id="1df34-118">2000</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="1df34-119">Notes</span><span class="sxs-lookup"><span data-stu-id="1df34-119">Remarks</span></span>

<span data-ttu-id="1df34-120">La logique interne du codec détermine l’emplacement réel de chaque image clé.</span><span class="sxs-lookup"><span data-stu-id="1df34-120">The internal logic of the codec determines the actual location of each key frame.</span></span> <span data-ttu-id="1df34-121">La distance entre deux images clés quelconques peut être inférieure à la valeur de cette propriété, mais elle ne sera jamais supérieure.</span><span class="sxs-lookup"><span data-stu-id="1df34-121">The distance between any two key frames may be less than the value of this property, however, it will never be greater.</span></span>

## <a name="requirements"></a><span data-ttu-id="1df34-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1df34-122">Requirements</span></span>



| <span data-ttu-id="1df34-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1df34-123">Requirement</span></span> | <span data-ttu-id="1df34-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1df34-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1df34-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1df34-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1df34-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1df34-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1df34-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1df34-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1df34-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1df34-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1df34-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1df34-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1df34-130"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1df34-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df34-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1df34-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df34-132">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1df34-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




