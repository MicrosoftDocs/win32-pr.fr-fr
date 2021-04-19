---
description: Décrit les formats d’heure pris en charge pour une utilisation dans la clause WHERE WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: Formats d’heure WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544788"
---
# <a name="wql-supported-time-formats"></a><span data-ttu-id="94852-103">Formats d’heure WQL-Supported</span><span class="sxs-lookup"><span data-stu-id="94852-103">WQL-Supported Time Formats</span></span>

<span data-ttu-id="94852-104">Outre le format DATETIME WMI, les formats de date suivants sont pris en charge pour une utilisation dans la clause WQL WQL.</span><span class="sxs-lookup"><span data-stu-id="94852-104">In addition to the WMI DATETIME format, the following date formats are supported for use in the WQL WHERE clause.</span></span>



| <span data-ttu-id="94852-105">Format</span><span class="sxs-lookup"><span data-stu-id="94852-105">Format</span></span>                                    | <span data-ttu-id="94852-106">Description</span><span class="sxs-lookup"><span data-stu-id="94852-106">Description</span></span>                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94852-107">HH \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="94852-107">hh\[ \]{AP}M</span></span><br/>                   | <span data-ttu-id="94852-108">Heure comme indiqué sur une horloge de 12 heures, et une désignation AM ou PM.</span><span class="sxs-lookup"><span data-stu-id="94852-108">Hour as shown on a twelve-hour clock, and AM or PM designation.</span></span><br/> <span data-ttu-id="94852-109">16:00</span><span class="sxs-lookup"><span data-stu-id="94852-109">4 PM</span></span><br/>                                                                                                             |
| <span data-ttu-id="94852-110">hh:mm</span><span class="sxs-lookup"><span data-stu-id="94852-110">hh:mm</span></span><br/>                          | <span data-ttu-id="94852-111">Heures et minutes délimitées par deux-points.</span><span class="sxs-lookup"><span data-stu-id="94852-111">Colon-delimited hour and minutes.</span></span> <span data-ttu-id="94852-112">Aucune dénomination AM ou PM.</span><span class="sxs-lookup"><span data-stu-id="94852-112">No AM or PM designation.</span></span><br/> <span data-ttu-id="94852-113">3:23</span><span class="sxs-lookup"><span data-stu-id="94852-113">3:23</span></span><br/>                                                                                                                  |
| <span data-ttu-id="94852-114">hh : mm \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="94852-114">hh:mm\[ \]{AP}M</span></span><br/>                | <span data-ttu-id="94852-115">Heures et minutes délimitées par deux-points, espace facultatif et désignation AM ou PM.</span><span class="sxs-lookup"><span data-stu-id="94852-115">Colon-delimited hour and minutes, optional space, and AM or PM designation.</span></span><br/> <span data-ttu-id="94852-116">3:23</span><span class="sxs-lookup"><span data-stu-id="94852-116">3:23 AM</span></span><br/>                                                                                              |
| <span data-ttu-id="94852-117">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="94852-117">hh:mm:ss</span></span><br/>                       | <span data-ttu-id="94852-118">Heure délimitée par deux-points, en minutes et en secondes.</span><span class="sxs-lookup"><span data-stu-id="94852-118">Colon-delimited hour, minutes and seconds.</span></span> <span data-ttu-id="94852-119">Aucune désignation AM/PM.</span><span class="sxs-lookup"><span data-stu-id="94852-119">No AM/PM designation.</span></span><br/> <span data-ttu-id="94852-120">3:23:00</span><span class="sxs-lookup"><span data-stu-id="94852-120">3:23:00</span></span><br/>                                                                                                         |
| <span data-ttu-id="94852-121">hh : mm : SS \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="94852-121">hh:mm:ss\[ \]{AP}M</span></span><br/>             | <span data-ttu-id="94852-122">L’heure, les minutes et les secondes, l’espace facultatif et la désignation AM/PM sont délimités par deux-points.</span><span class="sxs-lookup"><span data-stu-id="94852-122">Colon-delimited hour, minutes and seconds, optional space, and AM/PM designation.</span></span><br/> <span data-ttu-id="94852-123">3:23:14:00</span><span class="sxs-lookup"><span data-stu-id="94852-123">3:23:00PM</span></span><br/>                                                                                      |
| <span data-ttu-id="94852-124">hh : mm : SS : uuu</span><span class="sxs-lookup"><span data-stu-id="94852-124">hh:mm:ss:uuu</span></span><br/>                   | <span data-ttu-id="94852-125">Heure, minutes et secondes délimitée par deux-points, et décalage à trois chiffres qui indique le nombre de minutes pendant lequel le fuseau horaire d’origine s’écarte de l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="94852-125">Colon-delimited hour, minutes and seconds, and three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                                    |
| <span data-ttu-id="94852-126">hh : mm : \[ SS : u u u \[ \] \]</span><span class="sxs-lookup"><span data-stu-id="94852-126">hh:mm:ss:\[\[u\]u\]u</span></span><br/>           | <span data-ttu-id="94852-127">Heure délimitée par deux-points, minutes et secondes ; et un décalage d’un, deux ou trois chiffres qui indique le nombre de minutes pendant lequel le fuseau horaire d’origine s’écarte de l’heure UTC.</span><span class="sxs-lookup"><span data-stu-id="94852-127">Colon-delimited hour, minutes and seconds; and one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                       |
| <span data-ttu-id="94852-128">hh : mm : SS : uuu \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="94852-128">hh:mm:ss:uuu\[ \]{AP}M</span></span><br/>         | <span data-ttu-id="94852-129">Heure délimitée par deux-points, minutes et secondes, décalage à trois chiffres qui indique le nombre de minutes pendant lequel le fuseau horaire d’origine s’écarte de l’heure UTC et de la désignation AM ou PM.</span><span class="sxs-lookup"><span data-stu-id="94852-129">Colon-delimited hour, minutes and seconds, three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC, and AM or PM designation.</span></span><br/>              |
| <span data-ttu-id="94852-130">hh : mm : SS : u u u \[ \[ \] \] \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="94852-130">hh:mm:ss:\[\[u\]u\]u\[ \]{AP}M</span></span><br/> | <span data-ttu-id="94852-131">Heure délimitée par deux-points, minutes et secondes ; décalage un, deux ou trois chiffres qui indique le nombre de minutes que le fuseau horaire d’origine s’écarte de l’heure UTC ; et la désignation AM ou PM.</span><span class="sxs-lookup"><span data-stu-id="94852-131">Colon-delimited hour, minutes and seconds; one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC; and AM or PM designation.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="94852-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94852-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94852-133">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="94852-133">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




