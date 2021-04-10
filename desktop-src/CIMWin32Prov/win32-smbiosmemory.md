---
description: La \_ classe WMI SMBIOSMemory abstraite Win32 représente les propriétés d’une mémoire système de l’ordinateur, comme indiqué par l’interface SMBIOS (System Management BIOS).
ms.assetid: 2f609fc6-f0f5-45a5-9f9a-3873da034d49
ms.tgt_platform: multiple
title: Classe Win32_SMBIOSMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SMBIOSMemory
- Win32_SMBIOSMemory.Reset
- Win32_SMBIOSMemory.SetPowerState
- Win32_SMBIOSMemory.Access
- Win32_SMBIOSMemory.AdditionalErrorData
- Win32_SMBIOSMemory.Availability
- Win32_SMBIOSMemory.BlockSize
- Win32_SMBIOSMemory.Caption
- Win32_SMBIOSMemory.ConfigManagerErrorCode
- Win32_SMBIOSMemory.ConfigManagerUserConfig
- Win32_SMBIOSMemory.CorrectableError
- Win32_SMBIOSMemory.CreationClassName
- Win32_SMBIOSMemory.Description
- Win32_SMBIOSMemory.DeviceID
- Win32_SMBIOSMemory.EndingAddress
- Win32_SMBIOSMemory.ErrorAccess
- Win32_SMBIOSMemory.ErrorAddress
- Win32_SMBIOSMemory.ErrorCleared
- Win32_SMBIOSMemory.ErrorData
- Win32_SMBIOSMemory.ErrorDataOrder
- Win32_SMBIOSMemory.ErrorDescription
- Win32_SMBIOSMemory.ErrorInfo
- Win32_SMBIOSMemory.ErrorMethodology
- Win32_SMBIOSMemory.ErrorResolution
- Win32_SMBIOSMemory.ErrorTime
- Win32_SMBIOSMemory.ErrorTransferSize
- Win32_SMBIOSMemory.InstallDate
- Win32_SMBIOSMemory.LastErrorCode
- Win32_SMBIOSMemory.Name
- Win32_SMBIOSMemory.NumberOfBlocks
- Win32_SMBIOSMemory.OtherErrorDescription
- Win32_SMBIOSMemory.PNPDeviceID
- Win32_SMBIOSMemory.PowerManagementCapabilities
- Win32_SMBIOSMemory.PowerManagementSupported
- Win32_SMBIOSMemory.Purpose
- Win32_SMBIOSMemory.StartingAddress
- Win32_SMBIOSMemory.Status
- Win32_SMBIOSMemory.StatusInfo
- Win32_SMBIOSMemory.SystemCreationClassName
- Win32_SMBIOSMemory.SystemLevelAddress
- Win32_SMBIOSMemory.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4dc7a42732dfb00d965f79045254878f690309fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111338"
---
# <a name="win32_smbiosmemory-class"></a><span data-ttu-id="88cfd-103">\_Classe SMBIOSMemory Win32</span><span class="sxs-lookup"><span data-stu-id="88cfd-103">Win32\_SMBIOSMemory class</span></span>

<span data-ttu-id="88cfd-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SMBIOSMemory** abstraite Win32 représente les propriétés d’une mémoire système de l’ordinateur, comme indiqué par l’interface SMBIOS (System Management BIOS).</span><span class="sxs-lookup"><span data-stu-id="88cfd-104">The **Win32\_SMBIOSMemory** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a computer system memory as seen through the system management BIOS (SMBIOS) interface.</span></span> <span data-ttu-id="88cfd-105">L’interface SMBIOS ne fait pas la distinction entre les mémoires rémanentes, volatiles et Flash.</span><span class="sxs-lookup"><span data-stu-id="88cfd-105">The SMBIOS interface does not distinguish between nonvolatile, volatile, and flash memories.</span></span> <span data-ttu-id="88cfd-106">La classe de [**\_ mémoire CIM**](cim-memory.md) est la classe parente de tous les types de mémoire.</span><span class="sxs-lookup"><span data-stu-id="88cfd-106">The [**CIM\_Memory**](cim-memory.md) class is the parent class of all types of memory.</span></span>

