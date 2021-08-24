---
title: Win32_TerminalService, classe
description: Une sous-classe de la \_ classe de service Win32. Win32 \_ TerminalService représente la propriété d’élément de l' \_ Association Win32 TerminalServiceToSetting.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService de la classe Services Bureau à distance
- Win32_TerminalService de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 735b033017958816e8e9a40caea935847104fdcbe3e9acf3128890d88685d09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867849"
---
# <a name="win32_terminalservice-class"></a>\_Classe TerminalService Win32

La classe WMI **\_ TerminalService** WMI est une sous-classe de la classe de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) . **Win32 \_ TerminalService** représente la propriété d' **élément** de l’Association [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .

La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
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
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TerminalService** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TerminalService** possède ces méthodes.



| Méthode                                                                       | Description                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Modifier**](win32-terminalservice-change.md)                               | Modifie un service.<br/>                                                                       |
| [**ChangeStartMode**](win32-terminalservice-changestartmode.md)             | Modifie le mode de démarrage d’un service.<br/>                                                     |
| [**Créer**](win32-terminalservice-create.md)                               | Crée un nouveau service.<br/>                                                                    |
| [**Supprimer**](win32-terminalservice-delete.md)                               | Supprime un service existant.<br/>                                                              |
| [**GetSecurityDescriptor**](win32-terminalservice-getsecuritydescriptor.md) | Retourne le descripteur de sécurité qui contrôle l’accès au service.<br/>                      |
| [**InterrogateService**](win32-terminalservice-interrogateservice.md)       | Demande qu’un service met à jour son état dans Service Manager.<br/>                          |
| [**PauseService**](win32-terminalservice-pauseservice.md)                   | Tente de placer un service dans l’état suspendu.<br/>                                          |
| [**ResumeService**](win32-terminalservice-resumeservice.md)                 | Tente de placer un service dans l’État repris.<br/>                                         |
| [**SetSecurityDescriptor**](win32-terminalservice-setsecuritydescriptor.md) | Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.<br/> |
| [**StartService**](win32-terminalservice-startservice.md)                   | Tente de placer un service dans l’état de démarrage.<br/>                                       |
| [**StopService**](win32-terminalservice-stopservice.md)                     | Place un service dans l’état arrêté.<br/>                                                    |
| [**UserControlService**](win32-terminalservice-usercontrolservice.md)       | Tente d’envoyer un code de contrôle défini par l’utilisateur à un service.<br/>                                |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TerminalService** a ces propriétés.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| service \_ accepter \_ pause \_ continue"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("service accepte pause")
</dt> </dl>

Indique si le service peut être suspendu.

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| service \_ accepter \_ Stop"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("service accepte Stop")
</dt> </dl>

Indique si le service peut être arrêté.

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)
</dt> </dl>

Description succincte du service chaîne d’une ligne.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Contrôler**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("check point Count")
</dt> </dl>

Valeur que le service incrémente régulièrement pour signaler sa progression pendant une opération de démarrage, d’arrêt, de suspension ou de poursuite de longue durée. Par exemple, le service incrémente cette valeur lors de la fin de chaque étape de son initialisation au démarrage. Le programme d’interface utilisateur qui appelle l’opération sur le service utilise cette valeur pour suivre la progression du service au cours d’une opération de longue durée. Cette valeur n’est pas valide et doit être égale à zéro lorsque l’opération de démarrage, d’arrêt, de suspension ou de reprise du service n’est pas en attente.

Cette propriété est héritée [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")
</dt> </dl>

Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance. Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.

Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures service \| [**\_ retardées \_ \_ \_ informations de démarrage automatique**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« démarrage automatique retardé »)
</dt> </dl>

Si la **valeur est true**, le service est démarré après le démarrage d’autres services à démarrage automatique, plus un bref délai.

**Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 r2, Windows 7, Windows server 2008 et Windows Vista :** cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.

Cette propriété est héritée [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).

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

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ configuration**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| \_ Process interactive \_ Process »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« interagit avec Desktop »)
</dt> </dl>

Indique si le service peut créer ou communiquer avec Windows sur le bureau, et par conséquent interagir de quelque manière avec un utilisateur. Les services interactifs doivent s’exécuter sous le compte système local. La plupart des services ne sont pas interactifs. autrement dit, ils ne communiquent pas avec l’utilisateur de quelque manière que ce soit.

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**DisconnectedSessions**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de sessions déconnectées sur le serveur actuel. Ces sessions peuvent toujours consommer activement les ressources du serveur, mais elles ne disposent pas actuellement d’une connexion réseau avec un client.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Display Name »)
</dt> </dl>

Nom du service tel qu’il est affiché dans le composant logiciel enfichable Services. Cette chaîne a une longueur maximale de 256 caractères. Notez que le nom d’affichage et le nom du service (qui est stocké dans le registre) ne sont pas toujours identiques. Par exemple, le service client DHCP a le nom de service DHCP, mais le nom d’affichage client DHCP. Le nom est conservé dans le gestionnaire de contrôle des services. Toutefois, les comparaisons [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) ne respectent jamais la casse.

