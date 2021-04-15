---
description: La méthode GetTitleParentalLevels récupère les niveaux de gestion parental pour le titre spécifié.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Méthode GetTitleParentalLevels
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392623"
---
# <a name="gettitleparentallevels-method"></a><span data-ttu-id="a9a3e-103">Méthode GetTitleParentalLevels</span><span class="sxs-lookup"><span data-stu-id="a9a3e-103">GetTitleParentalLevels Method</span></span>

> [!Note]  
> <span data-ttu-id="a9a3e-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a9a3e-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a9a3e-106">La `GetTitleParentalLevels` méthode récupère les niveaux de gestion parental pour le titre spécifié.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-106">The `GetTitleParentalLevels` method retrieves the parental management levels for the specified title.</span></span>

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a><span data-ttu-id="a9a3e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9a3e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a3e-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="a9a3e-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="a9a3e-109">Spécifie le titre sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-109">Specifies the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9a3e-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a9a3e-110">Return Value</span></span>

<span data-ttu-id="a9a3e-111">Retourne une valeur entière dont les bits indiquent les niveaux de gestion du contrôle parental (PML) qui sont définis dans le titre spécifié.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-111">Returns an integer value whose individual bits indicate which parental management levels (PML) are set in the specified title.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9a3e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a9a3e-112">Remarks</span></span>

<span data-ttu-id="a9a3e-113">Un titre peut avoir des chapitres, voire des segments courts, qui ont un PML différent de la PML globale pour le titre.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-113">A title may have chapters or even short segments that have a PML different from the overall PML for the title.</span></span> <span data-ttu-id="a9a3e-114">Utilisez cette méthode pour déterminer tous les PMLs qui seront rencontrés lors de la diffusion d’un titre spécifié.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-114">Use this method to determine all the PMLs that will be encountered when playing a specified title.</span></span> <span data-ttu-id="a9a3e-115">L’entier retourné est un jeu d’indicateurs binaires définis comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-115">The returned integer is a set of bit flags that are defined as shown in the table below.</span></span> <span data-ttu-id="a9a3e-116">Effectuez une opération and au niveau du bit sur *iLevels* et chaque valeur possible.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-116">Perform a bitwise AND operation on *iLevels* and each possible value.</span></span> <span data-ttu-id="a9a3e-117">Si l’opération retourne la **valeur true**, cela signifie que PML sera rencontré à un moment donné dans ce titre.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-117">If the operation returns **true**, it means that PML will be encountered at some point in this title.</span></span>



| <span data-ttu-id="a9a3e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9a3e-118">Value</span></span>  | <span data-ttu-id="a9a3e-119">Description</span><span class="sxs-lookup"><span data-stu-id="a9a3e-119">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="a9a3e-120">0x100</span><span class="sxs-lookup"><span data-stu-id="a9a3e-120">0x100</span></span>  | <span data-ttu-id="a9a3e-121">Niveau parental du DVD 1</span><span class="sxs-lookup"><span data-stu-id="a9a3e-121">DVD Parental Level 1</span></span> |
| <span data-ttu-id="a9a3e-122">0x200</span><span class="sxs-lookup"><span data-stu-id="a9a3e-122">0x200</span></span>  | <span data-ttu-id="a9a3e-123">Niveau parental de DVD 2</span><span class="sxs-lookup"><span data-stu-id="a9a3e-123">DVD Parental Level 2</span></span> |
| <span data-ttu-id="a9a3e-124">0x400</span><span class="sxs-lookup"><span data-stu-id="a9a3e-124">0x400</span></span>  | <span data-ttu-id="a9a3e-125">Niveau parental de DVD 3</span><span class="sxs-lookup"><span data-stu-id="a9a3e-125">DVD Parental Level 3</span></span> |
| <span data-ttu-id="a9a3e-126">0x800</span><span class="sxs-lookup"><span data-stu-id="a9a3e-126">0x800</span></span>  | <span data-ttu-id="a9a3e-127">Niveau parental de DVD 4</span><span class="sxs-lookup"><span data-stu-id="a9a3e-127">DVD Parental Level 4</span></span> |
| <span data-ttu-id="a9a3e-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="a9a3e-128">0x1000</span></span> | <span data-ttu-id="a9a3e-129">Niveau parental de DVD 5</span><span class="sxs-lookup"><span data-stu-id="a9a3e-129">DVD Parental Level 5</span></span> |
| <span data-ttu-id="a9a3e-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="a9a3e-130">0x2000</span></span> | <span data-ttu-id="a9a3e-131">Niveau parental de DVD 6</span><span class="sxs-lookup"><span data-stu-id="a9a3e-131">DVD Parental Level 6</span></span> |
| <span data-ttu-id="a9a3e-132">0x4000</span><span class="sxs-lookup"><span data-stu-id="a9a3e-132">0x4000</span></span> | <span data-ttu-id="a9a3e-133">Niveau parental de DVD 7</span><span class="sxs-lookup"><span data-stu-id="a9a3e-133">DVD Parental Level 7</span></span> |
| <span data-ttu-id="a9a3e-134">0x8000</span><span class="sxs-lookup"><span data-stu-id="a9a3e-134">0x8000</span></span> | <span data-ttu-id="a9a3e-135">Niveau parental de DVD 8</span><span class="sxs-lookup"><span data-stu-id="a9a3e-135">DVD Parental Level 8</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="a9a3e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9a3e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a3e-137">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="a9a3e-137">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="a9a3e-138">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="a9a3e-138">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="a9a3e-139">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="a9a3e-139">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="a9a3e-140">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="a9a3e-140">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 



