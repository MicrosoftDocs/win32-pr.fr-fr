---
description: Représente le point de connexion logique d’un port de Fibre Channel.
ms.assetid: 54e9cb76-04f2-417b-b250-1b3156772694
title: Classe Msvm_FcEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcEndpoint
- Msvm_FcEndpoint.InstanceID
- Msvm_FcEndpoint.Caption
- Msvm_FcEndpoint.Description
- Msvm_FcEndpoint.ElementName
- Msvm_FcEndpoint.InstallDate
- Msvm_FcEndpoint.Name
- Msvm_FcEndpoint.OperationalStatus
- Msvm_FcEndpoint.StatusDescriptions
- Msvm_FcEndpoint.Status
- Msvm_FcEndpoint.HealthState
- Msvm_FcEndpoint.CommunicationStatus
- Msvm_FcEndpoint.DetailedStatus
- Msvm_FcEndpoint.OperatingStatus
- Msvm_FcEndpoint.PrimaryStatus
- Msvm_FcEndpoint.EnabledState
- Msvm_FcEndpoint.OtherEnabledState
- Msvm_FcEndpoint.RequestedState
- Msvm_FcEndpoint.EnabledDefault
- Msvm_FcEndpoint.TimeOfLastStateChange
- Msvm_FcEndpoint.AvailableRequestedStates
- Msvm_FcEndpoint.TransitioningToState
- Msvm_FcEndpoint.SystemCreationClassName
- Msvm_FcEndpoint.SystemName
- Msvm_FcEndpoint.CreationClassName
- Msvm_FcEndpoint.NameFormat
- Msvm_FcEndpoint.ProtocolType
- Msvm_FcEndpoint.ProtocolIFType
- Msvm_FcEndpoint.OtherTypeDescription
- Msvm_FcEndpoint.Connected
- Msvm_FcEndpoint.WWPN
- Msvm_FcEndpoint.WWNN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a49440158beffb159b2f931283cf902a21ca5c9de1addac462b494c30eec2100
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523389"
---
# <a name="msvm_fcendpoint-class"></a>MSVM \_ FcEndpoint, classe

Représente le point de connexion logique d’un port de Fibre Channel. Lorsque le point de terminaison de Fibre Channel est connecté à un port de commutateur, le port Fibre Channel connecté au point de terminaison Fibre Channel dispose d’une connectivité Fibre Channel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcEndpoint : CIM_ProtocolEndpoint
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  boolean  Connected;
  string   WWPN;
  string   WWNN;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ FcEndpoint** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ FcEndpoint** possède ces méthodes.



| Méthode                                                           | Description                         |
|:-----------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-fcendpoint-requeststatechange.md) | Demande un changement d’État.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **MSVM \_ FcEndpoint** possède les propriétés suivantes.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État. Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de la classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) . Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel. Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.

Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (.. )
</dt> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Connecté**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété a la valeur **true** si ce point de terminaison Fibre Channel est connecté activement à un autre point de terminaison de Fibre Channel.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**, **MaxLen** (256)
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée dans la création d’une instance. Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est l’une des valeurs suivantes.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’état activé du système planifié. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et peut prendre l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                       | Signification                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Désactivé**</dt> <dt>3</dt> </dl>                                             | Le système est désactivé.<br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicable**</dt> <dt>5</dt> </dl>                     | L’élément ne prend pas en charge l’activation ou la désactivation.<br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Activé mais hors connexion**</dt> <dt>6</dt> </dl> | Le système est activé, mais il est hors connexion. Toutes les nouvelles demandes seront supprimées.<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intégrité actuelle de l’élément. Cette propriété exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants. Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création de la configuration de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Étiquette par laquelle l’objet est connu. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (256)
</dt> </dl>

Contient l’heuristique d’attribution de noms sélectionnée pour garantir que la valeur de la propriété **Name** est unique. Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** . Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

États actuels de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »). Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Chaîne qui décrit le type de point de terminaison de protocole lorsque la propriété **ProtocolIFType** de cette classe (ou l’une de ses sous-classes) a la valeur 1 (autre). Cette propriété doit être définie sur **null** lorsque la propriété **ProtocolIFType** a une valeur autre que 1. Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations d’état de haut niveau. Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

La propriété est utilisée pour catégoriser et classer les instances de cette classe. Si **ProtocolIFType** a la valeur 1 (autre), les informations de type doivent être fournies dans la propriété **OtherTypeDescription** . Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

> [!Note]  
> **ProtocolIFType** est une énumération qui est synchronisée avec la [MIB ifType IANA](https://www.iana.org/assignments/ianaiftype-mib). Des valeurs supplémentaires définies par le DMTF sont également incluses.

 

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)
</dt> <dt>

