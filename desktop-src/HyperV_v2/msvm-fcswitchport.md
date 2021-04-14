---
description: Représente un port sur le commutateur de Fibre Channel virtuel.
ms.assetid: 6b4553b7-2717-4285-9e1a-e2ad22a60997
title: Msvm_FcSwitchPort, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcSwitchPort
- Msvm_FcSwitchPort.SetPowerState
- Msvm_FcSwitchPort.EnableDevice
- Msvm_FcSwitchPort.OnlineDevice
- Msvm_FcSwitchPort.QuiesceDevice
- Msvm_FcSwitchPort.SaveProperties
- Msvm_FcSwitchPort.RestoreProperties
- Msvm_FcSwitchPort.InstanceID
- Msvm_FcSwitchPort.Caption
- Msvm_FcSwitchPort.Description
- Msvm_FcSwitchPort.ElementName
- Msvm_FcSwitchPort.InstallDate
- Msvm_FcSwitchPort.Name
- Msvm_FcSwitchPort.OperationalStatus
- Msvm_FcSwitchPort.StatusDescriptions
- Msvm_FcSwitchPort.Status
- Msvm_FcSwitchPort.HealthState
- Msvm_FcSwitchPort.CommunicationStatus
- Msvm_FcSwitchPort.DetailedStatus
- Msvm_FcSwitchPort.OperatingStatus
- Msvm_FcSwitchPort.PrimaryStatus
- Msvm_FcSwitchPort.EnabledState
- Msvm_FcSwitchPort.OtherEnabledState
- Msvm_FcSwitchPort.RequestedState
- Msvm_FcSwitchPort.EnabledDefault
- Msvm_FcSwitchPort.TimeOfLastStateChange
- Msvm_FcSwitchPort.AvailableRequestedStates
- Msvm_FcSwitchPort.TransitioningToState
- Msvm_FcSwitchPort.SystemCreationClassName
- Msvm_FcSwitchPort.SystemName
- Msvm_FcSwitchPort.CreationClassName
- Msvm_FcSwitchPort.DeviceID
- Msvm_FcSwitchPort.PowerManagementSupported
- Msvm_FcSwitchPort.PowerManagementCapabilities
- Msvm_FcSwitchPort.Availability
- Msvm_FcSwitchPort.StatusInfo
- Msvm_FcSwitchPort.LastErrorCode
- Msvm_FcSwitchPort.ErrorDescription
- Msvm_FcSwitchPort.ErrorCleared
- Msvm_FcSwitchPort.OtherIdentifyingInfo
- Msvm_FcSwitchPort.PowerOnHours
- Msvm_FcSwitchPort.TotalPowerOnHours
- Msvm_FcSwitchPort.IdentifyingDescriptions
- Msvm_FcSwitchPort.AdditionalAvailability
- Msvm_FcSwitchPort.MaxQuiesceTime
- Msvm_FcSwitchPort.Speed
- Msvm_FcSwitchPort.MaxSpeed
- Msvm_FcSwitchPort.RequestedSpeed
- Msvm_FcSwitchPort.UsageRestriction
- Msvm_FcSwitchPort.PortType
- Msvm_FcSwitchPort.OtherPortType
- Msvm_FcSwitchPort.OtherNetworkPortType
- Msvm_FcSwitchPort.PortNumber
- Msvm_FcSwitchPort.LinkTechnology
- Msvm_FcSwitchPort.OtherLinkTechnology
- Msvm_FcSwitchPort.PermanentAddress
- Msvm_FcSwitchPort.NetworkAddresses
- Msvm_FcSwitchPort.FullDuplex
- Msvm_FcSwitchPort.AutoSense
- Msvm_FcSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_FcSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_FcSwitchPort.SupportedCOS
- Msvm_FcSwitchPort.ActiveCOS
- Msvm_FcSwitchPort.SupportedFC4Types
- Msvm_FcSwitchPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 443ae1065b7c7a6a4bb1523a672e388cacb91667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526841"
---
# <a name="msvm_fcswitchport-class"></a><span data-ttu-id="c3c40-103">MSVM \_ FcSwitchPort, classe</span><span class="sxs-lookup"><span data-stu-id="c3c40-103">Msvm\_FcSwitchPort class</span></span>

