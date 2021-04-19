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
# <a name="create-method-of-the-win32_process-class"></a>Créer une méthode de la \_ classe de processus Win32

La méthode **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) crée un nouveau processus.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ligne* \[ de commande dans\]
</dt> <dd>

Ligne de commande à exécuter. Le système ajoute un caractère null à la ligne de commande, en ajustant la chaîne si nécessaire, pour indiquer quel fichier a été réellement utilisé.

</dd> <dt>

*CurrentDirectory* \[ dans\]
</dt> <dd>

Lecteur et répertoire actifs pour le processus enfant. La chaîne requiert que le répertoire en cours soit résolu en chemin connu. Un utilisateur peut spécifier un chemin d’accès absolu ou un chemin d’accès relatif au répertoire de travail actuel. Si ce paramètre a la **valeur null**, le nouveau processus aura le même chemin d’accès que le processus appelant. Cette option est fournie principalement pour les interpréteurs de commande qui doivent démarrer une application et spécifier le lecteur initial et le répertoire de travail de l’application.

</dd> <dt>

*ProcessStartupInformation* \[ dans\]
</dt> <dd>

Configuration de démarrage d’un processus Windows. Pour plus d’informations, consultez [**Win32 \_ ProcessStartup**](win32-processstartup.md).

</dd> <dt>

*ProcessID* \[ à\]
</dt> <dd>

Identificateur de processus global qui peut être utilisé pour identifier un processus. La valeur est valide à partir du moment où le processus est créé jusqu’au moment où le processus est terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) si le processus a été créé avec succès, et tout autre nombre pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Achèvement réussi** (0)
</dt> <dt>

**Accès refusé** (2)
</dt> <dt>

**Privilèges insuffisants** (3)
</dt> <dt>

**Échec inconnu** (8)
</dt> <dt>

**Chemin introuvable** (9)
</dt> <dt>

**Paramètre non valide** (21)
</dt> <dt>

**Autre** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Notes

Vous pouvez créer une instance de la classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) pour configurer le processus avant d’appeler cette méthode.

Un chemin d’accès qualifié complet doit être spécifié dans les cas où le programme à lancer n’est pas dans le chemin de recherche de Winmgmt.exe. Si le processus nouvellement créé tente d’interagir avec des objets sur le système cible sans les privilèges d’accès appropriés, il est arrêté sans notification à cette méthode.

Pour des raisons de sécurité, la méthode **Win32 \_ Process. Create** ne peut pas être utilisée pour démarrer un processus interactif à distance.

Les processus créés avec la méthode **Win32 \_ Process. Create** sont limités par l’objet de traitement, à moins que l’indicateur **Create \_ dissociation \_ from \_ Job** soit spécifié. Pour plus d’informations, consultez [**Win32 \_ ProcessStartup**](win32-processstartup.md) et [**\_ \_ ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).

## <a name="examples"></a>Exemples

L’exemple VBScript suivant montre comment appeler une méthode CIM comme s’il s’agissait d’une méthode Automation de SWbemObject.


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



L’exemple perl suivant montre comment appeler une méthode CIM comme s’il s’agissait d’une méthode Automation de SWbemObject.


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



L’exemple de code VBScript suivant crée un processus Notepad sur l’ordinateur local. [**Win32 \_ ProcessStartup**](win32-processstartup.md) est utilisé pour configurer les paramètres de processus.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processus Win32**](win32-process.md)
</dt> <dt>

[Tâches WMI : processus](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

