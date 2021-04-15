---
description: Représente les fonctionnalités et la gestion des périphériques logiques liés à la mémoire.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: Classe CIM_Memory (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529505"
---
# <a name="cim_memory-class-hyper-v-management"></a><span data-ttu-id="495ea-103">Classe CIM_Memory (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="495ea-103">CIM_Memory class (Hyper-V management)</span></span>

<span data-ttu-id="495ea-104">Représente les fonctionnalités et la gestion des périphériques logiques liés à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="495ea-104">Represents the capabilities and management of memory-related logical devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="495ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="495ea-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="495ea-106">Membres</span><span class="sxs-lookup"><span data-stu-id="495ea-106">Members</span></span>

<span data-ttu-id="495ea-107">La classe de **\_ mémoire CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="495ea-107">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="495ea-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="495ea-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="495ea-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="495ea-109">Properties</span></span>

<span data-ttu-id="495ea-110">La classe de **\_ mémoire CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="495ea-110">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="495ea-111">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="495ea-111">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-112">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="495ea-112">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="495ea-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-114">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 005,18 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,13 ")</span><span class="sxs-lookup"><span data-stu-id="495ea-114">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.18", "MIF.DMTF\|Physical Memory Array\|001.13")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-115">Tableau d’octets qui contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="495ea-115">An array of octets that contains additional error information.</span></span> <span data-ttu-id="495ea-116">Par exemple, le syndrome ECC ou le retour des bits de vérification si une méthodologie d’erreur basée sur CRC est utilisée.</span><span class="sxs-lookup"><span data-stu-id="495ea-116">An example is ECC syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="495ea-117">Dans ce dernier cas, si une erreur de bit unique est reconnue et que l’algorithme CRC est connu, il est possible de déterminer le bit exact qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="495ea-117">In the latter case, if a single bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span>

<span data-ttu-id="495ea-118">Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="495ea-118">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-119">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="495ea-119">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-120">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="495ea-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-122">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="495ea-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-123">**true** si l’erreur la plus récente est correcte ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="495ea-123">**true** if the most recent error is correctable; otherwise, **false**.</span></span> <span data-ttu-id="495ea-124">Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="495ea-124">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="495ea-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="495ea-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-128">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilo-octets"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,4 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,5 "), **punitif** (" Byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="495ea-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-129">Adresse de fin référencée par une application ou un système d’exploitation, et mappée par un contrôleur de mémoire pour l’objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="495ea-129">The ending address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="495ea-130">L’adresse de fin est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="495ea-130">The ending address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-131">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="495ea-131">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-132">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="495ea-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-134">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="495ea-134">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-135">Opération d’accès mémoire qui a provoqué la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="495ea-135">The memory access operation that caused the last error.</span></span> <span data-ttu-id="495ea-136">Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="495ea-136">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="495ea-137">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="495ea-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="495ea-138">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="495ea-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="495ea-139">**Lecture** (3)</span><span class="sxs-lookup"><span data-stu-id="495ea-139">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="495ea-140">**Écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="495ea-140">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="495ea-141">**Écriture partielle** (5)</span><span class="sxs-lookup"><span data-stu-id="495ea-141">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="495ea-142">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="495ea-142">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-143">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="495ea-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-145">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. de l’unités de"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 005,19 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="495ea-145">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.19", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-146">Adresse de la dernière erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="495ea-146">The address of the last memory error.</span></span> <span data-ttu-id="495ea-147">Le type d’erreur est décrit par la propriété **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="495ea-147">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="495ea-148">Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="495ea-148">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-149">**Partagefichiers**</span><span class="sxs-lookup"><span data-stu-id="495ea-149">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-150">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="495ea-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="495ea-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-152">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorData"), **OctetString**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,12 ")</span><span class="sxs-lookup"><span data-stu-id="495ea-152">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorData"), **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.12")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-153">Tableau qui contient les données capturées au cours du dernier accès mémoire erroné.</span><span class="sxs-lookup"><span data-stu-id="495ea-153">An array that contains data captured during the last erroneous memory access.</span></span> <span data-ttu-id="495ea-154">Les données occupent les n premiers octets du tableau nécessaire pour contenir le nombre de bits spécifié par la propriété **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="495ea-154">The data occupies the first n octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span>

