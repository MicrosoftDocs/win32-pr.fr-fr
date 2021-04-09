---
description: La \_ classe WMI canal DMA WMI représente un canal d’accès direct à la mémoire (DMA) sur un système informatique exécutant Windows.
ms.assetid: cc517aac-7bd4-4937-8b07-2597076fca2c
ms.tgt_platform: multiple
title: Classe Win32_DMAChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DMAChannel
- Win32_DMAChannel.AddressSize
- Win32_DMAChannel.Availability
- Win32_DMAChannel.BurstMode
- Win32_DMAChannel.ByteMode
- Win32_DMAChannel.Caption
- Win32_DMAChannel.ChannelTiming
- Win32_DMAChannel.CreationClassName
- Win32_DMAChannel.CSCreationClassName
- Win32_DMAChannel.CSName
- Win32_DMAChannel.Description
- Win32_DMAChannel.DMAChannel
- Win32_DMAChannel.InstallDate
- Win32_DMAChannel.MaxTransferSize
- Win32_DMAChannel.Name
- Win32_DMAChannel.Port
- Win32_DMAChannel.Status
- Win32_DMAChannel.TransferWidths
- Win32_DMAChannel.TypeCTiming
- Win32_DMAChannel.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c2b36ff17931133d0dc4529e34f31ac24e00653
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861506"
---
# <a name="win32_dmachannel-class"></a><span data-ttu-id="0839a-103">\_Classe canal DMA Win32</span><span class="sxs-lookup"><span data-stu-id="0839a-103">Win32\_DMAChannel class</span></span>

<span data-ttu-id="0839a-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ canal DMA** WMI représente un canal d’accès direct à la mémoire (DMA) sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="0839a-104">The **Win32\_DMAChannel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a direct memory access (DMA) channel on a computer system running Windows.</span></span> <span data-ttu-id="0839a-105">DMA est une méthode permettant de déplacer des données d’un appareil vers la mémoire (ou vice versa) sans l’aide du microprocesseur.</span><span class="sxs-lookup"><span data-stu-id="0839a-105">DMA is a method of moving data from a device to memory (or vice versa) without the help of the microprocessor.</span></span> <span data-ttu-id="0839a-106">La carte système utilise un contrôleur DMA pour gérer un nombre fixe de canaux, chacun pouvant être utilisé par un (et un seul) appareil à la fois.</span><span class="sxs-lookup"><span data-stu-id="0839a-106">The system board uses a DMA controller to handle a fixed number of channels, each of which can be used by one (and only one) device at a time.</span></span>

<span data-ttu-id="0839a-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0839a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0839a-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0839a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0839a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0839a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DMAChannel : CIM_DMA
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
  uint32   Port;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="0839a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="0839a-110">Members</span></span>

<span data-ttu-id="0839a-111">La classe **Win32 \_ canal DMA** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0839a-111">The **Win32\_DMAChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="0839a-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0839a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0839a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0839a-113">Properties</span></span>

