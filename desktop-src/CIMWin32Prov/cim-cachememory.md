---
description: La \_ classe CIM CacheMemory définit les fonctionnalités et la gestion de la mémoire cache.
ms.assetid: cdf35122-2057-45fa-818b-ce542d8e82b0
ms.tgt_platform: multiple
title: Classe CIM_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory
- CIM_CacheMemory.Caption
- CIM_CacheMemory.Description
- CIM_CacheMemory.InstallDate
- CIM_CacheMemory.Name
- CIM_CacheMemory.Status
- CIM_CacheMemory.Availability
- CIM_CacheMemory.ConfigManagerErrorCode
- CIM_CacheMemory.ConfigManagerUserConfig
- CIM_CacheMemory.CreationClassName
- CIM_CacheMemory.DeviceID
- CIM_CacheMemory.PowerManagementCapabilities
- CIM_CacheMemory.ErrorCleared
- CIM_CacheMemory.ErrorDescription
- CIM_CacheMemory.LastErrorCode
- CIM_CacheMemory.PNPDeviceID
- CIM_CacheMemory.PowerManagementSupported
- CIM_CacheMemory.StatusInfo
- CIM_CacheMemory.SystemCreationClassName
- CIM_CacheMemory.SystemName
- CIM_CacheMemory.Access
- CIM_CacheMemory.BlockSize
- CIM_CacheMemory.NumberOfBlocks
- CIM_CacheMemory.Purpose
- CIM_CacheMemory.ErrorMethodology
- CIM_CacheMemory.AdditionalErrorData
- CIM_CacheMemory.CorrectableError
- CIM_CacheMemory.EndingAddress
- CIM_CacheMemory.ErrorAccess
- CIM_CacheMemory.ErrorAddress
- CIM_CacheMemory.ErrorData
- CIM_CacheMemory.ErrorDataOrder
- CIM_CacheMemory.ErrorInfo
- CIM_CacheMemory.ErrorResolution
- CIM_CacheMemory.ErrorTime
- CIM_CacheMemory.ErrorTransferSize
- CIM_CacheMemory.OtherErrorDescription
- CIM_CacheMemory.StartingAddress
- CIM_CacheMemory.SystemLevelAddress
- CIM_CacheMemory.Associativity
- CIM_CacheMemory.CacheType
- CIM_CacheMemory.FlushTimer
- CIM_CacheMemory.Level
- CIM_CacheMemory.LineSize
- CIM_CacheMemory.ReadPolicy
- CIM_CacheMemory.ReplacementPolicy
- CIM_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b7a7add96c523dae6b683d597ba36953c605d28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861362"
---
# <a name="cim_cachememory-class"></a><span data-ttu-id="f7a2d-103">\_Classe CIM CacheMemory</span><span class="sxs-lookup"><span data-stu-id="f7a2d-103">CIM\_CacheMemory class</span></span>

<span data-ttu-id="f7a2d-104">La classe **CIM \_ CacheMemory** définit les fonctionnalités et la gestion de la mémoire cache.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-104">The **CIM\_CacheMemory** class defines the capabilities and management of cache memory.</span></span>

<span data-ttu-id="f7a2d-105">La mémoire cache est la RAM dédiée ou allouée dans laquelle un processeur recherche d’abord des données.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-105">Cache memory is the dedicated or allocated RAM where a processor first searches for data.</span></span> <span data-ttu-id="f7a2d-106">Les données de la mémoire cache sont rapidement remises au processeur et sont généralement décrites par la proximité du processeur (par exemple, le cache principal ou secondaire).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-106">Data in cache memory is quickly delivered to the processor and is usually described by its proximity to the processor (for example, primary or secondary cache).</span></span> <span data-ttu-id="f7a2d-107">Un lecteur de disque qui comprend la mémoire vive allouée pour le maintien de la dernière lecture ou des données adjacentes du disque (pour accélérer la récupération) est également modélisé comme mémoire cache.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-107">A disk drive that includes RAM allocated for holding the disk's most recently read or adjacent data (to speed up retrieval) is also modeled as cache memory.</span></span>

