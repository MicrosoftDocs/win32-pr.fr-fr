---
description: Décrit les aspects virtuels d’un système virtuel via un ensemble de propriétés spécifiques à la virtualisation. \_Le VIRTUALSYSTEMSETTINGDATA CIM est également utilisé comme classe de niveau supérieur des configurations du système virtuel.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: Classe CIM_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535483"
---
# <a name="cim_virtualsystemsettingdata-class"></a>\_Classe CIM VirtualSystemSettingData

Décrit les aspects virtuels d’un système virtuel via un ensemble de propriétés spécifiques à la virtualisation. **CIM \_ VirtualSystemSettingData** est également utilisé comme classe de niveau supérieur des configurations du système virtuel.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ VirtualSystemSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ VirtualSystemSettingData** possède les propriétés suivantes.

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à entreprendre pour le système virtuel lorsque le logiciel exécuté par le système virtuel échoue. Les échecs résolus par cette propriété incluent uniquement ceux qui sont détectables par la plateforme hôte, tels qu’une condition d’état d’attente non interruptible.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (2)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Redémarrer** (3)


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

**Revenir à l’instantané** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à entreprendre pour le système virtuel lorsque l’ordinateur hôte est arrêté.

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

**Désactiver** (2)


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

**Enregistrer l’État** (3)


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

**Arrêt** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Action à effectuer sur le système virtuel au démarrage de l’hôte.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (2)


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

**Redémarrer si précédemment actif** (3)


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

**Toujours démarrer** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Délai de l’action de démarrage. Cette valeur est une variante d’intervalle du type de données **DateTime** .

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de séquence pour l’activation du système virtuel lorsque le système hôte est démarré. Un nombre inférieur indique une activation antérieure. Si une ou plusieurs configurations affichent la même valeur, la séquence dépend de l’implémentation. La valeur « 0 » indique que la séquence dépend de l’implémentation.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès du répertoire dans lequel sont stockées les informations relatives à la configuration du système virtuel. Le format de cette propriété est un URI basé sur la norme RFC 2079.

</dd> <dt>

**Fichier ConfigurationFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès relatif du fichier dans lequel sont stockées les informations relatives à la configuration du système virtuel. Le chemin d’accès relatif est ajouté à la valeur de la propriété **ConfigurationDataRoot** . Le format de cette propriété est un URI basé sur la norme RFC 2079.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

ID unique de la configuration du système virtuel.

> [!Note]  
> **ConfigurationID** est différent de l' **InstanceID** et est assigné par l’implémentation à un système virtuel ou à une configuration de système virtuel. **ConfigurationID** n’est pas une clé, et la même valeur peut se produire pour plusieurs instances.

 

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création de la configuration du système virtuel.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès relatif du répertoire où sont stockées les informations de journalisation du système virtuel. Le chemin d’accès relatif est ajouté à la valeur de la propriété **ConfigurationDataRoot** . Le format de cette propriété est un URI basé sur la norme RFC 2079.

</dd> <dt>

**Remarques**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau qui contient les notes fournies par l’utilisateur qui sont liées au système virtuel.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès du fichier dans lequel sont stockées les informations relatives à la récupération du système virtuel. Le format de cette propriété est un URI basé sur la norme RFC 2079.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès relatif du répertoire où sont stockées les informations sur les instantanés de système virtuel. Le chemin d’accès relatif est ajouté à la valeur de la propriété **ConfigurationDataRoot** . Le format de cette propriété est un URI basé sur la norme RFC 2079.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès relatif du répertoire dans lequel sont stockées les informations relatives à l’interruption du système virtuel. Le chemin d’accès relatif est ajouté à la valeur de la propriété **ConfigurationDataRoot** . Le format de cette propriété est un URI basé sur la norme RFC 2079.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès relatif du répertoire où sont stockés les fichiers d’échange du système virtuel. Le chemin d’accès relatif est ajouté à la valeur de la propriété **ConfigurationDataRoot** . Le format de cette propriété est un URI basé sur la norme RFC 2079.

</dd> <dt>

**Attribut virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom unique du système au sein de la plateforme de virtualisation. **Attribut virtualsystemidentifier** n’est pas le nom d’hôte affecté à l’instance de système d’exploitation en cours d’exécution dans le système virtuel, et il ne s’agit pas d’une adresse IP ou d’une adresse Mac affectée à l’un de ses ports réseau.

Le **attribut virtualsystemidentifier** peut contenir des règles spécifiques d’implémentation, comme des modèles simples ou une expression régulière qui peut être interprétée par l’implémentation lors de la définition de **attribut virtualsystemidentifier**.

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type du système virtuel.

> [!Note]  
> Si le type de système virtuel est inconnu, cette valeur doit être définie sur « DMTF : Unknown ».

 

Cette propriété est mise en forme à l’aide du format de ABNF (Backus Naur Form) augmenté suivant :

vs-type = DMTF-value/Other-org-value/Legacy-value ; DMTF-value = "DMTF :" Defining-org " :" org-vs-type ; Other-org-value = définition-org " :" org-vs-type ;

La valeur du format ABNF ci-dessus est la suivante :

-   *DMTF-valeur*   une valeur de propriété définie par DMTF et est définie dans la description de cette propriété.
-   *other-org-value*   est une valeur de propriété définie par une entité commerciale autre que DMTF et n’est pas définie dans la description de cette propriété.
-   *valeur héritée*   une valeur de propriété définie par une entité métier autre que DMTF et n’est pas définie dans la description de cette propriété. Ces valeurs sont autorisées, mais elles sont recommandées pour être dépréciées au fil du temps.
-   *définition-org*   identificateur de l’entité métier qui définit le type de système virtuel. Il doit inclure un nom de droits d’auteur, de marque déposée ou unique qui appartient à l’entité métier. Il ne doit pas être « DMTF » et ne doit pas contenir de deux-points.
-   *org-vs-tapez*   un identificateur pour le type de système virtuel au sein de l’entité métier de définition. Elle doit être unique au sein de la définition-org. org-vs-type peut utiliser n’importe quel caractère autorisé pour les chaînes CIM, à l’exception des suivantes : U0000-U001F (contrôles C0 Unicode), U0020 (Space), U007F (contrôles Unicode C0) ou U0080-U009F (contrôles C1 Unicode).
-   S’il est nécessaire de structurer la valeur en segments, les segments doivent être séparés par un seul signe deux-points.
-   Les valeurs de cette propriété doivent être traitées en respectant la casse. Ils sont destinés à être traités par programmation, au lieu d’être un nom complet, et doivent être courts.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