<span data-ttu-id="0839a-114">La classe **Win32 \_ canal DMA** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0839a-114">The **Win32\_DMAChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0839a-115">**AddressSize**</span><span class="sxs-lookup"><span data-stu-id="0839a-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0839a-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-118">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,3 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="0839a-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-119">Taille de l’adresse du canal DMA en bits.</span><span class="sxs-lookup"><span data-stu-id="0839a-119">DMA channel address size in bits.</span></span> <span data-ttu-id="0839a-120">Les valeurs autorisées sont 8, 16, 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0839a-120">Permissible values are 8, 16, 32, or 64 bits.</span></span> <span data-ttu-id="0839a-121">S’il est inconnu, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="0839a-121">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="0839a-122">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-122">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="0839a-123"> (0)</span><span class="sxs-lookup"><span data-stu-id="0839a-123">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0839a-124">(8)</span><span class="sxs-lookup"><span data-stu-id="0839a-124">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0839a-125">(16)</span><span class="sxs-lookup"><span data-stu-id="0839a-125">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0839a-126">(32)</span><span class="sxs-lookup"><span data-stu-id="0839a-126">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0839a-127">(64)</span><span class="sxs-lookup"><span data-stu-id="0839a-127">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0839a-128">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="0839a-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0839a-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-131">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="0839a-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-132">Disponibilité du DMA.</span><span class="sxs-lookup"><span data-stu-id="0839a-132">Availability of the DMA.</span></span> <span data-ttu-id="0839a-133">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-133">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0839a-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0839a-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0839a-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0839a-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="0839a-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (3)</span><span class="sxs-lookup"><span data-stu-id="0839a-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="0839a-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**En cours d’utilisation/non disponible** (4)</span><span class="sxs-lookup"><span data-stu-id="0839a-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0839a-138">En cours d’utilisation ou non disponible</span><span class="sxs-lookup"><span data-stu-id="0839a-138">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="0839a-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**En cours d’utilisation et disponible/partageable** (5)</span><span class="sxs-lookup"><span data-stu-id="0839a-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0839a-140">En cours d’utilisation et disponible ou partageable</span><span class="sxs-lookup"><span data-stu-id="0839a-140">In Use and Available or Sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0839a-141">**BurstMode**</span><span class="sxs-lookup"><span data-stu-id="0839a-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0839a-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-144">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="0839a-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-145">Indique si le canal DMA prend en charge le mode rafale.</span><span class="sxs-lookup"><span data-stu-id="0839a-145">Indicates whether or not the DMA channel supports burst mode.</span></span>

<span data-ttu-id="0839a-146">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-146">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="0839a-147">**ByteMode**</span><span class="sxs-lookup"><span data-stu-id="0839a-147">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-148">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0839a-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-150">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="0839a-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-151">Mode d’exécution DMA.</span><span class="sxs-lookup"><span data-stu-id="0839a-151">DMA execution mode.</span></span>

<span data-ttu-id="0839a-152">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-152">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0839a-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0839a-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0839a-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0839a-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="0839a-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Non exécuté dans le mode « comptage par octet »** (3)</span><span class="sxs-lookup"><span data-stu-id="0839a-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0839a-156">Ne s’exécute pas en mode « nombre par octet »</span><span class="sxs-lookup"><span data-stu-id="0839a-156">Does not execute in "count by byte" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="0839a-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Exécuter en mode « comptage par octet »** (4)</span><span class="sxs-lookup"><span data-stu-id="0839a-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0839a-158">Exécuter en mode « nombre par octet »</span><span class="sxs-lookup"><span data-stu-id="0839a-158">Execute in "count by byte" mode</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0839a-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0839a-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0839a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-162">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="0839a-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-163">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="0839a-163">Short description of the object a one-line string.</span></span>

<span data-ttu-id="0839a-164">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0839a-165">**ChannelTiming**</span><span class="sxs-lookup"><span data-stu-id="0839a-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-166">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0839a-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-168">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="0839a-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-169">Synchronisation du canal DMA.</span><span class="sxs-lookup"><span data-stu-id="0839a-169">DMA channel timing.</span></span>

<span data-ttu-id="0839a-170">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-170">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0839a-171">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0839a-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0839a-172">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0839a-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="0839a-173">**Compatible ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="0839a-173">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="0839a-174">**Tapez A** (4)</span><span class="sxs-lookup"><span data-stu-id="0839a-174">**Type A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="0839a-175">**Type B** (5)</span><span class="sxs-lookup"><span data-stu-id="0839a-175">**Type B** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="0839a-176">**Tapez F** (6)</span><span class="sxs-lookup"><span data-stu-id="0839a-176">**Type F** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0839a-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0839a-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0839a-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-180">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0839a-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0839a-181">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0839a-181">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0839a-182">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="0839a-182">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0839a-183">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-183">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="0839a-184">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0839a-184">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0839a-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-187">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0839a-187">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0839a-188">Nom de la classe de création de système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0839a-188">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="0839a-189">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-189">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="0839a-190">**CSName**</span><span class="sxs-lookup"><span data-stu-id="0839a-190">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0839a-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-193">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0839a-193">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0839a-194">Nom du système informatique d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0839a-194">Name of the scoping computer system.</span></span>