> [!Note]  
> <span data-ttu-id="f7a2d-108">La mémoire cache n’est pas un système d’exploitation ou une mémoire tampon au niveau de l’application ; Il s’agit de la mémoire RAM qui a été allouée pour la mise en cache des données du processeur.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-108">Cache memory is not an operating-system or application-level buffer; it is RAM that has been allocated for caching processor data.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="f7a2d-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f7a2d-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f7a2d-111">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f7a2d-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a2d-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7a2d-113">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B65-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CacheMemory : CIM_Memory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  uint64   NumberOfBlocks;
  string   Purpose;
  string   ErrorMethodology;
  uint8    AdditionalErrorData[];
  boolean  CorrectableError;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint16   ErrorInfo;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  string   OtherErrorDescription;
  uint64   StartingAddress;
  boolean  SystemLevelAddress;
  uint16   Associativity;
  uint16   CacheType;
  uint32   FlushTimer;
  uint16   Level;
  uint32   LineSize;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="f7a2d-114">Membres</span><span class="sxs-lookup"><span data-stu-id="f7a2d-114">Members</span></span>

<span data-ttu-id="f7a2d-115">La classe **CIM \_ CacheMemory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f7a2d-115">The **CIM\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="f7a2d-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f7a2d-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="f7a2d-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f7a2d-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f7a2d-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f7a2d-118">Methods</span></span>

<span data-ttu-id="f7a2d-119">La classe **CIM \_ CacheMemory** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-119">The **CIM\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="f7a2d-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="f7a2d-120">Method</span></span>                                                                 | <span data-ttu-id="f7a2d-121">Description</span><span class="sxs-lookup"><span data-stu-id="f7a2d-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7a2d-122">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-122">**Reset**</span></span>](reset-method-in-class-cim-cachememory.md)                 | <span data-ttu-id="f7a2d-123">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="f7a2d-124">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="f7a2d-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cachememory.md) | <span data-ttu-id="f7a2d-126">Définit l’état d’alimentation souhaité pour un périphérique logique et le moment où l’appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="f7a2d-127">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f7a2d-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f7a2d-128">Properties</span></span>

<span data-ttu-id="f7a2d-129">La classe **CIM \_ CacheMemory** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-129">The **CIM\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7a2d-130">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-133">Décrit les propriétés en lecture/écriture du média.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="f7a2d-134">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-135">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="f7a2d-136">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="f7a2d-137">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="f7a2d-138">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="f7a2d-139">**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-141">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-143">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,18 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-144">Tableau d’octets qui contiennent des informations d’erreur supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="f7a2d-145">Par exemple, le syndrome de la vérification et de la correction des erreurs (ECC), ou le retour des bits de vérification si une méthodologie d’erreur basée sur CRC est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="f7a2d-146">Dans ce dernier cas, si une erreur de bit unique est reconnue et que l’algorithme CRC est connu, le bit exact qui a échoué peut être déterminé.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="f7a2d-147">Ce type de données (syndrome ECC, données de bit de contrôle ou de parité ou autres informations fournies par le fournisseur) est inclus dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="f7a2d-148">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f7a2d-149">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-150">**Associativité**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-150">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-153">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,15»)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-154">Énumération qui définit l’associativité du cache système.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-154">Enumeration that defines the system cache associativity.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7a2d-155">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-156">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-156">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="f7a2d-157">**Mappé direct** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-157">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="f7a2d-158">**Set-associatif** bidirectionnel (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-158">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="f7a2d-159">**Set-associatif à 4 voies** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-159">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="f7a2d-160">**Entièrement associatif** (6)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-160">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="f7a2d-161">**Set-associatif à 8 voies** (7)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-161">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="f7a2d-162">**Set-associatif à 16 voies** (8)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-162">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-163">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-163">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-164">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-166">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-167">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-167">Availability and status of the device.</span></span>

