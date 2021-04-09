---
description: La \_ classe CIM VolatileStorage représente les fonctionnalités et la gestion du stockage volatile.
ms.assetid: c2f7e11e-d7e4-4709-be55-1c94a0b14010
ms.tgt_platform: multiple
title: Classe CIM_VolatileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolatileStorage
- CIM_VolatileStorage.Access
- CIM_VolatileStorage.AdditionalErrorData
- CIM_VolatileStorage.Availability
- CIM_VolatileStorage.BlockSize
- CIM_VolatileStorage.Cacheable
- CIM_VolatileStorage.CacheType
- CIM_VolatileStorage.Caption
- CIM_VolatileStorage.ConfigManagerErrorCode
- CIM_VolatileStorage.ConfigManagerUserConfig
- CIM_VolatileStorage.CorrectableError
- CIM_VolatileStorage.CreationClassName
- CIM_VolatileStorage.Description
- CIM_VolatileStorage.DeviceID
- CIM_VolatileStorage.EndingAddress
- CIM_VolatileStorage.ErrorAccess
- CIM_VolatileStorage.ErrorAddress
- CIM_VolatileStorage.ErrorCleared
- CIM_VolatileStorage.ErrorData
- CIM_VolatileStorage.ErrorDataOrder
- CIM_VolatileStorage.ErrorDescription
- CIM_VolatileStorage.ErrorInfo
- CIM_VolatileStorage.ErrorMethodology
- CIM_VolatileStorage.ErrorResolution
- CIM_VolatileStorage.ErrorTime
- CIM_VolatileStorage.ErrorTransferSize
- CIM_VolatileStorage.InstallDate
- CIM_VolatileStorage.LastErrorCode
- CIM_VolatileStorage.Name
- CIM_VolatileStorage.NumberOfBlocks
- CIM_VolatileStorage.OtherErrorDescription
- CIM_VolatileStorage.PNPDeviceID
- CIM_VolatileStorage.PowerManagementCapabilities
- CIM_VolatileStorage.PowerManagementSupported
- CIM_VolatileStorage.Purpose
- CIM_VolatileStorage.StartingAddress
- CIM_VolatileStorage.Status
- CIM_VolatileStorage.StatusInfo
- CIM_VolatileStorage.SystemCreationClassName
- CIM_VolatileStorage.SystemLevelAddress
- CIM_VolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99add7401d92d82385a4182e466de8b28ad4fc09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860737"
---
# <a name="cim_volatilestorage-class"></a><span data-ttu-id="18752-103">\_Classe CIM VolatileStorage</span><span class="sxs-lookup"><span data-stu-id="18752-103">CIM\_VolatileStorage class</span></span>

<span data-ttu-id="18752-104">La classe **CIM \_ VolatileStorage** représente les fonctionnalités et la gestion du stockage volatile.</span><span class="sxs-lookup"><span data-stu-id="18752-104">The **CIM\_VolatileStorage** class represents the capabilities and management of volatile storage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18752-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="18752-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="18752-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="18752-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="18752-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="18752-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="18752-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="18752-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="18752-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18752-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36851DFE-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_VolatileStorage : CIM_Memory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  boolean  Cacheable;
  uint16   CacheType;
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
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="18752-110">Membres</span><span class="sxs-lookup"><span data-stu-id="18752-110">Members</span></span>

<span data-ttu-id="18752-111">La classe **CIM \_ VolatileStorage** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="18752-111">The **CIM\_VolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="18752-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="18752-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="18752-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18752-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18752-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="18752-114">Methods</span></span>

<span data-ttu-id="18752-115">La classe **CIM \_ VolatileStorage** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="18752-115">The **CIM\_VolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="18752-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="18752-116">Method</span></span>                                                                     | <span data-ttu-id="18752-117">Description</span><span class="sxs-lookup"><span data-stu-id="18752-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18752-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="18752-118">**Reset**</span></span>](reset-method-in-class-cim-volatilestorage.md)                 | <span data-ttu-id="18752-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18752-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="18752-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="18752-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="18752-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="18752-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volatilestorage.md) | <span data-ttu-id="18752-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="18752-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="18752-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="18752-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="18752-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18752-124">Properties</span></span>

