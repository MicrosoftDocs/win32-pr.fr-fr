---
description: Représente un périphérique de mémoire physique situé sur un système informatique et disponible pour le système d’exploitation.
ms.assetid: 34baca53-ab85-4e06-9853-71b904ede4ab
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemory
- Win32_PhysicalMemory.Attributes
- Win32_PhysicalMemory.BankLabel
- Win32_PhysicalMemory.Capacity
- Win32_PhysicalMemory.Caption
- Win32_PhysicalMemory.ConfiguredClockSpeed
- Win32_PhysicalMemory.ConfiguredVoltage
- Win32_PhysicalMemory.CreationClassName
- Win32_PhysicalMemory.DataWidth
- Win32_PhysicalMemory.Description
- Win32_PhysicalMemory.DeviceLocator
- Win32_PhysicalMemory.FormFactor
- Win32_PhysicalMemory.HotSwappable
- Win32_PhysicalMemory.InstallDate
- Win32_PhysicalMemory.InterleaveDataDepth
- Win32_PhysicalMemory.InterleavePosition
- Win32_PhysicalMemory.Manufacturer
- Win32_PhysicalMemory.MaxVoltage
- Win32_PhysicalMemory.MemoryType
- Win32_PhysicalMemory.MinVoltage
- Win32_PhysicalMemory.Model
- Win32_PhysicalMemory.Name
- Win32_PhysicalMemory.OtherIdentifyingInfo
- Win32_PhysicalMemory.PartNumber
- Win32_PhysicalMemory.PositionInRow
- Win32_PhysicalMemory.PoweredOn
- Win32_PhysicalMemory.Removable
- Win32_PhysicalMemory.Replaceable
- Win32_PhysicalMemory.SerialNumber
- Win32_PhysicalMemory.SKU
- Win32_PhysicalMemory.SMBIOSMemoryType
- Win32_PhysicalMemory.Speed
- Win32_PhysicalMemory.Status
- Win32_PhysicalMemory.Tag
- Win32_PhysicalMemory.TotalWidth
- Win32_PhysicalMemory.TypeDetail
- Win32_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e026c3c3d0a29bbbd10ed2b5565708f0bcb0900c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483960"
---
# <a name="win32_physicalmemory-class"></a><span data-ttu-id="1ea8a-103">\_Classe PhysicalMemory Win32</span><span class="sxs-lookup"><span data-stu-id="1ea8a-103">Win32\_PhysicalMemory class</span></span>

<span data-ttu-id="1ea8a-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ PhysicalMemory Win32** représente un périphérique de mémoire physique situé sur un système informatique et disponible pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-104">The **Win32\_PhysicalMemory** [WMI class](../wmisdk/retrieving-a-class.md) represents a physical memory device located on a computer system and available to the operating system.</span></span>

<span data-ttu-id="1ea8a-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1ea8a-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea8a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ea8a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B93-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemory : CIM_PhysicalMemory
{
  uint32   Attributes;
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  uint32   ConfiguredClockSpeed;
  uint32   ConfiguredVoltage;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  string   DeviceLocator;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   InterleaveDataDepth;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint32   MaxVoltage;
  uint16   MemoryType;
  uint32   MinVoltage;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   SMBIOSMemoryType;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  uint16   TypeDetail;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="1ea8a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="1ea8a-108">Members</span></span>

<span data-ttu-id="1ea8a-109">La classe **Win32 \_ PhysicalMemory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1ea8a-109">The **Win32\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="1ea8a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1ea8a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ea8a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1ea8a-111">Properties</span></span>

<span data-ttu-id="1ea8a-112">La classe **Win32 \_ PhysicalMemory** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-112">The **Win32\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ea8a-113">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-113">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-116">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| attributes")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Attributes")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-117">SMBIOS-type 17-attributs.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-117">SMBIOS - Type 17 - Attributes.</span></span> <span data-ttu-id="1ea8a-118">Représente le rang.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-118">Represents the RANK.</span></span>