<span data-ttu-id="0839a-195">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-195">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="0839a-196">**Description**</span><span class="sxs-lookup"><span data-stu-id="0839a-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0839a-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-199">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0839a-199">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-200">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0839a-200">Description of the object.</span></span>

<span data-ttu-id="0839a-201">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0839a-202">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="0839a-202">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-203">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0839a-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-205">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="0839a-205">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-206">Numéro de canal DMA, qui fait partie de la valeur de clé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0839a-206">DMA channel number, part of the object's key value.</span></span>

<span data-ttu-id="0839a-207">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-207">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="0839a-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0839a-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-209">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0839a-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-211">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="0839a-211">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-212">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0839a-212">Date and time the object was installed.</span></span> <span data-ttu-id="0839a-213">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="0839a-213">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0839a-214">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0839a-215">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="0839a-215">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-216">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0839a-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-218">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="0839a-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-219">Nombre maximal d’octets qui peuvent être transférés par ce canal DMA.</span><span class="sxs-lookup"><span data-stu-id="0839a-219">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="0839a-220">S’il est inconnu, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="0839a-220">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="0839a-221">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-221">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="0839a-222">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0839a-222">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0839a-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-225">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0839a-225">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-226">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="0839a-226">Label by which the object is known.</span></span> <span data-ttu-id="0839a-227">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="0839a-227">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0839a-228">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0839a-229">**Port**</span><span class="sxs-lookup"><span data-stu-id="0839a-229">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-230">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0839a-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-232">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| System structures \| [**cm \_ Partial \_ Resource \_ descripteur**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| \| port DMA")</span><span class="sxs-lookup"><span data-stu-id="0839a-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Dma\|Port")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-233">Port DMA utilisé par l’adaptateur de bus hôte.</span><span class="sxs-lookup"><span data-stu-id="0839a-233">DMA port used by the host bus adapter.</span></span> <span data-ttu-id="0839a-234">Cela est significatif pour les bus de type MCA.</span><span class="sxs-lookup"><span data-stu-id="0839a-234">This is meaningful for MCA-type buses.</span></span>

<span data-ttu-id="0839a-235">Exemple : 12</span><span class="sxs-lookup"><span data-stu-id="0839a-235">Example: 12</span></span>

</dd> <dt>

<span data-ttu-id="0839a-236">**État**</span><span class="sxs-lookup"><span data-stu-id="0839a-236">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0839a-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-239">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0839a-239">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-240">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0839a-240">Current status of the object.</span></span> <span data-ttu-id="0839a-241">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="0839a-241">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0839a-242">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="0839a-242">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0839a-243">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="0839a-243">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0839a-244">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="0839a-244">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0839a-245">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="0839a-245">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0839a-246">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-246">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0839a-247">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0839a-247">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0839a-248">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="0839a-248">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0839a-249">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="0839a-249">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0839a-250">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0839a-250">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0839a-251">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="0839a-251">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0839a-252">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0839a-252">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0839a-253">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0839a-253">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0839a-254">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0839a-254">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0839a-255">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="0839a-255">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0839a-256">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="0839a-256">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0839a-257">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="0839a-257">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0839a-258">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="0839a-258">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0839a-259">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="0839a-259">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0839a-260">**TransferWidths**</span><span class="sxs-lookup"><span data-stu-id="0839a-260">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-261">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0839a-261">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0839a-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-263">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="0839a-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-264">Tableau de toutes les largeurs de transfert (en bits) prises en charge par ce canal DMA.</span><span class="sxs-lookup"><span data-stu-id="0839a-264">Array of all the transfer widths (in bits) supported by this DMA channel.</span></span> <span data-ttu-id="0839a-265">S’il est inconnu, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="0839a-265">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="0839a-266">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-266">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="0839a-267"> (0)</span><span class="sxs-lookup"><span data-stu-id="0839a-267">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0839a-268">(8)</span><span class="sxs-lookup"><span data-stu-id="0839a-268">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0839a-269">(16)</span><span class="sxs-lookup"><span data-stu-id="0839a-269">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0839a-270">(32)</span><span class="sxs-lookup"><span data-stu-id="0839a-270">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0839a-271">(64)</span><span class="sxs-lookup"><span data-stu-id="0839a-271">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0839a-272">(128)</span><span class="sxs-lookup"><span data-stu-id="0839a-272">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0839a-273">**TypeCTiming**</span><span class="sxs-lookup"><span data-stu-id="0839a-273">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-274">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0839a-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-276">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="0839a-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-277">Prise en charge du minutage de type C (rafale).</span><span class="sxs-lookup"><span data-stu-id="0839a-277">Support for C type (burst) timing.</span></span>

