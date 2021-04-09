---
description: La \_ classe de mémoire CIM représente les fonctionnalités et la gestion des périphériques logiques liés à la mémoire.
ms.assetid: ddc72aad-5687-4bc1-b402-e27b27eca9be
ms.tgt_platform: multiple
title: CIM_Memory, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Caption
- CIM_Memory.Description
- CIM_Memory.InstallDate
- CIM_Memory.Name
- CIM_Memory.Status
- CIM_Memory.Availability
- CIM_Memory.ConfigManagerErrorCode
- CIM_Memory.ConfigManagerUserConfig
- CIM_Memory.CreationClassName
- CIM_Memory.DeviceID
- CIM_Memory.PowerManagementCapabilities
- CIM_Memory.ErrorCleared
- CIM_Memory.ErrorDescription
- CIM_Memory.LastErrorCode
- CIM_Memory.PNPDeviceID
- CIM_Memory.PowerManagementSupported
- CIM_Memory.StatusInfo
- CIM_Memory.SystemCreationClassName
- CIM_Memory.SystemName
- CIM_Memory.Access
- CIM_Memory.BlockSize
- CIM_Memory.NumberOfBlocks
- CIM_Memory.Purpose
- CIM_Memory.ErrorMethodology
- CIM_Memory.AdditionalErrorData
- CIM_Memory.CorrectableError
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorAddress
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorInfo
- CIM_Memory.ErrorResolution
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorTransferSize
- CIM_Memory.OtherErrorDescription
- CIM_Memory.StartingAddress
- CIM_Memory.SystemLevelAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35fbb8467337da1ceab044a42533a6ca8628cf63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111062"
---
# <a name="cim_memory-class-cimwin32-wmi-providers"></a><span data-ttu-id="9b039-103">CIM_Memory, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9b039-103">CIM_Memory class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9b039-104">La classe de **\_ mémoire CIM** représente les fonctionnalités et la gestion des périphériques logiques liés à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="9b039-104">The **CIM\_Memory** class represents the capabilities and management of memory-related logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b039-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9b039-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b039-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b039-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b039-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9b039-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9b039-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9b039-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b039-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b039-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B64-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
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
};
```

## <a name="members"></a><span data-ttu-id="9b039-110">Membres</span><span class="sxs-lookup"><span data-stu-id="9b039-110">Members</span></span>

<span data-ttu-id="9b039-111">La classe de **\_ mémoire CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9b039-111">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="9b039-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9b039-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9b039-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b039-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9b039-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9b039-114">Methods</span></span>

<span data-ttu-id="9b039-115">La classe de **\_ mémoire CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9b039-115">The **CIM\_Memory** class has these methods.</span></span>



| <span data-ttu-id="9b039-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="9b039-116">Method</span></span>                                                            | <span data-ttu-id="9b039-117">Description</span><span class="sxs-lookup"><span data-stu-id="9b039-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b039-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="9b039-118">**Reset**</span></span>](reset-method-in-class-cim-memory.md)                 | <span data-ttu-id="9b039-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9b039-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="9b039-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="9b039-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9b039-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9b039-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-memory.md) | <span data-ttu-id="9b039-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="9b039-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9b039-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="9b039-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9b039-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b039-124">Properties</span></span>

<span data-ttu-id="9b039-125">La classe de **\_ mémoire CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9b039-125">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b039-126">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="9b039-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b039-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b039-129">Décrit les propriétés en lecture/écriture du média.</span><span class="sxs-lookup"><span data-stu-id="9b039-129">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="9b039-130">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b039-131">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9b039-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="9b039-132">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="9b039-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="9b039-133">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="9b039-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="9b039-134">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="9b039-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="9b039-135">**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="9b039-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b039-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="9b039-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-137">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="9b039-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9b039-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,18 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9b039-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9b039-140">Tableau d’octets qui contiennent des informations d’erreur supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9b039-140">Array of octets that hold additional error information.</span></span> <span data-ttu-id="9b039-141">Par exemple, le syndrome de la vérification et de la correction des erreurs (ECC), ou le retour des bits de vérification si une méthodologie d’erreur basée sur CRC est utilisée.</span><span class="sxs-lookup"><span data-stu-id="9b039-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="9b039-142">Dans ce dernier cas, si une erreur de bit unique est reconnue et que l’algorithme CRC est connu, le bit exact qui a échoué peut être déterminé.</span><span class="sxs-lookup"><span data-stu-id="9b039-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="9b039-143">Ce type de données (syndrome ECC, données de bit de contrôle ou de parité ou autres informations fournies par le fournisseur) est inclus dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="9b039-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="9b039-144">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="9b039-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="9b039-145">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="9b039-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-146">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b039-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9b039-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-149">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9b039-149">Availability and status of the device.</span></span>

<span data-ttu-id="9b039-150">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9b039-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9b039-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b039-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9b039-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9b039-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="9b039-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9b039-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="9b039-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9b039-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="9b039-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9b039-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="9b039-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9b039-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="9b039-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9b039-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="9b039-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9b039-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="9b039-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9b039-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="9b039-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9b039-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="9b039-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9b039-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="9b039-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9b039-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="9b039-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-164">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="9b039-164">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9b039-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="9b039-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-166">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="9b039-166">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9b039-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="9b039-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-168">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="9b039-168">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9b039-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="9b039-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9b039-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="9b039-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-171">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="9b039-171">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9b039-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="9b039-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-173">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="9b039-173">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9b039-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="9b039-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-175">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="9b039-175">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9b039-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="9b039-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-177">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="9b039-177">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9b039-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="9b039-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-179">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="9b039-179">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b039-180">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="9b039-180">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-181">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9b039-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-183">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="9b039-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-184">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="9b039-184">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="9b039-185">Si vous spécifiez une taille de bloc variable, la taille maximale du bloc, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9b039-185">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="9b039-186">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1 (un).</span><span class="sxs-lookup"><span data-stu-id="9b039-186">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="9b039-187">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9b039-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="9b039-188">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-188">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9b039-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-192">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="9b039-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-193">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9b039-193">A short textual description of the object.</span></span>

<span data-ttu-id="9b039-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9b039-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-196">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b039-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-198">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9b039-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-199">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="9b039-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="9b039-200">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9b039-201">**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="9b039-201">**This device is working properly.**</span></span> <span data-ttu-id="9b039-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="9b039-202">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9b039-203">**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="9b039-203">**This device is not configured correctly.**</span></span> <span data-ttu-id="9b039-204">(1)</span><span class="sxs-lookup"><span data-stu-id="9b039-204">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9b039-205">**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-205">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9b039-206">(2)</span><span class="sxs-lookup"><span data-stu-id="9b039-206">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9b039-207">**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="9b039-207">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9b039-208">(3)</span><span class="sxs-lookup"><span data-stu-id="9b039-208">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9b039-209">**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="9b039-209">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9b039-210">(4)</span><span class="sxs-lookup"><span data-stu-id="9b039-210">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9b039-211">**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="9b039-211">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9b039-212">(5)</span><span class="sxs-lookup"><span data-stu-id="9b039-212">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9b039-213">**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="9b039-213">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9b039-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="9b039-214">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9b039-215">**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="9b039-215">**Cannot filter.**</span></span> <span data-ttu-id="9b039-216">(7)</span><span class="sxs-lookup"><span data-stu-id="9b039-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9b039-217">**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="9b039-217">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9b039-218">(8)</span><span class="sxs-lookup"><span data-stu-id="9b039-218">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9b039-219">**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-219">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9b039-220">(9)</span><span class="sxs-lookup"><span data-stu-id="9b039-220">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9b039-221">**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-221">**This device cannot start.**</span></span> <span data-ttu-id="9b039-222">(10)</span><span class="sxs-lookup"><span data-stu-id="9b039-222">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9b039-223">**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-223">**This device failed.**</span></span> <span data-ttu-id="9b039-224">(11)</span><span class="sxs-lookup"><span data-stu-id="9b039-224">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9b039-225">**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="9b039-225">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9b039-226">douze</span><span class="sxs-lookup"><span data-stu-id="9b039-226">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9b039-227">**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-227">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9b039-228">(13)</span><span class="sxs-lookup"><span data-stu-id="9b039-228">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9b039-229">**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="9b039-229">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9b039-230">(14)</span><span class="sxs-lookup"><span data-stu-id="9b039-230">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9b039-231">**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="9b039-231">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9b039-232">(15)</span><span class="sxs-lookup"><span data-stu-id="9b039-232">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9b039-233">**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-233">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9b039-234">(16)</span><span class="sxs-lookup"><span data-stu-id="9b039-234">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9b039-235">**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="9b039-235">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9b039-236">(17)</span><span class="sxs-lookup"><span data-stu-id="9b039-236">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9b039-237">**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-237">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9b039-238">(18)</span><span class="sxs-lookup"><span data-stu-id="9b039-238">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9b039-239">**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="9b039-239">**Failure using the VxD loader.**</span></span> <span data-ttu-id="9b039-240">(19)</span><span class="sxs-lookup"><span data-stu-id="9b039-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9b039-241">**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="9b039-241">**Your registry might be corrupted.**</span></span> <span data-ttu-id="9b039-242">(20)</span><span class="sxs-lookup"><span data-stu-id="9b039-242">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9b039-243">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-243">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9b039-244">(21)</span><span class="sxs-lookup"><span data-stu-id="9b039-244">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9b039-245">**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="9b039-245">**This device is disabled.**</span></span> <span data-ttu-id="9b039-246">(22)</span><span class="sxs-lookup"><span data-stu-id="9b039-246">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9b039-247">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="9b039-247">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9b039-248">(23)</span><span class="sxs-lookup"><span data-stu-id="9b039-248">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9b039-249">**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="9b039-249">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9b039-250">(24)</span><span class="sxs-lookup"><span data-stu-id="9b039-250">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9b039-251">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-251">**Windows is still setting up this device.**</span></span> <span data-ttu-id="9b039-252">(25)</span><span class="sxs-lookup"><span data-stu-id="9b039-252">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9b039-253">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-253">**Windows is still setting up this device.**</span></span> <span data-ttu-id="9b039-254">(26)</span><span class="sxs-lookup"><span data-stu-id="9b039-254">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9b039-255">**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="9b039-255">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9b039-256">(27)</span><span class="sxs-lookup"><span data-stu-id="9b039-256">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9b039-257">**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="9b039-257">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9b039-258">(28)</span><span class="sxs-lookup"><span data-stu-id="9b039-258">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9b039-259">**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="9b039-259">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9b039-260">(29)</span><span class="sxs-lookup"><span data-stu-id="9b039-260">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9b039-261">**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="9b039-261">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9b039-262">(30)</span><span class="sxs-lookup"><span data-stu-id="9b039-262">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9b039-263">**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9b039-263">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9b039-264">31</span><span class="sxs-lookup"><span data-stu-id="9b039-264">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b039-265">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9b039-265">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-266">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9b039-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-268">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9b039-268">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-269">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9b039-269">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9b039-270">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-271">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="9b039-271">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-272">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9b039-272">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-274">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="9b039-274">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-275">Si la **valeur est true**, l’erreur la plus récente était correcte.</span><span class="sxs-lookup"><span data-stu-id="9b039-275">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="9b039-276">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="9b039-276">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="9b039-277">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9b039-277">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-280">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b039-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b039-281">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9b039-281">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9b039-282">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="9b039-282">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9b039-283">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-284">**Description**</span><span class="sxs-lookup"><span data-stu-id="9b039-284">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-285">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-287">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9b039-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-288">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9b039-288">A textual description of the object.</span></span>

<span data-ttu-id="9b039-289">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-289">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-290">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9b039-290">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-291">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-293">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b039-293">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b039-294">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9b039-294">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9b039-295">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-296">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="9b039-296">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-297">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9b039-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-299">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,4 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="9b039-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-300">Adresse de fin référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="9b039-300">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="9b039-301">L’adresse de fin est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="9b039-301">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="9b039-302">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9b039-302">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-303">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="9b039-303">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-304">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b039-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-306">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,15 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="9b039-306">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-307">Opération d’accès à la mémoire qui a provoqué la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="9b039-307">Memory access operation that caused the last error.</span></span> <span data-ttu-id="9b039-308">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="9b039-308">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="9b039-309">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="9b039-309">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9b039-310">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9b039-310">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b039-311">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9b039-311">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="9b039-312">**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="9b039-312">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="9b039-313">**Écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="9b039-313">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="9b039-314">**Écriture partielle** (5)</span><span class="sxs-lookup"><span data-stu-id="9b039-314">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b039-315">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="9b039-315">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-316">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9b039-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-318">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,19 "," MIF. \|Périphérique de mémoire DMTF \| 002,20 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="9b039-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-319">Adresse de la dernière erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9b039-319">Address of the last memory error.</span></span> <span data-ttu-id="9b039-320">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="9b039-320">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="9b039-321">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="9b039-321">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="9b039-322">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9b039-322">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9b039-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-324">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9b039-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b039-326">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="9b039-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9b039-327">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-328">**Partagefichiers**</span><span class="sxs-lookup"><span data-stu-id="9b039-328">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-329">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="9b039-329">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9b039-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-331">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,17 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9b039-331">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9b039-332">Données capturées au cours du dernier accès mémoire erroné.</span><span class="sxs-lookup"><span data-stu-id="9b039-332">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="9b039-333">Les données occupent les *n* premiers octets du tableau qui sont nécessaires pour contenir le nombre de bits spécifié par la propriété **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="9b039-333">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="9b039-334">Si **ErrorTransferSize** est égal à 0, cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="9b039-334">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="9b039-335">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="9b039-335">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-336">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b039-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b039-338">Ordre des données stockées dans la propriété **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="9b039-338">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="9b039-339">Si **ErrorTransferSize** est égal à 0, cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="9b039-339">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b039-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9b039-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-341">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="9b039-341">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="9b039-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Octet le moins significatif en premier** (1)</span><span class="sxs-lookup"><span data-stu-id="9b039-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-343">Octet le moins significatif en premier.</span><span class="sxs-lookup"><span data-stu-id="9b039-343">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="9b039-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Octet le plus significatif en premier** (2)</span><span class="sxs-lookup"><span data-stu-id="9b039-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-345">Octet le plus significatif en premier.</span><span class="sxs-lookup"><span data-stu-id="9b039-345">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b039-346">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9b039-346">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b039-349">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="9b039-349">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9b039-350">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-351">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="9b039-351">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-352">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b039-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-354">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ mémoire CIM**.**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="9b039-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-355">Type d’erreur qui s’est produite le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="9b039-355">Type of error that occurred most recently.</span></span> <span data-ttu-id="9b039-356">Les valeurs 12 à 14 ne sont pas définies dans le schéma CIM, car DMI mélange la sémantique du type d’erreur et indique si elle a été corrigée.</span><span class="sxs-lookup"><span data-stu-id="9b039-356">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="9b039-357">La propriété **CorrectableError** indique si une erreur peut être corrigée.</span><span class="sxs-lookup"><span data-stu-id="9b039-357">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9b039-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9b039-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-359">Autre.</span><span class="sxs-lookup"><span data-stu-id="9b039-359">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b039-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9b039-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-361">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="9b039-361">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9b039-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="9b039-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-363">OK.</span><span class="sxs-lookup"><span data-stu-id="9b039-363">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="9b039-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lecture incorrecte** (4)</span><span class="sxs-lookup"><span data-stu-id="9b039-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-365">Lecture incorrecte.</span><span class="sxs-lookup"><span data-stu-id="9b039-365">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="9b039-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Erreur de parité** (5)</span><span class="sxs-lookup"><span data-stu-id="9b039-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-367">Erreur de parité.</span><span class="sxs-lookup"><span data-stu-id="9b039-367">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="9b039-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Erreur de bit unique** (6)</span><span class="sxs-lookup"><span data-stu-id="9b039-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-369">Erreur sur un bit.</span><span class="sxs-lookup"><span data-stu-id="9b039-369">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="9b039-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Erreur double bit** (7)</span><span class="sxs-lookup"><span data-stu-id="9b039-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-371">Erreur double bit.</span><span class="sxs-lookup"><span data-stu-id="9b039-371">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="9b039-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Erreur multibits** (8)</span><span class="sxs-lookup"><span data-stu-id="9b039-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-373">Erreur multi-bit.</span><span class="sxs-lookup"><span data-stu-id="9b039-373">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="9b039-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Erreur de grignotage** (9)</span><span class="sxs-lookup"><span data-stu-id="9b039-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-375">Erreur de Quartet.</span><span class="sxs-lookup"><span data-stu-id="9b039-375">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="9b039-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Erreur de somme de contrôle** (10)</span><span class="sxs-lookup"><span data-stu-id="9b039-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-377">Erreur de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b039-377">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="9b039-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Erreur CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="9b039-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-379">Erreur CRC.</span><span class="sxs-lookup"><span data-stu-id="9b039-379">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="9b039-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (12)</span><span class="sxs-lookup"><span data-stu-id="9b039-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-381">Non défini.</span><span class="sxs-lookup"><span data-stu-id="9b039-381">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="9b039-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (13)</span><span class="sxs-lookup"><span data-stu-id="9b039-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-383">Non défini.</span><span class="sxs-lookup"><span data-stu-id="9b039-383">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="9b039-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (14)</span><span class="sxs-lookup"><span data-stu-id="9b039-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-385">Non défini.</span><span class="sxs-lookup"><span data-stu-id="9b039-385">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b039-386">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="9b039-386">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-387">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-389">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="9b039-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-390">Indique si la parité ou les algorithmes CRC, ECC ou d’autres mécanismes sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="9b039-390">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="9b039-391">Vous pouvez également fournir des détails sur l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="9b039-391">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="9b039-392">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="9b039-392">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-393">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9b039-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-395">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,21 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="9b039-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-396">Spécifie la plage, en octets, à laquelle la dernière erreur peut être résolue.</span><span class="sxs-lookup"><span data-stu-id="9b039-396">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="9b039-397">Par exemple, si les adresses d’erreurs sont résolues en bit 11 (c’est-à-dire, sur une base de page standard), les erreurs peuvent être résolues en limites de 4 Ko et cette propriété est définie sur 4000.</span><span class="sxs-lookup"><span data-stu-id="9b039-397">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="9b039-398">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="9b039-398">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="9b039-399">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9b039-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-400">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="9b039-400">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-401">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9b039-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b039-403">Date et heure auxquelles la dernière erreur de mémoire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9b039-403">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="9b039-404">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="9b039-404">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="9b039-405">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="9b039-405">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="9b039-406">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="9b039-406">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-407">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b039-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-409">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,16 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="9b039-409">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-410">Taille du transfert de données, en bits, à l’origine de la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="9b039-410">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="9b039-411">La valeur 0 indique qu’il n’y A pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9b039-411">A value of 0 indicates no error.</span></span> <span data-ttu-id="9b039-412">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété doit être définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="9b039-412">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9b039-413">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9b039-413">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-414">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9b039-414">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-416">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="9b039-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-417">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="9b039-417">Indicates when the object was installed.</span></span> <span data-ttu-id="9b039-418">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="9b039-418">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9b039-419">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-419">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-420">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9b039-420">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-421">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b039-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b039-423">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9b039-423">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9b039-424">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-424">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-425">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9b039-425">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-426">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-427">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-428">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9b039-428">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-429">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="9b039-429">Label by which the object is known.</span></span> <span data-ttu-id="9b039-430">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="9b039-430">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9b039-431">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-431">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-432">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="9b039-432">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-433">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9b039-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-435">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="9b039-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-436">Nombre de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="9b039-436">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="9b039-437">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9b039-437">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="9b039-438">Si la valeur de **BlockSize** est 1 (un), cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="9b039-438">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="9b039-439">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9b039-439">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="9b039-440">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-440">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-441">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9b039-441">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-442">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-443">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-444">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ mémoire CIM**.**ErrorInfo**»)</span><span class="sxs-lookup"><span data-stu-id="9b039-444">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-445">Chaîne de forme libre qui fournit des informations si la propriété **ErrorType** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="9b039-445">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="9b039-446">Si elle n’a pas la valeur 1, cette chaîne n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="9b039-446">If it is not set to 1, then this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="9b039-447">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9b039-447">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-448">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-449">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-450">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9b039-450">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-451">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="9b039-451">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="9b039-452">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="9b039-452">Example: "\*PNP030b"</span></span>

<span data-ttu-id="9b039-453">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-454">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9b039-454">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-455">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b039-455">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9b039-456">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b039-457">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="9b039-457">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="9b039-458">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b039-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9b039-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-460">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="9b039-460">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9b039-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="9b039-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-462">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="9b039-462">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9b039-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="9b039-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-464">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="9b039-464">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9b039-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="9b039-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-466">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="9b039-466">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9b039-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="9b039-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-468">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="9b039-468">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9b039-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="9b039-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-470">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9b039-470">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="9b039-471">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="9b039-471">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="9b039-472">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9b039-472">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9b039-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="9b039-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-474">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="9b039-474">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9b039-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="9b039-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9b039-476">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="9b039-476">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b039-477">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9b039-477">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-478">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9b039-478">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-479">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b039-480">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="9b039-480">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9b039-481">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9b039-481">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9b039-482">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9b039-482">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9b039-483">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9b039-483">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9b039-484">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-485">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="9b039-485">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-486">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-486">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b039-488">Chaîne de forme libre qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="9b039-488">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="9b039-489">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-490">**De la**</span><span class="sxs-lookup"><span data-stu-id="9b039-490">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-491">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9b039-491">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-492">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-493">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,3 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="9b039-493">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-494">Adresse de début, référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire, pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="9b039-494">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="9b039-495">L’adresse de départ est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="9b039-495">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="9b039-496">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9b039-496">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-497">**État**</span><span class="sxs-lookup"><span data-stu-id="9b039-497">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-498">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-499">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-500">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9b039-500">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-501">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9b039-501">String that indicates the current status of the object.</span></span> <span data-ttu-id="9b039-502">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="9b039-502">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9b039-503">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="9b039-503">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9b039-504">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="9b039-504">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9b039-505">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="9b039-505">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9b039-506">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="9b039-506">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9b039-507">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="9b039-507">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9b039-508">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-508">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9b039-509">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9b039-509">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9b039-510">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="9b039-510">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9b039-511">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="9b039-511">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9b039-512">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="9b039-512">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b039-513">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="9b039-513">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9b039-514">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="9b039-514">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9b039-515">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="9b039-515">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9b039-516">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="9b039-516">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9b039-517">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="9b039-517">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9b039-518">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="9b039-518">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9b039-519">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="9b039-519">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9b039-520">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="9b039-520">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9b039-521">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="9b039-521">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b039-522">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9b039-522">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-523">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b039-523">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-524">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-525">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9b039-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9b039-526">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9b039-526">State of the logical device.</span></span> <span data-ttu-id="9b039-527">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="9b039-527">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="9b039-528">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9b039-529">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9b039-529">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b039-530">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9b039-530">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9b039-531">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="9b039-531">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9b039-532">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="9b039-532">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9b039-533">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="9b039-533">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b039-534">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9b039-534">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-535">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-536">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-537">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b039-537">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b039-538">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9b039-538">The scoping system's creation class name.</span></span>

<span data-ttu-id="9b039-539">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-539">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b039-540">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="9b039-540">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-541">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9b039-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-542">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b039-543">Indique si les informations d’adresse dans la propriété **ErrorAddress** sont une adresse de niveau système (**true**) ou une adresse physique (**false**).</span><span class="sxs-lookup"><span data-stu-id="9b039-543">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="9b039-544">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="9b039-544">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="9b039-545">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9b039-545">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b039-546">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b039-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b039-547">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b039-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b039-548">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b039-548">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b039-549">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9b039-549">The scoping system's name.</span></span>

<span data-ttu-id="9b039-550">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b039-551">Notes</span><span class="sxs-lookup"><span data-stu-id="9b039-551">Remarks</span></span>

<span data-ttu-id="9b039-552">La classe de **\_ mémoire CIM** est dérivée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-552">The **CIM\_Memory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="9b039-553">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="9b039-553">WMI does not implement this class.</span></span> <span data-ttu-id="9b039-554">Pour les classes qui sont dérivées de la **\_ mémoire CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9b039-554">For classes that are derived from **CIM\_Memory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9b039-555">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9b039-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b039-556">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9b039-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b039-557">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b039-557">Requirements</span></span>



| <span data-ttu-id="9b039-558">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b039-558">Requirement</span></span> | <span data-ttu-id="9b039-559">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b039-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b039-560">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b039-560">Minimum supported client</span></span><br/> | <span data-ttu-id="9b039-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b039-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b039-562">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b039-562">Minimum supported server</span></span><br/> | <span data-ttu-id="9b039-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b039-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b039-564">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9b039-564">Namespace</span></span><br/>                | <span data-ttu-id="9b039-565">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9b039-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b039-566">MOF</span><span class="sxs-lookup"><span data-stu-id="9b039-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b039-567"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b039-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b039-568">DLL</span><span class="sxs-lookup"><span data-stu-id="9b039-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b039-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b039-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b039-570">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b039-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b039-571">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9b039-571">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

