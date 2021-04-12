---
description: Envoie un travail à un système d’exploitation pour une exécution à une date et une heure spécifiées à l’avenir.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317917"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="dea92-103">Créer une méthode de la \_ classe ScheduledJob Win32</span><span class="sxs-lookup"><span data-stu-id="dea92-103">Create method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="dea92-104">La méthode **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) soumet un travail à un système d’exploitation pour une exécution à une date et une heure spécifiées à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="dea92-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method submits a job to an operating system for execution at a specified time and date in the future.</span></span> <span data-ttu-id="dea92-105">Cette méthode nécessite que le service de planification soit démarré sur l’ordinateur sur lequel le travail est envoyé.</span><span class="sxs-lookup"><span data-stu-id="dea92-105">This method requires that the schedule service be started on the computer to which the job is submitted.</span></span>

<span data-ttu-id="dea92-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="dea92-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dea92-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dea92-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dea92-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea92-108">Syntax</span></span>


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a><span data-ttu-id="dea92-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dea92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea92-110">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dea92-110">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea92-111">Nom de la commande, du programme de traitement par lots ou du fichier binaire et des paramètres de ligne de commande que le service de planification utilise pour appeler le travail.</span><span class="sxs-lookup"><span data-stu-id="dea92-111">Name of the command, batch program, or binary file and command-line parameters that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="dea92-112">Exemple : « Defrag/q/f ».</span><span class="sxs-lookup"><span data-stu-id="dea92-112">Example: "defrag /q /f".</span></span>

</dd> <dt>

<span data-ttu-id="dea92-113">*StartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dea92-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea92-114">Temps universel coordonné (UTC) pour exécuter un travail.</span><span class="sxs-lookup"><span data-stu-id="dea92-114">Coordinated Universal Time (UTC) time to run a job.</span></span> <span data-ttu-id="dea92-115">Le formulaire doit être : «AAAAMMJJHHMMSS. MMMMMM (+-) OOO», où « AAAAMMJJ » doit être remplacé par « \* \* \* \* \* \* \* \* ».</span><span class="sxs-lookup"><span data-stu-id="dea92-115">The form must be: "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="dea92-116">Par exemple : « \* \* \* \* \* \* \* \* 143000.000000-420 » spécifie 14,30 (2:30 P.M.) PST avec l’heure d’été en vigueur.</span><span class="sxs-lookup"><span data-stu-id="dea92-116">For example: "\*\*\*\*\*\*\*\*143000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