> [!NOTE]
> <span data-ttu-id="c3c40-104">Cet article contient des références au terme esclave, un terme que Microsoft n’utilise plus.</span><span class="sxs-lookup"><span data-stu-id="c3c40-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="c3c40-105">Lorsque le terme sera supprimé du logiciel, nous le supprimerons de cet article.</span><span class="sxs-lookup"><span data-stu-id="c3c40-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="c3c40-106">Représente un port sur le commutateur de Fibre Channel virtuel.</span><span class="sxs-lookup"><span data-stu-id="c3c40-106">Represents a port on the virtual Fibre Channel switch.</span></span>

<span data-ttu-id="c3c40-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c3c40-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c40-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3c40-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcSwitchPort : CIM_FCPort
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
  uint16   LinkTechnology;
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

## <a name="members"></a><span data-ttu-id="c3c40-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c3c40-109">Members</span></span>

<span data-ttu-id="c3c40-110">La classe **MSVM \_ FcSwitchPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c3c40-110">The **Msvm\_FcSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="c3c40-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c3c40-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c3c40-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3c40-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c3c40-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c3c40-113">Methods</span></span>

<span data-ttu-id="c3c40-114">La classe **MSVM \_ FcSwitchPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c3c40-114">The **Msvm\_FcSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="c3c40-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="c3c40-115">Method</span></span>                                                             | <span data-ttu-id="c3c40-116">Description</span><span class="sxs-lookup"><span data-stu-id="c3c40-116">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="c3c40-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="c3c40-117">**EnableDevice**</span></span>                                                   | <span data-ttu-id="c3c40-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c3c40-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3c40-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="c3c40-119">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="c3c40-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c3c40-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3c40-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="c3c40-121">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="c3c40-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c3c40-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="c3c40-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c3c40-123">**RequestStateChange**</span></span>](msvm-fcswitchport-requeststatechange.md) | <span data-ttu-id="c3c40-124">demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="c3c40-124">requests a state change.</span></span><br/>      |
| [<span data-ttu-id="c3c40-125">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="c3c40-125">**Reset**</span></span>](msvm-fcswitchport-reset.md)                           | <span data-ttu-id="c3c40-126">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="c3c40-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="c3c40-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="c3c40-127">**RestoreProperties**</span></span>                                              | <span data-ttu-id="c3c40-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c3c40-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3c40-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="c3c40-129">**SaveProperties**</span></span>                                                 | <span data-ttu-id="c3c40-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c3c40-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3c40-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c3c40-131">**SetPowerState**</span></span>                                                  | <span data-ttu-id="c3c40-132">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c3c40-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c3c40-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3c40-133">Properties</span></span>

