---
description: La \_ classe WMI MemoryArray WMI représente les propriétés du tableau de la mémoire système de l’ordinateur et les adresses mappées.
ms.assetid: 56ff6960-cde3-4e34-b4df-d2993bafaa62
ms.tgt_platform: multiple
title: Classe Win32_MemoryArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArray
- Win32_MemoryArray.Reset
- Win32_MemoryArray.SetPowerState
- Win32_MemoryArray.Access
- Win32_MemoryArray.AdditionalErrorData
- Win32_MemoryArray.Availability
- Win32_MemoryArray.BlockSize
- Win32_MemoryArray.Caption
- Win32_MemoryArray.ConfigManagerErrorCode
- Win32_MemoryArray.ConfigManagerUserConfig
- Win32_MemoryArray.CorrectableError
- Win32_MemoryArray.CreationClassName
- Win32_MemoryArray.Description
- Win32_MemoryArray.DeviceID
- Win32_MemoryArray.EndingAddress
- Win32_MemoryArray.ErrorAccess
- Win32_MemoryArray.ErrorAddress
- Win32_MemoryArray.ErrorCleared
- Win32_MemoryArray.ErrorData
- Win32_MemoryArray.ErrorDataOrder
- Win32_MemoryArray.ErrorDescription
- Win32_MemoryArray.ErrorGranularity
- Win32_MemoryArray.ErrorInfo
- Win32_MemoryArray.ErrorMethodology
- Win32_MemoryArray.ErrorResolution
- Win32_MemoryArray.ErrorTime
- Win32_MemoryArray.ErrorTransferSize
- Win32_MemoryArray.InstallDate
- Win32_MemoryArray.LastErrorCode
- Win32_MemoryArray.Name
- Win32_MemoryArray.NumberOfBlocks
- Win32_MemoryArray.OtherErrorDescription
- Win32_MemoryArray.PNPDeviceID
- Win32_MemoryArray.PowerManagementCapabilities
- Win32_MemoryArray.PowerManagementSupported
- Win32_MemoryArray.Purpose
- Win32_MemoryArray.StartingAddress
- Win32_MemoryArray.Status
- Win32_MemoryArray.StatusInfo
- Win32_MemoryArray.SystemCreationClassName
- Win32_MemoryArray.SystemLevelAddress
- Win32_MemoryArray.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c102d383502bec4808b26a87eb2f6d8445b6c2a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201112"
---
# <a name="win32_memoryarray-class"></a><span data-ttu-id="abe44-103">\_Classe MemoryArray Win32</span><span class="sxs-lookup"><span data-stu-id="abe44-103">Win32\_MemoryArray class</span></span>

<span data-ttu-id="abe44-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryArray** WMI représente les propriétés du tableau de la mémoire système de l’ordinateur et les adresses mappées.</span><span class="sxs-lookup"><span data-stu-id="abe44-104">The **Win32\_MemoryArray** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of the computer system memory array and mapped addresses.</span></span>

<span data-ttu-id="abe44-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="abe44-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="abe44-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="abe44-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe44-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abe44-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryArray : Win32_SMBIOSMemory
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
  uint16   ErrorGranularity;
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
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="abe44-108">Membres</span><span class="sxs-lookup"><span data-stu-id="abe44-108">Members</span></span>

<span data-ttu-id="abe44-109">La classe **Win32 \_ MemoryArray** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="abe44-109">The **Win32\_MemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="abe44-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="abe44-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="abe44-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abe44-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="abe44-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="abe44-112">Methods</span></span>

<span data-ttu-id="abe44-113">La classe **Win32 \_ MemoryArray** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="abe44-113">The **Win32\_MemoryArray** class has these methods.</span></span>



