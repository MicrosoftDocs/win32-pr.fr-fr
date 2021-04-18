---
description: Représente un contrôleur d’affichage.
ms.assetid: 14598ae6-58e2-46ca-8653-b57e5833a224
title: Classe CIM_DisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisplayController
- CIM_DisplayController.Description
- CIM_DisplayController.VideoProcessor
- CIM_DisplayController.VideoMemoryType
- CIM_DisplayController.OtherVideoMemoryType
- CIM_DisplayController.NumberOfVideoPages
- CIM_DisplayController.MaxMemorySupported
- CIM_DisplayController.AcceleratorCapabilities
- CIM_DisplayController.CapabilityDescriptions
- CIM_DisplayController.OtherVideoArchitecture
- CIM_DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59db37a89ce1f57e01a6a9a27fb9c24177221b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529130"
---
# <a name="cim_displaycontroller-class"></a><span data-ttu-id="2094a-103">\_Classe CIM DisplayController</span><span class="sxs-lookup"><span data-stu-id="2094a-103">CIM\_DisplayController class</span></span>

<span data-ttu-id="2094a-104">Représente un contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="2094a-104">Represents a display controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="2094a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2094a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_DisplayController : CIM_Controller
{
  string Description;
  string VideoProcessor;
  uint16 VideoMemoryType;
  string OtherVideoMemoryType;
  uint32 NumberOfVideoPages;
  uint32 MaxMemorySupported;
  uint16 AcceleratorCapabilities[];
  string CapabilityDescriptions[];
  string OtherVideoArchitecture;
  uint16 VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="2094a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2094a-106">Members</span></span>

<span data-ttu-id="2094a-107">La classe **CIM \_ DisplayController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2094a-107">The **CIM\_DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="2094a-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2094a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2094a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2094a-109">Properties</span></span>

<span data-ttu-id="2094a-110">La classe **CIM \_ DisplayController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2094a-110">The **CIM\_DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2094a-111">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2094a-111">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2094a-112">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2094a-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2094a-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2094a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2094a-114">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="2094a-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="2094a-115">Les fonctionnalités graphiques et 3D du contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="2094a-115">The graphics and 3D capabilities of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2094a-116">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2094a-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2094a-117">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2094a-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="2094a-118">**Accélérateur graphique** (2)</span><span class="sxs-lookup"><span data-stu-id="2094a-118">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="2094a-119">**accélérateur 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="2094a-119">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Fast_Write"></span><span id="pci_fast_write"></span><span id="PCI_FAST_WRITE"></span>

<span data-ttu-id="2094a-120">**Écriture rapide PCI** (4)</span><span class="sxs-lookup"><span data-stu-id="2094a-120">**PCI Fast Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiMonitor_Support"></span><span id="multimonitor_support"></span><span id="MULTIMONITOR_SUPPORT"></span>

<span data-ttu-id="2094a-121">**Prise en charge multimoniteur** (5)</span><span class="sxs-lookup"><span data-stu-id="2094a-121">**MultiMonitor Support** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Mastering"></span><span id="pci_mastering"></span><span id="PCI_MASTERING"></span>

<span data-ttu-id="2094a-122">**Mastérisation PCI** (6)</span><span class="sxs-lookup"><span data-stu-id="2094a-122">**PCI Mastering** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Second_Monochrome_Adapter_Support"></span><span id="second_monochrome_adapter_support"></span><span id="SECOND_MONOCHROME_ADAPTER_SUPPORT"></span>

<span data-ttu-id="2094a-123">**Prise en charge d’un deuxième adaptateur monochrome** (7)</span><span class="sxs-lookup"><span data-stu-id="2094a-123">**Second Monochrome Adapter Support** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Large_Memory_Address_Support"></span><span id="large_memory_address_support"></span><span id="LARGE_MEMORY_ADDRESS_SUPPORT"></span>

<span data-ttu-id="2094a-124">**Prise en charge des adresses mémoire volumineuses** (8)</span><span class="sxs-lookup"><span data-stu-id="2094a-124">**Large Memory Address Support** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2094a-125">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2094a-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2094a-126">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2094a-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2094a-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2094a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2094a-128">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="2094a-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="2094a-129">Explications détaillées sur les fonctionnalités d’accélérateur vidéo du tableau **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2094a-129">Detailed explanations for video accelerator features of the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="2094a-130">Les éléments de ce tableau correspondent aux éléments de tableau dans **AcceleratorCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="2094a-130">The items in this array correspond to the array items in **AcceleratorCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="2094a-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="2094a-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2094a-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2094a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2094a-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2094a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2094a-134">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 004,18 ")</span><span class="sxs-lookup"><span data-stu-id="2094a-134">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.18")</span></span>
</dt> </dl>

