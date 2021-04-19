---
description: Représente les paramètres de déchargement du commutateur.
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Classe Msvm_EthernetSwitchHardwareOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ef0e22143ffd424ee3acee616504e45d8125bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543140"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a>MSVM \_ EthernetSwitchHardwareOffloadSettingData, classe

Représente les paramètres de déchargement du commutateur.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ EthernetSwitchHardwareOffloadSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ EthernetSwitchHardwareOffloadSettingData** possède les propriétés suivantes.

<dl> <dt>

**DefaultQueueVmmqEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Spécifie les paramètres VMMQ pour la file d’attente par défaut du vswitch.

</dd> <dt>

**DefaultQueueVmmqQueuePairs**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Spécifie le nombre de files d’attente pour la file d’attente par défaut.

</dd> <dt>

**DefaultQueueVrssEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Spécifie les paramètres VRss pour la file d’attente par défaut du vswitch.

</dd> <dt>

**DefaultQueueVrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indique si l’UC de l’unité centrale principale est exclue de la table d’indirection VRSS/VMMQ.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**DefaultQueueVrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indique s’il faut toujours effectuer la répartition VRSS pour la file d’attente par défaut, quel que soit l’État RSS du vPort externe.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**DefaultQueueVrssMinQueuePairs**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indique le nombre minimal de files d’attente utilisées pour VRSS/VMMQ.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**DefaultQueueVrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indique comment les files d’attente VRSS/VMMQ sont directrices sur différents processeurs hôtes.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