<span data-ttu-id="1ea8a-119">Cette valeur provient du membre **attributs** de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-119">This value comes from the **Attributes** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-120">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-120">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-121">**BankLabel**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-121">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-124">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-125">Étiquette physique sur laquelle se trouve la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-125">Physically labeled bank where the memory is located.</span></span>

<span data-ttu-id="1ea8a-126">Exemples : « Bank 0 », « Bank A »</span><span class="sxs-lookup"><span data-stu-id="1ea8a-126">Examples: "Bank 0", "Bank A"</span></span>

<span data-ttu-id="1ea8a-127">Cette valeur provient du membre du localisateur de la **Banque** de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-127">This value comes from the **Bank Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-128">Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-128">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-129">**Capacité**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-129">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-130">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-132">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,5 "), [**unités**](../wmisdk/standard-qualifiers.md) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-133">Capacité totale de la mémoire physique, en octets.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-133">Total capacity of the physical memory—in bytes.</span></span>

<span data-ttu-id="1ea8a-134">Cette valeur provient de la structure de l' **unité de mémoire** dans les informations de version SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-134">This value comes from the **Memory Device** structure in the SMBIOS version information.</span></span> <span data-ttu-id="1ea8a-135">Pour les versions SMBIOS 2,1 à 2,6, la valeur provient du membre **Size** .</span><span class="sxs-lookup"><span data-stu-id="1ea8a-135">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Size** member.</span></span> <span data-ttu-id="1ea8a-136">Pour SMBIOS version 2.7 +, la valeur provient du membre de **taille étendue** .</span><span class="sxs-lookup"><span data-stu-id="1ea8a-136">For SMBIOS version 2.7+ the value comes from the **Extended Size** member.</span></span>

<span data-ttu-id="1ea8a-137">Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-137">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<span data-ttu-id="1ea8a-138">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-142">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-143">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-143">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="1ea8a-144">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-145">**ConfiguredClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-145">**ConfiguredClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-148">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« SMBIOS \| type 17-vitesse d’horloge de la \| mémoire configurée »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured Memory Clock Speed")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-149">Vitesse d’horloge configurée de l’appareil mémoire, en mégahertz (MHz), ou 0, si la vitesse est inconnue.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-149">The configured clock speed of the memory device, in megahertz (MHz), or 0, if the speed is unknown.</span></span>

<span data-ttu-id="1ea8a-150">Cette valeur provient du membre de vitesse de l’horloge de la **mémoire configurée** de la structure du **périphérique de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-150">This value comes from the **Configured Memory Clock Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-151">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-151">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-152">**ConfiguredVoltage**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-152">**ConfiguredVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-153">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-155">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| tension configurée")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured voltage")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-156">Tension configurée pour cet appareil, en millivolts ou 0, si la tension est inconnue.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-156">Configured voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="1ea8a-157">Cette valeur provient du membre **voltage configuré** de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-157">This value comes from the **Configured voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-158">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-158">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-159">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-159">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-162">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-162">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-163">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-163">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1ea8a-164">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-164">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="1ea8a-165">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-165">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-166">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-166">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-169">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,8 "), [**unités**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-170">Largeur des données de la mémoire physique (en bits).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-170">Data width of the physical memory—in bits.</span></span> <span data-ttu-id="1ea8a-171">Une largeur de données de 0 (zéro) et une largeur totale de 8 (huit) indique que la mémoire est utilisée uniquement pour fournir des bits de correction d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-171">A data width of 0 (zero) and a total width of 8 (eight) indicates that the memory is used solely to provide error correction bits.</span></span>

<span data-ttu-id="1ea8a-172">Cette valeur provient du membre de la **largeur des données** de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-172">This value comes from the **Data Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-173">Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-173">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-174">**Description**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-174">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-177">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-177">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-178">Description d’un objet.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-178">Description of an object.</span></span>

<span data-ttu-id="1ea8a-179">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-180">**DeviceLocator**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-180">**DeviceLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-183">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| Device Locator")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Device Locator")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-184">Étiquette du socket ou de la carte de circuit qui contient la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-184">Label of the socket or circuit board that holds the memory.</span></span>

<span data-ttu-id="1ea8a-185">Exemple : « SIMM 3 »</span><span class="sxs-lookup"><span data-stu-id="1ea8a-185">Example: "SIMM 3"</span></span>

