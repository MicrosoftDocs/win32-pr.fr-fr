---
title: MONTHDAYSTATE
description: Le type de données MONTHDAYSTATE est un champ de type binaire qui contient l’état de chaque jour dans un mois.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2286482460ec87982c46a564e8441edd9bf7bb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839382"
---
# <a name="monthdaystate"></a><span data-ttu-id="e4dcc-103">MONTHDAYSTATE</span><span class="sxs-lookup"><span data-stu-id="e4dcc-103">MONTHDAYSTATE</span></span>

<span data-ttu-id="e4dcc-104">Le type de données MONTHDAYSTATE est un champ de type binaire qui contient l’état de chaque jour dans un mois.</span><span class="sxs-lookup"><span data-stu-id="e4dcc-104">The MONTHDAYSTATE data type is a bitfield that holds the state of each day in a month.</span></span> <span data-ttu-id="e4dcc-105">Le type de données est défini dans commctrl. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="e4dcc-105">The data type is defined in Commctrl.h as follows:</span></span>


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



<span data-ttu-id="e4dcc-106">Chaque bit (0 à 30) représente l’état d’un jour dans un mois.</span><span class="sxs-lookup"><span data-stu-id="e4dcc-106">Each bit (0 through 30) represents the state of a day in a month.</span></span> <span data-ttu-id="e4dcc-107">Si un bit est activé, le jour correspondant s'affiche en gras ; sinon il s'affiche sans l'accentuation.</span><span class="sxs-lookup"><span data-stu-id="e4dcc-107">If a bit is on, the corresponding day will be displayed in bold; otherwise it will be displayed with no emphasis.</span></span>

<span data-ttu-id="e4dcc-108">Ce type de données est utilisé avec le message [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) et la macro correspondante, [**calendrier monthcal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span><span class="sxs-lookup"><span data-stu-id="e4dcc-108">This data type is used with the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message and the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="e4dcc-109">Lorsque les valeurs MONTHDAYSTATE sont utilisées en référence à des mois plus courts que 31 jours, seuls les bits nécessaires sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="e4dcc-109">When MONTHDAYSTATE values are used in reference to months shorter than 31 days, only the needed bits will be accessed.</span></span>

<span data-ttu-id="e4dcc-110">Ce type de données a d’abord été défini dans la [Version 4,70](common-control-versions.md) de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="e4dcc-110">This data type was first defined in [Version 4.70](common-control-versions.md) of Comctl32.dll.</span></span>

 

 




