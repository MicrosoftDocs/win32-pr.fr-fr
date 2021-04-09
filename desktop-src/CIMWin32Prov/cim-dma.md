---
description: La \_ classe DMA CIM représente l’accès direct à la mémoire (DMA) de l’architecture d’ordinateur.
ms.assetid: 101fa9f3-a403-487d-8482-b1e8e9f957d6
ms.tgt_platform: multiple
title: Classe CIM_DMA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DMA
- CIM_DMA.AddressSize
- CIM_DMA.Availability
- CIM_DMA.BurstMode
- CIM_DMA.ByteMode
- CIM_DMA.Caption
- CIM_DMA.ChannelTiming
- CIM_DMA.CreationClassName
- CIM_DMA.CSCreationClassName
- CIM_DMA.CSName
- CIM_DMA.Description
- CIM_DMA.DMAChannel
- CIM_DMA.InstallDate
- CIM_DMA.MaxTransferSize
- CIM_DMA.Name
- CIM_DMA.Status
- CIM_DMA.TransferWidths
- CIM_DMA.TypeCTiming
- CIM_DMA.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71fe9c0ad29afa7be20df6fbf05c5d1183d23d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950662"
---
# <a name="cim_dma-class"></a><span data-ttu-id="26f0f-103">\_Classe DMA CIM</span><span class="sxs-lookup"><span data-stu-id="26f0f-103">CIM\_DMA class</span></span>