<span data-ttu-id="1ea8a-186">Cette valeur provient du membre **localisateur** de l’appareil de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-186">This value comes from the **Device Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-187">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-187">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-188">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-190">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-191">Facteur de forme d’implémentation pour la puce.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-191">Implementation form factor for the chip.</span></span>

<span data-ttu-id="1ea8a-192">Cette valeur provient du membre **facteur de forme** de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-192">This value comes from the **Form Factor** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-193">Cette propriété est héritée de la [**\_ puce CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-193">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>



 <span data-ttu-id="1ea8a-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-195">Unknown</span><span class="sxs-lookup"><span data-stu-id="1ea8a-195">Unknown</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-196">(1)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-197">Autres</span><span class="sxs-lookup"><span data-stu-id="1ea8a-197">Other</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-198">(2)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-198">(2)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-199">PANNEAU</span><span class="sxs-lookup"><span data-stu-id="1ea8a-199">SIP</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-200">(3)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-200">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-201">DIP</span><span class="sxs-lookup"><span data-stu-id="1ea8a-201">DIP</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-202">(4)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-203">ZIP</span><span class="sxs-lookup"><span data-stu-id="1ea8a-203">ZIP</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-204">(5)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-205">SOJ</span><span class="sxs-lookup"><span data-stu-id="1ea8a-205">SOJ</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-207">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="1ea8a-207">Proprietary</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-208">(7)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-208">(7)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-209">Barrett</span><span class="sxs-lookup"><span data-stu-id="1ea8a-209">SIMM</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-210">(8)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-211">ESTOMPAGE</span><span class="sxs-lookup"><span data-stu-id="1ea8a-211">DIMM</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-212">(9)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-213">TSOP</span><span class="sxs-lookup"><span data-stu-id="1ea8a-213">TSOP</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-214">(10)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-215">PGA</span><span class="sxs-lookup"><span data-stu-id="1ea8a-215">PGA</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-216">(11)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-217">RIMM</span><span class="sxs-lookup"><span data-stu-id="1ea8a-217">RIMM</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-218">douze</span><span class="sxs-lookup"><span data-stu-id="1ea8a-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-219">SODIMM</span><span class="sxs-lookup"><span data-stu-id="1ea8a-219">SODIMM</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-220">(13)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-221">SRIMM</span><span class="sxs-lookup"><span data-stu-id="1ea8a-221">SRIMM</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-222">(14)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-223">SMD</span><span class="sxs-lookup"><span data-stu-id="1ea8a-223">SMD</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-224">(15)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-224">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-225">SSMP</span><span class="sxs-lookup"><span data-stu-id="1ea8a-225">SSMP</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-226">(16)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-227">QFP</span><span class="sxs-lookup"><span data-stu-id="1ea8a-227">QFP</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-228">(17)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-229">TQFP</span><span class="sxs-lookup"><span data-stu-id="1ea8a-229">TQFP</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-230">(18)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-230">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-231">SOIC</span><span class="sxs-lookup"><span data-stu-id="1ea8a-231">SOIC</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-232">(19)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-232">(19)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-233">LLC</span><span class="sxs-lookup"><span data-stu-id="1ea8a-233">LCC</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-234">(20)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-235">PLCC</span><span class="sxs-lookup"><span data-stu-id="1ea8a-235">PLCC</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-236">(21)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-237">GRILLE</span><span class="sxs-lookup"><span data-stu-id="1ea8a-237">BGA</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-238">(22)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-238">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-239">FPBGA</span><span class="sxs-lookup"><span data-stu-id="1ea8a-239">FPBGA</span></span>

</dd> <dt>



 <span data-ttu-id="1ea8a-240">(23)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-240">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-241">LGA</span><span class="sxs-lookup"><span data-stu-id="1ea8a-241">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1ea8a-242">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-242">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-243">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-245">Si la **valeur est true**, ce composant de média physique peut être remplacé par un autre physiquement, mais équivalent, alors que l’alimentation est appliquée dans le package qui le contient.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-245">If **TRUE**, this physical media component can be replaced with a physically different but equivalent one while the containing package has the power applied.</span></span> <span data-ttu-id="1ea8a-246">Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-246">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="1ea8a-247">Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-247">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="1ea8a-248">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-248">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-250">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-252">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-253">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-253">Date and time the object is installed.</span></span> <span data-ttu-id="1ea8a-254">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1ea8a-255">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-256">**InterleaveDataDepth**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-256">**InterleaveDataDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-257">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-259">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| type SMBIOS 20 \| profondeur des données entrelacées")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-259">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Interleaved Data Depth")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-260">Entier 16 bits non signé nombre maximal de lignes consécutives de données qui sont accessibles en un seul transfert entrelacé à partir du périphérique de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-260">Unsigned 16-bit integer maximum number of consecutive rows of data that are accessed in a single interleaved transfer from the memory device.</span></span> <span data-ttu-id="1ea8a-261">Si la valeur est 0 (zéro), la mémoire n’est pas entrelacée.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-261">If the value is 0 (zero), the memory is not interleaved.</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-262">**InterleavePosition**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-262">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-263">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-265">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,7»)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-266">Position de la mémoire physique dans une entrelacement.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-266">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="1ea8a-267">Par exemple, dans une entrelacement 2:1, la valeur « 1 » indique que la mémoire est dans la position « paire ».</span><span class="sxs-lookup"><span data-stu-id="1ea8a-267">For example, in a 2:1 interleave, a value of "1" indicates that the memory is in the "even" position.</span></span>

