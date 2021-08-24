---
description: Arrêt&\# 8194 ; La méthode de classe WMI décharge les programmes et les dll jusqu’à ce qu’il soit possible de mettre l’ordinateur hors connexion.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Méthode Shutdown de la classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 068551ee013634bde9a42584764c36f255bf322bedb97e6ebb3a5075c113e742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800839"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a>Méthode Shutdown de la \_ classe Win32 OperatingSystem

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Shutdown** décharge les programmes et les dll jusqu’à ce qu’il soit possible de mettre l’ordinateur hors connexion.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Shutdown();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Autre** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Remarques

Les ordinateurs doivent parfois être supprimés du réseau, peut-être pour des raisons de maintenance planifiée, car l’ordinateur ne fonctionne pas correctement ou pour effectuer un processus de configuration. Par exemple, si un serveur DHCP remet des adresses IP erronées, vous pouvez arrêter l’ordinateur jusqu’à ce qu’un technicien de service puisse être distribué pour résoudre le problème. Si vous pensez qu’une violation de la sécurité s’est produite, vous devrez peut-être arrêter certains serveurs pour vous assurer qu’ils ne sont pas accessibles tant que le problème de sécurité n’a pas été résolu. Certaines opérations de configuration (telles que la modification d’un nom d’ordinateur) nécessitent le redémarrage de l’ordinateur pour que la modification prenne effet.

Cette méthode arrête immédiatement l’ordinateur, si possible. Le système arrête tous les processus en cours d’exécution, vide toutes les mémoires tampons de fichiers sur le disque, puis met le système sous tension. le processus appelant doit avoir le privilège **SE \_ SHUTDOWN \_ NAME** , comme décrit dans l’exemple suivant.


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



Pour plus d’informations sur la définition d’un privilège, consultez [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations) et [exécution d’opérations privilégiées à l’aide de VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript). Pour obtenir des options d’arrêt supplémentaires, telles qu’une fermeture de session ou un arrêt forcé, consultez la méthode [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) .

## <a name="examples"></a>Exemples

Le code VBScript suivant arrête l’ordinateur local.

> [!Note]  
> Vous devez disposer du privilège d’arrêt pour appeler correctement la méthode Shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



Le code perl suivant arrête l’ordinateur local.

> [!Note]  
> Vous devez disposer du privilège d’arrêt pour appeler correctement la méthode Shutdown.

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
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



Le code VBScript suivant arrête l’ordinateur distant spécifié. Renseignez *\_ \_ nom du système distant* avec le nom du système distant à arrêter.

> [!Note]  
> Vous devez disposer du privilège RemoteShutdown pour appeler correctement la méthode **Shutdown** .

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
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

[**\_OperatingSystem Win32**](win32-operatingsystem.md)
</dt> <dt>

[Tâches WMI : gestion des postes de travail](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[Exécution d’opérations privilégiées à l’aide de VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

