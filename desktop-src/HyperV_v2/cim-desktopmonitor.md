---
description: Représente un moniteur CRT Desktop.
ms.assetid: 26a06320-9fd9-434e-87c8-486e9ca4945c
title: Classe CIM_DesktopMonitor (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab152fc10f3fd404744c293d2368039ffcfdb291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544711"
---
# <a name="cim_desktopmonitor-class-hyper-v-management"></a><span data-ttu-id="50f19-103">Classe CIM_DesktopMonitor (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="50f19-103">CIM_DesktopMonitor class (Hyper-V management)</span></span>

<span data-ttu-id="50f19-104">Représente un moniteur CRT Desktop.</span><span class="sxs-lookup"><span data-stu-id="50f19-104">Represents a CRT desktop monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f19-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50f19-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices")]
class CIM_DesktopMonitor : CIM_Display
{
  uint16 DisplayType;
  uint32 Bandwidth;
  uint32 ScreenHeight;
  uint32 ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="50f19-106">Membres</span><span class="sxs-lookup"><span data-stu-id="50f19-106">Members</span></span>

<span data-ttu-id="50f19-107">La classe **CIM \_ desktopmonitor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="50f19-107">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="50f19-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="50f19-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50f19-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="50f19-109">Properties</span></span>

<span data-ttu-id="50f19-110">La classe **CIM \_ desktopmonitor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="50f19-110">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50f19-111">**Bande passante**</span><span class="sxs-lookup"><span data-stu-id="50f19-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50f19-112">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50f19-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50f19-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="50f19-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50f19-114">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« mégahertz »), **punitif** (« Hertz \* 10 ^ 6 »)</span><span class="sxs-lookup"><span data-stu-id="50f19-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="50f19-115">Bande passante de l’affichage, en MHertz.</span><span class="sxs-lookup"><span data-stu-id="50f19-115">The bandwidth of the display, in MHertz.</span></span> <span data-ttu-id="50f19-116">« 0 » indique inconnu.</span><span class="sxs-lookup"><span data-stu-id="50f19-116">"0" indicates unknown.</span></span>

</dd> <dt>

<span data-ttu-id="50f19-117">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="50f19-117">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50f19-118">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="50f19-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="50f19-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="50f19-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50f19-120">Type d’affichage du moniteur CRT.</span><span class="sxs-lookup"><span data-stu-id="50f19-120">The type of display type of the CRT monitor.</span></span> <span data-ttu-id="50f19-121">Par exemple, MultiScan Color ou monochrome.</span><span class="sxs-lookup"><span data-stu-id="50f19-121">For example, multiscan color, or monochrome.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="50f19-122">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="50f19-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="50f19-123">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="50f19-123">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="50f19-124">**Couleur multibalayage** (2)</span><span class="sxs-lookup"><span data-stu-id="50f19-124">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="50f19-125">**Multiscann monochrome** (3)</span><span class="sxs-lookup"><span data-stu-id="50f19-125">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="50f19-126">**Couleur de fréquence fixe** (4)</span><span class="sxs-lookup"><span data-stu-id="50f19-126">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="50f19-127">**Fréquence fixe monochrome** (5)</span><span class="sxs-lookup"><span data-stu-id="50f19-127">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50f19-128">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="50f19-128">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50f19-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50f19-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50f19-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="50f19-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50f19-131">Hauteur logique de l’affichage, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="50f19-131">The logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="50f19-132">**Largeur**</span><span class="sxs-lookup"><span data-stu-id="50f19-132">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50f19-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50f19-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50f19-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="50f19-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50f19-135">Largeur logique de l’affichage, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="50f19-135">The logical width of the display, in screen coordinates.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50f19-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50f19-136">Requirements</span></span>



| <span data-ttu-id="50f19-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50f19-137">Requirement</span></span> | <span data-ttu-id="50f19-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="50f19-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f19-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50f19-139">Minimum supported client</span></span><br/> | <span data-ttu-id="50f19-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="50f19-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="50f19-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50f19-141">Minimum supported server</span></span><br/> | <span data-ttu-id="50f19-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="50f19-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="50f19-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="50f19-143">Namespace</span></span><br/>                | <span data-ttu-id="50f19-144">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="50f19-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="50f19-145">MOF</span><span class="sxs-lookup"><span data-stu-id="50f19-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50f19-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50f19-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50f19-147">DLL</span><span class="sxs-lookup"><span data-stu-id="50f19-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50f19-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50f19-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50f19-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50f19-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f19-150">**\_Affichage CIM**</span><span class="sxs-lookup"><span data-stu-id="50f19-150">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

