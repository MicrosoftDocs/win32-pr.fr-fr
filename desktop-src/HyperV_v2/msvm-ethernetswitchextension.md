---
description: Représente une instance d’un composant d’extension lié à un commutateur Ethernet virtuel.
ms.assetid: 5b3e26e3-4cb9-47c9-865e-2f3232bbfc8e
title: Classe Msvm_EthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtension
- Msvm_EthernetSwitchExtension.InstanceID
- Msvm_EthernetSwitchExtension.Caption
- Msvm_EthernetSwitchExtension.Description
- Msvm_EthernetSwitchExtension.ElementName
- Msvm_EthernetSwitchExtension.InstallDate
- Msvm_EthernetSwitchExtension.OperationalStatus
- Msvm_EthernetSwitchExtension.StatusDescriptions
- Msvm_EthernetSwitchExtension.Status
- Msvm_EthernetSwitchExtension.HealthState
- Msvm_EthernetSwitchExtension.CommunicationStatus
- Msvm_EthernetSwitchExtension.DetailedStatus
- Msvm_EthernetSwitchExtension.OperatingStatus
- Msvm_EthernetSwitchExtension.PrimaryStatus
- Msvm_EthernetSwitchExtension.EnabledState
- Msvm_EthernetSwitchExtension.OtherEnabledState
- Msvm_EthernetSwitchExtension.RequestedState
- Msvm_EthernetSwitchExtension.EnabledDefault
- Msvm_EthernetSwitchExtension.TimeOfLastStateChange
- Msvm_EthernetSwitchExtension.AvailableRequestedStates
- Msvm_EthernetSwitchExtension.TransitioningToState
- Msvm_EthernetSwitchExtension.SystemCreationClassName
- Msvm_EthernetSwitchExtension.SystemName
- Msvm_EthernetSwitchExtension.CreationClassName
- Msvm_EthernetSwitchExtension.Name
- Msvm_EthernetSwitchExtension.ExtensionType
- Msvm_EthernetSwitchExtension.Vendor
- Msvm_EthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a6d760737ded1a12cf369ccb3a46595627d8e38e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531232"
---
# <a name="msvm_ethernetswitchextension-class"></a>MSVM \_ EthernetSwitchExtension, classe

Représente une instance d’un composant d’extension lié à un commutateur Ethernet virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtension : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption = "Virtual Switch Extension";
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchExtension";
  string   Name;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ EthernetSwitchExtension** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ EthernetSwitchExtension** possède ces méthodes.



| Méthode                                                                        | Description                         |
|:------------------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-ethernetswitchextension-requeststatechange.md) | Demande un changement d’État.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **MSVM \_ EthernetSwitchExtension** possède les propriétés suivantes.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État. Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)). Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel. Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.

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

Brève description de l’objet. Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « extension de commutateur virtuel ».

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance. Cette propriété a toujours la valeur « MSVM \_ EthernetSwitchExtension ».

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

Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et sera l’une des valeurs suivantes.

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

États activés et désactivés d’un élément. Cette propriété peut également indiquer les transitions entre ces États demandés. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).



| Valeur                                                                                                                                                                                                                                                                       | Signification                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Inconnu**</dt> <dt>0</dt> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Autre**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Activé**</dt> <dt>2</dt> </dl>                                                 | L’élément est ou peut exécuter des commandes, traite toutes les commandes mises en file d’attente et met en file d’attente les nouvelles requêtes.<br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Désactivé**</dt> <dt>3</dt> </dl>                                             | L’élément n’exécutera pas de commande et supprimera toutes les nouvelles demandes.<br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Arrêt**</dt> de <dt>4</dt> </dl>                         | L’élément est en cours de passage à un état désactivé.<br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicable**</dt> <dt>5</dt> </dl>                     | L’élément ne prend pas en charge l’activation ou la désactivation.<br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Activé mais hors connexion**</dt> <dt>6</dt> </dl> | L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.<br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**Dans le test**</dt> <dt>7</dt> </dl>                                                 | L’élément est dans un état de test.<br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Différé**</dt> <dt>8</dt> </dl>                                             | L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.<br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Suspension**</dt> <dt>9</dt> </dl>                                                 | L’élément est activé, mais en mode restreint. Le comportement de l’élément est similaire à l’état activé, mais ne traite qu’un ensemble restreint de commandes. Toutes les autres demandes sont mises en file d’attente.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> À <dt>**partir**</dt> de <dt>10</dt> </dl>                                            | L’élément est en train d’accéder à un état activé. Les nouvelles demandes sont mises en file d’attente.<br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF réservé**</dt> <dt>11 32767</dt> </dl>                  | Réservé.<br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Fournisseur réservé**</dt> <dt>32768 65535</dt> </dl>       | Réservé.<br/>                                                                                                                                                                                        |



 

</dd> <dt>

**ExtensionType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le type du composant d’extension.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

**Capture** (1)


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

**Filtre** (2)


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

**Transfert** (3)


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

**Analyse** (4)


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

**Natif** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’intégrité actuelle de l’élément. Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.

Lorsqu’une erreur critique se produit, consultez le journal des événements pour plus d’informations. La propriété **EnabledState** peut également contenir plus d’informations. Par exemple, lorsque l’espace disque est très faible, **HealthState** est défini sur 25, l’ordinateur virtuel s’interrompt et **EnabledState** a la valeur 32768 (suspendu).

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).



| Valeur                                                                                                                                                                                                                                                            | Signification                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>5</dt> </dl>                                                                               | L’élément est entièrement fonctionnel et fonctionne dans des paramètres opérationnels normaux et sans erreur.<br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Erreur majeure**</dt> <dt>20</dt> </dl>             | L’élément a subi un échec majeur.<br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Erreur critique**</dt> <dt>25</dt> </dl> | L’élément n’est pas fonctionnel et la récupération n’est peut-être pas possible.<br/>                                        |



 

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création de la configuration d’ordinateur virtuel pour un ordinateur virtuel, ou **valeur null**, pour un système d’exploitation de gestion. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom unique du composant d’extension.

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

Tableau qui contient les États actuels de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre). Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations d’état de haut niveau. Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants. Une valeur **null** indique que cette propriété n’est pas implémentée. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier État demandé ou souhaité pour l’élément passé à la méthode **RequestStateChange** , ou 12 (non applicable) si aucun changement d’État n’est en cours. L’état réel de l’élément est représenté par **EnabledState**. Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui spécifie l’état de l’élément. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **arrayType** ("indexé")
</dt> </dl>

Tableau qui contient des chaînes qui décrivent les valeurs de tableau **OperationalStatus** correspondantes. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom de la classe de création du système.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom du commutateur virtuel auquel l’instance d’extension est liée.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de la dernière modification de l’état activé de l’élément. Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique l’État cible de la transition de l’instance. Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**Fournisseur**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le fournisseur qui fournit l’extension.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version de l’extension dans un format «*major*. *Minor*», par exemple « 2,0 ».

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