<span data-ttu-id="0839a-278">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-278">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0839a-279">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0839a-279">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0839a-280">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0839a-280">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="0839a-281">**Compatible ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="0839a-281">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0839a-282">**Non pris en charge** (4)</span><span class="sxs-lookup"><span data-stu-id="0839a-282">**Not Supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="0839a-283">**Pris en charge** (5)</span><span class="sxs-lookup"><span data-stu-id="0839a-283">**Supported** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0839a-284">**WordMode**</span><span class="sxs-lookup"><span data-stu-id="0839a-284">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0839a-285">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0839a-285">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0839a-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0839a-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0839a-287">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations DMA de ressource système DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="0839a-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="0839a-288">Mode d’exécution DMA.</span><span class="sxs-lookup"><span data-stu-id="0839a-288">DMA execution mode.</span></span>

<span data-ttu-id="0839a-289">Cette propriété est héritée de la [**\_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-289">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0839a-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0839a-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0839a-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0839a-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="0839a-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Ne pas exécuter en mode « nombre par mot »** (3)</span><span class="sxs-lookup"><span data-stu-id="0839a-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0839a-293">Ne s’exécute pas en mode « nombre par mot »</span><span class="sxs-lookup"><span data-stu-id="0839a-293">Does not execute in "count by word" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="0839a-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Exécuter en mode « nombre par mot »** (4)</span><span class="sxs-lookup"><span data-stu-id="0839a-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0839a-295">Exécuter en mode « nombre par mot »</span><span class="sxs-lookup"><span data-stu-id="0839a-295">Execute in "count by word" mode</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0839a-296">Notes</span><span class="sxs-lookup"><span data-stu-id="0839a-296">Remarks</span></span>

<span data-ttu-id="0839a-297">La classe **Win32 \_ canal DMA** est dérivée [**de \_ DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="0839a-297">The **Win32\_DMAChannel** class is derived from [**CIM\_DMA**](cim-dma.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0839a-298">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0839a-298">Requirements</span></span>



| <span data-ttu-id="0839a-299">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0839a-299">Requirement</span></span> | <span data-ttu-id="0839a-300">Valeur</span><span class="sxs-lookup"><span data-stu-id="0839a-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0839a-301">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0839a-301">Minimum supported client</span></span><br/> | <span data-ttu-id="0839a-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0839a-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0839a-303">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0839a-303">Minimum supported server</span></span><br/> | <span data-ttu-id="0839a-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0839a-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0839a-305">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0839a-305">Namespace</span></span><br/>                | <span data-ttu-id="0839a-306">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0839a-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0839a-307">MOF</span><span class="sxs-lookup"><span data-stu-id="0839a-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0839a-308"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0839a-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0839a-309">DLL</span><span class="sxs-lookup"><span data-stu-id="0839a-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0839a-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0839a-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0839a-311">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0839a-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0839a-312">**\_DMA CIM**</span><span class="sxs-lookup"><span data-stu-id="0839a-312">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dt>

[<span data-ttu-id="0839a-313">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="0839a-313">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

