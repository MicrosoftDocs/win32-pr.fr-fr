---
description: Win32Shutdown &\# 8194 ; La méthode de classe WMI fournit l’ensemble complet d’options d’arrêt prises en charge par les systèmes d’exploitation Win32. Celles-ci incluent la fermeture, l’arrêt, le redémarrage et le forçage d’une déconnexion, d’un arrêt ou d’un redémarrage.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Méthode Win32Shutdown de la classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861570"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="55a87-104">Méthode Win32Shutdown de la \_ classe Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="55a87-104">Win32Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="55a87-105">La méthode de   [classe WMI](../wmisdk/retrieving-a-class.md) **Win32Shutdown** fournit l’ensemble complet d’options d’arrêt prises en charge par les systèmes d’exploitation Win32.</span><span class="sxs-lookup"><span data-stu-id="55a87-105">The **Win32Shutdown**   [WMI class](../wmisdk/retrieving-a-class.md) method provides the full set of shutdown options supported by Win32 operating systems.</span></span> <span data-ttu-id="55a87-106">Celles-ci incluent la fermeture, l’arrêt, le redémarrage et le forçage d’une déconnexion, d’un arrêt ou d’un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="55a87-106">These include logoff, shutdown, reboot, and forcing a logoff, shutdown, or reboot.</span></span>

<span data-ttu-id="55a87-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="55a87-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="55a87-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](../wmisdk/calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="55a87-108">For more information about using this method, see [Calling a Method](../wmisdk/calling-a-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="55a87-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55a87-109">Syntax</span></span>


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a><span data-ttu-id="55a87-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55a87-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a87-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="55a87-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a87-112">Jeu de balises bitmap pour arrêter l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55a87-112">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="55a87-113">Pour forcer une commande, ajoutez l’indicateur Force (4) à la valeur de la commande.</span><span class="sxs-lookup"><span data-stu-id="55a87-113">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="55a87-114">L’utilisation de force conjointement à l’arrêt ou au redémarrage sur un ordinateur distant arrête immédiatement tout (y compris WMI, COM, etc.) ou redémarre l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="55a87-114">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="55a87-115">Cela génère une valeur de retour indéterminée.</span><span class="sxs-lookup"><span data-stu-id="55a87-115">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="55a87-116">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="55a87-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="55a87-117">**Déconnecter** : déconnecte l’utilisateur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55a87-117">**Log Off** - Logs the user off the computer.</span></span> <span data-ttu-id="55a87-118">La fermeture de session arrête tous les processus associés au contexte de sécurité du processus qui a appelé la fonction EXIT, journalise l’utilisateur actuel du système et affiche la boîte de dialogue d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="55a87-118">Logging off stops all processes associated with the security context of the process that called the exit function, logs the current user off the system, and displays the logon dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="55a87-119">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="55a87-119">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="55a87-120">**Fermeture de session forcée (0 + 4)** : déconnecte immédiatement l’utilisateur de l’ordinateur et ne notifie pas les applications de la fin de l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="55a87-120">**Forced Log Off (0 + 4)** - Logs the user off the computer immediately and does not notify applications that the logon session is ending.</span></span> <span data-ttu-id="55a87-121">Cela peut entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="55a87-121">This can result in a loss of data.</span></span>

</dd> <dt>

<span data-ttu-id="55a87-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="55a87-122">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="55a87-123">**Shutdown** : arrête l’ordinateur jusqu’à un point où il est possible de le mettre hors tension.</span><span class="sxs-lookup"><span data-stu-id="55a87-123">**Shutdown** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="55a87-124">(Toutes les mémoires tampons de fichiers sont vidées sur le disque et tous les processus en cours d’exécution sont arrêtés.) Les utilisateurs voient le message, `It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="55a87-124">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message, `It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="55a87-125">Pendant l’arrêt, le système envoie un message à chaque application en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="55a87-125">During shutdown the system sends a message to each running application.</span></span> <span data-ttu-id="55a87-126">Les applications effectuent un nettoyage lors du traitement du message et retournent la valeur true pour indiquer qu’elles peuvent être arrêtées.</span><span class="sxs-lookup"><span data-stu-id="55a87-126">The applications perform any cleanup while processing the message and return True to indicate that they can be terminated.</span></span>

</dd> <dt>

<span data-ttu-id="55a87-127">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="55a87-127">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="55a87-128">**Arrêt forcé (1 + 4)** : arrête l’ordinateur jusqu’à un point où il est possible de le mettre hors tension.</span><span class="sxs-lookup"><span data-stu-id="55a87-128">**Forced Shutdown (1 + 4)** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="55a87-129">(Toutes les mémoires tampons de fichiers sont vidées sur le disque et tous les processus en cours d’exécution sont arrêtés.) Les utilisateurs voient le message,` It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="55a87-129">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message,` It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="55a87-130">Lorsque l’approche d’arrêt forcé est utilisée, tous les services, y compris WMI, sont arrêtés immédiatement.</span><span class="sxs-lookup"><span data-stu-id="55a87-130">When the forced shutdown approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="55a87-131">Pour cette raison, vous ne serez pas en mesure de recevoir une valeur de retour si vous exécutez le script sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="55a87-131">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="55a87-132">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="55a87-132">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="55a87-133">**Redémarrer** : arrête puis redémarre l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55a87-133">**Reboot** - Shuts down and then restarts the computer.</span></span>

