---
description: La méthode PlayAtTimeInTitle démarre la lecture à l’heure spécifiée dans le titre spécifié.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Méthode PlayAtTimeInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c40373b4327b6df5fc341ca392c223d464a70a8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480600"
---
# <a name="playattimeintitle-method"></a><span data-ttu-id="1f1f1-103">Méthode PlayAtTimeInTitle</span><span class="sxs-lookup"><span data-stu-id="1f1f1-103">PlayAtTimeInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="1f1f1-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1f1f1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1f1f1-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1f1f1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1f1f1-106">La `PlayAtTimeInTitle` méthode démarre la lecture à l’heure spécifiée dans le titre spécifié.</span><span class="sxs-lookup"><span data-stu-id="1f1f1-106">The `PlayAtTimeInTitle` method starts playback at the specified time within the specified title.</span></span>

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a><span data-ttu-id="1f1f1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f1f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f1f1-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span><span class="sxs-lookup"><span data-stu-id="1f1f1-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span></span>
</dt> <dd>

<span data-ttu-id="1f1f1-109">Spécifie l’heure de début de la lecture sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="1f1f1-109">Specifies the time at which to start playback as a string.</span></span> <span data-ttu-id="1f1f1-110">La chaîne doit être au format « hh : mm : SS : FF » (en spécifiant les heures, les minutes, les secondes, les frames).</span><span class="sxs-lookup"><span data-stu-id="1f1f1-110">The string must be in the format "hh:mm:ss:ff" (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="1f1f1-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="1f1f1-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="1f1f1-112">Spécifie l’index du titre sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="1f1f1-112">Specifies the index of the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f1f1-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f1f1-113">Return Value</span></span>

<span data-ttu-id="1f1f1-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="1f1f1-114">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f1f1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f1f1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1f1-116">**CurrentTitle**</span><span class="sxs-lookup"><span data-stu-id="1f1f1-116">**CurrentTitle**</span></span>](currenttitle-property.md)
</dt> <dt>

[<span data-ttu-id="1f1f1-117">**PlayAtTime**</span><span class="sxs-lookup"><span data-stu-id="1f1f1-117">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="1f1f1-118">**TitlesAvailable**</span><span class="sxs-lookup"><span data-stu-id="1f1f1-118">**TitlesAvailable**</span></span>](titlesavailable-property.md)
</dt> </dl>

 

 



