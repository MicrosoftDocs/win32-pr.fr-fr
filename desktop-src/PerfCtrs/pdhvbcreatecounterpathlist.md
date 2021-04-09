---
description: La fonction PdhVbCreateCounterPathList affiche la boîte de dialogue exploration des compteurs de performance, qui permet à l’utilisateur de sélectionner plusieurs compteurs de performances. Chaque chemin de compteur sélectionné doit ensuite être lu à l’aide de la fonction PdhVbGetCounterPathFromList.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: PdhVbCreateCounterPathList fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865117"
---
# <a name="pdhvbcreatecounterpathlist-function"></a><span data-ttu-id="7886c-104">PdhVbCreateCounterPathList fonction)</span><span class="sxs-lookup"><span data-stu-id="7886c-104">PdhVbCreateCounterPathList function</span></span>

<span data-ttu-id="7886c-105">La fonction **PdhVbCreateCounterPathList** affiche la boîte de dialogue exploration des compteurs de performance, qui permet à l’utilisateur de sélectionner plusieurs compteurs de performances.</span><span class="sxs-lookup"><span data-stu-id="7886c-105">The **PdhVbCreateCounterPathList** function displays the performance counter browsing dialog box, which lets the user select several performance counters.</span></span> <span data-ttu-id="7886c-106">Chaque chemin de compteur sélectionné doit ensuite être lu à l’aide de la fonction [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) .</span><span class="sxs-lookup"><span data-stu-id="7886c-106">Each selected counter path must then be read using the [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7886c-107">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="7886c-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="7886c-108">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7886c-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="7886c-109">Function PdhVbCreateCounterPathList ( \_ ByVal DetailLevel As long, \_ ByVal CaptionString As String \_ ) As long</span><span class="sxs-lookup"><span data-stu-id="7886c-109">Function PdhVbCreateCounterPathList( \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="7886c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7886c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7886c-111">*DetailLevel*</span><span class="sxs-lookup"><span data-stu-id="7886c-111">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="7886c-112">Types de compteurs à afficher dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7886c-112">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="7886c-113">Utilisez l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7886c-113">Use one of the following values.</span></span>



| <span data-ttu-id="7886c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7886c-114">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="7886c-115">Signification</span><span class="sxs-lookup"><span data-stu-id="7886c-115">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="7886c-116"><dt>**détail des performances- \_ \_ avancé**</dt></span><span class="sxs-lookup"><span data-stu-id="7886c-116"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="7886c-117">Compteurs que l’utilisateur avancé est susceptible de comprendre, en plus des compteurs utilisateur novice.</span><span class="sxs-lookup"><span data-stu-id="7886c-117">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="7886c-118"><dt>**\_expert en détail des performances \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7886c-118"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="7886c-119">Les compteurs que l’utilisateur expérimenté et le développeur de logiciels peuvent comprendre, en plus des compteurs pour les utilisateurs débutants et expérimentés.</span><span class="sxs-lookup"><span data-stu-id="7886c-119">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="7886c-120"><dt>**\_novice détaillé sur les performances \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7886c-120"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="7886c-121">Seuls les compteurs que l’utilisateur novice est susceptible de comprendre.</span><span class="sxs-lookup"><span data-stu-id="7886c-121">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="7886c-122"><dt>**\_Assistant détail des performances \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7886c-122"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="7886c-123">Tous les compteurs du système.</span><span class="sxs-lookup"><span data-stu-id="7886c-123">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="7886c-124">*CaptionString*</span><span class="sxs-lookup"><span data-stu-id="7886c-124">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="7886c-125">Variable de chaîne qui contient le texte qui sera affiché dans la barre de légende de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7886c-125">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7886c-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7886c-126">Return value</span></span>

<span data-ttu-id="7886c-127">La fonction retourne le nombre de chemins d’accès aux compteurs sélectionnés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7886c-127">The function returns the number of counter paths that the user selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="7886c-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7886c-128">Requirements</span></span>



| <span data-ttu-id="7886c-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7886c-129">Requirement</span></span> | <span data-ttu-id="7886c-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7886c-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7886c-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7886c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7886c-132">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7886c-132">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7886c-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7886c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7886c-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7886c-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7886c-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7886c-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7886c-136"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7886c-136"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="7886c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7886c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7886c-138"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7886c-138"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7886c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7886c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7886c-140">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="7886c-140">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="7886c-141">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="7886c-141">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="7886c-142">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="7886c-142">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




