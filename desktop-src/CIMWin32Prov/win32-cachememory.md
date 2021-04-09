---
description: Le \_ CacheMemory Win32&\# 32 ; La classe WMI représente la mémoire cache interne et externe sur un système informatique.
ms.assetid: 9cfb992d-fbac-4e56-b4f3-61c0c93f5852
ms.tgt_platform: multiple
title: Win32_CacheMemory, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CacheMemory
- Win32_CacheMemory.Reset
- Win32_CacheMemory.SetPowerState
- Win32_CacheMemory.Access
- Win32_CacheMemory.AdditionalErrorData
- Win32_CacheMemory.Associativity
- Win32_CacheMemory.Availability
- Win32_CacheMemory.BlockSize
- Win32_CacheMemory.CacheSpeed
- Win32_CacheMemory.CacheType
- Win32_CacheMemory.Caption
- Win32_CacheMemory.ConfigManagerErrorCode
- Win32_CacheMemory.ConfigManagerUserConfig
- Win32_CacheMemory.CorrectableError
- Win32_CacheMemory.CreationClassName
- Win32_CacheMemory.CurrentSRAM
- Win32_CacheMemory.Description
- Win32_CacheMemory.DeviceID
- Win32_CacheMemory.EndingAddress
- Win32_CacheMemory.ErrorAccess
- Win32_CacheMemory.ErrorAddress
- Win32_CacheMemory.ErrorCleared
- Win32_CacheMemory.ErrorCorrectType
- Win32_CacheMemory.ErrorData
- Win32_CacheMemory.ErrorDataOrder
- Win32_CacheMemory.ErrorDescription
- Win32_CacheMemory.ErrorInfo
- Win32_CacheMemory.ErrorMethodology
- Win32_CacheMemory.ErrorResolution
- Win32_CacheMemory.ErrorTime
- Win32_CacheMemory.ErrorTransferSize
- Win32_CacheMemory.FlushTimer
- Win32_CacheMemory.InstallDate
- Win32_CacheMemory.InstalledSize
- Win32_CacheMemory.LastErrorCode
- Win32_CacheMemory.Level
- Win32_CacheMemory.LineSize
- Win32_CacheMemory.Location
- Win32_CacheMemory.MaxCacheSize
- Win32_CacheMemory.Name
- Win32_CacheMemory.NumberOfBlocks
- Win32_CacheMemory.OtherErrorDescription
- Win32_CacheMemory.PNPDeviceID
- Win32_CacheMemory.PowerManagementCapabilities
- Win32_CacheMemory.PowerManagementSupported
- Win32_CacheMemory.Purpose
- Win32_CacheMemory.ReadPolicy
- Win32_CacheMemory.ReplacementPolicy
- Win32_CacheMemory.StartingAddress
- Win32_CacheMemory.Status
- Win32_CacheMemory.StatusInfo
- Win32_CacheMemory.SupportedSRAM
- Win32_CacheMemory.SystemCreationClassName
- Win32_CacheMemory.SystemLevelAddress
- Win32_CacheMemory.SystemName
- Win32_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83a8fefbe1104f24f208d232b8f6bc134efefd83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861521"
---
# <a name="win32_cachememory-class"></a><span data-ttu-id="d73f0-103">\_Classe CacheMemory Win32</span><span class="sxs-lookup"><span data-stu-id="d73f0-103">Win32\_CacheMemory class</span></span>

<span data-ttu-id="d73f0-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ CacheMemory** représente la mémoire cache interne et externe sur un système informatique.</span><span class="sxs-lookup"><span data-stu-id="d73f0-104">The **Win32\_CacheMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents internal and external cache memory on a computer system.</span></span>

<span data-ttu-id="d73f0-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d73f0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d73f0-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d73f0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d73f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d73f0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B97-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_CacheMemory : CIM_CacheMemory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Associativity;
  uint16   Availability;
  uint64   BlockSize;
  uint32   CacheSpeed;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  uint16   CurrentSRAM[];
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint16   ErrorCorrectType;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  uint32   FlushTimer;
  datetime InstallDate;
  uint32   InstalledSize;
  uint32   LastErrorCode;
  uint16   Level;
  uint32   LineSize;
  uint16   Location;
  uint32   MaxCacheSize;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  uint16   SupportedSRAM[];
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="d73f0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d73f0-108">Members</span></span>

<span data-ttu-id="d73f0-109">La classe **Win32 \_ CacheMemory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d73f0-109">The **Win32\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="d73f0-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d73f0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d73f0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d73f0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d73f0-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d73f0-112">Methods</span></span>

