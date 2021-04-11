---
description: La \_ classe WMI MemoryDevice WMI représente les propriétés d’un périphérique de mémoire système de l’ordinateur et de ses adresses mappées associées.
ms.assetid: d609dca5-2f5f-4f23-8fcc-bcc197d6c24b
ms.tgt_platform: multiple
title: Classe Win32_MemoryDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDevice
- Win32_MemoryDevice.Reset
- Win32_MemoryDevice.SetPowerState
- Win32_MemoryDevice.Access
- Win32_MemoryDevice.AdditionalErrorData
- Win32_MemoryDevice.Availability
- Win32_MemoryDevice.BlockSize
- Win32_MemoryDevice.Caption
- Win32_MemoryDevice.ConfigManagerErrorCode
- Win32_MemoryDevice.ConfigManagerUserConfig
- Win32_MemoryDevice.CorrectableError
- Win32_MemoryDevice.CreationClassName
- Win32_MemoryDevice.Description
- Win32_MemoryDevice.DeviceID
- Win32_MemoryDevice.EndingAddress
- Win32_MemoryDevice.ErrorAccess
- Win32_MemoryDevice.ErrorAddress
- Win32_MemoryDevice.ErrorCleared
- Win32_MemoryDevice.ErrorData
- Win32_MemoryDevice.ErrorDataOrder
- Win32_MemoryDevice.ErrorDescription
- Win32_MemoryDevice.ErrorGranularity
- Win32_MemoryDevice.ErrorInfo
- Win32_MemoryDevice.ErrorMethodology
- Win32_MemoryDevice.ErrorResolution
- Win32_MemoryDevice.ErrorTime
- Win32_MemoryDevice.ErrorTransferSize
- Win32_MemoryDevice.InstallDate
- Win32_MemoryDevice.LastErrorCode
- Win32_MemoryDevice.Name
- Win32_MemoryDevice.NumberOfBlocks
- Win32_MemoryDevice.OtherErrorDescription
- Win32_MemoryDevice.PNPDeviceID
- Win32_MemoryDevice.PowerManagementCapabilities
- Win32_MemoryDevice.PowerManagementSupported
- Win32_MemoryDevice.Purpose
- Win32_MemoryDevice.StartingAddress
- Win32_MemoryDevice.Status
- Win32_MemoryDevice.StatusInfo
- Win32_MemoryDevice.SystemCreationClassName
- Win32_MemoryDevice.SystemLevelAddress
- Win32_MemoryDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 277b868f1b92b9f7c6a0c520c77ab76fac6b544d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950480"
---
# <a name="win32_memorydevice-class"></a><span data-ttu-id="0e39e-103">\_Classe MemoryDevice Win32</span><span class="sxs-lookup"><span data-stu-id="0e39e-103">Win32\_MemoryDevice class</span></span>

<span data-ttu-id="0e39e-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryDevice** WMI représente les propriétés d’un périphérique de mémoire système de l’ordinateur et de ses adresses mappées associées.</span><span class="sxs-lookup"><span data-stu-id="0e39e-104">The **Win32\_MemoryDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a computer system memory device and its associated mapped addresses.</span></span>

<span data-ttu-id="0e39e-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0e39e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0e39e-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0e39e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e39e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e39e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDevice : Win32_SMBIOSMemory
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

## <a name="members"></a><span data-ttu-id="0e39e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0e39e-108">Members</span></span>

<span data-ttu-id="0e39e-109">La classe **Win32 \_ MemoryDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e39e-109">The **Win32\_MemoryDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="0e39e-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e39e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0e39e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e39e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0e39e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e39e-112">Methods</span></span>

<span data-ttu-id="0e39e-113">La classe **Win32 \_ MemoryDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0e39e-113">The **Win32\_MemoryDevice** class has these methods.</span></span>



| <span data-ttu-id="0e39e-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="0e39e-114">Method</span></span>            | <span data-ttu-id="0e39e-115">Description</span><span class="sxs-lookup"><span data-stu-id="0e39e-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e39e-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="0e39e-116">**Reset**</span></span>         | <span data-ttu-id="0e39e-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0e39e-117">Not implemented.</span></span> <span data-ttu-id="0e39e-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/>                 |
| <span data-ttu-id="0e39e-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0e39e-119">**SetPowerState**</span></span> | <span data-ttu-id="0e39e-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0e39e-120">Not implemented.</span></span> <span data-ttu-id="0e39e-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0e39e-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e39e-122">Properties</span></span>

