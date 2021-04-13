---
description: Le \_ NetworkProtocol Win32&\# 8194 ; La classe WMI représente un protocole et ses caractéristiques réseau sur un système informatique Win32.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Classe Win32_NetworkProtocol
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483792"
---
# <a name="win32_networkprotocol-class"></a>\_Classe NetworkProtocol Win32

La  [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ NetworkProtocol** représente un protocole et ses caractéristiques réseau sur un système informatique Win32.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ NetworkProtocol** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ NetworkProtocol** a ces propriétés.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Brève description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ConnectionlessService**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP1 \_ sans connexion »)
</dt> </dl>

Le protocole prend en charge le service sans connexion. Un service sans connexion (datagramme) décrit un protocole de communication ou un transport dans lequel les paquets de données sont acheminés indépendamment les uns des autres et peuvent suivre différents itinéraires et arriver dans un ordre différent de celui dans lequel ils ont été envoyés. À l’inverse, un service orienté connexion fournit un circuit virtuel par le biais duquel les paquets de données sont reçus dans l’ordre dans lequel ils ont été transmis. Si la connexion entre les ordinateurs échoue, l’application est avertie.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**GuaranteesDelivery**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| Protocol \_ info \| dwServiceFlags \| XP \_ garanti \_ Delivery »)
</dt> </dl>

Le protocole prend en charge la remise des paquets de données. Si cet indicateur a la **valeur false**, il est incertain que toutes les données envoyées atteindront la destination prévue.

</dd> <dt>

**GuaranteesSequencing**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ \_ ordre garanti »)
</dt> </dl>

Le protocole permet de s’assurer que les données arrivent dans l’ordre dans lequel elles ont été envoyées. N’oubliez pas que cette caractéristique ne garantit pas la distribution des données, mais uniquement leur ordre.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

Indique le moment où l’objet a été installé. L’absence de valeur n’indique pas que l’objet n’est pas installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**MaximumAddressSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| iMaxSockAddr »), [**unités**](../wmisdk/standard-qualifiers.md) (« caractères »)
</dt> </dl>

Longueur maximale d’une adresse de socket prise en charge par le protocole. Les adresses de socket peuvent être des éléments tels qu’une URL ( `www.microsoft.com` ) ou une adresse IP ( `130.215.24.1` ).

</dd> <dt>

**MaximumMessageSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwMessageSize »), [**unités**](../wmisdk/standard-qualifiers.md) (« caractères »)
</dt> </dl>

Taille maximale des messages prise en charge par le protocole. Il s’agit de la taille maximale d’un message qui peut être envoyé ou reçu par l’hôte. Pour les protocoles qui ne prennent pas en charge le tramage de message, la taille maximale réelle d’un message qui peut être envoyé à une adresse donnée peut être inférieure à cette valeur.

</dd> <dt>

**MessageOriented**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ \_ orienté message »)
</dt> </dl>

Le protocole est orienté message. Un protocole orienté message utilise des paquets de données pour transférer des informations. À l’inverse, les protocoles orientés flux transfèrent les données sous la forme d’un flux continu d’octets.

</dd> <dt>

**MinimumAddressSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| iMinSockAddr »), [**unités**](../wmisdk/standard-qualifiers.md) (« caractères »)
</dt> </dl>

Longueur minimale d’une adresse de socket prise en charge par le protocole.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets structures \| Protocol \_ info \| lpProtocol")
</dt> </dl>

Nom du protocole.

Exemple : « TCP/IP »

</dd> <dt>

**PseudoStreamOriented**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ Pseudo \_ Stream »)
</dt> </dl>

Le protocole est un protocole orienté message qui peut recevoir des paquets de données de longueur variable ou des données diffusées en continu pour toutes les opérations de réception. Cette capacité facultative est utile lorsqu’une application ne souhaite pas que le protocole trame des messages et nécessite des caractéristiques orientées flux. Si la **valeur est true**, le protocole est Pseudo-orienté en flux continu.

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Chaîne qui indique l’état actuel de l’objet. L’état opérationnel et non opérationnel peut être défini. L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ». « Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).

L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ». Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Les valeurs sont notamment les suivantes :

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (« OK »)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erreur** (« erreur »)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Détérioré** (« détérioré »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Échec** prévu (« échec prédit »)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Démarrage** en cours (« démarrage »)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arrêt** en cours (« arrêt »)


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** (« service »)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** (« stressed »)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Non **récupéré** (« non récupéré »)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Aucun contact** (« aucun contact »)


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Communication perdue** (« inversée comm »)


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsBroadcasting**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ prend en charge la \_ diffusion »)
</dt> </dl>

Le protocole prend en charge un mécanisme de diffusion des messages sur le réseau.

</dd> <dt>

**SupportsConnectData**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ Connect \_ Data »)
</dt> </dl>

Le protocole autorise la connexion des données sur le réseau.

</dd> <dt>

**SupportsDisconnectData**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ déconnecte les \_ données »)
</dt> </dl>

Le protocole autorise la déconnexion des données sur le réseau.

</dd> <dt>

**SupportsEncryption**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ chiffre »)
</dt> </dl>

Le protocole prend en charge le chiffrement des données.

</dd> <dt>

**SupportsExpeditedData**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| Protocol \_ info \| dwServiceFlags \| XP \_ Expedited \_ Data »)
</dt> </dl>

Le protocole prend en charge les données expédiées (également appelées données urgentes) sur le réseau. Les données expédiées peuvent contourner le contrôle de Flow et recevoir la priorité sur les paquets de données normaux.

</dd> <dt>

**SupportsFragmentation**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| Protocol \_ info \| dwServiceFlags \| XP \_ fragmentation »)
</dt> </dl>

Le protocole prend en charge la transmission des données par fragments. L’unité de transfert maximale (MTU) du réseau physique est masquée dans les applications. Chaque type de média a une taille de trame maximale qui ne peut pas être dépassée. La couche de liaison Découvre la MTU et la signale aux protocoles utilisés.

</dd> <dt>

**SupportsGracefulClosing**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ normal \_ Close »)
</dt> </dl>

Le protocole prend en charge les opérations de fermeture en deux phases, également appelées « opérations de fermeture gracieuse ». Si ce n’est pas le cas, le protocole prend en charge uniquement les opérations de fermeture abandonnées.

</dd> <dt>

**SupportsGuaranteedBandwidth**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ allocation de bande passante \_ »)
</dt> </dl>

Le protocole a un mécanisme permettant d’établir et de maintenir une bande passante.

</dd> <dt>

**SupportsMulticasting**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ prend en charge la \_ multidiffusion »)
</dt> </dl>

Le protocole prend en charge la multidiffusion.

</dd> <dt>

**SupportsQualityofService**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| WSAPROTOCOL \_ info \| dwServiceFlags1 \| XP1 \_ QoS \_ pris en charge »)
</dt> </dl>

Le protocole peut prendre en charge la qualité de service (QoS) par le fournisseur de services en couche sous-jacent ou le transporteur de transport. La qualité de service (QoS) est un ensemble de composants qui activent la différenciation et le traitement préférentiel pour les sous-ensembles de données transmises sur le réseau. La qualité de service (QoS) signifie que les sous-ensembles de données obtiennent une priorité plus élevée ou un service garanti lors du parcours d’un réseau.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ NetworkProtocol** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant montre comment récupérer une liste de services en cours d’exécution à partir d’instances de **Win32 \_ NetworkProtocol**.


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



L’exemple de code perl suivant montre comment récupérer une liste de services en cours d’exécution à partir d’instances de **Win32 \_ NetworkProtocol**.


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
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

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
