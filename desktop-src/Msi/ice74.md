---
description: ICE74 vérifie que la propriété FASTOEM n’a pas été créée dans la table de propriétés.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524495"
---
# <a name="ice74"></a><span data-ttu-id="65d83-103">ICE74</span><span class="sxs-lookup"><span data-stu-id="65d83-103">ICE74</span></span>

<span data-ttu-id="65d83-104">ICE74 vérifie que la propriété [**FASTOEM**](fastoem.md) n’a pas été créée dans la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="65d83-104">ICE74 verifies that the [**FASTOEM**](fastoem.md) property has not been authored into the [Property table](property-table.md).</span></span>

<span data-ttu-id="65d83-105">La propriété [**FASTOEM**](fastoem.md) permet aux OEM de réduire le temps nécessaire pour installer Windows Installer applications pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="65d83-105">The [**FASTOEM**](fastoem.md) property enables OEMs to reduce the time required to install Windows Installer applications for the first time.</span></span> <span data-ttu-id="65d83-106">Elle ne peut pas être utilisée après la première installation.</span><span class="sxs-lookup"><span data-stu-id="65d83-106">It cannot be used after the first install.</span></span> <span data-ttu-id="65d83-107">La propriété **FASTOEM** ne doit pas être créée dans la table de propriétés, car cela interfère avec les installations suivantes pour la maintenance, la suppression ou la réparation de l’application.</span><span class="sxs-lookup"><span data-stu-id="65d83-107">The **FASTOEM** property must not be authored in the Property table because this interferes with subsequent installations for the maintenance, removal, or repair of the application.</span></span>

<span data-ttu-id="65d83-108">ICE74 vérifie également que la propriété [**UpgradeCode**](upgradecode.md) est créée dans la table de [Propriétés](property-table.md), et que sa valeur n’est pas un GUID null, {00000000-0000-0000-0000-000000000000} .</span><span class="sxs-lookup"><span data-stu-id="65d83-108">ICE74 also verifies that the [**UpgradeCode**](upgradecode.md) property is authored into the [Property table](property-table.md), and that its value is not a null GUID, {00000000-0000-0000-0000-000000000000}.</span></span>

## <a name="result"></a><span data-ttu-id="65d83-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="65d83-109">Result</span></span>

<span data-ttu-id="65d83-110">ICE74 peut poster les erreurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="65d83-110">ICE74 can post the following errors.</span></span>



| <span data-ttu-id="65d83-111">Erreur ICE74</span><span class="sxs-lookup"><span data-stu-id="65d83-111">ICE74 error</span></span>                                                                       | <span data-ttu-id="65d83-112">Description</span><span class="sxs-lookup"><span data-stu-id="65d83-112">Description</span></span>                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d83-113">La propriété [**FASTOEM**](fastoem.md) ne peut pas être créée dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="65d83-113">The [**FASTOEM**](fastoem.md) property cannot be authored in the Property table.</span></span> | <span data-ttu-id="65d83-114">La propriété [**FASTOEM**](fastoem.md) a été définie dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="65d83-114">The [**FASTOEM**](fastoem.md) property has been set in the Property table.</span></span>                             |
| <span data-ttu-id="65d83-115">' \[ 2 \] 'n’est pas une [**UpgradeCode**](upgradecode.md)valide.</span><span class="sxs-lookup"><span data-stu-id="65d83-115">'\[2\]' is not a valid [**UpgradeCode**](upgradecode.md).</span></span>                        | <span data-ttu-id="65d83-116">Un GUID null a été entré pour la propriété [**UpgradeCode**](upgradecode.md) dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="65d83-116">A null GUID has been entered for the [**UpgradeCode**](upgradecode.md) property in the Property table.</span></span> |



 

<span data-ttu-id="65d83-117">ICE74 peut poster l’avertissement suivant.</span><span class="sxs-lookup"><span data-stu-id="65d83-117">ICE74 can post the following warning.</span></span>



| <span data-ttu-id="65d83-118">AVERTISSEMENT ICE74</span><span class="sxs-lookup"><span data-stu-id="65d83-118">ICE74 warning</span></span>                                                                                                                                                                                             | <span data-ttu-id="65d83-119">Description</span><span class="sxs-lookup"><span data-stu-id="65d83-119">Description</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65d83-120">La propriété [**UpgradeCode**](upgradecode.md) n’est pas créée dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="65d83-120">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> <span data-ttu-id="65d83-121">Il est fortement recommandé que les auteurs des packages d’installation spécifient une **UpgradeCode** pour leur application.</span><span class="sxs-lookup"><span data-stu-id="65d83-121">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span> | <span data-ttu-id="65d83-122">La propriété [**UpgradeCode**](upgradecode.md) n’est pas créée dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="65d83-122">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> |



 

## <a name="example"></a><span data-ttu-id="65d83-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="65d83-123">Example</span></span>

<span data-ttu-id="65d83-124">ICE74 signale l’erreur suivante si la propriété [**FASTOEM**](fastoem.md) est définie : FASTOEM</span><span class="sxs-lookup"><span data-stu-id="65d83-124">ICE74 reports the following error if the [**FASTOEM**](fastoem.md) property is set: The FASTOEM</span></span>

``` syntax
 property cannot be authored in the Property table.
```

<span data-ttu-id="65d83-125">[Table de propriétés](property-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="65d83-125">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="65d83-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="65d83-126">Property</span></span>                   | <span data-ttu-id="65d83-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="65d83-127">Value</span></span> |
|----------------------------|-------|
| [<span data-ttu-id="65d83-128">**FASTOEM**</span><span class="sxs-lookup"><span data-stu-id="65d83-128">**FASTOEM**</span></span>](fastoem.md) | <span data-ttu-id="65d83-129">1</span><span class="sxs-lookup"><span data-stu-id="65d83-129">1</span></span>     |



 

<span data-ttu-id="65d83-130">Pour corriger cette erreur, supprimez la propriété [**FASTOEM**](fastoem.md) de la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="65d83-130">To fix this error remove the [**FASTOEM**](fastoem.md) property from the Property Table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65d83-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65d83-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65d83-132">**FASTOEM, propriété**</span><span class="sxs-lookup"><span data-stu-id="65d83-132">**FASTOEM property**</span></span>](fastoem.md)
</dt> <dt>

[<span data-ttu-id="65d83-133">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="65d83-133">Property table</span></span>](property-table.md)
</dt> <dt>

[<span data-ttu-id="65d83-134">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="65d83-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



