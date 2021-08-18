---
description: Planifie l’exécution de Autochk sur le lecteur de disque représenté par le disque \_ logique Win32 au prochain redémarrage si le bit modifié est défini.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Méthode ScheduleAutoChk de la classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7e4920bdded79a7f63cbe7beaf28a70837ad7a47c2b28a1e37d83208b4f4e6f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588189"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>Méthode ScheduleAutoChk de la \_ classe disque logique Win32

La méthode de la classe **ScheduleAutoChk** planifie l’exécution de Autochk sur le lecteur de disque représenté par le disque [**\_ logique Win32**](win32-logicaldisk.md) au redémarrage suivant si le bit modifié est défini.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Disque logique* \[ dans\]
</dt> <dd>

Spécifie la liste des lecteurs à planifier pour Autochk au prochain redémarrage. La syntaxe de chaîne se compose de la lettre de lecteur suivie d’un signe deux-points pour le disque logique, par exemple : « C : »

> [!Note]  
> Vérifiez toujours la validité des lettres de lecteur dans le tableau de disques *logiques* lorsque les données proviennent d’une source inconnue ou d’une source qui n’est pas digne de confiance.

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) en cas de réussite, et une autre valeur si une autre erreur se produit. Les valeurs sont répertoriées dans la liste suivante. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Aucune erreur** (0)
</dt> <dt>

**Erreur : lecteur distant** (1)
</dt> <dt>

**Erreur : lecteur amovible** (2)
</dt> <dt>

**Erreur : le lecteur n’est pas un répertoire racine** (3)
</dt> <dt>

**Erreur : lecteur inconnu** (4)
</dt> </dl>

## <a name="remarks"></a>Remarques

Cette méthode s’applique uniquement aux instances de disque logique qui représentent un disque physique de l’ordinateur. Cette méthode n’est pas applicable aux lecteurs logiques mappés.

## <a name="examples"></a>Exemples

Les exemples VBScript et PowerShell suivants planifient Autochk.exe pour s’exécuter sur le lecteur C lors du prochain redémarrage de l’ordinateur.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
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

[**\_Disque logique Win32**](win32-logicaldisk.md)
</dt> </dl>

 