<span data-ttu-id="d73f0-113">La classe **Win32 \_ CacheMemory** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d73f0-113">The **Win32\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="d73f0-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="d73f0-114">Method</span></span>            | <span data-ttu-id="d73f0-115">Description</span><span class="sxs-lookup"><span data-stu-id="d73f0-115">Description</span></span>                                                                                                                                                                                                  |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d73f0-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="d73f0-116">**Reset**</span></span>         | <span data-ttu-id="d73f0-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="d73f0-117">Not implemented.</span></span> <span data-ttu-id="d73f0-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ CacheMemory**](cim-cachememory.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="d73f0-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="d73f0-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d73f0-119">**SetPowerState**</span></span> | <span data-ttu-id="d73f0-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="d73f0-120">Not implemented.</span></span> <span data-ttu-id="d73f0-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ CacheMemory**](cim-cachememory.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="d73f0-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d73f0-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d73f0-122">Properties</span></span>

<span data-ttu-id="d73f0-123">La classe **Win32 \_ CacheMemory** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d73f0-123">The **Win32\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d73f0-124">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="d73f0-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-127">Type d’accès.</span><span class="sxs-lookup"><span data-stu-id="d73f0-127">Type of access.</span></span>

<span data-ttu-id="d73f0-128">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d73f0-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="d73f0-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="d73f0-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-132">Accessible en écriture</span><span class="sxs-lookup"><span data-stu-id="d73f0-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="d73f0-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="d73f0-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="d73f0-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-136">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d73f0-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-138">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,18 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d73f0-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-139">Tableau d’octets qui contiennent des informations d’erreur supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d73f0-139">Array of octets that hold additional error information.</span></span> <span data-ttu-id="d73f0-140">Par exemple, le syndrome ECC ou le retour des bits de vérification si une méthodologie d’erreur basée sur CRC est utilisée.</span><span class="sxs-lookup"><span data-stu-id="d73f0-140">An example is ECC Syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="d73f0-141">Dans ce dernier cas, si une erreur de bit unique est reconnue et que l’algorithme CRC est connu, il est possible de déterminer le bit exact qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="d73f0-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="d73f0-142">Ce type de données (syndrome ECC, bit de vérification, données de bit de parité ou autres informations fournies par le fournisseur) est inclus dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="d73f0-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="d73f0-143">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="d73f0-143">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="d73f0-144">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-144">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-145">**Associativité**</span><span class="sxs-lookup"><span data-stu-id="d73f0-145">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-146">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,15»)</span><span class="sxs-lookup"><span data-stu-id="d73f0-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-149">Énumération entière qui définit l’associativité du cache système.</span><span class="sxs-lookup"><span data-stu-id="d73f0-149">An integer enumeration that defines the system cache associativity.</span></span>

<span data-ttu-id="d73f0-150">Cette valeur provient du membre **associativité** de la structure d' **informations du cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-150">This value comes from the **Associativity** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d73f0-151">Cette propriété est héritée de la [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-151">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-152">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-152">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-153">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-153">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="d73f0-154">**Mappé direct** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-154">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="d73f0-155">**Set-associatif** bidirectionnel (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-155">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="d73f0-156">**Set-associatif à 4 voies** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-156">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="d73f0-157">**Entièrement associatif** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-157">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="d73f0-158">**Set-associatif à 8 voies** (7)</span><span class="sxs-lookup"><span data-stu-id="d73f0-158">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="d73f0-159">**Set-associatif à 16 voies** (8)</span><span class="sxs-lookup"><span data-stu-id="d73f0-159">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-160">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="d73f0-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-161">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-163">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-164">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d73f0-164">Availability and status of the device.</span></span>

<span data-ttu-id="d73f0-165">Cette valeur provient du membre de **configuration du cache** de la structure d’informations du **cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-165">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d73f0-166">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-166">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d73f0-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-170">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="d73f0-170">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d73f0-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d73f0-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d73f0-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d73f0-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="d73f0-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d73f0-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="d73f0-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d73f0-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="d73f0-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d73f0-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="d73f0-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d73f0-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="d73f0-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d73f0-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="d73f0-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d73f0-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="d73f0-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-181">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d73f0-181">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d73f0-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="d73f0-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-183">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="d73f0-183">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d73f0-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="d73f0-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-185">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="d73f0-185">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d73f0-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="d73f0-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d73f0-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="d73f0-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-188">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="d73f0-188">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d73f0-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="d73f0-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-190">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="d73f0-190">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d73f0-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="d73f0-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-192">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="d73f0-192">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d73f0-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="d73f0-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-194">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="d73f0-194">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d73f0-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="d73f0-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-196">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="d73f0-196">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-197">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="d73f0-197">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-198">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d73f0-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-200">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-201">Taille en octets des blocs qui forment cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="d73f0-201">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="d73f0-202">S’il est inconnu ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1.</span><span class="sxs-lookup"><span data-stu-id="d73f0-202">If unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="d73f0-203">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-203">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="d73f0-204">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d73f0-204">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-205">**CacheSpeed**</span><span class="sxs-lookup"><span data-stu-id="d73f0-205">**CacheSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-206">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d73f0-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-208">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« SMBIOS \| type 7 \| cache Speed »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (nanosecondes)</span><span class="sxs-lookup"><span data-stu-id="d73f0-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Cache Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-209">Vitesse du cache.</span><span class="sxs-lookup"><span data-stu-id="d73f0-209">Speed of the cache.</span></span>

<span data-ttu-id="d73f0-210">Cette valeur provient du membre **Vitesse** du cache de la structure d' **informations du cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-210">This value comes from the **Cache Speed** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-211">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="d73f0-211">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-212">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-214">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,9»)</span><span class="sxs-lookup"><span data-stu-id="d73f0-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-215">Type de cache.</span><span class="sxs-lookup"><span data-stu-id="d73f0-215">Type of cache.</span></span>

