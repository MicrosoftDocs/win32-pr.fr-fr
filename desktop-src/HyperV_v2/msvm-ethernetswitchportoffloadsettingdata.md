---
description: Représente les données de paramètre de la fonctionnalité de déchargement de port.
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Classe Msvm_EthernetSwitchPortOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddf58a10e85003a00e0d757f29db55a49f98f0ba22e8c3124b83a593f2a3908f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148298"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a>MSVM \_ EthernetSwitchPortOffloadSettingData, classe

Représente les données de paramètre de la fonctionnalité de déchargement de port.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ EthernetSwitchPortOffloadSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ EthernetSwitchPortOffloadSettingData** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. cette propriété est héritée de [**CIM \_ propriété managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Ethernet Switch Port Offload Paramètres ».

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « représente le paramètre de fonctionnalité de déchargement de port données. ».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. cette propriété est héritée de [**CIM \_ propriété managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Ethernet Switch Port Offload Paramètres ».

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**IOVInterruptModeration**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Valeur de modération de l’interruption pour le déchargement des e/s (IOV). La valeur par défaut est 0.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valeur par défaut** (0)


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

**Adaptative** (1)


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Désactivé** (2)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Faible** (100)


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

**Moyenne** (200)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Élevé** (300)


</dt> <dd></dd> </dl>

</dd> <dt>

**IOVOffloadWeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Poids affecté à ce port pour le déchargement des e/s de virtualisation (IOV). Le poids est l’importance relative lors de l’affectation de ressources IOV. L’affectation de la valeur 0 à la propriété **IOVOffloadWeight** désactive le déchargement IOV sur le port. La valeur par défaut est 0.

</dd> <dt>

**IOVQueuePairsRequested**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Nombre de paires de files d’attente demandées pour ce port pour le déchargement des e/s (IOV). La valeur par défaut est 1.

</dd> <dt>

**IPSecOffloadLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Nombre maximal d’emplacements de déchargement d’association de sécurité (SA) autorisés à partir du port.

</dd> <dt>

**PacketDirectModerationCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Valeur du nombre de modération des interruptions pour Packet direct (PD). La valeur par défaut est 0.

> [!Note]  
> Propriété ajoutée dans Windows 10.

 

</dd> <dt>

**PacketDirectModerationInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Valeur de l’intervalle de modération des interruptions pour Packet direct (PD). La valeur par défaut est 0.

> [!Note]  
> Propriété ajoutée dans Windows 10.

 

</dd> <dt>

**PacketDirectNumProcs**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Nombre de processeurs utilisés par l’hôte pour traiter les paquets envoyés à partir de ce port en mode paquet direct. La valeur par défaut est 1.

> [!Note]  
> Propriété ajoutée dans Windows 10.

 

</dd> <dt>

**VmmqEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Activez le déchargement VMMQ s’il est pris en charge par le matériel. La valeur par défaut est false.

> [!Note]  
> cette propriété a été ajoutée dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

**VmmqQueuePairs**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Nombre de files d’attente à allouer lorsque VRSS est activé. La valeur par défaut est 16.

> [!Note]  
> cette propriété a été ajoutée dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

**VMQOffloadWeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Poids attribué à ce port pour le déchargement de la file d’attente d’ordinateurs virtuels. Le poids est l’importance relative lors de l’affectation de ressources d’ordinateurs virtuels. Si vous affectez la valeur 0 à la propriété **VMQOffloadWeight** , la valeur de la propriété de l’ordinateurs virtuels est désactivée La valeur par défaut est 100.

</dd> <dt>

**VrssEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Activez VRSS. La valeur par défaut est true.

> [!Note]  
> cette propriété a été ajoutée dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

**VrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Indique s’il faut exclure le processeur d’ordinateurs virtuels principal de la table d’indirection VRSS lorsque VRSS est activé. La valeur par défaut est false.

> [!Note]  
> ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**VrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Indique s’il faut toujours exécuter VRSS côté hôte lorsque VRSS est activé, quel que soit le paramètre RSS de la carte réseau virtuelle. La valeur par défaut est false.

> [!Note]  
> ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**VrssMinQueuePairs**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Nombre minimal de files d’attente à allouer lorsque VRSS est activé. La valeur par défaut est 1.

> [!Note]  
> ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**VrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Mode de planification de la file d’attente à utiliser lorsque le VRSS est activé. La valeur par défaut est la planification statique.

> [!Note]  
> ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**VrssVmbusChannelAffinityPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Stratégie d’affinité du canal VMBus à utiliser lorsque le paramètre VRSS est activé. La valeur par défaut est Strong.

> [!Note]  
> ajouté dans Windows 10, version 1709.

 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

