---
description: La méthode GetNumberOfChapters récupère le nombre de chapitres dans le titre spécifié.
ms.assetid: d1291f6d-9296-486f-adad-d8819a4e54d6
title: Méthode GetNumberOfChapters
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed328e2da3e28627083f7021ee999b79fae2e98
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846313"
---
# <a name="getnumberofchapters-method"></a><span data-ttu-id="cddd1-103">Méthode GetNumberOfChapters</span><span class="sxs-lookup"><span data-stu-id="cddd1-103">GetNumberOfChapters Method</span></span>

> [!Note]  
> <span data-ttu-id="cddd1-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cddd1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cddd1-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cddd1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cddd1-106">La `GetNumberOfChapters` méthode récupère le nombre de chapitres dans le titre spécifié.</span><span class="sxs-lookup"><span data-stu-id="cddd1-106">The `GetNumberOfChapters` method retrieves the number of chapters in the specified title.</span></span>

``` syntax
[iChapters = ] MSWebDVD.GetNumberOfChapters(iTitle)
```

## <a name="parameters"></a><span data-ttu-id="cddd1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cddd1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cddd1-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="cddd1-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="cddd1-109">Spécifie le titre sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="cddd1-109">Specifies the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cddd1-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cddd1-110">Return Value</span></span>

<span data-ttu-id="cddd1-111">Retourne une valeur entière comprise entre 1 et 999 indiquant le nombre de chapitres.</span><span class="sxs-lookup"><span data-stu-id="cddd1-111">Returns an integer value from 1 through 999 indicating the number of chapters.</span></span>

 

 



