---
description: Appelle l’opération chkdsk sur le disque.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Méthode CHKDSK de la classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111107"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a>Méthode CHKDSK de la \_ classe disque logique Win32

La méthode d’instance **chkdsk** appelle l’opération **chkdsk** sur le disque.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FixErrors* \[ dans\]
</dt> <dd>

Indique ce qui doit être fait pour les erreurs détectées sur le disque. Si la **valeur est true**, les erreurs sont résolues. La valeur par défaut est **false**.

</dd> <dt>

*VigorousIndexCheck* \[ dans\]
</dt> <dd>

Si la **valeur est true**, une vérification moins énergique des entrées d’index doit être effectuée. La valeur par défaut est **false**.

</dd> <dt>

*SkipFolderCycle* \[ dans\]
</dt> <dd>

Si la **valeur est true**, la vérification du cycle de dossier doit être ignorée. La valeur par défaut est **true**.

</dd> <dt>

*ForceDismount* \[ dans\]
</dt> <dd>

Si la **valeur est true**, le disque doit être forcé à démonter avant la vérification. La valeur par défaut est **false**.

</dd> <dt>

*RecoverBadSectors* \[ dans\]
</dt> <dd>

Si la **valeur est true**, les secteurs incorrects doivent être localisés et les informations lisibles doivent être récupérées à partir de ces secteurs. La valeur par défaut est **false**.

</dd> <dt>

*OKToRunAtBootUp* \[ dans\]
</dt> <dd>

Si la **valeur est true**, l’opération **chkdsk** doit être effectuée au prochain démarrage, au cas où l’opération n’aurait pas pu être effectuée parce que le disque est verrouillé au moment où cette méthode est appelée. La valeur par défaut est **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) en cas de réussite. D’autres valeurs sont répertoriées dans la liste suivante. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Opération réussie-CHKDSK terminée**
</dt> <dd>

0

Opération réussie- [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) terminée

</dd> <dt>

**Réussite-verrouillé et CHKDSK planifié au redémarrage**
</dt> <dd>

1

</dd> <dt>

**Échec : système de fichiers inconnu**
</dt> <dd>

2

</dd> <dt>

**Échec-erreur inconnue**
</dt> <dd>

3

</dd> <dt>

**Échec : système de fichiers non pris en charge**
</dt> <dd>

4

</dd> </dl>

## <a name="remarks"></a>Notes

Cette méthode s’applique uniquement aux instances de disque logique qui représentent un disque physique de l’ordinateur. Elle ne s’applique pas aux lecteurs logiques mappés.

## <a name="examples"></a>Exemples

L’exemple de code[is CHKDSK Dirty défini sur un serveur](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) de code PowerShell examine le système distant et retourne la valeur true ou false si l’indicateur chkdsk/f a été défini.

L’exemple de code PowerShell [Disk Scan à](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) distance démarre ou planifie l’analyse du disque.

L’exemple de code VBScript suivant exécute ChkDsk.exe sur le lecteur D sur un ordinateur.


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
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
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

