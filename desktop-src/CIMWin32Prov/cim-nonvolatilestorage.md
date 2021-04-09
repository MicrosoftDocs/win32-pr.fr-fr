---
description: La \_ classe CIM NonVolatileStorage représente les fonctionnalités et la gestion du stockage non volatile. La mémoire non volatile comprend en mode natif le stockage flash et ROM.
ms.assetid: 39158b31-31f7-460c-aef1-1ca423badad6
ms.tgt_platform: multiple
title: Classe CIM_NonVolatileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NonVolatileStorage
- CIM_NonVolatileStorage.Access
- CIM_NonVolatileStorage.AdditionalErrorData
- CIM_NonVolatileStorage.Availability
- CIM_NonVolatileStorage.BlockSize
- CIM_NonVolatileStorage.Caption
- CIM_NonVolatileStorage.ConfigManagerErrorCode
- CIM_NonVolatileStorage.ConfigManagerUserConfig
- CIM_NonVolatileStorage.CorrectableError
- CIM_NonVolatileStorage.CreationClassName
- CIM_NonVolatileStorage.Description
- CIM_NonVolatileStorage.DeviceID
- CIM_NonVolatileStorage.EndingAddress
- CIM_NonVolatileStorage.ErrorAccess
- CIM_NonVolatileStorage.ErrorAddress
- CIM_NonVolatileStorage.ErrorCleared
- CIM_NonVolatileStorage.ErrorData
- CIM_NonVolatileStorage.ErrorDataOrder
- CIM_NonVolatileStorage.ErrorDescription
- CIM_NonVolatileStorage.ErrorInfo
- CIM_NonVolatileStorage.ErrorMethodology
- CIM_NonVolatileStorage.ErrorResolution
- CIM_NonVolatileStorage.ErrorTime
- CIM_NonVolatileStorage.ErrorTransferSize
- CIM_NonVolatileStorage.InstallDate
- CIM_NonVolatileStorage.IsWriteable
- CIM_NonVolatileStorage.LastErrorCode
- CIM_NonVolatileStorage.Name
- CIM_NonVolatileStorage.NumberOfBlocks
- CIM_NonVolatileStorage.OtherErrorDescription
- CIM_NonVolatileStorage.PNPDeviceID
- CIM_NonVolatileStorage.PowerManagementCapabilities
- CIM_NonVolatileStorage.PowerManagementSupported
- CIM_NonVolatileStorage.Purpose
- CIM_NonVolatileStorage.StartingAddress
- CIM_NonVolatileStorage.Status
- CIM_NonVolatileStorage.StatusInfo
- CIM_NonVolatileStorage.SystemCreationClassName
- CIM_NonVolatileStorage.SystemLevelAddress
- CIM_NonVolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fca29f0b279994dc0b844127fd1925850094da8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860757"
---
# <a name="cim_nonvolatilestorage-class"></a><span data-ttu-id="8f0cb-104">\_Classe CIM NonVolatileStorage</span><span class="sxs-lookup"><span data-stu-id="8f0cb-104">CIM\_NonVolatileStorage class</span></span>

<span data-ttu-id="8f0cb-105">La classe **CIM \_ NonVolatileStorage** représente les fonctionnalités et la gestion du stockage non volatile.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-105">The **CIM\_NonVolatileStorage** class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="8f0cb-106">La mémoire non volatile comprend en mode natif le stockage flash et ROM.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-106">Nonvolatile memory natively includes flash and ROM storage.</span></span> <span data-ttu-id="8f0cb-107">En outre, la mémoire non volatile peut reposer sur un stockage volatile, si la mémoire volatile est sauvegardée par une batterie.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-107">In addition, nonvolatile memory can be based on volatile storage, if the volatile memory is backed by a battery.</span></span> <span data-ttu-id="8f0cb-108">Par exemple, ce scénario est décrit par une instance de la relation [**CIM \_ AssociatedBattery**](cim-associatedbattery.md) qui fait référence au stockage non volatile comme étant le **dépendant** et la batterie en tant qu' **antécédent**, et une instance de la relation [**CIM \_**](cim-basedon.md) qui fait référence au stockage non volatile en tant que stockage **dépendant** et le stockage volatil comme **antécédent**.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-108">For example, this scenario would be described by an instance of the [**CIM\_AssociatedBattery**](cim-associatedbattery.md) relationship that references the nonvolatile storage as the **Dependent** and the battery as the **Antecedent**; and an instance of the [**CIM\_BasedOn**](cim-basedon.md) relationship that references the non-volatile storage as the **Dependent** and the volatile storage as the **Antecedent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f0cb-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f0cb-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f0cb-111">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8f0cb-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f0cb-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f0cb-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{18074AFA-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_NonVolatileStorage : CIM_Memory
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
  boolean  IsWriteable;
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

