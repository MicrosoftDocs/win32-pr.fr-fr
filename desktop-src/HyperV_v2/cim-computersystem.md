---
description: Représente une collection qui fournit des fonctionnalités de calcul et se compose d' \_ objets MANAGEDSYSTEMELEMENT CIM.
ms.assetid: 410be43f-3368-4109-8b29-7b7cc2a3ec1b
title: Classe CIM_ComputerSystem (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.NameFormat
- CIM_ComputerSystem.Dedicated
- CIM_ComputerSystem.OtherDedicatedDescriptions
- CIM_ComputerSystem.ResetCapability
- CIM_ComputerSystem.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00a53d0c514113175c3c6ffb7ea40f8ef4e730d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535620"
---
# <a name="cim_computersystem-class-hyper-v-management"></a>Classe CIM_ComputerSystem (gestion Hyper-V)

Représente une collection qui fournit des fonctionnalités de calcul et se compose d’objets [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string NameFormat;
  uint16 Dedicated[];
  string OtherDedicatedDescriptions[];
  uint16 ResetCapability;
  uint16 PowerManagementCapabilities[];
};
```

## <a name="members"></a>Membres

La classe de l' **\_ ComputerSystem CIM** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de l' **\_ ComputerSystem CIM** possède ces méthodes.



| Méthode                                                    | Description                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetPowerState**](cim-computersystem-setpowerstate.md) | Cette méthode est déconseillée. Utilisez plutôt la méthode **RequestPowerStateChange** dans la classe **CIM \_ PowerManagementService** .<br/> **Description déconseillée :** Définit l’état d’alimentation de l’ordinateur.<br/> |



 

### <a name="properties"></a>Propriétés

La classe de l' **\_ ComputerSystem CIM** possède ces propriétés.

<dl> <dt>

**Dédié**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \|MIB-II.sysservices», «FC-GS. INCITSs-T11 \| plate-forme \| type»), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**CIMOM CIM \_**.**OtherDedicatedDescriptions**")
</dt> </dl>

L’objectif et les fonctionnalités du système informatique. Par exemple, un système dédié à l’impression peut spécifier « 11 » (impression). Un système à usage général avec des fonctionnalités d’impression peut être défini sur « 0 » (non dédié) et sur « 11 » (impression).

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Non dédié** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (1)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (2)


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Stockage** (3)


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Routeur** (4)


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Commutateur** (5)


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Commutateur de couche 3** (6)


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Commutateur Central Office** (7)


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Serveur d’accès** (9)


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Pare-feu** (10)


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Imprimer** (11)


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span id="I_O"></span><span id="i_o"></span>**E/s** (12)


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Mise en cache Web** (13)


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Gestion** (14)


</dt> <dd>

Cette instance est dédiée à l’hébergement du logiciel de gestion du système.

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Bloquer le serveur** (15)


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**Serveur de fichiers** (16)


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Appareil utilisateur mobile** (17)


</dt> <dd>

Par exemple, un appareil utilisateur dédié est un téléphone mobile ou un scanneur de codes-barres dans un magasin qui communique via la fréquence radio. Ces systèmes sont assez limités en matière de fonctionnalité et de programmabilité, et ne sont pas considérés comme des plates-formes de calcul « usage général ». Un exemple de système mobile qui est « usage général » (autrement dit, qui n’est pas dédié) est un ordinateur de poche. Bien qu’elles soient limitées dans sa programmation, de nouveaux logiciels peuvent être téléchargés et leurs fonctionnalités développées par l’utilisateur.

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Pont/extendeur** (19)


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Passerelle** (20)


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Virtualisation du stockage** (21)


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Bibliothèque multimédia** (22)


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**Tête NAS** (24)


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**NAS autonome** (25)


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span id="UPS"></span><span id="ups"></span>**UPS** (26)


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**Téléphone IP** (27)


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Contrôleur de gestion** (28)


</dt> <dd>

Cette instance représente un matériel spécialisé dédié à la gestion des systèmes (par exemple, un contrôleur de gestion de la carte de configuration (BMC) ou un processeur de service).

L’étendue de gestion d’un « contrôleur de gestion » est généralement un système géré unique dans lequel il est contenu.

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Gestionnaire de châssis** (29)


</dt> <dd>

Cette instance représente un système dédié à la gestion d’un châssis de panneau et de ses appareils contenus. Cette valeur est utilisée pour représenter un contrôleur de tablette. Un « gestionnaire de châssis » est un point d’agrégation pour la gestion et peut reposer sur des contrôleurs de gestion subordonnés pour la gestion des composants constitutifs.

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Contrôleur RAID basé sur l’hôte** (30)


</dt> <dd>

Cette instance représente un contrôleur de stockage RAID contenu dans un ordinateur hôte.

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Boîtier** de l’appareil de stockage (31)


</dt> <dd>

Cette instance représente un boîtier qui contient des dispositifs de stockage.

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Bureau** (32)


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Ordinateur portable** (33)


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Bibliothèque de bandes virtuelle** (34)


</dt> <dd>

Émulation d’une bibliothèque de bandes par un système de bibliothèque virtuelle.

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Système de bibliothèque virtuelle** (35)


</dt> <dd>

Utilise le stockage sur disque pour émuler les bibliothèques de bandes

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**PC réseau/client léger** (36)


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**Commutateur FC** (37)


</dt> <dd>

Dédié au basculement des frames Fibre Channel de couche 2.

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Commutateur Ethernet** (38)


</dt> <dd>

Dédié au basculement des frames Ethernet de couche 2

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32568.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")
</dt> </dl>

Format du nom du système de l’ordinateur.

<dt>



 (« Autre »)


</dt> <dd></dd> <dt>



 (« IP »)


</dt> <dd></dd> <dt>



 (« Dial »)


</dt> <dd></dd> <dt>



 (« HID »)


</dt> <dd></dd> <dt>



 (« NWA »)


</dt> <dd></dd> <dt>



 ("HWA")


</dt> <dd></dd> <dt>



 (« X25 »)


</dt> <dd></dd> <dt>



 (« RNIS »)


</dt> <dd></dd> <dt>



 (« IPX »)


</dt> <dd></dd> <dt>



 (« DCC »)


</dt> <dd></dd> <dt>



 (« ICD »)


</dt> <dd></dd> <dt>



 (« E. 164 »)


</dt> <dd></dd> <dt>



 (« SNA »)


</dt> <dd></dd> <dt>



 (« OID/OSI »)


</dt> <dd></dd> <dt>



 (« WWN »)


</dt> <dd></dd> <dt>



 ("NAA")


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ CIM**.**Dédié**»)
</dt> </dl>

Décrit comment ou pourquoi le système est dédié lorsque le tableau **dédié** comprend la valeur 2 (autre).

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Contrôle d’alimentation du système DMTF \| 001,2»)
</dt> </dl>

Cette propriété est déconseillée. Utilisez plutôt la méthode **PowerChangeCapabilities** dans la classe **CIM \_ PowerManagementCapabilitiesCIM \_ PowerManagementService** .

**Description déconseillée :** Les fonctionnalités de gestion de l’alimentation du système.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Non pris en charge** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (3)


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

**Modes d’économie d’énergie entrés automatiquement** (4)


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

**État d’alimentation définissable** (5)


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

**Cycle d’alimentation pris en charge** (6)


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

**Mise sous tension minutée prise en charge** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Hardware Security \| 001,4»)
</dt> </dl>

Indique si le système prend en charge l’opération de réinitialisation matérielle.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (3)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (4)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Non implémenté** (5)


</dt> <dd></dd> </dl>

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

[**\_Système CIM**](cim-system.md)
</dt> </dl>

 

