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
ms.openlocfilehash: d56bc65bba5728c95521a53a51ad77f34b710d3cddcb987f5209d28619870f34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118391628"
---
# <a name="typetext-method-of-the-msvm_keyboard-class"></a>Méthode TypeText de la \_ classe de clavier MSVM

Simule une série de caractères typés. Cela équivaut à appeler [**PressKey**](presskey-msvm-keyboard.md) suivi de [**ReleaseKey**](releasekey-msvm-keyboard.md) pour chaque caractère de la chaîne.

## <a name="syntax"></a>Syntaxe


```mof
uint32 TypeText(
  [in] string asciiText
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*asciiText* \[ dans\]
</dt> <dd>

Type : **chaîne**

Série de caractères ASCII ou Unicode à taper. La longueur maximale de cette chaîne dépend du type de caractères de la chaîne.



| Type string        | Nombre maximal de caractères                                                               |
|--------------------|----------------------------------------------------------------------------------|
| ASCII<br/>   | 512<br/>                                                                   |
| Unicode<br/> | 256 à 512, selon le nombre de paires de substitution dans la chaîne.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Une valeur de retour de zéro indique une réussite. Une valeur de retour d’une indique un échec provoqué par des caractères non traduisibles dans la chaîne d’entrée. Toutes les autres valeurs différentes de zéro indiquent un échec de modification de l’état de la clé.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe de [**\_ clavier MSVM**](msvm-keyboard.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemples

L’exemple C# suivant simule le texte tapé. Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).


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



l’exemple VBScript (Visual Basic scripting Edition) suivant simule le texte tapé.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Clavier MSVM**](msvm-keyboard.md)
</dt> </dl>

 

