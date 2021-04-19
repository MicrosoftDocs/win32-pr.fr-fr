---
description: Représente les fonctionnalités et la gestion d’un périphérique de port Fibre Channel (FC).
ms.assetid: 32a11971-9e18-410d-a3cd-4921a7e986f0
title: Classe CIM_FCPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FCPort
- CIM_FCPort.PortType
- CIM_FCPort.SupportedCOS
- CIM_FCPort.ActiveCOS
- CIM_FCPort.SupportedFC4Types
- CIM_FCPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6a858cbb4603743e1ddd11cac71500a9e39325a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517220"
---
# <a name="cim_fcport-class"></a><span data-ttu-id="ddda9-103">\_Classe CIM FCPort</span><span class="sxs-lookup"><span data-stu-id="ddda9-103">CIM\_FCPort class</span></span>

> [!NOTE]
> <span data-ttu-id="ddda9-104">Cet article contient des références au terme esclave, un terme que Microsoft n’utilise plus.</span><span class="sxs-lookup"><span data-stu-id="ddda9-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="ddda9-105">Lorsque le terme sera supprimé du logiciel, nous le supprimerons de cet article.</span><span class="sxs-lookup"><span data-stu-id="ddda9-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="ddda9-106">Représente les fonctionnalités et la gestion d’un périphérique de port Fibre Channel (FC).</span><span class="sxs-lookup"><span data-stu-id="ddda9-106">Represents the capabilities and management of a fibre channel (FC) port device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddda9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddda9-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::FC"), AMENDMENT]
class CIM_FCPort : CIM_NetworkPort
{
  uint16 PortType;
  uint16 SupportedCOS[];
  uint16 ActiveCOS[];
  uint16 SupportedFC4Types[];
  uint16 ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="ddda9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ddda9-108">Members</span></span>

> [!NOTE]
> <span data-ttu-id="ddda9-109">Cet article contient des références au terme esclave, un terme que Microsoft n’utilise plus.</span><span class="sxs-lookup"><span data-stu-id="ddda9-109">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="ddda9-110">Lorsque le terme sera supprimé du logiciel, nous le supprimerons de cet article.</span><span class="sxs-lookup"><span data-stu-id="ddda9-110">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="ddda9-111">La classe **CIM \_ FCPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ddda9-111">The **CIM\_FCPort** class has these types of members:</span></span>

-   [<span data-ttu-id="ddda9-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ddda9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ddda9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ddda9-113">Properties</span></span>

<span data-ttu-id="ddda9-114">La classe **CIM \_ FCPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ddda9-114">The **CIM\_FCPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddda9-115">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="ddda9-115">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddda9-116">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddda9-116">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddda9-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddda9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddda9-118">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ FCPort**.**SupportedCOS**")</span><span class="sxs-lookup"><span data-stu-id="ddda9-118">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedCOS**")</span></span>
</dt> </dl>

<span data-ttu-id="ddda9-119">Les paramètres de la classe active de service (COS) pour le Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="ddda9-119">The active class of service (COS) settings for the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddda9-120">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ddda9-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="ddda9-121">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="ddda9-121">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="ddda9-122">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="ddda9-122">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="ddda9-123">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="ddda9-123">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="ddda9-124">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="ddda9-124">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="ddda9-125">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="ddda9-125">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="ddda9-126">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="ddda9-126">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="ddda9-127">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="ddda9-127">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddda9-128">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="ddda9-128">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddda9-129">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddda9-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddda9-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddda9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddda9-131">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ FCPort**.**SupportedFC4Types**")</span><span class="sxs-lookup"><span data-stu-id="ddda9-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedFC4Types**")</span></span>
</dt> </dl>

<span data-ttu-id="ddda9-132">Les protocoles FC-4 qui s’exécutent sur le Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="ddda9-132">The FC-4 protocols that are running on the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddda9-133">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ddda9-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ddda9-134">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ddda9-134">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="ddda9-135">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="ddda9-135">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="ddda9-136">**IP sur FC** (5)</span><span class="sxs-lookup"><span data-stu-id="ddda9-136">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="ddda9-137">**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="ddda9-137">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="ddda9-138">**SCSI-préférences** (9)</span><span class="sxs-lookup"><span data-stu-id="ddda9-138">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="ddda9-139">**Maître IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="ddda9-139">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="ddda9-140">**Esclave IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="ddda9-140">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="ddda9-141">**Homologue-3 homologue** (19)</span><span class="sxs-lookup"><span data-stu-id="ddda9-141">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="ddda9-142">**Maître IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="ddda9-142">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="ddda9-143">**Esclave du CP IPI-3** (22)</span><span class="sxs-lookup"><span data-stu-id="ddda9-143">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="ddda9-144">**Homologue CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="ddda9-144">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="ddda9-145">**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="ddda9-145">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="ddda9-146">**Unité de contrôle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="ddda9-146">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="ddda9-147">**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="ddda9-147">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="ddda9-148">**Unité de contrôle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="ddda9-148">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="ddda9-149">**Services de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="ddda9-149">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="ddda9-150">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="ddda9-150">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="ddda9-151">**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="ddda9-151">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="ddda9-152">**HIPPA-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="ddda9-152">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="ddda9-153">**Contrôle BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="ddda9-153">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="ddda9-154">**PDU BBL FDDI encapsulé LAN** (81)</span><span class="sxs-lookup"><span data-stu-id="ddda9-154">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="ddda9-155">**PDU LAN encapsulé BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="ddda9-155">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="ddda9-156">**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="ddda9-156">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="ddda9-157">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="ddda9-157">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="ddda9-158">**Fournisseur unique** (255)</span><span class="sxs-lookup"><span data-stu-id="ddda9-158">**Vendor Unique** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddda9-159">**PortType**</span><span class="sxs-lookup"><span data-stu-id="ddda9-159">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddda9-160">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddda9-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddda9-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddda9-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddda9-162">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="ddda9-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="ddda9-163">Mode activé pour le port.</span><span class="sxs-lookup"><span data-stu-id="ddda9-163">The enabled mode for the port.</span></span> <span data-ttu-id="ddda9-164">Les modes de port sont définis par les normes ANSI X3.</span><span class="sxs-lookup"><span data-stu-id="ddda9-164">The port modes are defined by ANSI X3 standards.</span></span> <span data-ttu-id="ddda9-165">Si le port est connecté, il s’agit du type de port négocié ; sinon, le type de port configuré est signalé.</span><span class="sxs-lookup"><span data-stu-id="ddda9-165">If the port is logged in, this will be the negotiated port type, otherwise the configured port type will be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddda9-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ddda9-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ddda9-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ddda9-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ddda9-168">La propriété associée **OtherPortType** contient une description de chaîne du type de port.</span><span class="sxs-lookup"><span data-stu-id="ddda9-168">The related property **OtherPortType** contains a string description of the type of port</span></span>

</dd> <dt>

<span id="N"></span><span id="n"></span>

<span data-ttu-id="ddda9-169"><span id="N"></span><span id="n"></span>**N** (10)</span><span class="sxs-lookup"><span data-stu-id="ddda9-169"><span id="N"></span><span id="n"></span>**N** (10)</span></span>


</dt> <dd>

<span data-ttu-id="ddda9-170">Port du nœud</span><span class="sxs-lookup"><span data-stu-id="ddda9-170">Node Port</span></span>

</dd> <dt>

<span id="NL"></span><span id="nl"></span>

<span data-ttu-id="ddda9-171"><span id="NL"></span><span id="nl"></span>**NL** (11)</span><span class="sxs-lookup"><span data-stu-id="ddda9-171"><span id="NL"></span><span id="nl"></span>**NL** (11)</span></span>


</dt> <dd>

<span data-ttu-id="ddda9-172">Port node prenant en charge la boucle arbitrée FC</span><span class="sxs-lookup"><span data-stu-id="ddda9-172">Node Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="F_NL"></span><span id="f_nl"></span>

<span data-ttu-id="ddda9-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span><span class="sxs-lookup"><span data-stu-id="ddda9-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>

<span data-ttu-id="ddda9-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**NX** (13)</span><span class="sxs-lookup"><span data-stu-id="ddda9-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**Nx** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ddda9-175">Le port peut négocier pour devenir un port de nœud (N) ou un port de nœud prenant en charge la boucle arbitrée FC (NL)</span><span class="sxs-lookup"><span data-stu-id="ddda9-175">Port may negotiate to become either a node port (N) or a node port supporting FC arbitrated loop (NL)</span></span>

</dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="ddda9-176"><span id="E"></span><span id="e"></span>**E** (14)</span><span class="sxs-lookup"><span data-stu-id="ddda9-176"><span id="E"></span><span id="e"></span>**E** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ddda9-177">Port d’extension connectant les éléments de l’infrastructure (par exemple, commutateurs FC)</span><span class="sxs-lookup"><span data-stu-id="ddda9-177">Expansion Port connecting fabric elements (for example, FC switches)</span></span>

</dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="ddda9-178"><span id="F"></span><span id="f"></span>**F** (15)</span><span class="sxs-lookup"><span data-stu-id="ddda9-178"><span id="F"></span><span id="f"></span>**F** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ddda9-179">Port d’infrastructure (élément)</span><span class="sxs-lookup"><span data-stu-id="ddda9-179">Fabric (element) Port</span></span>

</dd> <dt>

<span id="FL"></span><span id="fl"></span>

<span data-ttu-id="ddda9-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span><span class="sxs-lookup"><span data-stu-id="ddda9-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ddda9-181">Port Fabric (element) prenant en charge la boucle arbitrée FC</span><span class="sxs-lookup"><span data-stu-id="ddda9-181">Fabric (element) Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="ddda9-182"><span id="B"></span><span id="b"></span>**B** (17)</span><span class="sxs-lookup"><span data-stu-id="ddda9-182"><span id="B"></span><span id="b"></span>**B** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ddda9-183">Port de pont</span><span class="sxs-lookup"><span data-stu-id="ddda9-183">Bridge port</span></span>

</dd> <dt>

<span id="G"></span><span id="g"></span>

<span data-ttu-id="ddda9-184"><span id="G"></span><span id="g"></span>**G** (18)</span><span class="sxs-lookup"><span data-stu-id="ddda9-184"><span id="G"></span><span id="g"></span>**G** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ddda9-185">Le port peut négocier pour devenir un port d’extension (E) ou un port de structure (F)</span><span class="sxs-lookup"><span data-stu-id="ddda9-185">Port may negotiate to become either an expansion port (E), or a fabric port (F)</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ddda9-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ddda9-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddda9-187">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="ddda9-187">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddda9-188">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddda9-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddda9-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddda9-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddda9-190">Les paramètres de classe de service (COS) pris en charge par le Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="ddda9-190">The class of service (COS) settings that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddda9-191">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ddda9-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="ddda9-192">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="ddda9-192">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="ddda9-193">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="ddda9-193">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="ddda9-194">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="ddda9-194">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="ddda9-195">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="ddda9-195">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="ddda9-196">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="ddda9-196">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="ddda9-197">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="ddda9-197">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="ddda9-198">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="ddda9-198">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddda9-199">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="ddda9-199">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddda9-200">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddda9-200">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddda9-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddda9-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddda9-202">Les protocoles FC-4 pris en charge par le Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="ddda9-202">The FC-4 protocols that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddda9-203">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ddda9-203">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ddda9-204">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ddda9-204">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="ddda9-205">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="ddda9-205">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="ddda9-206">**IP sur FC** (5)</span><span class="sxs-lookup"><span data-stu-id="ddda9-206">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="ddda9-207">**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="ddda9-207">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="ddda9-208">**SCSI-préférences** (9)</span><span class="sxs-lookup"><span data-stu-id="ddda9-208">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="ddda9-209">**Maître IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="ddda9-209">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="ddda9-210">**Esclave IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="ddda9-210">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="ddda9-211">**Homologue-3 homologue** (19)</span><span class="sxs-lookup"><span data-stu-id="ddda9-211">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="ddda9-212">**Maître IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="ddda9-212">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="ddda9-213">**Esclave du CP IPI-3** (22)</span><span class="sxs-lookup"><span data-stu-id="ddda9-213">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="ddda9-214">**Homologue CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="ddda9-214">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="ddda9-215">**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="ddda9-215">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="ddda9-216">**Unité de contrôle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="ddda9-216">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="ddda9-217">**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="ddda9-217">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="ddda9-218">**Unité de contrôle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="ddda9-218">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="ddda9-219">**Services de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="ddda9-219">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="ddda9-220">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="ddda9-220">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="ddda9-221">**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="ddda9-221">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="ddda9-222">**HIPPA-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="ddda9-222">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="ddda9-223">**Contrôle BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="ddda9-223">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="ddda9-224">**PDU BBL FDDI encapsulé LAN** (81)</span><span class="sxs-lookup"><span data-stu-id="ddda9-224">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="ddda9-225">**PDU LAN encapsulé BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="ddda9-225">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="ddda9-226">**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="ddda9-226">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="ddda9-227">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="ddda9-227">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="ddda9-228">**Fournisseur unique** (255)</span><span class="sxs-lookup"><span data-stu-id="ddda9-228">**Vendor Unique** (255)</span></span>


<span data-ttu-id="ddda9-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ddda9-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ddda9-230">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddda9-230">Requirements</span></span>



| <span data-ttu-id="ddda9-231">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddda9-231">Requirement</span></span> | <span data-ttu-id="ddda9-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddda9-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddda9-233">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddda9-233">Minimum supported client</span></span><br/> | <span data-ttu-id="ddda9-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ddda9-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ddda9-235">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddda9-235">Minimum supported server</span></span><br/> | <span data-ttu-id="ddda9-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ddda9-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ddda9-237">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ddda9-237">Namespace</span></span><br/>                | <span data-ttu-id="ddda9-238">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ddda9-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ddda9-239">MOF</span><span class="sxs-lookup"><span data-stu-id="ddda9-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddda9-240"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddda9-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddda9-241">DLL</span><span class="sxs-lookup"><span data-stu-id="ddda9-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddda9-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ddda9-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ddda9-243">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddda9-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddda9-244">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="ddda9-244">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

