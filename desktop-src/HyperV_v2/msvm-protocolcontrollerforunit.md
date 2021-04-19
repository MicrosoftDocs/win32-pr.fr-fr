---
description: Cette Association indique qu’une sous-classe de l’unité logique (par exemple, un volume de stockage) est connectée par le biais d’un contrôleur de protocole spécifique.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Classe Msvm_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536998"
---
# <a name="msvm_protocolcontrollerforunit-class"></a><span data-ttu-id="53ca0-103">MSVM \_ ProtocolControllerForUnit, classe</span><span class="sxs-lookup"><span data-stu-id="53ca0-103">Msvm\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="53ca0-104">Cette Association indique qu’une sous-classe de l’unité logique (par exemple, un volume de stockage) est connectée par le biais d’un contrôleur de protocole spécifique.</span><span class="sxs-lookup"><span data-stu-id="53ca0-104">This association indicates that a subclass of logical device (for example a storage volume) is connected through a specific protocol controller.</span></span> <span data-ttu-id="53ca0-105">Dans de nombreux cas (par exemple, le masquage de LUN de stockage), de nombreuses associations peuvent être utilisées pour établir un lien avec différents objets.</span><span class="sxs-lookup"><span data-stu-id="53ca0-105">In many situations (for example storage LUN masking), there may be many of these associations used to relate to different objects.</span></span> <span data-ttu-id="53ca0-106">Par conséquent, des sous-classes ont été définies pour optimiser l’énumération des associations.</span><span class="sxs-lookup"><span data-stu-id="53ca0-106">Therefore, subclasses have been defined to optimize enumeration of the associations.</span></span>

<span data-ttu-id="53ca0-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="53ca0-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="53ca0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53ca0-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="53ca0-109">Membres</span><span class="sxs-lookup"><span data-stu-id="53ca0-109">Members</span></span>

<span data-ttu-id="53ca0-110">La classe **MSVM \_ ProtocolControllerForUnit** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="53ca0-110">The **Msvm\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="53ca0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="53ca0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53ca0-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="53ca0-112">Properties</span></span>

<span data-ttu-id="53ca0-113">La classe **MSVM \_ ProtocolControllerForUnit** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="53ca0-113">The **Msvm\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53ca0-114">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="53ca0-114">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53ca0-115">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53ca0-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53ca0-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53ca0-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53ca0-117">Priorité donnée aux accès de l’appareil par le biais de ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="53ca0-117">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="53ca0-118">Le chemin d’accès avec la priorité la plus élevée aura la valeur la plus faible pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="53ca0-118">The highest priority path will have the lowest value for this parameter.</span></span> <span data-ttu-id="53ca0-119">Cette classe est héritée de **CIM \_ ProtocolControllerForDevice**.</span><span class="sxs-lookup"><span data-stu-id="53ca0-119">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> <dt>

<span data-ttu-id="53ca0-120">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="53ca0-120">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53ca0-121">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53ca0-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53ca0-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53ca0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53ca0-123">Indique si le contrôleur commande ou accède activement à l’appareil (2) ou non (3).</span><span class="sxs-lookup"><span data-stu-id="53ca0-123">Indicates whether the controller is actively commanding or accessing the device (2) or not (3).</span></span> <span data-ttu-id="53ca0-124">En outre, la valeur 0 (inconnu) peut être définie.</span><span class="sxs-lookup"><span data-stu-id="53ca0-124">Also, the value, 0 (Unknown), can be defined.</span></span> <span data-ttu-id="53ca0-125">Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par des contrôleurs de protocole, ou être accessible via plusieurs contrôleurs de protocole.</span><span class="sxs-lookup"><span data-stu-id="53ca0-125">This information is necessary when a logical device can be commanded by, or accessed through, multiple protocol controllers.</span></span> <span data-ttu-id="53ca0-126">Cette classe est héritée de **CIM \_ ProtocolControllerForDevice**.</span><span class="sxs-lookup"><span data-stu-id="53ca0-126">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

<dl> <dt>

<span data-ttu-id="53ca0-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="53ca0-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="53ca0-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Actif** (2)</span><span class="sxs-lookup"><span data-stu-id="53ca0-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Active** (2)</span></span>
</dt> <dt>

