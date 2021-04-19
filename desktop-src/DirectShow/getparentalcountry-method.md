---
description: La méthode DVDAdm. GetParentalCountry récupère le pays ou la région parente qui a été enregistré pour la dernière fois dans le registre.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Méthode GetParentalCountry (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535313"
---
# <a name="getparentalcountry-method"></a><span data-ttu-id="efd77-103">Méthode GetParentalCountry</span><span class="sxs-lookup"><span data-stu-id="efd77-103">GetParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="efd77-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="efd77-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="efd77-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="efd77-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="efd77-106">La `DVDAdm.GetParentalCountry` méthode récupère le pays ou la région parente qui a été enregistrée dans le registre.</span><span class="sxs-lookup"><span data-stu-id="efd77-106">The `DVDAdm.GetParentalCountry` method retrieves the parental country/region that was last saved to the registry.</span></span>

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a><span data-ttu-id="efd77-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="efd77-107">Return Value</span></span>

<span data-ttu-id="efd77-108">Retourne un entier indiquant le code de pays/région par défaut stocké dans le registre.</span><span class="sxs-lookup"><span data-stu-id="efd77-108">Returns an Integer indicating the default country/region code stored in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="efd77-109">Notes</span><span class="sxs-lookup"><span data-stu-id="efd77-109">Remarks</span></span>

<span data-ttu-id="efd77-110">Le pays ou la région parente que cette méthode récupère n’est pas nécessairement le même pays ou la même région actuellement stockée dans l’objet MSWebDVD.</span><span class="sxs-lookup"><span data-stu-id="efd77-110">The parental country/region this method retrieves is not necessarily the same country/region currently stored in the MSWebDVD object.</span></span>

## <a name="requirements"></a><span data-ttu-id="efd77-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efd77-111">Requirements</span></span>



| <span data-ttu-id="efd77-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efd77-112">Requirement</span></span> | <span data-ttu-id="efd77-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="efd77-113">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="efd77-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="efd77-114">Header</span></span><br/> | <dl> <span data-ttu-id="efd77-115"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="efd77-115"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efd77-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efd77-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efd77-117">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="efd77-117">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




