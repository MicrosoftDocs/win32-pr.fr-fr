---
description: Ajoute des paires clé-valeur à un ordinateur virtuel.
ms.assetid: D952EC3D-24EB-4A68-8527-5BF522957CB6
title: Méthode AddKvpItems de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9e01a02615b8bb395a589160a765dec4e08526e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524231"
---
# <a name="addkvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode AddKvpItems de la \_ classe VirtualSystemManagementService MSVM

Ajoute des paires clé-valeur à un ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TargetSystem* \[ dans\]
</dt> <dd>

Type : **[ **CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)**

Référence à un objet [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel sur lequel les paires clé-valeur seront ajoutées.

</dd> <dt>

*DataItems* \[ dans\]
</dt> <dd>

Type : **chaîne \[ \]**

Tableau de paires clé-valeur à ajouter. Chaque élément du tableau est une instance incorporée de la classe [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) . Cette méthode échoue si l’une des paires clé-valeur spécifiées existe déjà sur le système cible. Ce tableau peut contenir au maximum 128 éléments.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’une des valeurs suivantes.

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

## <a name="remarks"></a>Notes

L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemples

L’exemple C# suivant ajoute des paires clé-valeur à un ordinateur virtuel. Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.

 


```CSharp
public static void AddKvpItems(string vmName, string itemName, string itemValue)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("AddKvpItems");
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

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("AddKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Resources were added successfully.");

        }
        else
        {
            Console.WriteLine("Failed to add resources");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Resources were added successfully.");
    }
    else
    {
        Console.WriteLine("Add virtual system Kvp items failed with error {0}", outParams["ReturnValue"]);
    }

    if (inParams != null)
    {
        inParams.Dispose();
    }

    if (outParams != null)
    {
        outParams.Dispose();
    }
}
```



L’exemple de Visual Basic Scripting Edition (VBScript) suivant ajoute des paires clé-valeur à un ordinateur virtuel.

> [!IMPORTANT]
> Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.

 


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

    if AddKvpItems(myVm, itemName, itemValue) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "AddKvpItems failed"
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
' AddKvpItems
'-----------------------------------------------------------------
Function AddKvpItems(computerSystem, itemName, itemValue)

    dim dataItem, dataItems, objInParam, objOutParams
    
    AddKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = itemValue
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("AddKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.DataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("AddKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            AddKvpItems = true
        end if
    elseif (objOutParams.ReturnValue = wmiSuccessful) then
        AddKvpItems = true
    else
        WriteLog Format1("AddKvpItem failed with error {0}", objOutParams.ReturnValue)
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
    set fileStream = fileSystem.OpenTextFile(".\AddKvpItems.log", 8, true)
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