<span data-ttu-id="495ea-155">Si la propriété **ErrorTransferSize** contient « 0 » (OK), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="495ea-155">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-156">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="495ea-156">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-157">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="495ea-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-159">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorDataOrder")</span><span class="sxs-lookup"><span data-stu-id="495ea-159">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorDataOrder")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-160">Classement des données stockées dans la propriété **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="495ea-160">The ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="495ea-161">Vous pouvez spécifier « octet le moins significatif en premier » (valeur = 1) ou « octet le plus significatif en premier » (2).</span><span class="sxs-lookup"><span data-stu-id="495ea-161">"Least Significant Byte First" (value=1) or "Most Significant Byte First" (2) can be specified.</span></span> <span data-ttu-id="495ea-162">Si la propriété **ErrorTransferSize** contient « 0 » (OK), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="495ea-162">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="495ea-163">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="495ea-163">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="495ea-164">**Octet le moins significatif en premier** (1)</span><span class="sxs-lookup"><span data-stu-id="495ea-164">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="495ea-165">**Octet le plus significatif en premier** (2)</span><span class="sxs-lookup"><span data-stu-id="495ea-165">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="495ea-166">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="495ea-166">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="495ea-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-169">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 005,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ mémoire CIM**.**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="495ea-169">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-170">Type de la dernière erreur à se produire.</span><span class="sxs-lookup"><span data-stu-id="495ea-170">The type of the last error to occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="495ea-171">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="495ea-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="495ea-172">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="495ea-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="495ea-173">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="495ea-173">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="495ea-174">**Lecture incorrecte** (4)</span><span class="sxs-lookup"><span data-stu-id="495ea-174">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="495ea-175">**Erreur de parité** (5)</span><span class="sxs-lookup"><span data-stu-id="495ea-175">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="495ea-176">**Erreur de bit unique** (6)</span><span class="sxs-lookup"><span data-stu-id="495ea-176">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="495ea-177">**Erreur double bit** (7)</span><span class="sxs-lookup"><span data-stu-id="495ea-177">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="495ea-178">**Erreur multibits** (8)</span><span class="sxs-lookup"><span data-stu-id="495ea-178">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="495ea-179">**Erreur de grignotage** (9)</span><span class="sxs-lookup"><span data-stu-id="495ea-179">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="495ea-180">**Erreur de somme de contrôle** (10)</span><span class="sxs-lookup"><span data-stu-id="495ea-180">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="495ea-181">**Erreur CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="495ea-181">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="495ea-182">**Non défini** (12)</span><span class="sxs-lookup"><span data-stu-id="495ea-182">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="495ea-183">**Non défini** (13)</span><span class="sxs-lookup"><span data-stu-id="495ea-183">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="495ea-184">**Non défini** (14)</span><span class="sxs-lookup"><span data-stu-id="495ea-184">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="495ea-185">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="495ea-185">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495ea-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-188">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="495ea-188">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-189">Indique si les algorithmes de parité, les algorithmes CRC, l’ECC ou d’autres mécanismes sont utilisés par l’objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="495ea-189">Indicates whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used by the memory object.</span></span> <span data-ttu-id="495ea-190">Vous pouvez également fournir des détails sur l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="495ea-190">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-191">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="495ea-191">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-192">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="495ea-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-194">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorResolution"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 005,21 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,15 "), **punitif** (" Byte ")</span><span class="sxs-lookup"><span data-stu-id="495ea-194">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.21", "MIF.DMTF\|Physical Memory Array\|001.15"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-195">Plage, en octets, dans laquelle la dernière erreur peut être résolue.</span><span class="sxs-lookup"><span data-stu-id="495ea-195">The range, in bytes, in which the last error can be resolved.</span></span> <span data-ttu-id="495ea-196">Par exemple, si les adresses d’erreur sont résolues en bit 11, par exemple sur une base de page par défaut ; Ensuite, les erreurs peuvent être résolues en limites de 4 Ko, et cette propriété est définie sur « 4000 ».</span><span class="sxs-lookup"><span data-stu-id="495ea-196">For example, if error addresses are resolved to bit 11, such as on a typical page basis; then the errors can be resolved to 4K boundaries, and this property is set to "4000".</span></span> <span data-ttu-id="495ea-197">Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="495ea-197">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-198">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="495ea-198">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-199">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="495ea-199">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-201">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTime")</span><span class="sxs-lookup"><span data-stu-id="495ea-201">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTime")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-202">Heure à laquelle la dernière erreur de mémoire s’est produite.</span><span class="sxs-lookup"><span data-stu-id="495ea-202">The time when the last memory error occurred.</span></span> <span data-ttu-id="495ea-203">Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="495ea-203">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-204">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="495ea-204">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-205">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="495ea-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-207">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTransferSize"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,11 "), **punitif** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="495ea-207">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTransferSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.11"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-208">Taille du transfert de données, en bits, à l’origine de la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="495ea-208">The size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="495ea-209">« 0 » n’indique aucune erreur.</span><span class="sxs-lookup"><span data-stu-id="495ea-209">"0" indicates no error.</span></span> <span data-ttu-id="495ea-210">Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="495ea-210">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-211">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="495ea-211">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-212">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="495ea-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-214">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ mémoire CIM**.**ErrorInfo**»)</span><span class="sxs-lookup"><span data-stu-id="495ea-214">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-215">Description du type d’erreur, lorsque la propriété **ErrorType** est définie sur « 1 » (other).</span><span class="sxs-lookup"><span data-stu-id="495ea-215">A description of the error type, when the **ErrorType** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="495ea-216">**De la**</span><span class="sxs-lookup"><span data-stu-id="495ea-216">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-217">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="495ea-217">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-219">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilo-octets"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,3 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,4 "), **punitif** (" Byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="495ea-219">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-220">Adresse de départ référencée par une application ou un système d’exploitation, et mappée par un contrôleur de mémoire pour l’objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="495ea-220">The starting address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="495ea-221">L’adresse de départ est spécifiée en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="495ea-221">The starting address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-222">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="495ea-222">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-223">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="495ea-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495ea-225">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.SystemLevelAddress")</span><span class="sxs-lookup"><span data-stu-id="495ea-225">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.SystemLevelAddress")</span></span>
</dt> </dl>

