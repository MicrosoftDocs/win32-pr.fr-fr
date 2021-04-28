---
description: AM_RATE_ReverseMaxFullDataRate propriété-s’applique à Windows Vista et versions ultérieures.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e70a330433c8ea6e8116db944d8fb3d2ffff4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099967"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="7f465-103">\_ \_ Propriété REVERSEMAXFULLDATARATE rate AM</span><span class="sxs-lookup"><span data-stu-id="7f465-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="7f465-104">S’applique à Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7f465-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="7f465-105">Retourne la vitesse de lecture inversée maximale du décodeur.</span><span class="sxs-lookup"><span data-stu-id="7f465-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="7f465-106">La valeur de la propriété est la valeur absolue de la vitesse inversée maximale x 10000.</span><span class="sxs-lookup"><span data-stu-id="7f465-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="7f465-107">Par exemple, si la vitesse inversée maximale est-2,0, la valeur de cette propriété est 20000.</span><span class="sxs-lookup"><span data-stu-id="7f465-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="7f465-108">Le type de données de cette propriété **est \_ MaxFullDataRate**, qui est `typedef` de type **long**.</span><span class="sxs-lookup"><span data-stu-id="7f465-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="7f465-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7f465-109">This property is read-only.</span></span>



| <span data-ttu-id="7f465-110">Étiquette</span><span class="sxs-lookup"><span data-stu-id="7f465-110">Label</span></span> | <span data-ttu-id="7f465-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f465-111">Value</span></span> |
|-------------------|----------------------------------|
| <span data-ttu-id="7f465-112">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="7f465-112">Property Set GUID</span></span> | <span data-ttu-id="7f465-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="7f465-113">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="7f465-114">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="7f465-114">Property ID</span></span>       | <span data-ttu-id="7f465-115">\_Taux am \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="7f465-115">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="7f465-116">Type de données</span><span class="sxs-lookup"><span data-stu-id="7f465-116">Data Type</span></span>         | <span data-ttu-id="7f465-117">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="7f465-117">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="7f465-118">Notes </span><span class="sxs-lookup"><span data-stu-id="7f465-118">Remarks</span></span>

<span data-ttu-id="7f465-119">Les décodeurs qui prennent en charge la lecture inversée en douceur doivent exposer cette propriété.</span><span class="sxs-lookup"><span data-stu-id="7f465-119">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="7f465-120">Pour plus d’informations, consultez [améliorations de la lecture de DVD dans Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="7f465-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f465-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f465-121">Requirements</span></span>



| <span data-ttu-id="7f465-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f465-122">Requirement</span></span> | <span data-ttu-id="7f465-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f465-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f465-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f465-124">Header</span></span><br/> | <dl> <span data-ttu-id="7f465-125"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f465-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f465-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f465-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f465-127">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="7f465-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




