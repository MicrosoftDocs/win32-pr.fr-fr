---
description: La méthode Win32ShutdownTracker fournit le même ensemble d’options d’arrêt prises en charge par la méthode Win32Shutdown dans Win32 \_ OperatingSystem, mais elle vous permet également de spécifier des commentaires, une raison d’arrêt ou un délai d’attente.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Méthode Win32ShutdownTracker de la classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110215"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="be9f4-103">Méthode Win32ShutdownTracker de la \_ classe Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="be9f4-103">Win32ShutdownTracker method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="be9f4-104">La méthode **Win32ShutdownTracker** fournit le même ensemble d’options d’arrêt prises en charge par la méthode [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) dans [**Win32 \_ OperatingSystem**](win32-operatingsystem.md), mais elle vous permet également de spécifier des commentaires, une raison d’arrêt ou un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="be9f4-104">The **Win32ShutdownTracker** method provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in [**Win32\_OperatingSystem**](win32-operatingsystem.md), but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9f4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be9f4-105">Syntax</span></span>


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="be9f4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be9f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be9f4-107">*Délai d’expiration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be9f4-107">*Timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-108">Durée, en secondes, avant l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="be9f4-108">Time, in seconds, before shutdown takes place.</span></span> <span data-ttu-id="be9f4-109">La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="be9f4-109">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="be9f4-110">*Commentaire* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be9f4-110">*Comment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-111">Message à afficher dans la boîte de dialogue d’arrêt, également stocké sous forme de commentaire dans l’entrée du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="be9f4-111">Message to display in the shutdown dialog box that is also stored as a comment in the event log entry.</span></span>

</dd> <dt>

<span data-ttu-id="be9f4-112">*ReasonCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be9f4-112">*ReasonCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-113">Raison du lancement de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="be9f4-113">Reason for initiating the shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="be9f4-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="be9f4-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-115">Jeu de balises bitmap pour arrêter l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="be9f4-115">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="be9f4-116">Pour forcer une commande, ajoutez l’indicateur Force (4) à la valeur de la commande.</span><span class="sxs-lookup"><span data-stu-id="be9f4-116">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="be9f4-117">L’utilisation de force conjointement à l’arrêt ou au redémarrage sur un ordinateur distant arrête immédiatement tout (y compris WMI, COM, etc.) ou redémarre l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="be9f4-117">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="be9f4-118">Cela génère une valeur de retour indéterminée.</span><span class="sxs-lookup"><span data-stu-id="be9f4-118">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="be9f4-119">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="be9f4-119">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-120">Fermer la session</span><span class="sxs-lookup"><span data-stu-id="be9f4-120">Log Off</span></span>

</dd> <dt>

<span data-ttu-id="be9f4-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="be9f4-121">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-122">Désactivation de la journalisation forcée (0 + 4)</span><span class="sxs-lookup"><span data-stu-id="be9f4-122">Forced Log Off (0 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="be9f4-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="be9f4-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-124">Éteindre</span><span class="sxs-lookup"><span data-stu-id="be9f4-124">Shutdown</span></span>

</dd> <dt>

<span data-ttu-id="be9f4-125">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="be9f4-125">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-126">Arrêt forcé (1 + 4)</span><span class="sxs-lookup"><span data-stu-id="be9f4-126">Forced Shutdown (1 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="be9f4-127">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="be9f4-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-128">Reboot</span><span class="sxs-lookup"><span data-stu-id="be9f4-128">Reboot</span></span>

</dd> <dt>

<span data-ttu-id="be9f4-129">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="be9f4-129">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-130">Redémarrage forcé (2 + 4)</span><span class="sxs-lookup"><span data-stu-id="be9f4-130">Forced Reboot (2 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="be9f4-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="be9f4-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-132">Mise hors tension</span><span class="sxs-lookup"><span data-stu-id="be9f4-132">Power Off</span></span>

</dd> <dt>

<span data-ttu-id="be9f4-133">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="be9f4-133">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="be9f4-134">Mise hors tension forcée (8 + 4)</span><span class="sxs-lookup"><span data-stu-id="be9f4-134">Forced Power Off (8 + 4)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be9f4-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be9f4-135">Return value</span></span>

<span data-ttu-id="be9f4-136">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="be9f4-136">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="be9f4-137">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="be9f4-137">Any other number indicates an error.</span></span> <span data-ttu-id="be9f4-138">Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](../wmisdk/wmi-error-constants.md) ou [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="be9f4-138">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="be9f4-139">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="be9f4-139">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="be9f4-140">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="be9f4-140">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be9f4-141">**Autre** (1 à 4294967295)</span><span class="sxs-lookup"><span data-stu-id="be9f4-141">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="be9f4-142">Notes</span><span class="sxs-lookup"><span data-stu-id="be9f4-142">Remarks</span></span>

<span data-ttu-id="be9f4-143">Le processus appelant doit avoir le privilège **se \_ arrêter le \_ nom** .</span><span class="sxs-lookup"><span data-stu-id="be9f4-143">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="be9f4-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="be9f4-144">Examples</span></span>

<span data-ttu-id="be9f4-145">L’exemple de code VBScript suivant décrit comment appeler **Win32ShutdownTracker**.</span><span class="sxs-lookup"><span data-stu-id="be9f4-145">The following VBScript code sample describes how to call **Win32ShutdownTracker**.</span></span>


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
Next
```



## <a name="requirements"></a><span data-ttu-id="be9f4-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be9f4-146">Requirements</span></span>



| <span data-ttu-id="be9f4-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be9f4-147">Requirement</span></span> | <span data-ttu-id="be9f4-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="be9f4-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be9f4-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be9f4-149">Minimum supported client</span></span><br/> | <span data-ttu-id="be9f4-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be9f4-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be9f4-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be9f4-151">Minimum supported server</span></span><br/> | <span data-ttu-id="be9f4-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be9f4-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be9f4-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="be9f4-153">Namespace</span></span><br/>                | <span data-ttu-id="be9f4-154">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="be9f4-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be9f4-155">MOF</span><span class="sxs-lookup"><span data-stu-id="be9f4-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be9f4-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be9f4-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be9f4-157">DLL</span><span class="sxs-lookup"><span data-stu-id="be9f4-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be9f4-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be9f4-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9f4-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be9f4-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9f4-160">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="be9f4-160">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="be9f4-161">**\_OperatingSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="be9f4-161">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="be9f4-162">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="be9f4-162">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