<span data-ttu-id="1ea8a-268">Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-268">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span data-ttu-id="1ea8a-269">0</span><span class="sxs-lookup"><span data-stu-id="1ea8a-269">0</span></span>
</dt> <dd>

<span data-ttu-id="1ea8a-270">Pas entrelacé</span><span class="sxs-lookup"><span data-stu-id="1ea8a-270">Noninterleaved</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-271">1</span><span class="sxs-lookup"><span data-stu-id="1ea8a-271">1</span></span>
</dt> <dd>

<span data-ttu-id="1ea8a-272">Première position</span><span class="sxs-lookup"><span data-stu-id="1ea8a-272">First position</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-273">2</span><span class="sxs-lookup"><span data-stu-id="1ea8a-273">2</span></span>
</dt> <dd>

<span data-ttu-id="1ea8a-274">Deuxième position</span><span class="sxs-lookup"><span data-stu-id="1ea8a-274">Second position</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1ea8a-275">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-275">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-276">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-278">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-278">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-279">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-279">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="1ea8a-280">Cette valeur provient du membre du **fabricant** de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-280">This value comes from the **Manufacturer** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-281">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-282">**MaxVoltage**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-282">**MaxVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-283">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-285">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| voltage maximum")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Maximum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-286">Tension maximale de fonctionnement de cet appareil, en millivolts ou 0, si la tension est inconnue.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-286">The maximum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="1ea8a-287">Cette valeur provient du membre **voltage maximal** de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-287">This value comes from the **Maximum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-288">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-288">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-289">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-289">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-290">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-292">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,9 ")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-293">Type de mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-293">Type of physical memory.</span></span> <span data-ttu-id="1ea8a-294">Il s’agit d’une valeur CIM qui est mappée à la valeur SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-294">This is a CIM value that is mapped to the SMBIOS value.</span></span> <span data-ttu-id="1ea8a-295">La propriété **SMBIOSMemoryType** contient le type de mémoire SMBIOS brute.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-295">The **SMBIOSMemoryType** property contains the raw SMBIOS memory type.</span></span>

