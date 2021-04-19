---
description: Représente l’état du composant d’interface de service invité, qui fournit un mécanisme permettant d’interagir avec l’ordinateur virtuel à partir des interfaces de gestion sur le système hôte.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Classe Msvm_GuestServiceInterfaceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533746"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a>MSVM \_ GuestServiceInterfaceComponent, classe

Représente l’état du composant d’interface de service invité, qui fournit un mécanisme permettant d’interagir avec l’ordinateur virtuel à partir des interfaces de gestion sur le système hôte. Cette classe dérive de la classe [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ GuestServiceInterfaceComponent** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ GuestServiceInterfaceComponent** possède ces méthodes.



| Méthode                                                                               | Description                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-guestserviceinterfacecomponent.md) | Demande que l’état du composant d’interface de service invité soit remplacé par la valeur spécifiée.<br/>                           |
| [**Réinitialiser**](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | Demande la réinitialisation de l’unité logique. Non implémenté par WMI.<br/>                                                               |
| [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État. Non implémenté par WMI.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **MSVM \_ GuestServiceInterfaceComponent** possède les propriétés suivantes.

<dl> <dt>

**Disponibilité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Disponibilité et état de l’appareil.



| Valeur                                                                                                                                                                                                                                                                                                              | Signification                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Autre**</dt> <dt>1 (0x1)</dt> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Inconnu**</dt> <dt>2 (0X2)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <dt>**En cours d’exécution/Full Power**</dt> <dt>3 (0x3)</dt> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <dt>**Avertissement**</dt> <dt>4 (0x4)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**Dans le test**</dt> <dt>5 (0x5)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicable**</dt> <dt>6 (0x6)</dt> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <dt>**Mise hors tension**</dt> <dt>7 (0x7)</dt> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <dt>**Hors ligne**</dt> <dt>8 (0x8)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <dt>**Hors droit**</dt> <dt>9 (0x9)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt></dt> <dt>10 (0xA)</dt> détérioré </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <dt>**Non installé**</dt> <dt>11 (0xB)</dt> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <dt>**Erreur d’installation**</dt> <dt>12 (0xc)</dt> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> Économie <dt>**d’énergie-inconnu**</dt> <dt>13 (0xD)</dt> </dl>                             | L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.<br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> Économie <dt>**d’énergie-mode basse puissance**</dt> <dt>14 (0xE)</dt> </dl> | L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.<br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> Économie <dt>**d’énergie-secours**</dt> <dt>15 (0xF)</dt> </dl>                             | L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.<br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <dt>**Power cycle**</dt> <dt>16 (0x10)</dt> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> Économie <dt>**d’énergie-Avertissement**</dt> <dt>17 (0x11)</dt> </dl>                            | L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.<br/>                              |



 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Courte description textuelle de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Code d’erreur Configuration Manager Win32.



| Valeur                                                                                | Signification                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | L’appareil fonctionne correctement.<br/>                                                                                                   |
| <dl> <dt>1 (0x1)</dt> </dl>   | L’appareil n’est pas configuré correctement.<br/>                                                                                           |
| <dl> <dt>2 (0X2)</dt> </dl>   | Windows ne peut pas charger le pilote de cet appareil.<br/>                                                                               |
| <dl> <dt>3 (0x3)</dt> </dl>   | Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.<br/>                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | L’appareil ne fonctionne pas correctement. L’un de ses pilotes ou le Registre est peut-être endommagé.<br/>                                        |
| <dl> <dt>5 (0x5)</dt> </dl>   | Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.<br/>                                                         |
| <dl> <dt>6 (0x6)</dt> </dl>   | La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.<br/>                                                               |
| <dl> <dt>7 (0x7)</dt> </dl>   | Impossible de filtrer.<br/>                                                                                                                |
| <dl> <dt>8 (0x8)</dt> </dl>   | Le chargeur de pilote de l’appareil est manquant.<br/>                                                                                      |
| <dl> <dt>9 (0x9)</dt> </dl>   | L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.<br/>               |
| <dl> <dt>10 (0xA)</dt> </dl>  | Impossible de démarrer l’appareil.<br/>                                                                                                          |
| <dl> <dt>11 (0xB)</dt> </dl>  | Échec de l’appareil.<br/>                                                                                                                |
| <dl> <dt>12 (0xC)</dt> </dl>  | L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.<br/>                                                                              |
| <dl> <dt>13 (0xD)</dt> </dl>  | Windows ne peut pas vérifier les ressources de l’appareil.<br/>                                                                                 |
| <dl> <dt>14 (0xE)</dt> </dl>  | L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.<br/>                                                                  |
| <dl> <dt>15 (0xF)</dt> </dl>  | L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.<br/>                                                      |
| <dl> <dt>16 (0x10)</dt> </dl> | Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.<br/>                                                            |
| <dl> <dt>17 (0x11)</dt> </dl> | L’appareil demande un type de ressource inconnu.<br/>                                                                                |
| <dl> <dt>18 (0x12)</dt> </dl> | Les pilotes de périphérique doivent être réinstallés.<br/>                                                                                           |
| <dl> <dt>19 (0x13)</dt> </dl> | Échec lors de l’utilisation du chargeur VxD.<br/>                                                                                                 |
| <dl> <dt>20 (0x14)</dt> </dl> | Le Registre est peut-être endommagé.<br/>                                                                                                  |
| <dl> <dt>21 (0x15)</dt> </dl> | Défaillance du système. Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel. Windows supprime l’appareil.<br/> |
| <dl> <dt>22 (0x16)</dt> </dl> | L’appareil est désactivé.<br/>                                                                                                           |
| <dl> <dt>23 (0x17)</dt> </dl> | Défaillance du système. Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.<br/>                                 |
| <dl> <dt>24 (0x18)</dt> </dl> | L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.<br/>                                   |
| <dl> <dt>25 (0x19)</dt> </dl> | Windows est toujours en cours de configuration de l’appareil.<br/>                                                                                       |
| <dl> <dt>26 (0x1A)</dt> </dl> | Windows est toujours en cours de configuration de l’appareil.<br/>                                                                                       |
| <dl> <dt>27 (0x1B)</dt> </dl> | L’appareil n’a pas une configuration de journal valide.<br/>                                                                                 |
| <dl> <dt>28 (0x1C)</dt> </dl> | Les pilotes de périphérique ne sont pas installés.<br/>                                                                                             |
| <dl> <dt>29 (0x1D)</dt> </dl> | L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.<br/>                                               |
| <dl> <dt>30 (0x1E)</dt> </dl> | L’appareil utilise une ressource IRQ qu’un autre appareil utilise.<br/>                                                                 |
| <dl> <dt>31 (0x1F)</dt> </dl> | L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.<br/>                                              |



 

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée dans la création d’une instance. Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure d’installation de l’objet. Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier code d’erreur signalé par l’unité logique.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Étiquette par laquelle l’objet est connu. Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.

Exemple : « \* PNP030b »

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique. Cette propriété est héritée de **CIM \_ LogicalDevice**.



| Valeur                                                                                                                                                                                                                                                                                                                                                                 | Signification                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Inconnu**</dt> <dt>0 (0x0)</dt> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Non pris en charge**</dt> <dt>1 (0x1)</dt> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Désactivé**</dt> <dt>2 (0X2)</dt> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Activé**</dt> <dt>3 (0x3)</dt> </dl>                                                                                                                                     | Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.<br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <dt>**Modes d’économie d’énergie entrés automatiquement**</dt> <dt>4 (0x4)</dt> </dl> | L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.<br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <dt>**État d’alimentation définissable**</dt> <dt>5 (0x5)</dt> </dl>                                                                                 | La méthode [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) est prise en charge. Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée. Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).<br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <dt>**Cycle d’alimentation pris en charge**</dt> <dt>6 (0x6)</dt> </dl>                                                                     | La méthode [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).<br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <dt>**Mise sous tension minutée**</dt> <dt>7 (0X7)</dt> pris en charge </dl>                                                                 | La méthode [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.<br/>                                                                                       |



 

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie. Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .

Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge. Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État actuel de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

Les valeurs sont notamment les suivantes :

<dl><span id="OK"></span><span id="ok"></span><dt>

**OK**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**Erreurs**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**Détérioré**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**Connue**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**« Échec prévu »**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**Démarr**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**Arrêt**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**Services**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**Trop sollicité**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**« Non récupéré »**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**« Aucun contact »**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**« Comm. perdue »**
</dt> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État de l’unité logique. Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée. Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1 (0x1))
</dt> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2 (0X2))
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3 (0x3))
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (4 (0x4))
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (5 (0x5))
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe de création du système d’étendue.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du système d’étendue.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> <dt>

[**\_LOGICALDEVICE CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