<span data-ttu-id="88cfd-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="88cfd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="88cfd-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="88cfd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="88cfd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88cfd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FECB095B-F0FA-11d2-8617-0000F8102E5F}"), AMENDMENT]
class Win32_SMBIOSMemory : CIM_StorageExtent
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   StartingAddress;
  string   Status;
  uint16e  StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="88cfd-110">Membres</span><span class="sxs-lookup"><span data-stu-id="88cfd-110">Members</span></span>

<span data-ttu-id="88cfd-111">La classe **Win32 \_ SMBIOSMemory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="88cfd-111">The **Win32\_SMBIOSMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="88cfd-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="88cfd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="88cfd-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="88cfd-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="88cfd-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="88cfd-114">Methods</span></span>

<span data-ttu-id="88cfd-115">La classe **Win32 \_ SMBIOSMemory** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="88cfd-115">The **Win32\_SMBIOSMemory** class has these methods.</span></span>



| <span data-ttu-id="88cfd-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="88cfd-116">Method</span></span>            | <span data-ttu-id="88cfd-117">Description</span><span class="sxs-lookup"><span data-stu-id="88cfd-117">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88cfd-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="88cfd-118">**Reset**</span></span>         | <span data-ttu-id="88cfd-119">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="88cfd-119">Not implemented.</span></span> <span data-ttu-id="88cfd-120">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/>                 |
| <span data-ttu-id="88cfd-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="88cfd-121">**SetPowerState**</span></span> | <span data-ttu-id="88cfd-122">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="88cfd-122">Not implemented.</span></span> <span data-ttu-id="88cfd-123">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="88cfd-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="88cfd-124">Properties</span></span>

<span data-ttu-id="88cfd-125">La classe **Win32 \_ SMBIOSMemory** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="88cfd-125">The **Win32\_SMBIOSMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88cfd-126">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="88cfd-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88cfd-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-129">Type d’accès.</span><span class="sxs-lookup"><span data-stu-id="88cfd-129">Type of access.</span></span>