<span data-ttu-id="1ea8a-296">Cette valeur provient du membre de **type de mémoire** de la structure de l’unité de **mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-296">This value comes from the **Memory Type** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-297">Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-297">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1ea8a-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1ea8a-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="1ea8a-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="1ea8a-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**DRAM synchrone** (3)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="1ea8a-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="1ea8a-303"><span id="EDO"></span><span id="edo"></span>**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-303"><span id="EDO"></span><span id="edo"></span>**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="1ea8a-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="1ea8a-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="1ea8a-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="1ea8a-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="1ea8a-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="1ea8a-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="1ea8a-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="1ea8a-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="1ea8a-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="1ea8a-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="1ea8a-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="1ea8a-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="1ea8a-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="1ea8a-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="1ea8a-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="1ea8a-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-320">DDR2 — peut ne pas être disponible.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-320">DDR2—May not be available.</span></span>

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="1ea8a-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-322">DDR2 (FB-DIMM) peut ne pas être disponible.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-322">DDR2—FB-DIMM,May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-323">24</span><span class="sxs-lookup"><span data-stu-id="1ea8a-323">24</span></span>
</dt> <dd>

<span data-ttu-id="1ea8a-324">DDR3 — peut ne pas être disponible.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-324">DDR3—May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-325">25</span><span class="sxs-lookup"><span data-stu-id="1ea8a-325">25</span></span>
</dt> <dd>

<span data-ttu-id="1ea8a-326">FBD2</span><span class="sxs-lookup"><span data-stu-id="1ea8a-326">FBD2</span></span>

</dt> <dd></dd> <dt>

<span data-ttu-id="1ea8a-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1ea8a-328">**MinVoltage**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-328">**MinVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-329">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-331">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 20 \| voltage minimal")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Minimum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-332">Tension minimale de fonctionnement de cet appareil, en millivolts ou 0, si la tension est inconnue.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-332">The minimum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="1ea8a-333">Cette valeur provient du membre **voltage minimal** de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-333">This value comes from the **Minimum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-334">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-334">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-335">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-335">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-336">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-338">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-338">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-339">Nom de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-339">Name for the physical element.</span></span>

<span data-ttu-id="1ea8a-340">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-340">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-341">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-344">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-344">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-345">Étiquette de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-345">Label for the object.</span></span> <span data-ttu-id="1ea8a-346">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-346">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="1ea8a-347">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-351">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-351">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="1ea8a-352">Par exemple, les données de code-barres associées à un élément qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-352">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="1ea8a-353">Si seules les données de code-barres sont disponibles et uniques ou peuvent être utilisées comme clé d’élément, cette propriété a la **valeur null** et les données de code-barres sont utilisées comme clé de classe dans la propriété de balise.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-353">If only bar code data is available and unique or able to be used as an element key, this property is be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="1ea8a-354">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-355">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-355">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-356">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-358">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-358">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-359">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-359">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="1ea8a-360">Cette valeur provient du membre du **numéro de référence** de la structure de l’unité de **mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-360">This value comes from the **Part Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-361">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-361">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-362">**PositionInRow**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-362">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-363">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-365">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,6»)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-365">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-366">Position de la mémoire physique dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-366">Position of the physical memory in a row.</span></span> <span data-ttu-id="1ea8a-367">Par exemple, s’il utilise des périphériques de mémoire 2 8 bits pour former une ligne de 16 bits, une valeur de 2 (deux) signifie que cette mémoire est le deuxième périphérique, 0 (zéro) est une valeur non valide pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-367">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 (two) means that this memory is the second device—0 (zero) is an invalid value for this property.</span></span>

<span data-ttu-id="1ea8a-368">Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-368">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-369">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-369">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-370">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-372">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-372">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="1ea8a-373">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-373">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-374">**Bande**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-374">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-375">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-377">Si la **valeur est true**, un composant physique est amovible (s’il est conçu pour être pris dans et hors du conteneur physique dans lequel il est normalement trouvé, sans altérer la fonction de l’empaquetage global).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-377">If **TRUE**, a physical component is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="1ea8a-378">Un composant peut toujours être amovible si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-378">A component can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="1ea8a-379">Si l’alimentation peut être « activée » et que le composant a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-379">If power can be "on" and the component removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="1ea8a-380">Par exemple, une puce de processeur pouvant être mise à niveau est amovible.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-380">For example, an upgradable processor chip is removable.</span></span>

