---
description: Supprime tous les travaux, y compris celui qui est actuellement en cours d’impression dans la file d’attente.
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Méthode CancelAllJobs de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06aae96cec4e38c7ff9c213cd19dc35e9843a077c262aafcaf0aed43160505a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085839"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a>Méthode CancelAllJobs de la \_ classe Printer Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CancelAllJobs** supprime tous les travaux, y compris celui qui est actuellement en cours d’impression à partir de la file d’attente.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Succès

</dd> <dt>

**5**
</dt> <dd>

accès refusé

</dd> </dl>

## <a name="examples"></a>Exemples

La fonction [notifier les utilisateurs lorsqu’une file d’attente à l’impression est purgée](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) utilise Msg.exe pour envoyer une alerte réseau à tous les utilisateurs qui avaient des documents dans une file d’attente à l’impression sur le lieu d’être purgés. Après l’envoi des alertes, le script vide la file d’attente à l’impression.

L’exemple de code VBScript [Supprimer tous les travaux d’impression](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) supprime tous les travaux d’impression sur l’ordinateur local.

L’exemple VBScript suivant supprime tous les travaux d’impression pour une imprimante nommée HP QuietJet.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
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

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> <dt>

[**\_Imprimante Win32**](win32-printer.md)
</dt> </dl>

 

