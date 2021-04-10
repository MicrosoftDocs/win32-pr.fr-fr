---
description: Le redémarrage&\# 8194 ; La méthode de classe WMI arrête le système informatique, puis le redémarre.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Méthode reboot de la classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950775"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="f2b3d-103">Méthode reboot de la \_ classe Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f2b3d-103">Reboot method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="f2b3d-104">La méthode de **redémarrage** de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) arrête le système informatique, puis le redémarre.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-104">The **Reboot** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method shuts down the computer system, then restarts it.</span></span>

<span data-ttu-id="f2b3d-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f2b3d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f2b3d-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f2b3d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b3d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2b3d-107">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="f2b3d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2b3d-108">Parameters</span></span>

<span data-ttu-id="f2b3d-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2b3d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2b3d-110">Return value</span></span>

<span data-ttu-id="f2b3d-111">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="f2b3d-112">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-112">Any other number indicates an error.</span></span> <span data-ttu-id="f2b3d-113">Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f2b3d-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f2b3d-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f2b3d-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f2b3d-115">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="f2b3d-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f2b3d-116">**Autre** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="f2b3d-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f2b3d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f2b3d-117">Remarks</span></span>

<span data-ttu-id="f2b3d-118">La possibilité de redémarrer un ordinateur par programme permet aux administrateurs d’effectuer de nombreuses tâches de gestion d’ordinateur à distance.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-118">The ability to programmatically restart a computer allows administrators to perform many computer management tasks remotely.</span></span>

<span data-ttu-id="f2b3d-119">Par exemple, si vous créez un script pour installer un logiciel ou apporter une modification de configuration qui nécessite le redémarrage d’un ordinateur, vous pouvez inclure la commande de redémarrage dans le script et effectuer la totalité de l’opération à distance.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-119">For example, if you create a script to install software or make a configuration change that requires restarting a computer, you can include the restart command in the script and perform the entire operation remotely.</span></span> <span data-ttu-id="f2b3d-120">La méthode **reboot** peut être utilisée pour redémarrer un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-120">The **Reboot** method can be used to restart a computer.</span></span> <span data-ttu-id="f2b3d-121">À l’instar de la méthode [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) , la méthode **reboot** exige que l’utilisateur utilise les informations d’identification de sécurité utilisées par le script pour posséder le privilège Shutdown.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-121">Like the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method, the **Reboot** method requires the user whose security credentials are being used by the script to possess the Shutdown privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="f2b3d-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="f2b3d-122">Examples</span></span>

<span data-ttu-id="f2b3d-123">L’exemple de code VBScript suivant appelle la méthode reboot de la classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="f2b3d-123">The following VBScript code sample invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="f2b3d-124">Vous devez disposer du privilège d’arrêt pour appeler correctement la méthode Shutdown.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-124">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="f2b3d-125">Le code perl suivant appelle la méthode reboot de la classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="f2b3d-125">The following Perl code invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="f2b3d-126">Vous devez disposer du privilège d’arrêt pour appeler correctement la méthode Shutdown.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-126">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
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



<span data-ttu-id="f2b3d-127">Le code VBScript suivant appelle la méthode reboot de la classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) sur un système distant.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-127">The following VBScript invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="f2b3d-128">Renseignez \_ nom du système distant \_ avec le nom du système distant à redémarrer.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-128">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="f2b3d-129">Vous devez disposer du privilège RemoteShutdown pour appeler correctement la méthode reboot</span><span class="sxs-lookup"><span data-stu-id="f2b3d-129">You must have the RemoteShutdown privilege to successfully invoke the Reboot method</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="f2b3d-130">l’exemple suivant perl appelle la méthode reboot de la classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) sur un système distant.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-130">he following Perl invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="f2b3d-131">Renseignez \_ nom du système distant \_ avec le nom du système distant à redémarrer.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-131">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="f2b3d-132">Vous devez disposer du privilège RemoteShutdown pour appeler correctement la méthode reboot.</span><span class="sxs-lookup"><span data-stu-id="f2b3d-132">You must have the RemoteShutdown privilege to successfully invoke the Reboot method.</span></span>

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



## <a name="requirements"></a><span data-ttu-id="f2b3d-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2b3d-133">Requirements</span></span>



| <span data-ttu-id="f2b3d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2b3d-134">Requirement</span></span> | <span data-ttu-id="f2b3d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2b3d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b3d-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2b3d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b3d-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2b3d-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2b3d-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2b3d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b3d-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2b3d-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2b3d-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f2b3d-140">Namespace</span></span><br/>                | <span data-ttu-id="f2b3d-141">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f2b3d-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f2b3d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f2b3d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2b3d-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2b3d-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2b3d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f2b3d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2b3d-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2b3d-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b3d-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2b3d-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2b3d-147">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2b3d-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f2b3d-148">**\_OperatingSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="f2b3d-148">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="f2b3d-149">**\_Méthode CIM OperatingSystem. Shutdown**</span><span class="sxs-lookup"><span data-stu-id="f2b3d-149">**CIM\_OperatingSystem.Shutdown method**</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="f2b3d-150">Tâches WMI : gestion des postes de travail</span><span class="sxs-lookup"><span data-stu-id="f2b3d-150">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

