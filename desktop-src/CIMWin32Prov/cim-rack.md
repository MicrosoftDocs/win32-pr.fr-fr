---
description: La \_ classe de rack CIM représente un rack (cadre physique ou boîtier) dans lequel les châssis sont stockés. En règle générale, un rack représente le boîtier. tous les composants fonctionnels sont empaquetés dans le châssis.
ms.assetid: 1e0273ce-2a09-4f75-a82e-d0555d6a831e
ms.tgt_platform: multiple
title: Classe CIM_Rack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack
- CIM_Rack.AudibleAlarm
- CIM_Rack.BreachDescription
- CIM_Rack.CableManagementStrategy
- CIM_Rack.Caption
- CIM_Rack.CountryDesignation
- CIM_Rack.CreationClassName
- CIM_Rack.Depth
- CIM_Rack.Description
- CIM_Rack.Height
- CIM_Rack.HotSwappable
- CIM_Rack.InstallDate
- CIM_Rack.LockPresent
- CIM_Rack.Manufacturer
- CIM_Rack.Model
- CIM_Rack.Name
- CIM_Rack.OtherIdentifyingInfo
- CIM_Rack.PartNumber
- CIM_Rack.PoweredOn
- CIM_Rack.Removable
- CIM_Rack.Replaceable
- CIM_Rack.SecurityBreach
- CIM_Rack.SerialNumber
- CIM_Rack.ServiceDescriptions
- CIM_Rack.ServicePhilosophy
- CIM_Rack.SKU
- CIM_Rack.Status
- CIM_Rack.Tag
- CIM_Rack.TypeOfRack
- CIM_Rack.Version
- CIM_Rack.VisibleAlarm
- CIM_Rack.Weight
- CIM_Rack.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2eb5234e8dd65d7df86acec7ab121ef961c2121
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748236"
---
# <a name="cim_rack-class"></a><span data-ttu-id="12733-104">\_Classe de rack CIM</span><span class="sxs-lookup"><span data-stu-id="12733-104">CIM\_Rack class</span></span>

<span data-ttu-id="12733-105">La classe de **\_ rack CIM** représente un rack (cadre physique ou boîtier) dans lequel les châssis sont stockés.</span><span class="sxs-lookup"><span data-stu-id="12733-105">The **CIM\_Rack** class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="12733-106">En règle générale, un rack représente le boîtier. tous les composants fonctionnels sont empaquetés dans le châssis.</span><span class="sxs-lookup"><span data-stu-id="12733-106">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12733-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="12733-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="12733-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="12733-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="12733-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="12733-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="12733-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="12733-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12733-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12733-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B71-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Rack : CIM_PhysicalFrame
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CountryDesignation;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  uint16   TypeOfRack;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="12733-112">Membres</span><span class="sxs-lookup"><span data-stu-id="12733-112">Members</span></span>

<span data-ttu-id="12733-113">La classe de **\_ rack CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="12733-113">The **CIM\_Rack** class has these types of members:</span></span>

