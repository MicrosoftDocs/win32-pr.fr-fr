---
description: La \_ classe WMI PortResource WMI représente un port d’e/s sur un système informatique exécutant Windows.
ms.assetid: 820f4f49-571c-4044-aefc-69bac5d59e6f
ms.tgt_platform: multiple
title: Classe Win32_PortResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortResource
- Win32_PortResource.Alias
- Win32_PortResource.Caption
- Win32_PortResource.CreationClassName
- Win32_PortResource.CSCreationClassName
- Win32_PortResource.CSName
- Win32_PortResource.Description
- Win32_PortResource.EndingAddress
- Win32_PortResource.InstallDate
- Win32_PortResource.Name
- Win32_PortResource.StartingAddress
- Win32_PortResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3c08424dd1aee555068c78a9308afe732634c61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950475"
---
# <a name="win32_portresource-class"></a><span data-ttu-id="66ecb-103">\_Classe PortResource Win32</span><span class="sxs-lookup"><span data-stu-id="66ecb-103">Win32\_PortResource class</span></span>

<span data-ttu-id="66ecb-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PortResource** WMI représente un port d’e/s sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="66ecb-104">The **Win32\_PortResource** [WMI class](../wmisdk/retrieving-a-class.md) represents an I/O port on a computer system running Windows.</span></span>