<span data-ttu-id="495ea-226">**true** si les informations d’adresse dans la propriété **ErrorAddress** sont une adresse de niveau système, **false** s’il s’agit d’une adresse physique.</span><span class="sxs-lookup"><span data-stu-id="495ea-226">**true** if the address information in the **ErrorAddress** property is a system-level address, **false** if it is a physical address.</span></span>

</dd> <dt>

<span data-ttu-id="495ea-227">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="495ea-227">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495ea-228">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="495ea-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="495ea-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="495ea-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="495ea-230">**true** si la mémoire est volatile ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="495ea-230">**true** if the memory is volatile; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="495ea-231">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="495ea-231">Requirements</span></span>



| <span data-ttu-id="495ea-232">Condition requise</span><span class="sxs-lookup"><span data-stu-id="495ea-232">Requirement</span></span> | <span data-ttu-id="495ea-233">Valeur</span><span class="sxs-lookup"><span data-stu-id="495ea-233">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="495ea-234">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="495ea-234">Minimum supported client</span></span><br/> | <span data-ttu-id="495ea-235">Windows 8</span><span class="sxs-lookup"><span data-stu-id="495ea-235">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="495ea-236">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="495ea-236">Minimum supported server</span></span><br/> | <span data-ttu-id="495ea-237">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="495ea-237">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="495ea-238">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="495ea-238">Namespace</span></span><br/>                | <span data-ttu-id="495ea-239">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="495ea-239">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="495ea-240">MOF</span><span class="sxs-lookup"><span data-stu-id="495ea-240">MOF</span></span><br/>                      | <dl> <span data-ttu-id="495ea-241"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="495ea-241"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="495ea-242">DLL</span><span class="sxs-lookup"><span data-stu-id="495ea-242">DLL</span></span><br/>                      | <dl> <span data-ttu-id="495ea-243"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="495ea-243"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="495ea-244">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="495ea-244">See also</span></span>

<dl> <dt>

[<span data-ttu-id="495ea-245">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="495ea-245">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

