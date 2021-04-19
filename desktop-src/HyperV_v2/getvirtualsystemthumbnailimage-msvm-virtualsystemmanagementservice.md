---
description: Récupère l’image miniature d’une machine virtuelle existante.
ms.assetid: 8D670D2E-EAD7-47FF-B13C-764EFFDF4547
title: Méthode GetVirtualSystemThumbnailImage de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetVirtualSystemThumbnailImage
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2c8288d2acee5816c4546b968a9a26c083cbbc88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531881"
---
# <a name="getvirtualsystemthumbnailimage-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6a8cf-103">Méthode GetVirtualSystemThumbnailImage de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="6a8cf-103">GetVirtualSystemThumbnailImage method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6a8cf-104">Récupère l’image miniature d’une machine virtuelle existante.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-104">Retrieves the thumbnail image of an existing virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a8cf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a8cf-105">Syntax</span></span>


```mof
uint32 GetVirtualSystemThumbnailImage(
  [in]  CIM_VirtualSystemSettingData REF TargetSystem,
  [in]  uint16                           WidthPixels,
  [in]  uint16                           HeightPixels,
  [out] uint8                            ImageData[]
);
```



## <a name="parameters"></a><span data-ttu-id="6a8cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a8cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a8cf-107">*TargetSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a8cf-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8cf-108">Type : **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="6a8cf-108">Type: **CIM\_VirtualSystemSettingData**</span></span>

<span data-ttu-id="6a8cf-109">Référence à l’instance [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) dont l’image miniature doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-109">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance whose thumbnail image is to be retrieved.</span></span> <span data-ttu-id="6a8cf-110">Cette instance peut représenter l’instanciation actuelle de l’ordinateur virtuel ou une instance d’une capture instantanée d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-110">This instance may represent either the current instantiation of the virtual machine, or an instance of a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="6a8cf-111">*WidthPixels* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a8cf-111">*WidthPixels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8cf-112">Type : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a8cf-112">Type: **uint16**</span></span>

<span data-ttu-id="6a8cf-113">Largeur de l’image souhaitée, en pixels.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-113">The width of the desired image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6a8cf-114">*HeightPixels* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a8cf-114">*HeightPixels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8cf-115">Type : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a8cf-115">Type: **uint16**</span></span>

<span data-ttu-id="6a8cf-116">Hauteur de l’image souhaitée, en pixels.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-116">The height of the desired image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6a8cf-117">*ImageData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6a8cf-117">*ImageData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8cf-118">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="6a8cf-118">Type: **uint8\[\]**</span></span>

<span data-ttu-id="6a8cf-119">Données d’image demandées au format RGB brut 565.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-119">The requested image data, in raw RGB 565 format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a8cf-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a8cf-120">Return value</span></span>

<span data-ttu-id="6a8cf-121">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a8cf-121">Type: **uint32**</span></span>

<span data-ttu-id="6a8cf-122">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-122">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6a8cf-123">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-125">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-126">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-127">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-128">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-129">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-130">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-131">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-131">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-132">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-133">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-134">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6a8cf-135">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="6a8cf-135">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6a8cf-136">Notes</span><span class="sxs-lookup"><span data-stu-id="6a8cf-136">Remarks</span></span>

<span data-ttu-id="6a8cf-137">L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-137">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6a8cf-138">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6a8cf-138">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="6a8cf-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="6a8cf-139">Examples</span></span>

<span data-ttu-id="6a8cf-140">L’exemple C# suivant récupère l’image miniature d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-140">The following C# sample retrieves the thumbnail image of a virtual machine.</span></span> <span data-ttu-id="6a8cf-141">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="6a8cf-141">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a8cf-142">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-142">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
static void SaveImageData(byte[] imageData)
{
    FileStream fs = new FileStream(@"c:\test.bin", FileMode.Create, FileAccess.Write);
    fs.Write(imageData, 0, imageData.Length);
    fs.Flush();
    fs.Close();
}