| <span data-ttu-id="abe44-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="abe44-114">Method</span></span>            | <span data-ttu-id="abe44-115">Description</span><span class="sxs-lookup"><span data-stu-id="abe44-115">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abe44-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="abe44-116">**Reset**</span></span>         | <span data-ttu-id="abe44-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="abe44-117">Not implemented.</span></span> <span data-ttu-id="abe44-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="abe44-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="abe44-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="abe44-119">**SetPowerState**</span></span> | <span data-ttu-id="abe44-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="abe44-120">Not implemented.</span></span> <span data-ttu-id="abe44-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="abe44-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="abe44-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abe44-122">Properties</span></span>

<span data-ttu-id="abe44-123">La classe **Win32 \_ MemoryArray** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="abe44-123">The **Win32\_MemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abe44-124">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="abe44-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abe44-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abe44-127">Type d’accès aux médias disponible.</span><span class="sxs-lookup"><span data-stu-id="abe44-127">Type of media access available.</span></span>

<span data-ttu-id="abe44-128">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abe44-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="abe44-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="abe44-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="abe44-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="abe44-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="abe44-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-132">Accessible en écriture</span><span class="sxs-lookup"><span data-stu-id="abe44-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="abe44-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="abe44-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="abe44-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="abe44-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="abe44-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-136">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="abe44-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="abe44-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-138">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory information Error \| syndrome"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="abe44-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="abe44-139">Tableau d’informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="abe44-139">Array of additional error information.</span></span> <span data-ttu-id="abe44-140">Par exemple, le syndrome de la vérification et de la correction des erreurs (ECC), ou le retour des bits de vérification si une valeur **ErrorMethodology** basée sur un contrôle de redondance cyclique (CRC) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="abe44-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based **ErrorMethodology** value is used.</span></span> <span data-ttu-id="abe44-141">Dans ce dernier cas, si une erreur de bit unique est reconnue et que l’algorithme CRC est connu, il est possible de déterminer le bit exact qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="abe44-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="abe44-142">Ce type de données (syndrome ECC, bit de vérification, données de bit de parité ou autres informations fournies par le fournisseur) est inclus dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="abe44-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="abe44-143">Cette propriété est utilisée uniquement lorsque la propriété **errorInfo** n’est pas égale à 3.</span><span class="sxs-lookup"><span data-stu-id="abe44-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="abe44-144">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-145">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="abe44-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-146">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abe44-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="abe44-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-149">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abe44-149">Availability and status of the device.</span></span>