<span data-ttu-id="1ea8a-381">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-381">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-382">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-382">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-383">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-383">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-385">Si la **valeur est true**, ce composant de média physique peut être remplacé par un autre physiquement différent.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-385">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="1ea8a-386">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-386">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="1ea8a-387">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-387">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="1ea8a-388">Tous les composants amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-388">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="1ea8a-389">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-389">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-390">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-390">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-391">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-393">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-393">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-394">Numéro alloué par le fabricant pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-394">Manufacturer-allocated number to identify the physical element.</span></span>

<span data-ttu-id="1ea8a-395">Cette valeur provient du membre du **numéro de série** de la structure de l’unité de **mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-395">This value comes from the **Serial Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-396">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-396">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-397">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-397">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-398">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-400">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-400">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-401">Numéro d’unité de conservation de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-401">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="1ea8a-402">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-402">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-403">**SMBIOSMemoryType**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-403">**SMBIOSMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-404">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-406">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| Memory \_ type")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-406">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Memory\_Type")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-407">Type de mémoire SMBIOS brut.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-407">The raw SMBIOS memory type.</span></span> <span data-ttu-id="1ea8a-408">La valeur de la propriété **MemoryType** est une valeur CIM qui est mappée à la valeur SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-408">The value of the **MemoryType** property is a CIM value that is mapped to the SMBIOS value.</span></span>

<span data-ttu-id="1ea8a-409">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-409">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-410">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-410">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-411">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-413">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« nanosecondes »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-413">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-414">Vitesse de la mémoire physique, en nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-414">Speed of the physical memory—in nanoseconds.</span></span>

<span data-ttu-id="1ea8a-415">Cette valeur provient du membre **Speed** de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-415">This value comes from the **Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-416">Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-416">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-417">**État**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-417">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-418">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-420">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-420">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-421">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-421">Current status of the object.</span></span> <span data-ttu-id="1ea8a-422">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-422">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1ea8a-423">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-423">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1ea8a-424">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="1ea8a-424">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1ea8a-425">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-425">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1ea8a-426">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-426">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1ea8a-427">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-427">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1ea8a-428">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-428">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1ea8a-429">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-429">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1ea8a-430">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-430">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1ea8a-431">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-431">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1ea8a-432">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-432">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1ea8a-433">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-433">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1ea8a-434">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-434">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1ea8a-435">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-435">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1ea8a-436">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-436">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1ea8a-437">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-437">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1ea8a-438">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-438">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1ea8a-439">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-439">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1ea8a-440">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-440">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1ea8a-441">**Tag**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-441">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-442">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-443">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-444">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-444">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-445">Identificateur unique pour le périphérique de mémoire physique représenté par une instance de **Win32 \_ PhysicalMemory**.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-445">Unique identifier for the physical memory device that is represented by an instance of **Win32\_PhysicalMemory**.</span></span> <span data-ttu-id="1ea8a-446">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-446">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="1ea8a-447">Exemple : « mémoire physique 1 »</span><span class="sxs-lookup"><span data-stu-id="1ea8a-447">Example: "Physical Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-448">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-448">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-449">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-451">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de mémoire DMTF \| 002,7 "), [**unités**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-451">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-452">Largeur totale, en bits, de la mémoire physique, y compris les bits de vérification ou de correction des erreurs.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-452">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="1ea8a-453">S’il n’existe aucun bit de correction des erreurs, la valeur de cette propriété doit correspondre à ce qui est spécifié pour la propriété **DataWidth** .</span><span class="sxs-lookup"><span data-stu-id="1ea8a-453">If there are no error correction bits, the value in this property should match what is specified for the **DataWidth** property.</span></span>

<span data-ttu-id="1ea8a-454">Cette valeur provient du membre **Width total** de la structure de l' **unité de mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-454">This value comes from the **Total Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1ea8a-455">Cette propriété est héritée de la [**\_ PhysicalMemory CIM**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-455">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ea8a-456">**TypeDetail**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-456">**TypeDetail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-457">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-458">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-459">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 17 \| Detail type")</span><span class="sxs-lookup"><span data-stu-id="1ea8a-459">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Type Detail")</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-460">Type de mémoire physique représenté.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-460">Type of physical memory represented.</span></span>

