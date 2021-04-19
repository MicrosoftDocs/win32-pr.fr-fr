---
description: Simule un clic sur le bouton du périphérique spécifié.
ms.assetid: 1153BF91-F1F6-4E0A-8100-7625A3C73BB3
title: Méthode ClickButton de la classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2f5ea8e1f5984bd7e4b77222d6cbd8a05d1ed40b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544910"
---
# <a name="clickbutton-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="71865-103">Méthode ClickButton de la \_ classe SyntheticMouse MSVM</span><span class="sxs-lookup"><span data-stu-id="71865-103">ClickButton method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="71865-104">Simule un clic sur le bouton du périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="71865-104">Simulates a button click of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="71865-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71865-105">Syntax</span></span>


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="71865-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71865-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71865-107">*buttonIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71865-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71865-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71865-108">Type: **uint32**</span></span>

<span data-ttu-id="71865-109">Index de base 1 du bouton.</span><span class="sxs-lookup"><span data-stu-id="71865-109">The 1-based index of the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71865-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71865-110">Return value</span></span>

<span data-ttu-id="71865-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71865-111">Type: **uint32**</span></span>

<span data-ttu-id="71865-112">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="71865-112">A return value of zero indicates success.</span></span> <span data-ttu-id="71865-113">Une valeur différente de zéro indique un échec de modification de l’état du bouton.</span><span class="sxs-lookup"><span data-stu-id="71865-113">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="71865-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="71865-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="71865-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="71865-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="71865-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="71865-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="71865-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="71865-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="71865-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="71865-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="71865-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="71865-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="71865-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="71865-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="71865-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="71865-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="71865-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="71865-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="71865-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="71865-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="71865-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="71865-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="71865-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="71865-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="71865-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="71865-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="71865-127">Notes</span><span class="sxs-lookup"><span data-stu-id="71865-127">Remarks</span></span>

<span data-ttu-id="71865-128">L’accès à la classe [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="71865-128">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="71865-129">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="71865-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="71865-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="71865-130">Examples</span></span>

<span data-ttu-id="71865-131">L’exemple C# suivant simule un clic sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="71865-131">The following C# sample simulates a button click.</span></span> <span data-ttu-id="71865-132">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="71865-132">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class ClickButtonClass
    {
        static ManagementObject GetComputerMouse(ManagementObject vm)
        {
            ManagementObjectCollection mouseCollection = vm.GetRelated
            (
                "Msvm_SyntheticMouse",
                "Msvm_SystemDevice",
                null,
                null,
                "PartComponent",
                "GroupComponent",
                false,
                null
            );

            ManagementObject mouse = null;

            foreach (ManagementObject instance in mouseCollection)
            {
                mouse = instance;
                break;
            }

            return mouse;
        }

        static ManagementObject GetVideoHead(ManagementObject vm)
        {
            ManagementObjectCollection videoControllers = vm.GetRelated
             (
                 "Msvm_SyntheticDisplayController",
                 "Msvm_SystemDevice",
                 null,
                 null,
                 "PartComponent",
                 "GroupComponent",
                 false,
                 null
             );

            ManagementObject videoController = null;

            foreach (ManagementObject instance in videoControllers)
            {
                videoController = instance;
                break;
            }

            ManagementObjectCollection videoHeads = videoController.GetRelated
             (
                 "Msvm_VideoHead",
                 "Msvm_VideoHeadOnController",
                 null,
                 null,
                 "Dependent",
                 "Antecedent",
                 false,
                 null
             );

            ManagementObject videoHead = null;

            foreach (ManagementObject instance in videoHeads)
            {
                videoHead = instance;
                break;
            }

            videoController.Dispose();

            return videoHead;
        }

        static bool SetMousePosition(ManagementObject mouse, ManagementObject video)
        {
            bool passed = false;
            
            ManagementBaseObject inParams = mouse.GetMethodParameters("setAbsolutePosition");

            inParams["horizontalPosition"] = 1;
            inParams["verticalPosition"] = Convert.ToInt32(video["CurrentVerticalResolution"]) - 1;

            ManagementBaseObject outParams = mouse.InvokeMethod("setAbsolutePosition", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine("Mouse position is set at (1,{0})", inParams["verticalPosition"]);
                passed = true;
            }
            else
            {
                Console.WriteLine("setAbsolutePosition operation failed with {0} error.", outParams["ReturnValue"]);
            }

            inParams.Dispose();
            outParams.Dispose();

            return passed;

        }

        static void ClickButton(string vmName, int buttonIndex)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject videoHead = GetVideoHead(vm);
            ManagementObject mouse = GetComputerMouse(vm);

            if (!SetMousePosition(mouse, videoHead))
            {
                return;
            }

            ManagementBaseObject inParams = mouse.GetMethodParameters("ClickButton");

            inParams["buttonIndex"] = buttonIndex;

            ManagementBaseObject outParams = mouse.InvokeMethod("ClickButton", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Button {0} was clicked on {1}", buttonIndex, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to click button {0}' on {1}", buttonIndex, vm["ElementName"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            mouse.Dispose();
            vm.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: ClickButton vmName buttonIndex");
                return;
            }
            ClickButton(args[0], Convert.ToInt32(args[1]));
        }
    }
}
```



<span data-ttu-id="71865-133">L’exemple de Visual Basic Scripting Edition (VBScript) suivant simule un clic sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="71865-133">The following Visual Basic Scripting Edition (VBScript) sample simulates a button click.</span></span>


```VB
option explicit 

