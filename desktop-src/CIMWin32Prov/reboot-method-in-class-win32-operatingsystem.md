---
description: Le redémarrage&\# 8194 ; La méthode de classe WMI arrête le système informatique, puis le redémarre.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Méthode reboot de la classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006966"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Méthode reboot de la \_ classe Win32 OperatingSystem

La méthode de **redémarrage** de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) arrête le système informatique, puis le redémarre.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Reboot();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Autre** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Notes

La possibilité de redémarrer un ordinateur par programme permet aux administrateurs d’effectuer de nombreuses tâches de gestion d’ordinateur à distance.

Par exemple, si vous créez un script pour installer un logiciel ou apporter une modification de configuration qui nécessite le redémarrage d’un ordinateur, vous pouvez inclure la commande de redémarrage dans le script et effectuer la totalité de l’opération à distance. La méthode **reboot** peut être utilisée pour redémarrer un ordinateur. À l’instar de la méthode [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) , la méthode **reboot** exige que l’utilisateur utilise les informations d’identification de sécurité utilisées par le script pour posséder le privilège Shutdown.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant appelle la méthode reboot de la classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .

> [!Note]  
> Vous devez disposer du privilège d’arrêt pour appeler correctement la méthode Shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



Le code perl suivant appelle la méthode reboot de la classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .

> [!Note]  
> Vous devez disposer du privilège d’arrêt pour appeler correctement la méthode Shutdown.

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
  if (!defined $RetVal || $RetVal != 0)
  {
   print Win32::OLE->LastError, "\n"; 
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



Le code VBScript suivant appelle la méthode reboot de la classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) sur un système distant. Renseignez \_ nom du système distant \_ avec le nom du système distant à redémarrer.

> [!Note]  
> Vous devez disposer du privilège RemoteShutdown pour appeler correctement la méthode reboot

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



l’exemple suivant perl appelle la méthode reboot de la classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) sur un système distant. Renseignez \_ nom du système distant \_ avec le nom du système distant à redémarrer.

> [!Note]  
> Vous devez disposer du privilège RemoteShutdown pour appeler correctement la méthode reboot.

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



## <a name="requirements"></a>Spécifications



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

[**\_OperatingSystem Win32**](win32-operatingsystem.md)
</dt> <dt>

[**\_Méthode CIM OperatingSystem. Shutdown**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[Tâches WMI : gestion des postes de travail](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