<span data-ttu-id="abe44-150">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="abe44-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="abe44-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abe44-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="abe44-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="abe44-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="abe44-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-154">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="abe44-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="abe44-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="abe44-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="abe44-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="abe44-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="abe44-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="abe44-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="abe44-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="abe44-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="abe44-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="abe44-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="abe44-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="abe44-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="abe44-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="abe44-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="abe44-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="abe44-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="abe44-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="abe44-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="abe44-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="abe44-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-165">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="abe44-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="abe44-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="abe44-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-167">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="abe44-167">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="abe44-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="abe44-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-169">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="abe44-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="abe44-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="abe44-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="abe44-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="abe44-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-172">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="abe44-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="abe44-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="abe44-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-174">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="abe44-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="abe44-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="abe44-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-176">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="abe44-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="abe44-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="abe44-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-178">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="abe44-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="abe44-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="abe44-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-180">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="abe44-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="abe44-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-182">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abe44-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-184">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="abe44-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-185">Taille en octets des blocs qui forment cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="abe44-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="abe44-186">S’il est inconnu ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1.</span><span class="sxs-lookup"><span data-stu-id="abe44-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="abe44-187">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="abe44-188">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="abe44-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="abe44-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-192">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="abe44-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-193">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="abe44-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="abe44-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="abe44-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-196">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abe44-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-198">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="abe44-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-199">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="abe44-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="abe44-200">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="abe44-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="abe44-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="abe44-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="abe44-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-203">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="abe44-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="abe44-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="abe44-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="abe44-205">(1)</span><span class="sxs-lookup"><span data-stu-id="abe44-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-206">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="abe44-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="abe44-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="abe44-208">(2)</span><span class="sxs-lookup"><span data-stu-id="abe44-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="abe44-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="abe44-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="abe44-210">(3)</span><span class="sxs-lookup"><span data-stu-id="abe44-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-211">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="abe44-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="abe44-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="abe44-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="abe44-213">(4)</span><span class="sxs-lookup"><span data-stu-id="abe44-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-214">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="abe44-214">Device is not working properly.</span></span> <span data-ttu-id="abe44-215">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="abe44-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="abe44-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="abe44-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="abe44-217">(5)</span><span class="sxs-lookup"><span data-stu-id="abe44-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-218">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="abe44-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="abe44-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="abe44-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="abe44-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="abe44-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-221">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="abe44-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="abe44-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="abe44-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="abe44-223">(7)</span><span class="sxs-lookup"><span data-stu-id="abe44-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="abe44-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="abe44-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="abe44-225">(8)</span><span class="sxs-lookup"><span data-stu-id="abe44-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-226">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="abe44-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="abe44-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="abe44-228">(9)</span><span class="sxs-lookup"><span data-stu-id="abe44-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-229">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="abe44-229">Device is not working properly.</span></span> <span data-ttu-id="abe44-230">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abe44-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="abe44-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="abe44-232">(10)</span><span class="sxs-lookup"><span data-stu-id="abe44-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-233">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abe44-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="abe44-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="abe44-235">(11)</span><span class="sxs-lookup"><span data-stu-id="abe44-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-236">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abe44-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="abe44-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="abe44-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="abe44-238">douze</span><span class="sxs-lookup"><span data-stu-id="abe44-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-239">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="abe44-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="abe44-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="abe44-241">(13)</span><span class="sxs-lookup"><span data-stu-id="abe44-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-242">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abe44-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="abe44-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="abe44-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="abe44-244">(14)</span><span class="sxs-lookup"><span data-stu-id="abe44-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-245">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="abe44-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="abe44-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="abe44-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="abe44-247">(15)</span><span class="sxs-lookup"><span data-stu-id="abe44-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-248">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="abe44-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="abe44-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="abe44-250">(16)</span><span class="sxs-lookup"><span data-stu-id="abe44-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-251">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abe44-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="abe44-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="abe44-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="abe44-253">(17)</span><span class="sxs-lookup"><span data-stu-id="abe44-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-254">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="abe44-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="abe44-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="abe44-256">(18)</span><span class="sxs-lookup"><span data-stu-id="abe44-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-257">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="abe44-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="abe44-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="abe44-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="abe44-259">(19)</span><span class="sxs-lookup"><span data-stu-id="abe44-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="abe44-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="abe44-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="abe44-261">(20)</span><span class="sxs-lookup"><span data-stu-id="abe44-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-262">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="abe44-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="abe44-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="abe44-264">(21)</span><span class="sxs-lookup"><span data-stu-id="abe44-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-265">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="abe44-265">System failure.</span></span> <span data-ttu-id="abe44-266">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="abe44-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="abe44-267">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abe44-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="abe44-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="abe44-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="abe44-269">(22)</span><span class="sxs-lookup"><span data-stu-id="abe44-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-270">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="abe44-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="abe44-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="abe44-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="abe44-272">(23)</span><span class="sxs-lookup"><span data-stu-id="abe44-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-273">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="abe44-273">System failure.</span></span> <span data-ttu-id="abe44-274">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="abe44-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="abe44-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="abe44-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="abe44-276">(24)</span><span class="sxs-lookup"><span data-stu-id="abe44-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-277">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="abe44-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="abe44-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="abe44-279">(25)</span><span class="sxs-lookup"><span data-stu-id="abe44-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-280">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abe44-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="abe44-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="abe44-282">(26)</span><span class="sxs-lookup"><span data-stu-id="abe44-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-283">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abe44-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="abe44-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="abe44-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="abe44-285">(27)</span><span class="sxs-lookup"><span data-stu-id="abe44-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-286">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="abe44-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="abe44-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="abe44-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="abe44-288">(28)</span><span class="sxs-lookup"><span data-stu-id="abe44-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-289">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="abe44-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="abe44-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="abe44-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="abe44-291">(29)</span><span class="sxs-lookup"><span data-stu-id="abe44-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-292">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="abe44-292">Device is disabled.</span></span> <span data-ttu-id="abe44-293">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="abe44-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="abe44-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="abe44-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="abe44-295">(30)</span><span class="sxs-lookup"><span data-stu-id="abe44-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-296">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="abe44-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="abe44-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="abe44-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="abe44-298">31</span><span class="sxs-lookup"><span data-stu-id="abe44-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-299">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="abe44-299">Device is not working properly.</span></span> <span data-ttu-id="abe44-300">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="abe44-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="abe44-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-302">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="abe44-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-304">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="abe44-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-305">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abe44-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="abe44-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-307">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="abe44-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-308">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="abe44-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-310">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| type erreur")</span><span class="sxs-lookup"><span data-stu-id="abe44-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-311">Si la **valeur est true**, l’erreur la plus récente était correcte.</span><span class="sxs-lookup"><span data-stu-id="abe44-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="abe44-312">Cette propriété n’est pas utilisée si **errorInfo** a la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="abe44-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="abe44-313">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="abe44-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-317">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="abe44-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="abe44-318">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="abe44-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="abe44-319">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="abe44-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="abe44-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-321">**Description**</span><span class="sxs-lookup"><span data-stu-id="abe44-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-324">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="abe44-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-325">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="abe44-325">Description of the object.</span></span>