<span data-ttu-id="0e39e-123">La classe **Win32 \_ MemoryDevice** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0e39e-123">The **Win32\_MemoryDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e39e-124">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="0e39e-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e39e-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-127">Accès au média disponible.</span><span class="sxs-lookup"><span data-stu-id="0e39e-127">Media access available.</span></span>

<span data-ttu-id="0e39e-128">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e39e-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0e39e-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="0e39e-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="0e39e-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="0e39e-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="0e39e-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-132">Accessible en écriture</span><span class="sxs-lookup"><span data-stu-id="0e39e-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="0e39e-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="0e39e-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="0e39e-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="0e39e-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="0e39e-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-136">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="0e39e-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-138">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory information Error \| syndrome"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0e39e-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-139">Tableau d’informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0e39e-139">Array of additional error information.</span></span> <span data-ttu-id="0e39e-140">Par exemple, le syndrome de la vérification et de la correction des erreurs (ECC), ou le retour des bits de vérification si une méthodologie d’erreur basée sur une vérification de redondance cyclique (CRC) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="0e39e-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based error methodology is used.</span></span> <span data-ttu-id="0e39e-141">Dans ce dernier cas, si une erreur de bit unique est reconnue et que l’algorithme CRC est connu, il est possible de déterminer le bit exact qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="0e39e-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="0e39e-142">Ce type de données (syndrome ECC, bit de vérification, données de bit de parité ou autres informations fournies par le fournisseur) est inclus dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="0e39e-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="0e39e-143">Cette propriété est utilisée uniquement lorsque la propriété **errorInfo** n’est pas égale à 3.</span><span class="sxs-lookup"><span data-stu-id="0e39e-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="0e39e-144">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-145">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="0e39e-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-146">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e39e-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0e39e-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-149">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e39e-149">Availability and status of the device.</span></span>