<span data-ttu-id="18752-125">La classe **CIM \_ VolatileStorage** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="18752-125">The **CIM\_VolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18752-126">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="18752-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18752-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18752-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18752-129">Propriétés de lecture/écriture du média.</span><span class="sxs-lookup"><span data-stu-id="18752-129">Read/write properties of the media.</span></span>

<span data-ttu-id="18752-130">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18752-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18752-131">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="18752-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="18752-132">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="18752-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="18752-133">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="18752-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="18752-134">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="18752-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="18752-135">**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="18752-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18752-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="18752-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-137">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="18752-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="18752-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,18 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="18752-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="18752-140">Informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="18752-140">Additional error information.</span></span> <span data-ttu-id="18752-141">Par exemple, le syndrome de la vérification et de la correction des erreurs (ECC), ou le retour des bits de vérification si une méthodologie d’erreur basée sur CRC est utilisée.</span><span class="sxs-lookup"><span data-stu-id="18752-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="18752-142">Dans ce dernier cas, si une erreur de bit unique est reconnue et que l’algorithme CRC est connu, le bit exact qui a échoué peut être déterminé.</span><span class="sxs-lookup"><span data-stu-id="18752-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="18752-143">Ce type de données (syndrome ECC, données de bit de contrôle ou de parité ou autres informations fournies par le fournisseur) est inclus dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="18752-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="18752-144">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="18752-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="18752-145">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-145">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-146">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="18752-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-147">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18752-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18752-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-149">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="18752-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="18752-150">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18752-150">Availability and status of the device.</span></span>

<span data-ttu-id="18752-151">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18752-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="18752-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18752-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="18752-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="18752-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="18752-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18752-155">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="18752-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="18752-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="18752-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="18752-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="18752-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="18752-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="18752-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="18752-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="18752-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="18752-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="18752-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="18752-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="18752-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18752-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="18752-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="18752-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="18752-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="18752-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="18752-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="18752-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="18752-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="18752-166">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="18752-166">The device is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="18752-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="18752-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="18752-168">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="18752-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="18752-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="18752-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="18752-170">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="18752-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="18752-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="18752-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="18752-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="18752-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="18752-173">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="18752-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="18752-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="18752-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="18752-175">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="18752-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="18752-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="18752-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="18752-177">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="18752-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="18752-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="18752-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="18752-179">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="18752-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="18752-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="18752-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="18752-181">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="18752-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18752-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="18752-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-183">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18752-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18752-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-185">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="18752-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="18752-186">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="18752-186">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="18752-187">Si vous spécifiez une taille de bloc variable, la taille maximale du bloc, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="18752-187">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="18752-188">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1 (un).</span><span class="sxs-lookup"><span data-stu-id="18752-188">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="18752-189">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18752-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="18752-190">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="18752-190">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="18752-191">**Pouvant être mis en cache**</span><span class="sxs-lookup"><span data-stu-id="18752-191">**Cacheable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-192">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18752-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18752-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-194">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations sur la mémoire des ressources système DMTF \| 001,5»)</span><span class="sxs-lookup"><span data-stu-id="18752-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="18752-195">Si la **valeur est true**, cette mémoire peut être mise en cache.</span><span class="sxs-lookup"><span data-stu-id="18752-195">If **TRUE**, this memory can be cached.</span></span>

</dd> <dt>