<span data-ttu-id="dea92-117">La section « (+-) OOO » de la valeur de la propriété StartTime est le décalage actuel pour la traduction de l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="dea92-117">The "(+-)OOO" section of the StartTime property value is the current bias for local time translation.</span></span> <span data-ttu-id="dea92-118">Le biais correspond à la différence entre l’heure UTC et l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="dea92-118">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="dea92-119">Pour calculer le décalage pour votre fuseau horaire, multipliez le nombre d’heures d’avance ou de retard de l’heure de Greenwich (GMT) par 60 (utilisez un nombre positif comme nombre d’heures avant l’heure GMT et un nombre négatif si votre fuseau horaire est situé en arrière-plan GMT).</span><span class="sxs-lookup"><span data-stu-id="dea92-119">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="dea92-120">Ajoutez un 60 supplémentaire à votre calcul si votre fuseau horaire utilise l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="dea92-120">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="dea92-121">Par exemple, le fuseau horaire Pacifique est de huit heures après l’heure GMT. par conséquent, le décalage est égal à-420 (-8 \* 60 + 60) lorsque l’heure d’été est utilisée et-480 (-8 \* 60) lorsque l’heure d’été n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="dea92-121">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="dea92-122">Vous pouvez également déterminer la valeur du décalage en interrogeant la propriété Bias de la classe [**Win32 \_ TimeZone**](win32-timezone.md) .</span><span class="sxs-lookup"><span data-stu-id="dea92-122">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="dea92-123">*RunRepeatedly* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="dea92-123">*RunRepeatedly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dea92-124">Si la **valeur est true**, une tâche planifiée s’exécute de manière répétée sur des jours spécifiques.</span><span class="sxs-lookup"><span data-stu-id="dea92-124">If **True**, a scheduled job runs repeatedly on specific days.</span></span> <span data-ttu-id="dea92-125">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="dea92-125">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="dea92-126">*DaysOfWeek* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="dea92-126">*DaysOfWeek* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dea92-127">Jours de la semaine où un travail est planifié pour s’exécuter ; utilisé uniquement lorsque le paramètre *RunRepeatedly* a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="dea92-127">Days of the week when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span> <span data-ttu-id="dea92-128">Pour planifier un travail depuis plus d’un jour de la semaine, joignez les valeurs appropriées dans un ou logique.</span><span class="sxs-lookup"><span data-stu-id="dea92-128">To schedule a job for more than one day of the week, join the appropriate values in a logical OR.</span></span> <span data-ttu-id="dea92-129">Par exemple, pour planifier un travail pour les mardis et les vendredis, la valeur de *DaysOfWeek* est 2 ou 16.</span><span class="sxs-lookup"><span data-stu-id="dea92-129">For example, to schedule a job for Tuesdays and Fridays, the value of *DaysOfWeek* are 2 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="dea92-130">**Lundi** (1)</span><span class="sxs-lookup"><span data-stu-id="dea92-130">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="dea92-131">**Mardi** (2)</span><span class="sxs-lookup"><span data-stu-id="dea92-131">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="dea92-132">**Mercredi** (4)</span><span class="sxs-lookup"><span data-stu-id="dea92-132">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="dea92-133">**Jeudi** (8)</span><span class="sxs-lookup"><span data-stu-id="dea92-133">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="dea92-134">**Vendredi** (16)</span><span class="sxs-lookup"><span data-stu-id="dea92-134">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="dea92-135">**Samedi** (32)</span><span class="sxs-lookup"><span data-stu-id="dea92-135">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="dea92-136">**Dimanche** (64)</span><span class="sxs-lookup"><span data-stu-id="dea92-136">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="dea92-137">*DaysOfMonth* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="dea92-137">*DaysOfMonth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dea92-138">Jours du mois où un travail est planifié pour s’exécuter ; utilisé uniquement lorsque le paramètre *RunRepeatedly* a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="dea92-138">Days of the month when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="dea92-139"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="dea92-139"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-140">Jour 1 d’un mois</span><span class="sxs-lookup"><span data-stu-id="dea92-140">Day 1 of a month</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="dea92-141"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="dea92-141"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-142">Jour 2 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-142">Day 2 of a month</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="dea92-143"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="dea92-143"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-144">Jour 3 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-144">Day 3 of a month</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="dea92-145"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="dea92-145"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-146">Jour 4 d’un mois</span><span class="sxs-lookup"><span data-stu-id="dea92-146">Day 4 of a month</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="dea92-147"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="dea92-147"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-148">Jour 5 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-148">Day 5 of a month</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="dea92-149"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="dea92-149"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-150">Jour 6 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-150">Day 6 of a month</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="dea92-151"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="dea92-151"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-152">Jour 7 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-152">Day 7 of a month</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="dea92-153"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="dea92-153"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-154">Jour 8 d’un mois</span><span class="sxs-lookup"><span data-stu-id="dea92-154">Day 8 of a month</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="dea92-155"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="dea92-155"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-156">Jour 9 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-156">Day 9 of a month</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="dea92-157"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="dea92-157"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-158">Jour 10 d’un mois</span><span class="sxs-lookup"><span data-stu-id="dea92-158">Day 10 of a month</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="dea92-159"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="dea92-159"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-160">Jour 11 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-160">Day 11 of a month</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="dea92-161"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="dea92-161"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-162">Jour 12 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-162">Day 12 of a month</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="dea92-163"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="dea92-163"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-164">Jour 13 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-164">Day 13 of a month</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="dea92-165"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="dea92-165"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-166">Jour 14 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-166">Day 14 of a month</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="dea92-167"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="dea92-167"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-168">Jour 15 d’un mois</span><span class="sxs-lookup"><span data-stu-id="dea92-168">Day 15 of a month</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="dea92-169"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="dea92-169"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-170">Jour 16 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-170">Day 16 of a month</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="dea92-171"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="dea92-171"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-172">Jour 17 d’un mois</span><span class="sxs-lookup"><span data-stu-id="dea92-172">Day 17 of a month</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="dea92-173"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="dea92-173"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-174">Jour 18 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-174">Day 18 of a month</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="dea92-175"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="dea92-175"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-176">Jour 19 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-176">Day 19 of a month</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="dea92-177"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="dea92-177"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-178">Jour 20 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-178">Day 20 of a month</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="dea92-179"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="dea92-179"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-180">Jour 21 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-180">Day 21 of a month</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="dea92-181"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="dea92-181"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-182">Jour 22 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-182">Day 22 of a month</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="dea92-183"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="dea92-183"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-184">Jour 23 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-184">Day 23 of a month</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="dea92-185"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="dea92-185"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-186">Jour 24 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-186">Day 24 of a month</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="dea92-187"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="dea92-187"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-188">Jour 25 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-188">Day 25 of a month</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="dea92-189"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="dea92-189"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-190">Jour 26 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-190">Day 26 of a month</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="dea92-191"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="dea92-191"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-192">Jour 27 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-192">Day 27 of a month</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="dea92-193"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="dea92-193"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-194">Jour 28 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-194">Day 28 of a month</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="dea92-195"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="dea92-195"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-196">Jour 29 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-196">Day 29 of a month</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="dea92-197"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="dea92-197"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-198">Jour 30 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-198">Day 30 of a month</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="dea92-199"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="dea92-199"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="dea92-200">Jour 31 du mois</span><span class="sxs-lookup"><span data-stu-id="dea92-200">Day 31 of a month</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dea92-201">*InteractWithDesktop* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="dea92-201">*InteractWithDesktop* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dea92-202">Si la **valeur est true**, le travail spécifié doit être interactif, ce qui signifie qu’un utilisateur peut fournir une entrée à une tâche planifiée pendant l’exécution du travail.</span><span class="sxs-lookup"><span data-stu-id="dea92-202">If **True**, the specified job should be interactive, which means that a user can give input to a scheduled job while the job is executing.</span></span> <span data-ttu-id="dea92-203">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="dea92-203">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="dea92-204">*JobID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dea92-204">*JobId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea92-205">Numéro d’identification d’un travail.</span><span class="sxs-lookup"><span data-stu-id="dea92-205">Identifier number of a job.</span></span> <span data-ttu-id="dea92-206">Ce paramètre est un handle vers une tâche planifiée sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dea92-206">This parameter is a handle to a job being scheduled on a computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea92-207">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dea92-207">Return value</span></span>