<span data-ttu-id="abe44-326">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="abe44-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-330">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« DeviceID »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="abe44-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-331">Identificateur unique du tableau de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="abe44-331">Unique identifier of the memory array.</span></span>

<span data-ttu-id="abe44-332">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="abe44-333">Exemple : « Memory Array 1 »</span><span class="sxs-lookup"><span data-stu-id="abe44-333">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="abe44-334">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="abe44-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-335">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abe44-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-337">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 19 \| Memory Device deviced \| Addresss fin Address")</span><span class="sxs-lookup"><span data-stu-id="abe44-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-338">Adresse de fin référencée par une application ou un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="abe44-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="abe44-339">Cette adresse mémoire est mappée par un contrôleur de mémoire pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="abe44-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="abe44-340">Cette valeur provient de la structure d' **adresse mappée du tableau de mémoire** dans les informations de version SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="abe44-340">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="abe44-341">Pour les versions SMBIOS 2,1 à 2,6, la valeur provient du membre d' **adresse de fin** .</span><span class="sxs-lookup"><span data-stu-id="abe44-341">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Ending Address** member.</span></span> <span data-ttu-id="abe44-342">Pour SMBIOS version 2.7 +, la valeur provient du membre de l' **adresse de fin étendue** .</span><span class="sxs-lookup"><span data-stu-id="abe44-342">For SMBIOS version 2.7+ the value comes from the **Extended Ending Address** member.</span></span>