<span data-ttu-id="88cfd-130">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88cfd-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="88cfd-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="88cfd-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="88cfd-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="88cfd-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="88cfd-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-134">Accessible en écriture</span><span class="sxs-lookup"><span data-stu-id="88cfd-134">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="88cfd-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="88cfd-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="88cfd-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="88cfd-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88cfd-137">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="88cfd-137">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-138">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="88cfd-138">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-140">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 18 \| 32-bit Memory information Error \| syndrome"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="88cfd-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-141">Tableau d’octets qui contiennent des informations d’erreur supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="88cfd-141">Array of octets that hold additional error information.</span></span> <span data-ttu-id="88cfd-142">Par exemple, le syndrome de la vérification et de la correction des erreurs (ECC), ou le retour des bits de vérification si une méthodologie d’erreur basée sur CRC est utilisée.</span><span class="sxs-lookup"><span data-stu-id="88cfd-142">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="88cfd-143">Dans ce dernier cas, si une erreur de bit unique est reconnue et que l’algorithme de vérification de redondance cyclique (CRC) est connu, il est possible de déterminer le bit exact qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="88cfd-143">In the latter case, if a single bit error is recognized and the cyclical redundancy check (CRC) algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="88cfd-144">Ce type de données (syndrome ECC, donnée bit de vérification ou bit de parité, ou autres informations fournies par le fournisseur) est inclus dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="88cfd-144">This type of data (ECC Syndrome, Check Bit or Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="88cfd-145">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="88cfd-145">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-146">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="88cfd-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-147">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88cfd-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-149">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="88cfd-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-150">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88cfd-150">Availability and status of the device.</span></span>

<span data-ttu-id="88cfd-151">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88cfd-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="88cfd-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88cfd-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="88cfd-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="88cfd-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="88cfd-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-155">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="88cfd-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="88cfd-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="88cfd-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="88cfd-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="88cfd-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="88cfd-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="88cfd-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="88cfd-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="88cfd-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="88cfd-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="88cfd-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="88cfd-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="88cfd-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="88cfd-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="88cfd-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="88cfd-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="88cfd-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="88cfd-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="88cfd-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="88cfd-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="88cfd-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-166">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="88cfd-166">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="88cfd-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="88cfd-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-168">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="88cfd-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="88cfd-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="88cfd-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-170">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="88cfd-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="88cfd-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="88cfd-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="88cfd-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="88cfd-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-173">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="88cfd-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="88cfd-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="88cfd-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-175">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="88cfd-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="88cfd-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="88cfd-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-177">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="88cfd-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="88cfd-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="88cfd-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-179">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="88cfd-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="88cfd-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="88cfd-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-181">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="88cfd-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="88cfd-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="88cfd-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-183">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88cfd-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-185">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](../wmisdk/standard-qualifiers.md) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="88cfd-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-186">Taille en octets des blocs qui forment cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="88cfd-186">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="88cfd-187">S’il est inconnu ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1.</span><span class="sxs-lookup"><span data-stu-id="88cfd-187">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="88cfd-188">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="88cfd-189">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="88cfd-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-193">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-194">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="88cfd-194">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="88cfd-195">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-196">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="88cfd-196">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-197">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88cfd-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-199">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="88cfd-199">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-200">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="88cfd-200">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="88cfd-201">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-201">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="88cfd-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="88cfd-203"> (0)</span><span class="sxs-lookup"><span data-stu-id="88cfd-203">(0)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-204">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="88cfd-204">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="88cfd-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="88cfd-206">(1)</span><span class="sxs-lookup"><span data-stu-id="88cfd-206">(1)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-207">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="88cfd-207">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="88cfd-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="88cfd-209">(2)</span><span class="sxs-lookup"><span data-stu-id="88cfd-209">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="88cfd-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="88cfd-211">(3)</span><span class="sxs-lookup"><span data-stu-id="88cfd-211">(3)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-212">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="88cfd-212">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="88cfd-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="88cfd-214">(4)</span><span class="sxs-lookup"><span data-stu-id="88cfd-214">(4)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-215">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="88cfd-215">Device is not working properly.</span></span> <span data-ttu-id="88cfd-216">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="88cfd-216">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="88cfd-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="88cfd-218">(5)</span><span class="sxs-lookup"><span data-stu-id="88cfd-218">(5)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-219">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="88cfd-219">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="88cfd-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="88cfd-221"> (6)</span><span class="sxs-lookup"><span data-stu-id="88cfd-221">(6)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-222">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="88cfd-222">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="88cfd-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="88cfd-224">(7)</span><span class="sxs-lookup"><span data-stu-id="88cfd-224">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="88cfd-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="88cfd-226">(8)</span><span class="sxs-lookup"><span data-stu-id="88cfd-226">(8)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-227">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="88cfd-227">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="88cfd-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="88cfd-229">(9)</span><span class="sxs-lookup"><span data-stu-id="88cfd-229">(9)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-230">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="88cfd-230">Device is not working properly.</span></span> <span data-ttu-id="88cfd-231">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88cfd-231">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="88cfd-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="88cfd-233">(10)</span><span class="sxs-lookup"><span data-stu-id="88cfd-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-234">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88cfd-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="88cfd-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="88cfd-236">(11)</span><span class="sxs-lookup"><span data-stu-id="88cfd-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-237">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88cfd-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="88cfd-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="88cfd-239">douze</span><span class="sxs-lookup"><span data-stu-id="88cfd-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-240">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="88cfd-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="88cfd-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="88cfd-242">(13)</span><span class="sxs-lookup"><span data-stu-id="88cfd-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-243">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88cfd-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="88cfd-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="88cfd-245">(14)</span><span class="sxs-lookup"><span data-stu-id="88cfd-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-246">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="88cfd-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="88cfd-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="88cfd-248">(15)</span><span class="sxs-lookup"><span data-stu-id="88cfd-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-249">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="88cfd-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="88cfd-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="88cfd-251">(16)</span><span class="sxs-lookup"><span data-stu-id="88cfd-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-252">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88cfd-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="88cfd-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="88cfd-254">(17)</span><span class="sxs-lookup"><span data-stu-id="88cfd-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-255">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="88cfd-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="88cfd-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="88cfd-257">(18)</span><span class="sxs-lookup"><span data-stu-id="88cfd-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-258">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="88cfd-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="88cfd-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="88cfd-260">(19)</span><span class="sxs-lookup"><span data-stu-id="88cfd-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="88cfd-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="88cfd-262">(20)</span><span class="sxs-lookup"><span data-stu-id="88cfd-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-263">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="88cfd-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="88cfd-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="88cfd-265">(21)</span><span class="sxs-lookup"><span data-stu-id="88cfd-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-266">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="88cfd-266">System failure.</span></span> <span data-ttu-id="88cfd-267">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="88cfd-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="88cfd-268">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88cfd-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="88cfd-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="88cfd-270">(22)</span><span class="sxs-lookup"><span data-stu-id="88cfd-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-271">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="88cfd-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="88cfd-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="88cfd-273">(23)</span><span class="sxs-lookup"><span data-stu-id="88cfd-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-274">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="88cfd-274">System failure.</span></span> <span data-ttu-id="88cfd-275">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="88cfd-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="88cfd-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="88cfd-277">(24)</span><span class="sxs-lookup"><span data-stu-id="88cfd-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-278">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="88cfd-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="88cfd-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="88cfd-280">(25)</span><span class="sxs-lookup"><span data-stu-id="88cfd-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-281">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88cfd-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="88cfd-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="88cfd-283">(26)</span><span class="sxs-lookup"><span data-stu-id="88cfd-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-284">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88cfd-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="88cfd-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="88cfd-286">(27)</span><span class="sxs-lookup"><span data-stu-id="88cfd-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-287">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="88cfd-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="88cfd-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="88cfd-289">(28)</span><span class="sxs-lookup"><span data-stu-id="88cfd-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-290">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="88cfd-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="88cfd-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="88cfd-292">(29)</span><span class="sxs-lookup"><span data-stu-id="88cfd-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-293">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="88cfd-293">Device is disabled.</span></span> <span data-ttu-id="88cfd-294">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="88cfd-294">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="88cfd-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="88cfd-296">(30)</span><span class="sxs-lookup"><span data-stu-id="88cfd-296">(30)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-297">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="88cfd-297">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="88cfd-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="88cfd-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="88cfd-299">31</span><span class="sxs-lookup"><span data-stu-id="88cfd-299">(31)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-300">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="88cfd-300">Device is not working properly.</span></span> <span data-ttu-id="88cfd-301">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="88cfd-301">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="88cfd-302">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="88cfd-302">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-303">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="88cfd-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-305">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="88cfd-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-306">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88cfd-306">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="88cfd-307">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-308">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="88cfd-308">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-309">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="88cfd-309">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-311">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| type erreur")</span><span class="sxs-lookup"><span data-stu-id="88cfd-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-312">Si la **valeur est true**, l’erreur la plus récente était correcte.</span><span class="sxs-lookup"><span data-stu-id="88cfd-312">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="88cfd-313">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="88cfd-313">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="88cfd-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-317">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="88cfd-317">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-318">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="88cfd-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="88cfd-319">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="88cfd-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="88cfd-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-321">**Description**</span><span class="sxs-lookup"><span data-stu-id="88cfd-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-324">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="88cfd-324">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-325">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="88cfd-325">Description of the object.</span></span>

