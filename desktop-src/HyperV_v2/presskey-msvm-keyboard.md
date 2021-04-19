---
description: Simule une pression sur une touche.
ms.assetid: 42C11F92-6143-40D7-9C07-56A6514EB4D1
title: Méthode PressKey de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.PressKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9f196c5af3f8946460564e56bb425ffc24b51c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539338"
---
# <a name="presskey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="02dfb-103">Méthode PressKey de la \_ classe de clavier MSVM</span><span class="sxs-lookup"><span data-stu-id="02dfb-103">PressKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="02dfb-104">Simule une pression sur une touche.</span><span class="sxs-lookup"><span data-stu-id="02dfb-104">Simulates a key press.</span></span> <span data-ttu-id="02dfb-105">En cas de réussite, la clé est à l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="02dfb-105">When successful the key will be in the down state.</span></span>

## <a name="syntax"></a><span data-ttu-id="02dfb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02dfb-106">Syntax</span></span>


```mof
uint32 PressKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="02dfb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02dfb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02dfb-108">*keyCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02dfb-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02dfb-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02dfb-109">Type: **uint32**</span></span>

<span data-ttu-id="02dfb-110">Code de la touche virtuelle de la touche sur laquelle appuyer.</span><span class="sxs-lookup"><span data-stu-id="02dfb-110">The virtual-key code of the key to press.</span></span> <span data-ttu-id="02dfb-111">Pour obtenir la liste des codes de touche virtuelle, consultez la page [**codes de clé virtuelle**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="02dfb-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02dfb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02dfb-112">Return value</span></span>

<span data-ttu-id="02dfb-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02dfb-113">Type: **uint32**</span></span>

<span data-ttu-id="02dfb-114">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="02dfb-114">A return value of zero indicates success.</span></span> <span data-ttu-id="02dfb-115">Une valeur différente de zéro indique un échec de modification de l’état de la clé.</span><span class="sxs-lookup"><span data-stu-id="02dfb-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="02dfb-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="02dfb-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="02dfb-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="02dfb-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="02dfb-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="02dfb-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="02dfb-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="02dfb-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="02dfb-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="02dfb-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="02dfb-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="02dfb-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="02dfb-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="02dfb-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="02dfb-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="02dfb-129">Notes</span><span class="sxs-lookup"><span data-stu-id="02dfb-129">Remarks</span></span>

<span data-ttu-id="02dfb-130">La méthode **PressKey** mappe les références au **\_ menu VK** (18), **au \_ contrôle VK** (17) et à **VK \_ Shift** (16) **à VK \_ LMENU** (164), **VK \_ LCONTROL** (162) et **VK \_ LSHIFT** (160), respectivement, car le **\_ menu VK**, le **\_ contrôle VK** et les codes de touches virtuelles **VK \_ Shift** ne représentent pas des clés réelles sur un clavier.</span><span class="sxs-lookup"><span data-stu-id="02dfb-130">The **PressKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="02dfb-131">L’accès à la classe de [**\_ clavier MSVM**](msvm-keyboard.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="02dfb-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="02dfb-132">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="02dfb-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="02dfb-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="02dfb-133">Examples</span></span>

<span data-ttu-id="02dfb-134">L’exemple C# suivant simule une pression sur une touche.</span><span class="sxs-lookup"><span data-stu-id="02dfb-134">The following C# sample simulates a key press.</span></span> <span data-ttu-id="02dfb-135">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="02dfb-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class PressKeyClass
    {
        static ManagementObject GetComputerKeyboard(ManagementObject vm)
        {
            ManagementObjectCollection keyboardCollection = vm.GetRelated
            (
                "Msvm_Keyboard",
                "Msvm_SystemDevice",
                null,
                null,
                "PartComponent",
                "GroupComponent",
                false,
                null
            );

            ManagementObject keyboard = null;

            foreach (ManagementObject instance in keyboardCollection)
            {
                keyboard = instance;
                break;
            }

            return keyboard;
        }

        static void PressKey(string vmName, int keyCode)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("PressKey");

            inParams["keyCode"] = keyCode;

            ManagementBaseObject outParams = keyboard.InvokeMethod("PressKey", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Key {0} was pressed on {1}", keyCode, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to press key {0}' on {1}", keyCode, vm["ElementName"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            keyboard.Dispose();
            vm.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: PressKey vmName keyCode");
                return;
            }
            string vmName = args[0];
            int keyCode = int.Parse(args[1]);
            PressKey(args[0], keyCode);
        }

    }
}

```



<span data-ttu-id="02dfb-136">L’exemple de Visual Basic Scripting Edition (VBScript) suivant simule une pression sur une touche.</span><span class="sxs-lookup"><span data-stu-id="02dfb-136">The following Visual Basic Scripting Edition (VBScript) sample simulates a key press.</span></span>


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
    
    dim computer, objArgs, vmName, computerSystem, keycode, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       keycode = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript PressKey.vbs vmName keycode"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if PressKey(keyboard, keycode) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "PressKey failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    dim query
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_Keyboard from given computer system
' 
'-----------------------------------------------------------------
Function GetComputerKeyboard(computerSystem)
    dim query
    On Error Resume Next
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_Keyboard", computerSystem.Path_.Path)
    set GetComputerKeyboard = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' Press the key with the given key code on the given keyboard
'-----------------------------------------------------------------
Function PressKey(keyboard, keyCode)
    WriteLog Format2("PressKey({0}, {1})", keyboard.ElementName, keyCode)
    
    dim objInParam, objOutParams
    
    PressKey = false
    set objInParam = keyboard.Methods_("PressKey").InParameters.SpawnInstance_()
    objInParam.keyCode = keyCode

    set objOutParams = keyboard.ExecMethod_("PressKey", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("The key with code '{0}' is typed on {1}.", keyCode, keyboard.ElementName)
        PressKey = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\PressKey.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="02dfb-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02dfb-137">Requirements</span></span>



| <span data-ttu-id="02dfb-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02dfb-138">Requirement</span></span> | <span data-ttu-id="02dfb-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="02dfb-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02dfb-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02dfb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="02dfb-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02dfb-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="02dfb-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02dfb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="02dfb-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02dfb-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02dfb-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="02dfb-144">Namespace</span></span><br/>                | <span data-ttu-id="02dfb-145">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="02dfb-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="02dfb-146">MOF</span><span class="sxs-lookup"><span data-stu-id="02dfb-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02dfb-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02dfb-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02dfb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="02dfb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02dfb-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02dfb-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02dfb-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02dfb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02dfb-151">**\_Clavier MSVM**</span><span class="sxs-lookup"><span data-stu-id="02dfb-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="02dfb-152">**Codes de clé virtuelle**</span><span class="sxs-lookup"><span data-stu-id="02dfb-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