-   [<span data-ttu-id="12733-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="12733-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="12733-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="12733-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="12733-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="12733-116">Methods</span></span>

<span data-ttu-id="12733-117">La classe de **\_ rack CIM** présente ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="12733-117">The **CIM\_Rack** class has these methods.</span></span>



| <span data-ttu-id="12733-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="12733-118">Method</span></span>                                                        | <span data-ttu-id="12733-119">Description</span><span class="sxs-lookup"><span data-stu-id="12733-119">Description</span></span>                                                                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12733-120">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="12733-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-rack.md) | <span data-ttu-id="12733-121">Vérifie si l’élément physique référencé peut être contenu ou inséré dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="12733-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="12733-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="12733-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="12733-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="12733-123">Properties</span></span>

<span data-ttu-id="12733-124">La classe de **\_ rack CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="12733-124">The **CIM\_Rack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12733-125">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="12733-125">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-126">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12733-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12733-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12733-128">Si la **valeur est true**, le cadre est équipé d’une alarme sonore.</span><span class="sxs-lookup"><span data-stu-id="12733-128">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="12733-129">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="12733-129">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-130">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="12733-130">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-133">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="12733-133">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="12733-134">Chaîne de forme libre qui fournit des informations si la propriété **SecurityBreach** indique qu’une violation ou un autre événement lié à la sécurité s’est produit.</span><span class="sxs-lookup"><span data-stu-id="12733-134">Free-form string that provides information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="12733-135">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="12733-135">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-136">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="12733-136">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12733-139">Chaîne de forme libre qui contient des informations sur la façon dont les différents câbles sont connectés et regroupés pour le cadre.</span><span class="sxs-lookup"><span data-stu-id="12733-139">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="12733-140">Avec de nombreuses connexions réseau, liées au stockage et aux câbles d’alimentation, la gestion des câbles peut être un défi complexe et difficile.</span><span class="sxs-lookup"><span data-stu-id="12733-140">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="12733-141">Cette propriété de type chaîne contient des informations pour faciliter l’assembly et le service du frame.</span><span class="sxs-lookup"><span data-stu-id="12733-141">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="12733-142">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="12733-142">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-143">**Caption**</span><span class="sxs-lookup"><span data-stu-id="12733-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-146">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="12733-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="12733-147">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="12733-147">Short textual description of the object.</span></span>

<span data-ttu-id="12733-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-149">**CountryDesignation**</span><span class="sxs-lookup"><span data-stu-id="12733-149">**CountryDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-152">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ rack CIM**.**TypeOfRack**")</span><span class="sxs-lookup"><span data-stu-id="12733-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**TypeOfRack**")</span></span>
</dt> </dl>

<span data-ttu-id="12733-153">Pays ou région pour lequel le rack est conçu.</span><span class="sxs-lookup"><span data-stu-id="12733-153">Country or region for which the rack is designed.</span></span> <span data-ttu-id="12733-154">Les chaînes de code du pays ou de la région sont définies par la norme ISO/IEC 3166.</span><span class="sxs-lookup"><span data-stu-id="12733-154">Country or region code strings are as defined by ISO/IEC 3166.</span></span> <span data-ttu-id="12733-155">Le type de rack est spécifié dans la propriété **TypeOfRack** .</span><span class="sxs-lookup"><span data-stu-id="12733-155">The rack type is specified in the **TypeOfRack** property.</span></span>

</dd> <dt>

<span data-ttu-id="12733-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="12733-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-159">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="12733-159">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="12733-160">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="12733-160">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="12733-161">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="12733-161">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="12733-162">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-162">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-163">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="12733-163">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-164">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="12733-164">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="12733-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-166">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="12733-166">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="12733-167">Profondeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="12733-167">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="12733-168">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="12733-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-169">**Description**</span><span class="sxs-lookup"><span data-stu-id="12733-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-172">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="12733-172">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="12733-173">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="12733-173">Textual description of the object.</span></span>