## <a name="members"></a><span data-ttu-id="8f0cb-114">Membres</span><span class="sxs-lookup"><span data-stu-id="8f0cb-114">Members</span></span>

<span data-ttu-id="8f0cb-115">La classe **CIM \_ NonVolatileStorage** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8f0cb-115">The **CIM\_NonVolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="8f0cb-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8f0cb-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f0cb-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f0cb-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f0cb-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8f0cb-118">Methods</span></span>

<span data-ttu-id="8f0cb-119">La classe **CIM \_ NonVolatileStorage** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-119">The **CIM\_NonVolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="8f0cb-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="8f0cb-120">Method</span></span>                                                                        | <span data-ttu-id="8f0cb-121">Description</span><span class="sxs-lookup"><span data-stu-id="8f0cb-121">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f0cb-122">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-122">**Reset**</span></span>](reset-method-in-class-cim-nonvolatilestorage.md)                 | <span data-ttu-id="8f0cb-123">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="8f0cb-124">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="8f0cb-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-nonvolatilestorage.md) | <span data-ttu-id="8f0cb-126">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="8f0cb-127">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8f0cb-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f0cb-128">Properties</span></span>

<span data-ttu-id="8f0cb-129">La classe **CIM \_ NonVolatileStorage** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-129">The **CIM\_NonVolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f0cb-130">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-133">Propriétés de lecture/écriture du média.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-133">Read/write properties of the media.</span></span>

<span data-ttu-id="8f0cb-134">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f0cb-135">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="8f0cb-136">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="8f0cb-137">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="8f0cb-138">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="8f0cb-139">**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f0cb-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-141">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-143">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,18 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-144">Tableau d’octets qui contiennent des informations d’erreur supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="8f0cb-145">Par exemple, le syndrome de la vérification et de la correction des erreurs (ECC), ou le retour des bits de vérification si une méthodologie d’erreur basée sur CRC est utilisée.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="8f0cb-146">Dans ce dernier cas, si une erreur de bit unique est reconnue et que l’algorithme CRC est connu, le bit exact qui a échoué peut être déterminé.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="8f0cb-147">Ce type de données (syndrome ECC, données de bit de contrôle ou de parité ou autres informations fournies par le fournisseur) est inclus dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="8f0cb-148">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="8f0cb-149">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-150">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-153">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-154">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-154">Availability and status of the device.</span></span>

<span data-ttu-id="8f0cb-155">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-155">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f0cb-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f0cb-157"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-157"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8f0cb-158"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-158"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8f0cb-159"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-159"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8f0cb-160"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-160"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8f0cb-161"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-161"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8f0cb-162"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-162"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8f0cb-163"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-163"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8f0cb-164"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-164"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8f0cb-165"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-165"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8f0cb-166"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-166"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8f0cb-167"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-167"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8f0cb-168"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-168"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-169">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-169">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8f0cb-170"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-170"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-171">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-171">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8f0cb-172"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-172"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-173">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-173">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8f0cb-174"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-174"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8f0cb-175"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-175"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-176">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-176">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8f0cb-177"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-177"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-178">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-178">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8f0cb-179"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-179"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-180">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-180">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8f0cb-181"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-181"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-182">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-182">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8f0cb-183"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-183"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-184">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-184">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f0cb-185">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-185">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-186">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-188">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-189">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-189">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="8f0cb-190">Si vous spécifiez une taille de bloc variable, la taille maximale du bloc, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-190">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="8f0cb-191">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1 (un).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-191">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter 1 (one).</span></span>