<span data-ttu-id="0e39e-150">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e39e-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e39e-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e39e-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e39e-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0e39e-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="0e39e-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-154">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="0e39e-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0e39e-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="0e39e-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0e39e-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="0e39e-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0e39e-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="0e39e-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0e39e-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="0e39e-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0e39e-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="0e39e-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0e39e-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="0e39e-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0e39e-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="0e39e-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0e39e-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="0e39e-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0e39e-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="0e39e-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0e39e-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="0e39e-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-165">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="0e39e-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0e39e-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="0e39e-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-167">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="0e39e-167">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0e39e-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="0e39e-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-169">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="0e39e-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0e39e-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="0e39e-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0e39e-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="0e39e-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-172">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="0e39e-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0e39e-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="0e39e-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-174">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="0e39e-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0e39e-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="0e39e-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-176">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="0e39e-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0e39e-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="0e39e-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-178">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="0e39e-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0e39e-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="0e39e-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-180">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="0e39e-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="0e39e-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-182">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e39e-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-184">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="0e39e-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-185">Taille en octets des blocs qui forment cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="0e39e-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="0e39e-186">S’il est inconnu ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1.</span><span class="sxs-lookup"><span data-stu-id="0e39e-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="0e39e-187">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0e39e-188">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e39e-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0e39e-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-192">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-193">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="0e39e-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="0e39e-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0e39e-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-196">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e39e-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-198">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0e39e-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-199">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0e39e-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="0e39e-200">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0e39e-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0e39e-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="0e39e-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-203">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="0e39e-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0e39e-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0e39e-205">(1)</span><span class="sxs-lookup"><span data-stu-id="0e39e-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-206">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="0e39e-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0e39e-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0e39e-208">(2)</span><span class="sxs-lookup"><span data-stu-id="0e39e-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0e39e-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0e39e-210">(3)</span><span class="sxs-lookup"><span data-stu-id="0e39e-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-211">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="0e39e-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0e39e-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0e39e-213">(4)</span><span class="sxs-lookup"><span data-stu-id="0e39e-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-214">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0e39e-214">Device is not working properly.</span></span> <span data-ttu-id="0e39e-215">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="0e39e-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0e39e-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0e39e-217">(5)</span><span class="sxs-lookup"><span data-stu-id="0e39e-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-218">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="0e39e-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0e39e-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0e39e-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="0e39e-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-221">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="0e39e-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0e39e-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0e39e-223">(7)</span><span class="sxs-lookup"><span data-stu-id="0e39e-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0e39e-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0e39e-225">(8)</span><span class="sxs-lookup"><span data-stu-id="0e39e-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-226">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="0e39e-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0e39e-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0e39e-228">(9)</span><span class="sxs-lookup"><span data-stu-id="0e39e-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-229">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0e39e-229">Device is not working properly.</span></span> <span data-ttu-id="0e39e-230">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e39e-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0e39e-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0e39e-232">(10)</span><span class="sxs-lookup"><span data-stu-id="0e39e-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-233">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e39e-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0e39e-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0e39e-235">(11)</span><span class="sxs-lookup"><span data-stu-id="0e39e-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-236">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e39e-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0e39e-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0e39e-238">douze</span><span class="sxs-lookup"><span data-stu-id="0e39e-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-239">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0e39e-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0e39e-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0e39e-241">(13)</span><span class="sxs-lookup"><span data-stu-id="0e39e-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-242">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e39e-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0e39e-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0e39e-244">(14)</span><span class="sxs-lookup"><span data-stu-id="0e39e-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-245">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="0e39e-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0e39e-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0e39e-247">(15)</span><span class="sxs-lookup"><span data-stu-id="0e39e-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-248">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="0e39e-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0e39e-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0e39e-250">(16)</span><span class="sxs-lookup"><span data-stu-id="0e39e-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-251">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e39e-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0e39e-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0e39e-253">(17)</span><span class="sxs-lookup"><span data-stu-id="0e39e-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-254">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="0e39e-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0e39e-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0e39e-256">(18)</span><span class="sxs-lookup"><span data-stu-id="0e39e-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-257">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="0e39e-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0e39e-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0e39e-259">(19)</span><span class="sxs-lookup"><span data-stu-id="0e39e-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0e39e-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0e39e-261">(20)</span><span class="sxs-lookup"><span data-stu-id="0e39e-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-262">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="0e39e-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0e39e-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0e39e-264">(21)</span><span class="sxs-lookup"><span data-stu-id="0e39e-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-265">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="0e39e-265">System failure.</span></span> <span data-ttu-id="0e39e-266">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="0e39e-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0e39e-267">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e39e-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0e39e-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0e39e-269">(22)</span><span class="sxs-lookup"><span data-stu-id="0e39e-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-270">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="0e39e-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0e39e-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0e39e-272">(23)</span><span class="sxs-lookup"><span data-stu-id="0e39e-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-273">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="0e39e-273">System failure.</span></span> <span data-ttu-id="0e39e-274">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="0e39e-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0e39e-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0e39e-276">(24)</span><span class="sxs-lookup"><span data-stu-id="0e39e-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-277">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="0e39e-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0e39e-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0e39e-279">(25)</span><span class="sxs-lookup"><span data-stu-id="0e39e-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-280">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e39e-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0e39e-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0e39e-282">(26)</span><span class="sxs-lookup"><span data-stu-id="0e39e-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-283">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e39e-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0e39e-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0e39e-285">(27)</span><span class="sxs-lookup"><span data-stu-id="0e39e-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-286">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="0e39e-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0e39e-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0e39e-288">(28)</span><span class="sxs-lookup"><span data-stu-id="0e39e-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-289">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="0e39e-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0e39e-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0e39e-291">(29)</span><span class="sxs-lookup"><span data-stu-id="0e39e-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-292">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="0e39e-292">Device is disabled.</span></span> <span data-ttu-id="0e39e-293">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="0e39e-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0e39e-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0e39e-295">(30)</span><span class="sxs-lookup"><span data-stu-id="0e39e-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-296">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="0e39e-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0e39e-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e39e-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0e39e-298">31</span><span class="sxs-lookup"><span data-stu-id="0e39e-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-299">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0e39e-299">Device is not working properly.</span></span> <span data-ttu-id="0e39e-300">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="0e39e-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0e39e-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-302">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e39e-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-304">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0e39e-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-305">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e39e-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0e39e-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-307">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="0e39e-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-308">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e39e-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-310">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| type erreur")</span><span class="sxs-lookup"><span data-stu-id="0e39e-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-311">Si la **valeur est true**, l’erreur la plus récente était correcte.</span><span class="sxs-lookup"><span data-stu-id="0e39e-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="0e39e-312">Cette propriété n’est pas utilisée si **errorInfo** a la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="0e39e-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="0e39e-313">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e39e-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-317">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e39e-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-318">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0e39e-318">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0e39e-319">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="0e39e-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0e39e-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-321">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e39e-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-324">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0e39e-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-325">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e39e-325">Description of the object.</span></span>