<span data-ttu-id="abe44-343">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-343">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="abe44-344">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="abe44-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-345">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="abe44-345">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-346">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abe44-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-348">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| erreur Operation")</span><span class="sxs-lookup"><span data-stu-id="abe44-348">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-349">Type d’opération d’accès mémoire à l’origine de la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="abe44-349">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="abe44-350">Cette propriété est valide uniquement lorsque **errorInfo** n’a pas la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="abe44-350">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="abe44-351">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-351">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="abe44-352">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="abe44-352">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abe44-353">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="abe44-353">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="abe44-354">**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="abe44-354">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="abe44-355">**Écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="abe44-355">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="abe44-356">**Écriture partielle** (5)</span><span class="sxs-lookup"><span data-stu-id="abe44-356">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-357">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="abe44-357">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-358">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abe44-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-360">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| erreur Address")</span><span class="sxs-lookup"><span data-stu-id="abe44-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-361">Adresse de la dernière erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="abe44-361">Address of the last memory error.</span></span> <span data-ttu-id="abe44-362">Cette propriété est utilisée uniquement lorsque **errorInfo** n’a pas la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="abe44-362">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="abe44-363">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-363">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="abe44-364">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="abe44-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-365">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="abe44-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-366">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="abe44-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abe44-368">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="abe44-368">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="abe44-369">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-370">**Partagefichiers**</span><span class="sxs-lookup"><span data-stu-id="abe44-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-371">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="abe44-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="abe44-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-373">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="abe44-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="abe44-374">Tableau de données capturées à partir du dernier accès mémoire avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="abe44-374">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="abe44-375">Les données occupent les *n* premiers octets du tableau nécessaire pour contenir le nombre de bits spécifié par la propriété **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="abe44-375">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="abe44-376">Si **ErrorTransferSize** est égal à 0 (zéro), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="abe44-376">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="abe44-377">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-377">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-378">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="abe44-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-379">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abe44-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-381">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="abe44-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-382">Classement des données stockées dans la propriété **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="abe44-382">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="abe44-383">Cette propriété est utilisée uniquement lorsque **ErrorTransferSize** est égal à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="abe44-383">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="abe44-384">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-384">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abe44-385">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="abe44-385">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="abe44-386">**Octet le moins significatif en premier** (1)</span><span class="sxs-lookup"><span data-stu-id="abe44-386">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="abe44-387">**Octet le plus significatif en premier** (2)</span><span class="sxs-lookup"><span data-stu-id="abe44-387">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-388">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="abe44-388">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-389">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abe44-391">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="abe44-391">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="abe44-392">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-393">**ErrorGranularity**</span><span class="sxs-lookup"><span data-stu-id="abe44-393">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-394">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abe44-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-396">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| Error finesse")</span><span class="sxs-lookup"><span data-stu-id="abe44-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-397">Niveau où l’erreur peut être résolue.</span><span class="sxs-lookup"><span data-stu-id="abe44-397">Level where the error can be resolved.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="abe44-398">**1** (autre)</span><span class="sxs-lookup"><span data-stu-id="abe44-398">**1** (Other)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="abe44-399">**2** (inconnu)</span><span class="sxs-lookup"><span data-stu-id="abe44-399">**2** (Unknown)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="abe44-400">**3** (niveau de l’appareil)</span><span class="sxs-lookup"><span data-stu-id="abe44-400">**3** (Device level)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="abe44-401">**4** (niveau de la partition de mémoire)</span><span class="sxs-lookup"><span data-stu-id="abe44-401">**4** (Memory partition level)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-402">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="abe44-402">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-403">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abe44-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-405">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ mémoire CIM**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS \| type 18 \| 32-bit Memory Error information \| type erreur ")</span><span class="sxs-lookup"><span data-stu-id="abe44-405">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-406">Type d’erreur qui s’est produite le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="abe44-406">Type of error that occurred most recently.</span></span> <span data-ttu-id="abe44-407">Les valeurs 12-14, qui indiquent si une erreur peut être corrigée, ne sont pas utilisées avec cette propriété, mais ces informations se trouvent dans la propriété **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="abe44-407">The values 12-14, which indicate whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="abe44-408">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-408">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="abe44-409">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="abe44-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abe44-410">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="abe44-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="abe44-411">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="abe44-411">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="abe44-412">**Lecture incorrecte** (4)</span><span class="sxs-lookup"><span data-stu-id="abe44-412">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="abe44-413">**Erreur de parité** (5)</span><span class="sxs-lookup"><span data-stu-id="abe44-413">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="abe44-414">**Erreur de bit unique** (6)</span><span class="sxs-lookup"><span data-stu-id="abe44-414">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="abe44-415">**Erreur double bit** (7)</span><span class="sxs-lookup"><span data-stu-id="abe44-415">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="abe44-416">**Erreur multibits** (8)</span><span class="sxs-lookup"><span data-stu-id="abe44-416">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="abe44-417">**Erreur de grignotage** (9)</span><span class="sxs-lookup"><span data-stu-id="abe44-417">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="abe44-418">**Erreur de somme de contrôle** (10)</span><span class="sxs-lookup"><span data-stu-id="abe44-418">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="abe44-419">**Erreur CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="abe44-419">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="abe44-420">**Erreur de correction sur un bit** (12)</span><span class="sxs-lookup"><span data-stu-id="abe44-420">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="abe44-421">**Erreur corrigée** (13)</span><span class="sxs-lookup"><span data-stu-id="abe44-421">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="abe44-422">**Erreur** impossible à corriger (14)</span><span class="sxs-lookup"><span data-stu-id="abe44-422">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-423">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="abe44-423">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-424">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-426">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| type d’erreur de \| mémoire physique du groupe de mémoire physique de type SMBIOS \| ")</span><span class="sxs-lookup"><span data-stu-id="abe44-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-427">Types de contrôle d’erreur utilisés par le matériel de mémoire.</span><span class="sxs-lookup"><span data-stu-id="abe44-427">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="abe44-428">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="abe44-429">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="abe44-429">The values are:</span></span>

