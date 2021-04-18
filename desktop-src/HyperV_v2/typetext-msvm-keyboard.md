---
description: Simule une série de caractères typés.
ms.assetid: 5D4C9F27-84AA-4131-A9A3-2C72DB2E8909
title: Méthode TypeText de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeText
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 37e8227a545975a6193be63a8bd363e10e9805f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536197"
---
# <a name="typetext-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="f37bc-103">Méthode TypeText de la \_ classe de clavier MSVM</span><span class="sxs-lookup"><span data-stu-id="f37bc-103">TypeText method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="f37bc-104">Simule une série de caractères typés.</span><span class="sxs-lookup"><span data-stu-id="f37bc-104">Simulates a series of typed characters.</span></span> <span data-ttu-id="f37bc-105">Cela équivaut à appeler [**PressKey**](presskey-msvm-keyboard.md) suivi de [**ReleaseKey**](releasekey-msvm-keyboard.md) pour chaque caractère de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="f37bc-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md) for each character in the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f37bc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f37bc-106">Syntax</span></span>


```mof
uint32 TypeText(
  [in] string asciiText
);
```



## <a name="parameters"></a><span data-ttu-id="f37bc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f37bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f37bc-108">*asciiText* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f37bc-108">*asciiText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f37bc-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f37bc-109">Type: **string**</span></span>

<span data-ttu-id="f37bc-110">Série de caractères ASCII ou Unicode à taper.</span><span class="sxs-lookup"><span data-stu-id="f37bc-110">The series of ASCII or Unicode characters to type.</span></span> <span data-ttu-id="f37bc-111">La longueur maximale de cette chaîne dépend du type de caractères de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="f37bc-111">The maximum length of this string depends on the type of characters in the string.</span></span>



| <span data-ttu-id="f37bc-112">Type string</span><span class="sxs-lookup"><span data-stu-id="f37bc-112">String type</span></span>        | <span data-ttu-id="f37bc-113">Nombre maximal de caractères</span><span class="sxs-lookup"><span data-stu-id="f37bc-113">Maximum characters</span></span>                                                               |
|--------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f37bc-114">ASCII</span><span class="sxs-lookup"><span data-stu-id="f37bc-114">ASCII</span></span><br/>   | <span data-ttu-id="f37bc-115">512</span><span class="sxs-lookup"><span data-stu-id="f37bc-115">512</span></span><br/>                                                                   |
| <span data-ttu-id="f37bc-116">Unicode</span><span class="sxs-lookup"><span data-stu-id="f37bc-116">Unicode</span></span><br/> | <span data-ttu-id="f37bc-117">256 à 512, selon le nombre de paires de substitution dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="f37bc-117">256 to 512, depending on the number of surrogate pairs in the string.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f37bc-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f37bc-118">Return value</span></span>

<span data-ttu-id="f37bc-119">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f37bc-119">Type: **uint32**</span></span>

<span data-ttu-id="f37bc-120">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="f37bc-120">A return value of zero indicates success.</span></span> <span data-ttu-id="f37bc-121">Une valeur de retour d’une indique un échec provoqué par des caractères non traduisibles dans la chaîne d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f37bc-121">A return value of one indicates a failure caused by nontranslatable characters in the input string.</span></span> <span data-ttu-id="f37bc-122">Toutes les autres valeurs différentes de zéro indiquent un échec de modification de l’état de la clé.</span><span class="sxs-lookup"><span data-stu-id="f37bc-122">All other nonzero values indicate a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="f37bc-123">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="f37bc-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="f37bc-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-125">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="f37bc-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-126">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="f37bc-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-127">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="f37bc-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-128">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="f37bc-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-129">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="f37bc-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-130">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="f37bc-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-131">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="f37bc-131">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-132">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="f37bc-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-133">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="f37bc-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-134">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="f37bc-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f37bc-135">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="f37bc-135">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f37bc-136">Notes</span><span class="sxs-lookup"><span data-stu-id="f37bc-136">Remarks</span></span>

<span data-ttu-id="f37bc-137">L’accès à la classe de [**\_ clavier MSVM**](msvm-keyboard.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="f37bc-137">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f37bc-138">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f37bc-138">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="f37bc-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="f37bc-139">Examples</span></span>

<span data-ttu-id="f37bc-140">L’exemple C# suivant simule le texte tapé.</span><span class="sxs-lookup"><span data-stu-id="f37bc-140">The following C# sample simulates typing text.</span></span> <span data-ttu-id="f37bc-141">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="f37bc-141">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class TypeTextClass
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

        static void TypeText(string vmName, string text)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("TypeText");

            inParams["asciiText"] = text;

            ManagementBaseObject outParams = keyboard.InvokeMethod("TypeText", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Text {0} was typed on {1}", text, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to type '{0}' on {1}", text, vm["ElementName"]);
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
                Console.WriteLine("Usage: TypeText vmName Text");
                return;
            }
            TypeText(args[0], args[1]);
        }
    }
}

```



<span data-ttu-id="f37bc-142">L’exemple de Visual Basic Scripting Edition (VBScript) suivant simule le texte tapé.</span><span class="sxs-lookup"><span data-stu-id="f37bc-142">The following Visual Basic Scripting Edition (VBScript) sample simulates typing text.</span></span>


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
    dim computer, objArgs, vmName, computerSystem, text, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       text = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript TypeText.vbs vmName text"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if TypeText(keyboard, text) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "TypeText operation failed"
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
' Type the given text to the given keyboard
'-----------------------------------------------------------------
Function TypeText(keyboard, text)
    WriteLog Format2("TypeText({0}, {1})", keyboard.ElementName, text)
    
    dim objInParam, objOutParams

    TypeText = false
    set objInParam = keyboard.Methods_("TypeText").InParameters.SpawnInstance_()
    objInParam.asciiText = text

    set objOutParams = keyboard.ExecMethod_("TypeText", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("'{0}' was typed on {1}", text, keyboard.ElementName)
        TypeText = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\Typetext.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="f37bc-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f37bc-143">Requirements</span></span>



| <span data-ttu-id="f37bc-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f37bc-144">Requirement</span></span> | <span data-ttu-id="f37bc-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="f37bc-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f37bc-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f37bc-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f37bc-147">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f37bc-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f37bc-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f37bc-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f37bc-149">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f37bc-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f37bc-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f37bc-150">Namespace</span></span><br/>                | <span data-ttu-id="f37bc-151">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f37bc-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f37bc-152">MOF</span><span class="sxs-lookup"><span data-stu-id="f37bc-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f37bc-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f37bc-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f37bc-154">DLL</span><span class="sxs-lookup"><span data-stu-id="f37bc-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f37bc-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f37bc-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f37bc-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f37bc-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f37bc-157">**\_Clavier MSVM**</span><span class="sxs-lookup"><span data-stu-id="f37bc-157">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