<span data-ttu-id="18752-196">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="18752-196">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-197">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18752-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18752-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-199">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations sur la mémoire des ressources système DMTF \| 001,6»)</span><span class="sxs-lookup"><span data-stu-id="18752-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="18752-200">Type de cache qui est compatible avec la mémoire.</span><span class="sxs-lookup"><span data-stu-id="18752-200">Cache type that is compatible with the memory.</span></span> <span data-ttu-id="18752-201">Si la propriété **cacheable** est définie sur **false**, cette propriété n’a pas de signification et doit être définie sur 4 (« non applicable »).</span><span class="sxs-lookup"><span data-stu-id="18752-201">If the **Cacheable** property is set to **FALSE**, then this property does not have meaning and should be set to 4 ("Not Applicable").</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18752-202">**Autre** (0)</span><span class="sxs-lookup"><span data-stu-id="18752-202">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18752-203">**Inconnu** (1)</span><span class="sxs-lookup"><span data-stu-id="18752-203">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Back"></span><span id="write-back"></span><span id="WRITE-BACK"></span>

<span data-ttu-id="18752-204">**Écriture différée** (2)</span><span class="sxs-lookup"><span data-stu-id="18752-204">**Write-Back** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Through"></span><span id="write-through"></span><span id="WRITE-THROUGH"></span>

<span data-ttu-id="18752-205">**Écriture** (3)</span><span class="sxs-lookup"><span data-stu-id="18752-205">**Write-Through** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="18752-206">**Non applicable** (4)</span><span class="sxs-lookup"><span data-stu-id="18752-206">**Not Applicable** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18752-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="18752-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-210">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="18752-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="18752-211">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18752-211">Short textual description of the object.</span></span>

