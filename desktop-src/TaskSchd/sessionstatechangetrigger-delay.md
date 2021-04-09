---
title: SessionStateChangeTrigger. Delay, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la durée d’un délai avant le démarrage d’une tâche après la détection d’un changement d’état de session Terminal Server.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Planificateur de tâches de propriétés Delay
- Planificateur de tâches de propriété Delay, objet SessionStateChangeTrigger
- Planificateur de tâches objet SessionStateChangeTrigger, propriété Delay
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103189"
---
# <a name="sessionstatechangetriggerdelay-property"></a><span data-ttu-id="0d596-106">SessionStateChangeTrigger. Delay, propriété</span><span class="sxs-lookup"><span data-stu-id="0d596-106">SessionStateChangeTrigger.Delay property</span></span>

<span data-ttu-id="0d596-107">Pour les scripts, obtient ou définit une valeur qui indique la durée d’un délai avant le démarrage d’une tâche après la détection d’un changement d’état de session Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="0d596-107">For scripting, gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span> <span data-ttu-id="0d596-108">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="0d596-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d596-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d596-109">Syntax</span></span>


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="0d596-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0d596-110">Property value</span></span>

<span data-ttu-id="0d596-111">Délai qui s’écoule avant le démarrage d’une tâche après la détection d’une modification d’état de session Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="0d596-111">The delay that takes place before a task is started after a Terminal Server session state change is detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d596-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d596-112">Requirements</span></span>



| <span data-ttu-id="0d596-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d596-113">Requirement</span></span> | <span data-ttu-id="0d596-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d596-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d596-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d596-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0d596-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d596-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0d596-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d596-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0d596-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d596-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0d596-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0d596-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d596-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0d596-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0d596-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0d596-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d596-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d596-122"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





