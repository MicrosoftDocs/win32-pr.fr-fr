---
description: La \_ classe CIM UnitaryComputerSystem représente un ordinateur de bureau, mobile, réseau, serveur ou tout autre type de système informatique à nœud unique.
ms.assetid: c696050d-c921-4056-adc7-e4a2e9f4e119
ms.tgt_platform: multiple
title: Classe CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem
- CIM_UnitaryComputerSystem.Caption
- CIM_UnitaryComputerSystem.CreationClassName
- CIM_UnitaryComputerSystem.Description
- CIM_UnitaryComputerSystem.InitialLoadInfo
- CIM_UnitaryComputerSystem.InstallDate
- CIM_UnitaryComputerSystem.LastLoadInfo
- CIM_UnitaryComputerSystem.Name
- CIM_UnitaryComputerSystem.NameFormat
- CIM_UnitaryComputerSystem.PowerManagementCapabilities
- CIM_UnitaryComputerSystem.PowerManagementSupported
- CIM_UnitaryComputerSystem.PowerState
- CIM_UnitaryComputerSystem.PrimaryOwnerContact
- CIM_UnitaryComputerSystem.PrimaryOwnerName
- CIM_UnitaryComputerSystem.ResetCapability
- CIM_UnitaryComputerSystem.Roles
- CIM_UnitaryComputerSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e14812fda7971ffe045e8e36752c983cf5350402
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950490"
---
# <a name="cim_unitarycomputersystem-class"></a><span data-ttu-id="4c02a-103">\_Classe CIM UnitaryComputerSystem</span><span class="sxs-lookup"><span data-stu-id="4c02a-103">CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="4c02a-104">La classe **CIM \_ UnitaryComputerSystem** représente un ordinateur de bureau, mobile, réseau, serveur ou tout autre type de système informatique à nœud unique.</span><span class="sxs-lookup"><span data-stu-id="4c02a-104">The **CIM\_UnitaryComputerSystem** class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c02a-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4c02a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4c02a-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4c02a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4c02a-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4c02a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4c02a-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4c02a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c02a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c02a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C526-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UnitaryComputerSystem : CIM_ComputerSystem
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  string   InitialLoadInfo[];
  datetime InstallDate;
  string   LastLoadInfo;
  string   Name;
  string   NameFormat;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  string   Roles[];
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="4c02a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4c02a-110">Members</span></span>

<span data-ttu-id="4c02a-111">La classe **CIM \_ UnitaryComputerSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4c02a-111">The **CIM\_UnitaryComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="4c02a-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4c02a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4c02a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4c02a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4c02a-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4c02a-114">Methods</span></span>

<span data-ttu-id="4c02a-115">La classe **CIM \_ UnitaryComputerSystem** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4c02a-115">The **CIM\_UnitaryComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="4c02a-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="4c02a-116">Method</span></span>                                                                           | <span data-ttu-id="4c02a-117">Description</span><span class="sxs-lookup"><span data-stu-id="4c02a-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c02a-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4c02a-118">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md) | <span data-ttu-id="4c02a-119">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="4c02a-119">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="4c02a-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="4c02a-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4c02a-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4c02a-121">Properties</span></span>

<span data-ttu-id="4c02a-122">La classe **CIM \_ UnitaryComputerSystem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4c02a-122">The **CIM\_UnitaryComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c02a-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4c02a-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c02a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-126">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-127">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4c02a-127">Short textual description of the object.</span></span>

<span data-ttu-id="4c02a-128">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4c02a-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c02a-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-132">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4c02a-132">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-133">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="4c02a-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4c02a-134">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="4c02a-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4c02a-135">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-135">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-136">**Description**</span><span class="sxs-lookup"><span data-stu-id="4c02a-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c02a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-139">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4c02a-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-140">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4c02a-140">Textual description of the object.</span></span>

