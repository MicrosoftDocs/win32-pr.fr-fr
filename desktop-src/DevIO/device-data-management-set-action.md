---
description: Définissez l’ensemble d’actions pour le \_ Code de contrôle de gestion des attributs du jeu de données du stockage IOCTL \_ \_ \_ \_ .
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114385"
---
# <a name="device_data_management_set_action"></a>ACTION de définition de la \_ gestion des données d’appareil \_ \_ \_

Les valeurs constantes suivantes représentent l’ensemble des valeurs possibles pour le type d’action de définition de la gestion des données de l’appareil, qui est défini en tant que type **DWORD**. **\_ \_ \_ \_**

<dl> <dt>

<span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ aucun**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Aucune action n’est effectuée.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Une action de suppression est effectuée.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**\_Notification DeviceDsmAction**
</dt> <dd> <dl> <dt>

2 \| **DeviceDsmActionFlag non \_ destructif** (0x80000002)
</dt> <dt>



Une action de notification est effectuée. Les paramètres se trouvent dans une structure de [**paramètres de notification de DSM d’appareil \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) . Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction \_ OffloadRead**
</dt> <dd> <dl> <dt>

3 \| **DeviceDsmActionFlag non \_ destructif** (0x80000003)
</dt> <dt>



Une action de lecture de déchargement est effectuée. Les paramètres se trouvent dans une structure de [**\_ paramètres de \_ \_ lecture \_ de déchargement de DSM d’appareil**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) . La sortie se trouve dans une structure de [**\_ sortie de \_ lecture \_ de déchargement de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) . Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.

**Windows 7 et Windows Server 2008 R2 :** cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction \_ OffloadWrite**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Une action d’écriture de déchargement est effectuée. Les paramètres se trouvent dans une structure de [**\_ paramètres d' \_ \_ écriture \_ de déchargement de DSM d’appareil**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) . La sortie se trouve dans une structure de [**\_ sortie d' \_ écriture \_ de déchargement de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) .

**Windows 7 et Windows Server 2008 R2 :** cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**\_Allocation DeviceDsmAction**
</dt> <dd> <dl> <dt>

5 \| **DeviceDsmActionFlag non \_ destructif** (0x80000005)
</dt> <dt>



Une bitmap d’allocation est retournée pour la première plage de jeux de données passée. La sortie est dans une structure d' [**\_ \_ \_ \_ \_ État de provisionnement du jeu de données d’appareil**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) . Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.

**Windows 7 et Windows Server 2008 R2 :** cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**Réparation de DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

6 \| **DeviceDsmActionFlag non \_ destructif** (0x80000006)
</dt> <dt>



Une action de réparation est effectuée. Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.

**Windows 7 et Windows Server 2008 R2 :** cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**\_Nettoyage DeviceDsmAction**
</dt> <dd> <dl> <dt>

7 \| **DeviceDsmActionFlag non \_ destructif** (0x80000007)
</dt> <dt>



Une action de nettoyage est effectuée. Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.

**Windows 7 et Windows Server 2008 R2 :** cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**Résilience DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

8 \| **DeviceDsmActionFlag non \_ destructif** (0x80000008)
</dt> <dt>



Une action de résilience est effectuée. Le **DeviceDsmActionFlag non \_ destructif** (0x80000000) est un indicateur binaire pour indiquer à la pile de pilotes que cette opération n’est pas destructrice.

**Windows 7 et Windows Server 2008 R2 :** cette valeur n’est pas prise en charge avant Windows 8 et Windows Server 2012.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                                         |
| En-tête<br/>                   | <dl> <dt>WinIoCtl. h (inclure Windows. h)</dt> </dl> |



 

 




