---
description: Crée un fichier de disquette virtuelle.
ms.assetid: C7B5712C-55DD-4784-8B2E-A8DE02E4CFD8
title: Méthode CreateVirtualFloppyDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualFloppyDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 98781a4f72218ee61a4966dc76b21f7417353e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527678"
---
# <a name="createvirtualfloppydisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="20904-103">Méthode CreateVirtualFloppyDisk de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="20904-103">CreateVirtualFloppyDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="20904-104">Crée un fichier de disquette virtuelle.</span><span class="sxs-lookup"><span data-stu-id="20904-104">Creates a virtual floppy disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="20904-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20904-105">Syntax</span></span>


```mof
uint32 CreateVirtualFloppyDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="20904-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20904-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20904-107">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20904-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20904-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20904-108">Type: **string**</span></span>

<span data-ttu-id="20904-109">Chemin qualifié complet qui spécifie l’emplacement du nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="20904-109">A fully qualified path that specifies the location of the new file.</span></span>

</dd> <dt>

<span data-ttu-id="20904-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="20904-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20904-111">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="20904-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="20904-112">Référence au travail (peut avoir la **valeur null** si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="20904-112">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20904-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20904-113">Return value</span></span>

<span data-ttu-id="20904-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20904-114">Type: **uint32**</span></span>

<span data-ttu-id="20904-115">Cette méthode peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="20904-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="20904-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="20904-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="20904-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="20904-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="20904-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="20904-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="20904-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="20904-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="20904-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="20904-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="20904-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="20904-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="20904-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="20904-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="20904-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="20904-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="20904-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="20904-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="20904-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="20904-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="20904-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="20904-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="20904-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="20904-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="20904-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="20904-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="20904-129">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="20904-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="20904-130">Notes</span><span class="sxs-lookup"><span data-stu-id="20904-130">Remarks</span></span>

<span data-ttu-id="20904-131">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="20904-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="20904-132">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="20904-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="20904-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="20904-133">Examples</span></span>

<span data-ttu-id="20904-134">L’exemple C# suivant crée un fichier de disquette virtuelle.</span><span class="sxs-lookup"><span data-stu-id="20904-134">The following C# example creates a virtual floppy disk file.</span></span> <span data-ttu-id="20904-135">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="20904-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class CreateVFD
    {
        static void CreateVirtualFlopy(string vhdPath)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

            ManagementBaseObject inParams = imageService.GetMethodParameters("CreateVirtualFloppyDisk");
            inParams["Path"] = vhdPath;
            ManagementBaseObject outParams = imageService.InvokeMethod("CreateVirtualFloppyDisk", inParams, null);
            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("{0} was created successfully.", inParams["Path"]);
                }
                else
                {
                    Console.WriteLine("Unable to create {0}", inParams["Path"]);
                }
            }

            inParams.Dispose();
            outParams.Dispose();
            imageService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 1)
            {
                Console.WriteLine("Usage: CreateVFD path");
                return;
            }
            CreateVirtualFlopy(args[0]);
        }
    }
}

```



<span data-ttu-id="20904-136">L’exemple de Visual Basic Scripting Edition suivant (VBScript) crée un fichier de disquette virtuelle.</span><span class="sxs-lookup"><span data-stu-id="20904-136">The following Visual Basic Scripting Edition (VBScript) example creates a virtual floppy disk file.</span></span>


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096

const method = "CreateVirtualFloppyDisk"
Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, objArgs, vfdPath

    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("Select * from Msvm_ImageManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 1 then
       vfdPath = objArgs.Unnamed.Item(0)
    else
       WScript.Echo "usage: cscript CreateVFD.vbs VFDFilePath "
       WScript.Quit(1)
    end if

    if CreateVirtualFloppyDisk(vfdPath) then
        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "CreateVFD failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Execute CreateVirtualFloppyDisk method
'-----------------------------------------------------------------
Function CreateVirtualFloppyDisk(vfdPath)
    WriteLog Format1("Function CreateVirtualFloppyDisk({0})",  vfdPath)
    
    dim objInParam, objOutParams

    CreateVirtualFloppyDisk = false

    set objInParam = managementService.Methods_("CreateVirtualFloppyDisk").InParameters.SpawnInstance_()
    objInParam.Path = vfdPath

    set objOutParams = managementService.ExecMethod_("CreateVirtualFloppyDisk", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VHD {0} was created successfully", vfdPath)
            CreateVirtualFloppyDisk = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)
    WriteLog "Function WMIMethodStarted"
    
    dim wmiStatus
    
    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        else
            WriteLog Format2("Failed to create VFD {0} ConcreteJob with error {1}", vfdPath, wmiStatus)
        end if
   end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    WriteLog "Function WMIJobCompleted"
    dim WMIJob, jobState

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\CreateVFD.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="20904-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20904-137">Requirements</span></span>



| <span data-ttu-id="20904-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20904-138">Requirement</span></span> | <span data-ttu-id="20904-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="20904-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20904-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20904-140">Minimum supported client</span></span><br/> | <span data-ttu-id="20904-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20904-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="20904-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20904-142">Minimum supported server</span></span><br/> | <span data-ttu-id="20904-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20904-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20904-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="20904-144">Namespace</span></span><br/>                | <span data-ttu-id="20904-145">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="20904-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="20904-146">MOF</span><span class="sxs-lookup"><span data-stu-id="20904-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20904-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20904-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20904-148">DLL</span><span class="sxs-lookup"><span data-stu-id="20904-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20904-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20904-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20904-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20904-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="20904-151">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20904-151">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="20904-152">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="20904-152">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