<span data-ttu-id="4c02a-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-142">**InitialLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="4c02a-142">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-143">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4c02a-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-145">Données nécessaires pour trouver l’unité de charge initiale (sa clé) ou le service de démarrage pour demander le démarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4c02a-145">Data needed to find either the initial load device (its key) or the boot service to request the operating system to start.</span></span> <span data-ttu-id="4c02a-146">En outre, les paramètres de chargement (autrement dit, un nom de chemin d’accès et des paramètres) peuvent également être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="4c02a-146">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4c02a-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-148">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4c02a-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-150">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="4c02a-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-151">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4c02a-151">Date and time the object was installed.</span></span> <span data-ttu-id="4c02a-152">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="4c02a-152">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4c02a-153">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-154">**LastLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="4c02a-154">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c02a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-157">Données qui identifient l’unité de charge initiale (sa clé) ou le service de démarrage qui a demandé la dernière charge du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4c02a-157">Data that identifies either the initial load device (its key) or the boot service that requested the last operating system load.</span></span> <span data-ttu-id="4c02a-158">En outre, les paramètres de chargement (autrement dit, un nom de chemin d’accès et des paramètres) peuvent également être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="4c02a-158">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-159">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4c02a-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c02a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-162">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c02a-162">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-163">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="4c02a-163">Label by which the object is known.</span></span> <span data-ttu-id="4c02a-164">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="4c02a-164">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4c02a-165">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-166">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="4c02a-166">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c02a-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-169">L' [**objet \_ ComputerSystem CIM**](cim-computersystem.md) et ses dérivés sont des objets de niveau supérieur de CIM qui fournissent l’étendue de nombreux composants et requièrent des clés [**\_ système CIM**](cim-system.md) uniques.</span><span class="sxs-lookup"><span data-stu-id="4c02a-169">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of CIM that provide the scope for numerous components and require unique [**CIM\_System**](cim-system.md) keys.</span></span> <span data-ttu-id="4c02a-170">Une heuristique est définie pour créer le **nom \_ ComputerSystem CIM** en vue de toujours générer le même nom système, indépendamment du protocole de découverte.</span><span class="sxs-lookup"><span data-stu-id="4c02a-170">A heuristic is defined to create the **CIM\_ComputerSystem** name in an attempt to always generate the same system name, independent of discovery protocol.</span></span> <span data-ttu-id="4c02a-171">Cela empêche les problèmes d’inventaire et de gestion où la même ressource ou entité est découverte plusieurs fois, mais ne peut pas être résolue en un seul objet.</span><span class="sxs-lookup"><span data-stu-id="4c02a-171">This prevents inventory and management problems where the same asset or entity is discovered multiple times, but cannot be resolved to a single object.</span></span> <span data-ttu-id="4c02a-172">Cette propriété identifie la manière dont le nom du système a été généré à l’aide de la méthode heuristique de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="4c02a-172">This property identifies how the system name was generated by using the subclass heuristic.</span></span> <span data-ttu-id="4c02a-173">L’heuristique est décrite dans la spécification CIM v2 Common Model Specification et suppose que les règles documentées sont parcourues pour déterminer et assigner un nom.</span><span class="sxs-lookup"><span data-stu-id="4c02a-173">The heuristic is outlined in the CIM V2 Common Model specification and assumes that the documented rules are traversed to determine and assign a name.</span></span> <span data-ttu-id="4c02a-174">La liste de valeurs **NameFormat** définit l’ordre de priorité pour l’affectation du nom système avec plusieurs règles qui mappent à la même valeur.</span><span class="sxs-lookup"><span data-stu-id="4c02a-174">The **NameFormat** values list defines the precedence order for assigning the system name with several rules mapping to the same value.</span></span> <span data-ttu-id="4c02a-175">Notez que le **nom \_ CIM CIM** qui est calculé à l’aide de la méthode heuristique est la valeur de clé du système.</span><span class="sxs-lookup"><span data-stu-id="4c02a-175">Note that the **CIM\_ComputerSystem** name that is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="4c02a-176">D’autres noms peuvent être attribués et utilisés pour le **\_ ComputerSystem CIM** qui répondent mieux aux besoins de l’entreprise, à l’aide d’alias.</span><span class="sxs-lookup"><span data-stu-id="4c02a-176">Other names can be assigned and used for the **CIM\_ComputerSystem** that better suit the business, using aliases.</span></span>

