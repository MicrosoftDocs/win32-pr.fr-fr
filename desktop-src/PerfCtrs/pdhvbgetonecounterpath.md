---
description: La fonction PdhVbGetOneCounterPath affiche une boîte de dialogue qui permet à l’utilisateur de parcourir les compteurs de performance disponibles et de sélectionner un compteur.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: PdhVbGetOneCounterPath fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865113"
---
# <a name="pdhvbgetonecounterpath-function"></a><span data-ttu-id="6cc27-103">PdhVbGetOneCounterPath fonction)</span><span class="sxs-lookup"><span data-stu-id="6cc27-103">PdhVbGetOneCounterPath function</span></span>

<span data-ttu-id="6cc27-104">La fonction **PdhVbGetOneCounterPath** affiche une boîte de dialogue qui permet à l’utilisateur de parcourir les compteurs de performance disponibles et de sélectionner un compteur.</span><span class="sxs-lookup"><span data-stu-id="6cc27-104">The **PdhVbGetOneCounterPath** function displays a dialog box that lets the user browse the available performance counters and select one counter.</span></span> <span data-ttu-id="6cc27-105">Le compteur sélectionné est retourné dans la variable *PathString* .</span><span class="sxs-lookup"><span data-stu-id="6cc27-105">The counter selected is returned in the *PathString* variable.</span></span> <span data-ttu-id="6cc27-106">La variable *PathString* doit être dimensionnée et initialisée avant que cette fonction soit appelée, et la taille dimensionnée doit être indiquée par la variable *PathLength* .</span><span class="sxs-lookup"><span data-stu-id="6cc27-106">The *PathString* variable must be dimensioned and initialized before this function is called, and the dimensioned size must be indicated by the *PathLength* variable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cc27-107">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="6cc27-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="6cc27-108">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6cc27-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="6cc27-109">Function PdhVbGetOneCounterPath ( \_ ByVal PathString As String, \_ ByVal PathLength As long, \_ ByVal DetailLevel As long, \_ ByVal CaptionString As String \_ ) As long</span><span class="sxs-lookup"><span data-stu-id="6cc27-109">Function PdhVbGetOneCounterPath( \_ ByVal PathString As String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="6cc27-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cc27-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc27-111">*PathString*</span><span class="sxs-lookup"><span data-stu-id="6cc27-111">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc27-112">Variable de chaîne initialisée utilisée pour recevoir le chemin d’accès au compteur sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6cc27-112">Initialized string variable used to receive the counter path selected by the user.</span></span>

</dd> <dt>

<span data-ttu-id="6cc27-113">*PathLength*</span><span class="sxs-lookup"><span data-stu-id="6cc27-113">*PathLength*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc27-114">Longueur du PathString initialisé.</span><span class="sxs-lookup"><span data-stu-id="6cc27-114">Length of the initialized PathString.</span></span>

</dd> <dt>

<span data-ttu-id="6cc27-115">*DetailLevel*</span><span class="sxs-lookup"><span data-stu-id="6cc27-115">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc27-116">Types de compteurs à afficher dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6cc27-116">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="6cc27-117">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6cc27-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="6cc27-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cc27-118">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="6cc27-119">Signification</span><span class="sxs-lookup"><span data-stu-id="6cc27-119">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="6cc27-120"><dt>**détail des performances- \_ \_ avancé**</dt></span><span class="sxs-lookup"><span data-stu-id="6cc27-120"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="6cc27-121">Compteurs que l’utilisateur avancé est susceptible de comprendre, en plus des compteurs utilisateur novice.</span><span class="sxs-lookup"><span data-stu-id="6cc27-121">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="6cc27-122"><dt>**\_expert en détail des performances \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6cc27-122"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="6cc27-123">Les compteurs que l’utilisateur expérimenté et le développeur de logiciels peuvent comprendre, en plus des compteurs pour les utilisateurs débutants et expérimentés.</span><span class="sxs-lookup"><span data-stu-id="6cc27-123">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="6cc27-124"><dt>**\_novice détaillé sur les performances \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6cc27-124"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="6cc27-125">Seuls les compteurs que l’utilisateur novice est susceptible de comprendre.</span><span class="sxs-lookup"><span data-stu-id="6cc27-125">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="6cc27-126"><dt>**\_Assistant détail des performances \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6cc27-126"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="6cc27-127">Tous les compteurs du système.</span><span class="sxs-lookup"><span data-stu-id="6cc27-127">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="6cc27-128">*CaptionString*</span><span class="sxs-lookup"><span data-stu-id="6cc27-128">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc27-129">Variable de chaîne qui contient le texte qui sera affiché dans la barre de légende de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6cc27-129">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc27-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cc27-130">Return value</span></span>

<span data-ttu-id="6cc27-131">La fonction retourne le nombre de caractères écrits dans la mémoire tampon *PathString* .</span><span class="sxs-lookup"><span data-stu-id="6cc27-131">The function returns the number of characters written to the *PathString* buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc27-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cc27-132">Requirements</span></span>



| <span data-ttu-id="6cc27-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cc27-133">Requirement</span></span> | <span data-ttu-id="6cc27-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cc27-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc27-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cc27-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc27-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cc27-136">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cc27-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cc27-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc27-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cc27-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6cc27-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6cc27-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="6cc27-140"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cc27-140"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="6cc27-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6cc27-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cc27-142"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cc27-142"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cc27-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cc27-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc27-144">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="6cc27-144">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="6cc27-145">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="6cc27-145">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="6cc27-146">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="6cc27-146">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




