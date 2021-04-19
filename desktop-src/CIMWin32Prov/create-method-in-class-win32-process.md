---
description: Création&\# 8194 ; La méthode de classe WMI crée un processus.
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42c675f61fc8b42790aeb811ec275554b355a392
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515355"
---
# <a name="create-method-of-the-win32_process-class"></a><span data-ttu-id="2d72d-103">Créer une méthode de la \_ classe de processus Win32</span><span class="sxs-lookup"><span data-stu-id="2d72d-103">Create method of the Win32\_Process class</span></span>

<span data-ttu-id="2d72d-104">La méthode **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) crée un nouveau processus.</span><span class="sxs-lookup"><span data-stu-id="2d72d-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new process.</span></span>

<span data-ttu-id="2d72d-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2d72d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2d72d-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2d72d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d72d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d72d-107">Syntax</span></span>


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a><span data-ttu-id="2d72d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d72d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d72d-109">*Ligne* \[ de commande dans\]</span><span class="sxs-lookup"><span data-stu-id="2d72d-109">*CommandLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d72d-110">Ligne de commande à exécuter.</span><span class="sxs-lookup"><span data-stu-id="2d72d-110">Command line to execute.</span></span> <span data-ttu-id="2d72d-111">Le système ajoute un caractère null à la ligne de commande, en ajustant la chaîne si nécessaire, pour indiquer quel fichier a été réellement utilisé.</span><span class="sxs-lookup"><span data-stu-id="2d72d-111">The system adds a null character to the command line, trimming the string if necessary, to indicate which file was actually used.</span></span>

</dd> <dt>

<span data-ttu-id="2d72d-112">*CurrentDirectory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d72d-112">*CurrentDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d72d-113">Lecteur et répertoire actifs pour le processus enfant.</span><span class="sxs-lookup"><span data-stu-id="2d72d-113">Current drive and directory for the child process.</span></span> <span data-ttu-id="2d72d-114">La chaîne requiert que le répertoire en cours soit résolu en chemin connu.</span><span class="sxs-lookup"><span data-stu-id="2d72d-114">The string requires that the current directory resolves to a known path.</span></span> <span data-ttu-id="2d72d-115">Un utilisateur peut spécifier un chemin d’accès absolu ou un chemin d’accès relatif au répertoire de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="2d72d-115">A user can specify an absolute path or a path relative to the current working directory.</span></span> <span data-ttu-id="2d72d-116">Si ce paramètre a la **valeur null**, le nouveau processus aura le même chemin d’accès que le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="2d72d-116">If this parameter is **NULL**, the new process will have the same path as the calling process.</span></span> <span data-ttu-id="2d72d-117">Cette option est fournie principalement pour les interpréteurs de commande qui doivent démarrer une application et spécifier le lecteur initial et le répertoire de travail de l’application.</span><span class="sxs-lookup"><span data-stu-id="2d72d-117">This option is provided primarily for shells that must start an application and specify the application's initial drive and working directory.</span></span>

</dd> <dt>

<span data-ttu-id="2d72d-118">*ProcessStartupInformation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d72d-118">*ProcessStartupInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d72d-119">Configuration de démarrage d’un processus Windows.</span><span class="sxs-lookup"><span data-stu-id="2d72d-119">The startup configuration of a Windows process.</span></span> <span data-ttu-id="2d72d-120">Pour plus d’informations, consultez [**Win32 \_ ProcessStartup**](win32-processstartup.md).</span><span class="sxs-lookup"><span data-stu-id="2d72d-120">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d72d-121">*ProcessID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2d72d-121">*ProcessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d72d-122">Identificateur de processus global qui peut être utilisé pour identifier un processus.</span><span class="sxs-lookup"><span data-stu-id="2d72d-122">Global process identifier that can be used to identify a process.</span></span> <span data-ttu-id="2d72d-123">La valeur est valide à partir du moment où le processus est créé jusqu’au moment où le processus est terminé.</span><span class="sxs-lookup"><span data-stu-id="2d72d-123">The value is valid from the time the process is created until the time the process is terminated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d72d-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d72d-124">Return value</span></span>