<span data-ttu-id="8f0cb-192">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-192">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="8f0cb-193">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-194">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-197">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-198">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-198">Short textual description of the object.</span></span>

<span data-ttu-id="8f0cb-199">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-200">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-200">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-201">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-203">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-203">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-204">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-204">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="8f0cb-205">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-205">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="8f0cb-206"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-206"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="8f0cb-207"> (0)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-207">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-208">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-208">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="8f0cb-209"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-209"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="8f0cb-210">(1)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-210">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-211">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-211">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8f0cb-212"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-212"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="8f0cb-213">(2)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-213">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="8f0cb-214"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-214"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="8f0cb-215">(3)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-215">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-216">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-216">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8f0cb-217"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-217"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="8f0cb-218">(4)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-218">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-219">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-219">Device is not working properly.</span></span> <span data-ttu-id="8f0cb-220">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-220">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="8f0cb-221"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-221"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="8f0cb-222">(5)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-222">(5)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-223">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-223">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="8f0cb-224"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-224"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="8f0cb-225"> (6)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-225">(6)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-226">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-226">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="8f0cb-227"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-227"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="8f0cb-228">(7)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-228">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="8f0cb-229"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-229"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="8f0cb-230">(8)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-230">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-231">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-231">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="8f0cb-232"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-232"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="8f0cb-233">(9)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-233">(9)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-234">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-234">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="8f0cb-235"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-235"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="8f0cb-236">(10)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-236">(10)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-237">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-237">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="8f0cb-238"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-238"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="8f0cb-239">(11)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-239">(11)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-240">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-240">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="8f0cb-241"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-241"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="8f0cb-242">douze</span><span class="sxs-lookup"><span data-stu-id="8f0cb-242">(12)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-243">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-243">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="8f0cb-244"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-244"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="8f0cb-245">(13)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-245">(13)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-246">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-246">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="8f0cb-247"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-247"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="8f0cb-248">(14)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-248">(14)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-249">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-249">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="8f0cb-250"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-250"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="8f0cb-251">(15)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-251">(15)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-252">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-252">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="8f0cb-253"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-253"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="8f0cb-254">(16)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-254">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-255">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-255">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="8f0cb-256"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-256"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="8f0cb-257">(17)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-257">(17)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-258">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-258">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8f0cb-259"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-259"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="8f0cb-260">(18)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-260">(18)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-261">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-261">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="8f0cb-262"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-262"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="8f0cb-263">(19)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-263">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8f0cb-264"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-264"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="8f0cb-265">(20)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-265">(20)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-266">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-266">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="8f0cb-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="8f0cb-268">(21)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-268">(21)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-269">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-269">System failure.</span></span> <span data-ttu-id="8f0cb-270">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-270">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="8f0cb-271">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-271">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="8f0cb-272"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-272"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="8f0cb-273">(22)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-273">(22)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-274">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-274">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="8f0cb-275"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-275"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="8f0cb-276">(23)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-276">(23)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-277">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-277">System failure.</span></span> <span data-ttu-id="8f0cb-278">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-278">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="8f0cb-279"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-279"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="8f0cb-280">(24)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-280">(24)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-281">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-281">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8f0cb-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8f0cb-283">(25)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-283">(25)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-284">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8f0cb-285"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-285"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8f0cb-286">(26)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-286">(26)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-287">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-287">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="8f0cb-288"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-288"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="8f0cb-289">(27)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-289">(27)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-290">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-290">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="8f0cb-291"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-291"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="8f0cb-292">(28)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-292">(28)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-293">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-293">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="8f0cb-294"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-294"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="8f0cb-295">(29)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-295">(29)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-296">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-296">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="8f0cb-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="8f0cb-298">(30)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-299">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8f0cb-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="8f0cb-301">31</span><span class="sxs-lookup"><span data-stu-id="8f0cb-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-302">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-302">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f0cb-303">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-303">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-304">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-306">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-307">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-307">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="8f0cb-308">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-309">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-309">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-310">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-312">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-313">Si la **valeur est true**, l’erreur la plus récente était correcte.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-313">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="8f0cb-314">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-314">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="8f0cb-315">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-315">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-316">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-319">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-319">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-320">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-320">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8f0cb-321">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-321">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8f0cb-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-323">**Description**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-326">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-326">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-327">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-327">Textual description of the object.</span></span>

