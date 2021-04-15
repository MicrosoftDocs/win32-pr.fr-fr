---
description: Spécifie le paramètre par défaut pour le bit de copyright dans le flux audio MPEG-1. Cette propriété s’applique aux encodeurs audio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Propriété AVEncMPACopyright (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392759"
---
# <a name="avencmpacopyright-property"></a><span data-ttu-id="526c0-104">Propriété AVEncMPACopyright</span><span class="sxs-lookup"><span data-stu-id="526c0-104">AVEncMPACopyright property</span></span>

<span data-ttu-id="526c0-105">Spécifie le paramètre par défaut pour le bit de copyright dans le flux audio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="526c0-105">Specifies the default setting for the copyright bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="526c0-106">Cette propriété s’applique aux encodeurs audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="526c0-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="526c0-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="526c0-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="526c0-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="526c0-108">Data type</span></span>

<span data-ttu-id="526c0-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="526c0-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="526c0-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="526c0-110">Property GUID</span></span>

<span data-ttu-id="526c0-111">**CODECAPI \_ AVEncMPACopyright**</span><span class="sxs-lookup"><span data-stu-id="526c0-111">**CODECAPI\_AVEncMPACopyright**</span></span>

## <a name="property-value"></a><span data-ttu-id="526c0-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="526c0-112">Property value</span></span>

<span data-ttu-id="526c0-113">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="526c0-113">This property can have the following values.</span></span>



| <span data-ttu-id="526c0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="526c0-114">Value</span></span>          | <span data-ttu-id="526c0-115">Description</span><span class="sxs-lookup"><span data-stu-id="526c0-115">Description</span></span>           |
|----------------|-----------------------|
| <span data-ttu-id="526c0-116">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="526c0-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="526c0-117">Le bit de copyright est désactivé.</span><span class="sxs-lookup"><span data-stu-id="526c0-117">Copyright bit is off.</span></span> |
| <span data-ttu-id="526c0-118">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="526c0-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="526c0-119">Le bit de copyright est activé.</span><span class="sxs-lookup"><span data-stu-id="526c0-119">Copyright bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="526c0-120">Notes</span><span class="sxs-lookup"><span data-stu-id="526c0-120">Remarks</span></span>

<span data-ttu-id="526c0-121">L’encodeur peut remplacer ce paramètre en fonction du contenu du flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="526c0-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="526c0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="526c0-122">Requirements</span></span>



| <span data-ttu-id="526c0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="526c0-123">Requirement</span></span> | <span data-ttu-id="526c0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="526c0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="526c0-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="526c0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="526c0-126">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="526c0-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="526c0-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="526c0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="526c0-128">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="526c0-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="526c0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="526c0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="526c0-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="526c0-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="526c0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="526c0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="526c0-132">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="526c0-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="526c0-133">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="526c0-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