<span data-ttu-id="d73f0-216">Cette valeur provient du membre de **type de cache système** de la structure d' **informations du cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-216">This value comes from the **System Cache Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d73f0-217">Cette propriété est héritée de la [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-217">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-218">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-218">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-219">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-219">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="d73f0-220">**Instruction** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-220">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="d73f0-221">**Données** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-221">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="d73f0-222">**Unifié** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-222">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-223">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d73f0-223">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-224">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-226">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-226">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-227">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="d73f0-227">Short description of the object a one-line string.</span></span>

<span data-ttu-id="d73f0-228">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-229">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d73f0-229">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-230">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d73f0-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-232">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d73f0-232">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-233">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="d73f0-233">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d73f0-234">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-234">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d73f0-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d73f0-236"> (0)</span><span class="sxs-lookup"><span data-stu-id="d73f0-236">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-237">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="d73f0-237">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d73f0-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d73f0-239">(1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-239">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-240">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="d73f0-240">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d73f0-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d73f0-242">(2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-242">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d73f0-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d73f0-244">(3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-244">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-245">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="d73f0-245">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d73f0-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d73f0-247">(4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-247">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-248">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="d73f0-248">Device is not working properly.</span></span> <span data-ttu-id="d73f0-249">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="d73f0-249">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d73f0-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d73f0-251">(5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-251">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-252">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="d73f0-252">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d73f0-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d73f0-254"> (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-254">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-255">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="d73f0-255">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d73f0-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d73f0-257">(7)</span><span class="sxs-lookup"><span data-stu-id="d73f0-257">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d73f0-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d73f0-259">(8)</span><span class="sxs-lookup"><span data-stu-id="d73f0-259">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-260">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="d73f0-260">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d73f0-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d73f0-262">(9)</span><span class="sxs-lookup"><span data-stu-id="d73f0-262">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-263">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="d73f0-263">Device is not working properly.</span></span> <span data-ttu-id="d73f0-264">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d73f0-264">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d73f0-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d73f0-266">(10)</span><span class="sxs-lookup"><span data-stu-id="d73f0-266">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-267">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d73f0-267">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d73f0-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d73f0-269">(11)</span><span class="sxs-lookup"><span data-stu-id="d73f0-269">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-270">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d73f0-270">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d73f0-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d73f0-272">douze</span><span class="sxs-lookup"><span data-stu-id="d73f0-272">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-273">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d73f0-273">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d73f0-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d73f0-275">(13)</span><span class="sxs-lookup"><span data-stu-id="d73f0-275">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-276">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d73f0-276">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d73f0-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d73f0-278">(14)</span><span class="sxs-lookup"><span data-stu-id="d73f0-278">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-279">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="d73f0-279">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d73f0-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d73f0-281">(15)</span><span class="sxs-lookup"><span data-stu-id="d73f0-281">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-282">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="d73f0-282">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d73f0-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d73f0-284">(16)</span><span class="sxs-lookup"><span data-stu-id="d73f0-284">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-285">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d73f0-285">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d73f0-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d73f0-287">(17)</span><span class="sxs-lookup"><span data-stu-id="d73f0-287">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-288">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="d73f0-288">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d73f0-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d73f0-290">(18)</span><span class="sxs-lookup"><span data-stu-id="d73f0-290">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-291">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="d73f0-291">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d73f0-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d73f0-293">(19)</span><span class="sxs-lookup"><span data-stu-id="d73f0-293">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d73f0-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d73f0-295">(20)</span><span class="sxs-lookup"><span data-stu-id="d73f0-295">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-296">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="d73f0-296">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d73f0-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d73f0-298">(21)</span><span class="sxs-lookup"><span data-stu-id="d73f0-298">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-299">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="d73f0-299">System failure.</span></span> <span data-ttu-id="d73f0-300">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="d73f0-300">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d73f0-301">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d73f0-301">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d73f0-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d73f0-303">(22)</span><span class="sxs-lookup"><span data-stu-id="d73f0-303">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-304">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d73f0-304">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d73f0-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d73f0-306">(23)</span><span class="sxs-lookup"><span data-stu-id="d73f0-306">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-307">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="d73f0-307">System failure.</span></span> <span data-ttu-id="d73f0-308">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="d73f0-308">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d73f0-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d73f0-310">(24)</span><span class="sxs-lookup"><span data-stu-id="d73f0-310">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-311">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="d73f0-311">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d73f0-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d73f0-313">(25)</span><span class="sxs-lookup"><span data-stu-id="d73f0-313">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-314">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d73f0-314">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d73f0-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d73f0-316">(26)</span><span class="sxs-lookup"><span data-stu-id="d73f0-316">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-317">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d73f0-317">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d73f0-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d73f0-319">(27)</span><span class="sxs-lookup"><span data-stu-id="d73f0-319">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-320">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="d73f0-320">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d73f0-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d73f0-322">(28)</span><span class="sxs-lookup"><span data-stu-id="d73f0-322">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-323">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="d73f0-323">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d73f0-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d73f0-325">(29)</span><span class="sxs-lookup"><span data-stu-id="d73f0-325">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-326">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d73f0-326">Device is disabled.</span></span> <span data-ttu-id="d73f0-327">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="d73f0-327">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d73f0-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d73f0-329">(30)</span><span class="sxs-lookup"><span data-stu-id="d73f0-329">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-330">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="d73f0-330">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d73f0-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d73f0-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d73f0-332">31</span><span class="sxs-lookup"><span data-stu-id="d73f0-332">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-333">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="d73f0-333">Device is not working properly.</span></span> <span data-ttu-id="d73f0-334">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="d73f0-334">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-335">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d73f0-335">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-336">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d73f0-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-338">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d73f0-338">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-339">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d73f0-339">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d73f0-340">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-341">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="d73f0-341">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-342">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d73f0-342">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-344">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-345">Si la **valeur est true**, l’erreur la plus récente était correcte.</span><span class="sxs-lookup"><span data-stu-id="d73f0-345">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="d73f0-346">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="d73f0-346">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="d73f0-347">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-347">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-348">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d73f0-348">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-351">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d73f0-351">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-352">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d73f0-352">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d73f0-353">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="d73f0-353">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d73f0-354">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-355">**CurrentSRAM**</span><span class="sxs-lookup"><span data-stu-id="d73f0-355">**CurrentSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-356">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-356">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-358">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 7 \| Current SRAM type")</span><span class="sxs-lookup"><span data-stu-id="d73f0-358">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Current SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-359">Tableau de types de mémoire vive (SRAM) statique utilisé pour la mémoire cache.</span><span class="sxs-lookup"><span data-stu-id="d73f0-359">Array of types of Static Random Access Memory (SRAM) being used for the cache memory.</span></span>

<span data-ttu-id="d73f0-360">Cette valeur provient du membre de **type SRAM actuel** de la structure d' **informations du cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-360">This value comes from the **Current SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-361">**Autre** (0)</span><span class="sxs-lookup"><span data-stu-id="d73f0-361">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-362">**Inconnu** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-362">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="d73f0-363">**Non rafale** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-363">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="d73f0-364">**Rafale** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-364">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="d73f0-365">**Rafale de pipeline** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-365">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="d73f0-366">**Synchrone** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-366">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="d73f0-367">**Asynchrone** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-367">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-368">**Description**</span><span class="sxs-lookup"><span data-stu-id="d73f0-368">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-369">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-371">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d73f0-371">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-372">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d73f0-372">Description of the object.</span></span>

<span data-ttu-id="d73f0-373">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-374">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d73f0-374">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-375">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-377">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« DeviceID »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-377">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-378">Identificateur unique du cache représenté par une instance de **Win32 \_ CacheMemory**.</span><span class="sxs-lookup"><span data-stu-id="d73f0-378">Unique identifier of the cache represented by an instance of **Win32\_CacheMemory**.</span></span>

<span data-ttu-id="d73f0-379">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d73f0-380">Exemple : « cache Memory 1 »</span><span class="sxs-lookup"><span data-stu-id="d73f0-380">Example: "Cache Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-381">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="d73f0-381">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-382">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d73f0-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-384">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,4 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-385">Adresse de fin, référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire, pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="d73f0-385">Ending address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="d73f0-386">L’adresse de fin est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="d73f0-386">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="d73f0-387">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-387">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="d73f0-388">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d73f0-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-389">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="d73f0-389">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-390">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-392">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,15 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-393">Opération d’accès à la mémoire qui a provoqué la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="d73f0-393">Memory access operation that caused the last error.</span></span> <span data-ttu-id="d73f0-394">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="d73f0-394">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="d73f0-395">Si **errorInfo** est égal à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="d73f0-395">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="d73f0-396">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-396">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-397">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-398">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="d73f0-399">**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-399">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="d73f0-400">**Écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-400">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="d73f0-401">**Écriture partielle** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-401">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-402">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="d73f0-402">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-403">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d73f0-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-405">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,19 "," MIF. \|Périphérique de mémoire DMTF \| 002,20 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-406">Adresse de la dernière erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d73f0-406">Address of the last memory error.</span></span> <span data-ttu-id="d73f0-407">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="d73f0-407">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="d73f0-408">Si **errorInfo** est égal à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="d73f0-408">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="d73f0-409">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-409">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="d73f0-410">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d73f0-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-411">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d73f0-411">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-412">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d73f0-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-414">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="d73f0-414">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="d73f0-415">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-416">**ErrorCorrectType**</span><span class="sxs-lookup"><span data-stu-id="d73f0-416">**ErrorCorrectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-417">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-419">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| type de correction d’erreur de type SMBIOS 7 \| »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Error Correction Type")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-420">Méthode de correction d’erreur utilisée par la mémoire cache.</span><span class="sxs-lookup"><span data-stu-id="d73f0-420">Error correction method used by the cache memory.</span></span>

<span data-ttu-id="d73f0-421">Cette valeur provient du membre de **type de correction d’erreur** de la structure d’informations du **cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-421">This value comes from the **Error Correction Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d73f0-422">**Réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="d73f0-422">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-423">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-423">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-424">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-424">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="d73f0-425">**Aucun** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-425">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="d73f0-426">**Parité** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-426">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="d73f0-427">**ECC sur un bit** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-427">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="d73f0-428">**ECC multi-bits** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-428">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-429">**Partagefichiers**</span><span class="sxs-lookup"><span data-stu-id="d73f0-429">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-430">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d73f0-430">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-432">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,17 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d73f0-432">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-433">Tableau de données capturées au cours du dernier accès mémoire erroné.</span><span class="sxs-lookup"><span data-stu-id="d73f0-433">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="d73f0-434">Les données occupent les *n* premiers octets du tableau nécessaire pour contenir le nombre de bits spécifié par la propriété **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="d73f0-434">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="d73f0-435">Si **ErrorTransferSize** est égal à 0 (zéro), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="d73f0-435">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="d73f0-436">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-436">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-437">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="d73f0-437">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-438">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-439">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-440">Classement des données stockées dans la propriété **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="d73f0-440">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="d73f0-441">Si **ErrorTransferSize** est égal à 0 (zéro), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="d73f0-441">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="d73f0-442">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-443">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d73f0-443">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="d73f0-444">**Octet le moins significatif en premier** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-444">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="d73f0-445">**Octet le plus significatif en premier** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-445">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-446">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d73f0-446">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-447">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-448">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-449">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="d73f0-449">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="d73f0-450">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-451">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="d73f0-451">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-452">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-454">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ mémoire CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="d73f0-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-455">Type d’erreur qui s’est produite le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="d73f0-455">Type of error that occurred most recently.</span></span> <span data-ttu-id="d73f0-456">Les valeurs 12-14 ne sont pas définies dans le schéma CIM car, dans DMI, elles combinent la sémantique du type d’erreur et si elles sont correctes ou non.</span><span class="sxs-lookup"><span data-stu-id="d73f0-456">The values 12-14 are undefined in the CIM schema because in DMI they mix the semantics of the type of error and whether it was correctable or not.</span></span> <span data-ttu-id="d73f0-457">Ce dernier est indiqué dans la propriété **CorrectableError**.</span><span class="sxs-lookup"><span data-stu-id="d73f0-457">The latter is indicated in the property **CorrectableError**.</span></span>

<span data-ttu-id="d73f0-458">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-459">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-460">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-460">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d73f0-461">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-461">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="d73f0-462">**Lecture incorrecte** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-462">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="d73f0-463">**Erreur de parité** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-463">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="d73f0-464">**Erreur de bit unique** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-464">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="d73f0-465">**Erreur double bit** (7)</span><span class="sxs-lookup"><span data-stu-id="d73f0-465">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="d73f0-466">**Erreur multibits** (8)</span><span class="sxs-lookup"><span data-stu-id="d73f0-466">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="d73f0-467">**Erreur de grignotage** (9)</span><span class="sxs-lookup"><span data-stu-id="d73f0-467">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="d73f0-468">**Erreur de somme de contrôle** (10)</span><span class="sxs-lookup"><span data-stu-id="d73f0-468">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="d73f0-469">**Erreur CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="d73f0-469">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="d73f0-470">**Non défini** (12)</span><span class="sxs-lookup"><span data-stu-id="d73f0-470">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="d73f0-471">**Non défini** (13)</span><span class="sxs-lookup"><span data-stu-id="d73f0-471">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="d73f0-472">**Non défini** (14)</span><span class="sxs-lookup"><span data-stu-id="d73f0-472">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-473">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="d73f0-473">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-474">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-476">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-476">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-477">Détails sur la parité ou les algorithmes CRC, ECC ou autres mécanismes utilisés.</span><span class="sxs-lookup"><span data-stu-id="d73f0-477">Details on the parity or CRC algorithms, ECC, or other mechanisms used.</span></span>

<span data-ttu-id="d73f0-478">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-478">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-479">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="d73f0-479">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-480">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d73f0-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-481">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-482">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,21 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-483">Plage, en octets, à laquelle la dernière erreur peut être résolue.</span><span class="sxs-lookup"><span data-stu-id="d73f0-483">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="d73f0-484">Par exemple, si les adresses d’erreurs sont résolues en bit 11 (c’est-à-dire, sur une base de page standard), les erreurs peuvent être résolues en limites de 4 Ko et cette propriété est définie sur 4000.</span><span class="sxs-lookup"><span data-stu-id="d73f0-484">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="d73f0-485">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="d73f0-485">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="d73f0-486">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-486">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="d73f0-487">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d73f0-487">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-488">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="d73f0-488">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-489">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d73f0-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-490">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-491">Heure à laquelle la dernière erreur de mémoire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d73f0-491">Time that the last memory error occurred.</span></span> <span data-ttu-id="d73f0-492">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="d73f0-492">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="d73f0-493">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="d73f0-493">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="d73f0-494">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-494">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-495">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="d73f0-495">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-496">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d73f0-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-497">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-498">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,16 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-499">Taille du transfert de données en bits qui a provoqué la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="d73f0-499">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="d73f0-500">0 (zéro) indique qu’il n’y a pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d73f0-500">0 (zero) indicates no error.</span></span> <span data-ttu-id="d73f0-501">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d73f0-501">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="d73f0-502">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-502">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-503">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="d73f0-503">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-504">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d73f0-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-505">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-506">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,14 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" secondes ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-506">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-507">Durée maximale, en secondes, pendant laquelle les lignes modifiées ou les compartiments peuvent demeurer dans le cache avant d’être vidés.</span><span class="sxs-lookup"><span data-stu-id="d73f0-507">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="d73f0-508">La valeur 0 (zéro) indique qu’un vidage du cache n’est pas contrôlé par un minuteur de vidage.</span><span class="sxs-lookup"><span data-stu-id="d73f0-508">A value of 0 (zero) indicates that a cache flush is not controlled by a flushing timer.</span></span>

<span data-ttu-id="d73f0-509">Cette propriété est héritée de la [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-509">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d73f0-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-511">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d73f0-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-512">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-513">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-513">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-514">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d73f0-514">Date and time the object was installed.</span></span> <span data-ttu-id="d73f0-515">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="d73f0-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d73f0-516">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-517">**InstalledSize**</span><span class="sxs-lookup"><span data-stu-id="d73f0-517">**InstalledSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-518">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d73f0-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-520">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« SMBIOS \| type 7 \| Taille installée »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-520">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Installed Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-521">Taille actuelle de la mémoire cache installée.</span><span class="sxs-lookup"><span data-stu-id="d73f0-521">Current size of the installed cache memory.</span></span>

<span data-ttu-id="d73f0-522">Cette valeur provient du membre de la **Taille installée** de la structure d' **informations du cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-522">This value comes from the **Installed Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-523">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d73f0-523">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-524">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d73f0-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-525">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-526">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d73f0-526">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d73f0-527">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-528">**Niveau**</span><span class="sxs-lookup"><span data-stu-id="d73f0-528">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-529">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-529">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-530">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-531">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,2»)</span><span class="sxs-lookup"><span data-stu-id="d73f0-531">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-532">Niveau du cache.</span><span class="sxs-lookup"><span data-stu-id="d73f0-532">Level of the cache.</span></span>

<span data-ttu-id="d73f0-533">Cette valeur provient du membre de **configuration du cache** de la structure d’informations du **cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-533">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d73f0-534">Cette propriété est héritée de la [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-534">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="d73f0-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Principal** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="d73f0-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondaire** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="d73f0-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiaire** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d73f0-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-541">**Ligner**</span><span class="sxs-lookup"><span data-stu-id="d73f0-541">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-542">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d73f0-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-543">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-544">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,10 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-545">Taille, en octets, d’un compartiment ou d’une ligne de cache unique.</span><span class="sxs-lookup"><span data-stu-id="d73f0-545">Size, in bytes, of a single cache bucket or line.</span></span>

<span data-ttu-id="d73f0-546">Cette propriété est héritée de la [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-546">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-547">**Lieu**</span><span class="sxs-lookup"><span data-stu-id="d73f0-547">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-548">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-548">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-549">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-550">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 7 \| location")</span><span class="sxs-lookup"><span data-stu-id="d73f0-550">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-551">Emplacement physique de la mémoire cache.</span><span class="sxs-lookup"><span data-stu-id="d73f0-551">Physical location of the cache memory.</span></span>

<span data-ttu-id="d73f0-552">Cette valeur provient du membre de **configuration du cache** de la structure d’informations du **cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-552">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="d73f0-553">**Interne** (0)</span><span class="sxs-lookup"><span data-stu-id="d73f0-553">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="External"></span><span id="external"></span><span id="EXTERNAL"></span>

<span data-ttu-id="d73f0-554">**Externe** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-554">**External** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d73f0-555">**Réservé** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-555">**Reserved** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-556">**Inconnu** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-556">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-557">**MaxCacheSize**</span><span class="sxs-lookup"><span data-stu-id="d73f0-557">**MaxCacheSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-558">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d73f0-558">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-559">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-560">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 7 \| Max cache size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilo-octets")</span><span class="sxs-lookup"><span data-stu-id="d73f0-560">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Maximum Cache Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-561">Taille maximale du cache pouvant être installée sur cette mémoire cache particulière.</span><span class="sxs-lookup"><span data-stu-id="d73f0-561">Maximum cache size installable to this particular cache memory.</span></span>

<span data-ttu-id="d73f0-562">Cette valeur provient du membre de la **taille de cache maximale** de la structure d' **informations du cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-562">This value comes from the **Maximum Cache Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-563">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d73f0-563">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-564">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-564">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-565">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-565">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-566">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d73f0-566">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-567">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d73f0-567">Label by which the object is known.</span></span> <span data-ttu-id="d73f0-568">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="d73f0-568">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d73f0-569">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-569">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-570">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="d73f0-570">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-571">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d73f0-571">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-572">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-573">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-574">Nombre total de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forme cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="d73f0-574">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="d73f0-575">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d73f0-575">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="d73f0-576">Si la valeur de **BlockSize** est 1, cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="d73f0-576">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="d73f0-577">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-577">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="d73f0-578">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d73f0-578">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-579">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d73f0-579">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-580">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-581">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-582">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ mémoire CIM**](cim-memory.md).**ErrorInfo**»)</span><span class="sxs-lookup"><span data-stu-id="d73f0-582">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-583">Chaîne de forme libre fournissant plus d’informations si la propriété **ErrorType** a la valeur 1, other.</span><span class="sxs-lookup"><span data-stu-id="d73f0-583">Free-form string providing more information if the **ErrorType** property is set to 1, Other.</span></span> <span data-ttu-id="d73f0-584">Dans le cas contraire, cette chaîne n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="d73f0-584">Otherwise, this string has no meaning.</span></span>

<span data-ttu-id="d73f0-585">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-585">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-586">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d73f0-586">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-587">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-588">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-589">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d73f0-589">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-590">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d73f0-590">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d73f0-591">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d73f0-592">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="d73f0-592">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-593">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d73f0-593">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-594">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-594">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-595">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-595">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-596">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="d73f0-596">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d73f0-597">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="d73f0-597">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d73f0-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d73f0-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d73f0-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d73f0-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-602">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="d73f0-602">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d73f0-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-604">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="d73f0-604">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d73f0-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-606">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d73f0-606">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d73f0-607">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="d73f0-607">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d73f0-608">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d73f0-608">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d73f0-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-610">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="d73f0-610">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d73f0-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="d73f0-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d73f0-612">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="d73f0-612">Timed Power-On Supported</span></span>

<span data-ttu-id="d73f0-613">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="d73f0-613">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-614">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d73f0-614">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-615">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d73f0-615">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-616">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-616">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-617">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="d73f0-617">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="d73f0-618">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="d73f0-618">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="d73f0-619">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-619">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-620">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="d73f0-620">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-621">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-621">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-622">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-623">Chaîne de forme libre décrivant le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="d73f0-623">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="d73f0-624">Cette valeur provient du membre de **désignation de socket** de la structure d’informations du **cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-624">This value comes from the **Socket Designation** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d73f0-625">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-625">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-626">**Des**</span><span class="sxs-lookup"><span data-stu-id="d73f0-626">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-627">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-627">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-628">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-629">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,13»)</span><span class="sxs-lookup"><span data-stu-id="d73f0-629">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-630">Stratégie qui doit être utilisée par le cache pour gérer les demandes de lecture.</span><span class="sxs-lookup"><span data-stu-id="d73f0-630">Policy that shall be employed by the cache for handling read requests.</span></span>

<span data-ttu-id="d73f0-631">Cette propriété est héritée de la [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-631">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-632">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-632">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-633">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-633">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="d73f0-634">**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-634">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="d73f0-635">**Lecture anticipée** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-635">**Read-Ahead** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="d73f0-636">**Lecture et lecture anticipée** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-636">**Read and Read-Ahead** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="d73f0-637">**Détermination par e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-637">**Determination Per I/O** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-638">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="d73f0-638">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-639">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-639">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-640">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-640">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-641">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,12»)</span><span class="sxs-lookup"><span data-stu-id="d73f0-641">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-642">Algorithme permettant de déterminer les lignes ou les compartiments du cache qui doivent être réutilisés.</span><span class="sxs-lookup"><span data-stu-id="d73f0-642">Algorithm to determine which cache lines or buckets should be reused.</span></span>

<span data-ttu-id="d73f0-643">Cette propriété est héritée de la [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-643">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-644">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-644">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-645">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-645">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="d73f0-646">Le **moins récemment utilisé (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-646">**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="d73f0-647">**Premier entré, premier sorti (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-647">**First In First Out (FIFO)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="d73f0-648">**Dernier entré, premier sorti (LIFO)** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-648">**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="d73f0-649">Le **moins fréquemment utilisé (LFU)** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-649">**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="d73f0-650">Le **plus fréquemment utilisé (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="d73f0-650">**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="d73f0-651">**Algorithmes multiples dépendants des données** (8)</span><span class="sxs-lookup"><span data-stu-id="d73f0-651">**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-652">**De la**</span><span class="sxs-lookup"><span data-stu-id="d73f0-652">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-653">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d73f0-653">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-654">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-654">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-655">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,3 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-655">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-656">Adresse de début, référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire, pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="d73f0-656">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="d73f0-657">L’adresse de départ est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="d73f0-657">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="d73f0-658">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-658">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="d73f0-659">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d73f0-659">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-660">**État**</span><span class="sxs-lookup"><span data-stu-id="d73f0-660">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-661">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-662">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-663">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d73f0-663">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-664">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d73f0-664">Current status of the object.</span></span> <span data-ttu-id="d73f0-665">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="d73f0-665">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d73f0-666">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="d73f0-666">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d73f0-667">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="d73f0-667">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d73f0-668">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="d73f0-668">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d73f0-669">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="d73f0-669">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d73f0-670">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-670">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d73f0-671">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d73f0-671">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d73f0-672">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-672">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d73f0-673">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-673">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d73f0-674">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-674">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-675">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d73f0-675">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d73f0-676">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-676">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d73f0-677">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-677">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d73f0-678">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-678">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d73f0-679">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-679">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d73f0-680">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-680">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d73f0-681">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-681">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d73f0-682">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-682">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d73f0-683">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d73f0-683">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-684">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d73f0-684">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-685">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-685">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-686">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-687">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d73f0-687">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-688">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d73f0-688">State of the logical device.</span></span> <span data-ttu-id="d73f0-689">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d73f0-689">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d73f0-690">Cette valeur provient du membre de **configuration du cache** de la structure d’informations du **cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-690">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d73f0-691">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-691">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-692">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-692">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-693">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-693">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d73f0-694">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-694">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d73f0-695">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-695">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d73f0-696">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-696">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-697">**SupportedSRAM**</span><span class="sxs-lookup"><span data-stu-id="d73f0-697">**SupportedSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-698">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-698">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-699">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-700">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 7 \| prenait en charge le type SRAM")</span><span class="sxs-lookup"><span data-stu-id="d73f0-700">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Supported SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-701">Tableau de types pris en charge de mémoire vive statique (SRAM) qui peuvent être utilisés pour la mémoire cache.</span><span class="sxs-lookup"><span data-stu-id="d73f0-701">Array of supported types of Static Random Access Memory (SRAM) that can be used for the cache memory.</span></span>

<span data-ttu-id="d73f0-702">Cette valeur provient du membre de **type SRAM pris en charge** de la structure d' **informations du cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-702">This value comes from the **Supported SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-703">**Autre** (0)</span><span class="sxs-lookup"><span data-stu-id="d73f0-703">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-704">**Inconnu** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-704">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="d73f0-705">**Non rafale** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-705">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="d73f0-706">**Rafale** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-706">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="d73f0-707">**Rafale de pipeline** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-707">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="d73f0-708">**Synchrone** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-708">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="d73f0-709">**Asynchrone** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-709">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d73f0-710">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d73f0-710">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-711">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-711">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-712">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-713">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d73f0-713">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-714">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d73f0-714">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="d73f0-715">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-715">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-716">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="d73f0-716">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-717">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d73f0-717">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-718">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-718">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-719">Si la **valeur est true**, les informations d’adresse dans la propriété **ErrorAddress** sont une adresse de niveau système.</span><span class="sxs-lookup"><span data-stu-id="d73f0-719">If **True**, the address information in the property **ErrorAddress** is a system-level address.</span></span> <span data-ttu-id="d73f0-720">Si la **valeur est false**, il s’agit d’une adresse physique.</span><span class="sxs-lookup"><span data-stu-id="d73f0-720">If **False**, it is a physical address.</span></span> <span data-ttu-id="d73f0-721">Si la propriété **errorInfo** est égale à 3, cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="d73f0-721">If the **ErrorInfo** property is equal to 3, then this property has no meaning.</span></span>

<span data-ttu-id="d73f0-722">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-722">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-723">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d73f0-723">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-724">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d73f0-724">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-725">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-726">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d73f0-726">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-727">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d73f0-727">Name of the scoping system.</span></span>

<span data-ttu-id="d73f0-728">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-728">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73f0-729">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="d73f0-729">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d73f0-730">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d73f0-730">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-731">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d73f0-731">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d73f0-732">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache système DMTF \| 003,5»)</span><span class="sxs-lookup"><span data-stu-id="d73f0-732">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="d73f0-733">Écrire une définition de stratégie.</span><span class="sxs-lookup"><span data-stu-id="d73f0-733">Write policy definition.</span></span>

<span data-ttu-id="d73f0-734">Cette valeur provient du membre de **configuration du cache** de la structure d’informations du **cache** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d73f0-734">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d73f0-735">Cette propriété est héritée de la [**\_ CacheMemory CIM**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-735">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d73f0-736">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d73f0-736">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d73f0-737">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d73f0-737">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="d73f0-738">**Écriture différée** (3)</span><span class="sxs-lookup"><span data-stu-id="d73f0-738">**Write Back** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="d73f0-739">**Écriture par écrit** (4)</span><span class="sxs-lookup"><span data-stu-id="d73f0-739">**Write Through** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="d73f0-740">**Varie en fonction de l’adresse** (5)</span><span class="sxs-lookup"><span data-stu-id="d73f0-740">**Varies with Address** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="d73f0-741">**Détermination par e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="d73f0-741">**Determination Per I/O** (6)</span></span>


<span data-ttu-id="d73f0-742"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d73f0-742"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d73f0-743">Notes</span><span class="sxs-lookup"><span data-stu-id="d73f0-743">Remarks</span></span>

<span data-ttu-id="d73f0-744">La classe **Win32 \_ CacheMemory** est dérivée de [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="d73f0-744">The **Win32\_CacheMemory** class is derived from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d73f0-745">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d73f0-745">Requirements</span></span>



| <span data-ttu-id="d73f0-746">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d73f0-746">Requirement</span></span> | <span data-ttu-id="d73f0-747">Valeur</span><span class="sxs-lookup"><span data-stu-id="d73f0-747">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d73f0-748">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d73f0-748">Minimum supported client</span></span><br/> | <span data-ttu-id="d73f0-749">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d73f0-749">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d73f0-750">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d73f0-750">Minimum supported server</span></span><br/> | <span data-ttu-id="d73f0-751">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d73f0-751">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d73f0-752">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d73f0-752">Namespace</span></span><br/>                | <span data-ttu-id="d73f0-753">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d73f0-753">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d73f0-754">MOF</span><span class="sxs-lookup"><span data-stu-id="d73f0-754">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d73f0-755"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d73f0-755"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d73f0-756">DLL</span><span class="sxs-lookup"><span data-stu-id="d73f0-756">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d73f0-757"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d73f0-757"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d73f0-758">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d73f0-758">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73f0-759">**\_CACHEMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="d73f0-759">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dt>

[<span data-ttu-id="d73f0-760">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="d73f0-760">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