<span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Normal 1822** (2)
</dt> <dt>

<span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)
</dt> <dt>

<span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X. 25** (4)
</dt> <dt>

<span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5)
</dt> <dt>

<span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)
</dt> <dt>

<span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802,3 CSMA/CD** (7)
</dt> <dt>

<span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**Bus de jetons ISO 802,4** (8)
</dt> <dt>

<span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**Token Ring ISO 802,5** (9)
</dt> <dt>

<span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802,6 Man** (10)
</dt> <dt>

<span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**Starlan** (11)
</dt> <dt>

<span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)
</dt> <dt>

<span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)
</dt> <dt>

<span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**Hyperchannel** (14)
</dt> <dt>

<span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)
</dt> <dt>

<span id="LAP-B"></span><span id="lap-b"></span>**Lap-B** (16)
</dt> <dt>

<span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)
</dt> <dt>

<span id="DS1"></span><span id="ds1"></span>**DS1** (18)
</dt> <dt>

<span id="E1"></span><span id="e1"></span>**E1** (19)
</dt> <dt>

<span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**RNIS de base** (20)
</dt> <dt>

<span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**RNIS principal** (21)
</dt> <dt>

<span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Série point à point propriétaire** (22)
</dt> <dt>

<span id="PPP"></span><span id="ppp"></span>**PPP** (23)
</dt> <dt>

<span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Bouclage logiciel** (24)
</dt> <dt>

<span id="EON"></span><span id="eon"></span>**EON** (25)
</dt> <dt>

<span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**3Mbit Ethernet** (26)
</dt> <dt>

<span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)
</dt> <dt>

<span id="SLIP"></span><span id="slip"></span>**Slip** (28)
</dt> <dt>

<span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)
</dt> <dt>

<span id="DS3"></span><span id="ds3"></span>**DS3** (30)
</dt> <dt>

<span id="SIP"></span><span id="sip"></span>**SIP** (31)
</dt> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Relais de trames** (32)
</dt> <dt>

<span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)
</dt> <dt>

<span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallèle** (34)
</dt> <dt>

<span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**Arcnet** (35)
</dt> <dt>

<span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**Arcnet plus** (36)
</dt> <dt>

<span id="ATM"></span><span id="atm"></span>**ATM** (37)
</dt> <dt>

<span id="MIO_X.25"></span><span id="mio_x.25"></span>**Mio X. 25** (38)
</dt> <dt>

<span id="SONET"></span><span id="sonet"></span>**SONET** (39)
</dt> <dt>

<span id="X.25_PLE"></span><span id="x.25_ple"></span>**X. 25 espérance** de la (40)
</dt> <dt>

<span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211 c** (41)
</dt> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)
</dt> <dt>

<span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXi** (43)
</dt> <dt>

<span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Service Frame Relay** (44)
</dt> <dt>

<span id="V.35"></span><span id="v.35"></span>**V. 35** (45)
</dt> <dt>

<span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)
</dt> <dt>

<span id="HIPPI"></span><span id="hippi"></span>**HIPPA** (47)
</dt> <dt>

<span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)
</dt> <dt>

<span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)
</dt> <dt>

<span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**Chemin d’accès SONET** (50)
</dt> <dt>

<span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)
</dt> <dt>

<span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)
</dt> <dt>

<span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Propriétaire virtuel/interne** (53)
</dt> <dt>

<span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Multiplexeur propriétaire** (54)
</dt> <dt>

<span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802,12** (55)
</dt> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)
</dt> <dt>

<span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**Interface HIPPA** (57)
</dt> <dt>

<span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Interconnexion du relais de trames** (58)
</dt> <dt>

<span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**Réseau local émulé ATM pour 802,3** (59)
</dt> <dt>

<span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**Réseau local émulé ATM pour 802,5** (60)
</dt> <dt>

<span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**Circuit émulé ATM** (61)
</dt> <dt>

<span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)
</dt> <dt>

<span id="ISDN"></span><span id="isdn"></span>**RNIS** (63)
</dt> <dt>

<span id="V.11"></span><span id="v.11"></span>**V. 11** (64)
</dt> <dt>

<span id="V.36"></span><span id="v.36"></span>**V. 36** (65)
</dt> <dt>

<span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 à 64 Ko** (66)
</dt> <dt>

<span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 à 2 Mo** (67)
</dt> <dt>

<span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)
</dt> <dt>

<span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)
</dt> <dt>