</dd> <dt>

<span data-ttu-id="55a87-134">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="55a87-134">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="55a87-135">**Redémarrage forcé (2 + 4)** : arrête puis redémarre l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55a87-135">**Forced Reboot (2 + 4)** - Shuts down and then restarts the computer.</span></span>

<span data-ttu-id="55a87-136">Lorsque l’approche de redémarrage forcé est utilisée, tous les services, y compris WMI, sont arrêtés immédiatement.</span><span class="sxs-lookup"><span data-stu-id="55a87-136">When the forced reboot approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="55a87-137">Pour cette raison, vous ne serez pas en mesure de recevoir une valeur de retour si vous exécutez le script sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="55a87-137">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="55a87-138">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="55a87-138">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="55a87-139">**Mettre hors** tension : arrête l’ordinateur et éteint l’alimentation (si elle est prise en charge par l’ordinateur en question).</span><span class="sxs-lookup"><span data-stu-id="55a87-139">**Power Off** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

</dd> <dt>

<span data-ttu-id="55a87-140">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="55a87-140">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="55a87-141">**Mise hors tension forcée (8 + 4)** : arrête l’ordinateur et désactive l’alimentation (si elle est prise en charge par l’ordinateur en question).</span><span class="sxs-lookup"><span data-stu-id="55a87-141">**Forced Power Off (8 + 4)** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

<span data-ttu-id="55a87-142">Lorsque l’approche de mise hors tension forcée est utilisée, tous les services, y compris WMI, sont arrêtés immédiatement.</span><span class="sxs-lookup"><span data-stu-id="55a87-142">When the forced power off approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="55a87-143">Pour cette raison, vous ne serez pas en mesure de recevoir une valeur de retour si vous exécutez le script sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="55a87-143">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="55a87-144">*Réservé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55a87-144">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a87-145">Un moyen d’étendre **Win32Shutdown**.</span><span class="sxs-lookup"><span data-stu-id="55a87-145">A means to extend **Win32Shutdown**.</span></span> <span data-ttu-id="55a87-146">Actuellement, le paramètre *réservé* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="55a87-146">Currently, the *Reserved* parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a87-147">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55a87-147">Return value</span></span>

