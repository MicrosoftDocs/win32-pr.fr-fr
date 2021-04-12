---
description: Représente un service sur un système informatique exécutant Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Classe Win32_Service
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033605"
---
# <a name="win32_service-class"></a>\_Classe de service Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) du **\_ service Win32** représente un service sur un système informatique exécutant Windows.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
};
```

## <a name="members"></a>Membres

La classe de **\_ service Win32** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ service Win32** possède ces méthodes.



| Méthode                                                                               | Description                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Modifiés**](change-method-in-class-win32-service.md)                               | Modifie un service.<br/>                                                                       |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-service.md)             | Modifie le mode de démarrage d’un service.<br/>                                                     |
| [**Créés**](create-method-in-class-win32-service.md)                               | Crée un nouveau service.<br/>                                                                    |
| [**Supprimer**](delete-method-in-class-win32-service.md)                               | Supprime un service existant.<br/>                                                              |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-service.md) | Retourne le descripteur de sécurité qui contrôle l’accès au service.<br/>                      |
| [**InterrogateService**](interrogateservice-method-in-class-win32-service.md)       | Demande qu’un service met à jour son état dans Service Manager.<br/>                          |
| [**PauseService**](pauseservice-method-in-class-win32-service.md)                   | Tente de placer un service dans l’état suspendu.<br/>                                          |
| [**ResumeService**](resumeservice-method-in-class-win32-service.md)                 | Tente de placer un service dans l’État repris.<br/>                                         |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-service.md) | Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.<br/> |
| [**StartService**](startservice-method-in-class-win32-service.md)                   | Tente de placer un service dans l’état de démarrage.<br/>                                       |
| [**StopService**](stopservice-method-in-class-win32-service.md)                     | Place un service dans l’état arrêté.<br/>                                                    |
| [**UserControlService**](usercontrolservice-method-in-class-win32-service.md)       | Tente d’envoyer un code de contrôle défini par l’utilisateur à un service.<br/>                                |



 

### <a name="properties"></a>Propriétés

La classe de **\_ service Win32** a ces propriétés.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**service \_**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| service \_ accepter \_ pause \_ continue"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("service accepte pause")
</dt> </dl>

Indique si le service peut être suspendu.

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**service \_**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| service \_ accepter \_ Stop"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("service accepte Stop")
</dt> </dl>

Indique si le service peut être arrêté.

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Brève description du service : chaîne d’une ligne.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Contrôler**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("check point Count")
</dt> </dl>

Valeur que le service incrémente régulièrement pour signaler sa progression pendant une opération de démarrage, d’arrêt, de suspension ou de poursuite de longue durée. Par exemple, le service incrémente cette valeur lors de la fin de chaque étape de son initialisation au démarrage. Le programme d’interface utilisateur qui appelle l’opération sur le service utilise cette valeur pour suivre la progression du service au cours d’une opération de longue durée. Cette valeur n’est pas valide et doit être égale à zéro lorsque l’opération de démarrage, d’arrêt, de suspension ou de reprise du service n’est pas en attente.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nom de la classe")
</dt> </dl>

Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance. Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures service \| [**\_ retardées \_ \_ \_ informations de démarrage automatique**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« démarrage automatique retardé »)
</dt> </dl>

Si la **valeur est true**, le service est démarré après le démarrage d’autres services à démarrage automatique, plus un bref délai.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ configuration**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| \_ Process interactive \_ Process »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« interagit avec Desktop »)
</dt> </dl>

Indique si le service peut créer ou communiquer avec Windows sur le bureau, et par conséquent interagir de quelque manière avec un utilisateur. Les services interactifs doivent s’exécuter sous le compte système local. La plupart des services ne sont pas interactifs. autrement dit, ils ne communiquent pas avec l’utilisateur de quelque manière que ce soit.

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Display Name »)
</dt> </dl>

Nom du service tel qu’il est affiché dans le composant logiciel enfichable Services. Cette chaîne a une longueur maximale de 256 caractères. Notez que le nom d’affichage et le nom du service (qui est stocké dans le registre) ne sont pas toujours identiques. Par exemple, le service client DHCP a le nom de service DHCP, mais le nom d’affichage client DHCP. Le nom est conservé dans le gestionnaire de contrôle des services. Toutefois, les comparaisons **DisplayName** ne respectent jamais la casse.

Constraint : accepte la même valeur que la propriété **Name** .

Exemple : « Atdisk »

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« gravité de l’échec de démarrage »)
</dt> </dl>

Gravité de l’erreur si ce service ne parvient pas à démarrer au démarrage. La valeur indique l’action entreprise par le programme de démarrage en cas d’échec. Toutes les erreurs sont journalisées par le système informatique.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** ("ignorer")


</dt> <dd>

L'utilisateur n'est pas notifié.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (« normal »)


</dt> <dd>

L'utilisateur est notifié. Il s’agit généralement d’un message indiquant que l’utilisateur du problème est affiché.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (« grave »)


</dt> <dd>

Le système est redémarré avec la dernière bonne configuration connue.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (« critique »)


</dt> <dd>

Le système tente de redémarrer avec une bonne configuration. Si le service ne démarre pas une deuxième fois, le démarrage échoue.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** ("inconnu")


</dt> <dd>

La gravité de l’erreur est inconnue.

</dd> </dl>

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("code de sortie")
</dt> </dl>

Code d’erreur Windows qui définit les erreurs rencontrées lors du démarrage ou de l’arrêt du service. Cette propriété est définie sur **erreur \_ spécifique au service \_ \_** (1066) lorsque l’erreur est unique pour le service représenté par cette classe, et les informations sur l’erreur sont disponibles dans la propriété **ServiceSpecificExitCode** . Le service définit cette valeur sur **aucune \_ erreur** lors de l’exécution, et à nouveau sur fin normale.

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

L’objet date est installé. Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](../wmisdk/key-qualifier.md)
</dt> </dl>

Identificateur unique du service qui fournit une indication de la fonctionnalité gérée. Cette fonctionnalité est décrite dans la propriété **Description** de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("file path Name")
</dt> </dl>

Chemin d’accès complet au fichier binaire de service qui implémente le service.

Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys"

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process structures service \| [**\_ Status \_ Process**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process ID")
</dt> </dl>

Identificateur de processus du service.

Exemple : 324

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("code de sortie spécifique au serveur")
</dt> </dl>

Code d’erreur spécifique au service pour les erreurs qui se produisent pendant que le service est en cours de démarrage ou d’arrêt. Les codes de sortie sont définis par le service représenté par cette classe. Cette valeur est définie uniquement lorsque la valeur de la propriété **ExitCode** est erreur **\_ spécifique au service \_ \_** (1066).

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("type de service")
</dt> </dl>

Type de service fourni aux processus appelants.

Les valeurs sont :

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**Pilote de noyau** (« pilote de noyau »)


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**Pilote du système de fichiers** (« pilote du système de fichiers »)


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**Carte** (« adaptateur »)


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

**Pilote de reconnaissance** (« pilote de reconnaissance »)


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Propre processus** (« propre processus »)


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Processus de partage** (« processus de partage »)


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Processus interactif** (« processus interactif »)


</dt> <dd></dd> </dl>

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**Cours**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

Indique si le service est démarré ou non.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« mode de démarrage »)
</dt> </dl>

Mode de démarrage du service de base Windows.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Démarrage** (« démarrage »)


</dt> <dd>

Pilote de périphérique Démarré par le chargeur du système d’exploitation (valide uniquement pour les services de pilote).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Système** (« système »)


</dt> <dd>

Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** (« auto »)


</dt> <dd>

Le service doit être démarré automatiquement par le Gestionnaire de contrôle des services lors du démarrage du système. Les services automatiques sont démarrés même si un utilisateur ne se connecte pas.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuel** (« manuel »)


</dt> <dd>

Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-service.md) . Ces services ne démarrent pas à moins qu’un utilisateur se connecte et ne les démarre.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")


</dt> <dd>

Service qui ne peut pas être démarré tant que son StartMode n’a pas été modifié en auto ou manuellement.

</dd> </dl>

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Starting Account Name »)
</dt> </dl>

Nom du compte sous lequel un service s’exécute. Selon le type de service, le nom du compte peut se présenter sous la forme « nom_domaine \\ nom_utilisateur » ou au format UPN (« *Username@DomainName* »). Le processus de service est enregistré à l’aide de l’une de ces deux formes lorsqu’il s’exécute. Si le compte appartient au domaine intégré, «. \\ Nom d’utilisateur» peut être spécifié. Pour les pilotes au niveau du noyau ou du système, **StartName** contient le nom d’objet du pilote (c’est-à-dire « \\ FileSystem \\ RDR » ou « \\ Driver \\ XNS ») que le système d’e/s utilise pour charger le pilote de périphérique. En outre, si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.

Exemple : « DWDOM \\ admin »

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")
</dt> </dl>

État actuel du service de base.

Les valeurs sont :

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**Arrêté** (« arrêté »)


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**Start Pending** (« Start Pending »)


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**Arrêt en attente** (« arrêt en attente »)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**En cours d’exécution** (« en cours d’exécution »)


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Poursuite en attente** ("continuer en attente")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**Pause en attente** ("pause en attente")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Suspendu** (« suspendu »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> </dl>

**Windows Server 2008 et Windows Vista :** Cette propriété est en lecture seule avant Windows 7 et Windows Server 2008 R2.

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

État actuel de l’objet. Divers États opérationnels et inopérationnels peuvent être définis. Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche). Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ». Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Les valeurs sont :

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

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Class Name ")
</dt> </dl>

Nom de type du système qui héberge ce service.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ")
</dt> </dl>

Nom du système qui héberge ce service.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« ID de balise »)
</dt> </dl>

Valeur de balise unique pour ce service dans le groupe. La valeur 0 (zéro) indique que le service n’a pas de balise. Une balise peut être utilisée pour ordonner le démarrage du service dans un groupe d’ordre de chargement en spécifiant un vecteur d’ordre des balises dans le registre à l’emplacement suivant :

**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local GroupOrderList    

Les balises sont uniquement évaluées pour les services de type démarrage du pilote du noyau et du pilote du système de fichiers qui ont des modes de démarrage ou de démarrage du système.

Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« temps d’attente estimé »)
</dt> </dl>

Durée estimée, en millisecondes, pour une opération de démarrage, d’arrêt, de suspension ou de continuation en attente. Une fois le temps spécifié écoulé, le service effectue son prochain appel à la méthode **SetServiceStatus** avec une valeur **de point de contrôle** incrémentée ou une modification dans **CurrentState**. Si la durée spécifiée par **WaitHint** passe, si le **point** de contrôle n’a pas été incrémenté ou si **CurrentState** n’a pas changé, le gestionnaire de contrôle des services ou le programme de contrôle des services suppose qu’une erreur s’est produite.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe de **\_ service Win32** est dérivée de [**Win32 \_ BaseService**](win32-baseservice.md).

La façon dont vous gérez un ordinateur spécifique dépend beaucoup du rôle joué par l’ordinateur. Par exemple, vous surveillez généralement les différents aspects d’un serveur DNS par rapport à un serveur DHCP. Bien qu’aucune propriété unique ne vous indique si un ordinateur particulier est un serveur de base de données, un serveur de messagerie ou un serveur multimédia, vous pouvez souvent identifier le rôle joué par un ordinateur en identifiant les services installés sur celui-ci.

Dans les grandes organisations, un seul des principaux services (tels que le courrier électronique) est susceptible d’être installé sur un seul ordinateur. Il serait rare qu’un serveur de messagerie s’exécute également en tant que serveur pour Microsoft® les fichiers du lecteur Windows Media® Technologies. Pour cette raison, l’identification d’un service installé sur un ordinateur peut aider à identifier le rôle de l’ordinateur sur le réseau. Si le service Microsoft® Exchange Server est installé et en cours d’exécution sur un ordinateur, il est généralement possible de supposer que cet ordinateur fonctionne comme un serveur de messagerie.

Vous pouvez utiliser la classe WMI **Win32 \_ service** pour énumérer les services installés sur un ordinateur. En outre, vous pouvez utiliser cette classe pour déterminer si ces services sont en cours d’exécution et pour retourner toutes les autres informations requises sur ce service et la manière dont il a été configuré.

Une application de service est conforme aux règles d’interface du gestionnaire de contrôle des services (SCM) et peut être démarrée automatiquement par un utilisateur au démarrage du système via l’utilitaire du panneau de configuration des services ou par une application qui utilise les fonctions de service incluses dans l’API Windows. Les services peuvent démarrer quand aucun utilisateur n’est connecté à l’ordinateur.

Un utilisateur qui se connecte à partir d’un ordinateur distant doit disposer du privilège de **\_ \_ connexion SC Manager** pour pouvoir énumérer cette classe. Pour plus d’informations, consultez [sécurité des services et droits d’accès](../services/service-security-and-access-rights.md).

## <a name="examples"></a>Exemples

La [requête PS-WMI qui retourne le service « État » sur un groupe d’appareils](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) exemple PowerShell dans la Galerie TechNet utilise le **\_ service Win32** pour créer une liste d’appareils à partir de Active Directory, puis interroger chaque appareil qui répond avec pingfor un service spécifique en cours d’exécution.

L’exemple PowerShell de [rapport de serveur](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) de la Galerie TechNet utilise le **\_ service Win32** pour rassembler des informations sur le serveur et les publier dans un document Word.

L’exemple de code VBScript suivant affiche tous les services actuellement installés.


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



L’exemple de code VBScript suivant décrit les services suspendus, en cours d’exécution et arrêtés sur l’ordinateur spécifié.


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



Le script perl suivant montre comment récupérer une liste de services en cours d’exécution à partir d’instances du **\_ service Win32**.


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



L’exemple c suivant \# utilise [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) pour récupérer tous les services en cours d’exécution sur l’ordinateur local.


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



L' \# exemple de code C suivant utilise l’espace de noms [System. Management](/dotnet/api/system.management) pour récupérer tous les services en cours d’exécution sur l’ordinateur local.

> [!Note]  
> [System. Management](/dotnet/api/system.management) contient les classes d’origine utilisées pour accéder à WMI. Toutefois, ils sont considérés comme plus lents et ne sont généralement pas mis à l’échelle, ainsi que leurs équivalents [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


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

[**\_BaseService Win32**](win32-baseservice.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> <dt>

[Tâches WMI : services](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