<dl> <dd><span data-ttu-id="abe44-430">Autres</span><span class="sxs-lookup"><span data-stu-id="abe44-430">"Other"</span></span></dd> <dd><span data-ttu-id="abe44-431">Connue</span><span class="sxs-lookup"><span data-stu-id="abe44-431">"Unknown"</span></span></dd> <dd><span data-ttu-id="abe44-432">"None"</span><span class="sxs-lookup"><span data-stu-id="abe44-432">"None"</span></span></dd> <dd><span data-ttu-id="abe44-433">Parité</span><span class="sxs-lookup"><span data-stu-id="abe44-433">"Parity"</span></span></dd> <dd><span data-ttu-id="abe44-434">« ECC sur un bit »</span><span class="sxs-lookup"><span data-stu-id="abe44-434">"Single-bit ECC"</span></span></dd> <dd><span data-ttu-id="abe44-435">« ECC multi-bits »</span><span class="sxs-lookup"><span data-stu-id="abe44-435">"Multi-bit ECC"</span></span></dd> <dd><span data-ttu-id="abe44-436">Erreurs</span><span class="sxs-lookup"><span data-stu-id="abe44-436">"CRC"</span></span></dd> </dl>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="abe44-437">**Autre** (« autre »)</span><span class="sxs-lookup"><span data-stu-id="abe44-437">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abe44-438">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="abe44-438">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="abe44-439">**Aucun** (« aucun »)</span><span class="sxs-lookup"><span data-stu-id="abe44-439">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="abe44-440">**Parité** (« parité »)</span><span class="sxs-lookup"><span data-stu-id="abe44-440">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="abe44-441">**ECC sur** un bit (ECC sur un bit)</span><span class="sxs-lookup"><span data-stu-id="abe44-441">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="abe44-442">**ECC multi-bits** (« ECC multi-bits »)</span><span class="sxs-lookup"><span data-stu-id="abe44-442">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="abe44-443">**CRC** (« CRC »)</span><span class="sxs-lookup"><span data-stu-id="abe44-443">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-444">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="abe44-444">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-445">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abe44-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-447">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| résolution d’erreur"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="abe44-447">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-448">Quantité de données réellement déterminées pour provoquer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="abe44-448">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="abe44-449">Cette propriété n’est pas utilisée lorsque la propriété **errorInfo** a la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="abe44-449">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="abe44-450">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-450">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="abe44-451">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="abe44-451">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-452">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="abe44-452">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-453">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="abe44-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-454">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-455">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="abe44-455">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-456">Heure à laquelle la dernière erreur de mémoire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="abe44-456">Time that the last memory error occurred.</span></span> <span data-ttu-id="abe44-457">Cette propriété est valide uniquement lorsque **errorInfo** n’a pas la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="abe44-457">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="abe44-458">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-458">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-459">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="abe44-459">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-460">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abe44-460">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-461">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-462">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="abe44-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-463">Taille des données (contenant la dernière erreur) en cours de transfert.</span><span class="sxs-lookup"><span data-stu-id="abe44-463">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="abe44-464">Cette propriété a la valeur 0 (zéro) s’il n’y a pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="abe44-464">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="abe44-465">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-465">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-466">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="abe44-466">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-467">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="abe44-467">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-468">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-469">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="abe44-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-470">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="abe44-470">Date and time the object was installed.</span></span> <span data-ttu-id="abe44-471">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="abe44-471">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="abe44-472">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-472">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-473">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="abe44-473">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-474">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abe44-474">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abe44-476">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="abe44-476">Last error code reported by the logical device.</span></span>