<span data-ttu-id="55a87-148">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="55a87-148">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="55a87-149">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="55a87-149">Any other number indicates an error.</span></span> <span data-ttu-id="55a87-150">Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](../wmisdk/wmi-error-constants.md) ou [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="55a87-150">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="55a87-151">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="55a87-151">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="55a87-152">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="55a87-152">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="55a87-153">**Autre** (1 à 4294967295)</span><span class="sxs-lookup"><span data-stu-id="55a87-153">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="55a87-154">Notes</span><span class="sxs-lookup"><span data-stu-id="55a87-154">Remarks</span></span>

<span data-ttu-id="55a87-155">Pour une gestion plus efficace des ordinateurs d’une organisation, les administrateurs doivent pouvoir arrêter ou redémarrer un ordinateur à distance, ou pour fermer la session à distance d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55a87-155">For more efficient management of computers in an organization, administrators need the ability to remotely shut down or restart a computer, or to remotely log off a user.</span></span> <span data-ttu-id="55a87-156">La possibilité d’effectuer ces tâches permet aux administrateurs d’installer des logiciels, de reconfigurer les paramètres de l’ordinateur, de supprimer des ordinateurs du réseau et d’effectuer d’autres tâches sans avoir à arrêter ou redémarrer manuellement chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55a87-156">The ability to carry out these tasks allows administrators to install software, reconfigure computer settings, remove computers from the network, and perform other tasks without having to manually shut down or restart each computer.</span></span>

<span data-ttu-id="55a87-157">Par exemple, pour effectuer une mise à niveau du réseau, vous devrez peut-être arrêter tous les ordinateurs qui s’exécutent sur un segment de réseau particulier.</span><span class="sxs-lookup"><span data-stu-id="55a87-157">For example, to perform a network upgrade, you might need to shut down all the computers running on a particular network segment.</span></span> <span data-ttu-id="55a87-158">Pour forcer une mise à niveau stratégie de groupe, vous devez déconnecter les utilisateurs de leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55a87-158">To force a Group Policy upgrade, you need to log users off their computers.</span></span> <span data-ttu-id="55a87-159">Si un virus informatique est présent n’importe où dans votre organisation, vous souhaiterez peut-être arrêter autant d’ordinateurs que possible, avant que le virus n’ait la possibilité de se répandre.</span><span class="sxs-lookup"><span data-stu-id="55a87-159">If a computer virus is present anywhere in your organization, you might want to shut down as many computers as possible, before the virus has an opportunity to spread.</span></span> <span data-ttu-id="55a87-160">La possibilité d’arrêter et de redémarrer les ordinateurs et de se déconnecter des utilisateurs par programmation plutôt que manuellement peut être un économiseur de temps énorme.</span><span class="sxs-lookup"><span data-stu-id="55a87-160">The ability to shut down and restart computers and to log off users programmatically instead of manually can be an enormous time-saver.</span></span>

<span data-ttu-id="55a87-161">Le processus appelant doit avoir le privilège **se \_ arrêter le \_ nom** .</span><span class="sxs-lookup"><span data-stu-id="55a87-161">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

<span data-ttu-id="55a87-162">La méthode [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) fournit le même ensemble d’options d’arrêt prises en charge par la méthode **Win32Shutdown** dans [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) , mais elle vous permet également de spécifier des commentaires, une raison d’arrêt ou un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="55a87-162">The [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) method provides the same set of shutdown options supported by the **Win32Shutdown** method in [**Win32\_OperatingSystem**](win32-operatingsystem.md) but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

<span data-ttu-id="55a87-163">La méthode Win32Shutdown n’a pas de paramètre pour verrouiller une station de travail, ce qui laisse l’utilisateur ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="55a87-163">The Win32Shutdown method does not have a parameter for locking a workstation, leaving the user logged on.</span></span> <span data-ttu-id="55a87-164">Toutefois, les stations de travail peuvent être verrouillées à partir de la ligne de commande à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="55a87-164">However, workstations can be locked from the command line by using the following command:</span></span>

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a><span data-ttu-id="55a87-165">Exemples</span><span class="sxs-lookup"><span data-stu-id="55a87-165">Examples</span></span>

<span data-ttu-id="55a87-166">L’exemple VBScript de [déconnexion, de redémarrage ou d’arrêt de plusieurs ordinateurs](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) de la Galerie TechNet utilise Win32Shutdown pour la fermeture de session, l’arrêt, le redémarrage ou la mise hors tension (selon la sélection) des ordinateurs figurant dans le groupe de serveurs.</span><span class="sxs-lookup"><span data-stu-id="55a87-166">The [Log Out, Reboot, or Shut Down Multiple Computers](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) VBScript sample on TechNet Gallery uses Win32Shutdown to log off, shut down, reboot, or power off (depending on the selection) the computers listed in the Server array.</span></span>

<span data-ttu-id="55a87-167">L’exemple [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell sur la Galerie TechNet comprend une méthode qui appelle Win32Shutdown sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="55a87-167">The [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell sample on TechNet Gallery includes a method that calls Win32Shutdown on a remote computer.</span></span>

<span data-ttu-id="55a87-168">L’exemple PowerShell suivant utilise la méthode Win32Shutdown pour arrêter l’ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="55a87-168">The following PowerShell example uses the Win32Shutdown method to shut down the specified computer.</span></span>


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



<span data-ttu-id="55a87-169">L’exemple de code PowerShell suivant utilise le EnableAllPrivileges de l’applet de commande de l’applet de commande pour obtenir les droits appropriés.</span><span class="sxs-lookup"><span data-stu-id="55a87-169">The following PowerShell code sample uses the EnableAllPrivileges from get-wmiobject cmdlet to achieve the proper priviliges.</span></span>


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



<span data-ttu-id="55a87-170">L’exemple de code VB.NET suivant utilise la méthode Shutdown pour redémarrer ou déconnecter un système.</span><span class="sxs-lookup"><span data-stu-id="55a87-170">The following VB.NET sample code uses the Shutdown method to reboot or log off a system.</span></span>


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
```



## <a name="requirements"></a><span data-ttu-id="55a87-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55a87-171">Requirements</span></span>



| <span data-ttu-id="55a87-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55a87-172">Requirement</span></span> | <span data-ttu-id="55a87-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="55a87-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55a87-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55a87-174">Minimum supported client</span></span><br/> | <span data-ttu-id="55a87-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55a87-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55a87-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55a87-176">Minimum supported server</span></span><br/> | <span data-ttu-id="55a87-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55a87-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55a87-178">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="55a87-178">Namespace</span></span><br/>                | <span data-ttu-id="55a87-179">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="55a87-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55a87-180">MOF</span><span class="sxs-lookup"><span data-stu-id="55a87-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55a87-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55a87-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55a87-182">DLL</span><span class="sxs-lookup"><span data-stu-id="55a87-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55a87-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a87-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a87-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55a87-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a87-185">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="55a87-185">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="55a87-186">**\_OperatingSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="55a87-186">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="55a87-187">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="55a87-187">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="55a87-188">Tâches WMI : gestion des postes de travail</span><span class="sxs-lookup"><span data-stu-id="55a87-188">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[<span data-ttu-id="55a87-189">Exécution d’opérations privilégiées à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="55a87-189">Executing Privileged Operations Using VBScript</span></span>](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