dim objWMIService
dim fileSystem

const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    
    dim vmName, computer, objArgs, mouse, video, computerSystem, buttonIndex
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       buttonIndex = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript ClickButton.vbs vmName buttonIndex"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set mouse = GetComputerMouse(computerSystem)
    set video = GetComputerVideoHead(computerSystem)

    if ClickButton(mouse, buttonIndex, video) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "ClickButton failed"
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
' Retrieve Msvm_SyntheticMouse from given computer system
'-----------------------------------------------------------------
Function GetComputerMouse(computerSystem)
    On Error Resume Next
    dim query
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_SyntheticMouse", computerSystem.Path_.Path)
    set GetComputerMouse = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_VideoHead from given computer system
'-----------------------------------------------------------------
Function GetComputerVideoHead(computerSystem)
    On Error Resume Next
    dim query, controller
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_SyntheticDisplayController", computerSystem.Path_.Path)
    set controller = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
    
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_VideoHead", controller.Path_.Path)
    set GetComputerVideoHead = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if    
End Function
'-----------------------------------------------------------------
' set mouse relative position on a virtual machine
'-----------------------------------------------------------------
Function setAbsolutePosition(mouse, video)
    WriteLog Format1("setAbsolutePosition({0})", mouse.ElementName)
    
    dim objInParam, objOutParams
    
    setAbsolutePosition = false
    set objInParam = mouse.Methods_("setAbsolutePosition").InParameters.SpawnInstance_()
    objInParam.horizontalPosition = 1
    objInParam.verticalPosition = video.CurrentVerticalResolution - 1

    set objOutParams = mouse.ExecMethod_("setAbsolutePosition", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format1("Mouse position is set at (1,{0})", objInParam.verticalPosition)
        setAbsolutePosition = true
    end if

End Function

'-----------------------------------------------------------------
' Click mouse on a virtual machine
'-----------------------------------------------------------------
Function ClickButton(mouse, buttonIndex, video)
    WriteLog Format2("ClickButton({0}, {1})", mouse.ElementName, buttonIndex)
    
    dim objInParam, objOutParams
    
    ClickButton = false
    if Not setAbsolutePosition(mouse, video) then
        Exit Function
    end if


    set objInParam = mouse.Methods_("ClickButton").InParameters.SpawnInstance_()
    objInParam.buttonIndex = buttonIndex

    set objOutParams = mouse.ExecMethod_("ClickButton", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("{0} button {1} was clicked.", mouse.ElementName, buttonIndex)
        ClickButton = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\clickButton.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="71865-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71865-134">Requirements</span></span>



| <span data-ttu-id="71865-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71865-135">Requirement</span></span> | <span data-ttu-id="71865-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="71865-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71865-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71865-137">Minimum supported client</span></span><br/> | <span data-ttu-id="71865-138">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71865-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="71865-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71865-139">Minimum supported server</span></span><br/> | <span data-ttu-id="71865-140">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71865-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71865-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="71865-141">Namespace</span></span><br/>                | <span data-ttu-id="71865-142">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="71865-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="71865-143">MOF</span><span class="sxs-lookup"><span data-stu-id="71865-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71865-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71865-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="71865-145">DLL</span><span class="sxs-lookup"><span data-stu-id="71865-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71865-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71865-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="71865-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71865-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71865-148">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="71865-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

