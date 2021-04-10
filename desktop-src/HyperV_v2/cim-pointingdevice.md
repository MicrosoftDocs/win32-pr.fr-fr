---
description: Représente un appareil utilisé pour pointer vers les zones d’un affichage.
ms.assetid: ffc675c3-29bd-4c54-8e54-8b6212daf66d
title: Classe CIM_PointingDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.Resolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57cca8c81a2d363e9e31bfc958a75b71e1b910d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115986"
---
# <a name="cim_pointingdevice-class-hyper-v-management"></a><span data-ttu-id="e3ca4-103">Classe CIM_PointingDevice (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-103">CIM_PointingDevice class (Hyper-V management)</span></span>

<span data-ttu-id="e3ca4-104">Représente un appareil utilisé pour pointer vers les zones d’un affichage.</span><span class="sxs-lookup"><span data-stu-id="e3ca4-104">Represents a device used to point to regions of a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ca4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3ca4-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16 PointingType;
  uint8  NumberOfButtons;
  uint16 Handedness;
  uint32 Resolution;
};
```

## <a name="members"></a><span data-ttu-id="e3ca4-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e3ca4-106">Members</span></span>

<span data-ttu-id="e3ca4-107">La classe **CIM \_ PointingDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e3ca4-107">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="e3ca4-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e3ca4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3ca4-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e3ca4-109">Properties</span></span>

<span data-ttu-id="e3ca4-110">La classe **CIM \_ PointingDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e3ca4-110">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3ca4-111">**Ergonomie**</span><span class="sxs-lookup"><span data-stu-id="e3ca4-111">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3ca4-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3ca4-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3ca4-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e3ca4-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3ca4-114">Indique si le dispositif de pointage est configuré pour l’opération de la main droite ou gauche.</span><span class="sxs-lookup"><span data-stu-id="e3ca4-114">Indicates whether the pointing device is configured for right or left handed operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e3ca4-115">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-115">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e3ca4-116">**Non applicable** (1)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-116">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="e3ca4-117">**Bon fonctionnement** de la main (2)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-117">**Right Handed Operation** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="e3ca4-118">**Opération gauche** de la main (3)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-118">**Left Handed Operation** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3ca4-119">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="e3ca4-119">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3ca4-120">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="e3ca4-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e3ca4-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e3ca4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3ca4-122">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de pointage DMTF \| 003,4 ")</span><span class="sxs-lookup"><span data-stu-id="e3ca4-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.4")</span></span>
</dt> </dl>

<span data-ttu-id="e3ca4-123">Nombre de boutons sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e3ca4-123">The number of buttons on the device.</span></span> <span data-ttu-id="e3ca4-124">Si le périphérique de pointage n’a aucun bouton, cette valeur doit être définie sur « 0 ».</span><span class="sxs-lookup"><span data-stu-id="e3ca4-124">If the pointing device has no buttons, this value should be set to "0".</span></span>

</dd> <dt>

<span data-ttu-id="e3ca4-125">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="e3ca4-125">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3ca4-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3ca4-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3ca4-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e3ca4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3ca4-128">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de pointage DMTF \| 003,1 ")</span><span class="sxs-lookup"><span data-stu-id="e3ca4-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.1")</span></span>
</dt> </dl>

<span data-ttu-id="e3ca4-129">Type du dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="e3ca4-129">The type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e3ca4-130">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e3ca4-131">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-131">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="e3ca4-132">**Souris** (3)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-132">**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="e3ca4-133">**Suivre la balle** (4)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-133">**Track Ball** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="e3ca4-134">**Point de suivi** (5)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-134">**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="e3ca4-135">**Point coulissant** (6)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-135">**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="e3ca4-136">**Pavé tactile** (7)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-136">**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="e3ca4-137">**Écran tactile** (8)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-137">**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="e3ca4-138">**Capteur de souris optique** (9)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-138">**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3ca4-139">**Résolution :**</span><span class="sxs-lookup"><span data-stu-id="e3ca4-139">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3ca4-140">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3ca4-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e3ca4-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e3ca4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3ca4-142">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« nombres par pouce »), **punitif** (« nombre/pouce »)</span><span class="sxs-lookup"><span data-stu-id="e3ca4-142">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Counts per Inch"), **PUnit** ("count / inch")</span></span>
</dt> </dl>

<span data-ttu-id="e3ca4-143">Résolution de suivi du dispositif de pointage, en nombre par pouce.</span><span class="sxs-lookup"><span data-stu-id="e3ca4-143">The tracking resolution of the pointing device, in counts per inch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3ca4-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3ca4-144">Requirements</span></span>



| <span data-ttu-id="e3ca4-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3ca4-145">Requirement</span></span> | <span data-ttu-id="e3ca4-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3ca4-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ca4-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3ca4-147">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ca4-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e3ca4-148">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e3ca4-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3ca4-149">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ca4-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3ca4-150">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e3ca4-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e3ca4-151">Namespace</span></span><br/>                | <span data-ttu-id="e3ca4-152">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e3ca4-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e3ca4-153">MOF</span><span class="sxs-lookup"><span data-stu-id="e3ca4-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3ca4-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3ca4-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3ca4-155">DLL</span><span class="sxs-lookup"><span data-stu-id="e3ca4-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3ca4-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e3ca4-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e3ca4-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3ca4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ca4-158">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e3ca4-158">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

