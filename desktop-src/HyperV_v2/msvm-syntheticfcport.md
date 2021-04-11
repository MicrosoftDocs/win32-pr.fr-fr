---
description: Représente un port de Fibre Channel synthétique.
ms.assetid: 6ca827b5-3ea0-4967-ba1f-b41e84c84009
title: Msvm_SyntheticFcPort, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPort
- Msvm_SyntheticFcPort.SetPowerState
- Msvm_SyntheticFcPort.EnableDevice
- Msvm_SyntheticFcPort.OnlineDevice
- Msvm_SyntheticFcPort.QuiesceDevice
- Msvm_SyntheticFcPort.SaveProperties
- Msvm_SyntheticFcPort.RestoreProperties
- Msvm_SyntheticFcPort.InstanceID
- Msvm_SyntheticFcPort.Caption
- Msvm_SyntheticFcPort.Description
- Msvm_SyntheticFcPort.ElementName
- Msvm_SyntheticFcPort.InstallDate
- Msvm_SyntheticFcPort.Name
- Msvm_SyntheticFcPort.OperationalStatus
- Msvm_SyntheticFcPort.StatusDescriptions
- Msvm_SyntheticFcPort.Status
- Msvm_SyntheticFcPort.HealthState
- Msvm_SyntheticFcPort.CommunicationStatus
- Msvm_SyntheticFcPort.DetailedStatus
- Msvm_SyntheticFcPort.OperatingStatus
- Msvm_SyntheticFcPort.PrimaryStatus
- Msvm_SyntheticFcPort.EnabledState
- Msvm_SyntheticFcPort.OtherEnabledState
- Msvm_SyntheticFcPort.RequestedState
- Msvm_SyntheticFcPort.EnabledDefault
- Msvm_SyntheticFcPort.TimeOfLastStateChange
- Msvm_SyntheticFcPort.AvailableRequestedStates
- Msvm_SyntheticFcPort.TransitioningToState
- Msvm_SyntheticFcPort.SystemCreationClassName
- Msvm_SyntheticFcPort.SystemName
- Msvm_SyntheticFcPort.CreationClassName
- Msvm_SyntheticFcPort.DeviceID
- Msvm_SyntheticFcPort.PowerManagementSupported
- Msvm_SyntheticFcPort.PowerManagementCapabilities
- Msvm_SyntheticFcPort.Availability
- Msvm_SyntheticFcPort.StatusInfo
- Msvm_SyntheticFcPort.LastErrorCode
- Msvm_SyntheticFcPort.ErrorDescription
- Msvm_SyntheticFcPort.ErrorCleared
- Msvm_SyntheticFcPort.OtherIdentifyingInfo
- Msvm_SyntheticFcPort.PowerOnHours
- Msvm_SyntheticFcPort.TotalPowerOnHours
- Msvm_SyntheticFcPort.IdentifyingDescriptions
- Msvm_SyntheticFcPort.AdditionalAvailability
- Msvm_SyntheticFcPort.MaxQuiesceTime
- Msvm_SyntheticFcPort.Speed
- Msvm_SyntheticFcPort.MaxSpeed
- Msvm_SyntheticFcPort.RequestedSpeed
- Msvm_SyntheticFcPort.UsageRestriction
- Msvm_SyntheticFcPort.PortType
- Msvm_SyntheticFcPort.OtherPortType
- Msvm_SyntheticFcPort.OtherNetworkPortType
- Msvm_SyntheticFcPort.PortNumber
- Msvm_SyntheticFcPort.LinkTechnology
- Msvm_SyntheticFcPort.OtherLinkTechnology
- Msvm_SyntheticFcPort.PermanentAddress
- Msvm_SyntheticFcPort.NetworkAddresses
- Msvm_SyntheticFcPort.FullDuplex
- Msvm_SyntheticFcPort.AutoSense
- Msvm_SyntheticFcPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticFcPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticFcPort.SupportedCOS
- Msvm_SyntheticFcPort.ActiveCOS
- Msvm_SyntheticFcPort.SupportedFC4Types
- Msvm_SyntheticFcPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f28614a7c885c0cfc03d546219518cda240219a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112311"
---
# <a name="msvm_syntheticfcport-class"></a><span data-ttu-id="9521b-103">MSVM \_ SyntheticFcPort, classe</span><span class="sxs-lookup"><span data-stu-id="9521b-103">Msvm\_SyntheticFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="9521b-104">Cet article contient des références au terme esclave, un terme que Microsoft n’utilise plus.</span><span class="sxs-lookup"><span data-stu-id="9521b-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="9521b-105">Lorsque le terme sera supprimé du logiciel, nous le supprimerons de cet article.</span><span class="sxs-lookup"><span data-stu-id="9521b-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="9521b-106">Représente un port de Fibre Channel synthétique.</span><span class="sxs-lookup"><span data-stu-id="9521b-106">Represents a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="9521b-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9521b-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9521b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9521b-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPort : CIM_FCPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 4;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint16   SupportedCOS[];
  uint16   ActiveCOS[];
  uint16   SupportedFC4Types[];
  uint16   ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="9521b-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9521b-109">Members</span></span>

