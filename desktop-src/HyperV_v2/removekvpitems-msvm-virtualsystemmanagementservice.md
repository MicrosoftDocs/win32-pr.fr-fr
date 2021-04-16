---
description: Supprime des paires clé-valeur existantes d’une machine virtuelle.
ms.assetid: B2ECF609-89BB-4117-982B-EF56D51E1321
title: Méthode RemoveKvpItems de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4921805ade9538a4e05a15331f707b9356411aa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530099"
---
# <a name="removekvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="bf8a8-103">Méthode RemoveKvpItems de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="bf8a8-103">RemoveKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="bf8a8-104">Supprime des paires clé-valeur existantes d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="bf8a8-104">Removes existing key-value pairs from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf8a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf8a8-105">Syntax</span></span>


```mof
uint32 RemoveKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bf8a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf8a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf8a8-107">*TargetSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf8a8-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8a8-108">Type : **[ **CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="bf8a8-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="bf8a8-109">Référence à l’ordinateur virtuel sur lequel les paires clé/valeur seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="bf8a8-109">A reference to the virtual machine on which the key-value pairs will be removed.</span></span>

</dd> <dt>

<span data-ttu-id="bf8a8-110">*DataItems* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf8a8-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8a8-111">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="bf8a8-111">Type: **string\[\]**</span></span>

<span data-ttu-id="bf8a8-112">Tableau de paires clé-valeur à supprimer (seules les clés doivent correspondre).</span><span class="sxs-lookup"><span data-stu-id="bf8a8-112">An array of key-value pairs to be removed (only the keys need to match).</span></span> <span data-ttu-id="bf8a8-113">Chaque élément du tableau est une instance incorporée de la classe [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="bf8a8-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="bf8a8-114">Cette méthode échoue si l’une des paires clé-valeur spécifiées n’existe pas sur le système cible.</span><span class="sxs-lookup"><span data-stu-id="bf8a8-114">This method fails if any of the specified key-value pairs does not exist on the target system.</span></span> <span data-ttu-id="bf8a8-115">Ce tableau peut contenir au maximum 128 éléments.</span><span class="sxs-lookup"><span data-stu-id="bf8a8-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="bf8a8-116">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bf8a8-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8a8-117">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="bf8a8-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="bf8a8-118">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bf8a8-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf8a8-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf8a8-119">Return value</span></span>

<span data-ttu-id="bf8a8-120">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf8a8-120">Type: **uint32**</span></span>

<span data-ttu-id="bf8a8-121">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bf8a8-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bf8a8-122">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-124">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-125">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-126">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-127">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-128">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-129">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-130">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-131">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-132">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-133">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bf8a8-134">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="bf8a8-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bf8a8-135">Notes</span><span class="sxs-lookup"><span data-stu-id="bf8a8-135">Remarks</span></span>

<span data-ttu-id="bf8a8-136">L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="bf8a8-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bf8a8-137">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bf8a8-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="bf8a8-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="bf8a8-138">Examples</span></span>

<span data-ttu-id="bf8a8-139">L’exemple C# suivant supprime des paires clé-valeur d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="bf8a8-139">The following C# sample removes key-value pairs from a virtual machine.</span></span> <span data-ttu-id="bf8a8-140">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="bf8a8-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf8a8-141">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="bf8a8-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public static void RemoveKvpItems(string vmName, string itemName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("RemoveKvpItems");
    ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

    ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();

    dataItem["Data"] = "";
    dataItem["Name"] = itemName;
    dataItem["Source"] = 0;

    string[] dataItems = new string[1];
    dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    inParams["TargetSystem"] = vm.Path.Path;
    inParams["DataItems"] = dataItems;

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("RemoveKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("KvpItems were removed successfully.");

        }
        else
        {
            Console.WriteLine("Failed to remove KvpItems");
        }
    } 
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("KvpItems were removed successfully.");
    }
    else
    {
        Console.WriteLine("Remove KvpItems failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    dataItem.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
    
}
```



<span data-ttu-id="bf8a8-142">L’exemple de Visual Basic Scripting Edition (VBScript) suivant supprime des paires clé-valeur d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="bf8a8-142">The following Visual Basic Scripting Edition (VBScript) sample removes key-value pairs from a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf8a8-143">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="bf8a8-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


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

    dim computer, vmName, itemName, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if RemoveKvpItems(myVm, itemName) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "RemoveKvpItems failed"
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
' RemoveKvpItems
'-----------------------------------------------------------------
Function RemoveKvpItems(computerSystem, itemName)

    dim dataItem, dataItems, objInParam, objOutParams
    
    RemoveKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = ""
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("RemoveKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.dataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("RemoveKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            RemoveKvpItems = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        RemoveKvpItems = true
    else
        WriteLog Format1("RemoveKvpItems failed with {0}", objOutParams.ReturnValue )
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
    set fileStream = fileSystem.OpenTextFile(".\RemoveKvpItems.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="bf8a8-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf8a8-144">Requirements</span></span>



| <span data-ttu-id="bf8a8-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf8a8-145">Requirement</span></span> | <span data-ttu-id="bf8a8-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf8a8-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf8a8-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf8a8-147">Minimum supported client</span></span><br/> | <span data-ttu-id="bf8a8-148">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf8a8-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bf8a8-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf8a8-149">Minimum supported server</span></span><br/> | <span data-ttu-id="bf8a8-150">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf8a8-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf8a8-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bf8a8-151">Namespace</span></span><br/>                | <span data-ttu-id="bf8a8-152">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bf8a8-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bf8a8-153">MOF</span><span class="sxs-lookup"><span data-stu-id="bf8a8-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf8a8-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf8a8-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf8a8-155">DLL</span><span class="sxs-lookup"><span data-stu-id="bf8a8-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf8a8-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf8a8-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf8a8-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf8a8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf8a8-158">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="bf8a8-158">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