<span data-ttu-id="8f0cb-328">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-329">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-329">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-330">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-332">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-333">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-333">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="8f0cb-334">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-335">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-335">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-336">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-336">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-338">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,4 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-339">Adresse de fin, référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire, pour l’objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-339">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="8f0cb-340">L’adresse de fin est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-340">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="8f0cb-341">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="8f0cb-342">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-343">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-343">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-344">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-346">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,15 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-347">Énumération qui indique l’opération d’accès à la mémoire qui a provoqué la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-347">Enumeration that indicates the memory access operation that caused the last error.</span></span> <span data-ttu-id="8f0cb-348">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="8f0cb-348">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="8f0cb-349">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-349">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="8f0cb-350">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-350">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f0cb-351">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-351">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f0cb-352">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-352">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="8f0cb-353">**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-353">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="8f0cb-354">**Écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-354">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="8f0cb-355">**Écriture partielle** (5)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-355">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f0cb-356">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-356">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-357">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-359">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,19 "," MIF. \|Périphérique de mémoire DMTF \| 002,20 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-360">Adresse de la dernière erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-360">Address of the last memory error.</span></span> <span data-ttu-id="8f0cb-361">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="8f0cb-361">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="8f0cb-362">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-362">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="8f0cb-363">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-363">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="8f0cb-364">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-365">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-366">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-368">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-368">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="8f0cb-369">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-370">**Partagefichiers**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-371">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-373">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,17 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-374">Données capturées au cours du dernier accès mémoire erroné.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-374">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="8f0cb-375">Les données occupent les *n* premiers octets du tableau qui sont nécessaires pour contenir le nombre de bits spécifié par la propriété **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="8f0cb-375">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="8f0cb-376">Si **ErrorTransferSize** est égal à 0, cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-376">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="8f0cb-377">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-377">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-378">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-379">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-381">Classement des données stockées dans la propriété **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="8f0cb-381">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="8f0cb-382">Si **ErrorTransferSize** est égal à 0, cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-382">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="8f0cb-383">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-383">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f0cb-384">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-384">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="8f0cb-385">**Octet le moins significatif en premier** (1)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-385">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="8f0cb-386">**Octet le plus significatif en premier** (2)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-386">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f0cb-387">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-387">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-388">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-390">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-390">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="8f0cb-391">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-392">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-392">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-393">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-395">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ mémoire CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-396">Type d’erreur qui s’est produite le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-396">Type of error that occurred most recently.</span></span> <span data-ttu-id="8f0cb-397">Les valeurs 12 à 14 ne sont pas définies dans le schéma CIM, car DMI mélange la sémantique du type d’erreur et indique si elle a été corrigée.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-397">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="8f0cb-398">La propriété **CorrectableError** indique si une erreur peut être corrigée.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-398">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span> <span data-ttu-id="8f0cb-399">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f0cb-400"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-400"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-401">Autre.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-401">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f0cb-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-403">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-403">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8f0cb-404"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-404"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-405">OK.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-405">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="8f0cb-406"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lecture incorrecte** (4)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-406"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-407">Lecture incorrecte.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-407">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="8f0cb-408"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Erreur de parité** (5)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-408"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-409">Erreur de parité.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-409">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="8f0cb-410"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Erreur de bit unique** (6)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-410"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-411">Erreur sur un bit.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-411">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="8f0cb-412"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Erreur double bit** (7)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-412"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-413">Erreur double bit.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-413">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="8f0cb-414"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Erreur multibits** (8)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-414"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-415">Erreur multi-bit.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-415">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="8f0cb-416"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Erreur de grignotage** (9)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-416"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-417">Erreur de Quartet.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-417">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="8f0cb-418"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Erreur de somme de contrôle** (10)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-418"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-419">Erreur de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-419">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="8f0cb-420"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Erreur CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-420"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-421">Erreur CRC.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-421">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="8f0cb-422"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (12)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-422"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-423">Non défini.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-423">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="8f0cb-424"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (13)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-424"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-425">Non défini.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-425">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="8f0cb-426"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (14)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-426"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-427">Non défini.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-427">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f0cb-428">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-428">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-429">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-431">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-431">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-432">Spécifie si les algorithmes de parité, les algorithmes CRC, l’ECC ou d’autres mécanismes sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-432">Specifies whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used.</span></span> <span data-ttu-id="8f0cb-433">Vous pouvez également fournir des détails sur l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-433">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="8f0cb-434">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-434">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-435">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-435">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-436">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-436">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-438">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,21 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-439">Plage, en octets, à laquelle la dernière erreur peut être résolue.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-439">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="8f0cb-440">Par exemple, si les adresses d’erreurs sont résolues en bit 11 (c’est-à-dire, sur une base de page standard), les erreurs peuvent être résolues en limites de 4 Ko et cette propriété est définie sur 4000.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-440">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="8f0cb-441">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-441">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="8f0cb-442">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="8f0cb-443">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-443">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-444">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-444">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-445">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-445">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-447">Heure à laquelle la dernière erreur de mémoire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-447">Time that the last memory error occurred.</span></span> <span data-ttu-id="8f0cb-448">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="8f0cb-448">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="8f0cb-449">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-449">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="8f0cb-450">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-450">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-451">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-451">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-452">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-454">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,16 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-455">Taille du transfert de données, en bits, à l’origine de la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-455">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="8f0cb-456">La valeur 0 (zéro) indique qu’il n’y A pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-456">A value of 0 (zero) indicates no error.</span></span> <span data-ttu-id="8f0cb-457">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-457">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="8f0cb-458">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-460">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-461">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-462">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-463">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-463">Date and time the object was installed.</span></span> <span data-ttu-id="8f0cb-464">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-464">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8f0cb-465">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-466">**IsWriteable**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-466">**IsWriteable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-467">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-468">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-469">Si la **valeur est true**, le stockage non volatile peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-469">If **TRUE**, non-volatile storage is writeable.</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-471">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-473">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="8f0cb-474">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-475">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-476">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-478">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-479">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-479">Label by which the object is known.</span></span> <span data-ttu-id="8f0cb-480">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8f0cb-481">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-483">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-484">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-485">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-486">Nombre total de blocs consécutifs, chaque bloc est la taille de la valeur contenue dans la propriété **BlockSize** , qui forme l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-486">Total number of consecutive blocks, each block is the size of the value contained in the **BlockSize** property, which forms the storage extent.</span></span> <span data-ttu-id="8f0cb-487">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="8f0cb-488">Si la valeur de **BlockSize** est 1 (un), cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-488">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="8f0cb-489">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="8f0cb-490">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-491">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-492">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-493">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-494">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ mémoire CIM**](cim-memory.md).**ErrorInfo**»)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-495">Chaîne de forme libre qui fournit des informations si la propriété **ErrorType** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-495">Free-form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="8f0cb-496">Si la valeur n’est pas définie sur 1, cette chaîne n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-496">If not set to 1, this string has no meaning.</span></span>