<span data-ttu-id="88cfd-326">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="88cfd-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-330">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="88cfd-330">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-331">Identificateur unique de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="88cfd-331">Unique identifier of the logical device.</span></span>

<span data-ttu-id="88cfd-332">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-333">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="88cfd-333">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-334">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88cfd-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-336">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 19 \| Memory Device deviced \| Addresss fin Address")</span><span class="sxs-lookup"><span data-stu-id="88cfd-336">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-337">Adresse de fin, référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="88cfd-337">Ending address, referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="88cfd-338">L’adresse de fin est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="88cfd-338">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="88cfd-339">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-339">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-340">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="88cfd-340">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-341">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88cfd-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-343">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| erreur Operation")</span><span class="sxs-lookup"><span data-stu-id="88cfd-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-344">Opération d’accès à la mémoire qui a provoqué la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="88cfd-344">Memory access operation that caused the last error.</span></span> <span data-ttu-id="88cfd-345">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="88cfd-345">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="88cfd-346">Si **errorInfo** est égal à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="88cfd-346">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88cfd-347">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="88cfd-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88cfd-348">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="88cfd-348">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="88cfd-349">**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="88cfd-349">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="88cfd-350">**Écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="88cfd-350">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="88cfd-351">**Écriture partielle** (5)</span><span class="sxs-lookup"><span data-stu-id="88cfd-351">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88cfd-352">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="88cfd-352">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-353">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88cfd-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-355">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| erreur Address")</span><span class="sxs-lookup"><span data-stu-id="88cfd-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-356">Adresse de la dernière erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="88cfd-356">Address of the last memory error.</span></span> <span data-ttu-id="88cfd-357">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="88cfd-357">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="88cfd-358">Si **errorInfo** est égal à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="88cfd-358">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="88cfd-359">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-359">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-360">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="88cfd-360">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-361">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="88cfd-361">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-363">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="88cfd-363">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="88cfd-364">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-365">**Partagefichiers**</span><span class="sxs-lookup"><span data-stu-id="88cfd-365">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-366">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="88cfd-366">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-368">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="88cfd-368">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-369">Tableau de données capturées au cours du dernier accès mémoire erroné.</span><span class="sxs-lookup"><span data-stu-id="88cfd-369">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="88cfd-370">Les données occupent les *n* premiers octets du tableau nécessaire pour contenir le nombre de bits spécifié par la propriété **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="88cfd-370">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="88cfd-371">Si **ErrorTransferSize** est égal à 0 (zéro), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="88cfd-371">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-372">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="88cfd-372">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-373">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88cfd-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-375">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-376">Classement des données stockées dans la propriété **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="88cfd-376">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="88cfd-377">Si **ErrorTransferSize** est égal à 0 (zéro), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="88cfd-377">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88cfd-378">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="88cfd-378">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="88cfd-379">**Octet le moins significatif en premier** (1)</span><span class="sxs-lookup"><span data-stu-id="88cfd-379">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="88cfd-380">**Octet le plus significatif en premier** (2)</span><span class="sxs-lookup"><span data-stu-id="88cfd-380">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88cfd-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="88cfd-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-384">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="88cfd-384">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="88cfd-385">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="88cfd-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-387">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88cfd-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-389">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ mémoire CIM**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS \| type 18 \| 32-bit Memory Error information \| type erreur ")</span><span class="sxs-lookup"><span data-stu-id="88cfd-389">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-390">Type d’erreur qui s’est produite le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="88cfd-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="88cfd-391">Les valeurs 12 à 14 ne sont pas utilisées.</span><span class="sxs-lookup"><span data-stu-id="88cfd-391">The values 12 through 14 are unused.</span></span> <span data-ttu-id="88cfd-392">La possibilité d’être corrigée est indiquée dans la propriété **CorrectableError**.</span><span class="sxs-lookup"><span data-stu-id="88cfd-392">The ability to be corrected is indicated in the property **CorrectableError**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88cfd-393">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="88cfd-393">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88cfd-394">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="88cfd-394">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="88cfd-395">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="88cfd-395">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="88cfd-396">**Lecture incorrecte** (4)</span><span class="sxs-lookup"><span data-stu-id="88cfd-396">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="88cfd-397">**Erreur de parité** (5)</span><span class="sxs-lookup"><span data-stu-id="88cfd-397">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="88cfd-398">**Erreur de bit unique** (6)</span><span class="sxs-lookup"><span data-stu-id="88cfd-398">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="88cfd-399">**Erreur double bit** (7)</span><span class="sxs-lookup"><span data-stu-id="88cfd-399">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="88cfd-400">**Erreur multibits** (8)</span><span class="sxs-lookup"><span data-stu-id="88cfd-400">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="88cfd-401">**Erreur de grignotage** (9)</span><span class="sxs-lookup"><span data-stu-id="88cfd-401">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="88cfd-402">**Erreur de somme de contrôle** (10)</span><span class="sxs-lookup"><span data-stu-id="88cfd-402">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="88cfd-403">**Erreur CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="88cfd-403">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="88cfd-404">**Erreur de correction sur un bit** (12)</span><span class="sxs-lookup"><span data-stu-id="88cfd-404">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="88cfd-405">**Erreur corrigée** (13)</span><span class="sxs-lookup"><span data-stu-id="88cfd-405">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="88cfd-406">**Erreur** impossible à corriger (14)</span><span class="sxs-lookup"><span data-stu-id="88cfd-406">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88cfd-407">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="88cfd-407">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-408">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-410">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("erreur de \| \| mémoire physique du groupe de mémoires physiques du type SMBIOS \| ")</span><span class="sxs-lookup"><span data-stu-id="88cfd-410">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-411">Détails sur la parité ou les algorithmes CRC, ECC ou autres mécanismes utilisés.</span><span class="sxs-lookup"><span data-stu-id="88cfd-411">Details on the parity or CRC algorithms, ECC or other mechanisms used.</span></span>