<span data-ttu-id="f7a2d-168">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-168">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7a2d-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f7a2d-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f7a2d-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f7a2d-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f7a2d-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f7a2d-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f7a2d-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f7a2d-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f7a2d-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f7a2d-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f7a2d-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f7a2d-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-182">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-182">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f7a2d-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-184">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-184">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f7a2d-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-186">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-186">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f7a2d-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f7a2d-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-189">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-189">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f7a2d-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-191">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-191">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f7a2d-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-193">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-193">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f7a2d-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-195">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-195">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f7a2d-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-197">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-197">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-198">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-198">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-199">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-201">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-202">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-202">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="f7a2d-203">Si vous spécifiez une taille de bloc variable, la taille maximale du bloc, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-203">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="f7a2d-204">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1 (un).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-204">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="f7a2d-205">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f7a2d-206">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-207">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-207">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-210">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,9»)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-211">Spécifie la mise en cache des instructions, la mise en cache des données, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-211">Specifies instruction caching, data caching, or both.</span></span> <span data-ttu-id="f7a2d-212">« Other » et « Unknown » peuvent également être définis.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-212">"Other" and "Unknown" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7a2d-213">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-213">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-214">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-214">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="f7a2d-215">**Instruction** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-215">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="f7a2d-216">**Données** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-216">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="f7a2d-217">**Unifié** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-217">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-221">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-222">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-222">A short textual description of the object.</span></span>