<span data-ttu-id="8f0cb-497">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-499">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-500">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-501">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-502">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="8f0cb-503">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8f0cb-504">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="8f0cb-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-505">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-506">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-508">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="8f0cb-509">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f0cb-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8f0cb-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8f0cb-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8f0cb-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-514">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8f0cb-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-516">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8f0cb-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-518">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="8f0cb-519">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="8f0cb-520">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8f0cb-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-522">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8f0cb-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8f0cb-524">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f0cb-525">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-526">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-527">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-528">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="8f0cb-529">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="8f0cb-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="8f0cb-530">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="8f0cb-531">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="8f0cb-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="8f0cb-532">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-533">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-534">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-535">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-536">Chaîne de forme libre qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="8f0cb-537">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-538">**De la**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-539">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-540">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-541">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,3 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-542">Adresse de début référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-542">Beginning address that is referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="8f0cb-543">L’adresse de départ est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="8f0cb-544">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="8f0cb-545">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-546">**État**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-547">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-548">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-549">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-550">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-550">Current status of the object.</span></span>

<span data-ttu-id="8f0cb-551">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8f0cb-552">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f0cb-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8f0cb-553">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8f0cb-554">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8f0cb-555">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f0cb-556">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8f0cb-557">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8f0cb-558">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8f0cb-559">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8f0cb-560">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8f0cb-561">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8f0cb-562">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8f0cb-563">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8f0cb-564">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f0cb-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-566">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-567">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-568">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8f0cb-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-569">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-569">State of the logical device.</span></span> <span data-ttu-id="8f0cb-570">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="8f0cb-571">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f0cb-572">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f0cb-573">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8f0cb-574">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8f0cb-575">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8f0cb-576">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f0cb-577">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-578">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-579">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-580">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-581">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="8f0cb-582">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-584">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-585">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-586">Si la **valeur est true**, les informations d’adresse dans la propriété **ErrorAddress** sont une adresse de niveau système.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="8f0cb-587">Si la **valeur est false**, il s’agit d’une adresse physique.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-587">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="8f0cb-588">Si la propriété **errorInfo** est égale à 3 (« OK »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-588">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="8f0cb-589">Cette propriété est héritée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-589">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f0cb-590">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-590">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f0cb-591">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-592">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f0cb-592">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f0cb-593">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8f0cb-593">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8f0cb-594">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-594">Scoping system's name.</span></span>

<span data-ttu-id="8f0cb-595">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-595">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f0cb-596">Notes</span><span class="sxs-lookup"><span data-stu-id="8f0cb-596">Remarks</span></span>

<span data-ttu-id="8f0cb-597">La classe **CIM \_ NonVolatileStorage** est dérivée de la [**\_ mémoire CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="8f0cb-597">The **CIM\_NonVolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="8f0cb-598">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-598">WMI does not implement this class.</span></span>

<span data-ttu-id="8f0cb-599">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-599">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f0cb-600">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8f0cb-600">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f0cb-601">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f0cb-601">Requirements</span></span>



| <span data-ttu-id="8f0cb-602">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f0cb-602">Requirement</span></span> | <span data-ttu-id="8f0cb-603">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f0cb-603">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f0cb-604">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f0cb-604">Minimum supported client</span></span><br/> | <span data-ttu-id="8f0cb-605">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f0cb-605">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f0cb-606">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f0cb-606">Minimum supported server</span></span><br/> | <span data-ttu-id="8f0cb-607">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f0cb-607">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f0cb-608">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8f0cb-608">Namespace</span></span><br/>                | <span data-ttu-id="8f0cb-609">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8f0cb-609">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f0cb-610">MOF</span><span class="sxs-lookup"><span data-stu-id="8f0cb-610">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f0cb-611"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f0cb-611"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f0cb-612">DLL</span><span class="sxs-lookup"><span data-stu-id="8f0cb-612">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f0cb-613"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f0cb-613"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f0cb-614">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f0cb-614">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f0cb-615">**\_Mémoire CIM**</span><span class="sxs-lookup"><span data-stu-id="8f0cb-615">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

