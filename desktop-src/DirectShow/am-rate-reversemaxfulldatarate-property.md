---
description: S’applique à Windows Vista et versions ultérieures.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679e83038a74e64d7a39e8757a9ffaf61fc88c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525540"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="33c2b-103">\_ \_ Propriété REVERSEMAXFULLDATARATE rate AM</span><span class="sxs-lookup"><span data-stu-id="33c2b-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="33c2b-104">S’applique à Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="33c2b-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="33c2b-105">Retourne la vitesse de lecture inversée maximale du décodeur.</span><span class="sxs-lookup"><span data-stu-id="33c2b-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="33c2b-106">La valeur de la propriété est la valeur absolue de la vitesse inversée maximale x 10000.</span><span class="sxs-lookup"><span data-stu-id="33c2b-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="33c2b-107">Par exemple, si la vitesse inversée maximale est-2,0, la valeur de cette propriété est 20000.</span><span class="sxs-lookup"><span data-stu-id="33c2b-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="33c2b-108">Le type de données de cette propriété **est \_ MaxFullDataRate**, qui est `typedef` de type **long**.</span><span class="sxs-lookup"><span data-stu-id="33c2b-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="33c2b-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="33c2b-109">This property is read-only.</span></span>



|                   |                                  |
|-------------------|----------------------------------|
| <span data-ttu-id="33c2b-110">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="33c2b-110">Property Set GUID</span></span> | <span data-ttu-id="33c2b-111">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="33c2b-111">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="33c2b-112">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="33c2b-112">Property ID</span></span>       | <span data-ttu-id="33c2b-113">\_Taux am \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="33c2b-113">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="33c2b-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="33c2b-114">Data Type</span></span>         | <span data-ttu-id="33c2b-115">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="33c2b-115">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="33c2b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="33c2b-116">Remarks</span></span>

<span data-ttu-id="33c2b-117">Les décodeurs qui prennent en charge la lecture inversée en douceur doivent exposer cette propriété.</span><span class="sxs-lookup"><span data-stu-id="33c2b-117">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="33c2b-118">Pour plus d’informations, consultez [améliorations de la lecture de DVD dans Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="33c2b-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33c2b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33c2b-119">Requirements</span></span>



| <span data-ttu-id="33c2b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33c2b-120">Requirement</span></span> | <span data-ttu-id="33c2b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="33c2b-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33c2b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="33c2b-122">Header</span></span><br/> | <dl> <span data-ttu-id="33c2b-123"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="33c2b-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c2b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33c2b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c2b-125">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="33c2b-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




