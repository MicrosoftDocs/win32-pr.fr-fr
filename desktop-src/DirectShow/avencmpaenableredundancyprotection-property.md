---
description: Spécifie s’il faut ajouter une vérification de redondance cyclique (CRC) à l’en-tête de trame. Cette propriété s’applique aux encodeurs audio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Propriété AVEncMPAEnableRedundancyProtection (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515320"
---
# <a name="avencmpaenableredundancyprotection-property"></a><span data-ttu-id="75fc9-104">Propriété AVEncMPAEnableRedundancyProtection</span><span class="sxs-lookup"><span data-stu-id="75fc9-104">AVEncMPAEnableRedundancyProtection property</span></span>

<span data-ttu-id="75fc9-105">Spécifie s’il faut ajouter une vérification de redondance cyclique (CRC) à l’en-tête de trame.</span><span class="sxs-lookup"><span data-stu-id="75fc9-105">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span> <span data-ttu-id="75fc9-106">Cette propriété s’applique aux encodeurs audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="75fc9-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="75fc9-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="75fc9-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="75fc9-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="75fc9-108">Data type</span></span>

<span data-ttu-id="75fc9-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="75fc9-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="75fc9-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="75fc9-110">Property GUID</span></span>

<span data-ttu-id="75fc9-111">**CODECAPI \_ AVEncMPAEnableRedundancyProtection**</span><span class="sxs-lookup"><span data-stu-id="75fc9-111">**CODECAPI\_AVEncMPAEnableRedundancyProtection**</span></span>

## <a name="property-value"></a><span data-ttu-id="75fc9-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="75fc9-112">Property value</span></span>

<span data-ttu-id="75fc9-113">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="75fc9-113">This property can have the following values.</span></span>



| <span data-ttu-id="75fc9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="75fc9-114">Value</span></span>          | <span data-ttu-id="75fc9-115">Description</span><span class="sxs-lookup"><span data-stu-id="75fc9-115">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="75fc9-116">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="75fc9-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="75fc9-117">N’ajoutez pas de somme de contrôle CRC.</span><span class="sxs-lookup"><span data-stu-id="75fc9-117">Do not add a CRC checksum.</span></span> |
| <span data-ttu-id="75fc9-118">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="75fc9-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="75fc9-119">Ajoutez une somme de contrôle CRC.</span><span class="sxs-lookup"><span data-stu-id="75fc9-119">Add a CRC checksum.</span></span>        |



 

## <a name="requirements"></a><span data-ttu-id="75fc9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75fc9-120">Requirements</span></span>



| <span data-ttu-id="75fc9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75fc9-121">Requirement</span></span> | <span data-ttu-id="75fc9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="75fc9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75fc9-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75fc9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="75fc9-124">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="75fc9-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="75fc9-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75fc9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="75fc9-126">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="75fc9-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="75fc9-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="75fc9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="75fc9-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="75fc9-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75fc9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75fc9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75fc9-130">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="75fc9-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="75fc9-131">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="75fc9-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