<span data-ttu-id="18752-212">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18752-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-213">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18752-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-214">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18752-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18752-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-216">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18752-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18752-217">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="18752-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="18752-218">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="18752-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="18752-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="18752-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="18752-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="18752-221">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="18752-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="18752-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="18752-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="18752-223">(1)</span><span class="sxs-lookup"><span data-stu-id="18752-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="18752-224">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="18752-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18752-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="18752-226">(2)</span><span class="sxs-lookup"><span data-stu-id="18752-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="18752-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="18752-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="18752-228">(3)</span><span class="sxs-lookup"><span data-stu-id="18752-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="18752-229">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="18752-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="18752-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="18752-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="18752-231">(4)</span><span class="sxs-lookup"><span data-stu-id="18752-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="18752-232">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="18752-232">Device is not working properly.</span></span> <span data-ttu-id="18752-233">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="18752-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="18752-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="18752-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="18752-235">(5)</span><span class="sxs-lookup"><span data-stu-id="18752-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="18752-236">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="18752-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="18752-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="18752-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="18752-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="18752-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="18752-239">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="18752-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="18752-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="18752-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="18752-241">(7)</span><span class="sxs-lookup"><span data-stu-id="18752-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="18752-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="18752-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="18752-243">(8)</span><span class="sxs-lookup"><span data-stu-id="18752-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="18752-244">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="18752-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="18752-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="18752-246">(9)</span><span class="sxs-lookup"><span data-stu-id="18752-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="18752-247">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="18752-247">Device is not working properly.</span></span> <span data-ttu-id="18752-248">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18752-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="18752-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="18752-250">(10)</span><span class="sxs-lookup"><span data-stu-id="18752-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="18752-251">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18752-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="18752-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="18752-253">(11)</span><span class="sxs-lookup"><span data-stu-id="18752-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="18752-254">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18752-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="18752-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="18752-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="18752-256">douze</span><span class="sxs-lookup"><span data-stu-id="18752-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="18752-257">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="18752-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="18752-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="18752-259">(13)</span><span class="sxs-lookup"><span data-stu-id="18752-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="18752-260">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18752-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="18752-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="18752-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="18752-262">(14)</span><span class="sxs-lookup"><span data-stu-id="18752-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="18752-263">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="18752-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="18752-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="18752-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="18752-265">(15)</span><span class="sxs-lookup"><span data-stu-id="18752-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="18752-266">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="18752-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="18752-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="18752-268">(16)</span><span class="sxs-lookup"><span data-stu-id="18752-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="18752-269">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18752-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="18752-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="18752-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="18752-271">(17)</span><span class="sxs-lookup"><span data-stu-id="18752-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="18752-272">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="18752-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18752-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="18752-274">(18)</span><span class="sxs-lookup"><span data-stu-id="18752-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="18752-275">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="18752-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="18752-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="18752-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="18752-277">(19)</span><span class="sxs-lookup"><span data-stu-id="18752-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="18752-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="18752-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="18752-279">(20)</span><span class="sxs-lookup"><span data-stu-id="18752-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="18752-280">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="18752-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="18752-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="18752-282">(21)</span><span class="sxs-lookup"><span data-stu-id="18752-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="18752-283">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="18752-283">System failure.</span></span> <span data-ttu-id="18752-284">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="18752-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="18752-285">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18752-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="18752-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="18752-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="18752-287">(22)</span><span class="sxs-lookup"><span data-stu-id="18752-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="18752-288">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="18752-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="18752-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="18752-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="18752-290">(23)</span><span class="sxs-lookup"><span data-stu-id="18752-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="18752-291">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="18752-291">System failure.</span></span> <span data-ttu-id="18752-292">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="18752-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="18752-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="18752-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="18752-294">(24)</span><span class="sxs-lookup"><span data-stu-id="18752-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="18752-295">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="18752-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="18752-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="18752-297">(25)</span><span class="sxs-lookup"><span data-stu-id="18752-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="18752-298">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18752-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="18752-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="18752-300">(26)</span><span class="sxs-lookup"><span data-stu-id="18752-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="18752-301">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18752-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="18752-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="18752-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="18752-303">(27)</span><span class="sxs-lookup"><span data-stu-id="18752-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="18752-304">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="18752-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="18752-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="18752-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="18752-306">(28)</span><span class="sxs-lookup"><span data-stu-id="18752-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="18752-307">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="18752-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="18752-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="18752-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="18752-309">(29)</span><span class="sxs-lookup"><span data-stu-id="18752-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="18752-310">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="18752-310">Device is disabled.</span></span> <span data-ttu-id="18752-311">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="18752-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="18752-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="18752-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="18752-313">(30)</span><span class="sxs-lookup"><span data-stu-id="18752-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="18752-314">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="18752-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18752-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18752-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="18752-316">31</span><span class="sxs-lookup"><span data-stu-id="18752-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="18752-317">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="18752-317">Device is not working properly.</span></span> <span data-ttu-id="18752-318">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="18752-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18752-319">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="18752-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-320">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18752-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18752-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-322">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18752-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18752-323">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18752-323">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="18752-324">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-325">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="18752-325">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-326">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18752-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18752-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-328">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="18752-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="18752-329">Si la **valeur est true**, l’erreur la plus récente était correcte.</span><span class="sxs-lookup"><span data-stu-id="18752-329">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="18752-330">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="18752-330">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="18752-331">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-331">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18752-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-335">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="18752-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="18752-336">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="18752-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="18752-337">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="18752-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="18752-338">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-339">**Description**</span><span class="sxs-lookup"><span data-stu-id="18752-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-342">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="18752-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="18752-343">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18752-343">Textual description of the object.</span></span>

