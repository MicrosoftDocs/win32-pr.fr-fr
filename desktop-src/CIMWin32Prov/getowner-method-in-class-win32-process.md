---
description: GetOwner&\# 8194 ; La méthode de classe WMI récupère le nom d’utilisateur et le nom de domaine sous lesquels le processus est en cours d’exécution.
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Méthode GetOwner de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110490"
---
# <a name="getowner-method-of-the-win32_process-class"></a>Méthode GetOwner de la \_ classe de processus Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwner** récupère le nom d’utilisateur et le nom de domaine sous lesquels le processus s’exécute.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Utilisateur* \[ à\]
</dt> <dd>

Retourne le nom d’utilisateur du propriétaire de ce processus.

</dd> <dt>

*Domaine* \[ à\]
</dt> <dd>

Retourne le nom de domaine sous lequel ce processus s’exécute.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

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

## <a name="examples"></a>Exemples

[Le pourcentage d’UC du processus d’analyse par nom avec propriétaire](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) L’exemple VBScript collecte le pourcentage d’utilisation du processeur ou du processeur et recherche le propriétaire du processus.

Les [serveurs obtenir tous les serveurs qu’une liste d’utilisateurs est connectée](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) à PowerShell sont des exemples de requêtes WMI pour le propriétaire de tous les processus de explorer.exe.

L’exemple de code VBScript suivant obtient le propriétaire de chaque processus en cours d’exécution.


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
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
</dt> </dl>

 

