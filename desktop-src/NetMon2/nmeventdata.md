---
description: La structure NMEVENTDATA contient des informations sur une condition d’événement qui est transmise à Moniteur réseau pour insérer une ligne dans la visionneuse d’experts.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: NMEVENTDATA, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863030"
---
# <a name="nmeventdata-structure"></a><span data-ttu-id="5b92c-103">NMEVENTDATA, structure</span><span class="sxs-lookup"><span data-stu-id="5b92c-103">NMEVENTDATA structure</span></span>

<span data-ttu-id="5b92c-104">La structure **NMEVENTDATA** contient des informations sur une condition d’événement qui est transmise à Moniteur réseau pour insérer une ligne dans la visionneuse d’experts.</span><span class="sxs-lookup"><span data-stu-id="5b92c-104">The **NMEVENTDATA** structure contains information about an event condition that is passed to Network Monitor to insert a line in the expert viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b92c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b92c-105">Syntax</span></span>


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a><span data-ttu-id="5b92c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5b92c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b92c-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="5b92c-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-108">Numéro de version de la structure **NMEVENTDATA** .</span><span class="sxs-lookup"><span data-stu-id="5b92c-108">Version number of the **NMEVENTDATA** structure.</span></span> <span data-ttu-id="5b92c-109">Le numéro de version doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5b92c-109">The version number must be zero.</span></span> <span data-ttu-id="5b92c-110">Les futures versions de Moniteur réseau peuvent prendre en charge un numéro de version plus élevé.</span><span class="sxs-lookup"><span data-stu-id="5b92c-110">Future versions of Network Monitor may support a higher version number.</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-111">**EventIdent**</span><span class="sxs-lookup"><span data-stu-id="5b92c-111">**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-112">Identificateur de l’événement.</span><span class="sxs-lookup"><span data-stu-id="5b92c-112">Identifier of the event.</span></span> <span data-ttu-id="5b92c-113">**EventIdent** est unique pour chaque expert et référence une [page de référence d’événement](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="5b92c-113">**EventIdent** is unique to each expert, and references an [event reference page](event-reference-page.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-114">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="5b92c-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-115">Ensemble d’indicateurs qui décrit qui envoie les données d’événement et comment l’événement est affiché.</span><span class="sxs-lookup"><span data-stu-id="5b92c-115">A set of flags that describes who sends the event data, and how the event is displayed.</span></span>



| <span data-ttu-id="5b92c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b92c-116">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="5b92c-117">Signification</span><span class="sxs-lookup"><span data-stu-id="5b92c-117">Meaning</span></span>                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <span data-ttu-id="5b92c-118"><dt>**\_expert en indicateurs d’événements \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-118"><dt>**EVENT\_FLAG\_EXPERT**</dt></span></span> </dl>                                                                         | <span data-ttu-id="5b92c-119">L’événement provient d’un expert.</span><span class="sxs-lookup"><span data-stu-id="5b92c-119">The event came from an expert.</span></span> <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <span data-ttu-id="5b92c-120"><dt>**NMEVENTFLAG \_ n' \_ affiche pas la \_ \_ gravité**</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-120"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SEVERITY**</dt></span></span> </dl>                 | <span data-ttu-id="5b92c-121">N’affiche pas le niveau de gravité de l’événement.</span><span class="sxs-lookup"><span data-stu-id="5b92c-121">Do not display the severity level for the event.</span></span> <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <span data-ttu-id="5b92c-122"><dt>**NMEVENTFLAG \_ n' \_ affiche pas la \_ \_ source**</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-122"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SOURCE**</dt></span></span> </dl>                       | <span data-ttu-id="5b92c-123">N’affiche pas le nom de la source de l’événement.</span><span class="sxs-lookup"><span data-stu-id="5b92c-123">Do not display the source name for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <span data-ttu-id="5b92c-124"><dt>**NMEVENTFLAG \_ n' \_ affiche pas le nom de l' \_ \_ événement \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-124"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_EVENT\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="5b92c-125">N’affiche pas le nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="5b92c-125">Do not display the event name for the event.</span></span> <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <span data-ttu-id="5b92c-126"><dt>**NMEVENTFLAG \_ ne \_ pas \_ afficher la \_ Description**</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-126"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_DESCRIPTION**</dt></span></span> </dl>        | <span data-ttu-id="5b92c-127">N’affiche pas la description de l’événement.</span><span class="sxs-lookup"><span data-stu-id="5b92c-127">Do not display the description for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <span data-ttu-id="5b92c-128"><dt>**NMEVENTFLAG \_ n' \_ affiche pas l' \_ \_ ordinateur**</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-128"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_MACHINE**</dt></span></span> </dl>                    | <span data-ttu-id="5b92c-129">N’affiche pas le nom de l’ordinateur pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="5b92c-129">Do not display the machine name for the event.</span></span> <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <span data-ttu-id="5b92c-130"><dt>**NMEVENTFLAG \_ n' \_ affiche pas l' \_ \_ heure**</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-130"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_TIME**</dt></span></span> </dl>                             | <span data-ttu-id="5b92c-131">Ne pas afficher l’heure de l’événement</span><span class="sxs-lookup"><span data-stu-id="5b92c-131">Do not display the time for the event</span></span> <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <span data-ttu-id="5b92c-132"><dt>**NMEVENTFLAG \_ n' \_ \_ affiche pas \_ les \_ colonnes fixes**</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-132"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_FIXED\_COLUMNS**</dt></span></span> </dl> | <span data-ttu-id="5b92c-133">N’affiche pas les colonnes gravité, source, nom de l’événement, description, machine ou heure.</span><span class="sxs-lookup"><span data-stu-id="5b92c-133">Do not display the Severity, Source, Event Name, Description, Machine, or Time columns.</span></span> <span data-ttu-id="5b92c-134">Il ne s’agit pas d’un indicateur unique, mais il s’agit d’une Union des six précédents indicateurs.</span><span class="sxs-lookup"><span data-stu-id="5b92c-134">This is not a single flag, but it is a union of the previous six flags.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="5b92c-135">**Niveau de gravité**</span><span class="sxs-lookup"><span data-stu-id="5b92c-135">**Severity**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-136">Niveau de gravité de l’événement.</span><span class="sxs-lookup"><span data-stu-id="5b92c-136">Severity level of the event.</span></span> <span data-ttu-id="5b92c-137">Le niveau de gravité peut avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5b92c-137">The severity level can have one of the following values:</span></span>

<span data-ttu-id="5b92c-138">NMEVENT \_ Severity \_ information NMEVENT \_ gravité \_ Warning NMEVENT \_ gravité \_ Strong \_ Warning NMEVENT \_ gravité \_ erreur NMEVENT \_ gravité \_ grave \_ erreur NMEVENT \_ gravité \_ critique \_</span><span class="sxs-lookup"><span data-stu-id="5b92c-138">NMEVENT\_SEVERITY\_INFORMATIONAL NMEVENT\_SEVERITY\_WARNING NMEVENT\_SEVERITY\_STRONG\_WARNING NMEVENT\_SEVERITY\_ERROR NMEVENT\_SEVERITY\_SEVERE\_ERROR NMEVENT\_SEVERITY\_CRITICAL\_ERROR</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-139">**NumColumns**</span><span class="sxs-lookup"><span data-stu-id="5b92c-139">**NumColumns**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-140">Nombre de colonnes désignées dans la structure actuelle.</span><span class="sxs-lookup"><span data-stu-id="5b92c-140">Number of columns designated in the current structure.</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-141">**szSourceName**</span><span class="sxs-lookup"><span data-stu-id="5b92c-141">**szSourceName**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-142">Nom de l’expert qui est affiché.</span><span class="sxs-lookup"><span data-stu-id="5b92c-142">Name of the expert that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-143">**szEventName**</span><span class="sxs-lookup"><span data-stu-id="5b92c-143">**szEventName**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-144">Nom de l’événement qui est affiché.</span><span class="sxs-lookup"><span data-stu-id="5b92c-144">Name of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-145">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="5b92c-145">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-146">Description de l’événement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5b92c-146">Description of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-147">**szMachine**</span><span class="sxs-lookup"><span data-stu-id="5b92c-147">**szMachine**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-148">Obsolète, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5b92c-148">Obsolete, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-149">**Justification**</span><span class="sxs-lookup"><span data-stu-id="5b92c-149">**Justification**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-150">Informations affichées dans la deuxième fenêtre du observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="5b92c-150">Information displayed in the second window of the Event Viewer.</span></span> <span data-ttu-id="5b92c-151">Le membre de **Justification** peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5b92c-151">The **Justification** member may be **NULL**.</span></span> <span data-ttu-id="5b92c-152">Si la **valeur est null**, la deuxième fenêtre n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="5b92c-152">If it is **NULL**, the second window is not be visible.</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-153">**szUrl**</span><span class="sxs-lookup"><span data-stu-id="5b92c-153">**szUrl**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-154">Réservé ce membre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5b92c-154">Reserved; this member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-155">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="5b92c-155">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-156">Heure à laquelle la condition d’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="5b92c-156">Time at which the event condition occurs.</span></span> <span data-ttu-id="5b92c-157">L’heure est mesurée par rapport au début de la capture.</span><span class="sxs-lookup"><span data-stu-id="5b92c-157">The time is measured relative to the beginning of the capture.</span></span>

</dd> <dt>

<span data-ttu-id="5b92c-158">**Colonne**</span><span class="sxs-lookup"><span data-stu-id="5b92c-158">**Column**</span></span>
</dt> <dd>

<span data-ttu-id="5b92c-159">Tableau de structures de colonnes qui s’affiche dans le volet supérieur de la observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="5b92c-159">Table of column structures that appears in the top pane of the Event Viewer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b92c-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b92c-160">Requirements</span></span>



| <span data-ttu-id="5b92c-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b92c-161">Requirement</span></span> | <span data-ttu-id="5b92c-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b92c-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5b92c-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b92c-163">Minimum supported client</span></span><br/> | <span data-ttu-id="5b92c-164">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b92c-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5b92c-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b92c-165">Minimum supported server</span></span><br/> | <span data-ttu-id="5b92c-166">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b92c-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5b92c-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b92c-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b92c-168"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b92c-168"><dt>Netmon.h</dt></span></span> </dl> |



 

 