<span data-ttu-id="12733-174">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-175">**Height**</span><span class="sxs-lookup"><span data-stu-id="12733-175">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-176">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="12733-176">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="12733-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-178">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("height"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")</span><span class="sxs-lookup"><span data-stu-id="12733-178">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Height"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="12733-179">Hauteur du package physique, à l’aide de l’unité de mesure « U ».</span><span class="sxs-lookup"><span data-stu-id="12733-179">Height of the physical package, using the "U" unit of measure.</span></span> <span data-ttu-id="12733-180">Un « U » est une unité de mesure standard pour la hauteur d’un rack, ou un composant montable en rack et est égal à 1,75 pouces ou 4,445 centimètres.</span><span class="sxs-lookup"><span data-stu-id="12733-180">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

<span data-ttu-id="12733-181">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="12733-181">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-182">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="12733-182">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-183">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12733-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12733-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12733-185">Si la **valeur est true**, le package peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="12733-185">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="12733-186">Un package physique peut être échangé à chaud si l’élément peut être remplacé par un différent physiquement (mais équivalent), alors que le package qui le contient est activé.</span><span class="sxs-lookup"><span data-stu-id="12733-186">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="12733-187">Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="12733-187">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="12733-188">Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="12733-188">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="12733-189">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="12733-189">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-190">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="12733-190">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-191">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="12733-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="12733-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-193">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="12733-193">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="12733-194">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="12733-194">Date and time the object was installed.</span></span> <span data-ttu-id="12733-195">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="12733-195">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="12733-196">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-197">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="12733-197">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-198">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12733-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12733-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12733-200">Si la **valeur est true**, le frame est protégé par un verrou.</span><span class="sxs-lookup"><span data-stu-id="12733-200">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="12733-201">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="12733-201">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-202">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="12733-202">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-205">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="12733-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="12733-206">Nom de l’organisation qui a produit l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="12733-206">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="12733-207">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="12733-207">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="12733-208">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-208">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-209">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="12733-209">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-212">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="12733-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="12733-213">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="12733-213">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="12733-214">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-214">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-215">**Nom**</span><span class="sxs-lookup"><span data-stu-id="12733-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-218">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="12733-218">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="12733-219">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="12733-219">Label by which the object is known.</span></span> <span data-ttu-id="12733-220">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="12733-220">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="12733-221">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-222">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="12733-222">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12733-225">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="12733-225">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="12733-226">Par exemple, les données de code-barres associées à un élément qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="12733-226">One example is bar-code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="12733-227">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="12733-228">Si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées comme clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="12733-228">If only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="12733-229">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="12733-229">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-232">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="12733-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="12733-233">Numéro de référence attribué par l’organisation qui a produit ou fabriqué l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="12733-233">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="12733-234">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-234">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-235">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="12733-235">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-236">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12733-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12733-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12733-238">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="12733-238">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="12733-239">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-240">**Bande**</span><span class="sxs-lookup"><span data-stu-id="12733-240">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-241">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12733-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12733-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12733-243">Si la **valeur est true**, cet élément est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global.</span><span class="sxs-lookup"><span data-stu-id="12733-243">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="12733-244">Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="12733-244">A package is considered removable even if the power must be "off" to perform the removal.</span></span> <span data-ttu-id="12733-245">Si l’alimentation peut être « activée » et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="12733-245">If the power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="12733-246">Par exemple, une batterie supplémentaire dans un ordinateur portable est amovible, comme c’est le cas d’un package de lecteur de disque inséré à l’aide de connecteurs SCA. Toutefois, cette dernière peut être permutée à chaud.</span><span class="sxs-lookup"><span data-stu-id="12733-246">For example, an extra battery in a laptop is removable, as is a disk-drive package inserted using SCA connectors; however, the latter can be hot-swapped.</span></span> <span data-ttu-id="12733-247">L’affichage d’un ordinateur portable n’est pas amovible et n’est pas une alimentation non redondante.</span><span class="sxs-lookup"><span data-stu-id="12733-247">A laptop's display is not removable, nor is a non-redundant power supply.</span></span> <span data-ttu-id="12733-248">La suppression de ces composants a un impact sur la fonction de l’ensemble de l’empaquetage ou est impossible en raison de l’intégration étroite du package.</span><span class="sxs-lookup"><span data-stu-id="12733-248">Removing these components impacts the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="12733-249">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="12733-249">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-250">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="12733-250">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-251">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12733-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12733-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12733-253">Si la **valeur est true**, il est possible de remplacer l’élément par un élément différent physiquement.</span><span class="sxs-lookup"><span data-stu-id="12733-253">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="12733-254">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="12733-254">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="12733-255">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="12733-255">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="12733-256">Tous les composants amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="12733-256">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="12733-257">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="12733-257">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-258">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="12733-258">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-259">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12733-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12733-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-261">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Table globale du conteneur physique DMTF \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="12733-261">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="12733-262">Indique si une violation physique du frame a été tentée, mais a échoué ou a été tentée et réussie.</span><span class="sxs-lookup"><span data-stu-id="12733-262">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span> <span data-ttu-id="12733-263">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="12733-263">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12733-264">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="12733-264">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12733-265">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="12733-265">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="12733-266">**Aucune violation** (3)</span><span class="sxs-lookup"><span data-stu-id="12733-266">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="12733-267">**Tentative de violation** (4)</span><span class="sxs-lookup"><span data-stu-id="12733-267">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="12733-268">**Violation réussie** (5)</span><span class="sxs-lookup"><span data-stu-id="12733-268">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12733-269">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="12733-269">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-270">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-272">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="12733-272">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="12733-273">Numéro alloué par le fabricant utilisé pour identifier le rack.</span><span class="sxs-lookup"><span data-stu-id="12733-273">Manufacturer-allocated number used to identify the rack.</span></span>

<span data-ttu-id="12733-274">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-274">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-275">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="12733-275">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-276">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="12733-276">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="12733-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-278">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="12733-278">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="12733-279">Chaînes de forme libre qui fournissent des explications détaillées sur les entrées dans le tableau **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="12733-279">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="12733-280">Notez que chaque entrée du tableau est liée à l’entrée dans **ServicePhilosophy** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="12733-280">Note, each entry of the array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="12733-281">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="12733-281">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-282">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="12733-282">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-283">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12733-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="12733-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-285">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="12733-285">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="12733-286">Indique si le frame est pris en service à partir du haut, de l’avant, de l’arrière ou du côté ; et s’il a des bacs coulissants ou des côtés amovibles, et si le cadre est mobile (par exemple, des rouleaux).</span><span class="sxs-lookup"><span data-stu-id="12733-286">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="12733-287">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="12733-287">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12733-288">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="12733-288">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12733-289">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="12733-289">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="12733-290">**Service à partir du haut** (2)</span><span class="sxs-lookup"><span data-stu-id="12733-290">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="12733-291">**Service à l’avant** (3)</span><span class="sxs-lookup"><span data-stu-id="12733-291">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="12733-292">**Service à partir de l’arrière** (4)</span><span class="sxs-lookup"><span data-stu-id="12733-292">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="12733-293">**Service de la côte** (5)</span><span class="sxs-lookup"><span data-stu-id="12733-293">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="12733-294">**Plateaux coulissants** (6)</span><span class="sxs-lookup"><span data-stu-id="12733-294">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="12733-295">**Côtés amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="12733-295">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="12733-296">**Mobile** (8)</span><span class="sxs-lookup"><span data-stu-id="12733-296">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12733-297">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="12733-297">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-298">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-300">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="12733-300">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="12733-301">Numéro d’unité de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="12733-301">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="12733-302">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-303">**État**</span><span class="sxs-lookup"><span data-stu-id="12733-303">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-306">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="12733-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="12733-307">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="12733-307">Current status of the object.</span></span> <span data-ttu-id="12733-308">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="12733-309">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="12733-309">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="12733-310">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="12733-310">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="12733-311">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="12733-311">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="12733-312">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="12733-312">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12733-313">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="12733-313">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="12733-314">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="12733-314">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="12733-315">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="12733-315">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="12733-316">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="12733-316">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="12733-317">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="12733-317">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="12733-318">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="12733-318">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="12733-319">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="12733-319">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="12733-320">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="12733-320">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="12733-321">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="12733-321">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12733-322">**Tag**</span><span class="sxs-lookup"><span data-stu-id="12733-322">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-323">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-325">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="12733-325">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="12733-326">Chaîne arbitraire qui identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="12733-326">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="12733-327">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="12733-327">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="12733-328">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="12733-328">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="12733-329">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="12733-329">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="12733-330">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="12733-330">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="12733-331">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="12733-331">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="12733-332">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-332">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-333">**TypeOfRack**</span><span class="sxs-lookup"><span data-stu-id="12733-333">**TypeOfRack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-334">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12733-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12733-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-336">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ rack CIM**.**CountryDesignation**")</span><span class="sxs-lookup"><span data-stu-id="12733-336">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**CountryDesignation**")</span></span>
</dt> </dl>