<span data-ttu-id="2094a-135">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2094a-135">A text description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="2094a-136">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="2094a-136">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2094a-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2094a-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2094a-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2094a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2094a-139">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="2094a-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="2094a-140">Quantité maximale de mémoire prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="2094a-140">The maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2094a-141">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="2094a-141">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2094a-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2094a-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2094a-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2094a-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2094a-144">Nombre de pages vidéo prises en charge en fonction des résolutions actuelles et de la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="2094a-144">The number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="2094a-145">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="2094a-145">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2094a-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2094a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2094a-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2094a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2094a-148">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**VideoArchitecture**")</span><span class="sxs-lookup"><span data-stu-id="2094a-148">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoArchitecture**")</span></span>
</dt> </dl>

<span data-ttu-id="2094a-149">Description du type d’architecture vidéo lorsque la propriété **VideoArchitecture** contient « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="2094a-149">A description of the video architecture type when the **VideoArchitecture** property contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="2094a-150">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="2094a-150">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2094a-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2094a-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2094a-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2094a-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2094a-153">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**VideoMemoryType**")</span><span class="sxs-lookup"><span data-stu-id="2094a-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="2094a-154">Type de mémoire vidéo lorsque la propriété **VideoMemoryType** est « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="2094a-154">The video memory type when the **VideoMemoryType** property is "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="2094a-155">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="2094a-155">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2094a-156">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2094a-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2094a-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2094a-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2094a-158">Architecture vidéo des contrôleurs d’affichage utilisée pour générer le signal vidéo.</span><span class="sxs-lookup"><span data-stu-id="2094a-158">The display controllers video architecture used to generate the video signal.</span></span> <span data-ttu-id="2094a-159">En règle générale, un processeur vidéo dédié génère le signal vidéo conformément à l’architecture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2094a-159">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="2094a-160">L’architecture indique la capacité de résolution maximale du contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="2094a-160">The architecture indicates of the maximum resolution capability of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2094a-161">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2094a-161">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2094a-162">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2094a-162">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="2094a-163">**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="2094a-163">**CGA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="2094a-164">**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="2094a-164">**EGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="2094a-165">**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="2094a-165">**VGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="2094a-166">**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="2094a-166">**SVGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="2094a-167">**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="2094a-167">**MDA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="2094a-168">**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="2094a-168">**HGC** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="2094a-169">**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="2094a-169">**MCGA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="2094a-170">**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="2094a-170">**8514A** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="2094a-171">**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="2094a-171">**XGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="2094a-172">**Mémoire tampon de trame linéaire** (11)</span><span class="sxs-lookup"><span data-stu-id="2094a-172">**Linear Frame Buffer** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="2094a-173">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="2094a-173">**PC-98** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2094a-174">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2094a-174">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2094a-175">**Fournisseur réservé** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="2094a-175">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2094a-176">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="2094a-176">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2094a-177">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2094a-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2094a-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2094a-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2094a-179">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 004,6 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**OtherVideoMemoryType**")</span><span class="sxs-lookup"><span data-stu-id="2094a-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.6"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**OtherVideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="2094a-180">Type de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="2094a-180">The type of video memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2094a-181">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2094a-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2094a-182">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2094a-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="2094a-183">**VRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="2094a-183">**VRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="2094a-184">**DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="2094a-184">**DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="2094a-185">**SRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="2094a-185">**SRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="2094a-186">**WRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="2094a-186">**WRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="2094a-187">**Mémoire vive Edo** (6)</span><span class="sxs-lookup"><span data-stu-id="2094a-187">**EDO RAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="2094a-188">**DRAM synchrone en rafale** (7)</span><span class="sxs-lookup"><span data-stu-id="2094a-188">**Burst Synchronous DRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="2094a-189">**SRAM en rafale pipeline** (8)</span><span class="sxs-lookup"><span data-stu-id="2094a-189">**Pipelined Burst SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="2094a-190">**CDRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="2094a-190">**CDRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="2094a-191">**3DRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="2094a-191">**3DRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="2094a-192">**SDRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="2094a-192">**SDRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="2094a-193">**SGRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="2094a-193">**SGRAM** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2094a-194">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="2094a-194">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2094a-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2094a-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2094a-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2094a-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2094a-197">Description textuelle du processeur/contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="2094a-197">A text description of the video processor/controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2094a-198">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2094a-198">Requirements</span></span>



| <span data-ttu-id="2094a-199">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2094a-199">Requirement</span></span> | <span data-ttu-id="2094a-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="2094a-200">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2094a-201">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2094a-201">Minimum supported client</span></span><br/> | <span data-ttu-id="2094a-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2094a-202">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2094a-203">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2094a-203">Minimum supported server</span></span><br/> | <span data-ttu-id="2094a-204">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2094a-204">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2094a-205">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2094a-205">Namespace</span></span><br/>                | <span data-ttu-id="2094a-206">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2094a-206">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2094a-207">MOF</span><span class="sxs-lookup"><span data-stu-id="2094a-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2094a-208"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2094a-208"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2094a-209">DLL</span><span class="sxs-lookup"><span data-stu-id="2094a-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2094a-210"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2094a-210"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2094a-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2094a-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2094a-212">**\_Contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="2094a-212">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