<span data-ttu-id="0e39e-326">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0e39e-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-330">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« DeviceID »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-331">Identificateur unique du périphérique de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0e39e-331">Unique identifier of the memory device.</span></span>

<span data-ttu-id="0e39e-332">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0e39e-333">Exemple : « Memory Device 1 »</span><span class="sxs-lookup"><span data-stu-id="0e39e-333">Example: "Memory Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-334">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="0e39e-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-335">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e39e-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-337">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 19 \| Memory Device deviced \| Addresss fin Address")</span><span class="sxs-lookup"><span data-stu-id="0e39e-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-338">Adresse de fin référencée par une application ou un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0e39e-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="0e39e-339">Cette adresse mémoire est mappée par un contrôleur de mémoire pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="0e39e-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="0e39e-340">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-340">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="0e39e-341">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e39e-341">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-342">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="0e39e-342">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-343">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e39e-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-345">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| erreur Operation")</span><span class="sxs-lookup"><span data-stu-id="0e39e-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-346">Type d’opération d’accès mémoire à l’origine de la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="0e39e-346">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="0e39e-347">Cette propriété est valide uniquement lorsque **errorInfo** n’a pas la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="0e39e-347">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="0e39e-348">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-348">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e39e-349">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e39e-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e39e-350">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e39e-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="0e39e-351">**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="0e39e-351">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="0e39e-352">**Écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="0e39e-352">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="0e39e-353">**Écriture partielle** (5)</span><span class="sxs-lookup"><span data-stu-id="0e39e-353">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-354">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="0e39e-354">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-355">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e39e-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-357">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| erreur Address")</span><span class="sxs-lookup"><span data-stu-id="0e39e-357">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-358">Adresse de la dernière erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0e39e-358">Address of the last memory error.</span></span> <span data-ttu-id="0e39e-359">Cette propriété est utilisée uniquement lorsque **errorInfo** n’a pas la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="0e39e-359">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="0e39e-360">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-360">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="0e39e-361">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e39e-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-362">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0e39e-362">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-363">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e39e-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-365">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="0e39e-365">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="0e39e-366">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-367">**Partagefichiers**</span><span class="sxs-lookup"><span data-stu-id="0e39e-367">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-368">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="0e39e-368">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-370">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0e39e-370">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-371">Tableau de données capturées à partir du dernier accès mémoire avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="0e39e-371">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="0e39e-372">Les données occupent les *n* premiers octets du tableau nécessaire pour contenir le nombre de bits spécifié par la propriété **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="0e39e-372">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="0e39e-373">Si **ErrorTransferSize** est égal à 0 (zéro), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0e39e-373">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="0e39e-374">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-374">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-375">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="0e39e-375">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-376">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e39e-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-378">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-378">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-379">Classement des données stockées dans la propriété **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="0e39e-379">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="0e39e-380">Cette propriété est utilisée uniquement lorsque **ErrorTransferSize** est égal à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="0e39e-380">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="0e39e-381">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-381">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e39e-382">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0e39e-382">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="0e39e-383">**Octet le moins significatif en premier** (1)</span><span class="sxs-lookup"><span data-stu-id="0e39e-383">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="0e39e-384">**Octet le plus significatif en premier** (2)</span><span class="sxs-lookup"><span data-stu-id="0e39e-384">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-385">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0e39e-385">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-386">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-388">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="0e39e-388">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="0e39e-389">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-390">**ErrorGranularity**</span><span class="sxs-lookup"><span data-stu-id="0e39e-390">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-391">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e39e-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-393">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| Error finesse")</span><span class="sxs-lookup"><span data-stu-id="0e39e-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-394">Niveau où l’erreur peut être résolue.</span><span class="sxs-lookup"><span data-stu-id="0e39e-394">Level where the error can be resolved.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e39e-395">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e39e-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e39e-396">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e39e-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_level"></span><span id="device_level"></span><span id="DEVICE_LEVEL"></span>