public static void GetVirtualSystemThumbnailImage(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);

    ManagementObjectCollection vmsettingDatas = vm.GetRelated(
        "Msvm_VirtualSystemsettingData",
        "Msvm_SettingsDefineState",
        null,
        null,
        "SettingData",
        "ManagedElement",
        false,
        null);

    ManagementObject settingData = null;

    foreach (ManagementObject data in vmsettingDatas)
    {
        settingData = data;
        break;
    }


    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetVirtualSystemThumbnailImage");
    inParams["HeightPixels"] = 16;
    inParams["WidthPixels"] = 16;
    inParams["TargetSystem"] = settingData.Path.Path;


    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetVirtualSystemThumbnailImage", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            SaveImageData((byte[])outParams["ImageData"]);
            Console.WriteLine("VM '{0}' thumbnail were retrieved successfully.", vm["ElementName"]);
        }
        else
        {
            Console.WriteLine("Failed to retrieve VM thumbnail");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        SaveImageData((byte[])outParams["ImageData"]);
        Console.WriteLine("VM '{0}' thumbnail were retrieved successfully.", vm["ElementName"]);
    }
    else
    {
        Console.WriteLine("Failed to retrieve VM thumbnail with error {0}", (UInt32)outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    settingData.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



<span data-ttu-id="6a8cf-143">L’exemple de Visual Basic Scripting Edition suivant (VBScript) récupère l’image miniature d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-143">The following Visual Basic Scripting Edition (VBScript) sample retrieves the thumbnail image of a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a8cf-144">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-144">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem

const wmiStarted = 4096
const wmiSuccessful = 0

Main()


'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, objArgs, vmName, vm
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")
    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)
    
    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 1 then
        vmName = objArgs.Unnamed.Item(0)
    else
        WScript.Echo "usage: cscript GetVirtualSystemThumbnailImage.vbs vmName"
        WScript.Quit(1)
    end if
    
    set vm = GetComputerSystem(vmName)
    
    if StartVm(vm) then
        if GetVirtualSystemThumbnailImage(vm) then
            WriteLog "Done"
            WScript.Quit(0)
         End if
    end if
    
    WriteLog "GetVirtualSystemThumbnailImage Failed."
    WScript.Quit(1)
    
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
' Save the thumbnail
'-----------------------------------------------------------------
Sub SaveThumbnailImage(thumbnailBytes)

    dim stream 
    Const adTypeText = 2
    Const adSaveCreateOverWrite = 2  
    
    set stream = CreateObject("ADODB.Stream")
    stream.Type = adTypeText
  
    stream.Open
    Redim text(ubound(thumbnailBytes) \ 2)
    for i = lbound(thumbnailBytes) to ubound(thumbnailBytes) step 2
        text(i\2) = ChrW(thumbnailBytes(i + 1) * &HFF + thumbnailBytes(i))
    next
    stream.WriteText text
  
    stream.SaveToFile ".\thumbnail.bin", adSaveCreateOverWrite
    stream.Close
    
  
End Sub

'-----------------------------------------------------------------
' Start the virtual machine 
'-----------------------------------------------------------------
Function StartVm(computerSystem)
    
    dim objInParam, objOutParams
    StartVm = false
    if computerSystem.OperationalStatus(0) = 2 then
        StartVm = true
        Exit Function
    end if
    
    set objInParam = computerSystem.Methods_("RequestStateChange").InParameters.SpawnInstance_()
    objInParam.RequestedState = 2
    set objOutParams = computerSystem.ExecMethod_("RequestStateChange", objInParam)
    
    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            StartVm = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        StartVm = true
    else
        WriteLog Format1("StartVM failed with ReturnValue {0}", wmiStatus)
    end if
    
End Function


'-----------------------------------------------------------------
' Print the thumbnail data
'-----------------------------------------------------------------
Sub PrintThumbnailImage(thumbnailBytes)
    dim index
    for index = lbound(thumbnailBytes) to ubound(thumbnailBytes)
        WriteLog Format2("{0}:{1} ", index, thumbnailBytes(i))
    next
End Sub
'-----------------------------------------------------------------
' Define a virtual system
'-----------------------------------------------------------------
Function GetVirtualSystemThumbnailImage(computerSystem)
    dim query, objInParam, objOutParams, virtualSystemsetting
    
    GetVirtualSystemThumbnailImage = false
    
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_VirtualSystemsettingData", computerSystem.Path_.Path)
    set virtualSystemsetting = objWMIService.ExecQuery(query).ItemIndex(0)
    
    set objInParam = managementService.Methods_("GetVirtualSystemThumbnailImage").InParameters.SpawnInstance_()

    objInParam.HeightPixels = 16
    objInParam.WidthPixels = 16
    objInParam.TargetSystem = virtualSystemsetting.Path_.Path
    
    set objOutParams = managementService.ExecMethod_("GetVirtualSystemThumbnailImage", objInParam)
    
    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            GetVirtualSystemThumbnailImage = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        GetVirtualSystemThumbnailImage = true
    else
        WriteLog Format1("GetVirtualSystemThumbnailImage failed with ReturnValue {0}", wmiStatus)
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    
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
    set fileStream = fileSystem.OpenTextFile(".\GetVirtualSystemThumbnailImage.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="6a8cf-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a8cf-145">Requirements</span></span>



| <span data-ttu-id="6a8cf-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a8cf-146">Requirement</span></span> | <span data-ttu-id="6a8cf-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8cf-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a8cf-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a8cf-148">Minimum supported client</span></span><br/> | <span data-ttu-id="6a8cf-149">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a8cf-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6a8cf-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a8cf-150">Minimum supported server</span></span><br/> | <span data-ttu-id="6a8cf-151">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a8cf-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6a8cf-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6a8cf-152">Namespace</span></span><br/>                | <span data-ttu-id="6a8cf-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6a8cf-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6a8cf-154">MOF</span><span class="sxs-lookup"><span data-stu-id="6a8cf-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a8cf-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a8cf-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a8cf-156">DLL</span><span class="sxs-lookup"><span data-stu-id="6a8cf-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a8cf-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a8cf-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6a8cf-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a8cf-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a8cf-159">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6a8cf-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