<span data-ttu-id="4c02a-177">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-177">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="4c02a-178">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c02a-178">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="4c02a-179">**IP** (« IP »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-179">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="4c02a-180">**Composer** (« composer »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-180">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="4c02a-181">**HID** (« HID »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-181">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="4c02a-182">**NWA** (« NWA »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-182">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="4c02a-183">**Hwa** (« Hwa »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-183">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="4c02a-184">**X25** (« x25 »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-184">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="4c02a-185">**RNIS** (« RNIS »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-185">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="4c02a-186">**IPX** (« IPX »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-186">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="4c02a-187">**DCC** (« DCC »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-187">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="4c02a-188">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="4c02a-188">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="4c02a-189">**E. 164** ("e. 164")</span><span class="sxs-lookup"><span data-stu-id="4c02a-189">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="4c02a-190">**SNA** (« SNA »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-190">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="4c02a-191">**OID/OSI** (« OID/OSI »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-191">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4c02a-192">**Autre** (« autre »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-192">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4c02a-193">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4c02a-193">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-194">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4c02a-194">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-196">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Contrôle d’alimentation du système DMTF \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="4c02a-196">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-197">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="4c02a-197">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="4c02a-198">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="4c02a-198">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4c02a-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4c02a-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4c02a-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="4c02a-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4c02a-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="4c02a-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4c02a-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="4c02a-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-203">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="4c02a-203">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4c02a-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="4c02a-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-205">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="4c02a-205">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4c02a-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="4c02a-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-207">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4c02a-207">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="4c02a-208">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="4c02a-208">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="4c02a-209">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="4c02a-209">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4c02a-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="4c02a-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-211">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="4c02a-211">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4c02a-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="4c02a-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-213">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="4c02a-213">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4c02a-214">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4c02a-214">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-215">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4c02a-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-217">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="4c02a-217">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="4c02a-218">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="4c02a-218">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="4c02a-219">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4c02a-219">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="4c02a-220">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="4c02a-220">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-221">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="4c02a-221">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-222">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4c02a-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-224">État actuel de l’alimentation du système informatique et du système d’exploitation qui lui est associé.</span><span class="sxs-lookup"><span data-stu-id="4c02a-224">Current power state of the computer system and its associated operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4c02a-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4c02a-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-226">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="4c02a-226">Unknown.</span></span>

</dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="4c02a-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Pleine puissance** (1)</span><span class="sxs-lookup"><span data-stu-id="4c02a-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-228">Toute la puissance.</span><span class="sxs-lookup"><span data-stu-id="4c02a-228">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4c02a-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (2)</span><span class="sxs-lookup"><span data-stu-id="4c02a-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-230">Le système est dans un état d’économie d’énergie et fonctionne toujours, mais peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="4c02a-230">System is in a power-save state and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4c02a-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (3)</span><span class="sxs-lookup"><span data-stu-id="4c02a-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-232">Le système ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="4c02a-232">System is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4c02a-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (4)</span><span class="sxs-lookup"><span data-stu-id="4c02a-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-234">Le système est connu pour être en mode économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="4c02a-234">System is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4c02a-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (5)</span><span class="sxs-lookup"><span data-stu-id="4c02a-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-236">Cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="4c02a-236">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4c02a-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (6)</span><span class="sxs-lookup"><span data-stu-id="4c02a-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-238">Mise hors tension.</span><span class="sxs-lookup"><span data-stu-id="4c02a-238">Power off.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4c02a-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (7)</span><span class="sxs-lookup"><span data-stu-id="4c02a-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-240">Le système est dans un état d’avertissement et également dans un mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="4c02a-240">System is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="4c02a-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>Économie **d’énergie-mise en veille prolongée** (8)</span><span class="sxs-lookup"><span data-stu-id="4c02a-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-242">Économie d’énergie en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="4c02a-242">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="4c02a-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Économie **d’énergie-désactivation douce** (9)</span><span class="sxs-lookup"><span data-stu-id="4c02a-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="4c02a-244">Économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="4c02a-244">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4c02a-245">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="4c02a-245">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c02a-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-248">Chaîne qui fournit des informations sur la façon d’atteindre le propriétaire du système principal (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="4c02a-248">String that provides information on how to reach the primary system owner (for example, phone number, email address, and so on).</span></span>

<span data-ttu-id="4c02a-249">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-249">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-250">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="4c02a-250">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c02a-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-253">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4c02a-253">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-254">Nom du propriétaire du système principal.</span><span class="sxs-lookup"><span data-stu-id="4c02a-254">Name of the primary system owner.</span></span>

<span data-ttu-id="4c02a-255">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-255">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-256">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="4c02a-256">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-257">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4c02a-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-259">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Hardware Security \| 001,4»)</span><span class="sxs-lookup"><span data-stu-id="4c02a-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-260">S’il est activé, le système d’ordinateur unitaire peut être réinitialisé avec le matériel (par exemple, avec les boutons d’alimentation et de réinitialisation).</span><span class="sxs-lookup"><span data-stu-id="4c02a-260">If enabled, the unitary computer system can be reset with hardware (for example, with the power and reset buttons).</span></span> <span data-ttu-id="4c02a-261">Si elle est désactivée, la réinitialisation matérielle n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="4c02a-261">If disabled, hardware reset is not allowed.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4c02a-262">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4c02a-262">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4c02a-263">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4c02a-263">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4c02a-264">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="4c02a-264">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4c02a-265">**Activé** (4)</span><span class="sxs-lookup"><span data-stu-id="4c02a-265">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="4c02a-266">**Non implémenté** (5)</span><span class="sxs-lookup"><span data-stu-id="4c02a-266">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4c02a-267">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="4c02a-267">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-268">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4c02a-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-269">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4c02a-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-270">Rôles joués par le système dans l’environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="4c02a-270">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="4c02a-271">Les sous-classes du système peuvent remplacer cette propriété pour définir des valeurs de rôle explicites.</span><span class="sxs-lookup"><span data-stu-id="4c02a-271">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="4c02a-272">Un groupe de travail peut également décrire les heuristiques, les conventions et les instructions pour la spécification des rôles.</span><span class="sxs-lookup"><span data-stu-id="4c02a-272">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="4c02a-273">Par exemple, pour une instance d’un système de mise en réseau, cette propriété peut contenir la chaîne « Switch » ou « Bridge ».</span><span class="sxs-lookup"><span data-stu-id="4c02a-273">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="4c02a-274">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-274">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c02a-275">**État**</span><span class="sxs-lookup"><span data-stu-id="4c02a-275">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c02a-276">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4c02a-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c02a-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c02a-278">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="4c02a-278">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4c02a-279">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4c02a-279">Current status of the object.</span></span> <span data-ttu-id="4c02a-280">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4c02a-281">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c02a-281">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4c02a-282">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-282">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4c02a-283">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-283">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4c02a-284">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-284">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4c02a-285">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="4c02a-285">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4c02a-286">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-286">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4c02a-287">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-287">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4c02a-288">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-288">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4c02a-289">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-289">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4c02a-290">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-290">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4c02a-291">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-291">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4c02a-292">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-292">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4c02a-293">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="4c02a-293">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="4c02a-294"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4c02a-294"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="4c02a-295">Notes</span><span class="sxs-lookup"><span data-stu-id="4c02a-295">Remarks</span></span>

<span data-ttu-id="4c02a-296">La classe **CIM \_ UnitaryComputerSystem** est dérivée de [**CIM \_ ComputerSystem**](cim-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-296">The **CIM\_UnitaryComputerSystem** class is derived from [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="4c02a-297">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="4c02a-297">WMI does not implement this class.</span></span> <span data-ttu-id="4c02a-298">Pour les classes WMI dérivées de **CIM \_ UnitaryComputerSystem**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4c02a-298">For WMI classes derived from **CIM\_UnitaryComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4c02a-299">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4c02a-299">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4c02a-300">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4c02a-300">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c02a-301">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c02a-301">Requirements</span></span>



| <span data-ttu-id="4c02a-302">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c02a-302">Requirement</span></span> | <span data-ttu-id="4c02a-303">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c02a-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c02a-304">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c02a-304">Minimum supported client</span></span><br/> | <span data-ttu-id="4c02a-305">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c02a-305">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c02a-306">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c02a-306">Minimum supported server</span></span><br/> | <span data-ttu-id="4c02a-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c02a-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c02a-308">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4c02a-308">Namespace</span></span><br/>                | <span data-ttu-id="4c02a-309">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4c02a-309">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4c02a-310">MOF</span><span class="sxs-lookup"><span data-stu-id="4c02a-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c02a-311"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c02a-311"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c02a-312">DLL</span><span class="sxs-lookup"><span data-stu-id="4c02a-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c02a-313"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c02a-313"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c02a-314">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c02a-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c02a-315">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="4c02a-315">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