<span data-ttu-id="abe44-477">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-478">**Nom**</span><span class="sxs-lookup"><span data-stu-id="abe44-478">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-479">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-480">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-481">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="abe44-481">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-482">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="abe44-482">Label by which the object is known.</span></span> <span data-ttu-id="abe44-483">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="abe44-483">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="abe44-484">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-484">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-485">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="abe44-485">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-486">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abe44-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-488">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="abe44-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-489">Nombre total de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forme cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="abe44-489">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="abe44-490">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="abe44-490">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="abe44-491">Si la valeur de **BlockSize** est 1, cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="abe44-491">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="abe44-492">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-492">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="abe44-493">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="abe44-493">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-494">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="abe44-494">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-495">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-496">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-497">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ mémoire CIM**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="abe44-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-498">Plus d’informations lorsque la propriété **errorInfo** est définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="abe44-498">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="abe44-499">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-499">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="abe44-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-501">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-502">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-503">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="abe44-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-504">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="abe44-504">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="abe44-505">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="abe44-506">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="abe44-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="abe44-507">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="abe44-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-508">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abe44-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="abe44-509">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abe44-510">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="abe44-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="abe44-511">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="abe44-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abe44-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="abe44-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="abe44-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="abe44-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="abe44-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="abe44-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="abe44-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="abe44-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-516">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="abe44-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="abe44-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="abe44-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-518">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="abe44-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="abe44-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="abe44-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-520">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="abe44-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="abe44-521">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="abe44-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="abe44-522">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="abe44-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="abe44-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="abe44-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-524">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="abe44-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="abe44-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="abe44-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="abe44-526">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="abe44-526">Timed Power-On Supported</span></span>

<span data-ttu-id="abe44-527">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="abe44-527">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-528">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="abe44-528">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-529">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="abe44-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-530">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abe44-531">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="abe44-531">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="abe44-532">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="abe44-532">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="abe44-533">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-533">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-534">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="abe44-534">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-535">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-536">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abe44-537">Chaîne de forme libre décrivant le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="abe44-537">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="abe44-538">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-538">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-539">**De la**</span><span class="sxs-lookup"><span data-stu-id="abe44-539">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-540">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abe44-540">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-541">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-542">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 19 \| Memory Device mapped \| Addresss Start Address")</span><span class="sxs-lookup"><span data-stu-id="abe44-542">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-543">Adresse de début référencée par une application ou le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="abe44-543">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="abe44-544">Cette adresse mémoire est mappée par un contrôleur de mémoire pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="abe44-544">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="abe44-545">Cette valeur provient de la structure d' **adresse mappée du tableau de mémoire** dans les informations de version SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="abe44-545">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="abe44-546">Pour les versions SMBIOS 2,1 à 2,6, la valeur provient du membre **adresse de départ** .</span><span class="sxs-lookup"><span data-stu-id="abe44-546">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Starting Address** member.</span></span> <span data-ttu-id="abe44-547">Pour SMBIOS version 2.7 +, la valeur provient du membre de l' **adresse de départ étendue** .</span><span class="sxs-lookup"><span data-stu-id="abe44-547">For SMBIOS version 2.7+ the value comes from the **Extended Starting Address** member.</span></span>