<span data-ttu-id="f7a2d-223">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-224">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-225">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-227">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-228">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-228">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f7a2d-229">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f7a2d-230">**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-230">**This device is working properly.**</span></span> <span data-ttu-id="f7a2d-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-231">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f7a2d-232">**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-232">**This device is not configured correctly.**</span></span> <span data-ttu-id="f7a2d-233">(1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-233">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f7a2d-234">**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-234">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f7a2d-235">(2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f7a2d-236">**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-236">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f7a2d-237">(3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-237">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f7a2d-238">**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-238">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f7a2d-239">(4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-239">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f7a2d-240">**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-240">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f7a2d-241">(5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-241">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f7a2d-242">**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-242">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f7a2d-243"> (6)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-243">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f7a2d-244">**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-244">**Cannot filter.**</span></span> <span data-ttu-id="f7a2d-245">(7)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-245">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f7a2d-246">**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-246">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f7a2d-247">(8)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-247">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f7a2d-248">**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-248">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f7a2d-249">(9)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-249">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f7a2d-250">**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-250">**This device cannot start.**</span></span> <span data-ttu-id="f7a2d-251">(10)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-251">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f7a2d-252">**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-252">**This device failed.**</span></span> <span data-ttu-id="f7a2d-253">(11)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-253">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f7a2d-254">**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-254">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f7a2d-255">douze</span><span class="sxs-lookup"><span data-stu-id="f7a2d-255">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f7a2d-256">**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-256">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f7a2d-257">(13)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-257">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f7a2d-258">**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-258">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f7a2d-259">(14)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-259">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f7a2d-260">**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-260">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f7a2d-261">(15)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-261">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f7a2d-262">**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-262">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f7a2d-263">(16)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-263">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f7a2d-264">**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-264">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f7a2d-265">(17)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-265">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f7a2d-266">**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-266">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f7a2d-267">(18)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-267">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f7a2d-268">**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-268">**Failure using the VxD loader.**</span></span> <span data-ttu-id="f7a2d-269">(19)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-269">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f7a2d-270">**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-270">**Your registry might be corrupted.**</span></span> <span data-ttu-id="f7a2d-271">(20)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-271">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f7a2d-272">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-272">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f7a2d-273">(21)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-273">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f7a2d-274">**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-274">**This device is disabled.**</span></span> <span data-ttu-id="f7a2d-275">(22)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-275">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f7a2d-276">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-276">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f7a2d-277">(23)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-277">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f7a2d-278">**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-278">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f7a2d-279">(24)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-279">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f7a2d-280">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-280">**Windows is still setting up this device.**</span></span> <span data-ttu-id="f7a2d-281">(25)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-281">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f7a2d-282">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-282">**Windows is still setting up this device.**</span></span> <span data-ttu-id="f7a2d-283">(26)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-283">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f7a2d-284">**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-284">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f7a2d-285">(27)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-285">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f7a2d-286">**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-286">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f7a2d-287">(28)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-287">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f7a2d-288">**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-288">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f7a2d-289">(29)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-289">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f7a2d-290">**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-290">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f7a2d-291">(30)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-291">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f7a2d-292">**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-292">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f7a2d-293">31</span><span class="sxs-lookup"><span data-stu-id="f7a2d-293">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-295">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-297">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-298">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f7a2d-299">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-300">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-300">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-301">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-303">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-304">Si la **valeur est true**, l’erreur la plus récente était correcte.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-304">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="f7a2d-305">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-305">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f7a2d-306">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-306">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-308">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-310">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-311">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f7a2d-312">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f7a2d-313">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-314">**Description**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-317">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-318">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-318">A textual description of the object.</span></span>

<span data-ttu-id="f7a2d-319">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-323">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-324">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-324">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="f7a2d-325">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-326">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-326">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-327">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-329">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,4 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-330">Adresse de fin référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-330">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="f7a2d-331">L’adresse de fin est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-331">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="f7a2d-332">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-332">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f7a2d-333">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-333">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-334">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-334">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-335">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-337">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,15 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-338">Opération d’accès à la mémoire qui a provoqué la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-338">Memory access operation that caused the last error.</span></span> <span data-ttu-id="f7a2d-339">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="f7a2d-339">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="f7a2d-340">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-340">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f7a2d-341">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7a2d-342">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-342">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-343">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-343">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="f7a2d-344">**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-344">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="f7a2d-345">**Écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-345">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="f7a2d-346">**Écriture partielle** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-346">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-347">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-347">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-348">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-350">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,19 "," MIF. \|Périphérique de mémoire DMTF \| 002,20 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-350">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-351">Adresse de la dernière erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-351">Address of the last memory error.</span></span> <span data-ttu-id="f7a2d-352">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="f7a2d-352">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="f7a2d-353">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-353">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f7a2d-354">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-354">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f7a2d-355">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-355">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-357">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-359">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-359">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f7a2d-360">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-361">**Partagefichiers**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-361">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-362">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-362">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-364">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,17 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-364">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-365">Données capturées au cours du dernier accès mémoire erroné.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-365">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="f7a2d-366">Les données occupent les *n* premiers octets du tableau qui sont nécessaires pour contenir le nombre de bits spécifié par la propriété **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="f7a2d-366">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="f7a2d-367">Si **ErrorTransferSize** est égal à 0, cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-367">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="f7a2d-368">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-368">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-369">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-369">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-370">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-372">Ordre des données stockées dans la propriété **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="f7a2d-372">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="f7a2d-373">Si **ErrorTransferSize** est égal à 0, cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-373">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="f7a2d-374">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-374">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-376">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-376">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="f7a2d-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Octet le moins significatif en premier** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-378">Octet le moins significatif en premier.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-378">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="f7a2d-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Octet le plus significatif en premier** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-380">Octet le plus significatif en premier.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-380">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-384">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-384">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="f7a2d-385">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-387">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-389">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ mémoire CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-390">Type d’erreur qui s’est produite le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="f7a2d-391">Les valeurs 12 à 14 ne sont pas définies dans le schéma CIM, car DMI mélange la sémantique du type d’erreur et indique si elle a été corrigée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-391">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="f7a2d-392">La propriété **CorrectableError** indique si une erreur peut être corrigée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-392">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<span data-ttu-id="f7a2d-393">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7a2d-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-395">Autre.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-395">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-397">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-397">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f7a2d-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-399">OK.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-399">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="f7a2d-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lecture incorrecte** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-401">Lecture incorrecte.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-401">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="f7a2d-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Erreur de parité** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-403">Erreur de parité.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-403">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="f7a2d-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Erreur de bit unique** (6)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-405">Erreur sur un bit.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-405">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="f7a2d-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Erreur double bit** (7)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-407">Erreur double bit.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-407">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="f7a2d-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Erreur multibits** (8)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-409">Erreur multi-bit.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-409">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="f7a2d-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Erreur de grignotage** (9)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-411">Erreur de Quartet.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-411">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="f7a2d-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Erreur de somme de contrôle** (10)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-413">Erreur de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-413">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="f7a2d-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Erreur CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-415">Erreur CRC.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-415">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f7a2d-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (12)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-417">Non défini.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-417">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f7a2d-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (13)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-419">Non défini.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-419">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f7a2d-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (14)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-421">Non défini.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-421">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-422">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-422">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-423">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-425">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-426">Indique si la parité ou les algorithmes CRC, ECC ou d’autres mécanismes sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-426">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="f7a2d-427">Vous pouvez également fournir des détails sur l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-427">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="f7a2d-428">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-428">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-429">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-429">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-430">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-432">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,21 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-433">Spécifie la plage, en octets, à laquelle la dernière erreur peut être résolue.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-433">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="f7a2d-434">Par exemple, si les adresses d’erreurs sont résolues en bit 11 (c’est-à-dire, sur une base de page standard), les erreurs peuvent être résolues en limites de 4 Ko et cette propriété est définie sur 4000.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-434">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="f7a2d-435">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-435">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f7a2d-436">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-436">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f7a2d-437">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-437">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-438">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-438">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-439">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-441">Date et heure auxquelles la dernière erreur de mémoire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-441">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="f7a2d-442">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="f7a2d-442">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="f7a2d-443">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-443">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f7a2d-444">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-444">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-445">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-445">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-446">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-446">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-448">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,16 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-449">Taille du transfert de données, en bits, à l’origine de la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-449">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="f7a2d-450">La valeur 0 indique qu’il n’y A pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-450">A value of 0 indicates no error.</span></span> <span data-ttu-id="f7a2d-451">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété doit être définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-451">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

<span data-ttu-id="f7a2d-452">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-452">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-453">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-453">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-454">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-454">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-456">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,14 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" secondes ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-457">Durée maximale, en secondes, pendant laquelle les lignes modifiées ou les compartiments peuvent demeurer dans le cache avant d’être vidés.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-457">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="f7a2d-458">La valeur 0 indique qu’un vidage du cache n’est pas contrôlé par un minuteur de vidage.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-458">A value of 0 indicates that a cache flush is not controlled by a flushing timer.</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-460">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-461">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-462">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-463">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-463">Indicates when the object was installed.</span></span> <span data-ttu-id="f7a2d-464">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-464">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f7a2d-465">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-466">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-466">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-467">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-468">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-469">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-469">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f7a2d-470">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-471">**Niveau**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-471">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-472">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-473">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-474">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,2»)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-475">Spécifie s’il s’agit du cache principal, secondaire ou tertiaire.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-475">Specifies whether this is the primary, secondary or tertiary cache.</span></span> <span data-ttu-id="f7a2d-476">« Other », « Unknown » et « non applicable » peuvent également être définis.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-476">"Other", "Unknown", and "Not Applicable" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7a2d-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-478">Autre.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-478">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-480">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-480">Unknown.</span></span>

</dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="f7a2d-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Principal** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-482">Essentielles.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-482">Primary.</span></span>

</dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="f7a2d-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondaire** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-484">Secondaire.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-484">Secondary.</span></span>

</dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="f7a2d-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiaire** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-486">Tertiaire.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-486">Tertiary.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f7a2d-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-488">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-488">Not applicable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-489">**Ligner**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-489">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-490">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-490">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-491">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-492">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,10 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-492">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-493">Taille, en octets, d’un compartiment ou d’une ligne de cache unique.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-493">Size, in bytes, of a single cache bucket or line.</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-494">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-494">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-495">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-496">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-497">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-497">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-498">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-498">Label by which the object is known.</span></span> <span data-ttu-id="f7a2d-499">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-499">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f7a2d-500">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-500">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-501">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-501">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-502">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-502">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-503">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-504">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-505">Nombre de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-505">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="f7a2d-506">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-506">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="f7a2d-507">Si la valeur de **BlockSize** est 1 (un), cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-507">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="f7a2d-508">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-508">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f7a2d-509">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-509">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-510">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-510">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-511">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-512">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-513">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ mémoire CIM**](cim-memory.md).**ErrorInfo**»)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-513">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-514">Chaîne de forme libre qui fournit des informations si la propriété **ErrorType** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-514">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="f7a2d-515">Si elle n’a pas la valeur 1, cette chaîne n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-515">If it is not set to 1, then this string has no meaning.</span></span>

<span data-ttu-id="f7a2d-516">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-516">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-517">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-517">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-518">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-520">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-520">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-521">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-521">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f7a2d-522">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="f7a2d-522">Example: "\*PNP030b"</span></span>

<span data-ttu-id="f7a2d-523">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-524">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-524">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-525">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-525">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-526">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-527">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-527">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="f7a2d-528">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-530">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-530">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f7a2d-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-532">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-532">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f7a2d-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-534">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-534">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f7a2d-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-536">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-536">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f7a2d-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-538">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-538">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f7a2d-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-540">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-540">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="f7a2d-541">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-541">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="f7a2d-542">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-542">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f7a2d-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-544">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-544">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f7a2d-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-546">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-546">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-547">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-547">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-548">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-548">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-549">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-550">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-550">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f7a2d-551">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f7a2d-551">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f7a2d-552">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-552">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f7a2d-553">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f7a2d-553">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f7a2d-554">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-554">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-555">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-555">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-556">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-557">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-557">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-558">Chaîne de forme libre qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-558">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="f7a2d-559">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-559">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-560">**Des**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-560">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-561">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-562">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-563">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,13»)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-563">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-564">Stratégie utilisée par le cache pour gérer les demandes de lecture.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-564">Policy employed by the cache for handling read requests.</span></span> <span data-ttu-id="f7a2d-565">Si la stratégie de lecture est déterminée individuellement, c’est-à-dire, pour chaque demande, la valeur 6 (« détermination par e/s ») doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-565">If the read policy is determined individually, that is, for each request, then the value 6 ("Determination per I/O") should be specified.</span></span> <span data-ttu-id="f7a2d-566">« Other » et « Unknown » sont également des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-566">"Other" and "Unknown" are also valid values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7a2d-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-568">Autre.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-568">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-570">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-570">Unknown.</span></span>

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="f7a2d-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-572">Lecture.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-572">Read.</span></span>

</dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="f7a2d-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Lecture anticipée** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-574">Lecture anticipée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-574">Read-ahead.</span></span>

</dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="f7a2d-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Lecture et lecture anticipée** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Read and Read-Ahead** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-576">Lecture et lecture anticipée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-576">Read and read-ahead.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="f7a2d-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Détermination par e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-578">Détermination par e/s.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-578">Determination per I/O.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-579">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-579">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-580">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-580">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-581">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-582">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,12»)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-583">Énumération entière décrivant l’algorithme qui détermine les lignes de cache ou les compartiments qui doivent être réutilisés.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-583">Integer enumeration describing the algorithm that determines which cache lines or buckets should be re-used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7a2d-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-585">Autre.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-585">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-587">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-587">Unknown.</span></span>

</dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="f7a2d-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>Le **moins récemment utilisé (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-589">Le moins récemment utilisé (LRU).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-589">Least recently used (LRU).</span></span>

</dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="f7a2d-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**Premier entré, premier sorti (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**First In First Out (FIFO)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-591">Premier entré, premier sorti (FIFO).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-591">First-in, first-out (FIFO).</span></span>

</dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="f7a2d-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Dernier entré, premier sorti (LIFO)** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-593">Dernier entré, premier sorti (LIFO).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-593">Last-in, first-out (LIFO).</span></span>

</dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="f7a2d-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>Le **moins fréquemment utilisé (LFU)** (6)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-595">Le moins fréquemment utilisé (LFU.)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-595">Least frequently used (LFU.)</span></span>

</dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="f7a2d-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>Le **plus fréquemment utilisé (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-597">Le plus fréquemment utilisé (MFU).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-597">Most frequently used (MFU).</span></span>

</dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="f7a2d-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Algorithmes multiples dépendants des données** (8)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-599">Algorithmes multiples dépendant des données.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-599">Data-dependent multiple algorithms.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-600">**De la**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-600">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-601">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-601">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-602">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-603">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,3 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-603">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-604">Adresse de début, référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire, pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-604">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="f7a2d-605">L’adresse de départ est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-605">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="f7a2d-606">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-606">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f7a2d-607">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-607">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-608">**État**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-608">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-609">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-609">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-610">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-610">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-611">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-611">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-612">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-612">String that indicates the current status of the object.</span></span> <span data-ttu-id="f7a2d-613">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-613">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f7a2d-614">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="f7a2d-614">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f7a2d-615">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-615">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f7a2d-616">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="f7a2d-616">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f7a2d-617">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-617">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f7a2d-618">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-618">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f7a2d-619">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-619">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f7a2d-620">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7a2d-620">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f7a2d-621">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-621">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f7a2d-622">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-622">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f7a2d-623">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-623">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-624">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-624">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f7a2d-625">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-625">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f7a2d-626">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-626">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f7a2d-627">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-627">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f7a2d-628">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-628">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f7a2d-629">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-629">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f7a2d-630">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-630">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f7a2d-631">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-631">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f7a2d-632">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-632">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-633">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-633">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-634">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-634">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-635">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-636">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f7a2d-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-637">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-637">State of the logical device.</span></span> <span data-ttu-id="f7a2d-638">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-638">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="f7a2d-639">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7a2d-640">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-640">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-641">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-641">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f7a2d-642">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-642">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f7a2d-643">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-643">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f7a2d-644">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-644">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7a2d-645">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-645">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-646">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-647">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-648">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-648">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-649">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-649">The scoping system's creation class name.</span></span>

<span data-ttu-id="f7a2d-650">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-650">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-651">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-651">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-652">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-652">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-653">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-653">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-654">Indique si les informations d’adresse dans la propriété **ErrorAddress** sont une adresse de niveau système (**true**) ou une adresse physique (**false**).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-654">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="f7a2d-655">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-655">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f7a2d-656">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-656">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-657">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-657">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-658">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-659">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-659">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-660">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-660">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-661">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-661">The scoping system's name.</span></span>

<span data-ttu-id="f7a2d-662">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-662">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a2d-663">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-663">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a2d-664">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-664">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-665">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7a2d-665">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a2d-666">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,5»)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-666">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="f7a2d-667">Définit si le cache est en écriture différée ou en écriture différée, ou si les informations « varient avec l’adresse » ou sont définies individuellement pour chaque entrée/sortie.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-667">Defines whether the cache is write-back or write-through, or whether the information "Varies with Address" or is defined individually for each input/output.</span></span> <span data-ttu-id="f7a2d-668">« Other » et « Unknown » peuvent également être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-668">"Other" and "Unknown" also can be specified.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7a2d-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-670">Autre.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-670">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7a2d-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-672">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-672">Unknown.</span></span>

</dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="f7a2d-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Écriture différée** (3)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Write Back** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-674">Écriture différée.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-674">Write back.</span></span>

</dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="f7a2d-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Écriture par écrit** (4)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Write Through** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-676">Écrire.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-676">Write through.</span></span>

</dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="f7a2d-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varie en fonction de l’adresse** (5)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varies with Address** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-678">Varie en fonction de l’adresse.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-678">Varies with address.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="f7a2d-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Détermination par e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="f7a2d-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f7a2d-680">Détermination par e/s.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-680">Determination per I/O.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7a2d-681">Notes</span><span class="sxs-lookup"><span data-stu-id="f7a2d-681">Remarks</span></span>

<span data-ttu-id="f7a2d-682">La classe **CIM \_ CacheMemory** est dérivée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-682">The **CIM\_CacheMemory** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="f7a2d-683">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-683">WMI does not implement this class.</span></span> <span data-ttu-id="f7a2d-684">Pour plus d’informations sur les classes dérivées de **CIM \_ CacheMemory**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f7a2d-684">For more information about classes derived from **CIM\_CacheMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f7a2d-685">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-685">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f7a2d-686">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="f7a2d-686">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7a2d-687">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7a2d-687">Requirements</span></span>



| <span data-ttu-id="f7a2d-688">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7a2d-688">Requirement</span></span> | <span data-ttu-id="f7a2d-689">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7a2d-689">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a2d-690">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7a2d-690">Minimum supported client</span></span><br/> | <span data-ttu-id="f7a2d-691">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7a2d-691">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7a2d-692">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7a2d-692">Minimum supported server</span></span><br/> | <span data-ttu-id="f7a2d-693">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7a2d-693">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7a2d-694">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f7a2d-694">Namespace</span></span><br/>                | <span data-ttu-id="f7a2d-695">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f7a2d-695">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f7a2d-696">MOF</span><span class="sxs-lookup"><span data-stu-id="f7a2d-696">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7a2d-697"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7a2d-697"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7a2d-698">DLL</span><span class="sxs-lookup"><span data-stu-id="f7a2d-698">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7a2d-699"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7a2d-699"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7a2d-700">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7a2d-700">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a2d-701">**\_Mémoire CIM**</span><span class="sxs-lookup"><span data-stu-id="f7a2d-701">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