<span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Canal** (70)
</dt> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)
</dt> <dt>

<span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**Canal IBM 260/370 OEMI** (72)
</dt> <dt>

<span id="ESCON"></span><span id="escon"></span>**ESCON** (73)
</dt> <dt>

<span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Commutation des liaisons de données** (74)
</dt> <dt>

<span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**Interface RNIS S/T** (75)
</dt> <dt>

<span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**Interface RNIS U** (76)
</dt> <dt>

<span id="LAP-D"></span><span id="lap-d"></span>**Lap-D** (77)
</dt> <dt>

<span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**Commutateur IP** (78)
</dt> <dt>

<span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Pontage d’itinéraires source distants** (79)
</dt> <dt>

<span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM logique** (80)
</dt> <dt>

<span id="DS0"></span><span id="ds0"></span>**DS0** (81)
</dt> <dt>

<span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**Bundle DS0** (82)
</dt> <dt>

<span id="BSC"></span><span id="bsc"></span>**BSC** (83)
</dt> <dt>

<span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)
</dt> <dt>

<span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Radio combat net** (85)
</dt> <dt>

<span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5 r DTR** (86)
</dt> <dt>

<span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Système de rapports ext POS Loc** (87)
</dt> <dt>

<span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**Protocole d’accès à distance AppleTalk** (88)
</dt> <dt>

<span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Propriétaire sans connexion** (89)
</dt> <dt>

<span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**Bloc-notes de l’hôte ITU X. 29** (90)
</dt> <dt>

<span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**Boîtier terminal ITU X. 3** (91)
</dt> <dt>

<span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**MPI de relais de trames** (92)
</dt> <dt>

<span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X. 213** (93)
</dt> <dt>

<span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)
</dt> <dt>

<span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)
</dt> <dt>

<span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)
</dt> <dt>

<span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)
</dt> <dt>

<span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802,5 CRFP** (98)
</dt> <dt>

<span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)
</dt> <dt>

<span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Réception et transmission vocales** (100)
</dt> <dt>

<span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Office de Exchange étrangères vocales** (101)
</dt> <dt>

<span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Service de Exchange étranger vocal** (102)
</dt> <dt>

<span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Encapsulation vocale** (103)
</dt> <dt>

<span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voix sur IP** (104)
</dt> <dt>

<span id="ATM_DXI"></span><span id="atm_dxi"></span>**DXi ATM** (105)
</dt> <dt>

<span id="ATM_FUNI"></span><span id="atm_funi"></span>**FUNI ATM** (106)
</dt> <dt>

<span id="ATM_IMA"></span><span id="atm_ima"></span>**Certificat IMA ATM** (107)
</dt> <dt>

<span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**Bundle à liaisons multiples PPP** (108)
</dt> <dt>

<span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP sur CDLC** (109)
</dt> <dt>

<span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP sur la griffe** (110)
</dt> <dt>

<span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Pile à pile** (111)
</dt> <dt>

<span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Adresse IP virtuelle** (112)
</dt> <dt>

<span id="MPC"></span><span id="mpc"></span>**MPC** (113)
</dt> <dt>

<span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP sur ATM** (114)
</dt> <dt>

<span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>Carte **Token Ring ISO 802.5 j** (115)
</dt> <dt>

<span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)
</dt> <dt>

<span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)
</dt> <dt>

<span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)
</dt> <dt>

<span id="LAP-F"></span><span id="lap-f"></span>**Lap-F** (119)
</dt> <dt>

<span id="V.37"></span><span id="v.37"></span>**V. 37** (120)
</dt> <dt>

<span id="X.25_MLP"></span><span id="x.25_mlp"></span>**MLP de X. 25** (121)
</dt> <dt>

<span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X. 25 groupe de recherche** (122)
</dt> <dt>

<span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Domaine HDLC** (123)
</dt> <dt>

<span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Canal entrelacé** (124)
</dt> <dt>

<span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**canal FAST** (125)
</dt> <dt>

<span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (pour APPN HPR dans les réseaux IP)** (126)
</dt> <dt>

<span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**Couche MAC CATV** (127)
</dt> <dt>

<span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV en aval** (128)
</dt> <dt>

<span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV en amont** (129)
</dt> <dt>

<span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Commutateur 12MPP de Avalon** (130)
</dt> <dt>

<span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)
</dt> <dt>

<span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Café** (132)
</dt> <dt>

<span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Service d’émulation de circuit** (133)
</dt> <dt>

<span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>Sous- **interface ATM** (134)
</dt> <dt>