<span data-ttu-id="18752-344">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18752-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="18752-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-348">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="18752-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="18752-349">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18752-349">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="18752-350">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-351">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="18752-351">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-352">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18752-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18752-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-354">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,4 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="18752-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="18752-355">Adresse de fin, référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire, pour l’objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="18752-355">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="18752-356">L’adresse de fin est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="18752-356">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="18752-357">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-357">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="18752-358">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="18752-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="18752-359">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="18752-359">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-360">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18752-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18752-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-362">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,15 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="18752-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="18752-363">Opération d’accès à la mémoire qui a provoqué la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="18752-363">Memory access operation that caused the last error.</span></span> <span data-ttu-id="18752-364">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="18752-364">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="18752-365">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="18752-365">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="18752-366">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-366">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18752-367">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="18752-367">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18752-368">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="18752-368">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="18752-369">**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="18752-369">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="18752-370">**Écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="18752-370">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="18752-371">**Écriture partielle** (5)</span><span class="sxs-lookup"><span data-stu-id="18752-371">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18752-372">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="18752-372">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-373">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18752-373">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18752-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-375">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,19 "," MIF. \|Périphérique de mémoire DMTF \| 002,20 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="18752-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="18752-376">Adresse de la dernière erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="18752-376">Address of the last memory error.</span></span> <span data-ttu-id="18752-377">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="18752-377">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="18752-378">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="18752-378">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="18752-379">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-379">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="18752-380">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="18752-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="18752-381">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="18752-381">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-382">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18752-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18752-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18752-384">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="18752-384">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="18752-385">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-386">**Partagefichiers**</span><span class="sxs-lookup"><span data-stu-id="18752-386">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-387">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="18752-387">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="18752-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-389">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,17 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="18752-389">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="18752-390">Données capturées au cours du dernier accès mémoire erroné.</span><span class="sxs-lookup"><span data-stu-id="18752-390">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="18752-391">Les données occupent les *n* premiers octets du tableau nécessaire pour contenir le nombre de bits spécifié par la propriété **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="18752-391">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="18752-392">Si **ErrorTransferSize** est égal à 0, cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="18752-392">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="18752-393">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-394">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="18752-394">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-395">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18752-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18752-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18752-397">Classement des données stockées dans le tableau **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="18752-397">Ordering for data stored in the **ErrorData** array.</span></span> <span data-ttu-id="18752-398">Si **ErrorTransferSize** est égal à 0, cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="18752-398">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="18752-399">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18752-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="18752-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18752-401">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="18752-401">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="18752-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Octet le moins significatif en premier** (1)</span><span class="sxs-lookup"><span data-stu-id="18752-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18752-403">Octet le moins significatif en premier.</span><span class="sxs-lookup"><span data-stu-id="18752-403">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="18752-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Octet le plus significatif en premier** (2)</span><span class="sxs-lookup"><span data-stu-id="18752-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18752-405">Octet le plus significatif en premier.</span><span class="sxs-lookup"><span data-stu-id="18752-405">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18752-406">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="18752-406">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-407">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18752-409">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="18752-409">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="18752-410">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-411">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="18752-411">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-412">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18752-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18752-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-414">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ mémoire CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="18752-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="18752-415">Type d’erreur qui s’est produite le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="18752-415">Type of error that occurred most recently.</span></span> <span data-ttu-id="18752-416">Les valeurs 12-14 ne sont pas définies dans le schéma CIM, car la sémantique du type d’erreur et la nécessité ou non de la corriger sont mélangées dans DMI.</span><span class="sxs-lookup"><span data-stu-id="18752-416">The values 12-14 are undefined in the CIM schema since the semantics of the type of error and whether or not it was correctable are mixed in DMI.</span></span> <span data-ttu-id="18752-417">La propriété **CorrectableError** indique si elle a été corrigée.</span><span class="sxs-lookup"><span data-stu-id="18752-417">The **CorrectableError** property indicates whether it was correctable.</span></span>

