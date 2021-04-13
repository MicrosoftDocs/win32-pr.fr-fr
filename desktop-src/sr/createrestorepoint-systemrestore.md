---
title: Méthode CreateRestorePoint de la classe SystemRestore
description: Crée un point de restauration.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Restauration du système de méthode CreateRestorePoint
- Restauration du système de méthode CreateRestorePoint, classe SystemRestore
- Restauration du système de la classe SystemRestore, méthode CreateRestorePoint
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465594"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a>Méthode CreateRestorePoint de la classe SystemRestore

Crée un point de restauration.

Cette méthode est l’équivalent scriptable de la fonction [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Description* \[ dans\]
</dt> <dd>

Description à afficher pour permettre à l’utilisateur d’identifier facilement un point de restauration. La longueur maximale d’une chaîne ANSI est la valeur \_ desc max. La longueur maximale d’une chaîne Unicode est le nombre maximal de \_ desc \_ W. Pour plus d’informations, consultez [texte de description du point de restauration](restore-point-description-text.md).

</dd> <dt>

*RestorePointType* \[ dans\]
</dt> <dd>

Type de point de restauration. Ce membre peut être l’une des valeurs suivantes.



| Type de point de restauration                                                                                                                                                                                                                             | Signification                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**Application \_ INSTALLER**</dt> <dt>0</dt> </dl>         | Une application a été installée.<br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**Application \_ Désinstaller**</dt> <dt>1</dt> </dl>   | Une application a été désinstallée.<br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**Appareil mobile \_ \_Installation du pilote**</dt> <dt>10</dt> </dl> | Un pilote de périphérique a été installé.<br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**Modifier \_ PARAMÈTRES**</dt> <dt>12</dt> </dl>                    | Des fonctionnalités ont été ajoutées ou supprimées pour une application.<br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**Annulé \_ OPÉRATION**</dt> <dt>13</dt> </dl>        | Une application doit supprimer le point de restauration créé. Par exemple, une application utilise cet indicateur lorsqu’un utilisateur annule une installation.<br/> |



 

</dd> <dt>

*EventType* \[ dans\]
</dt> <dd>

Type de l'événement. Ce membre peut être l’une des valeurs suivantes.



| Type d'événement                                                                                                                                                                                                                                                      | Signification                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**Commencer \_ \_ \_ Modification système imbriquée**</dt> <dt>102</dt> </dl> | Une modification du système a commencé. Un appel imbriqué suivant ne crée pas de nouveau point de restauration. <br/> Les appels suivants doivent utiliser la fin du \_ \_ \_ changement de système imbriqué, pas la modification du système de fin \_ \_ .<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**Commencer \_ \_Modification système**</dt> <dt>100</dt> </dl>                       | Une modification du système a commencé. <br/> Un appel suivant doit utiliser la \_ modification du système \_ de fin, et non une \_ modification du système imbriquée \_ \_ .<br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**Fin \_ \_ \_ Modification système imbriquée**</dt> <dt>103</dt> </dl>       | Une modification du système s’est terminée.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**Fin \_ \_Modification système**</dt> <dt>101</dt> </dl>                             | Une modification du système s’est terminée.<br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, la valeur de retour est S \_ OK. Sinon, la méthode retourne l’un des codes d’erreur COM définis dans WinError. h.

## <a name="remarks"></a>Notes

* * Windows 8 : * *

Une nouvelle clé de registre permet aux développeurs d’applications de modifier la fréquence de création du point de restauration.

Les applications doivent créer cette clé pour l’utiliser, car elle n’est pas préexistante dans le système. Les éléments suivants s’appliquent par défaut si la clé n’existe pas. Si une application appelle la méthode **CreateRestorePoint** pour créer un point de restauration, Windows ignore la création de ce nouveau point de restauration si des points de restauration ont été créés au cours des dernières 24 heures. La méthode **CreateRestorePoint** retourne **S \_ OK**.

Les développeurs peuvent écrire des applications qui créent la valeur **DWORD** **SystemRestorePointCreationFrequency** sous la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. La valeur de cette clé de Registre peut modifier la fréquence de création du point de restauration. La valeur de cette clé de Registre peut modifier la fréquence de création du point de restauration.

Si l’application appelle **CreateRestorePoint** pour créer un point de restauration et que la valeur de la clé de Registre est 0, la restauration du système n’ignore pas la création du nouveau point de restauration.

Si l’application appelle **CreateRestorePoint** pour créer un point de restauration et que la valeur de la clé de Registre est l’entier N, la restauration du système ignore la création d’un nouveau point de restauration si des points de restauration ont été créés au cours des N minutes précédentes.

## <a name="examples"></a>Exemples


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                         |
| Espace de noms<br/>                | Racine \\ par défaut<br/>                                                          |
| MOF<br/>                      | <dl> <dt>SR. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





