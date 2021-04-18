---
description: paramètres régionaux \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 7f391fb167a9362fc8770bbcc5a495170148b489
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "106523091"
---
# <a name="locale_ifirstweekofyear"></a><span data-ttu-id="d771e-103">paramètres régionaux \_ IFIRSTWEEKOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d771e-103">LOCALE\_IFIRSTWEEKOFYEAR</span></span>

<span data-ttu-id="d771e-104">Première semaine de l’année.</span><span class="sxs-lookup"><span data-stu-id="d771e-104">The first week of the year.</span></span>



| <span data-ttu-id="d771e-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="d771e-105">Value</span></span> | <span data-ttu-id="d771e-106">Signification</span><span class="sxs-lookup"><span data-stu-id="d771e-106">Meaning</span></span>                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d771e-107">0</span><span class="sxs-lookup"><span data-stu-id="d771e-107">0</span></span>     | <span data-ttu-id="d771e-108">La semaine contenant 1/1 est la première semaine de l’année.</span><span class="sxs-lookup"><span data-stu-id="d771e-108">Week containing 1/1 is the first week of the year.</span></span> <span data-ttu-id="d771e-109">Notez qu’il peut s’agir d’une seule journée, si 1/1 tombe le dernier jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="d771e-109">Note that this can be a single day, if 1/1 falls on the last day of the week.</span></span> |
| <span data-ttu-id="d771e-110">1</span><span class="sxs-lookup"><span data-stu-id="d771e-110">1</span></span>     | <span data-ttu-id="d771e-111">La première semaine complète suivante 1/1 est la première semaine de l’année.</span><span class="sxs-lookup"><span data-stu-id="d771e-111">First full week following 1/1 is the first week of the year.</span></span>                                                                     |
| <span data-ttu-id="d771e-112">2</span><span class="sxs-lookup"><span data-stu-id="d771e-112">2</span></span>     | <span data-ttu-id="d771e-113">La première semaine contenant au moins quatre jours est la première semaine de l’année.</span><span class="sxs-lookup"><span data-stu-id="d771e-113">First week containing at least four days is the first week of the year.</span></span> <span data-ttu-id="d771e-114">Compatible ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="d771e-114">ISO 8601 compatible.</span></span>                                     |

<span data-ttu-id="d771e-115">Si LOCALE_IFIRSTWEEKOFYEAR a la valeur 2, LOCALE_IFIRSTDAYOFWEEK a la valeur 0 (lundi) et LOCALE_ICALENDARTYPE est grégorien, la première semaine suit la définition ISO 8601, où la première semaine est la semaine avec le premier jeudi de l’année grégorienne.</span><span class="sxs-lookup"><span data-stu-id="d771e-115">If LOCALE_IFIRSTWEEKOFYEAR is 2, LOCALE_IFIRSTDAYOFWEEK is 0 (Monday), and LOCALE_ICALENDARTYPE is Gregorian, then the first week follows the ISO 8601 definition where the first week is the week with the first Thursday of the Gregorian year in it.</span></span>


 

 

 