<span data-ttu-id="9521b-110">La classe **MSVM \_ SyntheticFcPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9521b-110">The **Msvm\_SyntheticFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="9521b-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9521b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9521b-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9521b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9521b-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9521b-113">Methods</span></span>

<span data-ttu-id="9521b-114">La classe **MSVM \_ SyntheticFcPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9521b-114">The **Msvm\_SyntheticFcPort** class has these methods.</span></span>



| <span data-ttu-id="9521b-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="9521b-115">Method</span></span>                                                                | <span data-ttu-id="9521b-116">Description</span><span class="sxs-lookup"><span data-stu-id="9521b-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="9521b-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="9521b-117">**EnableDevice**</span></span>                                                      | <span data-ttu-id="9521b-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9521b-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9521b-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="9521b-119">**OnlineDevice**</span></span>                                                      | <span data-ttu-id="9521b-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9521b-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9521b-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="9521b-121">**QuiesceDevice**</span></span>                                                     | <span data-ttu-id="9521b-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9521b-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9521b-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9521b-123">**RequestStateChange**</span></span>](msvm-syntheticfcport-requeststatechange.md) | <span data-ttu-id="9521b-124">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="9521b-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="9521b-125">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="9521b-125">**Reset**</span></span>](msvm-syntheticfcport-reset.md)                           | <span data-ttu-id="9521b-126">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="9521b-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="9521b-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="9521b-127">**RestoreProperties**</span></span>                                                 | <span data-ttu-id="9521b-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9521b-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9521b-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="9521b-129">**SaveProperties**</span></span>                                                    | <span data-ttu-id="9521b-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9521b-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9521b-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9521b-131">**SetPowerState**</span></span>                                                     | <span data-ttu-id="9521b-132">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9521b-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9521b-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9521b-133">Properties</span></span>