<span data-ttu-id="0e39e-397">**Niveau** de l’appareil (3)</span><span class="sxs-lookup"><span data-stu-id="0e39e-397">**Device level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_partition_level"></span><span id="memory_partition_level"></span><span id="MEMORY_PARTITION_LEVEL"></span>

<span data-ttu-id="0e39e-398">**Niveau** de la partition de mémoire (4)</span><span class="sxs-lookup"><span data-stu-id="0e39e-398">**Memory partition level** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-399">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="0e39e-399">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-400">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e39e-400">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-401">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-402">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ mémoire CIM**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS \| type 18 \| 32-bit Memory Error information \| type erreur ")</span><span class="sxs-lookup"><span data-stu-id="0e39e-402">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-403">Type d’erreur qui s’est produite le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="0e39e-403">Type of error that occurred most recently.</span></span> <span data-ttu-id="0e39e-404">Les valeurs 12-14, indiquant si une erreur peut être corrigée, ne sont pas utilisées avec cette propriété, mais ces informations se trouvent dans la propriété **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="0e39e-404">The values 12-14, indicating whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="0e39e-405">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-405">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e39e-406">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e39e-406">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e39e-407">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e39e-407">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0e39e-408">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="0e39e-408">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="0e39e-409">**Lecture incorrecte** (4)</span><span class="sxs-lookup"><span data-stu-id="0e39e-409">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="0e39e-410">**Erreur de parité** (5)</span><span class="sxs-lookup"><span data-stu-id="0e39e-410">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="0e39e-411">**Erreur de bit unique** (6)</span><span class="sxs-lookup"><span data-stu-id="0e39e-411">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="0e39e-412">**Erreur double bit** (7)</span><span class="sxs-lookup"><span data-stu-id="0e39e-412">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="0e39e-413">**Erreur multibits** (8)</span><span class="sxs-lookup"><span data-stu-id="0e39e-413">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="0e39e-414">**Erreur de grignotage** (9)</span><span class="sxs-lookup"><span data-stu-id="0e39e-414">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="0e39e-415">**Erreur de somme de contrôle** (10)</span><span class="sxs-lookup"><span data-stu-id="0e39e-415">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="0e39e-416">**Erreur CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="0e39e-416">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="0e39e-417">**Erreur de correction sur un bit** (12)</span><span class="sxs-lookup"><span data-stu-id="0e39e-417">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="0e39e-418">**Erreur corrigée** (13)</span><span class="sxs-lookup"><span data-stu-id="0e39e-418">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="0e39e-419">**Erreur** impossible à corriger (14)</span><span class="sxs-lookup"><span data-stu-id="0e39e-419">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-420">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="0e39e-420">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-421">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-423">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| type d’erreur de \| mémoire physique du groupe de mémoire physique de type SMBIOS \| ")</span><span class="sxs-lookup"><span data-stu-id="0e39e-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-424">Types de contrôle d’erreur utilisés par le matériel de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0e39e-424">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="0e39e-425">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-425">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0e39e-426">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="0e39e-426">The values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e39e-427">**Autre** (« autre »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-427">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e39e-428">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="0e39e-428">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="0e39e-429">**Parité** (« parité »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-429">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="0e39e-430">**ECC sur** un bit (ECC sur un bit)</span><span class="sxs-lookup"><span data-stu-id="0e39e-430">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="0e39e-431">**ECC multi-bits** (« ECC multi-bits »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-431">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="0e39e-432">**Aucun** (« aucun »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-432">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="0e39e-433">**CRC** (« CRC »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-433">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-434">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="0e39e-434">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-435">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e39e-435">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-436">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-437">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| résolution d’erreur"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="0e39e-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-438">Quantité de données réellement déterminées pour provoquer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0e39e-438">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="0e39e-439">Cette propriété n’est pas utilisée lorsque la propriété **errorInfo** a la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="0e39e-439">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="0e39e-440">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-440">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="0e39e-441">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e39e-441">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-442">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="0e39e-442">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-443">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e39e-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-445">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-445">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-446">Heure à laquelle la dernière erreur de mémoire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0e39e-446">Time that the last memory error occurred.</span></span> <span data-ttu-id="0e39e-447">Cette propriété est valide uniquement lorsque **errorInfo** n’a pas la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="0e39e-447">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="0e39e-448">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-448">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-449">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="0e39e-449">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-450">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e39e-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-452">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="0e39e-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-453">Taille des données (contenant la dernière erreur) en cours de transfert.</span><span class="sxs-lookup"><span data-stu-id="0e39e-453">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="0e39e-454">Cette propriété a la valeur 0 (zéro) s’il n’y a pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0e39e-454">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="0e39e-455">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-455">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-456">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0e39e-456">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-457">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e39e-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-458">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-459">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="0e39e-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-460">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e39e-460">Date and time the object was installed.</span></span> <span data-ttu-id="0e39e-461">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="0e39e-461">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0e39e-462">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-462">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-463">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0e39e-463">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-464">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e39e-464">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-465">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-466">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0e39e-466">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0e39e-467">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-468">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0e39e-468">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-469">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-471">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0e39e-471">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-472">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="0e39e-472">Label by which the object is known.</span></span> <span data-ttu-id="0e39e-473">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="0e39e-473">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0e39e-474">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-474">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-475">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="0e39e-475">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-476">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e39e-476">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-478">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="0e39e-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-479">Nombre total de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forme cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="0e39e-479">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="0e39e-480">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0e39e-480">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="0e39e-481">Si la valeur de **BlockSize** est 1, cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="0e39e-481">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="0e39e-482">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-482">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0e39e-483">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e39e-483">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-484">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0e39e-484">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-485">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-486">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-487">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ mémoire CIM**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="0e39e-487">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-488">Plus d’informations lorsque la propriété **errorInfo** est définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="0e39e-488">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="0e39e-489">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-489">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-490">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0e39e-490">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-491">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-492">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-493">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0e39e-493">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-494">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0e39e-494">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0e39e-495">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-495">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0e39e-496">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="0e39e-496">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-497">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0e39e-497">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-498">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e39e-498">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-499">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-500">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="0e39e-500">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0e39e-501">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="0e39e-501">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e39e-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0e39e-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0e39e-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="0e39e-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0e39e-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="0e39e-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0e39e-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="0e39e-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-506">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="0e39e-506">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0e39e-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="0e39e-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-508">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="0e39e-508">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0e39e-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="0e39e-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-510">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0e39e-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0e39e-511">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="0e39e-511">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="0e39e-512">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0e39e-512">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0e39e-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="0e39e-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-514">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="0e39e-514">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0e39e-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="0e39e-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0e39e-516">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e39e-516">Timed Power-On Supported</span></span>

<span data-ttu-id="0e39e-517">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="0e39e-517">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-518">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0e39e-518">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-519">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e39e-519">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-520">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-520">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-521">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="0e39e-521">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="0e39e-522">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="0e39e-522">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="0e39e-523">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-524">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="0e39e-524">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-525">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-526">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-527">Chaîne de forme libre décrivant le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="0e39e-527">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="0e39e-528">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-528">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-529">**De la**</span><span class="sxs-lookup"><span data-stu-id="0e39e-529">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-530">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e39e-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-531">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-532">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 19 \| Memory Device mapped \| Addresss Start Address")</span><span class="sxs-lookup"><span data-stu-id="0e39e-532">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-533">Adresse de début référencée par une application ou le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0e39e-533">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="0e39e-534">Cette adresse mémoire est mappée par un contrôleur de mémoire pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="0e39e-534">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="0e39e-535">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-535">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="0e39e-536">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e39e-536">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-537">**État**</span><span class="sxs-lookup"><span data-stu-id="0e39e-537">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-538">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-539">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-540">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0e39e-540">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-541">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e39e-541">Current status of the object.</span></span> <span data-ttu-id="0e39e-542">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="0e39e-542">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0e39e-543">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="0e39e-543">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0e39e-544">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="0e39e-544">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0e39e-545">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="0e39e-545">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0e39e-546">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="0e39e-546">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0e39e-547">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-547">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0e39e-548">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e39e-548">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0e39e-549">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-549">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0e39e-550">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-550">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0e39e-551">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-551">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e39e-552">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="0e39e-552">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0e39e-553">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-553">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0e39e-554">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-554">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0e39e-555">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-555">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0e39e-556">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-556">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0e39e-557">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-557">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0e39e-558">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-558">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0e39e-559">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-559">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0e39e-560">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="0e39e-560">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-561">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0e39e-561">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-562">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e39e-562">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-563">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-563">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-564">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0e39e-564">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-565">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0e39e-565">State of the logical device.</span></span> <span data-ttu-id="0e39e-566">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="0e39e-566">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0e39e-567">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-567">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e39e-568">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e39e-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e39e-569">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e39e-569">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0e39e-570">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="0e39e-570">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0e39e-571">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="0e39e-571">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0e39e-572">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="0e39e-572">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39e-573">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e39e-573">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-574">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-575">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-575">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-576">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e39e-576">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-577">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0e39e-577">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="0e39e-578">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-578">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-579">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="0e39e-579">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-580">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e39e-580">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-581">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-582">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 18 \| 32-bit Memory Error information \| erreur Address")</span><span class="sxs-lookup"><span data-stu-id="0e39e-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-583">Si la **valeur est true**, les informations d’adresse dans la propriété **ErrorAddress** sont une adresse de niveau système.</span><span class="sxs-lookup"><span data-stu-id="0e39e-583">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="0e39e-584">Si la **valeur est false**, il s’agit d’une adresse physique.</span><span class="sxs-lookup"><span data-stu-id="0e39e-584">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="0e39e-585">Cette propriété est utilisée uniquement lorsque **errorInfo** n’a pas la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="0e39e-585">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="0e39e-586">Cette propriété est héritée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-586">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e39e-587">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0e39e-587">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39e-588">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e39e-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-589">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e39e-589">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e39e-590">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e39e-590">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e39e-591">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0e39e-591">Name of the scoping system.</span></span>

<span data-ttu-id="0e39e-592">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-592">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e39e-593">Notes</span><span class="sxs-lookup"><span data-stu-id="0e39e-593">Remarks</span></span>

<span data-ttu-id="0e39e-594">La classe **Win32 \_ MemoryDevice** est dérivée de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="0e39e-594">The **Win32\_MemoryDevice** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0e39e-595">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e39e-595">Examples</span></span>

<span data-ttu-id="0e39e-596">L’exemple perl [List Memory Devices](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) retourne les adresses de début et de fin pour tous les périphériques de mémoire installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0e39e-596">The [List Memory Devices](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) Perl sample returns starting and ending addresses for all memory devices installed on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e39e-597">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e39e-597">Requirements</span></span>



| <span data-ttu-id="0e39e-598">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e39e-598">Requirement</span></span> | <span data-ttu-id="0e39e-599">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e39e-599">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e39e-600">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e39e-600">Minimum supported client</span></span><br/> | <span data-ttu-id="0e39e-601">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e39e-601">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e39e-602">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e39e-602">Minimum supported server</span></span><br/> | <span data-ttu-id="0e39e-603">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e39e-603">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e39e-604">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e39e-604">Namespace</span></span><br/>                | <span data-ttu-id="0e39e-605">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0e39e-605">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e39e-606">MOF</span><span class="sxs-lookup"><span data-stu-id="0e39e-606">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e39e-607"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e39e-607"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e39e-608">DLL</span><span class="sxs-lookup"><span data-stu-id="0e39e-608">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e39e-609"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e39e-609"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e39e-610">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e39e-610">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e39e-611">**\_SMBIOSMemory Win32**</span><span class="sxs-lookup"><span data-stu-id="0e39e-611">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="0e39e-612">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="0e39e-612">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