<span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**VLAN de couche 2 avec 802.1 q** (135)
</dt> <dt>

<span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Réseau local virtuel de couche 3 utilisant IP** (136)
</dt> <dt>

<span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Réseau local virtuel de couche 3 utilisant IPX** (137)
</dt> <dt>

<span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Power Line numérique** (138)
</dt> <dt>

<span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Messagerie multimédia sur IP** (139)
</dt> <dt>

<span id="DTM"></span><span id="dtm"></span>**DTM** (140)
</dt> <dt>

<span id="DCN"></span><span id="dcn"></span>**DCN** (141)
</dt> <dt>

<span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**Transfert IP** (142)
</dt> <dt>

<span id="MSDSL"></span><span id="msdsl"></span>**MSDS** (143)
</dt> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)
</dt> <dt>

<span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**If-GSN/hippai-6400** (145)
</dt> <dt>

<span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**Couche MAC-RCC-RCC** (146)
</dt> <dt>

<span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC en aval** (147)
</dt> <dt>

<span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC en amont** (148)
</dt> <dt>

<span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**Virtuel ATM** (149)
</dt> <dt>

<span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**Tunnel MPLS** (150)
</dt> <dt>

<span id="SRP"></span><span id="srp"></span>**SRP** (151)
</dt> <dt>

<span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voix sur ATM** (152)
</dt> <dt>

<span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voix sur relais de trame** (153)
</dt> <dt>

<span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)
</dt> <dt>

<span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Lien composite** (155)
</dt> <dt>

<span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**Lien de signalisation SS7** (156)
</dt> <dt>

<span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Sans fil P2P propriétaire** (157)
</dt> <dt>

<span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Image vers l’avant** (158)
</dt> <dt>

<span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol sur ATM** (159)
</dt> <dt>

<span id="USB"></span><span id="usb"></span>**USB** (160)
</dt> <dt>

<span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**Agrégat de liens ad IEEE 802.3** (161)
</dt> <dt>

<span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**Gestion des stratégies BGP** (162)
</dt> <dt>

<span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink fr** (163)
</dt> <dt>

<span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**Gatekeeper H. 323** (164)
</dt> <dt>

<span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**Proxy H. 323** (165)
</dt> <dt>

<span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)
</dt> <dt>

<span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Lien de signalisation à plusieurs fréquences** (167)
</dt> <dt>

<span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)
</dt> <dt>

<span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)
</dt> <dt>

<span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**Liaison de données de l’installation DS1** (170)
</dt> <dt>

<span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Paquet sur SONET/SDH** (171)
</dt> <dt>

<span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**Entrée DVB-ASI** (172)
</dt> <dt>

<span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**Sortie DVB-ASI** (173)
</dt> <dt>

<span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Ligne électrique** (174)
</dt> <dt>

<span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Signal non associé à une installation** (175)
</dt> <dt>

<span id="TR008"></span><span id="tr008"></span>**TR008** (176)
</dt> <dt>

<span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)
</dt> <dt>

<span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)
</dt> <dt>

<span id="ISUP"></span><span id="isup"></span>**ISUP** (179)
</dt> <dt>

<span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Couche Mac sans fil propriétaire** (180)
</dt> <dt>

<span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>En **aval sans fil propriétaire** (181)
</dt> <dt>

<span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Flux de communication sans fil propriétaire** (182)
</dt> <dt>

<span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HiperLAN type 2** (183)
</dt> <dt>

<span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Point d’accès sans fil haut débit propriétaire sur multipoint** (184)
</dt> <dt>

<span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**Canal de surcharge SONET** (185)
</dt> <dt>

<span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Canal de surcharge du wrapper numérique** (186)
</dt> <dt>

<span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**Couche d’adaptation ATM 2** (187)
</dt> <dt>

<span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Mac radio** (188)
</dt> <dt>

<span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**Radio ATM** (189)
</dt> <dt>

<span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Trunk inter-machine** (190)
</dt> <dt>

<span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)
</dt> <dt>

<span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long lecture DSL** (192)
</dt> <dt>

<span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Point de terminaison DLCI de relais de trame** (193)
</dt> <dt>

<span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**Point de terminaison VCI ATM** (194)
</dt> <dt>

<span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Canal optique** (195)
</dt> <dt>

<span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Transport optique** (196)
</dt> <dt>

<span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**ATM propriétaire** (197)
</dt> <dt>

<span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Câble vocal** (198)
</dt> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**InfiniBand** (199)
</dt> <dt>

<span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**Lien te** (200)
</dt> <dt>