<span data-ttu-id="88cfd-412">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-412">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88cfd-413">**Autre** (« autre »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-413">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88cfd-414">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="88cfd-414">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="88cfd-415">**Aucun** (« aucun »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-415">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="88cfd-416">**Parité** (« parité »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-416">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="88cfd-417">**ECC sur** un bit (ECC sur un bit)</span><span class="sxs-lookup"><span data-stu-id="88cfd-417">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="88cfd-418">**ECC multi-bits** (« ECC multi-bits »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-418">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="88cfd-419">**CRC** (« CRC »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-419">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88cfd-420">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="88cfd-420">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-421">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88cfd-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-423">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| résolution d’erreur"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="88cfd-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-424">Plage, en octets, à laquelle la dernière erreur peut être résolue.</span><span class="sxs-lookup"><span data-stu-id="88cfd-424">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="88cfd-425">Par exemple, si les adresses d’erreurs sont résolues en bit 11 (c’est-à-dire, sur une base de page standard), les erreurs peuvent être résolues en limites de 4 Ko et cette propriété est définie sur 4000.</span><span class="sxs-lookup"><span data-stu-id="88cfd-425">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="88cfd-426">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="88cfd-426">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="88cfd-427">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-427">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-428">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="88cfd-428">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-429">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88cfd-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-431">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-431">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-432">Heure à laquelle la dernière erreur de mémoire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="88cfd-432">Time that the last memory error occurred.</span></span> <span data-ttu-id="88cfd-433">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="88cfd-433">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="88cfd-434">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="88cfd-434">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-435">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="88cfd-435">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-436">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88cfd-436">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-438">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="88cfd-438">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-439">Taille du transfert de données en bits qui a provoqué la dernière erreur : 0 (zéro) indique qu’il n’y a pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="88cfd-439">Size of the data transfer in bits that caused the last error—0 (zero) indicates no error.</span></span> <span data-ttu-id="88cfd-440">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="88cfd-440">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-441">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88cfd-441">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-442">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88cfd-442">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-443">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-444">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="88cfd-444">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-445">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="88cfd-445">Date and time the object was installed.</span></span> <span data-ttu-id="88cfd-446">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="88cfd-446">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="88cfd-447">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-448">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="88cfd-448">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-449">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88cfd-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-451">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="88cfd-451">Last error code reported by the logical device.</span></span>

<span data-ttu-id="88cfd-452">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-453">**Nom**</span><span class="sxs-lookup"><span data-stu-id="88cfd-453">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-454">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-456">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="88cfd-456">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-457">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="88cfd-457">Label by which the object is known.</span></span> <span data-ttu-id="88cfd-458">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="88cfd-458">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="88cfd-459">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-459">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-460">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="88cfd-460">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-461">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88cfd-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-462">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-463">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="88cfd-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-464">Nombre total de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forme cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="88cfd-464">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="88cfd-465">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88cfd-465">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="88cfd-466">Si la valeur de **BlockSize** est 1, cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="88cfd-466">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="88cfd-467">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-467">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="88cfd-468">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-468">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-469">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="88cfd-469">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-470">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-470">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-471">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-472">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ mémoire CIM**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="88cfd-472">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-473">Chaîne de forme libre qui fournit plus d’informations si la propriété **ErrorType** est définie sur 1 ; dans le cas contraire, cette chaîne n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="88cfd-473">Free-form string that provides more information if the **ErrorType** property is set to 1; otherwise, this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-474">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="88cfd-474">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-475">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-476">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-477">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="88cfd-477">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-478">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="88cfd-478">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="88cfd-479">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="88cfd-479">Example: "\*PNP030b"</span></span>

<span data-ttu-id="88cfd-480">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-481">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="88cfd-481">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-482">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88cfd-482">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-483">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-484">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="88cfd-484">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="88cfd-485">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88cfd-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="88cfd-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="88cfd-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="88cfd-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="88cfd-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="88cfd-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="88cfd-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="88cfd-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-490">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="88cfd-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="88cfd-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="88cfd-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-492">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="88cfd-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="88cfd-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="88cfd-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-494">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="88cfd-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="88cfd-495">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="88cfd-495">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="88cfd-496">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-496">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="88cfd-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="88cfd-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-498">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="88cfd-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="88cfd-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="88cfd-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="88cfd-500">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="88cfd-500">Timed Power-On Supported</span></span>

<span data-ttu-id="88cfd-501">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="88cfd-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="88cfd-502">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="88cfd-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-503">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="88cfd-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-504">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-505">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="88cfd-505">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="88cfd-506">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="88cfd-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="88cfd-507">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-508">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="88cfd-508">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-509">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-509">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-510">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-511">Chaîne de forme libre décrivant le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="88cfd-511">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="88cfd-512">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-512">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-513">**De la**</span><span class="sxs-lookup"><span data-stu-id="88cfd-513">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-514">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88cfd-514">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-515">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-516">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 19 \| Memory Device mapped \| Addresss Start Address")</span><span class="sxs-lookup"><span data-stu-id="88cfd-516">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-517">Adresse de début référencée par une application ou un système d’exploitation, et mappée par un contrôleur de mémoire pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="88cfd-517">Beginning address that is referenced by an application or operating system, and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="88cfd-518">L’adresse de départ est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="88cfd-518">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="88cfd-519">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-519">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-520">**État**</span><span class="sxs-lookup"><span data-stu-id="88cfd-520">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-521">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-522">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-523">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="88cfd-523">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-524">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="88cfd-524">Current status of the object.</span></span> <span data-ttu-id="88cfd-525">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="88cfd-525">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="88cfd-526">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="88cfd-526">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="88cfd-527">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="88cfd-527">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="88cfd-528">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="88cfd-528">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="88cfd-529">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="88cfd-529">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="88cfd-530">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-530">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="88cfd-531">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="88cfd-531">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="88cfd-532">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-532">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="88cfd-533">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-533">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="88cfd-534">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-534">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88cfd-535">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="88cfd-535">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="88cfd-536">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-536">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="88cfd-537">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-537">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="88cfd-538">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-538">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="88cfd-539">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-539">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="88cfd-540">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-540">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="88cfd-541">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-541">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="88cfd-542">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-542">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="88cfd-543">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="88cfd-543">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88cfd-544">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="88cfd-544">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-545">Type de données : **uint16e**</span><span class="sxs-lookup"><span data-stu-id="88cfd-545">Data type: **uint16e**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-546">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-547">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="88cfd-547">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-548">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="88cfd-548">State of the logical device.</span></span> <span data-ttu-id="88cfd-549">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="88cfd-549">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="88cfd-550">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88cfd-551">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="88cfd-551">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88cfd-552">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="88cfd-552">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="88cfd-553">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="88cfd-553">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="88cfd-554">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="88cfd-554">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="88cfd-555">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="88cfd-555">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88cfd-556">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="88cfd-556">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-557">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-558">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-559">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="88cfd-559">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-560">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="88cfd-560">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="88cfd-561">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-561">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-562">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="88cfd-562">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-563">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="88cfd-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-564">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-565">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| erreur Address")</span><span class="sxs-lookup"><span data-stu-id="88cfd-565">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-566">Si la **valeur est true**, les informations d’adresse dans la propriété **ErrorAddress** sont une adresse de niveau système.</span><span class="sxs-lookup"><span data-stu-id="88cfd-566">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="88cfd-567">Si la **valeur est false**, il s’agit d’une adresse physique.</span><span class="sxs-lookup"><span data-stu-id="88cfd-567">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="88cfd-568">Si la propriété **errorInfo** est égale à 3 (OK), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="88cfd-568">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88cfd-569">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="88cfd-569">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88cfd-570">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="88cfd-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-571">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88cfd-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88cfd-572">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="88cfd-572">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="88cfd-573">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="88cfd-573">Name of the scoping system.</span></span>

<span data-ttu-id="88cfd-574">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-574">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88cfd-575">Notes</span><span class="sxs-lookup"><span data-stu-id="88cfd-575">Remarks</span></span>

<span data-ttu-id="88cfd-576">La classe **Win32 \_ SMBIOSMemory** est dérivée de [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="88cfd-576">The **Win32\_SMBIOSMemory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88cfd-577">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88cfd-577">Requirements</span></span>



| <span data-ttu-id="88cfd-578">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88cfd-578">Requirement</span></span> | <span data-ttu-id="88cfd-579">Valeur</span><span class="sxs-lookup"><span data-stu-id="88cfd-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88cfd-580">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88cfd-580">Minimum supported client</span></span><br/> | <span data-ttu-id="88cfd-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88cfd-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88cfd-582">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88cfd-582">Minimum supported server</span></span><br/> | <span data-ttu-id="88cfd-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88cfd-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88cfd-584">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="88cfd-584">Namespace</span></span><br/>                | <span data-ttu-id="88cfd-585">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="88cfd-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88cfd-586">MOF</span><span class="sxs-lookup"><span data-stu-id="88cfd-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88cfd-587"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88cfd-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88cfd-588">DLL</span><span class="sxs-lookup"><span data-stu-id="88cfd-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88cfd-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88cfd-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88cfd-590">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88cfd-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88cfd-591">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="88cfd-591">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="88cfd-592">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="88cfd-592">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
