---
description: La méthode Win32ShutdownTracker fournit le même ensemble d’options d’arrêt prises en charge par la méthode Win32Shutdown dans Win32 \_ OperatingSystem, mais elle vous permet également de spécifier des commentaires, une raison d’arrêt ou un délai d’attente.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Méthode Win32ShutdownTracker de la classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110215"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a>Méthode Win32ShutdownTracker de la \_ classe Win32 OperatingSystem

La méthode **Win32ShutdownTracker** fournit le même ensemble d’options d’arrêt prises en charge par la méthode [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) dans [**Win32 \_ OperatingSystem**](win32-operatingsystem.md), mais elle vous permet également de spécifier des commentaires, une raison d’arrêt ou un délai d’attente.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Délai d’expiration* \[ dans\]
</dt> <dd>

Durée, en secondes, avant l’arrêt. La valeur par défaut est 0 (zéro).

</dd> <dt>

*Commentaire* \[ dans\]
</dt> <dd>

Message à afficher dans la boîte de dialogue d’arrêt, également stocké sous forme de commentaire dans l’entrée du journal des événements.

</dd> <dt>

*ReasonCode* \[ dans\]
</dt> <dd>

Raison du lancement de l’arrêt.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Jeu de balises bitmap pour arrêter l’ordinateur. Pour forcer une commande, ajoutez l’indicateur Force (4) à la valeur de la commande. L’utilisation de force conjointement à l’arrêt ou au redémarrage sur un ordinateur distant arrête immédiatement tout (y compris WMI, COM, etc.) ou redémarre l’ordinateur distant. Cela génère une valeur de retour indéterminée.

<dt>

0 (0x0)
</dt> <dd>

Fermer la session

</dd> <dt>

4 (0x4)
</dt> <dd>

Désactivation de la journalisation forcée (0 + 4)

</dd> <dt>

1 (0x1)
</dt> <dd>

Éteindre

</dd> <dt>

5 (0x5)
</dt> <dd>

Arrêt forcé (1 + 4)

</dd> <dt>

2 (0X2)
</dt> <dd>

Reboot

</dd> <dt>

6 (0x6)
</dt> <dd>

Redémarrage forcé (2 + 4)

</dd> <dt>

8 (0x8)
</dt> <dd>

Mise hors tension

</dd> <dt>

12 (0xC)
</dt> <dd>

Mise hors tension forcée (8 + 4)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](../wmisdk/wmi-error-constants.md) ou [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](../debug/system-error-codes.md).

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Autre** (1 à 4294967295)
</dt> </dl>

## <a name="remarks"></a>Notes

Le processus appelant doit avoir le privilège **se \_ arrêter le \_ nom** .

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant décrit comment appeler **Win32ShutdownTracker**.


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
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

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> <dt>

[**\_OperatingSystem Win32**](win32-operatingsystem.md)
</dt> <dt>

[**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