<span data-ttu-id="9521b-134">La classe **MSVM \_ SyntheticFcPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9521b-134">The **Msvm\_SyntheticFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9521b-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="9521b-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-136">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-138">Tableau d’entiers qui indique les classes de service qui sont actives.</span><span class="sxs-lookup"><span data-stu-id="9521b-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="9521b-139">Les COS pris en charge sont spécifiés par la propriété **SupportedCOS** .</span><span class="sxs-lookup"><span data-stu-id="9521b-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="9521b-140">Cette propriété est héritée de la **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="9521b-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="9521b-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9521b-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="9521b-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="9521b-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="9521b-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="9521b-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="9521b-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="9521b-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="9521b-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9521b-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="9521b-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-150">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-152">Tableau d’entiers qui indique le Fibre Channel les protocoles FC-4 en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9521b-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="9521b-153">La liste de tous les protocoles pris en charge est spécifiée par la propriété **SupportedFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="9521b-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="9521b-154">Cette propriété est héritée de la **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="9521b-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="9521b-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9521b-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9521b-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="9521b-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP sur FC** (5)</span><span class="sxs-lookup"><span data-stu-id="9521b-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="9521b-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-préférences** (9)</span><span class="sxs-lookup"><span data-stu-id="9521b-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Maître IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="9521b-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**Esclave IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="9521b-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**Homologue-3 homologue** (19)</span><span class="sxs-lookup"><span data-stu-id="9521b-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**Maître IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="9521b-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**Esclave du CP IPI-3** (22)</span><span class="sxs-lookup"><span data-stu-id="9521b-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**Homologue CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="9521b-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="9521b-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unité de contrôle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="9521b-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="9521b-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unité de contrôle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="9521b-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Services de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="9521b-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="9521b-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="9521b-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPA-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="9521b-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Contrôle BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="9521b-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU BBL FDDI encapsulé LAN** (81)</span><span class="sxs-lookup"><span data-stu-id="9521b-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU LAN encapsulé BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="9521b-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="9521b-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="9521b-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Fournisseur unique** (255)</span><span class="sxs-lookup"><span data-stu-id="9521b-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9521b-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="9521b-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-182">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9521b-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9521b-184">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9521b-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9521b-185">Unité de transmission maximale (MTU) active ou négociée qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="9521b-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="9521b-186">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9521b-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="9521b-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-188">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-190">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9521b-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="9521b-191">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-192">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="9521b-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-193">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9521b-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-195">Indique si le port peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché.</span><span class="sxs-lookup"><span data-stu-id="9521b-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="9521b-196">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9521b-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-197">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="9521b-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-198">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-200">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9521b-200">The primary availability and status of the device.</span></span> <span data-ttu-id="9521b-201">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9521b-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-203">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-205">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9521b-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="9521b-206">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9521b-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9521b-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-210">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9521b-210">A short description of the object.</span></span> <span data-ttu-id="9521b-211">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9521b-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-213">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-215">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="9521b-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9521b-216">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9521b-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9521b-217">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9521b-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9521b-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9521b-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="9521b-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="9521b-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="9521b-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9521b-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9521b-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9521b-225">)</span><span class="sxs-lookup"><span data-stu-id="9521b-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9521b-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9521b-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-229">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9521b-229">The scoping system's creation class name.</span></span> <span data-ttu-id="9521b-230">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="9521b-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-231">**Description**</span><span class="sxs-lookup"><span data-stu-id="9521b-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-234">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="9521b-234">A description of the object.</span></span> <span data-ttu-id="9521b-235">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9521b-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-237">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-239">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9521b-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9521b-240">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9521b-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9521b-241">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9521b-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="9521b-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="9521b-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="9521b-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="9521b-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="9521b-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="9521b-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9521b-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9521b-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9521b-250">)</span><span class="sxs-lookup"><span data-stu-id="9521b-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9521b-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9521b-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-254">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9521b-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="9521b-255">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="9521b-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9521b-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-259">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9521b-259">A display name for the object.</span></span> <span data-ttu-id="9521b-260">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9521b-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-262">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-264">Configuration par défaut ou de démarrage d’un administrateur pour la propriété **EnabledState** d’un élément.</span><span class="sxs-lookup"><span data-stu-id="9521b-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="9521b-265">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="9521b-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9521b-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-267">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-269">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="9521b-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9521b-270">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9521b-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="9521b-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="9521b-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9521b-272">Signification</span><span class="sxs-lookup"><span data-stu-id="9521b-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9521b-273"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9521b-274">Impossible de déterminer l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9521b-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="9521b-275"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="9521b-276"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="9521b-277">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9521b-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="9521b-278"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="9521b-279">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9521b-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="9521b-280"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="9521b-281">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="9521b-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="9521b-282"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="9521b-283">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="9521b-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="9521b-284"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="9521b-285">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="9521b-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="9521b-286"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="9521b-287">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="9521b-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="9521b-288"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="9521b-289">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="9521b-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="9521b-290"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="9521b-291">L’élément est activé, mais en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="9521b-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="9521b-292">Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="9521b-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="9521b-293">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9521b-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="9521b-294">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="9521b-295">L’élément est en train d’accéder à un état activé (2).</span><span class="sxs-lookup"><span data-stu-id="9521b-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="9521b-296">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9521b-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="9521b-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9521b-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-298">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9521b-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-300">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="9521b-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="9521b-301">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9521b-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-305">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="9521b-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="9521b-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="9521b-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-308">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9521b-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-310">Indique si le port fonctionne en mode duplex intégral.</span><span class="sxs-lookup"><span data-stu-id="9521b-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="9521b-311">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9521b-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9521b-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-313">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-315">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9521b-315">The current health of the element.</span></span> <span data-ttu-id="9521b-316">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9521b-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-318">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9521b-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-320">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="9521b-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="9521b-321">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9521b-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-323">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9521b-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-325">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9521b-325">The date and time when the object was installed.</span></span> <span data-ttu-id="9521b-326">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="9521b-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="9521b-327">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9521b-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-329">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9521b-331">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="9521b-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9521b-332">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="9521b-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9521b-333">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9521b-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-335">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9521b-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-337">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9521b-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="9521b-338">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-339">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="9521b-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-340">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-342">Spécifie le type de technologie de lien pour le port.</span><span class="sxs-lookup"><span data-stu-id="9521b-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="9521b-343">Lorsque la valeur 1 (autre) est définie, la propriété **OtherLinkTechnology** contient une description de chaîne du type de lien.</span><span class="sxs-lookup"><span data-stu-id="9521b-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="9521b-344">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9521b-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="9521b-345">Valeur</span><span class="sxs-lookup"><span data-stu-id="9521b-345">Value</span></span>                                                                                                                                                                              | <span data-ttu-id="9521b-346">Signification</span><span class="sxs-lookup"><span data-stu-id="9521b-346">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC"></span><span id="fc"></span><dl> <span data-ttu-id="9521b-347"><dt>**FC**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-347"><dt>**FC**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="9521b-348">Fibre Channel</span><span class="sxs-lookup"><span data-stu-id="9521b-348">Fibre channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9521b-349">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="9521b-349">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-350">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9521b-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-352">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="9521b-352">This property has been deprecated.</span></span> <span data-ttu-id="9521b-353">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-354">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="9521b-354">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-355">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9521b-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9521b-357">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="9521b-357">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="9521b-358">Bande passante maximale du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="9521b-358">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="9521b-359">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9521b-359">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-360">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9521b-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-363">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="9521b-363">The label by which the object is known.</span></span> <span data-ttu-id="9521b-364">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-365">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="9521b-365">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-366">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9521b-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9521b-368">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="9521b-368">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="9521b-369">Tableau de chaînes qui contient les adresses MAC du port.</span><span class="sxs-lookup"><span data-stu-id="9521b-369">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="9521b-370">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9521b-370">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-371">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9521b-371">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-372">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-374">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9521b-374">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9521b-375">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9521b-375">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9521b-376">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9521b-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9521b-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9521b-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="9521b-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="9521b-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="9521b-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="9521b-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="9521b-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="9521b-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="9521b-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="9521b-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="9521b-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="9521b-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="9521b-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="9521b-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="9521b-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="9521b-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="9521b-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9521b-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9521b-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9521b-396">)</span><span class="sxs-lookup"><span data-stu-id="9521b-396">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9521b-397">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9521b-397">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-398">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-400">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9521b-400">The current statuses of the object.</span></span> <span data-ttu-id="9521b-401">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-402">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9521b-402">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-403">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-405">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="9521b-405">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9521b-406">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="9521b-406">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="9521b-407">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9521b-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-408">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9521b-408">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-409">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9521b-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-411">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="9521b-411">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="9521b-412">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-413">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="9521b-413">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-414">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-416">Valeur de chaîne qui décrit **LinkTechnology** lorsqu’il a la valeur 1, (other).</span><span class="sxs-lookup"><span data-stu-id="9521b-416">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="9521b-417">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9521b-417">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-418">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="9521b-418">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-419">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-421">L’utilisation de cette propriété est déconseillée à la place de la propriété **portType** .</span><span class="sxs-lookup"><span data-stu-id="9521b-421">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="9521b-422">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9521b-422">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-423">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="9521b-423">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-424">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-426">Décrit le type de module, lorsque **portType** a la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="9521b-426">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="9521b-427">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9521b-427">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-428">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="9521b-428">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-429">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9521b-431">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="9521b-431">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="9521b-432">Adresse réseau qui est codée en dur dans un port.</span><span class="sxs-lookup"><span data-stu-id="9521b-432">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="9521b-433">Cette adresse codée en dur peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="9521b-433">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="9521b-434">Lorsque cette modification est apportée, le champ doit être mis à jour en même temps.</span><span class="sxs-lookup"><span data-stu-id="9521b-434">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="9521b-435">Cette propriété doit avoir la **valeur null** s’il n’existe aucune adresse codée en dur pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="9521b-435">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="9521b-436">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9521b-436">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-437">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="9521b-437">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-438">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-439">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-440">Le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="9521b-440">The port number.</span></span> <span data-ttu-id="9521b-441">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9521b-441">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-442">**PortType**</span><span class="sxs-lookup"><span data-stu-id="9521b-442">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-443">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-445">Mode spécifique actuellement activé pour le port.</span><span class="sxs-lookup"><span data-stu-id="9521b-445">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="9521b-446">Si la valeur 1 (autre) est définie, la propriété **OtherPortType** associée contient une description de chaîne du type de port.</span><span class="sxs-lookup"><span data-stu-id="9521b-446">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="9521b-447">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9521b-447">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9521b-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9521b-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9521b-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 cuivre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="9521b-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="9521b-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="9521b-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="9521b-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="9521b-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="9521b-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="9521b-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="9521b-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="9521b-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="9521b-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="9521b-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="9521b-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="9521b-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="9521b-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="9521b-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="9521b-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="9521b-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="9521b-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-SEM** (111)</span><span class="sxs-lookup"><span data-stu-id="9521b-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9521b-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9521b-470">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9521b-470">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-471">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-471">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-473">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9521b-473">The power management capabilities of the device.</span></span> <span data-ttu-id="9521b-474">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-474">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-475">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9521b-475">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-476">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9521b-476">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-478">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="9521b-478">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="9521b-479">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-479">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-480">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="9521b-480">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-481">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9521b-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-483">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="9521b-483">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="9521b-484">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-485">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9521b-485">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-486">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-488">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="9521b-488">Provides high level status information.</span></span> <span data-ttu-id="9521b-489">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="9521b-489">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9521b-490">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9521b-490">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9521b-491">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-491">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9521b-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9521b-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="9521b-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="9521b-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="9521b-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9521b-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9521b-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9521b-498">)</span><span class="sxs-lookup"><span data-stu-id="9521b-498">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9521b-499">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="9521b-499">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-500">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9521b-500">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-501">Type d’accès : écriture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-501">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="9521b-502">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="9521b-502">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="9521b-503">Bande passante demandée du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="9521b-503">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="9521b-504">La bande passante réelle est indiquée dans la propriété **Speed** .</span><span class="sxs-lookup"><span data-stu-id="9521b-504">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="9521b-505">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9521b-505">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-506">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9521b-506">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-507">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-507">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-508">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-509">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="9521b-509">The last requested or desired state for the element.</span></span> <span data-ttu-id="9521b-510">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="9521b-510">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-511">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="9521b-511">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-512">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9521b-512">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-513">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9521b-514">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="9521b-514">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="9521b-515">La bande passante du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="9521b-515">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="9521b-516">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9521b-516">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-517">**État**</span><span class="sxs-lookup"><span data-stu-id="9521b-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-518">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-520">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9521b-520">The current status of the object.</span></span> <span data-ttu-id="9521b-521">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-521">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-522">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9521b-522">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-523">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9521b-523">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-524">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-524">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-525">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9521b-525">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9521b-526">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9521b-526">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-527">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9521b-527">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-528">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-529">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-530">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9521b-530">The current state of the logical device.</span></span> <span data-ttu-id="9521b-531">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-531">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-532">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="9521b-532">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-533">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-533">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-534">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-535">Tableau d’entiers qui indique les Fibre Channel les classes de service (COS) prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9521b-535">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="9521b-536">Les co actifs sont spécifiés par la propriété **ActiveCOS** .</span><span class="sxs-lookup"><span data-stu-id="9521b-536">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="9521b-537">Cette propriété est héritée de la **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="9521b-537">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="9521b-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9521b-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-539"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="9521b-539"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-540"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="9521b-540"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-541"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="9521b-541"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-542"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="9521b-542"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-543"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="9521b-543"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-544"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="9521b-544"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-545"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="9521b-545"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9521b-546">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="9521b-546">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-547">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-547">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9521b-548">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-549">Tableau d’entiers qui indique le Fibre Channel les protocoles FC-4 pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9521b-549">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="9521b-550">Les protocoles qui sont actifs et en cours d’exécution sont spécifiés par la propriété **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="9521b-550">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="9521b-551">Cette propriété est héritée de la **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="9521b-551">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="9521b-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9521b-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9521b-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="9521b-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP sur FC** (5)</span><span class="sxs-lookup"><span data-stu-id="9521b-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="9521b-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-préférences** (9)</span><span class="sxs-lookup"><span data-stu-id="9521b-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Maître IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="9521b-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**Esclave IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="9521b-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**Homologue-3 homologue** (19)</span><span class="sxs-lookup"><span data-stu-id="9521b-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**Maître IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="9521b-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**Esclave du CP IPI-3** (22)</span><span class="sxs-lookup"><span data-stu-id="9521b-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**Homologue CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="9521b-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="9521b-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unité de contrôle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="9521b-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="9521b-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unité de contrôle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="9521b-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Services de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="9521b-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="9521b-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="9521b-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPA-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="9521b-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Contrôle BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="9521b-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU BBL FDDI encapsulé LAN** (81)</span><span class="sxs-lookup"><span data-stu-id="9521b-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU LAN encapsulé BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="9521b-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="9521b-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="9521b-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Fournisseur unique** (255)</span><span class="sxs-lookup"><span data-stu-id="9521b-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9521b-578">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="9521b-578">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-579">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9521b-579">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-580">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9521b-581">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9521b-581">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9521b-582">Unité de transmission maximale (MTU) qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="9521b-582">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="9521b-583">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9521b-583">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-584">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9521b-584">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-585">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-586">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-587">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9521b-587">The scoping system's creation class name.</span></span> <span data-ttu-id="9521b-588">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="9521b-588">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9521b-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-590">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9521b-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-591">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-592">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9521b-592">The scoping system's name.</span></span> <span data-ttu-id="9521b-593">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="9521b-593">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9521b-594">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9521b-594">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-595">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9521b-595">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-596">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-596">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-597">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9521b-597">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9521b-598">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9521b-598">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-599">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="9521b-599">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-600">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9521b-600">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-601">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-601">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-602">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="9521b-602">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="9521b-603">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9521b-603">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-604">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9521b-604">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-605">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-605">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-606">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-607">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="9521b-607">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9521b-608">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9521b-608">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9521b-609">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="9521b-609">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9521b-610">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9521b-610">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9521b-611">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9521b-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9521b-612">Dans certains cas, un port logique peut être identifiable comme un port frontal ou back end.</span><span class="sxs-lookup"><span data-stu-id="9521b-612">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="9521b-613">C’est le cas, par exemple, d’un groupe de stockage qui peut avoir back end ports pour communiquer avec les lecteurs de disque et les ports frontaux pour communiquer avec les hôtes.</span><span class="sxs-lookup"><span data-stu-id="9521b-613">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="9521b-614">S’il n’existe aucune restriction sur l’utilisation du port, la valeur doit être définie sur 4 (non limité).</span><span class="sxs-lookup"><span data-stu-id="9521b-614">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="9521b-615">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9521b-615">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9521b-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9521b-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Frontal uniquement** (2)</span><span class="sxs-lookup"><span data-stu-id="9521b-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Serveur principal uniquement** (3)</span><span class="sxs-lookup"><span data-stu-id="9521b-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9521b-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Non restreint** (4)</span><span class="sxs-lookup"><span data-stu-id="9521b-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9521b-620">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9521b-620">Requirements</span></span>



| <span data-ttu-id="9521b-621">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9521b-621">Requirement</span></span> | <span data-ttu-id="9521b-622">Valeur</span><span class="sxs-lookup"><span data-stu-id="9521b-622">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9521b-623">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9521b-623">Minimum supported client</span></span><br/> | <span data-ttu-id="9521b-624">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9521b-624">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9521b-625">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9521b-625">Minimum supported server</span></span><br/> | <span data-ttu-id="9521b-626">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9521b-626">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9521b-627">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9521b-627">Namespace</span></span><br/>                | <span data-ttu-id="9521b-628">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9521b-628">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9521b-629">MOF</span><span class="sxs-lookup"><span data-stu-id="9521b-629">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9521b-630"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-630"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9521b-631">DLL</span><span class="sxs-lookup"><span data-stu-id="9521b-631">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9521b-632"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9521b-632"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