<span id="Q.2931"></span><span id="q.2931"></span>**Q. 2931** (201)
</dt> <dt>

<span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Groupe Trunk virtuel** (202)
</dt> <dt>

<span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**Groupe SIP Trunk** (203)
</dt> <dt>

<span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**Signalisation SIP** (204)
</dt> <dt>

<span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**Canal CATV en amont** (205)
</dt> <dt>

<span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)
</dt> <dt>

<span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155MB PON** (207)
</dt> <dt>

<span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622MB PON** (208)
</dt> <dt>

<span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Pont transparent** (209)
</dt> <dt>

<span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Groupe de lignes** (210)
</dt> <dt>

<span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Groupe de fonctionnalités de & vocal** (211)
</dt> <dt>

<span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voix FGD eana** (212)
</dt> <dt>

<span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voix** (213)
</dt> <dt>

<span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**Transport MPEG** (214)
</dt> <dt>

<span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6to4** (215)
</dt> <dt>

<span id="GTP"></span><span id="gtp"></span>**GTP** (216)
</dt> <dt>

<span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)
</dt> <dt>

<span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)
</dt> <dt>

<span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Groupe de canaux optiques** (219)
</dt> <dt>

<span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)
</dt> <dt>

<span id="GFP"></span><span id="gfp"></span>**GFP** (221)
</dt> <dt>

<span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)
</dt> <dt>

<span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)
</dt> <dt>

<span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**FCIP** (224)
</dt> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA réservé** (225.. 4095)
</dt> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)
</dt> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)
</dt> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)
</dt> <dt>

<span id="IPX"></span><span id="ipx"></span>**IPX** (4099)
</dt> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)
</dt> <dt>

<span id="SNA"></span><span id="sna"></span>**SNA** (4101)
</dt> <dt>

<span id="CONP"></span><span id="conp"></span>**CONP** (4102)
</dt> <dt>

<span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)
</dt> <dt>

<span id="VINES"></span><span id="vines"></span>**Vignes** (4104)
</dt> <dt>

<span id="XNS"></span><span id="xns"></span>**XNS** (4105)
</dt> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**Point de terminaison de canal B RNIS** (4106)
</dt> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**Point de terminaison de canal D RNIS** (4107)
</dt> <dt>

<span id="BGP"></span><span id="bgp"></span>**BGP** (4108)
</dt> <dt>

<span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)
</dt> <dt>

<span id="UDP"></span><span id="udp"></span>**UDP** (4110)
</dt> <dt>

<span id="TCP"></span><span id="tcp"></span>**TCP** (4111)
</dt> <dt>

<span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112)
</dt> <dt>

<span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113)
</dt> <dt>

<span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114)
</dt> <dt>

<span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115)
</dt> <dt>

<span id="NFS"></span><span id="nfs"></span>**NFS** (4200)
</dt> <dt>

<span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)
</dt> <dt>

<span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)
</dt> <dt>

<span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)
</dt> <dt>

<span id="HTTP"></span><span id="http"></span>**Http** (4204)
</dt> <dt>

<span id="FTP"></span><span id="ftp"></span>**FTP** (4205)
</dt> <dt>

<span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)
</dt> <dt>

<span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)
</dt> <dt>

<span id="SSH"></span><span id="ssh"></span>**SSH** (4401)
</dt> <dt>

<span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)
</dt> <dt>

<span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)
</dt> <dt>

<span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)
</dt> <dt>

<span id="RDP"></span><span id="rdp"></span>**RDP** (4405)
</dt> <dt>

<span id="HTTPS"></span><span id="https"></span>**Https** (4406)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (32768.. )
</dt> </dl>

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est déconseillée à la place de la propriété **ProtocolIFType** . Cette propriété est héritée de l' [**\_ ProtocolEndpoint CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier État demandé ou souhaité pour le service de gestion. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).



| Valeur                                                                         | Signification                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Non applicable.<br/> |



 

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décrit l’état de l’élément. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

OK

Erreurs

Détérioré

Connue

« Échec prévu »

Démarr

Arrêt

Services

Trop sollicité

« Non récupéré »

« Aucun contact »

« Comm. perdue »

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** . Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe de création du système d’hébergement. Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**, **MaxLen** (256)
</dt> </dl>

Nom du système d’hébergement. Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de la dernière modification de l’état activé de l’élément. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas prise en charge.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique l’État cible de la transition de l’instance. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**WWNN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de nœud WWPN du port Fibre Channel auquel ce point de terminaison est connecté.

</dd> <dt>

**WWPN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom WWN du port Fibre Channel auquel ce point de terminaison est connecté.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

