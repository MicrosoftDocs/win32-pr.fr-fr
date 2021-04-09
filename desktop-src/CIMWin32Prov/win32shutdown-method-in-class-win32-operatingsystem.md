---
description: Win32Shutdown &\# 8194 ; La méthode de classe WMI fournit l’ensemble complet d’options d’arrêt prises en charge par les systèmes d’exploitation Win32. Celles-ci incluent la fermeture, l’arrêt, le redémarrage et le forçage d’une déconnexion, d’un arrêt ou d’un redémarrage.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Méthode Win32Shutdown de la classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861570"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a>Méthode Win32Shutdown de la \_ classe Win32 OperatingSystem

La méthode de   [classe WMI](../wmisdk/retrieving-a-class.md) **Win32Shutdown** fournit l’ensemble complet d’options d’arrêt prises en charge par les systèmes d’exploitation Win32. Celles-ci incluent la fermeture, l’arrêt, le redémarrage et le forçage d’une déconnexion, d’un arrêt ou d’un redémarrage.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](../wmisdk/calling-a-method.md).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Jeu de balises bitmap pour arrêter l’ordinateur. Pour forcer une commande, ajoutez l’indicateur Force (4) à la valeur de la commande. L’utilisation de force conjointement à l’arrêt ou au redémarrage sur un ordinateur distant arrête immédiatement tout (y compris WMI, COM, etc.) ou redémarre l’ordinateur distant. Cela génère une valeur de retour indéterminée.

<dt>

0 (0x0)
</dt> <dd>

**Déconnecter** : déconnecte l’utilisateur de l’ordinateur. La fermeture de session arrête tous les processus associés au contexte de sécurité du processus qui a appelé la fonction EXIT, journalise l’utilisateur actuel du système et affiche la boîte de dialogue d’ouverture de session.

</dd> <dt>

4 (0x4)
</dt> <dd>

**Fermeture de session forcée (0 + 4)** : déconnecte immédiatement l’utilisateur de l’ordinateur et ne notifie pas les applications de la fin de l’ouverture de session. Cela peut entraîner une perte de données.

</dd> <dt>

1 (0x1)
</dt> <dd>

**Shutdown** : arrête l’ordinateur jusqu’à un point où il est possible de le mettre hors tension. (Toutes les mémoires tampons de fichiers sont vidées sur le disque et tous les processus en cours d’exécution sont arrêtés.) Les utilisateurs voient le message, `It is now safe to turn off your computer.`

Pendant l’arrêt, le système envoie un message à chaque application en cours d’exécution. Les applications effectuent un nettoyage lors du traitement du message et retournent la valeur true pour indiquer qu’elles peuvent être arrêtées.

</dd> <dt>

5 (0x5)
</dt> <dd>

**Arrêt forcé (1 + 4)** : arrête l’ordinateur jusqu’à un point où il est possible de le mettre hors tension. (Toutes les mémoires tampons de fichiers sont vidées sur le disque et tous les processus en cours d’exécution sont arrêtés.) Les utilisateurs voient le message,` It is now safe to turn off your computer.`

Lorsque l’approche d’arrêt forcé est utilisée, tous les services, y compris WMI, sont arrêtés immédiatement. Pour cette raison, vous ne serez pas en mesure de recevoir une valeur de retour si vous exécutez le script sur un ordinateur distant.

</dd> <dt>

2 (0X2)
</dt> <dd>

**Redémarrer** : arrête puis redémarre l’ordinateur.

</dd> <dt>

6 (0x6)
</dt> <dd>

**Redémarrage forcé (2 + 4)** : arrête puis redémarre l’ordinateur.

Lorsque l’approche de redémarrage forcé est utilisée, tous les services, y compris WMI, sont arrêtés immédiatement. Pour cette raison, vous ne serez pas en mesure de recevoir une valeur de retour si vous exécutez le script sur un ordinateur distant.

</dd> <dt>

8 (0x8)
</dt> <dd>

**Mettre hors** tension : arrête l’ordinateur et éteint l’alimentation (si elle est prise en charge par l’ordinateur en question).

</dd> <dt>

12 (0xC)
</dt> <dd>

**Mise hors tension forcée (8 + 4)** : arrête l’ordinateur et désactive l’alimentation (si elle est prise en charge par l’ordinateur en question).

Lorsque l’approche de mise hors tension forcée est utilisée, tous les services, y compris WMI, sont arrêtés immédiatement. Pour cette raison, vous ne serez pas en mesure de recevoir une valeur de retour si vous exécutez le script sur un ordinateur distant.

</dd> </dl> </dd> <dt>

*Réservé* \[ dans\]
</dt> <dd>

Un moyen d’étendre **Win32Shutdown**. Actuellement, le paramètre *réservé* est ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](../wmisdk/wmi-error-constants.md) ou [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](../debug/system-error-codes.md).

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Autre** (1 à 4294967295)
</dt> </dl>

## <a name="remarks"></a>Notes

Pour une gestion plus efficace des ordinateurs d’une organisation, les administrateurs doivent pouvoir arrêter ou redémarrer un ordinateur à distance, ou pour fermer la session à distance d’un utilisateur. La possibilité d’effectuer ces tâches permet aux administrateurs d’installer des logiciels, de reconfigurer les paramètres de l’ordinateur, de supprimer des ordinateurs du réseau et d’effectuer d’autres tâches sans avoir à arrêter ou redémarrer manuellement chaque ordinateur.

Par exemple, pour effectuer une mise à niveau du réseau, vous devrez peut-être arrêter tous les ordinateurs qui s’exécutent sur un segment de réseau particulier. Pour forcer une mise à niveau stratégie de groupe, vous devez déconnecter les utilisateurs de leur ordinateur. Si un virus informatique est présent n’importe où dans votre organisation, vous souhaiterez peut-être arrêter autant d’ordinateurs que possible, avant que le virus n’ait la possibilité de se répandre. La possibilité d’arrêter et de redémarrer les ordinateurs et de se déconnecter des utilisateurs par programmation plutôt que manuellement peut être un économiseur de temps énorme.

Le processus appelant doit avoir le privilège **se \_ arrêter le \_ nom** .

La méthode [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) fournit le même ensemble d’options d’arrêt prises en charge par la méthode **Win32Shutdown** dans [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) , mais elle vous permet également de spécifier des commentaires, une raison d’arrêt ou un délai d’attente.

La méthode Win32Shutdown n’a pas de paramètre pour verrouiller une station de travail, ce qui laisse l’utilisateur ouvert une session. Toutefois, les stations de travail peuvent être verrouillées à partir de la ligne de commande à l’aide de la commande suivante :

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a>Exemples

L’exemple VBScript de [déconnexion, de redémarrage ou d’arrêt de plusieurs ordinateurs](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) de la Galerie TechNet utilise Win32Shutdown pour la fermeture de session, l’arrêt, le redémarrage ou la mise hors tension (selon la sélection) des ordinateurs figurant dans le groupe de serveurs.

L’exemple [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell sur la Galerie TechNet comprend une méthode qui appelle Win32Shutdown sur un ordinateur distant.

L’exemple PowerShell suivant utilise la méthode Win32Shutdown pour arrêter l’ordinateur spécifié.


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



L’exemple de code PowerShell suivant utilise le EnableAllPrivileges de l’applet de commande de l’applet de commande pour obtenir les droits appropriés.


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



L’exemple de code VB.NET suivant utilise la méthode Shutdown pour redémarrer ou déconnecter un système.


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

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

[**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[Tâches WMI : gestion des postes de travail](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[Exécution d’opérations privilégiées à l’aide de VBScript](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