<span data-ttu-id="12733-337">Type de rack.</span><span class="sxs-lookup"><span data-stu-id="12733-337">Type of rack.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12733-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="12733-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>

<span data-ttu-id="12733-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**19 pouces standard** (1)</span><span class="sxs-lookup"><span data-stu-id="12733-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Standard 19 Inch** (1)</span></span>


</dt> <dd>

<span data-ttu-id="12733-340">19 pouces standard</span><span class="sxs-lookup"><span data-stu-id="12733-340">Standard 19-inch</span></span>

</dd> <dt>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>

<span data-ttu-id="12733-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span><span class="sxs-lookup"><span data-stu-id="12733-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>

<span data-ttu-id="12733-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Étagère d’équipement** (3)</span><span class="sxs-lookup"><span data-stu-id="12733-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Equipment Shelf** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>

<span data-ttu-id="12733-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Non standard** (4)</span><span class="sxs-lookup"><span data-stu-id="12733-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Non-Standard** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12733-344">**Version**</span><span class="sxs-lookup"><span data-stu-id="12733-344">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-345">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12733-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12733-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-347">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="12733-347">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="12733-348">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="12733-348">Version of the physical element.</span></span>

<span data-ttu-id="12733-349">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12733-349">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-350">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="12733-350">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-351">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12733-351">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12733-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12733-353">Si la **valeur est true**, l’équipement comprend une alarme visible.</span><span class="sxs-lookup"><span data-stu-id="12733-353">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="12733-354">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="12733-354">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-355">**Poids**</span><span class="sxs-lookup"><span data-stu-id="12733-355">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-356">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="12733-356">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="12733-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-358">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« livres »)</span><span class="sxs-lookup"><span data-stu-id="12733-358">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="12733-359">Poids du package physique, en livres.</span><span class="sxs-lookup"><span data-stu-id="12733-359">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="12733-360">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="12733-360">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="12733-361">**Width**</span><span class="sxs-lookup"><span data-stu-id="12733-361">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12733-362">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="12733-362">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="12733-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12733-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12733-364">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="12733-364">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="12733-365">Largeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="12733-365">Width of the physical package, in inches.</span></span>

