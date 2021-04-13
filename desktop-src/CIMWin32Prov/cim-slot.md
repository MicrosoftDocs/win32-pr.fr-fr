---
description: La \_ classe d’emplacement CIM représente les connecteurs dans lesquels des packages sont insérés.
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: Classe CIM_Slot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a63c8cd200096aa132d8205691669d765e54f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483832"
---
# <a name="cim_slot-class"></a><span data-ttu-id="ee3d0-103">\_Classe d’emplacement CIM</span><span class="sxs-lookup"><span data-stu-id="ee3d0-103">CIM\_Slot class</span></span>

<span data-ttu-id="ee3d0-104">La classe d' **\_ emplacement CIM** représente les connecteurs dans lesquels des packages sont insérés.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-104">The **CIM\_Slot** class represents connectors into which packages are inserted.</span></span> <span data-ttu-id="ee3d0-105">Par exemple, un package physique qui est un lecteur de disque peut être inséré dans un emplacement SCA, ou une carte (une sous-classe de [ \_ PhysicalPackage CIM](cim-physicalpackage.md)) peut être insérée dans un emplacement d’extension 16, 32 ou 64 bits sur un tableau d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-105">For example, a physical package that is a disk drive can be inserted into an SCA slot, or a card (a subclass of [CIM\_PhysicalPackage](cim-physicalpackage.md)) can be inserted into a 16-, 32-, or 64-bit expansion slot on a hosting board.</span></span> <span data-ttu-id="ee3d0-106">Les emplacements PCI ou PCMCIA de type III sont des exemples de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-106">PCI or PCMCIA Type III Slots are examples of the latter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee3d0-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ee3d0-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ee3d0-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ee3d0-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee3d0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee3d0-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a><span data-ttu-id="ee3d0-112">Membres</span><span class="sxs-lookup"><span data-stu-id="ee3d0-112">Members</span></span>

<span data-ttu-id="ee3d0-113">La classe d' **\_ emplacement CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ee3d0-113">The **CIM\_Slot** class has these types of members:</span></span>