<span data-ttu-id="dea92-208">Retourne la valeur 0 (zéro) en cas de réussite et un autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="dea92-208">Returns a value of 0 (zero) when successful, and a different number to indicate an error.</span></span> <span data-ttu-id="dea92-209">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="dea92-209">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="dea92-210">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="dea92-210">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="dea92-211">**Opération réussie**</span><span class="sxs-lookup"><span data-stu-id="dea92-211">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="dea92-212">0</span><span class="sxs-lookup"><span data-stu-id="dea92-212">0</span></span>

<span data-ttu-id="dea92-213">La demande est acceptée.</span><span class="sxs-lookup"><span data-stu-id="dea92-213">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="dea92-214">**Non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="dea92-214">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="dea92-215">1</span><span class="sxs-lookup"><span data-stu-id="dea92-215">1</span></span>

<span data-ttu-id="dea92-216">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dea92-216">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dea92-217">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="dea92-217">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="dea92-218">2</span><span class="sxs-lookup"><span data-stu-id="dea92-218">2</span></span>

<span data-ttu-id="dea92-219">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dea92-219">The user does not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="dea92-220">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="dea92-220">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="dea92-221">8</span><span class="sxs-lookup"><span data-stu-id="dea92-221">8</span></span>

<span data-ttu-id="dea92-222">Processus interactif.</span><span class="sxs-lookup"><span data-stu-id="dea92-222">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="dea92-223">**Chemin d'accès introuvable**</span><span class="sxs-lookup"><span data-stu-id="dea92-223">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="dea92-224">9</span><span class="sxs-lookup"><span data-stu-id="dea92-224">9</span></span>

<span data-ttu-id="dea92-225">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="dea92-225">The directory path to the service executable file cannot be found.</span></span>

</dd> <dt>

<span data-ttu-id="dea92-226">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="dea92-226">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="dea92-227">21</span><span class="sxs-lookup"><span data-stu-id="dea92-227">21</span></span>

<span data-ttu-id="dea92-228">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="dea92-228">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="dea92-229">**Service non démarré**</span><span class="sxs-lookup"><span data-stu-id="dea92-229">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="dea92-230">22</span><span class="sxs-lookup"><span data-stu-id="dea92-230">22</span></span>

<span data-ttu-id="dea92-231">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="dea92-231">The account that this service runs under is invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="dea92-232">**Autres**</span><span class="sxs-lookup"><span data-stu-id="dea92-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="dea92-233">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="dea92-233">23 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dea92-234">Notes</span><span class="sxs-lookup"><span data-stu-id="dea92-234">Remarks</span></span>

<span data-ttu-id="dea92-235">Si votre tâche planifiée démarre un programme interactif tel que le bloc-notes, la propriété **InteractWithDeskto** doit avoir la valeur **true** ou l’écran du programme n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="dea92-235">If your scheduled job starts an interactive program such as Notepad, then the **InteractWithDeskto** property must be set to **True** or the program's screen is not visible.</span></span> <span data-ttu-id="dea92-236">Le processus apparaît toujours dans le **Gestionnaire des tâches** , même s’il n’apparaît pas à l’écran.</span><span class="sxs-lookup"><span data-stu-id="dea92-236">The process still appears in the **Task Manager** even if it does not appear on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea92-237">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dea92-237">Requirements</span></span>



| <span data-ttu-id="dea92-238">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dea92-238">Requirement</span></span> | <span data-ttu-id="dea92-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="dea92-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dea92-240">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dea92-240">Minimum supported client</span></span><br/> | <span data-ttu-id="dea92-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dea92-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dea92-242">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dea92-242">Minimum supported server</span></span><br/> | <span data-ttu-id="dea92-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dea92-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dea92-244">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dea92-244">Namespace</span></span><br/>                | <span data-ttu-id="dea92-245">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="dea92-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dea92-246">MOF</span><span class="sxs-lookup"><span data-stu-id="dea92-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dea92-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dea92-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dea92-248">DLL</span><span class="sxs-lookup"><span data-stu-id="dea92-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dea92-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dea92-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dea92-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dea92-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="dea92-251">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dea92-251">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dea92-252">**\_ScheduledJob Win32**</span><span class="sxs-lookup"><span data-stu-id="dea92-252">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