Constraint : accepte la même valeur que la propriété [**Name**](/windows/desktop/CIMWin32Prov/win32-service) .

Exemple : « Atdisk »

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« gravité de l’échec de démarrage »)
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

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("code de sortie")
</dt> </dl>

Windows code d’erreur qui définit les erreurs rencontrées lors du démarrage ou de l’arrêt du service. Cette propriété est définie sur **erreur \_ spécifique au service \_ \_** (1066) lorsque l’erreur est unique pour le service représenté par cette classe, et les informations sur l’erreur sont disponibles dans la propriété [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) . Le service définit cette valeur sur **aucune \_ erreur** lors de l’exécution, et à nouveau sur fin normale.

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")
</dt> </dl>

L’objet date est installé. Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificateur unique du service qui fournit une indication de la fonctionnalité gérée. Cette fonctionnalité est décrite dans la propriété [**Description**](/windows/desktop/CIMWin32Prov/win32-service) de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Process structures service \| [**\_ Status \_ Process**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process ID")
</dt> </dl>

Identificateur de processus du service.

Exemple : 324

Cette propriété est héritée [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("code de sortie spécifique au serveur")
</dt> </dl>

Code d’erreur spécifique au service pour les erreurs qui se produisent pendant que le service est en cours de démarrage ou d’arrêt. Les codes de sortie sont définis par le service représenté par cette classe. Cette valeur est définie uniquement lorsque la valeur de la propriété [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) est erreur **\_ spécifique au service \_ \_** (1066).

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de service")
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

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Démarré**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

Indique si le service est démarré ou non.

Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« mode de démarrage »)
</dt> </dl>

mode de démarrage du service de base Windows.

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

Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) . Ces services ne démarrent pas à moins qu’un utilisateur se connecte et ne les démarre.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")


</dt> <dd>

Service qui ne peut pas être démarré tant que son StartMode n’a pas été modifié en auto ou manuellement.

</dd> </dl>

Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Starting Account Name »)
</dt> </dl>

Nom du compte sous lequel un service s’exécute. Selon le type de service, le nom du compte peut se présenter sous la forme « nom_domaine \\ nom_utilisateur » ou au format UPN (« *Username@DomainName* »). Le processus de service est enregistré à l’aide de l’une de ces deux formes lorsqu’il s’exécute. Si le compte appartient au domaine intégré, «. \\ Nom d’utilisateur» peut être spécifié. Pour les pilotes au niveau du noyau ou du système, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contient le nom d’objet du pilote (c’est-à-dire « \\ FileSystem \\ RDR » ou « \\ Driver \\ XNS ») que le système d’e/s utilise pour charger le pilote de périphérique. En outre, si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.

Exemple : « DWDOM \\ admin »

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

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

**Windows Server 2008 et Windows Vista :** cette propriété est en lecture seule avant Windows 7 et Windows Server 2008 R2.

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

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

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName "), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ")
</dt> </dl>

Nom de type du système qui héberge ce service.

Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](/windows/desktop/CIMWin32Prov/cim-system). Name "), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")
</dt> </dl>

Nom du système qui héberge ce service.

Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« ID de balise »)
</dt> </dl>

Valeur de balise unique pour ce service dans le groupe. La valeur 0 (zéro) indique que le service n’a pas de balise. Une balise peut être utilisée pour ordonner le démarrage du service dans un groupe d’ordre de chargement en spécifiant un vecteur d’ordre des balises dans le registre à l’emplacement suivant :

**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local GroupOrderList    

Les balises sont uniquement évaluées pour les services de type démarrage du pilote du noyau et du pilote du système de fichiers qui ont des modes de démarrage ou de démarrage du système.

Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**TotalSessions**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total de sessions sur le serveur actuel. Cela comprend les sessions connectées et déconnectées.

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« temps d’attente estimé »)
</dt> </dl>

Durée estimée, en millisecondes, pour une opération de démarrage, d’arrêt, de suspension ou de continuation en attente. Une fois le temps spécifié écoulé, le service effectue son prochain appel à la méthode **SetServiceStatus** avec une valeur [**de point de contrôle**](/windows/desktop/CIMWin32Prov/win32-service) incrémentée ou une modification dans **CurrentState**. Si la durée spécifiée par **WaitHint** passe, si le **point** de contrôle n’a pas été incrémenté ou si **CurrentState** n’a pas changé, le gestionnaire de contrôle des services ou le programme de contrôle des services suppose qu’une erreur s’est produite.

Cette propriété est héritée [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> </dl>

## <a name="remarks"></a>Remarques

Étant donné que la classe **\_ TerminalService Win32** est une sous-classe de la classe de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) , la classe hérite de toutes les propriétés et méthodes du **\_ service Win32**.

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) est associé à **Win32 \_ TerminalService** en tant que propriété de **paramètre** de l’Association [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) est associé à **Win32 \_ TerminalService** en tant que propriété de **paramètre** de l’Association [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**\_TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md)
</dt> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> <dt>

[**\_BaseService Win32**](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[**\_Service CIM**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

