---
description: Retourne le descripteur de sécurité qui contrôle l’accès à l’imprimante.
ms.assetid: c12ca35c-07b3-41ad-98c4-48ee584059d1
ms.tgt_platform: multiple
title: Méthode GetSecurityDescriptor de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c74d79430d15fa136c6edeb2a6e77e79e76b02ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514337"
---
# <a name="getsecuritydescriptor-method-of-the-win32_printer-class"></a>Méthode GetSecurityDescriptor de la \_ classe Printer Win32

La méthode **GetSecurityDescriptor** retourne le descripteur de sécurité qui contrôle l’accès à l’imprimante. Le descripteur est retourné sous la forme d’une instance de l’expression [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Descripteur* \[ à\]
</dt> <dd>

Descripteur de sécurité associé à l’imprimante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Achèvement réussi.

</dd> <dt>

**2**
</dt> <dd>

L’utilisateur n’a pas accès aux informations demandées.

</dd> <dt>

**8**
</dt> <dd>

Échec inconnu.

</dd> <dt>

**9**
</dt> <dd>

L’utilisateur ne dispose pas des privilèges suffisants pour exécuter la méthode.

</dd> <dt>

**21**
</dt> <dd>

Un paramètre spécifié dans l’appel de méthode n’est pas valide.

</dd> </dl>

## <a name="remarks"></a>Notes

L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL). Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).

Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné. Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant répertorie les imprimantes connectées à l’ordinateur local et obtient le descripteur de sécurité pour chaque imprimante. Les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) de la liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) sont extraites pour déterminer les utilisateurs ayant accès à l’imprimante.


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set objWMIService = GetObject("winmgmts:")
Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        arrACEs = objSD.DACL
    For Each objACE in arrACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Imprimante Win32**](win32-printer.md)
</dt> <dt>

[**Constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modification de la sécurité d’accès sur les objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