<span data-ttu-id="1ea8a-461">Cette valeur provient du membre de **détail de type** de la structure de l’unité de **mémoire** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-461">This value comes from the **Type Detail** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="1ea8a-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Réservé** (1)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1ea8a-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (2)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1ea8a-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (4)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span data-ttu-id="1ea8a-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Page rapide** (8)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Fast-paged** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span data-ttu-id="1ea8a-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Colonne statique** (16)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Static column** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span data-ttu-id="1ea8a-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-statique** (32)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-static** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span data-ttu-id="1ea8a-468"><span id="RAMBUS"></span><span id="rambus"></span>**Rambus** (64)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-468"><span id="RAMBUS"></span><span id="rambus"></span>**RAMBUS** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="1ea8a-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchrone** (128)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchronous** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span data-ttu-id="1ea8a-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="1ea8a-471"><span id="EDO"></span><span id="edo"></span>**Edo** (512)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-471"><span id="EDO"></span><span id="edo"></span>**EDO** (512)</span></span>


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span data-ttu-id="1ea8a-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**DRAM de fenêtre** (1024)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Window DRAM** (1024)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="1ea8a-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Mémoire cache DRAM** (2048)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (2048)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>

<span data-ttu-id="1ea8a-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Non volatile** (4096)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Non-volatile** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="1ea8a-475">Non volatil</span><span class="sxs-lookup"><span data-stu-id="1ea8a-475">Nonvolatile</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1ea8a-476">**Version**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-476">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ea8a-477">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-478">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea8a-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ea8a-479">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1ea8a-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1ea8a-480">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-480">Version of the physical element.</span></span>

<span data-ttu-id="1ea8a-481">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-481">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ea8a-482">Notes</span><span class="sxs-lookup"><span data-stu-id="1ea8a-482">Remarks</span></span>

