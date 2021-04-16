---
description: SetPriority&\# 32 ; La méthode de classe WMI tente de modifier la priorité d’exécution du processus.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Méthode SetPriority de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf08057ec075448d9912e37c33b6087c381f97d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524143"
---
# <a name="setpriority-method-of-the-win32_process-class"></a><span data-ttu-id="f446b-103">Méthode SetPriority de la \_ classe Process Win32</span><span class="sxs-lookup"><span data-stu-id="f446b-103">SetPriority method of the Win32\_Process class</span></span>

<span data-ttu-id="f446b-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPriority** tente de modifier la priorité d’exécution du processus.</span><span class="sxs-lookup"><span data-stu-id="f446b-104">The **SetPriority** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to change the execution priority of the process.</span></span>

<span data-ttu-id="f446b-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f446b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f446b-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f446b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f446b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f446b-107">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="f446b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f446b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f446b-109">*Priorité* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f446b-109">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f446b-110">Nouvelle classe de priorité pour le processus.</span><span class="sxs-lookup"><span data-stu-id="f446b-110">New priority class for the process.</span></span> <span data-ttu-id="f446b-111">Notez que ces valeurs sont différentes de celles explicitement indiquées dans la propriété **Priority** du [**\_ processus Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="f446b-111">Note that these values are different than those explicitly stated in the **Priority** property of [**Win32\_Process**](win32-process.md).</span></span>

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="f446b-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactif** (64)</span><span class="sxs-lookup"><span data-stu-id="f446b-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="f446b-113">Spécifié pour un processus avec des threads qui s’exécutent uniquement lorsque le système est inactif.</span><span class="sxs-lookup"><span data-stu-id="f446b-113">Specified for a process with threads that run only when the system is idle.</span></span> <span data-ttu-id="f446b-114">Les threads du processus sont reportés par les threads d’un processus qui s’exécutent dans une classe de priorité plus élevée, par exemple un économiseur d’écran.</span><span class="sxs-lookup"><span data-stu-id="f446b-114">The threads of the process are preempted by the threads of a process that run in a higher priority class, for example, a screen saver.</span></span> <span data-ttu-id="f446b-115">La classe idle-priority est héritée par les processus enfants.</span><span class="sxs-lookup"><span data-stu-id="f446b-115">The idle-priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="f446b-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Inférieure** à la normale (16384)</span><span class="sxs-lookup"><span data-stu-id="f446b-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="f446b-117">Indique un processus qui a une priorité supérieure à la **\_ \_ classe de priorité inactive**, mais qui se trouve en dessous de la **\_ \_ classe de priorité normale**.</span><span class="sxs-lookup"><span data-stu-id="f446b-117">Indicates a process that has priority above **IDLE\_PRIORITY\_CLASS**, but below **NORMAL\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="f446b-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span><span class="sxs-lookup"><span data-stu-id="f446b-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="f446b-119">Spécifié pour un processus sans besoins de planification spéciaux.</span><span class="sxs-lookup"><span data-stu-id="f446b-119">Specified for a process with no special scheduling needs.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="f446b-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Au-dessus** de la normale (32768)</span><span class="sxs-lookup"><span data-stu-id="f446b-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="f446b-121">Indique un processus qui a une priorité supérieure à la **\_ \_ classe de priorité normale**, mais qui se trouve en dessous de la **\_ \_ classe de priorité élevée**.</span><span class="sxs-lookup"><span data-stu-id="f446b-121">Indicates a process that has priority above **NORMAL\_PRIORITY\_CLASS**, but below **HIGH\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span data-ttu-id="f446b-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Haute priorité** (128)</span><span class="sxs-lookup"><span data-stu-id="f446b-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**High Priority** (128)</span></span>


</dt> <dd>

<span data-ttu-id="f446b-123">Spécifié pour un processus qui exécute des tâches critiques à l’heure qui doivent être exécutées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f446b-123">Specified for a process that performs time-critical tasks that must be executed immediately.</span></span> <span data-ttu-id="f446b-124">Les threads du processus prévalent sur les threads de processus de classe de priorités normale ou inactive.</span><span class="sxs-lookup"><span data-stu-id="f446b-124">The threads of the process preempt the threads of normal or idle priority class processes.</span></span> <span data-ttu-id="f446b-125">Par exemple, la Liste des tâches, qui doit répondre rapidement lorsqu’elle est appelée par l’utilisateur, quelle que soit la charge sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f446b-125">An example is the Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="f446b-126">Soyez extrêmement vigilant lorsque vous utilisez la classe de priorité élevée, car une application de classe de priorité élevée peut utiliser presque tout le temps processeur disponible.</span><span class="sxs-lookup"><span data-stu-id="f446b-126">Use extreme care when using the high-priority class, because a high-priority class application can use nearly all of the available CPU time.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="f446b-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Temps réel** (256)</span><span class="sxs-lookup"><span data-stu-id="f446b-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="f446b-128">Spécifié pour un processus qui a la priorité la plus élevée possible.</span><span class="sxs-lookup"><span data-stu-id="f446b-128">Specified for a process that has the highest possible priority.</span></span> <span data-ttu-id="f446b-129">Les threads du processus devancent les threads de tous les autres processus, y compris les processus du système d’exploitation qui effectuent des tâches importantes.</span><span class="sxs-lookup"><span data-stu-id="f446b-129">The threads of the process preempt the threads of all of the other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="f446b-130">Par exemple, un processus en temps réel qui s’exécute depuis plus d’un intervalle très court peut empêcher le vidage du cache disque ou la non-réponse d’une souris.</span><span class="sxs-lookup"><span data-stu-id="f446b-130">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush or a mouse to be unresponsive.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f446b-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f446b-131">Return value</span></span>

<span data-ttu-id="f446b-132">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="f446b-132">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="f446b-133">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f446b-133">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f446b-134">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f446b-134">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f446b-135">**Achèvement réussi** (0)</span><span class="sxs-lookup"><span data-stu-id="f446b-135">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f446b-136">**Accès refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="f446b-136">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f446b-137">**Privilèges insuffisants** (3)</span><span class="sxs-lookup"><span data-stu-id="f446b-137">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f446b-138">**Échec inconnu** (8)</span><span class="sxs-lookup"><span data-stu-id="f446b-138">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f446b-139">**Chemin introuvable** (9)</span><span class="sxs-lookup"><span data-stu-id="f446b-139">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f446b-140">**Paramètre non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="f446b-140">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="f446b-141">**Autre** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="f446b-141">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f446b-142">Notes</span><span class="sxs-lookup"><span data-stu-id="f446b-142">Remarks</span></span>

<span data-ttu-id="f446b-143">Pour définir la priorité en temps réel, l’appelant doit disposer de **SeIncreaseBasePriorityPrivilege** (privilège de priorité de **base de se \_ \_ \_ \_ Inc**).</span><span class="sxs-lookup"><span data-stu-id="f446b-143">To set the priority to Realtime, the caller must have **SeIncreaseBasePriorityPrivilege** (**SE\_INC\_BASE\_PRIORITY\_PRIVILEGE**).</span></span> <span data-ttu-id="f446b-144">Sans ce privilège, la priorité la plus élevée peut être définie sur la priorité haute.</span><span class="sxs-lookup"><span data-stu-id="f446b-144">Without this privilege, the highest the priority can be set to is High Priority.</span></span>

## <a name="examples"></a><span data-ttu-id="f446b-145">Exemples</span><span class="sxs-lookup"><span data-stu-id="f446b-145">Examples</span></span>

<span data-ttu-id="f446b-146">L’exemple de [modification de la priorité d’un processus en cours d’exécution](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript modifie la priorité d’une instance en cours d’exécution de Notepad.exe de la normale à au-dessus de la normale.</span><span class="sxs-lookup"><span data-stu-id="f446b-146">The [Modify the Priority Of a Running Process](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript sample changes the priority of a running instance of Notepad.exe from Normal to Above Normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="f446b-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f446b-147">Requirements</span></span>



| <span data-ttu-id="f446b-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f446b-148">Requirement</span></span> | <span data-ttu-id="f446b-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="f446b-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f446b-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f446b-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f446b-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f446b-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f446b-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f446b-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f446b-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f446b-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f446b-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f446b-154">Namespace</span></span><br/>                | <span data-ttu-id="f446b-155">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f446b-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f446b-156">MOF</span><span class="sxs-lookup"><span data-stu-id="f446b-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f446b-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f446b-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f446b-158">DLL</span><span class="sxs-lookup"><span data-stu-id="f446b-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f446b-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f446b-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f446b-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f446b-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="f446b-161">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f446b-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f446b-162">**\_Processus Win32**</span><span class="sxs-lookup"><span data-stu-id="f446b-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