<span data-ttu-id="12733-366">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="12733-366">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12733-367">Notes</span><span class="sxs-lookup"><span data-stu-id="12733-367">Remarks</span></span>

<span data-ttu-id="12733-368">La classe de **\_ rack CIM** est dérivée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="12733-368">The **CIM\_Rack** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="12733-369">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="12733-369">WMI does not implement this class.</span></span>

<span data-ttu-id="12733-370">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="12733-370">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="12733-371">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="12733-371">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="12733-372">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12733-372">Requirements</span></span>



| <span data-ttu-id="12733-373">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12733-373">Requirement</span></span> | <span data-ttu-id="12733-374">Valeur</span><span class="sxs-lookup"><span data-stu-id="12733-374">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12733-375">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12733-375">Minimum supported client</span></span><br/> | <span data-ttu-id="12733-376">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12733-376">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12733-377">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12733-377">Minimum supported server</span></span><br/> | <span data-ttu-id="12733-378">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12733-378">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12733-379">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="12733-379">Namespace</span></span><br/>                | <span data-ttu-id="12733-380">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="12733-380">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12733-381">MOF</span><span class="sxs-lookup"><span data-stu-id="12733-381">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12733-382"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12733-382"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12733-383">DLL</span><span class="sxs-lookup"><span data-stu-id="12733-383">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12733-384"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12733-384"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12733-385">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12733-385">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12733-386">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="12733-386">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

