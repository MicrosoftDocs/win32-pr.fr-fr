---
description: Représente un en-tête d’un \_ objet CIM DisplayController.
ms.assetid: 2bb034d9-d1df-4cc8-a6a8-b6ad7289f582
title: Classe CIM_VideoHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHead
- CIM_VideoHead.CurrentBitsPerPixel
- CIM_VideoHead.CurrentHorizontalResolution
- CIM_VideoHead.CurrentVerticalResolution
- CIM_VideoHead.MaxRefreshRate
- CIM_VideoHead.MinRefreshRate
- CIM_VideoHead.CurrentRefreshRate
- CIM_VideoHead.CurrentScanMode
- CIM_VideoHead.OtherCurrentScanMode
- CIM_VideoHead.CurrentNumberOfRows
- CIM_VideoHead.CurrentNumberOfColumns
- CIM_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22f8176c9bdbeae460dfa22ca395e7ed8dd8351e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524154"
---
# <a name="cim_videohead-class"></a><span data-ttu-id="8b672-103">\_Classe CIM VideoHead</span><span class="sxs-lookup"><span data-stu-id="8b672-103">CIM\_VideoHead class</span></span>

<span data-ttu-id="8b672-104">Représente un en-tête d’un objet [**CIM \_ DisplayController**](cim-displaycontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="8b672-104">Represents one head of a [**CIM\_DisplayController**](cim-displaycontroller.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b672-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b672-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHead : CIM_LogicalDevice
{
  uint32 CurrentBitsPerPixel;
  uint32 CurrentHorizontalResolution;
  uint32 CurrentVerticalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 CurrentRefreshRate;
  uint16 CurrentScanMode;
  string OtherCurrentScanMode;
  uint32 CurrentNumberOfRows;
  uint32 CurrentNumberOfColumns;
  uint64 CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="8b672-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8b672-106">Members</span></span>

<span data-ttu-id="8b672-107">La classe **CIM \_ VideoHead** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8b672-107">The **CIM\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="8b672-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b672-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b672-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b672-109">Properties</span></span>

<span data-ttu-id="8b672-110">La classe **CIM \_ VideoHead** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8b672-110">The **CIM\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b672-111">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="8b672-111">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-112">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b672-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-114">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 004,12 "), **punitif** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="8b672-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.12"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-115">Nombre de bits utilisés pour afficher chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="8b672-115">The number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="8b672-116">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="8b672-116">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-117">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b672-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-119">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,11 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. HorizontalResolution "), **punitif** (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="8b672-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.11"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.HorizontalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-120">Nombre actuel de pixels horizontaux.</span><span class="sxs-lookup"><span data-stu-id="8b672-120">The current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8b672-121">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="8b672-121">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-122">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b672-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-124">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VideoHeadResolution. NumberOfColors")</span><span class="sxs-lookup"><span data-stu-id="8b672-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.NumberOfColors")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-125">Nombre de couleurs prises en charge à la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="8b672-125">The number of colors supported at the current resolution.</span></span>

</dd> <dt>

<span data-ttu-id="8b672-126">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="8b672-126">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-127">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b672-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 004,14 ")</span><span class="sxs-lookup"><span data-stu-id="8b672-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.14")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-130">En mode caractère, le nombre de colonnes pour le contrôleur d’affichage ; Sinon, « 0 ».</span><span class="sxs-lookup"><span data-stu-id="8b672-130">If in character mode, the number of columns for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="8b672-131">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="8b672-131">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-132">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b672-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-134">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 004,13 ")</span><span class="sxs-lookup"><span data-stu-id="8b672-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.13")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-135">En mode caractère, le nombre de lignes du contrôleur d’affichage ; Sinon, « 0 ».</span><span class="sxs-lookup"><span data-stu-id="8b672-135">If in character mode, the number of rows for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="8b672-136">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="8b672-136">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b672-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-139">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,15 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. RefreshRate "), **punitif** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="8b672-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.15"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.RefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-140">Taux d’actualisation actuel du contrôleur d’affichage, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="8b672-140">The current refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="8b672-141">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="8b672-141">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-142">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b672-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-144">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 004,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoHead**.**OtherCurrentScanMode**, CIM \_ VideoHeadResolution. ScanMode ")</span><span class="sxs-lookup"><span data-stu-id="8b672-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**OtherCurrentScanMode**, CIM\_VideoHeadResolution.ScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-145">Mode d’analyse actuel du contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8b672-145">The current scan mode of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8b672-146">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8b672-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8b672-147">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8b672-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8b672-148">**Non pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="8b672-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="8b672-149">**Opération non entrelacée** (3)</span><span class="sxs-lookup"><span data-stu-id="8b672-149">**Non-Interlaced Operation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="8b672-150">**Opération entrelacée** (4)</span><span class="sxs-lookup"><span data-stu-id="8b672-150">**Interlaced Operation** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8b672-151">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="8b672-151">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b672-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-154">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,10 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. VerticalResolution "), **punitif** (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="8b672-154">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.10"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.VerticalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-155">Nombre actuel de pixels verticaux.</span><span class="sxs-lookup"><span data-stu-id="8b672-155">The current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8b672-156">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="8b672-156">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b672-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-159">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MaxRefreshRate "), **punitif** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="8b672-159">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MaxRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-160">Taux de rafraîchissement maximal du contrôleur d’affichage, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="8b672-160">The maximum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="8b672-161">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="8b672-161">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b672-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-164">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MinRefreshRate "), **punitif** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="8b672-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MinRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-165">Taux d’actualisation minimal du contrôleur d’affichage, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="8b672-165">The minimum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="8b672-166">**OtherCurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="8b672-166">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b672-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b672-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b672-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b672-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b672-169">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoHead**.**CurrentScanMode**, CIM \_ VideoHeadResolution. OtherScanMode ")</span><span class="sxs-lookup"><span data-stu-id="8b672-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**CurrentScanMode**, CIM\_VideoHeadResolution.OtherScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="8b672-170">Description du mode d’analyse en cours lorsque la propriété **CurrentScanMode** est « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="8b672-170">A description of current scan mode when the **CurrentScanMode** property is "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b672-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b672-171">Requirements</span></span>



| <span data-ttu-id="8b672-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b672-172">Requirement</span></span> | <span data-ttu-id="8b672-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b672-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b672-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b672-174">Minimum supported client</span></span><br/> | <span data-ttu-id="8b672-175">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8b672-175">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8b672-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b672-176">Minimum supported server</span></span><br/> | <span data-ttu-id="8b672-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b672-177">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8b672-178">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8b672-178">Namespace</span></span><br/>                | <span data-ttu-id="8b672-179">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b672-179">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8b672-180">MOF</span><span class="sxs-lookup"><span data-stu-id="8b672-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b672-181"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b672-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b672-182">DLL</span><span class="sxs-lookup"><span data-stu-id="8b672-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b672-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b672-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b672-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b672-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b672-185">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8b672-185">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