<span data-ttu-id="c3c40-134">La classe **MSVM \_ FcSwitchPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c3c40-134">The **Msvm\_FcSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="c3c40-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-136">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-138">Tableau d’entiers qui indique les classes de service qui sont actives.</span><span class="sxs-lookup"><span data-stu-id="c3c40-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="c3c40-139">Les COS pris en charge sont spécifiés par la propriété **SupportedCOS** .</span><span class="sxs-lookup"><span data-stu-id="c3c40-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="c3c40-140">Cette propriété est héritée de la **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="c3c40-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="c3c40-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="c3c40-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="c3c40-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="c3c40-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="c3c40-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="c3c40-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="c3c40-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3c40-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="c3c40-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-150">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-152">Tableau d’entiers qui indique le Fibre Channel les protocoles FC-4 en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c3c40-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="c3c40-153">La liste de tous les protocoles pris en charge est spécifiée par la propriété **SupportedFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="c3c40-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="c3c40-154">Cette propriété est héritée de la **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="c3c40-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c3c40-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="c3c40-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP sur FC** (5)</span><span class="sxs-lookup"><span data-stu-id="c3c40-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="c3c40-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-préférences** (9)</span><span class="sxs-lookup"><span data-stu-id="c3c40-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Maître IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="c3c40-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**Esclave IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="c3c40-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**Homologue-3 homologue** (19)</span><span class="sxs-lookup"><span data-stu-id="c3c40-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**Maître IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="c3c40-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**Esclave du CP IPI-3** (22)</span><span class="sxs-lookup"><span data-stu-id="c3c40-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**Homologue CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="c3c40-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="c3c40-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unité de contrôle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="c3c40-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="c3c40-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unité de contrôle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="c3c40-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Services de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="c3c40-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="c3c40-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="c3c40-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPA-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="c3c40-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Contrôle BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="c3c40-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU BBL FDDI encapsulé LAN** (81)</span><span class="sxs-lookup"><span data-stu-id="c3c40-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU LAN encapsulé BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="c3c40-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="c3c40-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="c3c40-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Fournisseur unique** (255)</span><span class="sxs-lookup"><span data-stu-id="c3c40-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3c40-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="c3c40-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-182">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3c40-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-184">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c3c40-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-185">Unité de transmission maximale (MTU) active ou négociée qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="c3c40-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="c3c40-186">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c3c40-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="c3c40-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-188">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-190">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3c40-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="c3c40-191">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-192">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="c3c40-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-193">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c3c40-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-195">Indique si le port peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché.</span><span class="sxs-lookup"><span data-stu-id="c3c40-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="c3c40-196">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c3c40-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-197">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="c3c40-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-198">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-200">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3c40-200">The primary availability and status of the device.</span></span> <span data-ttu-id="c3c40-201">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="c3c40-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-203">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-205">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="c3c40-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="c3c40-206">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="c3c40-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c3c40-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-210">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c3c40-210">A short description of the object.</span></span> <span data-ttu-id="c3c40-211">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c3c40-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-213">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-215">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c3c40-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c3c40-216">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3c40-217">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="c3c40-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="c3c40-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="c3c40-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="c3c40-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c3c40-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c3c40-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3c40-225">)</span><span class="sxs-lookup"><span data-stu-id="c3c40-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3c40-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c3c40-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-229">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="c3c40-229">The scoping system's creation class name.</span></span> <span data-ttu-id="c3c40-230">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c3c40-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-231">**Description**</span><span class="sxs-lookup"><span data-stu-id="c3c40-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-234">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="c3c40-234">A description of the object.</span></span> <span data-ttu-id="c3c40-235">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c3c40-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-237">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-239">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c3c40-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c3c40-240">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3c40-241">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="c3c40-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="c3c40-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="c3c40-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="c3c40-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="c3c40-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c3c40-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c3c40-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3c40-250">)</span><span class="sxs-lookup"><span data-stu-id="c3c40-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3c40-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c3c40-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-254">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c3c40-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="c3c40-255">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c3c40-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c3c40-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-259">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c3c40-259">A display name for the object.</span></span> <span data-ttu-id="c3c40-260">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="c3c40-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-262">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-264">Configuration par défaut ou de démarrage d’un administrateur pour la propriété **EnabledState** d’un élément.</span><span class="sxs-lookup"><span data-stu-id="c3c40-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="c3c40-265">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="c3c40-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c3c40-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-267">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-269">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="c3c40-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c3c40-270">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c3c40-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="c3c40-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3c40-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="c3c40-272">Signification</span><span class="sxs-lookup"><span data-stu-id="c3c40-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="c3c40-273"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="c3c40-274">Impossible de déterminer l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c3c40-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="c3c40-275"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="c3c40-276"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="c3c40-277">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c3c40-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="c3c40-278"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="c3c40-279">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c3c40-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="c3c40-280"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="c3c40-281">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="c3c40-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="c3c40-282"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="c3c40-283">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="c3c40-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="c3c40-284"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="c3c40-285">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="c3c40-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="c3c40-286"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="c3c40-287">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="c3c40-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="c3c40-288"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="c3c40-289">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="c3c40-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="c3c40-290"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="c3c40-291">L’élément est activé, mais en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="c3c40-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="c3c40-292">Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="c3c40-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="c3c40-293">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c3c40-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="c3c40-294">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="c3c40-295">L’élément est en train d’accéder à un état activé (2).</span><span class="sxs-lookup"><span data-stu-id="c3c40-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="c3c40-296">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c3c40-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="c3c40-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c3c40-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-298">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c3c40-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-300">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="c3c40-301">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c3c40-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-305">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="c3c40-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="c3c40-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="c3c40-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-308">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c3c40-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-310">Indique si le port fonctionne en mode duplex intégral.</span><span class="sxs-lookup"><span data-stu-id="c3c40-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="c3c40-311">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c3c40-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c3c40-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-313">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-315">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c3c40-315">The current health of the element.</span></span> <span data-ttu-id="c3c40-316">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c3c40-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-318">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="c3c40-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-320">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="c3c40-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="c3c40-321">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c3c40-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-323">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3c40-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-325">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c3c40-325">The date and time when the object was installed.</span></span> <span data-ttu-id="c3c40-326">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="c3c40-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="c3c40-327">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c3c40-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-329">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-331">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="c3c40-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-332">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="c3c40-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c3c40-333">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c3c40-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-335">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3c40-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-337">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c3c40-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="c3c40-338">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-339">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="c3c40-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-340">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-342">Spécifie le type de technologie de lien pour le port.</span><span class="sxs-lookup"><span data-stu-id="c3c40-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="c3c40-343">Lorsque la valeur 1 (autre) est définie, la propriété **OtherLinkTechnology** contient une description de chaîne du type de lien.</span><span class="sxs-lookup"><span data-stu-id="c3c40-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="c3c40-344">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c3c40-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c3c40-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-347"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="c3c40-347"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-348"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="c3c40-348"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-349"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="c3c40-349"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-350"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="c3c40-350"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-351"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="c3c40-351"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-352"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="c3c40-352"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-353"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Relais de trames** (8)</span><span class="sxs-lookup"><span data-stu-id="c3c40-353"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-354"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarouge** (9)</span><span class="sxs-lookup"><span data-stu-id="c3c40-354"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-355"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="c3c40-355"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-356"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Réseau local sans fil** (11)</span><span class="sxs-lookup"><span data-stu-id="c3c40-356"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3c40-357">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="c3c40-357">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-358">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3c40-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-360">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-360">This property has been deprecated.</span></span> <span data-ttu-id="c3c40-361">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-362">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="c3c40-362">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-363">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3c40-363">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-365">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="c3c40-365">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-366">Bande passante maximale du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="c3c40-366">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c3c40-367">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c3c40-367">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-368">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c3c40-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-369">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-371">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="c3c40-371">The label by which the object is known.</span></span> <span data-ttu-id="c3c40-372">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-373">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="c3c40-373">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-374">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="c3c40-374">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-376">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="c3c40-376">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-377">Tableau de chaînes qui contient les adresses MAC du port.</span><span class="sxs-lookup"><span data-stu-id="c3c40-377">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="c3c40-378">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c3c40-378">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-379">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c3c40-379">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-380">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-382">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c3c40-382">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c3c40-383">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3c40-384">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-386"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="c3c40-386"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-387"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="c3c40-387"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-388"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="c3c40-388"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-389"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="c3c40-389"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-390"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="c3c40-390"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-391"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="c3c40-391"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-392"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="c3c40-392"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-393"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="c3c40-393"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-394"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="c3c40-394"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-395"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="c3c40-395"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-396"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="c3c40-396"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-397"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="c3c40-397"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-398"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="c3c40-398"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-399"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="c3c40-399"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-400"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="c3c40-400"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-401"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="c3c40-401"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-402"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c3c40-402"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-403"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c3c40-403"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3c40-404">)</span><span class="sxs-lookup"><span data-stu-id="c3c40-404">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3c40-405">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c3c40-405">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-406">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-408">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c3c40-408">The current statuses of the object.</span></span> <span data-ttu-id="c3c40-409">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-410">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="c3c40-410">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-411">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-413">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="c3c40-413">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="c3c40-414">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="c3c40-414">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="c3c40-415">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="c3c40-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-416">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c3c40-416">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-417">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="c3c40-417">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-419">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="c3c40-419">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="c3c40-420">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-421">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="c3c40-421">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-422">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-423">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-424">Valeur de chaîne qui décrit **LinkTechnology** lorsqu’il a la valeur 1, (other).</span><span class="sxs-lookup"><span data-stu-id="c3c40-424">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="c3c40-425">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c3c40-425">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-426">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="c3c40-426">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-427">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-429">L’utilisation de cette propriété est déconseillée à la place de la propriété **portType** .</span><span class="sxs-lookup"><span data-stu-id="c3c40-429">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="c3c40-430">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c3c40-430">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-431">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="c3c40-431">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-432">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-433">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-434">Décrit le type de module lorsque **portType** a la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="c3c40-434">Describes the type of module when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="c3c40-435">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c3c40-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-436">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="c3c40-436">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-437">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-438">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-439">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="c3c40-439">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-440">Adresse réseau qui est codée en dur dans un port.</span><span class="sxs-lookup"><span data-stu-id="c3c40-440">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="c3c40-441">Cette adresse codée en dur peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="c3c40-441">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="c3c40-442">Lorsque cette modification est apportée, le champ doit être mis à jour en même temps.</span><span class="sxs-lookup"><span data-stu-id="c3c40-442">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="c3c40-443">Cette propriété doit avoir la **valeur null** s’il n’existe aucune adresse codée en dur pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="c3c40-443">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="c3c40-444">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c3c40-444">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-445">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="c3c40-445">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-446">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-448">Le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="c3c40-448">The port number.</span></span> <span data-ttu-id="c3c40-449">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c3c40-449">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-450">**PortType**</span><span class="sxs-lookup"><span data-stu-id="c3c40-450">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-451">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-452">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-453">Mode spécifique actuellement activé pour le port.</span><span class="sxs-lookup"><span data-stu-id="c3c40-453">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="c3c40-454">Si la valeur 1 (autre) est définie, la propriété **OtherPortType** associée contient une description de chaîne du type de port.</span><span class="sxs-lookup"><span data-stu-id="c3c40-454">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="c3c40-455">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c3c40-455">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c3c40-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-458"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 cuivre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="c3c40-458"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-459"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="c3c40-459"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-460"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="c3c40-460"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-461"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="c3c40-461"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-462"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="c3c40-462"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-463"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="c3c40-463"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-464"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="c3c40-464"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-465"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="c3c40-465"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-466"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="c3c40-466"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-467"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="c3c40-467"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-468"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="c3c40-468"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-469"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="c3c40-469"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-470"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="c3c40-470"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-471"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="c3c40-471"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-472"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="c3c40-472"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-473"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="c3c40-473"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-474"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="c3c40-474"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-475"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="c3c40-475"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-476"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-SEM** (111)</span><span class="sxs-lookup"><span data-stu-id="c3c40-476"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c3c40-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3c40-478">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c3c40-478">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-479">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-479">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-480">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-481">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3c40-481">The power management capabilities of the device.</span></span> <span data-ttu-id="c3c40-482">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-482">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-483">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c3c40-483">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-484">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c3c40-484">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-485">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-486">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="c3c40-486">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="c3c40-487">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-488">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c3c40-488">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-489">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3c40-489">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-490">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-491">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="c3c40-491">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="c3c40-492">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-493">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c3c40-493">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-494">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-495">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-496">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="c3c40-496">Provides high level status information.</span></span> <span data-ttu-id="c3c40-497">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="c3c40-497">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c3c40-498">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-498">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3c40-499">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-499">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-500"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-500"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-501"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="c3c40-501"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-502"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="c3c40-502"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-503"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="c3c40-503"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-504"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c3c40-504"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-505"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c3c40-505"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3c40-506">)</span><span class="sxs-lookup"><span data-stu-id="c3c40-506">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3c40-507">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="c3c40-507">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-508">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3c40-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-509">Type d’accès : écriture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-509">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-510">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="c3c40-510">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-511">Bande passante demandée du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="c3c40-511">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c3c40-512">La bande passante réelle est indiquée dans la propriété **Speed** .</span><span class="sxs-lookup"><span data-stu-id="c3c40-512">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="c3c40-513">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c3c40-513">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-514">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c3c40-514">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-515">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-516">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-517">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="c3c40-517">The last requested or desired state for the element.</span></span> <span data-ttu-id="c3c40-518">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="c3c40-518">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-519">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="c3c40-519">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-520">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3c40-520">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-521">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-522">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="c3c40-522">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-523">La bande passante du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="c3c40-523">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c3c40-524">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c3c40-524">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-525">**État**</span><span class="sxs-lookup"><span data-stu-id="c3c40-525">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-526">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-527">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-528">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c3c40-528">The current status of the object.</span></span> <span data-ttu-id="c3c40-529">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-530">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c3c40-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-531">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="c3c40-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-532">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-533">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c3c40-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c3c40-534">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3c40-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-535">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c3c40-535">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-536">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-537">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-538">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c3c40-538">The current state of the logical device.</span></span> <span data-ttu-id="c3c40-539">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-539">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-540">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="c3c40-540">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-541">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-542">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-543">Tableau d’entiers qui indique les Fibre Channel les classes de service (COS) prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c3c40-543">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="c3c40-544">Les co actifs sont spécifiés par la propriété **ActiveCOS** .</span><span class="sxs-lookup"><span data-stu-id="c3c40-544">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="c3c40-545">Cette propriété est héritée de la **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="c3c40-545">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-547"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="c3c40-547"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-548"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="c3c40-548"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-549"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="c3c40-549"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-550"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="c3c40-550"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-551"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="c3c40-551"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-552"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="c3c40-552"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-553"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="c3c40-553"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3c40-554">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="c3c40-554">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-555">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-555">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-556">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-557">Tableau d’entiers qui indique le Fibre Channel les protocoles FC-4 pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c3c40-557">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="c3c40-558">Les protocoles qui sont actifs et en cours d’exécution sont spécifiés par la propriété **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="c3c40-558">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="c3c40-559">Cette propriété est héritée de la **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="c3c40-559">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-560"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-560"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-561"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c3c40-561"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-562"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="c3c40-562"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-563"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP sur FC** (5)</span><span class="sxs-lookup"><span data-stu-id="c3c40-563"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-564"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="c3c40-564"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-565"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-préférences** (9)</span><span class="sxs-lookup"><span data-stu-id="c3c40-565"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-566"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Maître IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="c3c40-566"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-567"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**Esclave IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="c3c40-567"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-568"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**Homologue-3 homologue** (19)</span><span class="sxs-lookup"><span data-stu-id="c3c40-568"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-569"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**Maître IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="c3c40-569"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-570"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**Esclave du CP IPI-3** (22)</span><span class="sxs-lookup"><span data-stu-id="c3c40-570"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-571"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**Homologue CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="c3c40-571"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-572"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="c3c40-572"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-573"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unité de contrôle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="c3c40-573"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-574"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="c3c40-574"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-575"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unité de contrôle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="c3c40-575"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-576"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Services de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="c3c40-576"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-577"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="c3c40-577"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-578"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="c3c40-578"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-579"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPA-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="c3c40-579"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-580"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Contrôle BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="c3c40-580"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-581"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU BBL FDDI encapsulé LAN** (81)</span><span class="sxs-lookup"><span data-stu-id="c3c40-581"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-582"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU LAN encapsulé BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="c3c40-582"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-583"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="c3c40-583"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-584"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="c3c40-584"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-585"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Fournisseur unique** (255)</span><span class="sxs-lookup"><span data-stu-id="c3c40-585"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3c40-586">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="c3c40-586">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-587">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3c40-587">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-588">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-589">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c3c40-589">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-590">Unité de transmission maximale (MTU) qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="c3c40-590">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="c3c40-591">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c3c40-591">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-592">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c3c40-592">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-593">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-593">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-594">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-594">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-595">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="c3c40-595">The scoping system's creation class name.</span></span> <span data-ttu-id="c3c40-596">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c3c40-596">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-597">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c3c40-597">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-598">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3c40-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-599">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-599">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-600">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="c3c40-600">The scoping system's name.</span></span> <span data-ttu-id="c3c40-601">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c3c40-601">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-602">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c3c40-602">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-603">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3c40-603">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-604">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-604">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-605">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c3c40-605">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c3c40-606">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="c3c40-606">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-607">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c3c40-607">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-608">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3c40-608">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-609">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-609">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-610">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="c3c40-610">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="c3c40-611">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3c40-611">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-612">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="c3c40-612">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-613">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-614">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-615">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="c3c40-615">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c3c40-616">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="c3c40-616">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3c40-617">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="c3c40-617">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c40-618">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3c40-618">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-619">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3c40-619">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c40-620">Dans certains cas, un port logique peut être identifiable comme un port frontal ou back end.</span><span class="sxs-lookup"><span data-stu-id="c3c40-620">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="c3c40-621">C’est le cas, par exemple, d’un groupe de stockage qui peut avoir back end ports pour communiquer avec les lecteurs de disque et les ports frontaux pour communiquer avec les hôtes.</span><span class="sxs-lookup"><span data-stu-id="c3c40-621">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="c3c40-622">S’il n’existe aucune restriction sur l’utilisation du port, la valeur doit être définie sur 4 (non limité).</span><span class="sxs-lookup"><span data-stu-id="c3c40-622">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="c3c40-623">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c3c40-623">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="c3c40-624"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3c40-624"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-625"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Frontal uniquement** (2)</span><span class="sxs-lookup"><span data-stu-id="c3c40-625"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-626"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Serveur principal uniquement** (3)</span><span class="sxs-lookup"><span data-stu-id="c3c40-626"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3c40-627"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Non restreint** (4)</span><span class="sxs-lookup"><span data-stu-id="c3c40-627"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3c40-628">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3c40-628">Requirements</span></span>



| <span data-ttu-id="c3c40-629">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3c40-629">Requirement</span></span> | <span data-ttu-id="c3c40-630">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3c40-630">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c40-631">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3c40-631">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c40-632">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3c40-632">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c3c40-633">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3c40-633">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c40-634">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3c40-634">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3c40-635">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c3c40-635">Namespace</span></span><br/>                | <span data-ttu-id="c3c40-636">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c3c40-636">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c3c40-637">MOF</span><span class="sxs-lookup"><span data-stu-id="c3c40-637">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3c40-638"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-638"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3c40-639">DLL</span><span class="sxs-lookup"><span data-stu-id="c3c40-639">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3c40-640"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3c40-640"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

