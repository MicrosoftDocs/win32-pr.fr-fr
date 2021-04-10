---
description: Représente les fonctionnalités et la gestion d’un processeur.
ms.assetid: 70cf9776-eeda-42c2-90c4-704ecf1cdafe
title: Classe CIM_Processor (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.Role
- CIM_Processor.Family
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.UpgradeMethod
- CIM_Processor.MaxClockSpeed
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.AddressWidth
- CIM_Processor.LoadPercentage
- CIM_Processor.Stepping
- CIM_Processor.UniqueID
- CIM_Processor.CPUStatus
- CIM_Processor.ExternalBusClockSpeed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00e78834c0a3a782c5fdc48cd52a67b85aa2a241
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749644"
---
# <a name="cim_processor-class-hyper-v-management"></a><span data-ttu-id="2df4e-103">Classe CIM_Processor (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="2df4e-103">CIM_Processor class (Hyper-V management)</span></span>

<span data-ttu-id="2df4e-104">Représente les fonctionnalités et la gestion d’un processeur.</span><span class="sxs-lookup"><span data-stu-id="2df4e-104">Represents the capabilities and management of a processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df4e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2df4e-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.1"), UMLPackagePath("CIM::Device::Processor"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  string Role;
  uint16 Family;
  string OtherFamilyDescription;
  uint16 UpgradeMethod;
  uint32 MaxClockSpeed;
  uint32 CurrentClockSpeed;
  uint16 DataWidth;
  uint16 AddressWidth;
  uint16 LoadPercentage;
  string Stepping;
  string UniqueID;
  uint16 CPUStatus;
  uint32 ExternalBusClockSpeed;
};
```

## <a name="members"></a><span data-ttu-id="2df4e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2df4e-106">Members</span></span>

<span data-ttu-id="2df4e-107">La classe de **\_ processeur CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2df4e-107">The **CIM\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="2df4e-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2df4e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2df4e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2df4e-109">Properties</span></span>

<span data-ttu-id="2df4e-110">La classe du **\_ processeur CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2df4e-110">The **CIM\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2df4e-111">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="2df4e-111">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2df4e-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-114">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »), **punitif** (« bit »)</span><span class="sxs-lookup"><span data-stu-id="2df4e-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-115">Largeur d’adresse du processeur, en bits.</span><span class="sxs-lookup"><span data-stu-id="2df4e-115">The processor address width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="2df4e-116">**CPUStatus**</span><span class="sxs-lookup"><span data-stu-id="2df4e-116">**CPUStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2df4e-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-119">État actuel du processeur.</span><span class="sxs-lookup"><span data-stu-id="2df4e-119">The current status of the processor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2df4e-120">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2df4e-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Enabled"></span><span id="cpu_enabled"></span><span id="CPU_ENABLED"></span>

<span data-ttu-id="2df4e-121">**Processeur activé** (1)</span><span class="sxs-lookup"><span data-stu-id="2df4e-121">**CPU Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Disabled_by_User"></span><span id="cpu_disabled_by_user"></span><span id="CPU_DISABLED_BY_USER"></span>

<span data-ttu-id="2df4e-122">**UC désactivée par l’utilisateur** (2)</span><span class="sxs-lookup"><span data-stu-id="2df4e-122">**CPU Disabled by User** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Disabled_By_BIOS__POST_Error_"></span><span id="cpu_disabled_by_bios__post_error_"></span><span id="CPU_DISABLED_BY_BIOS__POST_ERROR_"></span>

<span data-ttu-id="2df4e-123">**Processeur désactivé par le BIOS (erreur de publication)** (3)</span><span class="sxs-lookup"><span data-stu-id="2df4e-123">**CPU Disabled By BIOS (POST Error)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Is_Idle"></span><span id="cpu_is_idle"></span><span id="CPU_IS_IDLE"></span>

<span data-ttu-id="2df4e-124">Le **processeur est inactif** (4)</span><span class="sxs-lookup"><span data-stu-id="2df4e-124">**CPU Is Idle** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2df4e-125">**Autre** (7)</span><span class="sxs-lookup"><span data-stu-id="2df4e-125">**Other** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2df4e-126">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="2df4e-126">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-127">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2df4e-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-129">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("mégahertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 017,6 "), **punitif** (" Hertz \* 10 ^ 6 ")</span><span class="sxs-lookup"><span data-stu-id="2df4e-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.6"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-130">Vitesse actuelle, en MHz, du processeur.</span><span class="sxs-lookup"><span data-stu-id="2df4e-130">The current speed, in MHz, of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="2df4e-131">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="2df4e-131">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-132">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2df4e-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-134">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »), **punitif** (« bit »)</span><span class="sxs-lookup"><span data-stu-id="2df4e-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-135">Largeur des données du processeur, en bits.</span><span class="sxs-lookup"><span data-stu-id="2df4e-135">The processor data width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="2df4e-136">**ExternalBusClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="2df4e-136">**ExternalBusClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2df4e-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-139">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« mégahertz »), **punitif** (« Hertz \* 10 ^ 6 »)</span><span class="sxs-lookup"><span data-stu-id="2df4e-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-140">Vitesse, en MHz, de l’interface de bus externe (également appelée bus frontal).</span><span class="sxs-lookup"><span data-stu-id="2df4e-140">The speed, in MHz, of the external bus interface (also known as the front side bus).</span></span>

</dd> <dt>

<span data-ttu-id="2df4e-141">**Famille**</span><span class="sxs-lookup"><span data-stu-id="2df4e-141">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-142">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2df4e-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-144">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 017,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processeur CIM**.**OtherFamilyDescription**")</span><span class="sxs-lookup"><span data-stu-id="2df4e-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**OtherFamilyDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-145">Type de la famille de processeurs.</span><span class="sxs-lookup"><span data-stu-id="2df4e-145">The processor family type.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2df4e-146">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2df4e-146">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2df4e-147">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="2df4e-147">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="8086"></span>

<span data-ttu-id="2df4e-148">**8086** (3)</span><span class="sxs-lookup"><span data-stu-id="2df4e-148">**8086** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="80286"></span>

<span data-ttu-id="2df4e-149">**80286** (4)</span><span class="sxs-lookup"><span data-stu-id="2df4e-149">**80286** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="80386"></span>

<span data-ttu-id="2df4e-150">**80386** (5)</span><span class="sxs-lookup"><span data-stu-id="2df4e-150">**80386** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="80486"></span>

<span data-ttu-id="2df4e-151">**80486** (6)</span><span class="sxs-lookup"><span data-stu-id="2df4e-151">**80486** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8087"></span>

<span data-ttu-id="2df4e-152">**8087** (7)</span><span class="sxs-lookup"><span data-stu-id="2df4e-152">**8087** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="80287"></span>

<span data-ttu-id="2df4e-153">**80287** (8)</span><span class="sxs-lookup"><span data-stu-id="2df4e-153">**80287** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="80387"></span>

<span data-ttu-id="2df4e-154">**80387** (9)</span><span class="sxs-lookup"><span data-stu-id="2df4e-154">**80387** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="80487"></span>

<span data-ttu-id="2df4e-155">**80487** (10)</span><span class="sxs-lookup"><span data-stu-id="2df4e-155">**80487** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

<span data-ttu-id="2df4e-156">**Pentium (R)** (11)</span><span class="sxs-lookup"><span data-stu-id="2df4e-156">**Pentium(R) brand** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

<span data-ttu-id="2df4e-157">**Pentium (R) Pro** (12)</span><span class="sxs-lookup"><span data-stu-id="2df4e-157">**Pentium(R) Pro** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

<span data-ttu-id="2df4e-158">**Pentium (R) II** (13)</span><span class="sxs-lookup"><span data-stu-id="2df4e-158">**Pentium(R) II** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

<span data-ttu-id="2df4e-159">**Processeur Pentium (R) avec technologie MMX (TM)** (14)</span><span class="sxs-lookup"><span data-stu-id="2df4e-159">**Pentium(R) processor with MMX(TM) technology** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

<span data-ttu-id="2df4e-160">**Celeron (TM)** (15)</span><span class="sxs-lookup"><span data-stu-id="2df4e-160">**Celeron(TM)** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

<span data-ttu-id="2df4e-161">**Pentium (R) II Xeon (TM)** (16)</span><span class="sxs-lookup"><span data-stu-id="2df4e-161">**Pentium(R) II Xeon(TM)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

<span data-ttu-id="2df4e-162">**Pentium (R) III** (17)</span><span class="sxs-lookup"><span data-stu-id="2df4e-162">**Pentium(R) III** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

<span data-ttu-id="2df4e-163">**Famille M1** (18)</span><span class="sxs-lookup"><span data-stu-id="2df4e-163">**M1 Family** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

<span data-ttu-id="2df4e-164">**Famille m2** (19)</span><span class="sxs-lookup"><span data-stu-id="2df4e-164">**M2 Family** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Celeron_R__M_processor"></span><span id="intel_r__celeron_r__m_processor"></span><span id="INTEL_R__CELERON_R__M_PROCESSOR"></span>

<span data-ttu-id="2df4e-165">**Processeur Intel (r) Celeron (r) M** (20)</span><span class="sxs-lookup"><span data-stu-id="2df4e-165">**Intel(R) Celeron(R) M processor** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__4_HT_processor"></span><span id="intel_r__pentium_r__4_ht_processor"></span><span id="INTEL_R__PENTIUM_R__4_HT_PROCESSOR"></span>

<span data-ttu-id="2df4e-166">**Processeur Intel (r) Pentium (r) 4 HT** (21)</span><span class="sxs-lookup"><span data-stu-id="2df4e-166">**Intel(R) Pentium(R) 4 HT processor** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

<span data-ttu-id="2df4e-167">**Famille K5** (24)</span><span class="sxs-lookup"><span data-stu-id="2df4e-167">**K5 Family** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

<span data-ttu-id="2df4e-168">**Famille K6** (25)</span><span class="sxs-lookup"><span data-stu-id="2df4e-168">**K6 Family** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

<span data-ttu-id="2df4e-169">**K6-2** (26)</span><span class="sxs-lookup"><span data-stu-id="2df4e-169">**K6-2** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

<span data-ttu-id="2df4e-170">**K6-3** (27)</span><span class="sxs-lookup"><span data-stu-id="2df4e-170">**K6-3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-171">**Famille de processeurs AMD Athlon (TM)** (28)</span><span class="sxs-lookup"><span data-stu-id="2df4e-171">**AMD Athlon(TM) Processor Family** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

<span data-ttu-id="2df4e-172">**Processeur AMD (R) Duron (TM)** (29)</span><span class="sxs-lookup"><span data-stu-id="2df4e-172">**AMD(R) Duron(TM) Processor** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

<span data-ttu-id="2df4e-173">**Famille AMD29000** (30)</span><span class="sxs-lookup"><span data-stu-id="2df4e-173">**AMD29000 Family** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

<span data-ttu-id="2df4e-174">**K6-2 +** (31)</span><span class="sxs-lookup"><span data-stu-id="2df4e-174">**K6-2+** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

<span data-ttu-id="2df4e-175">**Famille Power PC** (32)</span><span class="sxs-lookup"><span data-stu-id="2df4e-175">**Power PC Family** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

<span data-ttu-id="2df4e-176">**Power PC 601** (33)</span><span class="sxs-lookup"><span data-stu-id="2df4e-176">**Power PC 601** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

<span data-ttu-id="2df4e-177">**Power PC 603** (34)</span><span class="sxs-lookup"><span data-stu-id="2df4e-177">**Power PC 603** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

<span data-ttu-id="2df4e-178">**Power PC 603 +** (35)</span><span class="sxs-lookup"><span data-stu-id="2df4e-178">**Power PC 603+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

<span data-ttu-id="2df4e-179">**Power PC 604** (36)</span><span class="sxs-lookup"><span data-stu-id="2df4e-179">**Power PC 604** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

<span data-ttu-id="2df4e-180">**Power PC 620** (37)</span><span class="sxs-lookup"><span data-stu-id="2df4e-180">**Power PC 620** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

<span data-ttu-id="2df4e-181">**Power PC X704** (38)</span><span class="sxs-lookup"><span data-stu-id="2df4e-181">**Power PC X704** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

<span data-ttu-id="2df4e-182">**Power PC 750** (39)</span><span class="sxs-lookup"><span data-stu-id="2df4e-182">**Power PC 750** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Duo_processor"></span><span id="intel_r__core_tm__duo_processor"></span><span id="INTEL_R__CORE_TM__DUO_PROCESSOR"></span>

<span data-ttu-id="2df4e-183">**Processeur Intel (R) Core (TM) Duo** (40)</span><span class="sxs-lookup"><span data-stu-id="2df4e-183">**Intel(R) Core(TM) Duo processor** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Duo_mobile_processor"></span><span id="intel_r__core_tm__duo_mobile_processor"></span><span id="INTEL_R__CORE_TM__DUO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="2df4e-184">**Processeur mobile Intel (R) Core (TM) Duo** (41)</span><span class="sxs-lookup"><span data-stu-id="2df4e-184">**Intel(R) Core(TM) Duo mobile processor** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Solo_mobile_processor"></span><span id="intel_r__core_tm__solo_mobile_processor"></span><span id="INTEL_R__CORE_TM__SOLO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="2df4e-185">**Processeur mobile Intel (R) Core (TM) solo** (42)</span><span class="sxs-lookup"><span data-stu-id="2df4e-185">**Intel(R) Core(TM) Solo mobile processor** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Atom_TM__processor"></span><span id="intel_r__atom_tm__processor"></span><span id="INTEL_R__ATOM_TM__PROCESSOR"></span>

<span data-ttu-id="2df4e-186">**Processeur Intel (R) Atom (TM)** (43)</span><span class="sxs-lookup"><span data-stu-id="2df4e-186">**Intel(R) Atom(TM) processor** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

<span data-ttu-id="2df4e-187">**Famille alpha** (48)</span><span class="sxs-lookup"><span data-stu-id="2df4e-187">**Alpha Family** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

<span data-ttu-id="2df4e-188">**Alpha 21064** (49)</span><span class="sxs-lookup"><span data-stu-id="2df4e-188">**Alpha 21064** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

<span data-ttu-id="2df4e-189">**Alpha 21066** (50)</span><span class="sxs-lookup"><span data-stu-id="2df4e-189">**Alpha 21066** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

<span data-ttu-id="2df4e-190">**Alpha 21164** (51)</span><span class="sxs-lookup"><span data-stu-id="2df4e-190">**Alpha 21164** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

<span data-ttu-id="2df4e-191">**Alpha 21164PC** (52)</span><span class="sxs-lookup"><span data-stu-id="2df4e-191">**Alpha 21164PC** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

<span data-ttu-id="2df4e-192">**Alpha 21164a** (53)</span><span class="sxs-lookup"><span data-stu-id="2df4e-192">**Alpha 21164a** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

<span data-ttu-id="2df4e-193">**Alpha 21264** (54)</span><span class="sxs-lookup"><span data-stu-id="2df4e-193">**Alpha 21264** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

<span data-ttu-id="2df4e-194">**Alpha 21364** (55)</span><span class="sxs-lookup"><span data-stu-id="2df4e-194">**Alpha 21364** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__II_Ultra_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_turion_tm__ii_ultra_dual-core_mobile_m_processor_family"></span><span id="AMD_TURION_TM__II_ULTRA_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-195">**Famille de processeurs AMD Turion (TM) II Ultra Dual-Core mobile M** (56)</span><span class="sxs-lookup"><span data-stu-id="2df4e-195">**AMD Turion(TM) II Ultra Dual-Core Mobile M Processor Family** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__II_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_turion_tm__ii_dual-core_mobile_m_processor_family"></span><span id="AMD_TURION_TM__II_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-196">**Famille de processeurs AMD Turion (TM) II Dual-Core mobile M** (57)</span><span class="sxs-lookup"><span data-stu-id="2df4e-196">**AMD Turion(TM) II Dual-Core Mobile M Processor Family** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__II_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_athlon_tm__ii_dual-core_mobile_m_processor_family"></span><span id="AMD_ATHLON_TM__II_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-197">**Famille de processeurs AMD Athlon (TM) II Dual-Core mobile M** (58)</span><span class="sxs-lookup"><span data-stu-id="2df4e-197">**AMD Athlon(TM) II Dual-Core Mobile M Processor Family** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__6100_Series_Processor"></span><span id="amd_opteron_tm__6100_series_processor"></span><span id="AMD_OPTERON_TM__6100_SERIES_PROCESSOR"></span>

<span data-ttu-id="2df4e-198">**Processeur AMD Opteron (TM) 6100 Series** (59)</span><span class="sxs-lookup"><span data-stu-id="2df4e-198">**AMD Opteron(TM) 6100 Series Processor** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__4100_Series_Processor"></span><span id="amd_opteron_tm__4100_series_processor"></span><span id="AMD_OPTERON_TM__4100_SERIES_PROCESSOR"></span>

<span data-ttu-id="2df4e-199">**Processeur AMD Opteron (TM) 4100 Series** (60)</span><span class="sxs-lookup"><span data-stu-id="2df4e-199">**AMD Opteron(TM) 4100 Series Processor** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

<span data-ttu-id="2df4e-200">**Famille mips** (64)</span><span class="sxs-lookup"><span data-stu-id="2df4e-200">**MIPS Family** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

<span data-ttu-id="2df4e-201">**R4000 mips** (65)</span><span class="sxs-lookup"><span data-stu-id="2df4e-201">**MIPS R4000** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

<span data-ttu-id="2df4e-202">**R4200 mips** (66)</span><span class="sxs-lookup"><span data-stu-id="2df4e-202">**MIPS R4200** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

<span data-ttu-id="2df4e-203">**R4400 mips** (67)</span><span class="sxs-lookup"><span data-stu-id="2df4e-203">**MIPS R4400** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

<span data-ttu-id="2df4e-204">**R4600 mips** (68)</span><span class="sxs-lookup"><span data-stu-id="2df4e-204">**MIPS R4600** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

<span data-ttu-id="2df4e-205">**R10000 mips** (69)</span><span class="sxs-lookup"><span data-stu-id="2df4e-205">**MIPS R10000** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

<span data-ttu-id="2df4e-206">**Famille sparc** (80)</span><span class="sxs-lookup"><span data-stu-id="2df4e-206">**SPARC Family** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

<span data-ttu-id="2df4e-207">**SuperSPARC** (81)</span><span class="sxs-lookup"><span data-stu-id="2df4e-207">**SuperSPARC** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

<span data-ttu-id="2df4e-208">**MICROSPARC II** (82)</span><span class="sxs-lookup"><span data-stu-id="2df4e-208">**microSPARC II** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

<span data-ttu-id="2df4e-209">**MicroSPARC IIep** (83)</span><span class="sxs-lookup"><span data-stu-id="2df4e-209">**microSPARC IIep** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

<span data-ttu-id="2df4e-210">**UltraSPARC** (84)</span><span class="sxs-lookup"><span data-stu-id="2df4e-210">**UltraSPARC** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

<span data-ttu-id="2df4e-211">**ULTRASPARC II** (85)</span><span class="sxs-lookup"><span data-stu-id="2df4e-211">**UltraSPARC II** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="2df4e-212">**UltraSPARC III** (86)</span><span class="sxs-lookup"><span data-stu-id="2df4e-212">**UltraSPARC IIi** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="2df4e-213">**ULTRASPARC III** (87)</span><span class="sxs-lookup"><span data-stu-id="2df4e-213">**UltraSPARC III** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

<span data-ttu-id="2df4e-214">**UltraSPARC IIIi** (88)</span><span class="sxs-lookup"><span data-stu-id="2df4e-214">**UltraSPARC IIIi** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="68040"></span>

<span data-ttu-id="2df4e-215">**68040** (96)</span><span class="sxs-lookup"><span data-stu-id="2df4e-215">**68040** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

<span data-ttu-id="2df4e-216">**famille 68xxx** (97)</span><span class="sxs-lookup"><span data-stu-id="2df4e-216">**68xxx Family** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="68000"></span>

<span data-ttu-id="2df4e-217">**68000** (98)</span><span class="sxs-lookup"><span data-stu-id="2df4e-217">**68000** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="68010"></span>

<span data-ttu-id="2df4e-218">**68010** (99)</span><span class="sxs-lookup"><span data-stu-id="2df4e-218">**68010** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="68020"></span>

<span data-ttu-id="2df4e-219">**68020** (100)</span><span class="sxs-lookup"><span data-stu-id="2df4e-219">**68020** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="68030"></span>

<span data-ttu-id="2df4e-220">**68030** (101)</span><span class="sxs-lookup"><span data-stu-id="2df4e-220">**68030** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

<span data-ttu-id="2df4e-221">**Famille Hobbit** (112)</span><span class="sxs-lookup"><span data-stu-id="2df4e-221">**Hobbit Family** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

<span data-ttu-id="2df4e-222">**Famille Crusoe (TM) TM5000** (120)</span><span class="sxs-lookup"><span data-stu-id="2df4e-222">**Crusoe(TM) TM5000 Family** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

<span data-ttu-id="2df4e-223">**Famille Crusoe (TM) TM3000** (121)</span><span class="sxs-lookup"><span data-stu-id="2df4e-223">**Crusoe(TM) TM3000 Family** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

<span data-ttu-id="2df4e-224">**Famille Efficeon (TM) TM8000** (122)</span><span class="sxs-lookup"><span data-stu-id="2df4e-224">**Efficeon(TM) TM8000 Family** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

<span data-ttu-id="2df4e-225">**Weitek** (128)</span><span class="sxs-lookup"><span data-stu-id="2df4e-225">**Weitek** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

<span data-ttu-id="2df4e-226">**Processeur Itanium (** 130)</span><span class="sxs-lookup"><span data-stu-id="2df4e-226">**Itanium(TM) Processor** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-227">**Famille de processeurs AMD Athlon (TM) 64** (131)</span><span class="sxs-lookup"><span data-stu-id="2df4e-227">**AMD Athlon(TM) 64 Processor Family** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__Processor_Family"></span><span id="amd_opteron_tm__processor_family"></span><span id="AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-228">**Famille de processeurs AMD Opteron (TM)** (132)</span><span class="sxs-lookup"><span data-stu-id="2df4e-228">**AMD Opteron(TM) Processor Family** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__Processor_Family"></span><span id="amd_sempron_tm__processor_family"></span><span id="AMD_SEMPRON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-229">**Famille de processeurs AMD Sempron (TM)** (133)</span><span class="sxs-lookup"><span data-stu-id="2df4e-229">**AMD Sempron(TM) Processor Family** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__64_Mobile_Technology"></span><span id="amd_turion_tm__64_mobile_technology"></span><span id="AMD_TURION_TM__64_MOBILE_TECHNOLOGY"></span>

<span data-ttu-id="2df4e-230">**Technologie mobile AMD Turion (TM) 64** (134)</span><span class="sxs-lookup"><span data-stu-id="2df4e-230">**AMD Turion(TM) 64 Mobile Technology** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_AMD_Opteron_TM__Processor_Family"></span><span id="dual-core_amd_opteron_tm__processor_family"></span><span id="DUAL-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-231">**Famille de processeurs double cœur AMD Opteron (TM)** (135)</span><span class="sxs-lookup"><span data-stu-id="2df4e-231">**Dual-Core AMD Opteron(TM) Processor Family** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__64_X2_Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__64_x2_dual-core_processor_family"></span><span id="AMD_ATHLON_TM__64_X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-232">**Famille de processeurs AMD Athlon (TM) 64 X2 Dual-Core** (136)</span><span class="sxs-lookup"><span data-stu-id="2df4e-232">**AMD Athlon(TM) 64 X2 Dual-Core Processor Family** (136)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__64_X2_Mobile_Technology"></span><span id="amd_turion_tm__64_x2_mobile_technology"></span><span id="AMD_TURION_TM__64_X2_MOBILE_TECHNOLOGY"></span>

<span data-ttu-id="2df4e-233">**AMD Turion (TM) 64 x2 Mobile Technology** (137)</span><span class="sxs-lookup"><span data-stu-id="2df4e-233">**AMD Turion(TM) 64 X2 Mobile Technology** (137)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_AMD_Opteron_TM__Processor_Family"></span><span id="quad-core_amd_opteron_tm__processor_family"></span><span id="QUAD-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-234">**Famille de processeurs AMD Opteron (TM) Quad Core** (138)</span><span class="sxs-lookup"><span data-stu-id="2df4e-234">**Quad-Core AMD Opteron(TM) Processor Family** (138)</span></span>


</dt> <dd></dd> <dt>

<span id="Third-Generation_AMD_Opteron_TM__Processor_Family"></span><span id="third-generation_amd_opteron_tm__processor_family"></span><span id="THIRD-GENERATION_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-235">**Famille de processeurs AMD Opteron (TM) de troisième génération** (139)</span><span class="sxs-lookup"><span data-stu-id="2df4e-235">**Third-Generation AMD Opteron(TM) Processor Family** (139)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__FX_Quad-Core_Processor_Family"></span><span id="amd_phenom_tm__fx_quad-core_processor_family"></span><span id="AMD_PHENOM_TM__FX_QUAD-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-236">**Famille de processeurs AMD Phenom (TM) FX Quad-Core** (140)</span><span class="sxs-lookup"><span data-stu-id="2df4e-236">**AMD Phenom(TM) FX Quad-Core Processor Family** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__X4_Quad-Core_Processor_Family"></span><span id="amd_phenom_tm__x4_quad-core_processor_family"></span><span id="AMD_PHENOM_TM__X4_QUAD-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-237">**Famille de processeurs AMD Phenom (TM) X4 Quad-Core** (141)</span><span class="sxs-lookup"><span data-stu-id="2df4e-237">**AMD Phenom(TM) X4 Quad-Core Processor Family** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__X2_Dual-Core_Processor_Family"></span><span id="amd_phenom_tm__x2_dual-core_processor_family"></span><span id="AMD_PHENOM_TM__X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-238">**Famille de processeurs AMD Phenom (TM) X2 Dual-Core** (142)</span><span class="sxs-lookup"><span data-stu-id="2df4e-238">**AMD Phenom(TM) X2 Dual-Core Processor Family** (142)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__X2_Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__x2_dual-core_processor_family"></span><span id="AMD_ATHLON_TM__X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-239">**Famille de processeurs AMD Athlon (TM) X2 Dual-Core** (143)</span><span class="sxs-lookup"><span data-stu-id="2df4e-239">**AMD Athlon(TM) X2 Dual-Core Processor Family** (143)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

<span data-ttu-id="2df4e-240">**Famille PA-RISC** (144)</span><span class="sxs-lookup"><span data-stu-id="2df4e-240">**PA-RISC Family** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

<span data-ttu-id="2df4e-241">**PA-RISC 8500** (145)</span><span class="sxs-lookup"><span data-stu-id="2df4e-241">**PA-RISC 8500** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

<span data-ttu-id="2df4e-242">**PA-RISC 8000** (146)</span><span class="sxs-lookup"><span data-stu-id="2df4e-242">**PA-RISC 8000** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

<span data-ttu-id="2df4e-243">**PA-RISC 7300LC** (147)</span><span class="sxs-lookup"><span data-stu-id="2df4e-243">**PA-RISC 7300LC** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

<span data-ttu-id="2df4e-244">**PA-RISC 7200** (148)</span><span class="sxs-lookup"><span data-stu-id="2df4e-244">**PA-RISC 7200** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

<span data-ttu-id="2df4e-245">**PA-RISC 7100LC** (149)</span><span class="sxs-lookup"><span data-stu-id="2df4e-245">**PA-RISC 7100LC** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

<span data-ttu-id="2df4e-246">**PA-RISC 7100** (150)</span><span class="sxs-lookup"><span data-stu-id="2df4e-246">**PA-RISC 7100** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

<span data-ttu-id="2df4e-247">**Famille V30** (160)</span><span class="sxs-lookup"><span data-stu-id="2df4e-247">**V30 Family** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_3200_Series"></span><span id="quad-core_intel_r__xeon_r__processor_3200_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_3200_SERIES"></span>

<span data-ttu-id="2df4e-248">**Processeur quadruple cœur Intel (r) Xeon (r)-série 3200** (161)</span><span class="sxs-lookup"><span data-stu-id="2df4e-248">**Quad-Core Intel(R) Xeon(R) processor 3200 Series** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_3000_Series"></span><span id="dual-core_intel_r__xeon_r__processor_3000_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_3000_SERIES"></span>

<span data-ttu-id="2df4e-249">**Processeur double cœur Intel (r) Xeon (r)-série 3000** (162)</span><span class="sxs-lookup"><span data-stu-id="2df4e-249">**Dual-Core Intel(R) Xeon(R) processor 3000 Series** (162)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5300_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5300_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5300_SERIES"></span>

<span data-ttu-id="2df4e-250">**Processeur quadruple cœur Intel (r) Xeon (r)-série 5300** (163)</span><span class="sxs-lookup"><span data-stu-id="2df4e-250">**Quad-Core Intel(R) Xeon(R) processor 5300 Series** (163)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5100_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5100_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5100_SERIES"></span>

<span data-ttu-id="2df4e-251">**Processeur double cœur Intel (r) Xeon (r)-série 5100** (164)</span><span class="sxs-lookup"><span data-stu-id="2df4e-251">**Dual-Core Intel(R) Xeon(R) processor 5100 Series** (164)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5000_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5000_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5000_SERIES"></span>

<span data-ttu-id="2df4e-252">**Processeur double cœur Intel (r) Xeon (r)-série 5000** (165)</span><span class="sxs-lookup"><span data-stu-id="2df4e-252">**Dual-Core Intel(R) Xeon(R) processor 5000 Series** (165)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_LV"></span><span id="dual-core_intel_r__xeon_r__processor_lv"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_LV"></span>

<span data-ttu-id="2df4e-253">**Processeur double cœur Intel (r) Xeon (r) LV** (166)</span><span class="sxs-lookup"><span data-stu-id="2df4e-253">**Dual-Core Intel(R) Xeon(R) processor LV** (166)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_ULV"></span><span id="dual-core_intel_r__xeon_r__processor_ulv"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_ULV"></span>

<span data-ttu-id="2df4e-254">**Processeur double cœur Intel (r) Xeon (r) TBT** (167)</span><span class="sxs-lookup"><span data-stu-id="2df4e-254">**Dual-Core Intel(R) Xeon(R) processor ULV** (167)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7100_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7100_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7100_SERIES"></span>

<span data-ttu-id="2df4e-255">**Processeur double cœur Intel (r) Xeon (r)-série 7100** (168)</span><span class="sxs-lookup"><span data-stu-id="2df4e-255">**Dual-Core Intel(R) Xeon(R) processor 7100 Series** (168)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5400_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5400_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5400_SERIES"></span>

<span data-ttu-id="2df4e-256">**Processeur quadruple cœur Intel (r) Xeon (r)-série 5400** (169)</span><span class="sxs-lookup"><span data-stu-id="2df4e-256">**Quad-Core Intel(R) Xeon(R) processor 5400 Series** (169)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor"></span><span id="quad-core_intel_r__xeon_r__processor"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR"></span>

<span data-ttu-id="2df4e-257">**Processeur quadruple cœur Intel (r) Xeon (r)** (170)</span><span class="sxs-lookup"><span data-stu-id="2df4e-257">**Quad-Core Intel(R) Xeon(R) processor** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5200_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5200_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5200_SERIES"></span>

<span data-ttu-id="2df4e-258">**Processeur double cœur Intel (r) Xeon (r)-série 5200** (171)</span><span class="sxs-lookup"><span data-stu-id="2df4e-258">**Dual-Core Intel(R) Xeon(R) processor 5200 Series** (171)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7200_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7200_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7200_SERIES"></span>

<span data-ttu-id="2df4e-259">**Processeur double cœur Intel (r) Xeon (r)-série 7200** (172)</span><span class="sxs-lookup"><span data-stu-id="2df4e-259">**Dual-Core Intel(R) Xeon(R) processor 7200 Series** (172)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7300_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7300_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7300_SERIES"></span>

<span data-ttu-id="2df4e-260">**Processeur quadruple cœur Intel (r) Xeon (r)-série 7300** (173)</span><span class="sxs-lookup"><span data-stu-id="2df4e-260">**Quad-Core Intel(R) Xeon(R) processor 7300 Series** (173)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7400_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7400_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7400_SERIES"></span>

<span data-ttu-id="2df4e-261">**Processeur quadruple cœur Intel (r) Xeon (r)-série 7400** (174)</span><span class="sxs-lookup"><span data-stu-id="2df4e-261">**Quad-Core Intel(R) Xeon(R) processor 7400 Series** (174)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_7400_Series"></span><span id="multi-core_intel_r__xeon_r__processor_7400_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_7400_SERIES"></span>

<span data-ttu-id="2df4e-262">**Processeur multicœur Intel (r) Xeon (r)-série 7400** (175)</span><span class="sxs-lookup"><span data-stu-id="2df4e-262">**Multi-Core Intel(R) Xeon(R) processor 7400 Series** (175)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

<span data-ttu-id="2df4e-263">**Pentium (R) III Xeon (TM)** (176)</span><span class="sxs-lookup"><span data-stu-id="2df4e-263">**Pentium(R) III Xeon(TM)** (176)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

<span data-ttu-id="2df4e-264">**Processeur Pentium (r) III avec technologie Intel (r) SpeedStep (TM)** (177)</span><span class="sxs-lookup"><span data-stu-id="2df4e-264">**Pentium(R) III Processor with Intel(R) SpeedStep(TM) Technology** (177)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

<span data-ttu-id="2df4e-265">**Pentium (R) 4** (178)</span><span class="sxs-lookup"><span data-stu-id="2df4e-265">**Pentium(R) 4** (178)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

<span data-ttu-id="2df4e-266">**Intel (R) Xeon (TM)** (179)</span><span class="sxs-lookup"><span data-stu-id="2df4e-266">**Intel(R) Xeon(TM)** (179)</span></span>


</dt> <dd></dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

<span data-ttu-id="2df4e-267">**Famille AS400** (180)</span><span class="sxs-lookup"><span data-stu-id="2df4e-267">**AS400 Family** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

<span data-ttu-id="2df4e-268">**Processeur Intel (R) Xeon (TM) MP** (181)</span><span class="sxs-lookup"><span data-stu-id="2df4e-268">**Intel(R) Xeon(TM) processor MP** (181)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__XP_Family"></span><span id="amd_athlon_tm__xp_family"></span><span id="AMD_ATHLON_TM__XP_FAMILY"></span>

<span data-ttu-id="2df4e-269">**Famille AMD Athlon (TM) XP** (182)</span><span class="sxs-lookup"><span data-stu-id="2df4e-269">**AMD Athlon(TM) XP Family** (182)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__MP_Family"></span><span id="amd_athlon_tm__mp_family"></span><span id="AMD_ATHLON_TM__MP_FAMILY"></span>

<span data-ttu-id="2df4e-270">**Famille de MP AMD Athlon (TM)** (183)</span><span class="sxs-lookup"><span data-stu-id="2df4e-270">**AMD Athlon(TM) MP Family** (183)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

<span data-ttu-id="2df4e-271">**Intel (r) Itanium (r) 2** (184)</span><span class="sxs-lookup"><span data-stu-id="2df4e-271">**Intel(R) Itanium(R) 2** (184)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__M_processor"></span><span id="intel_r__pentium_r__m_processor"></span><span id="INTEL_R__PENTIUM_R__M_PROCESSOR"></span>

<span data-ttu-id="2df4e-272">**Processeur Intel (r) Pentium (r) M** (185)</span><span class="sxs-lookup"><span data-stu-id="2df4e-272">**Intel(R) Pentium(R) M processor** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Celeron_R__D_processor"></span><span id="intel_r__celeron_r__d_processor"></span><span id="INTEL_R__CELERON_R__D_PROCESSOR"></span>

<span data-ttu-id="2df4e-273">**Processeur Intel (r) Celeron (r) D** (186)</span><span class="sxs-lookup"><span data-stu-id="2df4e-273">**Intel(R) Celeron(R) D processor** (186)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__D_processor"></span><span id="intel_r__pentium_r__d_processor"></span><span id="INTEL_R__PENTIUM_R__D_PROCESSOR"></span>

<span data-ttu-id="2df4e-274">**Processeur Intel (r) Pentium (r) D** (187)</span><span class="sxs-lookup"><span data-stu-id="2df4e-274">**Intel(R) Pentium(R) D processor** (187)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__Processor_Extreme_Edition"></span><span id="intel_r__pentium_r__processor_extreme_edition"></span><span id="INTEL_R__PENTIUM_R__PROCESSOR_EXTREME_EDITION"></span>

<span data-ttu-id="2df4e-275">**Processeur Intel (r) Pentium (r) Extreme Edition** (188)</span><span class="sxs-lookup"><span data-stu-id="2df4e-275">**Intel(R) Pentium(R) Processor Extreme Edition** (188)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Solo_Processor"></span><span id="intel_r__core_tm__solo_processor"></span><span id="INTEL_R__CORE_TM__SOLO_PROCESSOR"></span>

<span data-ttu-id="2df4e-276">**Processeur Intel (R) Core (TM) solo** (189)</span><span class="sxs-lookup"><span data-stu-id="2df4e-276">**Intel(R) Core(TM) Solo Processor** (189)</span></span>


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

<span data-ttu-id="2df4e-277">**K7** (190)</span><span class="sxs-lookup"><span data-stu-id="2df4e-277">**K7** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Duo_Processor"></span><span id="intel_r__core_tm_2_duo_processor"></span><span id="INTEL_R__CORE_TM_2_DUO_PROCESSOR"></span>

<span data-ttu-id="2df4e-278">**Processeur Intel (R) Core (TM) 2 Duo** (191)</span><span class="sxs-lookup"><span data-stu-id="2df4e-278">**Intel(R) Core(TM)2 Duo Processor** (191)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Solo_processor"></span><span id="intel_r__core_tm_2_solo_processor"></span><span id="INTEL_R__CORE_TM_2_SOLO_PROCESSOR"></span>

<span data-ttu-id="2df4e-279">**Processeur Intel (R) Core (TM) 2 solo** (192)</span><span class="sxs-lookup"><span data-stu-id="2df4e-279">**Intel(R) Core(TM)2 Solo processor** (192)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Extreme_processor"></span><span id="intel_r__core_tm_2_extreme_processor"></span><span id="INTEL_R__CORE_TM_2_EXTREME_PROCESSOR"></span>

<span data-ttu-id="2df4e-280">**Processeur Intel (R) Core (TM) 2 Extreme** (193)</span><span class="sxs-lookup"><span data-stu-id="2df4e-280">**Intel(R) Core(TM)2 Extreme processor** (193)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Quad_processor"></span><span id="intel_r__core_tm_2_quad_processor"></span><span id="INTEL_R__CORE_TM_2_QUAD_PROCESSOR"></span>

<span data-ttu-id="2df4e-281">**Processeur Intel (R) Core (TM) 2 Quad** (194)</span><span class="sxs-lookup"><span data-stu-id="2df4e-281">**Intel(R) Core(TM)2 Quad processor** (194)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Extreme_mobile_processor"></span><span id="intel_r__core_tm_2_extreme_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_EXTREME_MOBILE_PROCESSOR"></span>

<span data-ttu-id="2df4e-282">**Processeur Intel (R) Core (TM) 2 Extreme mobile** (195)</span><span class="sxs-lookup"><span data-stu-id="2df4e-282">**Intel(R) Core(TM)2 Extreme mobile processor** (195)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Duo_mobile_processor"></span><span id="intel_r__core_tm_2_duo_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_DUO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="2df4e-283">**Processeur mobile Intel (R) Core (TM) 2 Duo** (196)</span><span class="sxs-lookup"><span data-stu-id="2df4e-283">**Intel(R) Core(TM)2 Duo mobile processor** (196)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Solo_mobile_processor"></span><span id="intel_r__core_tm_2_solo_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_SOLO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="2df4e-284">**Processeur mobile Intel (R) Core (TM) 2 solo** (197)</span><span class="sxs-lookup"><span data-stu-id="2df4e-284">**Intel(R) Core(TM)2 Solo mobile processor** (197)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i7_processor"></span><span id="intel_r__core_tm__i7_processor"></span><span id="INTEL_R__CORE_TM__I7_PROCESSOR"></span>

<span data-ttu-id="2df4e-285">**Processeur Intel (R) Core (TM) i7** (198)</span><span class="sxs-lookup"><span data-stu-id="2df4e-285">**Intel(R) Core(TM) i7 processor** (198)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Celeron_R__Processor"></span><span id="dual-core_intel_r__celeron_r__processor"></span><span id="DUAL-CORE_INTEL_R__CELERON_R__PROCESSOR"></span>

<span data-ttu-id="2df4e-286">**Processeur double cœur Intel (r) Celeron (r)** (199)</span><span class="sxs-lookup"><span data-stu-id="2df4e-286">**Dual-Core Intel(R) Celeron(R) Processor** (199)</span></span>


</dt> <dd></dd> <dt>

<span id="S_390_and_zSeries_Family"></span><span id="s_390_and_zseries_family"></span><span id="S_390_AND_ZSERIES_FAMILY"></span>

<span data-ttu-id="2df4e-287">**Famille S/390 et zSeries** (200)</span><span class="sxs-lookup"><span data-stu-id="2df4e-287">**S/390 and zSeries Family** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="ESA_390_G4"></span><span id="esa_390_g4"></span>

<span data-ttu-id="2df4e-288">**Sec/390 G4** (201)</span><span class="sxs-lookup"><span data-stu-id="2df4e-288">**ESA/390 G4** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="ESA_390_G5"></span><span id="esa_390_g5"></span>

<span data-ttu-id="2df4e-289">**Sec/390 G5** (202)</span><span class="sxs-lookup"><span data-stu-id="2df4e-289">**ESA/390 G5** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="ESA_390_G6"></span><span id="esa_390_g6"></span>

<span data-ttu-id="2df4e-290">**Sec/390 G6** (203)</span><span class="sxs-lookup"><span data-stu-id="2df4e-290">**ESA/390 G6** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="z_Architectur_base"></span><span id="z_architectur_base"></span><span id="Z_ARCHITECTUR_BASE"></span>

<span data-ttu-id="2df4e-291">**base z/architectur** (204)</span><span class="sxs-lookup"><span data-stu-id="2df4e-291">**z/Architectur base** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i5_processor"></span><span id="intel_r__core_tm__i5_processor"></span><span id="INTEL_R__CORE_TM__I5_PROCESSOR"></span>

<span data-ttu-id="2df4e-292">**Processeur Intel (R) Core (TM) i5** (205)</span><span class="sxs-lookup"><span data-stu-id="2df4e-292">**Intel(R) Core(TM) i5 processor** (205)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i3_processor"></span><span id="intel_r__core_tm__i3_processor"></span><span id="INTEL_R__CORE_TM__I3_PROCESSOR"></span>

<span data-ttu-id="2df4e-293">**Processeur Intel (R) Core (TM) i3** (206)</span><span class="sxs-lookup"><span data-stu-id="2df4e-293">**Intel(R) Core(TM) i3 processor** (206)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM_-M_Processor_Family"></span><span id="via_c7_tm_-m_processor_family"></span><span id="VIA_C7_TM_-M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-294">**Famille de processeurs Via C7 (TM)-M** (210)</span><span class="sxs-lookup"><span data-stu-id="2df4e-294">**VIA C7(TM)-M Processor Family** (210)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM_-D_Processor_Family"></span><span id="via_c7_tm_-d_processor_family"></span><span id="VIA_C7_TM_-D_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-295">**Famille de processeurs Via C7 (TM)-D** (211)</span><span class="sxs-lookup"><span data-stu-id="2df4e-295">**VIA C7(TM)-D Processor Family** (211)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM__Processor_Family"></span><span id="via_c7_tm__processor_family"></span><span id="VIA_C7_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-296">**Famille de processeurs Via C7 (TM)** (212)</span><span class="sxs-lookup"><span data-stu-id="2df4e-296">**VIA C7(TM) Processor Family** (212)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_Eden_TM__Processor_Family"></span><span id="via_eden_tm__processor_family"></span><span id="VIA_EDEN_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-297">**Famille de processeurs via Eden (TM)** (213)</span><span class="sxs-lookup"><span data-stu-id="2df4e-297">**VIA Eden(TM) Processor Family** (213)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor"></span><span id="multi-core_intel_r__xeon_r__processor"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR"></span>

<span data-ttu-id="2df4e-298">**Processeur multicœur Intel (r) Xeon (r)** (214)</span><span class="sxs-lookup"><span data-stu-id="2df4e-298">**Multi-Core Intel(R) Xeon(R) processor** (214)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_3xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_3xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_3XXX_SERIES"></span>

<span data-ttu-id="2df4e-299">**Processeur double cœur Intel (r) Xeon (r)-série 3xxx** (215)</span><span class="sxs-lookup"><span data-stu-id="2df4e-299">**Dual-Core Intel(R) Xeon(R) processor 3xxx Series** (215)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_3xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_3xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_3XXX_SERIES"></span>

<span data-ttu-id="2df4e-300">**Processeur quadruple cœur Intel (r) Xeon (r)-série 3xxx** (216)</span><span class="sxs-lookup"><span data-stu-id="2df4e-300">**Quad-Core Intel(R) Xeon(R) processor 3xxx Series** (216)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_Nano_TM__Processor_Family"></span><span id="via_nano_tm__processor_family"></span><span id="VIA_NANO_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-301">**Famille de processeurs Nano (TM)** (217)</span><span class="sxs-lookup"><span data-stu-id="2df4e-301">**VIA Nano(TM) Processor Family** (217)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5XXX_SERIES"></span>

<span data-ttu-id="2df4e-302">**Processeur double cœur Intel (r) Xeon (r)-série 5xxx** (218)</span><span class="sxs-lookup"><span data-stu-id="2df4e-302">**Dual-Core Intel(R) Xeon(R) processor 5xxx Series** (218)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5XXX_SERIES"></span>

<span data-ttu-id="2df4e-303">**Processeur quadruple cœur Intel (r) Xeon (r)-série 5xxx** (219)</span><span class="sxs-lookup"><span data-stu-id="2df4e-303">**Quad-Core Intel(R) Xeon(R) processor 5xxx Series** (219)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

<span data-ttu-id="2df4e-304">**Processeur double cœur Intel (r) Xeon (r)-série 7xxx** (221)</span><span class="sxs-lookup"><span data-stu-id="2df4e-304">**Dual-Core Intel(R) Xeon(R) processor 7xxx Series** (221)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

<span data-ttu-id="2df4e-305">**Processeur quadruple cœur Intel (r) Xeon (r)-série 7xxx** (222)</span><span class="sxs-lookup"><span data-stu-id="2df4e-305">**Quad-Core Intel(R) Xeon(R) processor 7xxx Series** (222)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="multi-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

<span data-ttu-id="2df4e-306">**Processeur multicœur Intel (r) Xeon (r)-série 7xxx** (223)</span><span class="sxs-lookup"><span data-stu-id="2df4e-306">**Multi-Core Intel(R) Xeon(R) processor 7xxx Series** (223)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_3400_Series"></span><span id="multi-core_intel_r__xeon_r__processor_3400_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_3400_SERIES"></span>

<span data-ttu-id="2df4e-307">**Processeur multicœur Intel (r) Xeon (r)-série 3400** (224)</span><span class="sxs-lookup"><span data-stu-id="2df4e-307">**Multi-Core Intel(R) Xeon(R) processor 3400 Series** (224)</span></span>


</dt> <dd></dd> <dt>

<span id="Embedded_AMD_Opteron_TM__Quad-Core_Processor_Family"></span><span id="embedded_amd_opteron_tm__quad-core_processor_family"></span><span id="EMBEDDED_AMD_OPTERON_TM__QUAD-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-308">**Famille de processeurs AMD Opteron (TM) Quad-Core incorporée** (230)</span><span class="sxs-lookup"><span data-stu-id="2df4e-308">**Embedded AMD Opteron(TM) Quad-Core Processor Family** (230)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__Triple-Core_Processor_Family"></span><span id="amd_phenom_tm__triple-core_processor_family"></span><span id="AMD_PHENOM_TM__TRIPLE-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-309">**Famille de processeurs AMD Phenom (TM) Triple-Core** (231)</span><span class="sxs-lookup"><span data-stu-id="2df4e-309">**AMD Phenom(TM) Triple-Core Processor Family** (231)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__Ultra_Dual-Core_Mobile_Processor_Family"></span><span id="amd_turion_tm__ultra_dual-core_mobile_processor_family"></span><span id="AMD_TURION_TM__ULTRA_DUAL-CORE_MOBILE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-310">**Famille de processeurs mobiles AMD Turion (TM) Ultra Dual-Core** (232)</span><span class="sxs-lookup"><span data-stu-id="2df4e-310">**AMD Turion(TM) Ultra Dual-Core Mobile Processor Family** (232)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__Dual-Core_Mobile_Processor_Family"></span><span id="amd_turion_tm__dual-core_mobile_processor_family"></span><span id="AMD_TURION_TM__DUAL-CORE_MOBILE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-311">**Famille de processeurs mobiles AMD Turion (TM) Dual-Core** (233)</span><span class="sxs-lookup"><span data-stu-id="2df4e-311">**AMD Turion(TM) Dual-Core Mobile Processor Family** (233)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__dual-core_processor_family"></span><span id="AMD_ATHLON_TM__DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-312">**Famille de processeurs AMD Athlon (TM) Dual-Core** (234)</span><span class="sxs-lookup"><span data-stu-id="2df4e-312">**AMD Athlon(TM) Dual-Core Processor Family** (234)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__SI_Processor_Family"></span><span id="amd_sempron_tm__si_processor_family"></span><span id="AMD_SEMPRON_TM__SI_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-313">**Famille de processeurs AMD Sempron (TM) si** (235)</span><span class="sxs-lookup"><span data-stu-id="2df4e-313">**AMD Sempron(TM) SI Processor Family** (235)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__II_Processor_Family"></span><span id="amd_phenom_tm__ii_processor_family"></span><span id="AMD_PHENOM_TM__II_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-314">**Famille de processeurs AMD Phenom (TM) II** (236)</span><span class="sxs-lookup"><span data-stu-id="2df4e-314">**AMD Phenom(TM) II Processor Family** (236)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__II_Processor_Family"></span><span id="amd_athlon_tm__ii_processor_family"></span><span id="AMD_ATHLON_TM__II_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-315">**Famille de processeurs AMD Athlon (TM) II** (237)</span><span class="sxs-lookup"><span data-stu-id="2df4e-315">**AMD Athlon(TM) II Processor Family** (237)</span></span>


</dt> <dd></dd> <dt>

<span id="Six-Core_AMD_Opteron_TM__Processor_Family"></span><span id="six-core_amd_opteron_tm__processor_family"></span><span id="SIX-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-316">**Famille de processeurs AMD Opteron (TM) à six cœurs** (238)</span><span class="sxs-lookup"><span data-stu-id="2df4e-316">**Six-Core AMD Opteron(TM) Processor Family** (238)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__M_Processor_Family"></span><span id="amd_sempron_tm__m_processor_family"></span><span id="AMD_SEMPRON_TM__M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="2df4e-317">**Famille de processeurs AMD Sempron (TM) M** (239)</span><span class="sxs-lookup"><span data-stu-id="2df4e-317">**AMD Sempron(TM) M Processor Family** (239)</span></span>


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

<span data-ttu-id="2df4e-318">**i860** (250)</span><span class="sxs-lookup"><span data-stu-id="2df4e-318">**i860** (250)</span></span>


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

<span data-ttu-id="2df4e-319">**i960** (251)</span><span class="sxs-lookup"><span data-stu-id="2df4e-319">**i960** (251)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__SMBIOS_Extension_"></span><span id="reserved__smbios_extension_"></span><span id="RESERVED__SMBIOS_EXTENSION_"></span>

<span data-ttu-id="2df4e-320">**Réservé (extension SMBIOS)** (254)</span><span class="sxs-lookup"><span data-stu-id="2df4e-320">**Reserved (SMBIOS Extension)** (254)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__Un-initialized_Flash_Content_-_Lo_"></span><span id="reserved__un-initialized_flash_content_-_lo_"></span><span id="RESERVED__UN-INITIALIZED_FLASH_CONTENT_-_LO_"></span>

<span data-ttu-id="2df4e-321">**Réservé (contenu Flash non initialisé-Lo)** (255)</span><span class="sxs-lookup"><span data-stu-id="2df4e-321">**Reserved (Un-initialized Flash Content - Lo)** (255)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

<span data-ttu-id="2df4e-322">**SH-3** (260)</span><span class="sxs-lookup"><span data-stu-id="2df4e-322">**SH-3** (260)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

<span data-ttu-id="2df4e-323">**SH-4** (261)</span><span class="sxs-lookup"><span data-stu-id="2df4e-323">**SH-4** (261)</span></span>


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

<span data-ttu-id="2df4e-324">**ARM** (280)</span><span class="sxs-lookup"><span data-stu-id="2df4e-324">**ARM** (280)</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

<span data-ttu-id="2df4e-325">**StrongARM** (281)</span><span class="sxs-lookup"><span data-stu-id="2df4e-325">**StrongARM** (281)</span></span>


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

<span data-ttu-id="2df4e-326">**6 x86** (300)</span><span class="sxs-lookup"><span data-stu-id="2df4e-326">**6x86** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

<span data-ttu-id="2df4e-327">**MediaGX** (301)</span><span class="sxs-lookup"><span data-stu-id="2df4e-327">**MediaGX** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

<span data-ttu-id="2df4e-328">**MII** (302)</span><span class="sxs-lookup"><span data-stu-id="2df4e-328">**MII** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

<span data-ttu-id="2df4e-329">**WinChip** (320)</span><span class="sxs-lookup"><span data-stu-id="2df4e-329">**WinChip** (320)</span></span>


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

<span data-ttu-id="2df4e-330">**DSP** (350)</span><span class="sxs-lookup"><span data-stu-id="2df4e-330">**DSP** (350)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

<span data-ttu-id="2df4e-331">**Processeur vidéo** (500)</span><span class="sxs-lookup"><span data-stu-id="2df4e-331">**Video Processor** (500)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__For_Future_Special_Purpose_Assignment_"></span><span id="reserved__for_future_special_purpose_assignment_"></span><span id="RESERVED__FOR_FUTURE_SPECIAL_PURPOSE_ASSIGNMENT_"></span>

<span data-ttu-id="2df4e-332">**Réservé (à des fins d’affectation spéciale ultérieure)** (65534)</span><span class="sxs-lookup"><span data-stu-id="2df4e-332">**Reserved (For Future Special Purpose Assignment)** (65534)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__Un-initialized_Flash_Content_-_Hi_"></span><span id="reserved__un-initialized_flash_content_-_hi_"></span><span id="RESERVED__UN-INITIALIZED_FLASH_CONTENT_-_HI_"></span>

<span data-ttu-id="2df4e-333">**Réservé (contenu Flash non initialisé-HI)** (65535)</span><span class="sxs-lookup"><span data-stu-id="2df4e-333">**Reserved (Un-initialized Flash Content - Hi)** (65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2df4e-334">**LoadPercentage**</span><span class="sxs-lookup"><span data-stu-id="2df4e-334">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-335">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2df4e-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-337">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« percent »), [**jauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) («MIB. IETF \| Host-Resources-MIB. hrProcessorLoad "), **punitif** (" percent ")</span><span class="sxs-lookup"><span data-stu-id="2df4e-337">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrProcessorLoad"), **PUnit** ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-338">Le chargement du processeur, en moyenne au cours de la dernière minute, en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="2df4e-338">The loading of the processor, averaged over the last minute, as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="2df4e-339">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="2df4e-339">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-340">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2df4e-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-342">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("mégahertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 017,5 "), **punitif** (" Hertz \* 10 ^ 6 ")</span><span class="sxs-lookup"><span data-stu-id="2df4e-342">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.5"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-343">Vitesse maximale, en MHz, du processeur.</span><span class="sxs-lookup"><span data-stu-id="2df4e-343">The maximum speed, in MHz, of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="2df4e-344">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="2df4e-344">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-345">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2df4e-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-347">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processeur CIM**.**Family**»)</span><span class="sxs-lookup"><span data-stu-id="2df4e-347">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-348">Type de la famille de processeurs lorsque la propriété **Family** est définie sur **other** (« 1 »).</span><span class="sxs-lookup"><span data-stu-id="2df4e-348">The processor family type when the **Family** property is set to **Other** ("1").</span></span> <span data-ttu-id="2df4e-349">Cette chaîne doit être définie sur NULL lorsque la propriété Family a une valeur autre que **other**.</span><span class="sxs-lookup"><span data-stu-id="2df4e-349">This string should be set to NULL when the Family property is any value other than **Other**.</span></span>

</dd> <dt>

<span data-ttu-id="2df4e-350">**Rôle**</span><span class="sxs-lookup"><span data-stu-id="2df4e-350">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-351">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2df4e-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-353">Rôle du processeur, par exemple « processeur central » ou « processeur mathématique ».</span><span class="sxs-lookup"><span data-stu-id="2df4e-353">The role of the processor, for example, "Central Processor" or "Math Processor".</span></span>

</dd> <dt>

<span data-ttu-id="2df4e-354">**Exécution pas à pas**</span><span class="sxs-lookup"><span data-stu-id="2df4e-354">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2df4e-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-357">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ processeur CIM**».**Family**»)</span><span class="sxs-lookup"><span data-stu-id="2df4e-357">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-358">Niveau de révision du processeur au sein de la famille de processeurs.</span><span class="sxs-lookup"><span data-stu-id="2df4e-358">The revision level of the processor within the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="2df4e-359">**Quei**</span><span class="sxs-lookup"><span data-stu-id="2df4e-359">**UniqueID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-360">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2df4e-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-362">Identificateur global unique du processeur, au sein de la portée de la famille de processeurs.</span><span class="sxs-lookup"><span data-stu-id="2df4e-362">A globally unique identifier for the processor, within the scope of the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="2df4e-363">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="2df4e-363">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df4e-364">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2df4e-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2df4e-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2df4e-366">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 017,7 ")</span><span class="sxs-lookup"><span data-stu-id="2df4e-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.7")</span></span>
</dt> </dl>

<span data-ttu-id="2df4e-367">Informations sur le socket d’UC qui incluent des données sur la façon dont le processeur peut être mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="2df4e-367">The CPU socket information that includes data on how the processor can be upgraded.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2df4e-368">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2df4e-368">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2df4e-369">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="2df4e-369">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

<span data-ttu-id="2df4e-370">**Carte fille** (3)</span><span class="sxs-lookup"><span data-stu-id="2df4e-370">**Daughter Board** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

<span data-ttu-id="2df4e-371">**Connecteur ZIF** (4)</span><span class="sxs-lookup"><span data-stu-id="2df4e-371">**ZIF Socket** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

<span data-ttu-id="2df4e-372">**Remplacement/** superposition (5)</span><span class="sxs-lookup"><span data-stu-id="2df4e-372">**Replacement/Piggy Back** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="2df4e-373">**Aucun** (6)</span><span class="sxs-lookup"><span data-stu-id="2df4e-373">**None** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

<span data-ttu-id="2df4e-374">**Socket LIF** (7)</span><span class="sxs-lookup"><span data-stu-id="2df4e-374">**LIF Socket** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

<span data-ttu-id="2df4e-375">**Emplacement 1** (8)</span><span class="sxs-lookup"><span data-stu-id="2df4e-375">**Slot 1** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

<span data-ttu-id="2df4e-376">**Emplacement 2** (9)</span><span class="sxs-lookup"><span data-stu-id="2df4e-376">**Slot 2** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

<span data-ttu-id="2df4e-377">**Socket de broche 370** (10)</span><span class="sxs-lookup"><span data-stu-id="2df4e-377">**370 Pin Socket** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

<span data-ttu-id="2df4e-378">**Emplacement A** (11)</span><span class="sxs-lookup"><span data-stu-id="2df4e-378">**Slot A** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

<span data-ttu-id="2df4e-379">**Emplacement M** (12)</span><span class="sxs-lookup"><span data-stu-id="2df4e-379">**Slot M** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

<span data-ttu-id="2df4e-380">**Socket 423** (13)</span><span class="sxs-lookup"><span data-stu-id="2df4e-380">**Socket 423** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

<span data-ttu-id="2df4e-381">**Socket A (socket 462)** (14)</span><span class="sxs-lookup"><span data-stu-id="2df4e-381">**Socket A (Socket 462)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

<span data-ttu-id="2df4e-382">**Socket 478** (15)</span><span class="sxs-lookup"><span data-stu-id="2df4e-382">**Socket 478** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

<span data-ttu-id="2df4e-383">**Socket 754** (16)</span><span class="sxs-lookup"><span data-stu-id="2df4e-383">**Socket 754** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

<span data-ttu-id="2df4e-384">**Socket 940** (17)</span><span class="sxs-lookup"><span data-stu-id="2df4e-384">**Socket 940** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

<span data-ttu-id="2df4e-385">**Socket 939** (18)</span><span class="sxs-lookup"><span data-stu-id="2df4e-385">**Socket 939** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_mPGA604"></span><span id="socket_mpga604"></span><span id="SOCKET_MPGA604"></span>

<span data-ttu-id="2df4e-386">**Socket mPGA604** (19)</span><span class="sxs-lookup"><span data-stu-id="2df4e-386">**Socket mPGA604** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA771"></span><span id="socket_lga771"></span><span id="SOCKET_LGA771"></span>

<span data-ttu-id="2df4e-387">**Socket LGA771** (20)</span><span class="sxs-lookup"><span data-stu-id="2df4e-387">**Socket LGA771** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA775"></span><span id="socket_lga775"></span><span id="SOCKET_LGA775"></span>

<span data-ttu-id="2df4e-388">**Conditionnement LGA775** (21)</span><span class="sxs-lookup"><span data-stu-id="2df4e-388">**Socket LGA775** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_S1"></span><span id="socket_s1"></span><span id="SOCKET_S1"></span>

<span data-ttu-id="2df4e-389">**Socket S1** (22)</span><span class="sxs-lookup"><span data-stu-id="2df4e-389">**Socket S1** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_AM2"></span><span id="socket_am2"></span><span id="SOCKET_AM2"></span>

<span data-ttu-id="2df4e-390">**Socket AM2** (23)</span><span class="sxs-lookup"><span data-stu-id="2df4e-390">**Socket AM2** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_F__1207_"></span><span id="socket_f__1207_"></span><span id="SOCKET_F__1207_"></span>

<span data-ttu-id="2df4e-391">**Socket F (1207)** (24)</span><span class="sxs-lookup"><span data-stu-id="2df4e-391">**Socket F (1207)** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA1366"></span><span id="socket_lga1366"></span><span id="SOCKET_LGA1366"></span>

<span data-ttu-id="2df4e-392">**Socket LGA1366** (25)</span><span class="sxs-lookup"><span data-stu-id="2df4e-392">**Socket LGA1366** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_G34"></span><span id="socket_g34"></span><span id="SOCKET_G34"></span>

<span data-ttu-id="2df4e-393">**G34 Socket** (26)</span><span class="sxs-lookup"><span data-stu-id="2df4e-393">**Socket G34** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_AM3"></span><span id="socket_am3"></span><span id="SOCKET_AM3"></span>

<span data-ttu-id="2df4e-394">**Socket AM3** (27)</span><span class="sxs-lookup"><span data-stu-id="2df4e-394">**Socket AM3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_C32"></span><span id="socket_c32"></span><span id="SOCKET_C32"></span>

<span data-ttu-id="2df4e-395">**Socket C32** (28)</span><span class="sxs-lookup"><span data-stu-id="2df4e-395">**Socket C32** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA1156"></span><span id="socket_lga1156"></span><span id="SOCKET_LGA1156"></span>

<span data-ttu-id="2df4e-396">**Socket LGA1156** (29)</span><span class="sxs-lookup"><span data-stu-id="2df4e-396">**Socket LGA1156** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA1567"></span><span id="socket_lga1567"></span><span id="SOCKET_LGA1567"></span>

<span data-ttu-id="2df4e-397">**Socket LGA1567** (30)</span><span class="sxs-lookup"><span data-stu-id="2df4e-397">**Socket LGA1567** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_PGA988A"></span><span id="socket_pga988a"></span><span id="SOCKET_PGA988A"></span>

<span data-ttu-id="2df4e-398">**Socket PGA988A** (31)</span><span class="sxs-lookup"><span data-stu-id="2df4e-398">**Socket PGA988A** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_BGA1288"></span><span id="socket_bga1288"></span><span id="SOCKET_BGA1288"></span>

<span data-ttu-id="2df4e-399">**Socket BGA1288** (32)</span><span class="sxs-lookup"><span data-stu-id="2df4e-399">**Socket BGA1288** (32)</span></span>


<span data-ttu-id="2df4e-400"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2df4e-400"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2df4e-401">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2df4e-401">Requirements</span></span>



| <span data-ttu-id="2df4e-402">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2df4e-402">Requirement</span></span> | <span data-ttu-id="2df4e-403">Valeur</span><span class="sxs-lookup"><span data-stu-id="2df4e-403">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2df4e-404">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2df4e-404">Minimum supported client</span></span><br/> | <span data-ttu-id="2df4e-405">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2df4e-405">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2df4e-406">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2df4e-406">Minimum supported server</span></span><br/> | <span data-ttu-id="2df4e-407">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2df4e-407">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2df4e-408">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2df4e-408">Namespace</span></span><br/>                | <span data-ttu-id="2df4e-409">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2df4e-409">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2df4e-410">MOF</span><span class="sxs-lookup"><span data-stu-id="2df4e-410">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2df4e-411"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2df4e-411"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2df4e-412">DLL</span><span class="sxs-lookup"><span data-stu-id="2df4e-412">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2df4e-413"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2df4e-413"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2df4e-414">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2df4e-414">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df4e-415">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2df4e-415">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