<span data-ttu-id="66ecb-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="66ecb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="66ecb-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="66ecb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ecb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66ecb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PortResource : Win32_SystemMemoryResource
{
  boolean  Alias;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="66ecb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="66ecb-108">Members</span></span>

<span data-ttu-id="66ecb-109">La classe **Win32 \_ PortResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="66ecb-109">The **Win32\_PortResource** class has these types of members:</span></span>

-   [<span data-ttu-id="66ecb-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66ecb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66ecb-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66ecb-111">Properties</span></span>

<span data-ttu-id="66ecb-112">La classe **Win32 \_ PortResource** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="66ecb-112">The **Win32\_PortResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66ecb-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="66ecb-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-114">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="66ecb-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-116">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Configuration Manager structures \| IO \_ info")</span><span class="sxs-lookup"><span data-stu-id="66ecb-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Configuration Manager Structures\|IO\_INFO")</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-117">Si la **valeur est true**, cette instance représente l’une des plages avec un alias.</span><span class="sxs-lookup"><span data-stu-id="66ecb-117">If **TRUE**, this instance represents one of the ranges with an alias.</span></span> <span data-ttu-id="66ecb-118">Si la **valeur est false**, l’instance représente une adresse de port de base.</span><span class="sxs-lookup"><span data-stu-id="66ecb-118">If **FALSE**, the instance represents a base port address.</span></span> <span data-ttu-id="66ecb-119">Une adresse de port de base est une adresse de port prédéterminée dédiée à un service ou un périphérique spécifique.</span><span class="sxs-lookup"><span data-stu-id="66ecb-119">A base port address is a predetermined port address dedicated to a specific service or device.</span></span> <span data-ttu-id="66ecb-120">L’adresse d’un alias de port est celle à laquelle un appareil répond comme s’il s’agissait de l’adresse réelle d’un port d’e/s.</span><span class="sxs-lookup"><span data-stu-id="66ecb-120">A port alias address is one that a device responds to as if it were the actual address of an I/O port.</span></span>

</dd> <dt>

<span data-ttu-id="66ecb-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="66ecb-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66ecb-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-124">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-125">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="66ecb-125">Short description of the object.</span></span>

<span data-ttu-id="66ecb-126">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="66ecb-127">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="66ecb-127">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66ecb-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-130">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="66ecb-130">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-131">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="66ecb-131">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="66ecb-132">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="66ecb-132">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="66ecb-133">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-133">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="66ecb-134">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="66ecb-134">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66ecb-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-137">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="66ecb-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-138">Nom de la classe de création du système d’étendue de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="66ecb-138">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="66ecb-139">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-139">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="66ecb-140">**CSName**</span><span class="sxs-lookup"><span data-stu-id="66ecb-140">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66ecb-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-143">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="66ecb-143">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-144">Nom du système informatique d’étendue.</span><span class="sxs-lookup"><span data-stu-id="66ecb-144">Name of the scoping computer system.</span></span>

<span data-ttu-id="66ecb-145">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-145">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="66ecb-146">**Description**</span><span class="sxs-lookup"><span data-stu-id="66ecb-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66ecb-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-149">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="66ecb-149">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-150">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="66ecb-150">Description of the object.</span></span>

<span data-ttu-id="66ecb-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="66ecb-152">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="66ecb-152">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-153">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66ecb-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-155">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s mappées en mémoire DMTF \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="66ecb-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-156">Adresse de fin des e/s mappées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="66ecb-156">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="66ecb-157">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-157">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="66ecb-158">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="66ecb-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="66ecb-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-160">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="66ecb-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-162">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="66ecb-162">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-163">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="66ecb-163">Date and time the object was installed.</span></span> <span data-ttu-id="66ecb-164">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="66ecb-164">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="66ecb-165">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="66ecb-166">**Nom**</span><span class="sxs-lookup"><span data-stu-id="66ecb-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66ecb-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-169">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="66ecb-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-170">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="66ecb-170">Label by which the object is known.</span></span> <span data-ttu-id="66ecb-171">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="66ecb-171">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="66ecb-172">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="66ecb-173">**De la**</span><span class="sxs-lookup"><span data-stu-id="66ecb-173">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-174">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66ecb-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-176">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("MappingStrings"), [**Key**](../wmisdk/key-qualifier.md), [](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s mappées en mémoire DMTF \| 001,1»)</span><span class="sxs-lookup"><span data-stu-id="66ecb-176">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-177">Adresse de début des e/s mappées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="66ecb-177">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="66ecb-178">La propriété de l’identificateur de ressource matérielle doit être définie sur cette valeur pour construire la clé de ressource d’e/s mappée.</span><span class="sxs-lookup"><span data-stu-id="66ecb-178">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="66ecb-179">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-179">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="66ecb-180">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="66ecb-181">**État**</span><span class="sxs-lookup"><span data-stu-id="66ecb-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66ecb-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66ecb-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66ecb-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66ecb-184">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="66ecb-184">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="66ecb-185">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="66ecb-185">Current status of the object.</span></span> <span data-ttu-id="66ecb-186">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="66ecb-186">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="66ecb-187">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="66ecb-187">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="66ecb-188">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="66ecb-188">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="66ecb-189">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="66ecb-189">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="66ecb-190">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="66ecb-190">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="66ecb-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="66ecb-192">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="66ecb-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="66ecb-193">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="66ecb-194">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="66ecb-195">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66ecb-196">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="66ecb-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="66ecb-197">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="66ecb-198">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="66ecb-199">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="66ecb-200">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="66ecb-201">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="66ecb-202">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="66ecb-203">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="66ecb-204">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="66ecb-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="66ecb-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="66ecb-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="66ecb-206">Notes</span><span class="sxs-lookup"><span data-stu-id="66ecb-206">Remarks</span></span>

<span data-ttu-id="66ecb-207">La classe **Win32 \_ PortResource** est dérivée de [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md).</span><span class="sxs-lookup"><span data-stu-id="66ecb-207">The **Win32\_PortResource** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66ecb-208">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66ecb-208">Requirements</span></span>



| <span data-ttu-id="66ecb-209">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66ecb-209">Requirement</span></span> | <span data-ttu-id="66ecb-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="66ecb-210">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66ecb-211">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66ecb-211">Minimum supported client</span></span><br/> | <span data-ttu-id="66ecb-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66ecb-212">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66ecb-213">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66ecb-213">Minimum supported server</span></span><br/> | <span data-ttu-id="66ecb-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66ecb-214">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66ecb-215">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66ecb-215">Namespace</span></span><br/>                | <span data-ttu-id="66ecb-216">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="66ecb-216">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66ecb-217">MOF</span><span class="sxs-lookup"><span data-stu-id="66ecb-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66ecb-218"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66ecb-218"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66ecb-219">DLL</span><span class="sxs-lookup"><span data-stu-id="66ecb-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66ecb-220"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66ecb-220"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ecb-221">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66ecb-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ecb-222">**\_SystemMemoryResource Win32**</span><span class="sxs-lookup"><span data-stu-id="66ecb-222">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="66ecb-223">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="66ecb-223">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
