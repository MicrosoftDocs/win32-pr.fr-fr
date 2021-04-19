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
# <a name="cim_computersystem-class-hyper-v-management"></a><span data-ttu-id="df9ca-103">Classe CIM_ComputerSystem (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="df9ca-103">CIM_ComputerSystem class (Hyper-V management)</span></span>

<span data-ttu-id="df9ca-104">Représente une collection qui fournit des fonctionnalités de calcul et se compose d’objets [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="df9ca-104">Represents a collection that provides computing capabilities and consists of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="df9ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df9ca-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="df9ca-106">Membres</span><span class="sxs-lookup"><span data-stu-id="df9ca-106">Members</span></span>

<span data-ttu-id="df9ca-107">La classe de l' **\_ ComputerSystem CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="df9ca-107">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="df9ca-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="df9ca-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="df9ca-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df9ca-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="df9ca-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="df9ca-110">Methods</span></span>

<span data-ttu-id="df9ca-111">La classe de l' **\_ ComputerSystem CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="df9ca-111">The **CIM\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="df9ca-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="df9ca-112">Method</span></span>                                                    | <span data-ttu-id="df9ca-113">Description</span><span class="sxs-lookup"><span data-stu-id="df9ca-113">Description</span></span>                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df9ca-114">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="df9ca-114">**SetPowerState**</span></span>](cim-computersystem-setpowerstate.md) | <span data-ttu-id="df9ca-115">Cette méthode est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="df9ca-115">This method is deprecated.</span></span> <span data-ttu-id="df9ca-116">Utilisez plutôt la méthode **RequestPowerStateChange** dans la classe **CIM \_ PowerManagementService** .</span><span class="sxs-lookup"><span data-stu-id="df9ca-116">Instead, use the **RequestPowerStateChange** method in the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="df9ca-117">**Description déconseillée :** Définit l’état d’alimentation de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="df9ca-117">**Deprecated description:** Sets the power state of the computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="df9ca-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df9ca-118">Properties</span></span>

<span data-ttu-id="df9ca-119">La classe de l' **\_ ComputerSystem CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="df9ca-119">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df9ca-120">**Dédié**</span><span class="sxs-lookup"><span data-stu-id="df9ca-120">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9ca-121">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9ca-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df9ca-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df9ca-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9ca-123">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \|MIB-II.sysservices», «FC-GS. INCITSs-T11 \| plate-forme \| type»), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**CIMOM CIM \_**.**OtherDedicatedDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="df9ca-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.sysServices", "FC-GS.INCITS-T11 \| Platform \| PlatformType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**OtherDedicatedDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="df9ca-124">L’objectif et les fonctionnalités du système informatique.</span><span class="sxs-lookup"><span data-stu-id="df9ca-124">The purpose and features of the computer system.</span></span> <span data-ttu-id="df9ca-125">Par exemple, un système dédié à l’impression peut spécifier « 11 » (impression).</span><span class="sxs-lookup"><span data-stu-id="df9ca-125">For example, a system dedicated to printing could specify "11" (Print).</span></span> <span data-ttu-id="df9ca-126">Un système à usage général avec des fonctionnalités d’impression peut être défini sur « 0 » (non dédié) et sur « 11 » (impression).</span><span class="sxs-lookup"><span data-stu-id="df9ca-126">A general purpose system with printing capabilities can be set to "0" (Not Dedicated) and "11" (Print).</span></span>

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span data-ttu-id="df9ca-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Non dédié** (0)</span><span class="sxs-lookup"><span data-stu-id="df9ca-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Not Dedicated** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9ca-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (1)</span><span class="sxs-lookup"><span data-stu-id="df9ca-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9ca-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (2)</span><span class="sxs-lookup"><span data-stu-id="df9ca-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="df9ca-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Stockage** (3)</span><span class="sxs-lookup"><span data-stu-id="df9ca-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span data-ttu-id="df9ca-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Routeur** (4)</span><span class="sxs-lookup"><span data-stu-id="df9ca-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="df9ca-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Commutateur** (5)</span><span class="sxs-lookup"><span data-stu-id="df9ca-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span data-ttu-id="df9ca-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Commutateur de couche 3** (6)</span><span class="sxs-lookup"><span data-stu-id="df9ca-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Layer 3 Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span data-ttu-id="df9ca-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Commutateur Central Office** (7)</span><span class="sxs-lookup"><span data-stu-id="df9ca-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Central Office Switch** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span data-ttu-id="df9ca-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span><span class="sxs-lookup"><span data-stu-id="df9ca-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span data-ttu-id="df9ca-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Serveur d’accès** (9)</span><span class="sxs-lookup"><span data-stu-id="df9ca-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Access Server** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span data-ttu-id="df9ca-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Pare-feu** (10)</span><span class="sxs-lookup"><span data-stu-id="df9ca-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="df9ca-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Imprimer** (11)</span><span class="sxs-lookup"><span data-stu-id="df9ca-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Print** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span data-ttu-id="df9ca-139"><span id="I_O"></span><span id="i_o"></span>**E/s** (12)</span><span class="sxs-lookup"><span data-stu-id="df9ca-139"><span id="I_O"></span><span id="i_o"></span>**I/O** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span data-ttu-id="df9ca-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Mise en cache Web** (13)</span><span class="sxs-lookup"><span data-stu-id="df9ca-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Web Caching** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span data-ttu-id="df9ca-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Gestion** (14)</span><span class="sxs-lookup"><span data-stu-id="df9ca-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Management** (14)</span></span>


</dt> <dd>

<span data-ttu-id="df9ca-142">Cette instance est dédiée à l’hébergement du logiciel de gestion du système.</span><span class="sxs-lookup"><span data-stu-id="df9ca-142">This instance is dedicated to hosting system management software</span></span>

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span data-ttu-id="df9ca-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Bloquer le serveur** (15)</span><span class="sxs-lookup"><span data-stu-id="df9ca-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Block Server** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span data-ttu-id="df9ca-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**Serveur de fichiers** (16)</span><span class="sxs-lookup"><span data-stu-id="df9ca-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**File Server** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span data-ttu-id="df9ca-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Appareil utilisateur mobile** (17)</span><span class="sxs-lookup"><span data-stu-id="df9ca-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Mobile User Device** (17)</span></span>


</dt> <dd>

<span data-ttu-id="df9ca-146">Par exemple, un appareil utilisateur dédié est un téléphone mobile ou un scanneur de codes-barres dans un magasin qui communique via la fréquence radio.</span><span class="sxs-lookup"><span data-stu-id="df9ca-146">An example of a dedicated user device is a mobile phone or a barcode scanner in a store that communicates via radio frequency.</span></span> <span data-ttu-id="df9ca-147">Ces systèmes sont assez limités en matière de fonctionnalité et de programmabilité, et ne sont pas considérés comme des plates-formes de calcul « usage général ».</span><span class="sxs-lookup"><span data-stu-id="df9ca-147">These systems are quite limited in functionality and programmability, and are not considered 'general purpose' computing platforms.</span></span> <span data-ttu-id="df9ca-148">Un exemple de système mobile qui est « usage général » (autrement dit, qui n’est pas dédié) est un ordinateur de poche.</span><span class="sxs-lookup"><span data-stu-id="df9ca-148">Alternately, an example of a mobile system that is 'general purpose' (i.e., is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="df9ca-149">Bien qu’elles soient limitées dans sa programmation, de nouveaux logiciels peuvent être téléchargés et leurs fonctionnalités développées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="df9ca-149">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span>

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span data-ttu-id="df9ca-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span><span class="sxs-lookup"><span data-stu-id="df9ca-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span data-ttu-id="df9ca-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Pont/extendeur** (19)</span><span class="sxs-lookup"><span data-stu-id="df9ca-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span data-ttu-id="df9ca-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Passerelle** (20)</span><span class="sxs-lookup"><span data-stu-id="df9ca-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span data-ttu-id="df9ca-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Virtualisation du stockage** (21)</span><span class="sxs-lookup"><span data-stu-id="df9ca-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Storage Virtualizer** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span data-ttu-id="df9ca-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Bibliothèque multimédia** (22)</span><span class="sxs-lookup"><span data-stu-id="df9ca-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Media Library** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span data-ttu-id="df9ca-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span><span class="sxs-lookup"><span data-stu-id="df9ca-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span data-ttu-id="df9ca-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**Tête NAS** (24)</span><span class="sxs-lookup"><span data-stu-id="df9ca-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**NAS Head** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span data-ttu-id="df9ca-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**NAS autonome** (25)</span><span class="sxs-lookup"><span data-stu-id="df9ca-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Self-contained NAS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span data-ttu-id="df9ca-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span><span class="sxs-lookup"><span data-stu-id="df9ca-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span data-ttu-id="df9ca-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**Téléphone IP** (27)</span><span class="sxs-lookup"><span data-stu-id="df9ca-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP Phone** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span data-ttu-id="df9ca-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Contrôleur de gestion** (28)</span><span class="sxs-lookup"><span data-stu-id="df9ca-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Management Controller** (28)</span></span>


</dt> <dd>

<span data-ttu-id="df9ca-161">Cette instance représente un matériel spécialisé dédié à la gestion des systèmes (par exemple, un contrôleur de gestion de la carte de configuration (BMC) ou un processeur de service).</span><span class="sxs-lookup"><span data-stu-id="df9ca-161">This instance represents specialized hardware dedicated to systems management (i.e., a Baseboard Management Controller (BMC) or service processor).</span></span>

<span data-ttu-id="df9ca-162">L’étendue de gestion d’un « contrôleur de gestion » est généralement un système géré unique dans lequel il est contenu.</span><span class="sxs-lookup"><span data-stu-id="df9ca-162">The management scope of a "Management Controller" is typically a single managed system in which it is contained.</span></span>

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span data-ttu-id="df9ca-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Gestionnaire de châssis** (29)</span><span class="sxs-lookup"><span data-stu-id="df9ca-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Chassis Manager** (29)</span></span>


</dt> <dd>

<span data-ttu-id="df9ca-164">Cette instance représente un système dédié à la gestion d’un châssis de panneau et de ses appareils contenus.</span><span class="sxs-lookup"><span data-stu-id="df9ca-164">This instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="df9ca-165">Cette valeur est utilisée pour représenter un contrôleur de tablette.</span><span class="sxs-lookup"><span data-stu-id="df9ca-165">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="df9ca-166">Un « gestionnaire de châssis » est un point d’agrégation pour la gestion et peut reposer sur des contrôleurs de gestion subordonnés pour la gestion des composants constitutifs.</span><span class="sxs-lookup"><span data-stu-id="df9ca-166">A "Chassis Manager" is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span>

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span data-ttu-id="df9ca-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Contrôleur RAID basé sur l’hôte** (30)</span><span class="sxs-lookup"><span data-stu-id="df9ca-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Host-based RAID controller** (30)</span></span>


</dt> <dd>

<span data-ttu-id="df9ca-168">Cette instance représente un contrôleur de stockage RAID contenu dans un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="df9ca-168">This instance represents a RAID storage controller contained within a host computer.</span></span>

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span data-ttu-id="df9ca-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Boîtier** de l’appareil de stockage (31)</span><span class="sxs-lookup"><span data-stu-id="df9ca-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Storage Device Enclosure** (31)</span></span>


</dt> <dd>

<span data-ttu-id="df9ca-170">Cette instance représente un boîtier qui contient des dispositifs de stockage.</span><span class="sxs-lookup"><span data-stu-id="df9ca-170">This instance represents an enclosure that contains storage devices.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="df9ca-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Bureau** (32)</span><span class="sxs-lookup"><span data-stu-id="df9ca-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="df9ca-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Ordinateur portable** (33)</span><span class="sxs-lookup"><span data-stu-id="df9ca-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span data-ttu-id="df9ca-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Bibliothèque de bandes virtuelle** (34)</span><span class="sxs-lookup"><span data-stu-id="df9ca-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Virtual Tape Library** (34)</span></span>


</dt> <dd>

<span data-ttu-id="df9ca-174">Émulation d’une bibliothèque de bandes par un système de bibliothèque virtuelle.</span><span class="sxs-lookup"><span data-stu-id="df9ca-174">The emulation of a tape library by a Virtual Library System.</span></span>

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span data-ttu-id="df9ca-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Système de bibliothèque virtuelle** (35)</span><span class="sxs-lookup"><span data-stu-id="df9ca-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Virtual Library System** (35)</span></span>


</dt> <dd>

<span data-ttu-id="df9ca-176">Utilise le stockage sur disque pour émuler les bibliothèques de bandes</span><span class="sxs-lookup"><span data-stu-id="df9ca-176">Uses disk storage to emulate tape libraries</span></span>

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span data-ttu-id="df9ca-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**PC réseau/client léger** (36)</span><span class="sxs-lookup"><span data-stu-id="df9ca-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Network PC/Thin Client** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span data-ttu-id="df9ca-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**Commutateur FC** (37)</span><span class="sxs-lookup"><span data-stu-id="df9ca-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**FC Switch** (37)</span></span>


</dt> <dd>

<span data-ttu-id="df9ca-179">Dédié au basculement des frames Fibre Channel de couche 2.</span><span class="sxs-lookup"><span data-stu-id="df9ca-179">Dedicated to switching layer 2 fibre channel frames.</span></span>

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span data-ttu-id="df9ca-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Commutateur Ethernet** (38)</span><span class="sxs-lookup"><span data-stu-id="df9ca-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Ethernet Switch** (38)</span></span>


</dt> <dd>

<span data-ttu-id="df9ca-181">Dédié au basculement des frames Ethernet de couche 2</span><span class="sxs-lookup"><span data-stu-id="df9ca-181">Dedicated to switching layer 2 ethernet frames</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="df9ca-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="df9ca-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="df9ca-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32568.. 65535)</span><span class="sxs-lookup"><span data-stu-id="df9ca-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32568..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9ca-184">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="df9ca-184">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9ca-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df9ca-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9ca-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df9ca-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9ca-187">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="df9ca-187">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="df9ca-188">Format du nom du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="df9ca-188">The format of the computer system name.</span></span>

<dt>



 <span data-ttu-id="df9ca-189">(« Autre »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-189">("Other")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-190">(« IP »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-190">("IP")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-191">(« Dial »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-191">("Dial")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-192">(« HID »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-192">("HID")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-193">(« NWA »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-193">("NWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-194">("HWA")</span><span class="sxs-lookup"><span data-stu-id="df9ca-194">("HWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-195">(« X25 »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-195">("X25")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-196">(« RNIS »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-196">("ISDN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-197">(« IPX »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-197">("IPX")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-198">(« DCC »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-198">("DCC")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-199">(« ICD »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-199">("ICD")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-200">(« E. 164 »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-200">("E.164")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-201">(« SNA »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-201">("SNA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-202">(« OID/OSI »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-202">("OID/OSI")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-203">(« WWN »)</span><span class="sxs-lookup"><span data-stu-id="df9ca-203">("WWN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="df9ca-204">("NAA")</span><span class="sxs-lookup"><span data-stu-id="df9ca-204">("NAA")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9ca-205">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="df9ca-205">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9ca-206">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="df9ca-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df9ca-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df9ca-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9ca-208">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ CIM**.**Dédié**»)</span><span class="sxs-lookup"><span data-stu-id="df9ca-208">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**Dedicated**")</span></span>
</dt> </dl>

<span data-ttu-id="df9ca-209">Décrit comment ou pourquoi le système est dédié lorsque le tableau **dédié** comprend la valeur 2 (autre).</span><span class="sxs-lookup"><span data-stu-id="df9ca-209">Describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="df9ca-210">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="df9ca-210">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9ca-211">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9ca-211">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df9ca-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df9ca-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9ca-213">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Contrôle d’alimentation du système DMTF \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="df9ca-213">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="df9ca-214">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="df9ca-214">This property is deprecated.</span></span> <span data-ttu-id="df9ca-215">Utilisez plutôt la méthode **PowerChangeCapabilities** dans la classe **CIM \_ PowerManagementCapabilitiesCIM \_ PowerManagementService** .</span><span class="sxs-lookup"><span data-stu-id="df9ca-215">Instead, use the **PowerChangeCapabilities** method in the **CIM\_PowerManagementCapabilitiesCIM\_PowerManagementService** class.</span></span>

<span data-ttu-id="df9ca-216">**Description déconseillée :** Les fonctionnalités de gestion de l’alimentation du système.</span><span class="sxs-lookup"><span data-stu-id="df9ca-216">**Deprecated description:** The power management capabilities of the system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9ca-217">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="df9ca-217">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="df9ca-218">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="df9ca-218">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="df9ca-219">**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="df9ca-219">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="df9ca-220">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="df9ca-220">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="df9ca-221">**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="df9ca-221">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="df9ca-222">**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="df9ca-222">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="df9ca-223">**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="df9ca-223">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="df9ca-224">**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="df9ca-224">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9ca-225">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="df9ca-225">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9ca-226">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9ca-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9ca-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df9ca-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9ca-228">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Hardware Security \| 001,4»)</span><span class="sxs-lookup"><span data-stu-id="df9ca-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="df9ca-229">Indique si le système prend en charge l’opération de réinitialisation matérielle.</span><span class="sxs-lookup"><span data-stu-id="df9ca-229">Indicates whether the system supports the hardware reset operation.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9ca-230">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="df9ca-230">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9ca-231">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="df9ca-231">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="df9ca-232">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="df9ca-232">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="df9ca-233">**Activé** (4)</span><span class="sxs-lookup"><span data-stu-id="df9ca-233">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="df9ca-234">**Non implémenté** (5)</span><span class="sxs-lookup"><span data-stu-id="df9ca-234">**Not Implemented** (5)</span></span>


<span data-ttu-id="df9ca-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="df9ca-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="df9ca-236">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df9ca-236">Requirements</span></span>



| <span data-ttu-id="df9ca-237">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df9ca-237">Requirement</span></span> | <span data-ttu-id="df9ca-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="df9ca-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df9ca-239">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df9ca-239">Minimum supported client</span></span><br/> | <span data-ttu-id="df9ca-240">Windows 8</span><span class="sxs-lookup"><span data-stu-id="df9ca-240">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="df9ca-241">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df9ca-241">Minimum supported server</span></span><br/> | <span data-ttu-id="df9ca-242">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df9ca-242">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="df9ca-243">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="df9ca-243">Namespace</span></span><br/>                | <span data-ttu-id="df9ca-244">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="df9ca-244">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="df9ca-245">MOF</span><span class="sxs-lookup"><span data-stu-id="df9ca-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df9ca-246"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df9ca-246"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df9ca-247">DLL</span><span class="sxs-lookup"><span data-stu-id="df9ca-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df9ca-248"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df9ca-248"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="df9ca-249">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df9ca-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9ca-250">**\_Système CIM**</span><span class="sxs-lookup"><span data-stu-id="df9ca-250">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