<span data-ttu-id="1ea8a-483">La classe **Win32 \_ PhysicalMemory** est dérivée de [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1ea8a-483">The **Win32\_PhysicalMemory** class is derived from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1ea8a-484">Exemples</span><span class="sxs-lookup"><span data-stu-id="1ea8a-484">Examples</span></span>

<span data-ttu-id="1ea8a-485">L’exemple PowerShell- [ComputerInfo-Query Computer Info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sur la Galerie TechNet utilise un certain nombre d’appels au matériel et aux logiciels, notamment **Win32 \_ PhysicalMemory**, pour afficher des informations sur un système local ou distant.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-485">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to display information about a local or remote system.</span></span>

<span data-ttu-id="1ea8a-486">L’exemple PowerShell de [rapport de serveur](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) de la Galerie TechNet utilise un certain nombre d’appels au matériel et aux logiciels, y compris **Win32 \_ PhysicalMemory**, pour recueillir des informations sur le serveur et les publier dans un document Word.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-486">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to gather server information and publish in Word document.</span></span>

<span data-ttu-id="1ea8a-487">L’exemple de code PowerShell suivant récupère des informations relatives à la mémoire physique de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1ea8a-487">The following PowerShell code sample retrieves information regarding the physical memory of the local computer.</span></span>


```PowerShell
function get-WmiMemoryFormFactor {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 22) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-SiP"}
3     {"03-DIP"}
4     {"04-ZIP"}
5     {"05-SOJ"}
6     {"06-Proprietary"}
7     {"07-SIMM"}
8     {"08-DIMM"}
9     {"09-TSOPO"}
10     {"10-PGA"}
11     {"11-RIM"}
12     {"12-SODIMM"}
13     {"13-SRIMM"}
14     {"14-SMD"}
15     {"15-SSMP"}
16     {"16-QFP"}
17     {"17-TQFP"}
18     {"18-SOIC"}
19     {"19-LCC"}
20     {"20-PLCC"}
21     {"21-FPGA"}
22     {"22-LGA"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}

# Helper function to return memory Interleave  Position

function get-WmiInterleavePosition {
param ([uint32] $char)

If ($char -ge 0 -and  $char -le 2) {

switch ($char) {
0     {"00-Non-Interleaved"}
1     {"01-First Position"}
2     {"02-Second Position"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}


# Helper function to return Memory Tupe
function get-WmiMemoryType {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 20) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-DRAM"}
3     {"03-Synchronous DRAM"}
4     {"04-Cache DRAM"}
5     {"05-EDO"}
6     {"06-EDRAM"}
7     {"07-VRAM"}
8     {"08-SRAM"}
9     {"09-ROM"}
10     {"10-ROM"}
11     {"11-FLASH"}
12     {"12-EEPROM"}
13     {"13-FEPROM"}
14     {"14-EPROM"}
15     {"15-CDRAM"}
16     {"16-3DRAM"}
17     {"17-SDRAM"}
18     {"18-SGRAM"}
19     {"19-RDRAM"}
20     {"20-DDR"}
}

}

else {"{0} - undefined value" -f $char
}

Return
}


# Get the object
$memory = Get-WMIObject Win32_PhysicalMemory

#  Format and Print
"System has {0} memory sticks:" -f $memory.count

Foreach ($stick in $memory) {

# Do some conversions
$cap=$stick.capacity/1mb
$ff=get-WmiMemoryFormFactor($stick.FormFactor)
$ilp=get-WmiInterleavePosition($stick.InterleavePosition)
$mt=get-WMIMemoryType($stick.MemoryType)

# print details of each stick
"BankLabel            {0}"  -f $stick.banklabel
"Capacity (MB)        {0}"  -f $cap
"Caption              {0}"  -f $stick.Caption
"CreationClassName    {0}"  -f $stick.creationclassname
"DataWidth            {0}"  -f $stick.DataWidth
"Description          {0}"  -f $stick.Description
"DeviceLocator        {0}"  -f $stick.DeviceLocator
"FormFactor           {0}"  -f $ff
"HotSwappable         {0}"  -f $stick.HotSwappable
"InstallDate          {0}"  -f $stick.InstallDate
"InterleaveDataDepth  {0}"  -f $stick.InterleaveDataDepth
"InterleavePosition   {0}"  -f $ilp
"Manufacturer         {0}"  -f $stick.Manufacturer
"MemoryType           {0}"  -f $mt
"Model                {0}"  -f $stick.Model
"Name                 {0}"  -f $stick.Name
"OtherIdentifyingInfo {0}"  -f $stick.OtherIdentifyingInfo
"PartNumber           {0}"  -f $stick.PartNumber
"PositionInRow        {0}"  -f $stick.PositionInRow
"PoweredOn            {0}"  -f $stick.PoweredOn
"Removable            {0}"  -f $stick.Removable
"Replaceable          {0}"  -f $stick.Replaceable
"SerialNumber         {0}"  -f $stick.SerialNumber
"SKU                  {0}"  -f $stick.SKU 
"Speed                {0}"  -f $stick.Speed 
"Status               {0}"  -f $stick.Status
"Tag                  {0}"  -f $stick.Tag
"TotalWidth           {0}"  -f $stick.TotalWidth 
"TypeDetail           {0}"  -f $stick.TypeDetail
"Version              {0}"  -f $stick.Version
""
}
"-----"
```



## <a name="requirements"></a><span data-ttu-id="1ea8a-488">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ea8a-488">Requirements</span></span>



| <span data-ttu-id="1ea8a-489">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ea8a-489">Requirement</span></span> | <span data-ttu-id="1ea8a-490">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ea8a-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea8a-491">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ea8a-491">Minimum supported client</span></span><br/> | <span data-ttu-id="1ea8a-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ea8a-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1ea8a-493">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ea8a-493">Minimum supported server</span></span><br/> | <span data-ttu-id="1ea8a-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ea8a-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1ea8a-495">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1ea8a-495">Namespace</span></span><br/>                | <span data-ttu-id="1ea8a-496">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1ea8a-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1ea8a-497">MOF</span><span class="sxs-lookup"><span data-stu-id="1ea8a-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ea8a-498"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ea8a-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ea8a-499">DLL</span><span class="sxs-lookup"><span data-stu-id="1ea8a-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ea8a-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ea8a-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ea8a-501">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ea8a-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea8a-502">**\_PHYSICALMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="1ea8a-502">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dt>

[<span data-ttu-id="1ea8a-503">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="1ea8a-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