<span data-ttu-id="abe44-548">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-548">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="abe44-549">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="abe44-549">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-550">**État**</span><span class="sxs-lookup"><span data-stu-id="abe44-550">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-551">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-552">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-553">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="abe44-553">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-554">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="abe44-554">Current status of the object.</span></span> <span data-ttu-id="abe44-555">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="abe44-555">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="abe44-556">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="abe44-556">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="abe44-557">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="abe44-557">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="abe44-558">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="abe44-558">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="abe44-559">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="abe44-559">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="abe44-560">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-560">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="abe44-561">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="abe44-561">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="abe44-562">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="abe44-562">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="abe44-563">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="abe44-563">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="abe44-564">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="abe44-564">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abe44-565">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="abe44-565">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="abe44-566">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="abe44-566">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="abe44-567">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="abe44-567">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="abe44-568">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="abe44-568">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="abe44-569">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="abe44-569">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="abe44-570">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="abe44-570">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="abe44-571">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="abe44-571">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="abe44-572">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="abe44-572">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="abe44-573">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="abe44-573">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-574">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="abe44-574">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-575">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abe44-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-576">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-577">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="abe44-577">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-578">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="abe44-578">State of the logical device.</span></span> <span data-ttu-id="abe44-579">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="abe44-579">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="abe44-580">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-580">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="abe44-581">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="abe44-581">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abe44-582">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="abe44-582">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="abe44-583">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="abe44-583">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="abe44-584">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="abe44-584">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="abe44-585">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="abe44-585">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abe44-586">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="abe44-586">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-587">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-588">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-589">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="abe44-589">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="abe44-590">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="abe44-590">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="abe44-591">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-592">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="abe44-592">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-593">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="abe44-593">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-594">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-594">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-595">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| erreur Address")</span><span class="sxs-lookup"><span data-stu-id="abe44-595">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="abe44-596">Si la **valeur est true**, les informations d’adresse dans la propriété **ErrorAddress** sont une adresse de niveau système.</span><span class="sxs-lookup"><span data-stu-id="abe44-596">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="abe44-597">Si la **valeur est false**, il s’agit d’une adresse physique.</span><span class="sxs-lookup"><span data-stu-id="abe44-597">If **False**, it is a physical address.</span></span> <span data-ttu-id="abe44-598">Cette propriété est utilisée uniquement lorsque **errorInfo** n’a pas la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="abe44-598">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="abe44-599">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-599">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe44-600">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="abe44-600">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abe44-601">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abe44-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abe44-602">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abe44-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abe44-603">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="abe44-603">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="abe44-604">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="abe44-604">Name of the scoping system.</span></span>

<span data-ttu-id="abe44-605">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-605">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abe44-606">Notes</span><span class="sxs-lookup"><span data-stu-id="abe44-606">Remarks</span></span>

<span data-ttu-id="abe44-607">La classe **Win32 \_ MemoryArray** est dérivée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="abe44-607">The **Win32\_MemoryArray** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abe44-608">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abe44-608">Requirements</span></span>



| <span data-ttu-id="abe44-609">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abe44-609">Requirement</span></span> | <span data-ttu-id="abe44-610">Valeur</span><span class="sxs-lookup"><span data-stu-id="abe44-610">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abe44-611">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abe44-611">Minimum supported client</span></span><br/> | <span data-ttu-id="abe44-612">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abe44-612">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="abe44-613">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abe44-613">Minimum supported server</span></span><br/> | <span data-ttu-id="abe44-614">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abe44-614">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="abe44-615">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="abe44-615">Namespace</span></span><br/>                | <span data-ttu-id="abe44-616">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="abe44-616">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="abe44-617">MOF</span><span class="sxs-lookup"><span data-stu-id="abe44-617">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abe44-618"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abe44-618"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="abe44-619">DLL</span><span class="sxs-lookup"><span data-stu-id="abe44-619">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abe44-620"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abe44-620"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe44-621">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abe44-621">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe44-622">**\_SMBIOSMemory Win32**</span><span class="sxs-lookup"><span data-stu-id="abe44-622">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="abe44-623">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="abe44-623">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

