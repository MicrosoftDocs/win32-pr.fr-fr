---
description: Arrêt&\# 8194 ; La méthode de classe WMI décharge les programmes et les dll jusqu’à ce qu’il soit possible de mettre l’ordinateur hors connexion.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Méthode Shutdown de la classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af80442087a0498849388f0da10946b08e282712
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483968"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="30d45-103">Méthode Shutdown de la \_ classe Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="30d45-103">Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="30d45-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Shutdown** décharge les programmes et les dll jusqu’à ce qu’il soit possible de mettre l’ordinateur hors connexion.</span><span class="sxs-lookup"><span data-stu-id="30d45-104">The **Shutdown** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method unloads programs and DLLs until it is safe to turn off the computer.</span></span>

<span data-ttu-id="30d45-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="30d45-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="30d45-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="30d45-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="30d45-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30d45-107">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="30d45-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30d45-108">Parameters</span></span>

<span data-ttu-id="30d45-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="30d45-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30d45-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30d45-110">Return value</span></span>

<span data-ttu-id="30d45-111">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="30d45-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="30d45-112">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="30d45-112">Any other number indicates an error.</span></span> <span data-ttu-id="30d45-113">Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="30d45-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="30d45-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="30d45-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="30d45-115">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="30d45-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="30d45-116">**Autre** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="30d45-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="30d45-117">Notes</span><span class="sxs-lookup"><span data-stu-id="30d45-117">Remarks</span></span>

<span data-ttu-id="30d45-118">Les ordinateurs doivent parfois être supprimés du réseau, peut-être pour des raisons de maintenance planifiée, car l’ordinateur ne fonctionne pas correctement ou pour effectuer un processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="30d45-118">Computers occasionally need to be removed from the network, perhaps for scheduled maintenance, because the computer is not functioning correctly, or to complete a configuration process.</span></span> <span data-ttu-id="30d45-119">Par exemple, si un serveur DHCP remet des adresses IP erronées, vous pouvez arrêter l’ordinateur jusqu’à ce qu’un technicien de service puisse être distribué pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="30d45-119">For example, if a DHCP server is handing out erroneous IP addresses, you might want to shut the computer down until a service technician can be dispatched to fix the problem.</span></span> <span data-ttu-id="30d45-120">Si vous pensez qu’une violation de la sécurité s’est produite, vous devrez peut-être arrêter certains serveurs pour vous assurer qu’ils ne sont pas accessibles tant que le problème de sécurité n’a pas été résolu.</span><span class="sxs-lookup"><span data-stu-id="30d45-120">If you suspect that a security breach has occurred, you might need to shut down certain servers to ensure that they cannot be accessed until the security issue has been resolved.</span></span> <span data-ttu-id="30d45-121">Certaines opérations de configuration (telles que la modification d’un nom d’ordinateur) nécessitent le redémarrage de l’ordinateur pour que la modification prenne effet.</span><span class="sxs-lookup"><span data-stu-id="30d45-121">Some configuration operations (such as changing a computer name) require you to restart the computer before the change takes effect.</span></span>

<span data-ttu-id="30d45-122">Cette méthode arrête immédiatement l’ordinateur, si possible.</span><span class="sxs-lookup"><span data-stu-id="30d45-122">This method immediately shuts the computer down, if possible.</span></span> <span data-ttu-id="30d45-123">Le système arrête tous les processus en cours d’exécution, vide toutes les mémoires tampons de fichiers sur le disque, puis met le système sous tension.</span><span class="sxs-lookup"><span data-stu-id="30d45-123">The system stops all running processes, flushes all file buffers to the disk, and then powers down the system.</span></span> <span data-ttu-id="30d45-124">Le processus appelant doit avoir le privilège **se \_ arrêter le \_ nom** , comme décrit dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="30d45-124">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege, as described in the following example.</span></span>


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



<span data-ttu-id="30d45-125">Pour plus d’informations sur la définition d’un privilège, consultez [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations) et [exécution d’opérations privilégiées à l’aide de VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="30d45-125">For more information on setting a privilege, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations) and [Executing Privileged Operations Using VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span></span> <span data-ttu-id="30d45-126">Pour obtenir des options d’arrêt supplémentaires, telles qu’une fermeture de session ou un arrêt forcé, consultez la méthode [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="30d45-126">For additional shutdown options, such as a logoff or a forced shutdown, see the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="30d45-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="30d45-127">Examples</span></span>

<span data-ttu-id="30d45-128">Le code VBScript suivant arrête l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="30d45-128">The following VBScript code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="30d45-129">Vous devez disposer du privilège d’arrêt pour appeler correctement la méthode Shutdown.</span><span class="sxs-lookup"><span data-stu-id="30d45-129">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



<span data-ttu-id="30d45-130">Le code perl suivant arrête l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="30d45-130">The following Perl code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="30d45-131">Vous devez disposer du privilège d’arrêt pour appeler correctement la méthode Shutdown.</span><span class="sxs-lookup"><span data-stu-id="30d45-131">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
  if (!defined $RetVal || $RetVal != 0)
  { 
   print Win32::OLE->LastError, "\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="30d45-132">Le code VBScript suivant arrête l’ordinateur distant spécifié.</span><span class="sxs-lookup"><span data-stu-id="30d45-132">The following VBScript code shuts the specified remote computer down.</span></span> <span data-ttu-id="30d45-133">Renseignez *\_ \_ nom du système distant* avec le nom du système distant à arrêter.</span><span class="sxs-lookup"><span data-stu-id="30d45-133">Fill in *REMOTE\_SYSTEM\_NAME* with the name of the remote system to shutdown.</span></span>

> [!Note]  
> <span data-ttu-id="30d45-134">Vous devez disposer du privilège RemoteShutdown pour appeler correctement la méthode **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="30d45-134">You must have the RemoteShutdown privilege to successfully invoke the **Shutdown** method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



## <a name="requirements"></a><span data-ttu-id="30d45-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30d45-135">Requirements</span></span>



| <span data-ttu-id="30d45-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30d45-136">Requirement</span></span> | <span data-ttu-id="30d45-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="30d45-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30d45-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30d45-138">Minimum supported client</span></span><br/> | <span data-ttu-id="30d45-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30d45-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30d45-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30d45-140">Minimum supported server</span></span><br/> | <span data-ttu-id="30d45-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30d45-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30d45-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="30d45-142">Namespace</span></span><br/>                | <span data-ttu-id="30d45-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="30d45-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="30d45-144">MOF</span><span class="sxs-lookup"><span data-stu-id="30d45-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30d45-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30d45-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="30d45-146">DLL</span><span class="sxs-lookup"><span data-stu-id="30d45-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30d45-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30d45-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30d45-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30d45-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="30d45-149">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="30d45-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="30d45-150">**\_OperatingSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="30d45-150">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="30d45-151">Tâches WMI : gestion des postes de travail</span><span class="sxs-lookup"><span data-stu-id="30d45-151">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[<span data-ttu-id="30d45-152">Exécution d’opérations privilégiées à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="30d45-152">Executing Privileged Operations Using VBScript</span></span>](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

