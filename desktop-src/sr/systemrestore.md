---
title: SystemRestore, classe
description: Fournit des méthodes pour désactiver et activer la surveillance, répertorier les points de restauration disponibles et initialiser une restauration sur le système local.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Restauration du système de la classe SystemRestore
- Restauration du système de la classe SystemRestore, Description
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032983"
---
# <a name="systemrestore-class"></a>SystemRestore, classe

Fournit des méthodes pour désactiver et activer la surveillance, répertorier les points de restauration disponibles et initialiser une restauration sur le système local.

## <a name="syntax"></a>Syntaxe

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a>Membres

La classe **SystemRestore** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **SystemRestore** possède ces méthodes.



| Méthode                                                             | Description                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [**CreateRestorePoint**](createrestorepoint-systemrestore.md)     | Crée un point de restauration.<br/>                         |
| [**Désactiver**](disable-systemrestore.md)                           | Désactive la surveillance sur un lecteur particulier.<br/>       |
| [**Activer**](enable-systemrestore.md)                             | Active la surveillance sur un lecteur particulier.<br/>        |
| [**GetLastRestoreStatus**](getlastrestorestatus-systemrestore.md) | Récupère l’état de la dernière restauration du système.<br/> |
| [**Restaurer**](restore-systemrestore.md)                           | Lance une restauration du système.<br/>                      |



 

### <a name="properties"></a>Propriétés

La classe **SystemRestore** possède les propriétés suivantes.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Heure à laquelle le changement d’État s’est produit.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Description à afficher pour permettre à l’utilisateur d’identifier facilement un point de restauration. La longueur maximale d’une chaîne ANSI est la valeur \_ desc max. La longueur maximale d’une chaîne Unicode est le nombre maximal de \_ desc \_ W. Pour plus d’informations, consultez [texte de description du point de restauration](restore-point-description-text.md).

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Type de l'événement. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**Commencer \_ \_ \_ Modification système imbriquée**</dt> <dt>102</dt> </dl> | Une modification du système a commencé. Un appel imbriqué suivant ne crée pas de nouveau point de restauration. <br/> Les appels suivants doivent utiliser la fin du \_ \_ \_ changement de système imbriqué, pas la modification du système de fin \_ \_ .<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**Commencer \_ \_Modification système**</dt> <dt>100</dt> </dl>                       | Une modification du système a commencé.<br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**Fin \_ \_ \_ Modification système imbriquée**</dt> <dt>103</dt> </dl>       | Une modification du système s’est terminée.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**Fin \_ \_Modification système**</dt> <dt>101</dt> </dl>                             | Une modification du système s’est terminée.<br/>                                                                                                                                                           |



 

</dd> <dt>

**RestorePointType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Type de point de restauration. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                          | Signification                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**Application \_ INSTALLER**</dt> <dt>0</dt> </dl>         | Une application a été installée.<br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**Application \_ Désinstaller**</dt> <dt>1</dt> </dl>   | Une application a été désinstallée.<br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**Annulé \_ OPÉRATION**</dt> <dt>13</dt> </dl>        | Une application doit supprimer le point de restauration créé. Par exemple, une application utilise cet indicateur lorsqu’un utilisateur annule une installation. <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**Appareil mobile \_ \_Installation du pilote**</dt> <dt>10</dt> </dl> | Un pilote de périphérique a été installé.<br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**Modifier \_ PARAMÈTRES**</dt> <dt>12</dt> </dl>                    | Des fonctionnalités ont été ajoutées ou supprimées pour une application.<br/>                                                                                                  |



 

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Numéro de séquence du point de restauration.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous pouvez obtenir une liste de points de restauration à l’aide de la méthode [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) pour récupérer une collection d’objets **SystemRestore** . Vous pouvez utiliser les propriétés de la classe pour identifier le point de restauration.

## <a name="examples"></a>Exemples

L’exemple de script suivant énumère les points de restauration actuels.


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
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

[Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