<span data-ttu-id="18752-418">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-418">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18752-419">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="18752-419">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18752-420">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="18752-420">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="18752-421">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="18752-421">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="18752-422">**Lecture incorrecte** (4)</span><span class="sxs-lookup"><span data-stu-id="18752-422">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="18752-423">**Erreur de parité** (5)</span><span class="sxs-lookup"><span data-stu-id="18752-423">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="18752-424">**Erreur de bit unique** (6)</span><span class="sxs-lookup"><span data-stu-id="18752-424">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="18752-425">**Erreur double bit** (7)</span><span class="sxs-lookup"><span data-stu-id="18752-425">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="18752-426">**Erreur multibits** (8)</span><span class="sxs-lookup"><span data-stu-id="18752-426">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="18752-427">**Erreur de grignotage** (9)</span><span class="sxs-lookup"><span data-stu-id="18752-427">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="18752-428">**Erreur de somme de contrôle** (10)</span><span class="sxs-lookup"><span data-stu-id="18752-428">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="18752-429">**Erreur CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="18752-429">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="18752-430">**Non défini** (12)</span><span class="sxs-lookup"><span data-stu-id="18752-430">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="18752-431">**Non défini** (13)</span><span class="sxs-lookup"><span data-stu-id="18752-431">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="18752-432">**Non défini** (14)</span><span class="sxs-lookup"><span data-stu-id="18752-432">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18752-433">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="18752-433">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-436">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="18752-436">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="18752-437">Chaîne de forme libre qui décrit le type de détection d’erreurs et de correction pris en charge par l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="18752-437">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="18752-438">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-438">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-439">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="18752-439">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-440">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18752-440">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18752-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-442">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,21 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="18752-442">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="18752-443">Plage, en octets, à laquelle la dernière erreur peut être résolue.</span><span class="sxs-lookup"><span data-stu-id="18752-443">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="18752-444">Par exemple, si les adresses d’erreurs sont résolues en bit 11 (c’est-à-dire, sur une base de page standard), les erreurs peuvent être résolues en limites de 4 Ko et cette propriété est définie sur 4000.</span><span class="sxs-lookup"><span data-stu-id="18752-444">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="18752-445">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="18752-445">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="18752-446">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-446">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="18752-447">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="18752-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="18752-448">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="18752-448">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-449">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18752-449">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18752-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18752-451">Heure à laquelle la dernière erreur de mémoire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="18752-451">Time that the last memory error occurred.</span></span> <span data-ttu-id="18752-452">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="18752-452">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="18752-453">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="18752-453">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="18752-454">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-454">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-455">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="18752-455">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-456">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18752-456">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18752-457">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-458">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,16 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="18752-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="18752-459">Taille du transfert de données en bits qui a provoqué la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="18752-459">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="18752-460">0 indique qu’il n’y a pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="18752-460">0 indicates no error.</span></span> <span data-ttu-id="18752-461">Si la propriété **errorInfo** est égale à 3, « OK », cette propriété doit être définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="18752-461">If the **ErrorInfo** property is equal to 3, "OK", then this property should be set to 0.</span></span>

<span data-ttu-id="18752-462">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-462">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-463">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18752-463">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-464">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18752-464">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18752-465">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-466">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="18752-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="18752-467">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18752-467">Date and time the object was installed.</span></span> <span data-ttu-id="18752-468">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="18752-468">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="18752-469">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18752-469">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18752-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-471">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18752-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18752-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18752-473">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18752-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="18752-474">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-475">**Nom**</span><span class="sxs-lookup"><span data-stu-id="18752-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-476">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-478">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="18752-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="18752-479">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="18752-479">Label by which the object is known.</span></span> <span data-ttu-id="18752-480">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="18752-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="18752-481">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18752-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="18752-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-483">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18752-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18752-484">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-485">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="18752-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="18752-486">Nombre total de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forme cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="18752-486">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="18752-487">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="18752-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="18752-488">Si la valeur de **BlockSize** est 1 (un), cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="18752-488">If the value of **BlockSize** is 1 (one), then this property is the total size of the storage extent.</span></span>

<span data-ttu-id="18752-489">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18752-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="18752-490">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="18752-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="18752-491">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="18752-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-492">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-493">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-494">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ mémoire CIM**](cim-memory.md).**ErrorInfo**»)</span><span class="sxs-lookup"><span data-stu-id="18752-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="18752-495">Chaîne de forme libre qui fournit des informations supplémentaires si la propriété **ErrorType** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="18752-495">Free-form string that provides additional information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="18752-496">Si une valeur autre que 1 (un), cette chaîne n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="18752-496">If a value other than 1 (one), this string has no meaning.</span></span>