<span data-ttu-id="26f0f-104">La **classe \_ DMA CIM** représente l’accès direct à la mémoire (DMA) de l’architecture d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="26f0f-104">The **CIM\_DMA** class represents computer architecture direct memory access (DMA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26f0f-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="26f0f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="26f0f-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="26f0f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="26f0f-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="26f0f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="26f0f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="26f0f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f0f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26f0f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C523-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DMA : CIM_SystemResource
{
  uint16   AddressSize;
  uint16   Availability;
  boolean  BurstMode;
  uint16   ByteMode;
  string   Caption;
  uint16   ChannelTiming;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint32   DMAChannel;
  datetime InstallDate;
  uint32   MaxTransferSize;
  string   Name;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="26f0f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="26f0f-110">Members</span></span>

<span data-ttu-id="26f0f-111">La **classe \_ DMA CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="26f0f-111">The **CIM\_DMA** class has these types of members:</span></span>

-   [<span data-ttu-id="26f0f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26f0f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26f0f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26f0f-113">Properties</span></span>

<span data-ttu-id="26f0f-114">La **classe \_ DMA CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="26f0f-114">The **CIM\_DMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26f0f-115">**AddressSize**</span><span class="sxs-lookup"><span data-stu-id="26f0f-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26f0f-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-118">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,3 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-119">Taille de l’adresse du canal DMA, en bits.</span><span class="sxs-lookup"><span data-stu-id="26f0f-119">DMA channel address size, in bits.</span></span> <span data-ttu-id="26f0f-120">Les valeurs autorisées sont 8, 16, 32 et 64.</span><span class="sxs-lookup"><span data-stu-id="26f0f-120">Permissible values are 8, 16, 32, and 64.</span></span> <span data-ttu-id="26f0f-121">S’il est inconnu, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="26f0f-121">If unknown, enter 0.</span></span>

<dt>



 <span data-ttu-id="26f0f-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="26f0f-122">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26f0f-123">(8)</span><span class="sxs-lookup"><span data-stu-id="26f0f-123">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26f0f-124">(16)</span><span class="sxs-lookup"><span data-stu-id="26f0f-124">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26f0f-125">(32)</span><span class="sxs-lookup"><span data-stu-id="26f0f-125">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26f0f-126">(64)</span><span class="sxs-lookup"><span data-stu-id="26f0f-126">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26f0f-127">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="26f0f-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26f0f-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-130">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-131">Disponibilité du DMA.</span><span class="sxs-lookup"><span data-stu-id="26f0f-131">Availability of the DMA.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="26f0f-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="26f0f-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26f0f-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="26f0f-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-134">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="26f0f-134">Unknown.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="26f0f-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (3)</span><span class="sxs-lookup"><span data-stu-id="26f0f-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-136">Disponible.</span><span class="sxs-lookup"><span data-stu-id="26f0f-136">Available.</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="26f0f-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**En cours d’utilisation/non disponible** (4)</span><span class="sxs-lookup"><span data-stu-id="26f0f-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-138">En cours d’utilisation (non disponible).</span><span class="sxs-lookup"><span data-stu-id="26f0f-138">In use (not available).</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="26f0f-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**En cours d’utilisation et disponible/partageable** (5)</span><span class="sxs-lookup"><span data-stu-id="26f0f-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-140">En cours d’utilisation, mais disponibles (partageable).</span><span class="sxs-lookup"><span data-stu-id="26f0f-140">In use, but available (sharable).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="26f0f-141">**BurstMode**</span><span class="sxs-lookup"><span data-stu-id="26f0f-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="26f0f-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-144">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-145">Si la **valeur est true**, le canal DMA prend en charge le mode rafale.</span><span class="sxs-lookup"><span data-stu-id="26f0f-145">If **TRUE**, the DMA channel supports burst mode.</span></span>

</dd> <dt>

<span data-ttu-id="26f0f-146">**ByteMode**</span><span class="sxs-lookup"><span data-stu-id="26f0f-146">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-147">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26f0f-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-149">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-150">Indique si DMA peut s’exécuter en mode nombre par octet.</span><span class="sxs-lookup"><span data-stu-id="26f0f-150">Indicates whether DMA can execute in count-by-byte mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="26f0f-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="26f0f-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-152">Autre.</span><span class="sxs-lookup"><span data-stu-id="26f0f-152">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26f0f-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="26f0f-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-154">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="26f0f-154">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="26f0f-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Non exécuté dans le mode « comptage par octet »** (3)</span><span class="sxs-lookup"><span data-stu-id="26f0f-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-156">Exécution impossible en mode nombre par octet.</span><span class="sxs-lookup"><span data-stu-id="26f0f-156">Cannot execute in count-by-byte mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="26f0f-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Exécuter en mode « comptage par octet »** (4)</span><span class="sxs-lookup"><span data-stu-id="26f0f-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-158">Exécution en mode nombre par octet.</span><span class="sxs-lookup"><span data-stu-id="26f0f-158">Able to execute in count-by-byte mode.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="26f0f-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="26f0f-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26f0f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-162">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-163">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="26f0f-163">Short textual description of the object.</span></span>

<span data-ttu-id="26f0f-164">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26f0f-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26f0f-165">**ChannelTiming**</span><span class="sxs-lookup"><span data-stu-id="26f0f-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-166">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26f0f-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-168">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-169">Synchronisation du canal DMA.</span><span class="sxs-lookup"><span data-stu-id="26f0f-169">DMA channel timing.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="26f0f-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="26f0f-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-171">Autre.</span><span class="sxs-lookup"><span data-stu-id="26f0f-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26f0f-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="26f0f-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-173">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="26f0f-173">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="26f0f-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Compatible ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="26f0f-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-175">Compatible ISA.</span><span class="sxs-lookup"><span data-stu-id="26f0f-175">ISA-compatible.</span></span>

</dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="26f0f-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Tapez A** (4)</span><span class="sxs-lookup"><span data-stu-id="26f0f-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Type A** (4)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-177">Tapez un.</span><span class="sxs-lookup"><span data-stu-id="26f0f-177">Type A.</span></span>

</dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="26f0f-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Type B** (5)</span><span class="sxs-lookup"><span data-stu-id="26f0f-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Type B** (5)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-179">Tapez B.</span><span class="sxs-lookup"><span data-stu-id="26f0f-179">Type B.</span></span>

</dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="26f0f-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Tapez F** (6)</span><span class="sxs-lookup"><span data-stu-id="26f0f-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Type F** (6)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-181">Tapez F.</span><span class="sxs-lookup"><span data-stu-id="26f0f-181">Type F.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="26f0f-182">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="26f0f-182">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26f0f-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-185">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="26f0f-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-186">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="26f0f-186">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="26f0f-187">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="26f0f-187">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="26f0f-188">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="26f0f-188">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26f0f-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-191">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="26f0f-191">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-192">Portée du nom de la classe de création du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="26f0f-192">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="26f0f-193">**CSName**</span><span class="sxs-lookup"><span data-stu-id="26f0f-193">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26f0f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-196">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="26f0f-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-197">Nom du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="26f0f-197">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="26f0f-198">**Description**</span><span class="sxs-lookup"><span data-stu-id="26f0f-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26f0f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-201">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="26f0f-201">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-202">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="26f0f-202">Textual description of the object.</span></span>

<span data-ttu-id="26f0f-203">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26f0f-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26f0f-204">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="26f0f-204">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-205">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26f0f-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-207">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-208">Numéro de canal DMA.</span><span class="sxs-lookup"><span data-stu-id="26f0f-208">DMA channel number.</span></span> <span data-ttu-id="26f0f-209">Ce nombre fait partie de la valeur de clé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="26f0f-209">This number is part of the object's key value.</span></span>

</dd> <dt>

<span data-ttu-id="26f0f-210">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="26f0f-210">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-211">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="26f0f-211">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-213">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-214">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="26f0f-214">Date and time the object was installed.</span></span> <span data-ttu-id="26f0f-215">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="26f0f-215">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="26f0f-216">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26f0f-216">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26f0f-217">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="26f0f-217">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-218">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26f0f-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-220">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-220">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-221">Nombre maximal d’octets qui peuvent être transférés par ce canal DMA.</span><span class="sxs-lookup"><span data-stu-id="26f0f-221">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="26f0f-222">S’il est inconnu, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="26f0f-222">If unknown, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="26f0f-223">**Nom**</span><span class="sxs-lookup"><span data-stu-id="26f0f-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-224">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26f0f-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-226">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="26f0f-226">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-227">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="26f0f-227">Label by which the object is known.</span></span> <span data-ttu-id="26f0f-228">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="26f0f-228">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="26f0f-229">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26f0f-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26f0f-230">**État**</span><span class="sxs-lookup"><span data-stu-id="26f0f-230">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26f0f-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-233">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="26f0f-233">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-234">Indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="26f0f-234">Indicates the current status of the object.</span></span>

<span data-ttu-id="26f0f-235">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26f0f-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="26f0f-236">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="26f0f-236">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="26f0f-237">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-237">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="26f0f-238">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-238">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="26f0f-239">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-239">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26f0f-240">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="26f0f-240">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="26f0f-241">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-241">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="26f0f-242">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-242">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="26f0f-243">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-243">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="26f0f-244">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-244">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="26f0f-245">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-245">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="26f0f-246">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-246">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="26f0f-247">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-247">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="26f0f-248">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="26f0f-248">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26f0f-249">**TransferWidths**</span><span class="sxs-lookup"><span data-stu-id="26f0f-249">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-250">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26f0f-250">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-252">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-253">Tableau qui indique toutes les largeurs de transfert, en bits, prises en charge par ce canal DMA.</span><span class="sxs-lookup"><span data-stu-id="26f0f-253">Array that indicates all of the transfer widths, in bits, supported by this DMA channel.</span></span> <span data-ttu-id="26f0f-254">Les valeurs autorisées sont 8, 16, 32, 64 et 128 bits.</span><span class="sxs-lookup"><span data-stu-id="26f0f-254">Permissible values are 8, 16, 32, 64, and 128 bits.</span></span> <span data-ttu-id="26f0f-255">S’il est inconnu, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="26f0f-255">If unknown, enter 0 (zero).</span></span>

<dt>



 <span data-ttu-id="26f0f-256"> (0)</span><span class="sxs-lookup"><span data-stu-id="26f0f-256">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26f0f-257">(8)</span><span class="sxs-lookup"><span data-stu-id="26f0f-257">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26f0f-258">(16)</span><span class="sxs-lookup"><span data-stu-id="26f0f-258">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26f0f-259">(32)</span><span class="sxs-lookup"><span data-stu-id="26f0f-259">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26f0f-260">(64)</span><span class="sxs-lookup"><span data-stu-id="26f0f-260">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26f0f-261">(128)</span><span class="sxs-lookup"><span data-stu-id="26f0f-261">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26f0f-262">**TypeCTiming**</span><span class="sxs-lookup"><span data-stu-id="26f0f-262">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-263">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26f0f-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-265">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-266">Indique si le minutage du type C (rafale) est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="26f0f-266">Indicates whether Type C (burst) timing is supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="26f0f-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="26f0f-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-268">Autre.</span><span class="sxs-lookup"><span data-stu-id="26f0f-268">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26f0f-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="26f0f-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-270">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="26f0f-270">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="26f0f-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Compatible ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="26f0f-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-272">Compatible ISA.</span><span class="sxs-lookup"><span data-stu-id="26f0f-272">ISA-compatible.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="26f0f-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (4)</span><span class="sxs-lookup"><span data-stu-id="26f0f-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-274">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="26f0f-274">Not supported.</span></span>

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="26f0f-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Pris en charge** (5)</span><span class="sxs-lookup"><span data-stu-id="26f0f-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Supported** (5)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-276">Pris en charge.</span><span class="sxs-lookup"><span data-stu-id="26f0f-276">Supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="26f0f-277">**WordMode**</span><span class="sxs-lookup"><span data-stu-id="26f0f-277">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26f0f-278">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26f0f-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26f0f-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26f0f-280">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="26f0f-280">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="26f0f-281">Indique si DMA peut s’exécuter en mode Count-by-Word.</span><span class="sxs-lookup"><span data-stu-id="26f0f-281">Indicates whether DMA can execute in count-by-word mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="26f0f-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="26f0f-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-283">Autre.</span><span class="sxs-lookup"><span data-stu-id="26f0f-283">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26f0f-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="26f0f-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-285">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="26f0f-285">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="26f0f-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Ne pas exécuter en mode « nombre par mot »** (3)</span><span class="sxs-lookup"><span data-stu-id="26f0f-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-287">Exécution impossible en mode Count-by-Word.</span><span class="sxs-lookup"><span data-stu-id="26f0f-287">Cannot execute in count-by-word mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="26f0f-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Exécuter en mode « nombre par mot »** (4)</span><span class="sxs-lookup"><span data-stu-id="26f0f-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="26f0f-289">Exécution en mode Count-by-Word.</span><span class="sxs-lookup"><span data-stu-id="26f0f-289">Able to execute in count-by-word mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26f0f-290">Notes</span><span class="sxs-lookup"><span data-stu-id="26f0f-290">Remarks</span></span>

<span data-ttu-id="26f0f-291">La **classe \_ DMA CIM** est dérivée de la [**\_ SystemResource CIM**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="26f0f-291">The **CIM\_DMA** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="26f0f-292">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="26f0f-292">WMI does not implement this class.</span></span> <span data-ttu-id="26f0f-293">Pour les classes dérivées de la classe **\_ DMA CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="26f0f-293">For classes derived from **CIM\_DMA**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="26f0f-294">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="26f0f-294">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="26f0f-295">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="26f0f-295">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f0f-296">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26f0f-296">Requirements</span></span>



| <span data-ttu-id="26f0f-297">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26f0f-297">Requirement</span></span> | <span data-ttu-id="26f0f-298">Valeur</span><span class="sxs-lookup"><span data-stu-id="26f0f-298">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26f0f-299">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26f0f-299">Minimum supported client</span></span><br/> | <span data-ttu-id="26f0f-300">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26f0f-300">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26f0f-301">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26f0f-301">Minimum supported server</span></span><br/> | <span data-ttu-id="26f0f-302">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26f0f-302">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26f0f-303">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="26f0f-303">Namespace</span></span><br/>                | <span data-ttu-id="26f0f-304">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="26f0f-304">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26f0f-305">MOF</span><span class="sxs-lookup"><span data-stu-id="26f0f-305">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26f0f-306"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26f0f-306"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26f0f-307">DLL</span><span class="sxs-lookup"><span data-stu-id="26f0f-307">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26f0f-308"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26f0f-308"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f0f-309">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26f0f-309">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f0f-310">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="26f0f-310">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