<span data-ttu-id="53ca0-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactif** (3)</span><span class="sxs-lookup"><span data-stu-id="53ca0-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactive** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="53ca0-130">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="53ca0-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53ca0-131">Type de données : **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span><span class="sxs-lookup"><span data-stu-id="53ca0-131">Data type: **[**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span></span>
</dt> <dt>

<span data-ttu-id="53ca0-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53ca0-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53ca0-133">Contrôleur de protocole.</span><span class="sxs-lookup"><span data-stu-id="53ca0-133">The protocol controller.</span></span> <span data-ttu-id="53ca0-134">Cette classe est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="53ca0-134">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="53ca0-135">**Charge**</span><span class="sxs-lookup"><span data-stu-id="53ca0-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53ca0-136">Type de données : **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="53ca0-136">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="53ca0-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53ca0-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53ca0-138">Périphérique contrôlé.</span><span class="sxs-lookup"><span data-stu-id="53ca0-138">The controlled device.</span></span> <span data-ttu-id="53ca0-139">Cette classe est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="53ca0-139">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="53ca0-140">**DeviceAccess**</span><span class="sxs-lookup"><span data-stu-id="53ca0-140">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53ca0-141">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53ca0-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53ca0-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53ca0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53ca0-143">Droits d’accès accordés à l’appareil via ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="53ca0-143">The access rights granted to the device through this controller.</span></span> <span data-ttu-id="53ca0-144">Cette classe est héritée de **CIM \_ ProtocolControllerForUnit**.</span><span class="sxs-lookup"><span data-stu-id="53ca0-144">This class is inherited from **CIM\_ProtocolControllerForUnit**.</span></span>



| <span data-ttu-id="53ca0-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="53ca0-145">Value</span></span>                                                                               | <span data-ttu-id="53ca0-146">Signification</span><span class="sxs-lookup"><span data-stu-id="53ca0-146">Meaning</span></span>                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="53ca0-147"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="53ca0-147"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="53ca0-148">Unknown</span><span class="sxs-lookup"><span data-stu-id="53ca0-148">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="53ca0-149"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="53ca0-149"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="53ca0-150">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="53ca0-150">Read/Write</span></span><br/>      |
| <dl> <span data-ttu-id="53ca0-151"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="53ca0-151"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="53ca0-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53ca0-152">Read-only</span></span><br/>       |
| <dl> <span data-ttu-id="53ca0-153"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="53ca0-153"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="53ca0-154">Pas d'accès.</span><span class="sxs-lookup"><span data-stu-id="53ca0-154">No access.</span></span><br/>      |
| <dl> <span data-ttu-id="53ca0-155"><dt>5.. 15999</dt></span><span class="sxs-lookup"><span data-stu-id="53ca0-155"><dt>5..15999</dt></span></span> </dl> | <span data-ttu-id="53ca0-156">DMTF, réservé</span><span class="sxs-lookup"><span data-stu-id="53ca0-156">DMTF Reserved</span></span><br/>   |
| <dl> <span data-ttu-id="53ca0-157"><dt>16000..</dt></span><span class="sxs-lookup"><span data-stu-id="53ca0-157"><dt>16000..</dt></span></span> </dl>  | <span data-ttu-id="53ca0-158">Fournisseur réservé</span><span class="sxs-lookup"><span data-stu-id="53ca0-158">Vendor reserved</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="53ca0-159">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="53ca0-159">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53ca0-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="53ca0-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53ca0-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53ca0-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53ca0-162">Adresse de l’appareil associé dans le contexte du contrôleur antécédent.</span><span class="sxs-lookup"><span data-stu-id="53ca0-162">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="53ca0-163">Cette classe est héritée de **CIM \_ ProtocolControllerForDevice**.</span><span class="sxs-lookup"><span data-stu-id="53ca0-163">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53ca0-164">Notes</span><span class="sxs-lookup"><span data-stu-id="53ca0-164">Remarks</span></span>

<span data-ttu-id="53ca0-165">L’accès à la classe **MSVM \_ ProtocolControllerForUnit** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="53ca0-165">Access to the **Msvm\_ProtocolControllerForUnit** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="53ca0-166">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="53ca0-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="53ca0-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53ca0-167">Requirements</span></span>



| <span data-ttu-id="53ca0-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53ca0-168">Requirement</span></span> | <span data-ttu-id="53ca0-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="53ca0-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53ca0-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53ca0-170">Minimum supported client</span></span><br/> | <span data-ttu-id="53ca0-171">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53ca0-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="53ca0-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53ca0-172">Minimum supported server</span></span><br/> | <span data-ttu-id="53ca0-173">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53ca0-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53ca0-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="53ca0-174">Namespace</span></span><br/>                | <span data-ttu-id="53ca0-175">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="53ca0-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="53ca0-176">MOF</span><span class="sxs-lookup"><span data-stu-id="53ca0-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53ca0-177"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53ca0-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53ca0-178">DLL</span><span class="sxs-lookup"><span data-stu-id="53ca0-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53ca0-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53ca0-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53ca0-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53ca0-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ca0-181">**\_PROTOCOLCONTROLLERFORUNIT CIM**</span><span class="sxs-lookup"><span data-stu-id="53ca0-181">**CIM\_ProtocolControllerForUnit**</span></span>](cim-protocolcontrollerforunit.md)
</dt> <dt>

<span data-ttu-id="53ca0-182">[**\_PROTOCOLCONTROLLERFORUNIT CIM**](/previous-versions//cc150672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="53ca0-182">[**CIM\_ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="53ca0-183">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="53ca0-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