<span data-ttu-id="2d72d-125">Retourne la valeur 0 (zéro) si le processus a été créé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="2d72d-125">Returns a value of 0 (zero) if the process was successfully created, and any other number to indicate an error.</span></span> <span data-ttu-id="2d72d-126">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2d72d-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2d72d-127">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2d72d-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2d72d-128">**Achèvement réussi** (0)</span><span class="sxs-lookup"><span data-stu-id="2d72d-128">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2d72d-129">**Accès refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="2d72d-129">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2d72d-130">**Privilèges insuffisants** (3)</span><span class="sxs-lookup"><span data-stu-id="2d72d-130">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2d72d-131">**Échec inconnu** (8)</span><span class="sxs-lookup"><span data-stu-id="2d72d-131">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2d72d-132">**Chemin introuvable** (9)</span><span class="sxs-lookup"><span data-stu-id="2d72d-132">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2d72d-133">**Paramètre non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="2d72d-133">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="2d72d-134">**Autre** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="2d72d-134">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2d72d-135">Notes</span><span class="sxs-lookup"><span data-stu-id="2d72d-135">Remarks</span></span>

<span data-ttu-id="2d72d-136">Vous pouvez créer une instance de la classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) pour configurer le processus avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2d72d-136">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process before calling this method.</span></span>

<span data-ttu-id="2d72d-137">Un chemin d’accès qualifié complet doit être spécifié dans les cas où le programme à lancer n’est pas dans le chemin de recherche de Winmgmt.exe.</span><span class="sxs-lookup"><span data-stu-id="2d72d-137">A fully qualified path must be specified in cases where the program to be launched is not in the search path of Winmgmt.exe.</span></span> <span data-ttu-id="2d72d-138">Si le processus nouvellement créé tente d’interagir avec des objets sur le système cible sans les privilèges d’accès appropriés, il est arrêté sans notification à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2d72d-138">If the newly created process attempts to interact with objects on the target system without the appropriate access privileges, it is terminated without notification to this method.</span></span>

<span data-ttu-id="2d72d-139">Pour des raisons de sécurité, la méthode **Win32 \_ Process. Create** ne peut pas être utilisée pour démarrer un processus interactif à distance.</span><span class="sxs-lookup"><span data-stu-id="2d72d-139">For security reasons the **Win32\_Process.Create** method cannot be used to start an interactive process remotely.</span></span>

<span data-ttu-id="2d72d-140">Les processus créés avec la méthode **Win32 \_ Process. Create** sont limités par l’objet de traitement, à moins que l’indicateur **Create \_ dissociation \_ from \_ Job** soit spécifié.</span><span class="sxs-lookup"><span data-stu-id="2d72d-140">Processes created with the **Win32\_Process.Create** method are limited by the job object unless the **CREATE\_BREAKAWAY\_FROM\_JOB** flag is specified.</span></span> <span data-ttu-id="2d72d-141">Pour plus d’informations, consultez [**Win32 \_ ProcessStartup**](win32-processstartup.md) et [**\_ \_ ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span><span class="sxs-lookup"><span data-stu-id="2d72d-141">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md) and [**\_\_ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span></span>

## <a name="examples"></a><span data-ttu-id="2d72d-142">Exemples</span><span class="sxs-lookup"><span data-stu-id="2d72d-142">Examples</span></span>

<span data-ttu-id="2d72d-143">L’exemple VBScript suivant montre comment appeler une méthode CIM comme s’il s’agissait d’une méthode Automation de SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="2d72d-143">The following VBScript example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



<span data-ttu-id="2d72d-144">L’exemple perl suivant montre comment appeler une méthode CIM comme s’il s’agissait d’une méthode Automation de SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="2d72d-144">The following Perl example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="2d72d-145">L’exemple de code VBScript suivant crée un processus Notepad sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2d72d-145">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="2d72d-146">[**Win32 \_ ProcessStartup**](win32-processstartup.md) est utilisé pour configurer les paramètres de processus.</span><span class="sxs-lookup"><span data-stu-id="2d72d-146">[**Win32\_ProcessStartup**](win32-processstartup.md) is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="2d72d-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d72d-147">Requirements</span></span>



| <span data-ttu-id="2d72d-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d72d-148">Requirement</span></span> | <span data-ttu-id="2d72d-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d72d-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d72d-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d72d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="2d72d-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d72d-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d72d-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d72d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="2d72d-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d72d-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d72d-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d72d-154">Namespace</span></span><br/>                | <span data-ttu-id="2d72d-155">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2d72d-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2d72d-156">MOF</span><span class="sxs-lookup"><span data-stu-id="2d72d-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d72d-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d72d-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d72d-158">DLL</span><span class="sxs-lookup"><span data-stu-id="2d72d-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d72d-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d72d-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d72d-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d72d-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d72d-161">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2d72d-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2d72d-162">**\_Processus Win32**</span><span class="sxs-lookup"><span data-stu-id="2d72d-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="2d72d-163">Tâches WMI : processus</span><span class="sxs-lookup"><span data-stu-id="2d72d-163">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

