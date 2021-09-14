---
description: Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’imprimante.
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: Méthode SetSecurityDescriptor de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1572919d0ac0b5c18a6fc5084636c52b9b3ea1c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012338"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a>Méthode SetSecurityDescriptor de la \_ classe Printer Win32

La méthode **SetSecurityDescriptor** écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’imprimante. Le descripteur de sécurité est une instance de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Descripteur* \[ dans\]
</dt> <dd>

Descripteur de sécurité associé à l’imprimante.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

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

Vous pouvez mettre à jour la liste DACL et la liste SACL dans l’instance [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) lors de l’appel de cette méthode, mais vous pouvez également mettre à jour uniquement la liste DACL ou uniquement la liste SACL.

Les valeurs suivantes dans [**le \_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) déterminent si la liste DACL, la liste SACL ou les deux sont mises à jour.

-   **SE \_ liste DACL \_ présente**

    Indique que la liste DACL doit être mise à jour. Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste DACL.

-   **SE \_ liste SACL \_ présente**

    Indique que la liste SACL doit être mise à jour. Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste SACL. Pour mettre à jour la liste SACL, le privilège **SeSecurityPrivilege** doit être activé sur le compte. Pour les scripts, le nom du privilège est **SeSecurityPrivilege**. Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants).

Si les propriétés tiers de confiance du groupe et tiers de confiance du propriétaire ne sont pas **null**, elles sont mises à jour. Dans le cas contraire, WMI conserve les valeurs d’origine. Pour plus d’informations, consultez [objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).

Quand une nouvelle SACL est **null** dans un appel à cette méthode, alors le descripteur de sécurité SACL de l’objet sécurisable cible reste inchangé.

## <a name="examples"></a>Exemples

L’exemple PowerShell [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) remplace les autorisations (ACL) d’une imprimante à une autre.

L’exemple de code PowerShell suivant décrit comment définir le descripteur de sécurité d’une imprimante.


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a>Spécifications



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

 

