---
description: Cette propriété est utilisée pour indiquer la version de la propriété de modification de taux que le décodeur doit utiliser.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: AM_RATE_UseRateVersion, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab609d2d38dc28257d13994e6cd464094b714be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543849"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="4b8ce-103">\_ \_ Propriété USERATEVERSION rate AM</span><span class="sxs-lookup"><span data-stu-id="4b8ce-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="4b8ce-104">Cette propriété est utilisée pour indiquer la version de la propriété de modification de taux que le décodeur doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="4b8ce-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="4b8ce-105">La valeur est un type de **mot** .</span><span class="sxs-lookup"><span data-stu-id="4b8ce-105">The value is a **WORD** type.</span></span> <span data-ttu-id="4b8ce-106">L’octet de poids fort contient le numéro de version mineure et l’octet de poids faible contient l’octet de poids faible.</span><span class="sxs-lookup"><span data-stu-id="4b8ce-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="4b8ce-107">Par conséquent, la version 1,1 est signalée par la valeur 0x0101.</span><span class="sxs-lookup"><span data-stu-id="4b8ce-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="4b8ce-108">Si le décodeur ne prend pas en charge la version spécifiée, il doit faire échouer l’appel à [**IKsPropertySet :: Set**](ikspropertyset-set.md) et retourner E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="4b8ce-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="4b8ce-109">Si le filtre source ne définit pas la version, le décodeur doit avoir la valeur par défaut version 1,0.</span><span class="sxs-lookup"><span data-stu-id="4b8ce-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="4b8ce-110">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="4b8ce-110">Property Set GUID</span></span> | <span data-ttu-id="4b8ce-111">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="4b8ce-111">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="4b8ce-112">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="4b8ce-112">Property ID</span></span>       | <span data-ttu-id="4b8ce-113">\_Taux am \_ UseRateVersion</span><span class="sxs-lookup"><span data-stu-id="4b8ce-113">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="4b8ce-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="4b8ce-114">Data Type</span></span>         | <span data-ttu-id="4b8ce-115">**WORD**</span><span class="sxs-lookup"><span data-stu-id="4b8ce-115">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="4b8ce-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b8ce-116">Requirements</span></span>



| <span data-ttu-id="4b8ce-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b8ce-117">Requirement</span></span> | <span data-ttu-id="4b8ce-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b8ce-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8ce-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b8ce-119">Header</span></span><br/> | <dl> <span data-ttu-id="4b8ce-120"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b8ce-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b8ce-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b8ce-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8ce-122">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="4b8ce-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