<span data-ttu-id="18752-497">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="18752-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-499">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-500">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-501">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18752-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18752-502">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18752-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="18752-503">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="18752-504">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="18752-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="18752-505">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="18752-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-506">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18752-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18752-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18752-508">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="18752-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="18752-509">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="18752-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18752-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="18752-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="18752-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="18752-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="18752-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="18752-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="18752-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="18752-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18752-514">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="18752-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="18752-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="18752-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="18752-516">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="18752-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="18752-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="18752-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="18752-518">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18752-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="18752-519">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="18752-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="18752-520">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="18752-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="18752-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="18752-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="18752-522">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="18752-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="18752-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="18752-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="18752-524">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="18752-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18752-525">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="18752-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-526">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18752-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18752-527">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18752-528">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="18752-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="18752-529">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="18752-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="18752-530">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="18752-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="18752-531">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="18752-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="18752-532">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-533">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="18752-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-534">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-535">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18752-536">Chaîne de forme libre qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="18752-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="18752-537">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="18752-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-538">**De la**</span><span class="sxs-lookup"><span data-stu-id="18752-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-539">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18752-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18752-540">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-541">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,3 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="18752-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="18752-542">Adresse de début, référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire, pour l’objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="18752-542">Beginning address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="18752-543">L’adresse de départ est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="18752-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="18752-544">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="18752-545">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="18752-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="18752-546">**État**</span><span class="sxs-lookup"><span data-stu-id="18752-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-547">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-548">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-549">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="18752-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="18752-550">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18752-550">Current status of the object.</span></span> <span data-ttu-id="18752-551">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18752-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="18752-552">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="18752-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="18752-553">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="18752-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="18752-554">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="18752-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18752-555">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="18752-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18752-556">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="18752-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="18752-557">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="18752-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="18752-558">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="18752-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="18752-559">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="18752-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="18752-560">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="18752-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="18752-561">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="18752-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="18752-562">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="18752-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="18752-563">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="18752-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="18752-564">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="18752-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18752-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="18752-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-566">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18752-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18752-567">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-568">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="18752-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="18752-569">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18752-569">State of the logical device.</span></span> <span data-ttu-id="18752-570">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="18752-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="18752-571">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18752-572">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="18752-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18752-573">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="18752-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="18752-574">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="18752-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="18752-575">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="18752-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="18752-576">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="18752-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18752-577">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18752-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-578">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-579">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-580">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="18752-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="18752-581">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18752-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="18752-582">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="18752-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-584">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18752-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18752-585">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18752-586">Si la **valeur est true**, les informations d’adresse dans la propriété **ErrorAddress** sont une adresse de niveau système ; Si la **valeur est false**, il s’agit d’une adresse physique.</span><span class="sxs-lookup"><span data-stu-id="18752-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address; if **FALSE**, it is a physical address.</span></span> <span data-ttu-id="18752-587">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="18752-587">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="18752-588">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-588">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="18752-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="18752-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18752-590">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18752-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18752-591">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18752-591">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18752-592">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="18752-592">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="18752-593">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18752-593">Scoping system's name.</span></span>

<span data-ttu-id="18752-594">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18752-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18752-595">Notes</span><span class="sxs-lookup"><span data-stu-id="18752-595">Remarks</span></span>

<span data-ttu-id="18752-596">La classe **CIM \_ VolatileStorage** est dérivée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="18752-596">The **CIM\_VolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="18752-597">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="18752-597">WMI does not implement this class.</span></span>

<span data-ttu-id="18752-598">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="18752-598">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="18752-599">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="18752-599">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="18752-600">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18752-600">Requirements</span></span>



| <span data-ttu-id="18752-601">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18752-601">Requirement</span></span> | <span data-ttu-id="18752-602">Valeur</span><span class="sxs-lookup"><span data-stu-id="18752-602">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18752-603">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18752-603">Minimum supported client</span></span><br/> | <span data-ttu-id="18752-604">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18752-604">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18752-605">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18752-605">Minimum supported server</span></span><br/> | <span data-ttu-id="18752-606">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18752-606">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18752-607">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18752-607">Namespace</span></span><br/>                | <span data-ttu-id="18752-608">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="18752-608">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18752-609">MOF</span><span class="sxs-lookup"><span data-stu-id="18752-609">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18752-610"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18752-610"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18752-611">DLL</span><span class="sxs-lookup"><span data-stu-id="18752-611">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18752-612"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18752-612"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18752-613">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18752-613">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18752-614">**\_Mémoire CIM**</span><span class="sxs-lookup"><span data-stu-id="18752-614">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

