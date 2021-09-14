---
description: La \_ classe WMI BaseService abstraite Win32 représente des objets exécutables qui sont installés dans une base de données de Registre gérée par le gestionnaire de contrôle des services.
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b46f3b4bd37770a5f3a7c1a2d2faa93d49bc079a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124275"
---
# <a name="win32_baseservice-class"></a>\_Classe BaseService Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ BaseService** abstraite Win32 représente des objets exécutables qui sont installés dans une base de données de Registre gérée par le gestionnaire de contrôle des services. Le fichier exécutable associé à un service peut être démarré au démarrage par un programme de démarrage ou par le système. Il peut également être démarré à la demande par le gestionnaire de contrôle des services. Tout service ou processus qui n’appartient pas à un utilisateur spécifique, et qui fournit une interface à certaines fonctionnalités prises en charge par le système informatique, est un descendant (ou membre) de cette classe.

exemple : service client DHCP (dynamic host configuration protocol) sur un système d’ordinateur exécutant Windows Server.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ BaseService** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ BaseService** possède ces méthodes.



| Méthode                                                                             | Description                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Modifier**](change-method-in-class-win32-baseservice.md)                         | Modifie un service.<br/>                                                |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-baseservice.md)       | Modifie le mode de démarrage d’un service.<br/>                              |
| [**Créer**](create-method-in-class-win32-baseservice.md)                         | Crée un nouveau service.<br/>                                             |
| [**Supprimer**](delete-method-in-class-win32-baseservice.md)                         | Supprime un service existant.<br/>                                       |
| [**InterrogateService**](interrogateservice-method-in-class-win32-baseservice.md) | Demande que le service met à jour son état dans Service Manager.<br/> |
| [**PauseService**](pauseservice-method-in-class-win32-baseservice.md)             | Tente de placer le service dans l'état de pause.<br/>                 |
| [**ResumeService**](resumeservice-method-in-class-win32-baseservice.md)           | Tente de placer le service dans l'état de reprise.<br/>                |
| [**StartService**](startservice-method-in-class-win32-baseservice.md)             | Tente de placer le service dans son état de démarrage.<br/>              |
| [**StopService**](stopservice-method-in-class-win32-baseservice.md)               | Méthode de classe qui place le service dans l’état arrêté.<br/>         |
| [**UserControlService**](usercontrolservice-method-in-class-win32-baseservice.md) | Tente d’envoyer un code de contrôle défini par l’utilisateur à un service.<br/>         |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ BaseService** a ces propriétés.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| service \_ accepter \_ pause \_ continue"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("service accepte pause")
</dt> </dl>

Le service peut être suspendu.

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| service \_ accepter \_ Stop"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("service accepte Stop")
</dt> </dl>

Le service peut être arrêté.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)
</dt> </dl>

Brève description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")
</dt> </dl>

Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance. Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
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

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ configuration**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| \_ Process interactive \_ Process »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« interagit avec Desktop »)
</dt> </dl>

Le service peut créer ou communiquer avec Windows sur le bureau.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Display Name »)
</dt> </dl>

Nom complet du service. Cette chaîne a une longueur maximale de 256 caractères. Le nom est conservé dans le gestionnaire de contrôle des services. Les comparaisons de **DisplayName** ne respectent jamais la casse.

Contraintes : accepte la même valeur que la propriété **Name** .

Exemple : « Atdisk »

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« gravité de l’échec de démarrage »)
</dt> </dl>

Gravité de l’erreur. Échec du démarrage du service. La valeur indique l’action entreprise par le programme de démarrage en cas d’échec. Toutes les erreurs sont journalisées par le système informatique.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** ("ignorer")


</dt> <dd>

L'utilisateur n'est pas notifié.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (« normal »)


</dt> <dd>

L'utilisateur est notifié.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (« grave »)


</dt> <dd>

Le système a redémarré avec la dernière bonne configuration connue.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (« critique »)


</dt> <dd>

Le système tente de redémarrer avec une bonne configuration.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** ("inconnu")


</dt> <dd>

L’action effectuée n’est pas spécifiée.

</dd> </dl>

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("code de sortie")
</dt> </dl>

Définition des problèmes rencontrés lors du démarrage ou de l’arrêt du service. Cette propriété est définie sur **erreur \_ spécifique au service \_ \_** (1066) lorsque l’erreur est unique pour le service représenté par cette classe, et les informations sur l’erreur sont disponibles dans la propriété **ServiceSpecificExitCode** . Le service définit cette valeur sur **aucune \_ erreur** lors de l’exécution, et à nouveau sur fin normale.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")
</dt> </dl>

L’objet a été installé. Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificateur unique du service, qui fournit une indication de la fonctionnalité gérée. Cette fonctionnalité est décrite plus en détail dans la propriété **Description** de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file path Name")
</dt> </dl>

Chemin d’accès complet au fichier binaire de service qui implémente le service.

Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys"

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("code de sortie spécifique au serveur")
</dt> </dl>

Code d’erreur spécifique au service pour les erreurs qui se produisent pendant que le service est en cours de démarrage ou d’arrêt. Les codes de sortie sont définis par le service représenté par cette classe. Cette valeur est définie uniquement lorsque la valeur **ExitCodeproperty** est **erreur \_ spécifique au SERVICE d' \_ \_ erreur** (1066).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de service")
</dt> </dl>

Service fourni aux processus appelant.

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

</dd> <dt>

**Cours**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

Le service a été démarré.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("startMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("mode de démarrage")
</dt> </dl>

mode de démarrage du service de base Windows.

Cette propriété est héritée [**du \_ service CIM**](cim-service.md).

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

Service qui doit être démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuel** (« manuel »)


</dt> <dd>

Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-baseservice.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")


</dt> <dd>

Service qui ne peut plus être démarré.

</dd> </dl>

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Starting Account Name »)
</dt> </dl>

Nom du compte sous lequel le service s’exécute. Selon le type de service, le nom du compte peut se présenter sous la forme « nom_domaine \\ nom_utilisateur » ou UPN ( Username@DomainName ). Le processus de service sera journalisé à l’aide de l’une de ces deux formes lorsqu’il s’exécute. Si le compte appartient au domaine intégré,». \\ Nom d’utilisateur» peut être spécifié. Si **null** est spécifié, le service est connecté en tant que compte LocalSystem. Pour les pilotes au niveau du noyau ou du système, **StartName** contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou \\ \\ le pilote XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique. En outre, si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service. Exemple : « DWDOM \\ admin ».

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")
</dt> </dl>

État actuel du service de base.

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

**Windows Server 2008 et Windows Vista :** Cette propriété est en lecture seule.

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

État actuel de l’objet. Divers États opérationnels et inopérationnels peuvent être définis. Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche). Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ». Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.

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

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ")
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

Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")
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

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« ID de balise »)
</dt> </dl>

Valeur de balise unique pour ce service dans le groupe. La valeur 0 (zéro) indique que la balise n’a pas été assignée au service. Une balise peut être utilisée pour le tri du service Star tallation dans un groupe d’ordre de chargement en spécifiant un vecteur d’ordre des balises dans le registre situé à l’emplacement suivant : HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ GroupOrderList. Les balises sont uniquement évaluées pour les services du pilote du noyau et du pilote du système de fichiers qui ont des modes de démarrage ou de démarrage du système.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ BaseService** est dérivée [**du \_ service CIM**](cim-service.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service CIM**](cim-service.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

