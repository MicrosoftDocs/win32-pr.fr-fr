---
title: Schtasks.exe
description: Permet à un administrateur de créer, supprimer, interroger, modifier, exécuter et terminer des tâches planifiées sur un ordinateur local ou distant.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe Planificateur de tâches
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 2a57ee4edae1cd1604f10a88f3fc8cf2ea0971fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533002"
---
# <a name="schtasksexe"></a><span data-ttu-id="99b81-104">Schtasks.exe</span><span class="sxs-lookup"><span data-stu-id="99b81-104">Schtasks.exe</span></span>

<span data-ttu-id="99b81-105">Permet à un administrateur de créer, supprimer, interroger, modifier, exécuter et terminer des tâches planifiées sur un ordinateur local ou distant.</span><span class="sxs-lookup"><span data-stu-id="99b81-105">Enables an administrator to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> <span data-ttu-id="99b81-106">L’exécution de Schtasks.exe sans arguments affiche l’État et l’heure de la prochaine exécution pour chaque tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="99b81-106">Running Schtasks.exe without arguments displays the status and next run time for each registered task.</span></span> 

<span data-ttu-id="99b81-107">Pour plus d’informations sur Planificateur de tâches, consultez l’introduction suivante : [Planificateur de tâches pour les développeurs](task-scheduler-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="99b81-107">For more information on Task Scheduler, see this introduction: [Task Scheduler for developers](task-scheduler-start-page.md).</span></span>

## <a name="creating-a-task"></a><span data-ttu-id="99b81-108">Création d’une tâche</span><span class="sxs-lookup"><span data-stu-id="99b81-108">Creating a Task</span></span>

<span data-ttu-id="99b81-109">La syntaxe suivante est utilisée pour créer une tâche sur l’ordinateur local ou distant.</span><span class="sxs-lookup"><span data-stu-id="99b81-109">The following syntax is used to create a task on the local or remote computer.</span></span>

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

## <a name="parameters"></a><span data-ttu-id="99b81-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99b81-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b81-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s</span><span class="sxs-lookup"><span data-stu-id="99b81-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-112">Valeur qui spécifie l’ordinateur distant auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="99b81-112">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="99b81-113">En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="99b81-113">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="99b81-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-115">Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="99b81-115">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**</span><span class="sxs-lookup"><span data-stu-id="99b81-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-117">Valeur qui spécifie le mot de passe pour un contexte utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="99b81-117">A value that specifies the password for a given user context.</span></span> <span data-ttu-id="99b81-118">En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.</span><span class="sxs-lookup"><span data-stu-id="99b81-118">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span> **Nom d’utilisateur** /ru</span><span class="sxs-lookup"><span data-stu-id="99b81-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/RU** **username**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-120">Valeur qui spécifie le contexte utilisateur sous lequel la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="99b81-120">A value that specifies the user context under which the task runs.</span></span> <span data-ttu-id="99b81-121">Pour le compte système, les valeurs valides sont « », «NT AUTHORITY \\ System » ou « System ».</span><span class="sxs-lookup"><span data-stu-id="99b81-121">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="99b81-122">Pour les tâches Planificateur de tâches 2,0, « NT AUTHORITY \\ LOCALSERVICE » et « NT Authority \\ NetworkService » sont également des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="99b81-122">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE", and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[ mot_de_passe \]**</span><span class="sxs-lookup"><span data-stu-id="99b81-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-124">Valeur qui spécifie le mot de passe de l’utilisateur spécifié avec le paramètre/RU.</span><span class="sxs-lookup"><span data-stu-id="99b81-124">A value that specifies the password for the user specified with the /RU parameter.</span></span> <span data-ttu-id="99b81-125">Pour demander le mot de passe, la valeur doit être « \* » ou aucune valeur.</span><span class="sxs-lookup"><span data-stu-id="99b81-125">To prompt for the password, the value must be either "\*" or no value.</span></span> <span data-ttu-id="99b81-126">Ce mot de passe est ignoré pour le compte système.</span><span class="sxs-lookup"><span data-stu-id="99b81-126">This password is ignored for the system account.</span></span> <span data-ttu-id="99b81-127">Ce paramètre doit être combiné avec le commutateur/RU ou/XML.</span><span class="sxs-lookup"><span data-stu-id="99b81-127">This parameter must be combined with either /RU or the /XML switch.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **planification**</span><span class="sxs-lookup"><span data-stu-id="99b81-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **schedule**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-129">Valeur qui spécifie la fréquence de planification.</span><span class="sxs-lookup"><span data-stu-id="99b81-129">A value that specifies the schedule frequency.</span></span> <span data-ttu-id="99b81-130">Les valeurs valides sont : MINUTE, heure, quotidien, hebdomadaire, mensuelle, ONCE, ONLOGON, ONIDLE et ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="99b81-130">Valid values are: MINUTE, HOURLY, DAILY, WEEKLY, MONTHLY, ONCE, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/Mo** ( **modificateur** )</span><span class="sxs-lookup"><span data-stu-id="99b81-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/MO** **modifier**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-132">Valeur qui affine le type de planification pour permettre un contrôle plus fin de la périodicité de la planification.</span><span class="sxs-lookup"><span data-stu-id="99b81-132">A value that refines the schedule type to allow for finer control over the schedule recurrence.</span></span> <span data-ttu-id="99b81-133">Les valeurs autorisées sont :</span><span class="sxs-lookup"><span data-stu-id="99b81-133">Valid values are:</span></span>

-   <span data-ttu-id="99b81-134">MINUTE : 1-1439 minutes.</span><span class="sxs-lookup"><span data-stu-id="99b81-134">MINUTE: 1 - 1439 minutes.</span></span>
-   <span data-ttu-id="99b81-135">Toutes les heures : 1-23 heures.</span><span class="sxs-lookup"><span data-stu-id="99b81-135">HOURLY: 1 - 23 hours.</span></span>
-   <span data-ttu-id="99b81-136">QUOTIDIENNE : 1-365 jours.</span><span class="sxs-lookup"><span data-stu-id="99b81-136">DAILY: 1 - 365 days.</span></span>
-   <span data-ttu-id="99b81-137">HEBDOMADAIRE : semaines 1-52.</span><span class="sxs-lookup"><span data-stu-id="99b81-137">WEEKLY: weeks 1 - 52.</span></span>
-   <span data-ttu-id="99b81-138">UNE fois : aucun modificateur.</span><span class="sxs-lookup"><span data-stu-id="99b81-138">ONCE: No modifiers.</span></span>
-   <span data-ttu-id="99b81-139">ONSTARt : aucun modificateur.</span><span class="sxs-lookup"><span data-stu-id="99b81-139">ONSTART: No modifiers.</span></span>
-   <span data-ttu-id="99b81-140">ONLOGON : aucun modificateur.</span><span class="sxs-lookup"><span data-stu-id="99b81-140">ONLOGON: No modifiers.</span></span>
-   <span data-ttu-id="99b81-141">ONIDLE : aucun modificateur.</span><span class="sxs-lookup"><span data-stu-id="99b81-141">ONIDLE: No modifiers.</span></span>
-   <span data-ttu-id="99b81-142">MENSUELLE : 1-12 ou premier, deuxième, troisième, quatrième, dernier et LASTDAY.</span><span class="sxs-lookup"><span data-stu-id="99b81-142">MONTHLY: 1 - 12, or FIRST, SECOND, THIRD, FOURTH, LAST, and LASTDAY.</span></span>
-   <span data-ttu-id="99b81-143">ONEVENT : chaîne de requête d’événement XPath.</span><span class="sxs-lookup"><span data-stu-id="99b81-143">ONEVENT: XPath event query string.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **jours**</span><span class="sxs-lookup"><span data-stu-id="99b81-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **days**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-145">Valeur qui spécifie le jour de la semaine où exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-145">A value that specifies the day of the week to run the task.</span></span> <span data-ttu-id="99b81-146">Les valeurs valides sont les suivantes : Lun, Mar, WED, Thou, Ven, SAT, SUN et pour les planifications MENSUELles 1-31 (jours du mois).</span><span class="sxs-lookup"><span data-stu-id="99b81-146">Valid values are: MON, TUE, WED, THU, FRI, SAT, SUN and for MONTHLY schedules 1 - 31 (days of the month).</span></span> <span data-ttu-id="99b81-147">Le caractère générique ( \* ) spécifie tous les jours.</span><span class="sxs-lookup"><span data-stu-id="99b81-147">The wildcard character (\*) specifies all days.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **mois**</span><span class="sxs-lookup"><span data-stu-id="99b81-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **months**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-149">Valeur qui spécifie les mois de l’année.</span><span class="sxs-lookup"><span data-stu-id="99b81-149">A value that specifies months of the year.</span></span> <span data-ttu-id="99b81-150">La valeur par défaut est le premier jour du mois.</span><span class="sxs-lookup"><span data-stu-id="99b81-150">Defaults to the first day of the month.</span></span> <span data-ttu-id="99b81-151">Les valeurs valides sont les suivantes : JAN, fév, MAR, APR, mai, JUN, JUL, aoû, SEP, OCT, NOV et DEC.</span><span class="sxs-lookup"><span data-stu-id="99b81-151">Valid values are: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV, and DEC.</span></span> <span data-ttu-id="99b81-152">Le caractère générique ( \* ) spécifie tous les mois.</span><span class="sxs-lookup"><span data-stu-id="99b81-152">The wildcard character (\*) specifies all months.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **IdleTime**</span><span class="sxs-lookup"><span data-stu-id="99b81-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-154">Valeur qui spécifie la durée d’inactivité en attente avant l’exécution d’une tâche ONIDLE planifiée.</span><span class="sxs-lookup"><span data-stu-id="99b81-154">A value that specifies the amount of idle time to wait before running a scheduled ONIDLE task.</span></span> <span data-ttu-id="99b81-155">La plage valide est de 1-999 minutes.</span><span class="sxs-lookup"><span data-stu-id="99b81-155">The valid range is 1 - 999 minutes.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**</span><span class="sxs-lookup"><span data-stu-id="99b81-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-157">Valeur qui spécifie un nom qui identifie de façon unique la tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="99b81-157">A value that specifies a name which uniquely identifies the scheduled task.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **exécution_tâche**</span><span class="sxs-lookup"><span data-stu-id="99b81-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-159">Valeur qui spécifie le chemin d’accès et le nom de fichier de la tâche à exécuter à l’heure planifiée.</span><span class="sxs-lookup"><span data-stu-id="99b81-159">A value that specifies the path and file name of the task to be run at the scheduled time.</span></span> <span data-ttu-id="99b81-160">Par exemple : C : \\ Windows \\ system32 \\calc.exe.</span><span class="sxs-lookup"><span data-stu-id="99b81-160">For example: C:\\Windows\\System32\\calc.exe.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**</span><span class="sxs-lookup"><span data-stu-id="99b81-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-162">Valeur qui spécifie l’heure de début de l’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-162">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="99b81-163">Le format de l’heure est HH : mm (24 heures).</span><span class="sxs-lookup"><span data-stu-id="99b81-163">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="99b81-164">Par exemple, 14:30 spécifie 2:30.</span><span class="sxs-lookup"><span data-stu-id="99b81-164">For example, 14:30 specifies 2:30PM.</span></span> <span data-ttu-id="99b81-165">La valeur par défaut est l’heure actuelle:/ST n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="99b81-165">The default is the current time is /ST is not specified.</span></span> <span data-ttu-id="99b81-166">Cette option est requise pour l’argument/SC ONCE.</span><span class="sxs-lookup"><span data-stu-id="99b81-166">This option is required wit the /SC ONCE argument.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **intervalle**</span><span class="sxs-lookup"><span data-stu-id="99b81-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-168">Valeur qui spécifie l’intervalle de répétition en minutes.</span><span class="sxs-lookup"><span data-stu-id="99b81-168">A value that specifies the repetition interval in minutes.</span></span> <span data-ttu-id="99b81-169">Cela ne s’applique pas aux types de planification suivants : MINUTE, HOURly, ONSTARt, ONLOGON, ONIDLE et ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="99b81-169">This is not applicable for the following schedule types: MINUTE, HOURLY, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="99b81-170">La plage valide est de 1-599940 minutes.</span><span class="sxs-lookup"><span data-stu-id="99b81-170">The valid range is 1 - 599940 minutes.</span></span> <span data-ttu-id="99b81-171">Si les paramètres/ET ou/DU sont spécifiés, la valeur par défaut est 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="99b81-171">If either the /ET or /DU parameters are specified, the default is 10 minutes.</span></span>

<span data-ttu-id="99b81-172">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-172">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **heure_fin**</span><span class="sxs-lookup"><span data-stu-id="99b81-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-174">Valeur qui spécifie l’heure de fin de l’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-174">A value that specifies the end time to run the task.</span></span> <span data-ttu-id="99b81-175">Le format de l’heure est HH : mm (24 heures).</span><span class="sxs-lookup"><span data-stu-id="99b81-175">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="99b81-176">Par exemple, 14:50 spécifie 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="99b81-176">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="99b81-177">Cela ne s’applique pas aux types de planification suivants : ONSTARt, ONLOGON, ONIDLE et ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="99b81-177">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

<span data-ttu-id="99b81-178">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-178">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span> **Durée** /du</span><span class="sxs-lookup"><span data-stu-id="99b81-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-180">Valeur qui spécifie la durée d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-180">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="99b81-181">Le format de l’heure est HH : mm (24 heures).</span><span class="sxs-lookup"><span data-stu-id="99b81-181">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="99b81-182">Par exemple, 14:50 spécifie 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="99b81-182">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="99b81-183">Cela ne s’applique pas à/ET et aux types de planification suivants : ONSTARt, ONLOGON, ONIDLE et ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="99b81-183">This is not applicable with /ET and for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="99b81-184">Pour les tâches/v1 (tâches Planificateur de tâches 1,0), si/RI est spécifié, la durée par défaut est d’une heure.</span><span class="sxs-lookup"><span data-stu-id="99b81-184">For /V1 tasks (Task Scheduler 1.0 tasks), if /RI is specified, then the duration default is one hour.</span></span>

<span data-ttu-id="99b81-185">**Windows XP :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-185">**Windows XP:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="99b81-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-187">Valeur qui termine la tâche à l’heure de fin ou de la durée.</span><span class="sxs-lookup"><span data-stu-id="99b81-187">A value that terminates the task at the end time or duration time.</span></span> <span data-ttu-id="99b81-188">Cela ne s’applique pas aux types de planification suivants : ONSTARt, ONLOGON, ONIDLE et ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="99b81-188">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="99b81-189">Vous devez spécifier/ET ou/DU.</span><span class="sxs-lookup"><span data-stu-id="99b81-189">Either /ET or /DU must be specified.</span></span>

<span data-ttu-id="99b81-190">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-190">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **DateDébut**</span><span class="sxs-lookup"><span data-stu-id="99b81-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-192">Valeur qui spécifie la première date à laquelle la tâche doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="99b81-192">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="99b81-193">Le format est mm/jj/aaaa.</span><span class="sxs-lookup"><span data-stu-id="99b81-193">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="99b81-194">La valeur par défaut est la date actuelle.</span><span class="sxs-lookup"><span data-stu-id="99b81-194">This value defaults to the current date.</span></span> <span data-ttu-id="99b81-195">Cela ne s’applique pas aux types de planification suivants : ONCE, ONSTARt, ONLOGON, ONIDLE et ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="99b81-195">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**</span><span class="sxs-lookup"><span data-stu-id="99b81-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-197">Valeur qui spécifie la dernière date à laquelle la tâche s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="99b81-197">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="99b81-198">Le format est mm/jj/aaaa.</span><span class="sxs-lookup"><span data-stu-id="99b81-198">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="99b81-199">Cela ne s’applique pas aux types de planification suivants : ONCE, ONSTARt, ONLOGON, ONIDLE et ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="99b81-199">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/Ce** **ChannelName**</span><span class="sxs-lookup"><span data-stu-id="99b81-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-201">Valeur qui spécifie le canal d’événement pour les déclencheurs ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="99b81-201">A value that specifies the event channel for ONEVENT triggers.</span></span>

<span data-ttu-id="99b81-202">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-202">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="99b81-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-204">Valeur qui permet à la tâche de s’exécuter de manière interactive uniquement si l’utilisateur/RU est actuellement connecté au moment de l’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-204">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="99b81-205">La tâche s’exécute uniquement si l’utilisateur a ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="99b81-205">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="99b81-206">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-206">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span><span class="sxs-lookup"><span data-stu-id="99b81-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-208">Valeur qui indique qu’aucun mot de passe n’est stocké.</span><span class="sxs-lookup"><span data-stu-id="99b81-208">A value that indicates that no password is stored.</span></span> <span data-ttu-id="99b81-209">La tâche ne s’exécute pas de manière interactive en tant qu’utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="99b81-209">The task does not run interactively as the given user.</span></span> <span data-ttu-id="99b81-210">Seules les ressources locales sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="99b81-210">Only local resources are available.</span></span>

<span data-ttu-id="99b81-211">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-211">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-212"><span id="_Z_"></span><span id="_z_"></span>**Z**</span><span class="sxs-lookup"><span data-stu-id="99b81-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-213">Valeur qui marque la tâche à supprimer après sa dernière exécution.</span><span class="sxs-lookup"><span data-stu-id="99b81-213">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="99b81-214">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-214">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**</span><span class="sxs-lookup"><span data-stu-id="99b81-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-216">Valeur qui crée une tâche à partir d’un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="99b81-216">A value that creates a task from an XML file.</span></span> <span data-ttu-id="99b81-217">Ce paramètre peut être combiné avec les commutateurs/RU et/RP, ou avec le commutateur/RP seul lorsque le fichier XML de la tâche contient déjà le principal.</span><span class="sxs-lookup"><span data-stu-id="99b81-217">This parameter can be combined with /RU and /RP switches, or with the /RP switch alone when the task XML already contains the principal.</span></span>

<span data-ttu-id="99b81-218">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-218">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span><span class="sxs-lookup"><span data-stu-id="99b81-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-220">Valeur qui crée une tâche visible pour les plateformes Windows 2000, Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="99b81-220">A value that creates a task visible to Windows 2000, Windows Server 2003, and Windows XP platforms.</span></span>

<span data-ttu-id="99b81-221">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-221">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="99b81-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-223">Valeur qui force la création de la tâche et supprime les avertissements si la tâche spécifiée existe déjà.</span><span class="sxs-lookup"><span data-stu-id="99b81-223">A value that forcefully creates the task and suppresses warnings if the specified task already exists.</span></span>

<span data-ttu-id="99b81-224">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-224">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Niveau** /RL</span><span class="sxs-lookup"><span data-stu-id="99b81-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-226">Valeur qui définit le niveau d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-226">A value that sets the run level for the task.</span></span> <span data-ttu-id="99b81-227">Les valeurs valides sont LIMITED et HIGHEST.</span><span class="sxs-lookup"><span data-stu-id="99b81-227">Valid values are LIMITED and HIGHEST.</span></span> <span data-ttu-id="99b81-228">La valeur par défaut est LIMITED.</span><span class="sxs-lookup"><span data-stu-id="99b81-228">The default is LIMITED.</span></span>

<span data-ttu-id="99b81-229">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-229">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **DelayTime**</span><span class="sxs-lookup"><span data-stu-id="99b81-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-231">Valeur qui spécifie le temps d’attente pour retarder la tâche après le déclenchement du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="99b81-231">A value that specifies the wait time to delay the task after the trigger is fired.</span></span> <span data-ttu-id="99b81-232">Le format de l’heure est mmmm : SS.</span><span class="sxs-lookup"><span data-stu-id="99b81-232">The time format is mmmm:ss.</span></span> <span data-ttu-id="99b81-233">Cette option est valide uniquement pour les types de planification ONSTARt, ONLOGON et ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="99b81-233">This option is only valid for schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="99b81-234">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-234">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-235"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="99b81-235"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-236">Valeur qui affiche le message d’aide pour Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="99b81-236">A value that displays the help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99b81-237">Notes</span><span class="sxs-lookup"><span data-stu-id="99b81-237">Remarks</span></span>

<span data-ttu-id="99b81-238">Lorsque vous créez une tâche sur un ordinateur distant qui exécute le système d’exploitation Windows XP, Windows Server 2003 ou Windows 2000, utilisez le commutateur/v1</span><span class="sxs-lookup"><span data-stu-id="99b81-238">When creating a task on a remote computer running on the Windows XP, Windows Server 2003, or Windows 2000 operating system, use the /V1 switch.</span></span>

<span data-ttu-id="99b81-239">Vous ne pouvez pas créer une tâche de Planificateur de tâches à distance non interactive 1,0 (créez une tâche en n’utilisant pas le commutateur/IT et en utilisant le commutateur/v1) si l’exception de pare-feu de partage de fichiers et d’imprimantes est activée sur l’ordinateur distant et que l’exception de pare-feu de gestion des tâches planifiées distantes est désactivée.</span><span class="sxs-lookup"><span data-stu-id="99b81-239">You cannot create a non-interactive remote Task Scheduler 1.0 task (create a task by not using the /IT switch and using the /V1 switch) if the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled.</span></span>

## <a name="deleting-a-task"></a><span data-ttu-id="99b81-240">Suppression d’une tâche</span><span class="sxs-lookup"><span data-stu-id="99b81-240">Deleting a Task</span></span>

<span data-ttu-id="99b81-241">La syntaxe suivante est utilisée pour supprimer une ou plusieurs tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="99b81-241">The following syntax is used to delete one or more scheduled tasks.</span></span>

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

## <a name="parameters"></a><span data-ttu-id="99b81-242">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99b81-242">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b81-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s</span><span class="sxs-lookup"><span data-stu-id="99b81-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-244">Valeur qui spécifie l’ordinateur distant auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="99b81-244">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="99b81-245">En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="99b81-245">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="99b81-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-247">Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="99b81-247">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**</span><span class="sxs-lookup"><span data-stu-id="99b81-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-249">Valeur qui spécifie le mot de passe pour le contexte utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="99b81-249">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="99b81-250">En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.</span><span class="sxs-lookup"><span data-stu-id="99b81-250">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**</span><span class="sxs-lookup"><span data-stu-id="99b81-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-252">Valeur qui spécifie le nom de la tâche planifiée à supprimer.</span><span class="sxs-lookup"><span data-stu-id="99b81-252">A value that specifies the name of the scheduled task to delete.</span></span> <span data-ttu-id="99b81-253">Le caractère générique ( \* ) peut être utilisé pour supprimer toutes les tâches.</span><span class="sxs-lookup"><span data-stu-id="99b81-253">The wildcard character (\*) can be used to delete all tasks.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="99b81-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-255">Valeur qui supprime la tâche de force et supprime les avertissements si la tâche spécifiée est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="99b81-255">A value that forcefully deletes the task and suppresses warnings if the specified task is running.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-256"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="99b81-256"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-257">Valeur qui affiche l’aide pour Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="99b81-257">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="running-a-task"></a><span data-ttu-id="99b81-258">Exécution d’une tâche</span><span class="sxs-lookup"><span data-stu-id="99b81-258">Running a Task</span></span>

<span data-ttu-id="99b81-259">La syntaxe suivante est utilisée pour exécuter immédiatement une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="99b81-259">The following syntax is used to immediately run a scheduled task.</span></span>

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

## <a name="parameters"></a><span data-ttu-id="99b81-260">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99b81-260">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b81-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s</span><span class="sxs-lookup"><span data-stu-id="99b81-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-262">Valeur qui spécifie l’ordinateur distant auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="99b81-262">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="99b81-263">En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="99b81-263">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="99b81-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-265">Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="99b81-265">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**</span><span class="sxs-lookup"><span data-stu-id="99b81-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-267">Valeur qui spécifie le mot de passe pour le contexte utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="99b81-267">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="99b81-268">En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.</span><span class="sxs-lookup"><span data-stu-id="99b81-268">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**</span><span class="sxs-lookup"><span data-stu-id="99b81-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-270">Valeur qui spécifie le nom de la tâche planifiée à exécuter.</span><span class="sxs-lookup"><span data-stu-id="99b81-270">A value that specifies the name of the scheduled task to run.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-271"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="99b81-271"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-272">Valeur qui affiche l’aide pour Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="99b81-272">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="ending-a-running-task"></a><span data-ttu-id="99b81-273">Fin d’une tâche en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="99b81-273">Ending a Running Task</span></span>

<span data-ttu-id="99b81-274">La syntaxe suivante est utilisée pour arrêter une tâche planifiée en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="99b81-274">The following syntax is used to stop a running scheduled task.</span></span>

> [!Note]  
> <span data-ttu-id="99b81-275">Pour arrêter l’exécution d’une tâche à distance, assurez-vous que le partage de fichiers et d’imprimantes et les exceptions de pare-feu de gestion à distance des tâches planifiées sont activés sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="99b81-275">To stop a remote task from running, ensure that the remote computer has the File and Printer Sharing and Remote Scheduled Tasks Management firewall exceptions enabled.</span></span>

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

## <a name="parameters"></a><span data-ttu-id="99b81-276">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99b81-276">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b81-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s</span><span class="sxs-lookup"><span data-stu-id="99b81-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-278">Valeur qui spécifie l’ordinateur distant auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="99b81-278">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="99b81-279">En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="99b81-279">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="99b81-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-281">Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="99b81-281">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**</span><span class="sxs-lookup"><span data-stu-id="99b81-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-283">Valeur qui spécifie le mot de passe pour le contexte utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="99b81-283">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="99b81-284">En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.</span><span class="sxs-lookup"><span data-stu-id="99b81-284">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**</span><span class="sxs-lookup"><span data-stu-id="99b81-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-286">Valeur qui spécifie le nom de la tâche planifiée à arrêter.</span><span class="sxs-lookup"><span data-stu-id="99b81-286">A value that specifies the name of the scheduled task to stop.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-287"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="99b81-287"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-288">Valeur qui affiche l’aide pour Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="99b81-288">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="querying-for-task-information"></a><span data-ttu-id="99b81-289">Interrogation des informations sur les tâches</span><span class="sxs-lookup"><span data-stu-id="99b81-289">Querying for Task Information</span></span>

<span data-ttu-id="99b81-290">La syntaxe suivante est utilisée pour afficher les tâches planifiées à partir de l’ordinateur local ou distant.</span><span class="sxs-lookup"><span data-stu-id="99b81-290">The following syntax is used to display the scheduled tasks from the local or remote computer.</span></span>

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

## <a name="parameters"></a><span data-ttu-id="99b81-291">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99b81-291">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b81-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s</span><span class="sxs-lookup"><span data-stu-id="99b81-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-293">Valeur qui spécifie l’ordinateur distant auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="99b81-293">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="99b81-294">En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="99b81-294">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="99b81-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-296">Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="99b81-296">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**</span><span class="sxs-lookup"><span data-stu-id="99b81-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-298">Valeur qui spécifie le mot de passe pour le contexte utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="99b81-298">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="99b81-299">En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.</span><span class="sxs-lookup"><span data-stu-id="99b81-299">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **format**</span><span class="sxs-lookup"><span data-stu-id="99b81-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **format**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-301">Valeur qui spécifie le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="99b81-301">A value that specifies the output format.</span></span> <span data-ttu-id="99b81-302">Les valeurs valides sont TABLE, LIST et CSV.</span><span class="sxs-lookup"><span data-stu-id="99b81-302">The valid values are TABLE, LIST, and CSV.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span><span class="sxs-lookup"><span data-stu-id="99b81-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-304">Valeur qui spécifie que l’en-tête de colonne ne doit pas être affiché dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="99b81-304">A value that specifies that the column header should not be displayed in the output.</span></span> <span data-ttu-id="99b81-305">Cela est valide uniquement pour les formats TABLE et CSV.</span><span class="sxs-lookup"><span data-stu-id="99b81-305">This is valid only for TABLE and CSV formats.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-306"><span id="_V_"></span><span id="_v_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="99b81-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-307">Valeur qui affiche la sortie de tâche détaillée.</span><span class="sxs-lookup"><span data-stu-id="99b81-307">A value that displays verbose task output.</span></span>

> [!Note]  
> <span data-ttu-id="99b81-308">Si une tâche était planifiée pour s’exécuter une seule fois, les informations de planification affichées sont « les données de planification ne sont pas disponibles dans ce format ».</span><span class="sxs-lookup"><span data-stu-id="99b81-308">If a task was scheduled to run only one time, then the displayed schedule information is "Scheduling data is not available in this format."</span></span>

 

</dd> <dt>

<span data-ttu-id="99b81-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**</span><span class="sxs-lookup"><span data-stu-id="99b81-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-310">Valeur qui spécifie le nom de la tâche pour laquelle les informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="99b81-310">A value that specifies the task name for which to retrieve the information.</span></span> <span data-ttu-id="99b81-311">Si aucun nom de tâche n’est spécifié, les informations relatives à toutes les tâches sont affichées.</span><span class="sxs-lookup"><span data-stu-id="99b81-311">If no task name is specified, then information for all the tasks will be displayed.</span></span>

<span data-ttu-id="99b81-312">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-312">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span><span class="sxs-lookup"><span data-stu-id="99b81-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-314">Valeur utilisée pour afficher les définitions de tâche au format XML.</span><span class="sxs-lookup"><span data-stu-id="99b81-314">A value that is used to display the task definitions in XML format.</span></span>

<span data-ttu-id="99b81-315">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-315">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-316"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="99b81-316"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-317">Valeur utilisée pour afficher l’aide de Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="99b81-317">A value that is used to display the Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="changing-a-task"></a><span data-ttu-id="99b81-318">Modification d’une tâche</span><span class="sxs-lookup"><span data-stu-id="99b81-318">Changing a Task</span></span>

<span data-ttu-id="99b81-319">La syntaxe suivante est utilisée pour modifier le mode d’exécution du programme, ou pour modifier le compte d’utilisateur et le mot de passe utilisés par une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="99b81-319">The following syntax is used to change how the program runs, or change the user account and password used by a scheduled task.</span></span>

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

## <a name="parameters"></a><span data-ttu-id="99b81-320">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99b81-320">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b81-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s</span><span class="sxs-lookup"><span data-stu-id="99b81-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-322">Valeur qui spécifie l’ordinateur distant auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="99b81-322">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="99b81-323">En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="99b81-323">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="99b81-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-325">Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="99b81-325">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**</span><span class="sxs-lookup"><span data-stu-id="99b81-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-327">Valeur qui spécifie le mot de passe pour le contexte utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="99b81-327">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="99b81-328">En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.</span><span class="sxs-lookup"><span data-stu-id="99b81-328">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**</span><span class="sxs-lookup"><span data-stu-id="99b81-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-330">Valeur qui spécifie la tâche planifiée à modifier.</span><span class="sxs-lookup"><span data-stu-id="99b81-330">A value that specifies which scheduled task to change.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/Ru** **nom_d’emprunt**</span><span class="sxs-lookup"><span data-stu-id="99b81-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **runasuser**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-332">Valeur qui modifie le nom d’utilisateur (contexte utilisateur) sous lequel la tâche planifiée s’exécute.</span><span class="sxs-lookup"><span data-stu-id="99b81-332">A value that changes the user name (user context) under which the scheduled task will run.</span></span> <span data-ttu-id="99b81-333">Pour le compte système, les valeurs valides sont « », «NT AUTHORITY \\ System » ou « System ».</span><span class="sxs-lookup"><span data-stu-id="99b81-333">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="99b81-334">Pour les tâches Planificateur de tâches 2,0, les \\ \\ valeurs valides sont également valides : « NT Authority LOCALSERVICE » et « NT Authority NetworkService ».</span><span class="sxs-lookup"><span data-stu-id="99b81-334">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE" and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span><span class="sxs-lookup"><span data-stu-id="99b81-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-336">Valeur qui spécifie un nouveau mot de passe pour le contexte utilisateur existant ou le mot de passe d’un nouveau compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="99b81-336">A value that specifies a new password for the existing user context or the password for a new user account.</span></span> <span data-ttu-id="99b81-337">Ce mot de passe est ignoré pour le compte système.</span><span class="sxs-lookup"><span data-stu-id="99b81-337">This password is ignored for the system account.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **exécution_tâche**</span><span class="sxs-lookup"><span data-stu-id="99b81-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-339">Valeur qui spécifie un nouveau programme que la tâche exécutera.</span><span class="sxs-lookup"><span data-stu-id="99b81-339">A value that specifies a new program that the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**</span><span class="sxs-lookup"><span data-stu-id="99b81-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-341">Valeur qui spécifie l’heure de début de l’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-341">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="99b81-342">Le format de l’heure est HH : mm (24 heures).</span><span class="sxs-lookup"><span data-stu-id="99b81-342">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="99b81-343">Par exemple, 14:30 spécifie 2:30.</span><span class="sxs-lookup"><span data-stu-id="99b81-343">For example, 14:30 specifies 2:30PM.</span></span>

<span data-ttu-id="99b81-344">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-344">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **intervalle**</span><span class="sxs-lookup"><span data-stu-id="99b81-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-346">Valeur qui spécifie l’intervalle de répétition, en minutes.</span><span class="sxs-lookup"><span data-stu-id="99b81-346">A value that specifies the repetition interval, in minutes.</span></span> <span data-ttu-id="99b81-347">La plage valide est de 1-599940 minutes.</span><span class="sxs-lookup"><span data-stu-id="99b81-347">The valid range is 1 - 599940 minutes.</span></span>

<span data-ttu-id="99b81-348">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-348">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **heure_fin**</span><span class="sxs-lookup"><span data-stu-id="99b81-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-350">Valeur qui spécifie l’heure de fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-350">A value that specifies the end time for the task.</span></span> <span data-ttu-id="99b81-351">Le format de l’heure est HH : mm (24 heures).</span><span class="sxs-lookup"><span data-stu-id="99b81-351">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="99b81-352">Par exemple, 14:50 spécifie 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="99b81-352">For example, 14:50 specifies 2:50PM.</span></span>

<span data-ttu-id="99b81-353">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-353">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span> **Durée** /du</span><span class="sxs-lookup"><span data-stu-id="99b81-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-355">Valeur qui spécifie la durée d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-355">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="99b81-356">Le format de l’heure est HH : mm (24 heures).</span><span class="sxs-lookup"><span data-stu-id="99b81-356">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="99b81-357">Par exemple, 14:50 spécifie 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="99b81-357">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="99b81-358">Cela ne s’applique pas au paramètre/ET.</span><span class="sxs-lookup"><span data-stu-id="99b81-358">This is not applicable with the /ET parameter.</span></span>

<span data-ttu-id="99b81-359">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-359">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="99b81-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-361">Valeur qui termine la tâche à l’heure de fin ou de la durée.</span><span class="sxs-lookup"><span data-stu-id="99b81-361">A value that terminates the task at the end time or duration time.</span></span>

<span data-ttu-id="99b81-362">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-362">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **DateDébut**</span><span class="sxs-lookup"><span data-stu-id="99b81-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-364">Valeur qui spécifie la première date à laquelle la tâche doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="99b81-364">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="99b81-365">Le format est mm/jj/aaaa.</span><span class="sxs-lookup"><span data-stu-id="99b81-365">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="99b81-366">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-366">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**</span><span class="sxs-lookup"><span data-stu-id="99b81-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-368">Valeur qui spécifie la dernière date à laquelle la tâche s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="99b81-368">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="99b81-369">Le format est mm/jj/aaaa.</span><span class="sxs-lookup"><span data-stu-id="99b81-369">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="99b81-370">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-370">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="99b81-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-372">Valeur qui permet à la tâche de s’exécuter de manière interactive uniquement si l’utilisateur/RU est actuellement connecté au moment de l’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-372">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="99b81-373">La tâche s’exécute uniquement si l’utilisateur a ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="99b81-373">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="99b81-374">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-374">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Niveau** /RL</span><span class="sxs-lookup"><span data-stu-id="99b81-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-376">Valeur qui définit le niveau d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="99b81-376">A value that sets the run level for the task.</span></span> <span data-ttu-id="99b81-377">Les valeurs valides sont LIMITED et HIGHEST.</span><span class="sxs-lookup"><span data-stu-id="99b81-377">Valid values are LIMITED and HIGHEST.</span></span>

<span data-ttu-id="99b81-378">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-378">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span><span class="sxs-lookup"><span data-stu-id="99b81-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-380">Valeur qui active la tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="99b81-380">A value that enables the scheduled task.</span></span> <span data-ttu-id="99b81-381">Une tâche activée peut s’exécuter et une tâche désactivée ne peut pas s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="99b81-381">An enabled task can run, and a disabled task cannot run.</span></span>

<span data-ttu-id="99b81-382">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-382">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span><span class="sxs-lookup"><span data-stu-id="99b81-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-384">Valeur qui désactive l’exécution de la tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="99b81-384">A value that disables the scheduled task from running.</span></span>

> [!Note]  
> <span data-ttu-id="99b81-385">Si une tâche Planificateur de tâches distante 1,0 est désactivée par Schtasks.exe et que l’exception de pare-feu partage de fichiers et d’imprimantes est activée et que l’exception de pare-feu de gestion des tâches planifiées distantes est désactivée, la tâche ne sera pas désactivée lors de la lecture à partir d’une API Planificateur de tâches 2,0.</span><span class="sxs-lookup"><span data-stu-id="99b81-385">If a remote Task Scheduler 1.0 task is disabled by Schtasks.exe and the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled, then the task will not be disabled when read from a Task Scheduler 2.0 API.</span></span>

 

<span data-ttu-id="99b81-386">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-386">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-387"><span id="_Z_"></span><span id="_z_"></span>**Z**</span><span class="sxs-lookup"><span data-stu-id="99b81-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-388">Valeur qui marque la tâche à supprimer après sa dernière exécution.</span><span class="sxs-lookup"><span data-stu-id="99b81-388">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="99b81-389">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-389">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **DelayTime**</span><span class="sxs-lookup"><span data-stu-id="99b81-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="99b81-391">Valeur qui spécifie le temps d’attente pour retarder l’exécution de la tâche après le déclenchement du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="99b81-391">A value that specifies the wait time to delay the running of the task after the trigger is fired.</span></span> <span data-ttu-id="99b81-392">Le format de l’heure est mmmm : SS.</span><span class="sxs-lookup"><span data-stu-id="99b81-392">The time format is mmmm:ss.</span></span> <span data-ttu-id="99b81-393">Cette option est valide uniquement pour les tâches avec les types de planification ONSTARt, ONLOGON et ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="99b81-393">This option is only valid for tasks with the schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="99b81-394">**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="99b81-394">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="99b81-395"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="99b81-395"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="99b81-396">Valeur qui affiche le message d’aide pour Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="99b81-396">A value that displays the Help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99b81-397">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99b81-397">Requirements</span></span>



| <span data-ttu-id="99b81-398">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99b81-398">Requirement</span></span> | <span data-ttu-id="99b81-399">Valeur</span><span class="sxs-lookup"><span data-stu-id="99b81-399">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99b81-400">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99b81-400">Minimum supported client</span></span><br/> | <span data-ttu-id="99b81-401">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99b81-401">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="99b81-402">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99b81-402">Minimum supported server</span></span><br/> | <span data-ttu-id="99b81-403">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99b81-403">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 





