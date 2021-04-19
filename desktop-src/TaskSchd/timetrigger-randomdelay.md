---
title: TimeTrigger. RandomDelay, propriété
description: Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur. | TimeTrigger. RandomDelay, propriété
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- Planificateur de tâches de la propriété RandomDelay
- Planificateur de tâches de la propriété RandomDelay, objet TimeTrigger
- Planificateur de tâches objet TimeTrigger, propriété RandomDelay
topic_type:
- apiref
api_name:
- TimeTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39c4acf4f38670332e723ac0824276695919cb1d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535774"
---
# <a name="timetriggerrandomdelay-property"></a><span data-ttu-id="17163-107">TimeTrigger. RandomDelay, propriété</span><span class="sxs-lookup"><span data-stu-id="17163-107">TimeTrigger.RandomDelay property</span></span>

<span data-ttu-id="17163-108">Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="17163-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="17163-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17163-109">Syntax</span></span>


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="17163-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="17163-110">Property value</span></span>

<span data-ttu-id="17163-111">Délai d’ajout aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="17163-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="17163-112">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="17163-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="17163-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17163-113">Requirements</span></span>



| <span data-ttu-id="17163-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17163-114">Requirement</span></span> | <span data-ttu-id="17163-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="17163-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17163-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17163-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17163-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17163-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="17163-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17163-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17163-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17163-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="17163-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="17163-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="17163-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17163-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17163-122">DLL</span><span class="sxs-lookup"><span data-stu-id="17163-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17163-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17163-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





