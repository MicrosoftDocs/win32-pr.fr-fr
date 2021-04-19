---
description: Décrit les fonctionnalités et la gestion d’un contrôleur série.
ms.assetid: ce3e0424-4ab8-435d-a155-1164535b3b0d
title: Classe CIM_SerialController (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a2e69bab38bb8b68c15ed93b2bee721c35a7600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514453"
---
# <a name="cim_serialcontroller-class-hyper-v-management"></a><span data-ttu-id="e04aa-103">Classe CIM_SerialController (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e04aa-103">CIM_SerialController class (Hyper-V management)</span></span>

<span data-ttu-id="e04aa-104">Décrit les fonctionnalités et la gestion d’un contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="e04aa-104">Describes the capabilities and management of a serial controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="e04aa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e04aa-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint32 MaxBaudRate;
  uint16 Security;
};
```

## <a name="members"></a><span data-ttu-id="e04aa-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e04aa-106">Members</span></span>

<span data-ttu-id="e04aa-107">La classe **CIM \_ SerialController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e04aa-107">The **CIM\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="e04aa-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e04aa-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e04aa-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e04aa-109">Properties</span></span>

<span data-ttu-id="e04aa-110">La classe **CIM \_ SerialController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e04aa-110">The **CIM\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e04aa-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e04aa-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04aa-112">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e04aa-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e04aa-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e04aa-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e04aa-114">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ports série DMTF \| 004,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="e04aa-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="e04aa-115">Compatibilité du niveau de microprocesseur pour le contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="e04aa-115">The chip level compatibility for the serial controller.</span></span> <span data-ttu-id="e04aa-116">Cette propriété décrit la mise en mémoire tampon et d’autres fonctionnalités du contrôleur série qui peuvent être inhérentes au matériel de puce.</span><span class="sxs-lookup"><span data-stu-id="e04aa-116">This property describes the buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e04aa-117">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e04aa-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e04aa-118">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e04aa-118">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="e04aa-119">**Compatible XT/AT** (3)</span><span class="sxs-lookup"><span data-stu-id="e04aa-119">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="e04aa-120">**Compatible 16450** (4)</span><span class="sxs-lookup"><span data-stu-id="e04aa-120">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="e04aa-121">**Compatible 16550** (5)</span><span class="sxs-lookup"><span data-stu-id="e04aa-121">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="e04aa-122">**compatible 16550A** (6)</span><span class="sxs-lookup"><span data-stu-id="e04aa-122">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="e04aa-123">**Compatible 8251** (160)</span><span class="sxs-lookup"><span data-stu-id="e04aa-123">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="e04aa-124">**compatible 8251FIFO** (161)</span><span class="sxs-lookup"><span data-stu-id="e04aa-124">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e04aa-125">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e04aa-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04aa-126">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="e04aa-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e04aa-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e04aa-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e04aa-128">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="e04aa-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="e04aa-129">Tableau qui contient des explications plus détaillées sur les fonctionnalités du contrôleur série dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="e04aa-129">An array that contains more detailed explanations for serial controller features in the **Capabilities** array.</span></span> <span data-ttu-id="e04aa-130">Les éléments du tableau **CapabilityDescriptions** sont corrélés à ceux du tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="e04aa-130">The items in the **CapabilityDescriptions** array correlate to those in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="e04aa-131">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="e04aa-131">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04aa-132">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e04aa-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e04aa-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e04aa-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e04aa-134">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) («MIF. \|Ports série DMTF \| 004,6 "), **punitif** (" bit/seconde ")</span><span class="sxs-lookup"><span data-stu-id="e04aa-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.6"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="e04aa-135">Débit en bauds maximal, en bits par seconde, pris en charge par le contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="e04aa-135">The maximum baud rate in, bits per second, that is supported by the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="e04aa-136">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="e04aa-136">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e04aa-137">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e04aa-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e04aa-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e04aa-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e04aa-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ports série DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="e04aa-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="e04aa-140">La sécurité opérationnelle pour le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="e04aa-140">The operational security for the controller.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e04aa-141">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e04aa-141">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e04aa-142">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e04aa-142">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="e04aa-143">**Aucun** (3)</span><span class="sxs-lookup"><span data-stu-id="e04aa-143">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Locked_Out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="e04aa-144">**Interface externe verrouillée** (4)</span><span class="sxs-lookup"><span data-stu-id="e04aa-144">**External Interface Locked Out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="e04aa-145">**Interface externe activée** (5)</span><span class="sxs-lookup"><span data-stu-id="e04aa-145">**External Interface Enabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="e04aa-146">**Contournement du démarrage** (6)</span><span class="sxs-lookup"><span data-stu-id="e04aa-146">**Boot Bypass** (6)</span></span>


<span data-ttu-id="e04aa-147"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e04aa-147"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e04aa-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e04aa-148">Requirements</span></span>



| <span data-ttu-id="e04aa-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e04aa-149">Requirement</span></span> | <span data-ttu-id="e04aa-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="e04aa-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e04aa-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e04aa-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e04aa-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e04aa-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e04aa-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e04aa-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e04aa-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e04aa-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e04aa-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e04aa-155">Namespace</span></span><br/>                | <span data-ttu-id="e04aa-156">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e04aa-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e04aa-157">MOF</span><span class="sxs-lookup"><span data-stu-id="e04aa-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e04aa-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e04aa-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e04aa-159">DLL</span><span class="sxs-lookup"><span data-stu-id="e04aa-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e04aa-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e04aa-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e04aa-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e04aa-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04aa-162">**\_Contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="e04aa-162">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