-   [<span data-ttu-id="ee3d0-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee3d0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee3d0-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee3d0-115">Properties</span></span>

<span data-ttu-id="ee3d0-116">La classe d' **\_ emplacement CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-116">The **CIM\_Slot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee3d0-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-121">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-121">Short textual description of the object.</span></span>

<span data-ttu-id="ee3d0-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-123">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-123">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-126">Chaîne de forme libre qui décrit la configuration du code confidentiel et l’utilisation des signaux d’un connecteur physique.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-126">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

<span data-ttu-id="ee3d0-127">Cette propriété est héritée de la [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-127">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-128">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-129">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-131">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Emplacement système DMTF \| 004,2 ")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.2")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-132">Type de connecteur physique.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-132">Type of physical connector.</span></span> <span data-ttu-id="ee3d0-133">Un tableau est spécifié pour autoriser la description des combinaisons d’informations de connecteur.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-133">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="ee3d0-134">Par exemple, une entrée de tableau peut spécifier RS-232, un autre DB-25 et un troisième peut définir le connecteur comme « mâle ».</span><span class="sxs-lookup"><span data-stu-id="ee3d0-134">For example, one array entry could specify RS-232, another DB-25, and a third could define the connector as "Male".</span></span>

<span data-ttu-id="ee3d0-135">Cette propriété est héritée de la [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-135">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<dt>

<span data-ttu-id="ee3d0-136">0</span><span class="sxs-lookup"><span data-stu-id="ee3d0-136">0</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-137">Unknown</span><span class="sxs-lookup"><span data-stu-id="ee3d0-137">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-138">1</span><span class="sxs-lookup"><span data-stu-id="ee3d0-138">1</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-139">Autres</span><span class="sxs-lookup"><span data-stu-id="ee3d0-139">Other</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-140">2</span><span class="sxs-lookup"><span data-stu-id="ee3d0-140">2</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-141">Male</span><span class="sxs-lookup"><span data-stu-id="ee3d0-141">Male</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-142">3</span><span class="sxs-lookup"><span data-stu-id="ee3d0-142">3</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-143">Female</span><span class="sxs-lookup"><span data-stu-id="ee3d0-143">Female</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-144">4</span><span class="sxs-lookup"><span data-stu-id="ee3d0-144">4</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-145">Protégé</span><span class="sxs-lookup"><span data-stu-id="ee3d0-145">Shielded</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-146">5</span><span class="sxs-lookup"><span data-stu-id="ee3d0-146">5</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-147">Machine</span><span class="sxs-lookup"><span data-stu-id="ee3d0-147">Unshielded</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-148">6</span><span class="sxs-lookup"><span data-stu-id="ee3d0-148">6</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-149">Haute densité SCSI (A) (50 broches)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-149">SCSI (A) High-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-150">7</span><span class="sxs-lookup"><span data-stu-id="ee3d0-150">7</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-151">SCSI (A) faible densité (50 broches)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-151">SCSI (A) Low-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-152">8</span><span class="sxs-lookup"><span data-stu-id="ee3d0-152">8</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-153">Haute densité SCSI (P) (68 broches)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-153">SCSI (P) High-density (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-154">9</span><span class="sxs-lookup"><span data-stu-id="ee3d0-154">9</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-155">SCSI SCA-I (80 broches)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-155">SCSI SCA-I (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-156">10</span><span class="sxs-lookup"><span data-stu-id="ee3d0-156">10</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-157">SCSI SCA-II (80 broches)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-157">SCSI SCA-II (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-158">11</span><span class="sxs-lookup"><span data-stu-id="ee3d0-158">11</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-159">Fibre Channel SCSI (DB-9, cuivre)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-159">SCSI Fibre Channel (DB-9, Copper)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-160">12</span><span class="sxs-lookup"><span data-stu-id="ee3d0-160">12</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-161">Fibre Channel SCSI (fibre)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-161">SCSI Fibre Channel (Fibre)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-162">13</span><span class="sxs-lookup"><span data-stu-id="ee3d0-162">13</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-163">SCSI Fibre Channel SCA-II (pin 40)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-163">SCSI Fibre Channel SCA-II (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-164">14</span><span class="sxs-lookup"><span data-stu-id="ee3d0-164">14</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-165">SCSI Fibre Channel SCA-II (20 broches)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-165">SCSI Fibre Channel SCA-II (20 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-166">15</span><span class="sxs-lookup"><span data-stu-id="ee3d0-166">15</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-167">SCSI Fibre Channel BNC</span><span class="sxs-lookup"><span data-stu-id="ee3d0-167">SCSI Fibre Channel BNC</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-168">16</span><span class="sxs-lookup"><span data-stu-id="ee3d0-168">16</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-169">ATA 3-1/2 pouces (40 broches)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-169">ATA 3-1/2 Inch (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-170">17</span><span class="sxs-lookup"><span data-stu-id="ee3d0-170">17</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-171">ATA 2-1/2 pouces (44 broches)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-171">ATA 2-1/2 Inch (44 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-172">18</span><span class="sxs-lookup"><span data-stu-id="ee3d0-172">18</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-173">ATA-2</span><span class="sxs-lookup"><span data-stu-id="ee3d0-173">ATA-2</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-174">19</span><span class="sxs-lookup"><span data-stu-id="ee3d0-174">19</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-175">ATA-3</span><span class="sxs-lookup"><span data-stu-id="ee3d0-175">ATA-3</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-176">20</span><span class="sxs-lookup"><span data-stu-id="ee3d0-176">20</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-177">ATA/66</span><span class="sxs-lookup"><span data-stu-id="ee3d0-177">ATA/66</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-178">21</span><span class="sxs-lookup"><span data-stu-id="ee3d0-178">21</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-179">DB-9</span><span class="sxs-lookup"><span data-stu-id="ee3d0-179">DB-9</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-180">22</span><span class="sxs-lookup"><span data-stu-id="ee3d0-180">22</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-181">DB-15</span><span class="sxs-lookup"><span data-stu-id="ee3d0-181">DB-15</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-182">23</span><span class="sxs-lookup"><span data-stu-id="ee3d0-182">23</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-183">DB-25</span><span class="sxs-lookup"><span data-stu-id="ee3d0-183">DB-25</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-184">24</span><span class="sxs-lookup"><span data-stu-id="ee3d0-184">24</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-185">DB-36</span><span class="sxs-lookup"><span data-stu-id="ee3d0-185">DB-36</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-186">25</span><span class="sxs-lookup"><span data-stu-id="ee3d0-186">25</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-187">RS-232C</span><span class="sxs-lookup"><span data-stu-id="ee3d0-187">RS-232C</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-188">26</span><span class="sxs-lookup"><span data-stu-id="ee3d0-188">26</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-189">RS-422</span><span class="sxs-lookup"><span data-stu-id="ee3d0-189">RS-422</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-190">27</span><span class="sxs-lookup"><span data-stu-id="ee3d0-190">27</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-191">RS-423</span><span class="sxs-lookup"><span data-stu-id="ee3d0-191">RS-423</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-192">28</span><span class="sxs-lookup"><span data-stu-id="ee3d0-192">28</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-193">RS-485</span><span class="sxs-lookup"><span data-stu-id="ee3d0-193">RS-485</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-194">29</span><span class="sxs-lookup"><span data-stu-id="ee3d0-194">29</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-195">RS-449</span><span class="sxs-lookup"><span data-stu-id="ee3d0-195">RS-449</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-196">30</span><span class="sxs-lookup"><span data-stu-id="ee3d0-196">30</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-197">V. 35</span><span class="sxs-lookup"><span data-stu-id="ee3d0-197">V.35</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-198">31</span><span class="sxs-lookup"><span data-stu-id="ee3d0-198">31</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-199">X. 21</span><span class="sxs-lookup"><span data-stu-id="ee3d0-199">X.21</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-200">32</span><span class="sxs-lookup"><span data-stu-id="ee3d0-200">32</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-201">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="ee3d0-201">IEEE-488</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-202">33</span><span class="sxs-lookup"><span data-stu-id="ee3d0-202">33</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-203">BROCHES</span><span class="sxs-lookup"><span data-stu-id="ee3d0-203">AUI</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-204">34</span><span class="sxs-lookup"><span data-stu-id="ee3d0-204">34</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-205">UTP catégorie 3</span><span class="sxs-lookup"><span data-stu-id="ee3d0-205">UTP Category 3</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-206">35</span><span class="sxs-lookup"><span data-stu-id="ee3d0-206">35</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-207">UTP catégorie 4</span><span class="sxs-lookup"><span data-stu-id="ee3d0-207">UTP Category 4</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-208">36</span><span class="sxs-lookup"><span data-stu-id="ee3d0-208">36</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-209">UTP catégorie 5</span><span class="sxs-lookup"><span data-stu-id="ee3d0-209">UTP Category 5</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-210">37</span><span class="sxs-lookup"><span data-stu-id="ee3d0-210">37</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-211">ÉQUIPÉS</span><span class="sxs-lookup"><span data-stu-id="ee3d0-211">BNC</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-212">38</span><span class="sxs-lookup"><span data-stu-id="ee3d0-212">38</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-213">RJ11</span><span class="sxs-lookup"><span data-stu-id="ee3d0-213">RJ11</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-214">39</span><span class="sxs-lookup"><span data-stu-id="ee3d0-214">39</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-215">RJ</span><span class="sxs-lookup"><span data-stu-id="ee3d0-215">RJ45</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-216">40</span><span class="sxs-lookup"><span data-stu-id="ee3d0-216">40</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-217">MIC fibre</span><span class="sxs-lookup"><span data-stu-id="ee3d0-217">Fiber MIC</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-218">41</span><span class="sxs-lookup"><span data-stu-id="ee3d0-218">41</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-219">Apple AUI</span><span class="sxs-lookup"><span data-stu-id="ee3d0-219">Apple AUI</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-220">42</span><span class="sxs-lookup"><span data-stu-id="ee3d0-220">42</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-221">Port Apple</span><span class="sxs-lookup"><span data-stu-id="ee3d0-221">Apple GeoPort</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-222">43</span><span class="sxs-lookup"><span data-stu-id="ee3d0-222">43</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-223">PCI</span><span class="sxs-lookup"><span data-stu-id="ee3d0-223">PCI</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-224">44</span><span class="sxs-lookup"><span data-stu-id="ee3d0-224">44</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-225">ISA</span><span class="sxs-lookup"><span data-stu-id="ee3d0-225">ISA</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-226">45</span><span class="sxs-lookup"><span data-stu-id="ee3d0-226">45</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-227">EISA</span><span class="sxs-lookup"><span data-stu-id="ee3d0-227">EISA</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-228">46</span><span class="sxs-lookup"><span data-stu-id="ee3d0-228">46</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-229">VESA</span><span class="sxs-lookup"><span data-stu-id="ee3d0-229">VESA</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-230">47</span><span class="sxs-lookup"><span data-stu-id="ee3d0-230">47</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-231">PCMCIA</span><span class="sxs-lookup"><span data-stu-id="ee3d0-231">PCMCIA</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-232">48</span><span class="sxs-lookup"><span data-stu-id="ee3d0-232">48</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-233">Type PCMCIA I</span><span class="sxs-lookup"><span data-stu-id="ee3d0-233">PCMCIA Type I</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-234">49</span><span class="sxs-lookup"><span data-stu-id="ee3d0-234">49</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-235">PCMCIA type II</span><span class="sxs-lookup"><span data-stu-id="ee3d0-235">PCMCIA Type II</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-236">50</span><span class="sxs-lookup"><span data-stu-id="ee3d0-236">50</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-237">Type PCMCIA III</span><span class="sxs-lookup"><span data-stu-id="ee3d0-237">PCMCIA Type III</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-238">51</span><span class="sxs-lookup"><span data-stu-id="ee3d0-238">51</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-239">Port ZV</span><span class="sxs-lookup"><span data-stu-id="ee3d0-239">ZV Port</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-240">52</span><span class="sxs-lookup"><span data-stu-id="ee3d0-240">52</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-241">CardBus</span><span class="sxs-lookup"><span data-stu-id="ee3d0-241">CardBus</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-242">53</span><span class="sxs-lookup"><span data-stu-id="ee3d0-242">53</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-243">USB</span><span class="sxs-lookup"><span data-stu-id="ee3d0-243">USB</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-244">54</span><span class="sxs-lookup"><span data-stu-id="ee3d0-244">54</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-245">IEEE 1394</span><span class="sxs-lookup"><span data-stu-id="ee3d0-245">IEEE 1394</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-246">55</span><span class="sxs-lookup"><span data-stu-id="ee3d0-246">55</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-247">HIPPA</span><span class="sxs-lookup"><span data-stu-id="ee3d0-247">HIPPI</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-248">56</span><span class="sxs-lookup"><span data-stu-id="ee3d0-248">56</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-249">HSSDC (6 broches)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-249">HSSDC (6 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-250">57</span><span class="sxs-lookup"><span data-stu-id="ee3d0-250">57</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-251">GBIC</span><span class="sxs-lookup"><span data-stu-id="ee3d0-251">GBIC</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-252">58</span><span class="sxs-lookup"><span data-stu-id="ee3d0-252">58</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-253">DIN</span><span class="sxs-lookup"><span data-stu-id="ee3d0-253">DIN</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-254">59</span><span class="sxs-lookup"><span data-stu-id="ee3d0-254">59</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-255">Mini-DIN</span><span class="sxs-lookup"><span data-stu-id="ee3d0-255">Mini-DIN</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-256">60</span><span class="sxs-lookup"><span data-stu-id="ee3d0-256">60</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-257">Micro-DIN</span><span class="sxs-lookup"><span data-stu-id="ee3d0-257">Micro-DIN</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-258">61</span><span class="sxs-lookup"><span data-stu-id="ee3d0-258">61</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-259">PS/2</span><span class="sxs-lookup"><span data-stu-id="ee3d0-259">PS/2</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-260">62</span><span class="sxs-lookup"><span data-stu-id="ee3d0-260">62</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-261">Infrarouge</span><span class="sxs-lookup"><span data-stu-id="ee3d0-261">Infrared</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-262">63</span><span class="sxs-lookup"><span data-stu-id="ee3d0-262">63</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-263">HP-HIL</span><span class="sxs-lookup"><span data-stu-id="ee3d0-263">HP-HIL</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-264">64</span><span class="sxs-lookup"><span data-stu-id="ee3d0-264">64</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-265">Accès à. bus</span><span class="sxs-lookup"><span data-stu-id="ee3d0-265">Access.bus</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-266">65</span><span class="sxs-lookup"><span data-stu-id="ee3d0-266">65</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-267">NuBus</span><span class="sxs-lookup"><span data-stu-id="ee3d0-267">NuBus</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-268">66</span><span class="sxs-lookup"><span data-stu-id="ee3d0-268">66</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-269">Centronics</span><span class="sxs-lookup"><span data-stu-id="ee3d0-269">Centronics</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-270">67</span><span class="sxs-lookup"><span data-stu-id="ee3d0-270">67</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-271">Mini-Centronics</span><span class="sxs-lookup"><span data-stu-id="ee3d0-271">Mini-Centronics</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-272">68</span><span class="sxs-lookup"><span data-stu-id="ee3d0-272">68</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-273">Type de Mini-Centronics-14</span><span class="sxs-lookup"><span data-stu-id="ee3d0-273">Mini-Centronics Type-14</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-274">69</span><span class="sxs-lookup"><span data-stu-id="ee3d0-274">69</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-275">Type de Mini-Centronics-20</span><span class="sxs-lookup"><span data-stu-id="ee3d0-275">Mini-Centronics Type-20</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-276">70</span><span class="sxs-lookup"><span data-stu-id="ee3d0-276">70</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-277">Type de Mini-Centronics-26</span><span class="sxs-lookup"><span data-stu-id="ee3d0-277">Mini-Centronics Type-26</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-278">71</span><span class="sxs-lookup"><span data-stu-id="ee3d0-278">71</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-279">Souris bus</span><span class="sxs-lookup"><span data-stu-id="ee3d0-279">Bus Mouse</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-280">72</span><span class="sxs-lookup"><span data-stu-id="ee3d0-280">72</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-281">BUS</span><span class="sxs-lookup"><span data-stu-id="ee3d0-281">ADB</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-282">73</span><span class="sxs-lookup"><span data-stu-id="ee3d0-282">73</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-283">AGP</span><span class="sxs-lookup"><span data-stu-id="ee3d0-283">AGP</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-284">74</span><span class="sxs-lookup"><span data-stu-id="ee3d0-284">74</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-285">Bus VME</span><span class="sxs-lookup"><span data-stu-id="ee3d0-285">VME Bus</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-286">75</span><span class="sxs-lookup"><span data-stu-id="ee3d0-286">75</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-287">VME64</span><span class="sxs-lookup"><span data-stu-id="ee3d0-287">VME64</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-288">76</span><span class="sxs-lookup"><span data-stu-id="ee3d0-288">76</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-289">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="ee3d0-289">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-290">77</span><span class="sxs-lookup"><span data-stu-id="ee3d0-290">77</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-291">Emplacement de la carte de processeur propriétaire</span><span class="sxs-lookup"><span data-stu-id="ee3d0-291">Proprietary Processor Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-292">78</span><span class="sxs-lookup"><span data-stu-id="ee3d0-292">78</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-293">Emplacement de carte mémoire propriétaire</span><span class="sxs-lookup"><span data-stu-id="ee3d0-293">Proprietary Memory Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-294">79</span><span class="sxs-lookup"><span data-stu-id="ee3d0-294">79</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-295">Emplacement de la carte de montage d’e/s propriétaire</span><span class="sxs-lookup"><span data-stu-id="ee3d0-295">Proprietary I/O Riser Slot</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-296">80</span><span class="sxs-lookup"><span data-stu-id="ee3d0-296">80</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-297">PCI-66 MHZ</span><span class="sxs-lookup"><span data-stu-id="ee3d0-297">PCI-66MHZ</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-298">81</span><span class="sxs-lookup"><span data-stu-id="ee3d0-298">81</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-299">AGP2X</span><span class="sxs-lookup"><span data-stu-id="ee3d0-299">AGP2X</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-300">82</span><span class="sxs-lookup"><span data-stu-id="ee3d0-300">82</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-301">AGP4X</span><span class="sxs-lookup"><span data-stu-id="ee3d0-301">AGP4X</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-302">83</span><span class="sxs-lookup"><span data-stu-id="ee3d0-302">83</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-303">PC-98</span><span class="sxs-lookup"><span data-stu-id="ee3d0-303">PC-98</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-304">84</span><span class="sxs-lookup"><span data-stu-id="ee3d0-304">84</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-305">PC-98-Hireso</span><span class="sxs-lookup"><span data-stu-id="ee3d0-305">PC-98-Hireso</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-306">85 %</span><span class="sxs-lookup"><span data-stu-id="ee3d0-306">85</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-307">PC-H98</span><span class="sxs-lookup"><span data-stu-id="ee3d0-307">PC-H98</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-308">86</span><span class="sxs-lookup"><span data-stu-id="ee3d0-308">86</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-309">PC-98Note</span><span class="sxs-lookup"><span data-stu-id="ee3d0-309">PC-98Note</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-310">87</span><span class="sxs-lookup"><span data-stu-id="ee3d0-310">87</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-311">PC-98Full</span><span class="sxs-lookup"><span data-stu-id="ee3d0-311">PC-98Full</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-312">88</span><span class="sxs-lookup"><span data-stu-id="ee3d0-312">88</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-313">SCSI SSA</span><span class="sxs-lookup"><span data-stu-id="ee3d0-313">SSA SCSI</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-314">89</span><span class="sxs-lookup"><span data-stu-id="ee3d0-314">89</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-315">Circulaire</span><span class="sxs-lookup"><span data-stu-id="ee3d0-315">Circular</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-316">90</span><span class="sxs-lookup"><span data-stu-id="ee3d0-316">90</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-317">Connecteur IDE de la carte</span><span class="sxs-lookup"><span data-stu-id="ee3d0-317">On Board IDE Connector</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-318">91</span><span class="sxs-lookup"><span data-stu-id="ee3d0-318">91</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-319">Connecteur de disquette sur carte</span><span class="sxs-lookup"><span data-stu-id="ee3d0-319">On Board Floppy Connector</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-320">92</span><span class="sxs-lookup"><span data-stu-id="ee3d0-320">92</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-321">9 broches en double en ligne</span><span class="sxs-lookup"><span data-stu-id="ee3d0-321">9 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-322">93</span><span class="sxs-lookup"><span data-stu-id="ee3d0-322">93</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-323">25 broche en double en ligne</span><span class="sxs-lookup"><span data-stu-id="ee3d0-323">25 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-324">94</span><span class="sxs-lookup"><span data-stu-id="ee3d0-324">94</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-325">50 pin double Inline</span><span class="sxs-lookup"><span data-stu-id="ee3d0-325">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-326">95</span><span class="sxs-lookup"><span data-stu-id="ee3d0-326">95</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-327">68 pin double Inline</span><span class="sxs-lookup"><span data-stu-id="ee3d0-327">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-328">96</span><span class="sxs-lookup"><span data-stu-id="ee3d0-328">96</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-329">Connecteur audio sur carte</span><span class="sxs-lookup"><span data-stu-id="ee3d0-329">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-330">97</span><span class="sxs-lookup"><span data-stu-id="ee3d0-330">97</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-331">Mini-Jack</span><span class="sxs-lookup"><span data-stu-id="ee3d0-331">Mini-jack</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-332">98</span><span class="sxs-lookup"><span data-stu-id="ee3d0-332">98</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-333">PCI-X</span><span class="sxs-lookup"><span data-stu-id="ee3d0-333">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-334">99</span><span class="sxs-lookup"><span data-stu-id="ee3d0-334">99</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-335">SBus IEEE 1396-1993 32 bits</span><span class="sxs-lookup"><span data-stu-id="ee3d0-335">Sbus IEEE 1396-1993 32 bit</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-336">100</span><span class="sxs-lookup"><span data-stu-id="ee3d0-336">100</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-337">SBus IEEE 1396-1993 64 bits</span><span class="sxs-lookup"><span data-stu-id="ee3d0-337">Sbus IEEE 1396-1993 64 bit</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-338">101</span><span class="sxs-lookup"><span data-stu-id="ee3d0-338">101</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-339">MCA</span><span class="sxs-lookup"><span data-stu-id="ee3d0-339">MCA</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-340">102</span><span class="sxs-lookup"><span data-stu-id="ee3d0-340">102</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-341">GIO</span><span class="sxs-lookup"><span data-stu-id="ee3d0-341">GIO</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-342">103</span><span class="sxs-lookup"><span data-stu-id="ee3d0-342">103</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-343">XIO</span><span class="sxs-lookup"><span data-stu-id="ee3d0-343">XIO</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-344">104</span><span class="sxs-lookup"><span data-stu-id="ee3d0-344">104</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-345">HIO</span><span class="sxs-lookup"><span data-stu-id="ee3d0-345">HIO</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-346">105</span><span class="sxs-lookup"><span data-stu-id="ee3d0-346">105</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-347">NGIO</span><span class="sxs-lookup"><span data-stu-id="ee3d0-347">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-348">106</span><span class="sxs-lookup"><span data-stu-id="ee3d0-348">106</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-349">PMC</span><span class="sxs-lookup"><span data-stu-id="ee3d0-349">PMC</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-350">107</span><span class="sxs-lookup"><span data-stu-id="ee3d0-350">107</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-351">MTRJ</span><span class="sxs-lookup"><span data-stu-id="ee3d0-351">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-352">108</span><span class="sxs-lookup"><span data-stu-id="ee3d0-352">108</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-353">VF-45</span><span class="sxs-lookup"><span data-stu-id="ee3d0-353">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-354">109</span><span class="sxs-lookup"><span data-stu-id="ee3d0-354">109</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-355">E/s futures</span><span class="sxs-lookup"><span data-stu-id="ee3d0-355">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-356">110</span><span class="sxs-lookup"><span data-stu-id="ee3d0-356">110</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-357">SC</span><span class="sxs-lookup"><span data-stu-id="ee3d0-357">SC</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-358">111</span><span class="sxs-lookup"><span data-stu-id="ee3d0-358">111</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-359">SG</span><span class="sxs-lookup"><span data-stu-id="ee3d0-359">SG</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-360">112</span><span class="sxs-lookup"><span data-stu-id="ee3d0-360">112</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-361">Electrical</span><span class="sxs-lookup"><span data-stu-id="ee3d0-361">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-362">113</span><span class="sxs-lookup"><span data-stu-id="ee3d0-362">113</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-363">Optique</span><span class="sxs-lookup"><span data-stu-id="ee3d0-363">Optical</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-364">114</span><span class="sxs-lookup"><span data-stu-id="ee3d0-364">114</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-365">Ruban</span><span class="sxs-lookup"><span data-stu-id="ee3d0-365">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-366">115</span><span class="sxs-lookup"><span data-stu-id="ee3d0-366">115</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-367">GLM</span><span class="sxs-lookup"><span data-stu-id="ee3d0-367">GLM</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-368">116</span><span class="sxs-lookup"><span data-stu-id="ee3d0-368">116</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-369">1x9</span><span class="sxs-lookup"><span data-stu-id="ee3d0-369">1x9</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-370">117</span><span class="sxs-lookup"><span data-stu-id="ee3d0-370">117</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-371">Mini SG</span><span class="sxs-lookup"><span data-stu-id="ee3d0-371">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-372">118</span><span class="sxs-lookup"><span data-stu-id="ee3d0-372">118</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-373">LC</span><span class="sxs-lookup"><span data-stu-id="ee3d0-373">LC</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-374">119</span><span class="sxs-lookup"><span data-stu-id="ee3d0-374">119</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-375">HSSC</span><span class="sxs-lookup"><span data-stu-id="ee3d0-375">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-376">120</span><span class="sxs-lookup"><span data-stu-id="ee3d0-376">120</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-377">VHDCI protégé (68 broches)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-377">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-378">121</span><span class="sxs-lookup"><span data-stu-id="ee3d0-378">121</span></span>
</dt> <dd>

<span data-ttu-id="ee3d0-379">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="ee3d0-379">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee3d0-380">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-380">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-383">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-383">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-384">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-384">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ee3d0-385">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-385">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ee3d0-386">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-386">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-387">**Description**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-387">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-388">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-390">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-390">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-391">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-391">Textual description of the object.</span></span>

<span data-ttu-id="ee3d0-392">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-393">**HeightAllowed**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-393">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-394">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-394">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-396">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-397">Hauteur maximale, en pouces, d’une carte d’adaptateur pouvant être insérée dans l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-397">Maximum height, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-398">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-398">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-399">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-401">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-401">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-402">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-402">Date and time the object was installed.</span></span> <span data-ttu-id="ee3d0-403">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-403">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ee3d0-404">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-405">**LengthAllowed**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-405">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-406">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-406">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-408">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-408">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-409">Longueur maximale, en pouces, d’une carte d’adaptateur pouvant être insérée dans l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-409">Maximum length, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-410">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-410">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-411">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-413">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-413">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-414">Organisation qui a produit l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-414">Organization that produced the physical element.</span></span> <span data-ttu-id="ee3d0-415">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-415">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="ee3d0-416">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-416">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-417">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-417">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-418">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-420">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Emplacement système DMTF \| 004,3 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-421">Largeur de bus maximale, en bits, des cartes d’adaptateur qui peuvent être insérées dans l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-421">Maximum bus width, in bits, of adapter cards that can be inserted into the slot.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="ee3d0-422">**8** (0)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-422">**8** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="ee3d0-423">**16** (1)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-423">**16** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="ee3d0-424">**32** (2)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-424">**32** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="64"></span>

<span data-ttu-id="ee3d0-425">**64** (3)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-425">**64** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="128"></span>

<span data-ttu-id="ee3d0-426">**128** (4)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-426">**128** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee3d0-427">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-427">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-428">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-430">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-431">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-431">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="ee3d0-432">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-432">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-433">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-433">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-436">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-436">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-437">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-437">Label by which the object is known.</span></span> <span data-ttu-id="ee3d0-438">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-438">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ee3d0-439">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-440">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-440">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-441">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-443">Numéro d’emplacement physique, qui peut être utilisé comme index dans une table d’emplacements système pour déterminer si l’emplacement est physiquement occupé.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-443">Physical slot number, which can be used as an index into a system slot table, to determine whether the slot is physically occupied.</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-444">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-444">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-445">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-447">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-447">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="ee3d0-448">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-448">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="ee3d0-449">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="ee3d0-449">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="ee3d0-450">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-450">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-451">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-451">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-452">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-454">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-454">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-455">Numéro de référence attribué par l’organisation qui a produit ou fabriqué l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-455">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="ee3d0-456">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-456">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-457">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-457">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-458">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-459">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-460">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-460">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="ee3d0-461">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-461">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-462">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-462">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-463">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-464">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-465">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ emplacement CIM**.**SpecialPurpose**")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-465">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-466">Chaîne de forme libre qui décrit comment cet emplacement est physiquement unique et qui peut contenir des types de matériel spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-466">Free-form string that describes how this slot is physically unique and that it may hold special types of hardware.</span></span> <span data-ttu-id="ee3d0-467">Cette propriété n’a de sens que lorsque la propriété booléenne **SpecialPurpose** correspondante a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-467">This property only has meaning when the corresponding Boolean **SpecialPurpose** property is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-468">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-468">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-469">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-471">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-471">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-472">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-472">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="ee3d0-473">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-473">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-474">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-474">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-475">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-476">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-477">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-478">Numéro d’unité de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-478">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="ee3d0-479">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-479">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-480">**SpecialPurpose**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-480">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-481">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-481">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-483">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ emplacement CIM**.**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-483">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-484">Si la **valeur est true**, l’emplacement est physiquement unique et peut contenir des types spéciaux de matériel (par exemple, un emplacement de processeur graphique).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-484">If **TRUE**, the slot is physically unique and may hold special types of hardware, (for example, a graphics processor slot).</span></span> <span data-ttu-id="ee3d0-485">Si la **valeur est true**, la propriété **PurposeDescription** doit spécifier la manière dont l’emplacement est unique ou le rôle de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-485">If **TRUE**, the **PurposeDescription** property should specify how the slot is unique or the slot's purpose.</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-486">**État**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-486">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-488">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-489">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-489">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-490">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-490">Current status of the object.</span></span> <span data-ttu-id="ee3d0-491">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-491">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ee3d0-492">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee3d0-492">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ee3d0-493">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-493">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ee3d0-494">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-494">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ee3d0-495">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-495">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee3d0-496">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-496">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ee3d0-497">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-497">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ee3d0-498">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-498">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ee3d0-499">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-499">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ee3d0-500">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-500">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ee3d0-501">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-501">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ee3d0-502">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-502">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ee3d0-503">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-503">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ee3d0-504">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-504">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee3d0-505">**SupportsHotPlug**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-505">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-506">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-506">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-508">Si la **valeur est true**, l’emplacement prend en charge la connexion à chaud des cartes d’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-508">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-509">**Tag**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-509">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-510">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-511">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-512">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-512">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-513">Chaîne arbitraire qui identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-513">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="ee3d0-514">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-514">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="ee3d0-515">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel/l’entité, indépendamment de l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-515">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="ee3d0-516">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-516">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="ee3d0-517">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-517">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="ee3d0-518">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-518">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="ee3d0-519">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-519">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-520">**ThermalRating**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-520">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-521">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-522">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-523">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Emplacement système DMTF \| 004,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatts ")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-524">Dissipation thermique maximale de l’emplacement, en milliwatts.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-524">Maximum thermal dissipation of the slot, in milliwatts.</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-525">**VccMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-525">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-526">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-526">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-527">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-528">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Emplacement système DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-528">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-529">Tension Vcc prise en charge par l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-529">Vcc voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee3d0-530">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-530">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ee3d0-531">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-531">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="ee3d0-532">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-532">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="ee3d0-533">**5 v** (3)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-533">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee3d0-534">**Version**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-534">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-535">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-536">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-537">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-537">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-538">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-538">Version of the physical element.</span></span>

<span data-ttu-id="ee3d0-539">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-539">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee3d0-540">**VppMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-540">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee3d0-541">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-542">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee3d0-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee3d0-543">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Emplacement système DMTF \| 004,10 ")</span><span class="sxs-lookup"><span data-stu-id="ee3d0-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="ee3d0-544">Tension VPP prise en charge par l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-544">Vpp voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee3d0-545">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-545">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ee3d0-546">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-546">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="ee3d0-547">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-547">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="ee3d0-548">**5 v** (3)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-548">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="ee3d0-549">**12V** (4)</span><span class="sxs-lookup"><span data-stu-id="ee3d0-549">**12V** (4)</span></span>


<span data-ttu-id="ee3d0-550"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ee3d0-550"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ee3d0-551">Notes</span><span class="sxs-lookup"><span data-stu-id="ee3d0-551">Remarks</span></span>

<span data-ttu-id="ee3d0-552">La classe d' **\_ emplacement CIM** est dérivée de la [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-552">The **CIM\_Slot** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="ee3d0-553">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-553">WMI does not implement this class.</span></span> <span data-ttu-id="ee3d0-554">Pour les classes WMI dérivées de l' **\_ emplacement CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d0-554">For WMI classes derived from **CIM\_Slot**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ee3d0-555">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ee3d0-556">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ee3d0-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee3d0-557">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee3d0-557">Requirements</span></span>



| <span data-ttu-id="ee3d0-558">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee3d0-558">Requirement</span></span> | <span data-ttu-id="ee3d0-559">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee3d0-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3d0-560">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee3d0-560">Minimum supported client</span></span><br/> | <span data-ttu-id="ee3d0-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee3d0-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee3d0-562">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee3d0-562">Minimum supported server</span></span><br/> | <span data-ttu-id="ee3d0-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee3d0-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee3d0-564">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ee3d0-564">Namespace</span></span><br/>                | <span data-ttu-id="ee3d0-565">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ee3d0-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ee3d0-566">MOF</span><span class="sxs-lookup"><span data-stu-id="ee3d0-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee3d0-567"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee3d0-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee3d0-568">DLL</span><span class="sxs-lookup"><span data-stu-id="ee3d0-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee3d0-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee3d0-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee3d0-570">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee3d0-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3d0-571">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="ee3d0-571">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> </dl>

 

