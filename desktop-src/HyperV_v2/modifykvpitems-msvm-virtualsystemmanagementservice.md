---
description: Modifie des paires clé-valeur existantes sur un ordinateur virtuel.
ms.assetid: A014F681-4429-4982-95AA-DF371925BB3B
title: Méthode ModifyKvpItems de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6269e1a7794b6f04de606d13c90ef8dac1777369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540886"
---
# <a name="modifykvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="1bfe8-103">Méthode ModifyKvpItems de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="1bfe8-103">ModifyKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1bfe8-104">Modifie des paires clé-valeur existantes sur un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-104">Modifies existing key-value pairs on a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bfe8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bfe8-105">Syntax</span></span>


```mof
uint32 ModifyKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1bfe8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bfe8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bfe8-107">*TargetSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bfe8-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bfe8-108">Type : **[ **CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="1bfe8-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="1bfe8-109">Référence à l’ordinateur virtuel sur lequel les paires clé/valeur seront modifiées.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-109">A reference to the virtual machine on which the key-value pairs will be modified.</span></span>

</dd> <dt>

<span data-ttu-id="1bfe8-110">*DataItems* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bfe8-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bfe8-111">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="1bfe8-111">Type: **string\[\]**</span></span>

<span data-ttu-id="1bfe8-112">Tableau de paires clé-valeur à modifier.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-112">An array of key-value pairs to be modified.</span></span> <span data-ttu-id="1bfe8-113">Chaque élément du tableau est une instance incorporée de la classe [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1bfe8-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="1bfe8-114">Cette méthode échoue si l’une des paires clé-valeur spécifiées n’existe pas sur le système cible.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-114">This method fails if any of the specified key-value pairs does not exist on the target system.</span></span> <span data-ttu-id="1bfe8-115">Ce tableau peut contenir au maximum 128 éléments.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="1bfe8-116">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1bfe8-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bfe8-117">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1bfe8-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="1bfe8-118">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1bfe8-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bfe8-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1bfe8-119">Return value</span></span>

<span data-ttu-id="1bfe8-120">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1bfe8-120">Type: **uint32**</span></span>

<span data-ttu-id="1bfe8-121">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1bfe8-122">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-124">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-125">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-126">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-127">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-128">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-129">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-130">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-131">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-132">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-133">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1bfe8-134">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="1bfe8-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1bfe8-135">Notes</span><span class="sxs-lookup"><span data-stu-id="1bfe8-135">Remarks</span></span>

<span data-ttu-id="1bfe8-136">L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1bfe8-137">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1bfe8-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="1bfe8-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="1bfe8-138">Examples</span></span>

<span data-ttu-id="1bfe8-139">L’exemple C# suivant modifie des paires clé-valeur sur un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-139">The following C# sample modifies key-value pairs on a virtual machine.</span></span> <span data-ttu-id="1bfe8-140">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="1bfe8-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1bfe8-141">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class ModifyKvpItemsClass
    {
        static void ModifyKvpItems(string vmName, string itemName, string itemValue)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
            ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("ModifyKvpItems");
            ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

            ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();
            
            dataItem["Data"] = itemValue;
            dataItem["Name"] = itemName;
            dataItem["Source"] = 0;

            string[] dataItems = new string[1];
            dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            inParams["TargetSystem"] = vm.Path.Path;
            inParams["DataItems"] = dataItems;

            ManagementBaseObject outParams = virtualSystemService.InvokeMethod("ModifyKvpItems", inParams, null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("KvpItems were modified successfully.");
                }
                else
                {
                    Console.WriteLine("Failed to modify KvpItems");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine("KvpItems were modified successfully.");
            }
            else
            {
                Console.WriteLine("Modify virtual system kvp items failed with error {0}", outParams["ReturnValue"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            vm.Dispose();
            dataItem.Dispose();
            virtualSystemService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 3)
            {
                Console.WriteLine("Usage: ModifyKvpItems vmName itemName itemValue");
                return;
            }
            ModifyKvpItems(args[0], args[1], args[2]);
        }
    }
}
```



<span data-ttu-id="1bfe8-142">L’exemple de Visual Basic Scripting Edition (VBScript) suivant modifie les paires clé-valeur sur un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-142">The following Visual Basic Scripting Edition (VBScript) sample modifies key-value pairs on a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1bfe8-143">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1bfe8-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, vmName, itemName, itemValue, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
        itemValue = objArgs.Unnamed.Item(2)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName itemValue"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if ModifyKvpItems(myVm, itemName, itemValue) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "ModifyKvpItems failed"
        WScript.Quit(1)
    end if


End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    dim query
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' RemoveVirtualSystemResource
'-----------------------------------------------------------------
Function ModifyKvpItems(computerSystem, itemName, itemValue)

    dim dataItem, dataItems, objInParam, objOutParams
    
    ModifyKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    
    dataItem.Data = itemValue
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("ModifyKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.dataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("ModifyKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            ModifyKvpItems = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        ModifyKvpItems = true
    else
        WriteLog Format1("ModifyKvpItems failed with {0}", objOutParams.ReturnValue)
    end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)

    dim WMIJob, jobState
    WMIJobCompleted = true

    set WMIJob = objWMIService.Get(outParam.Job)
    
    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (WMIJob.JobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WMIJobCompleted = false
    end if
    
End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\ModifyKvpItems.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="1bfe8-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bfe8-144">Requirements</span></span>



| <span data-ttu-id="1bfe8-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bfe8-145">Requirement</span></span> | <span data-ttu-id="1bfe8-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bfe8-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfe8-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bfe8-147">Minimum supported client</span></span><br/> | <span data-ttu-id="1bfe8-148">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bfe8-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1bfe8-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bfe8-149">Minimum supported server</span></span><br/> | <span data-ttu-id="1bfe8-150">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bfe8-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1bfe8-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1bfe8-151">Namespace</span></span><br/>                | <span data-ttu-id="1bfe8-152">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1bfe8-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1bfe8-153">MOF</span><span class="sxs-lookup"><span data-stu-id="1bfe8-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bfe8-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bfe8-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bfe8-155">DLL</span><span class="sxs-lookup"><span data-stu-id="1bfe8-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bfe8-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1bfe8-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1bfe8-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bfe8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bfe8-158">**ModifyKvpItems (v1)**</span><span class="sxs-lookup"><span data-stu-id="1bfe8-158">**ModifyKvpItems (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifykvpitems-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="1bfe8-159">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="1bfe8-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

