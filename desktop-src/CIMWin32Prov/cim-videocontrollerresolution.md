---
description: La \_ classe CIM VideoControllerResolution représente les différents modes vidéo qu’un contrôleur vidéo peut prendre en charge.
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: Classe CIM_VideoControllerResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d448d92d79163bc6a4e1056e88434081c5878159
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861682"
---
# <a name="cim_videocontrollerresolution-class"></a><span data-ttu-id="89159-103">\_Classe CIM VideoControllerResolution</span><span class="sxs-lookup"><span data-stu-id="89159-103">CIM\_VideoControllerResolution class</span></span>

<span data-ttu-id="89159-104">La classe **CIM \_ VideoControllerResolution** représente les différents modes vidéo qu’un contrôleur vidéo peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="89159-104">The **CIM\_VideoControllerResolution** class represents the various video modes that a video controller can support.</span></span> <span data-ttu-id="89159-105">Les modes vidéo sont définis par les résolutions horizontales et verticales possibles, la fréquence d’actualisation, le mode d’analyse et le nombre de paramètres de couleur pris en charge par un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="89159-105">Video modes are defined by the possible horizontal and vertical resolutions, refresh rate, scan mode, and number of color settings supported by a controller.</span></span> <span data-ttu-id="89159-106">Les résolutions réelles utilisées sont les valeurs spécifiées dans l’objet [**CIM \_ VideoController**](cim-videocontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="89159-106">The actual resolutions in use are the values specified in the [**CIM\_VideoController**](cim-videocontroller.md) object.</span></span>

<span data-ttu-id="89159-107">Le matériel qui n’est pas compatible avec le modèle WDDM (Windows Display Driver Model) retourne des valeurs de propriété inexactes pour les instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="89159-107">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89159-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="89159-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89159-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="89159-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89159-110">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="89159-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="89159-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="89159-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89159-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89159-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="89159-113">Membres</span><span class="sxs-lookup"><span data-stu-id="89159-113">Members</span></span>

<span data-ttu-id="89159-114">La classe **CIM \_ VideoControllerResolution** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="89159-114">The **CIM\_VideoControllerResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="89159-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89159-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89159-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89159-116">Properties</span></span>

<span data-ttu-id="89159-117">La classe **CIM \_ VideoControllerResolution** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="89159-117">The **CIM\_VideoControllerResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89159-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="89159-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89159-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89159-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89159-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89159-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89159-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="89159-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="89159-122">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="89159-122">Short textual description of the current object.</span></span>

<span data-ttu-id="89159-123">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="89159-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="89159-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="89159-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89159-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89159-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89159-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89159-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89159-127">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="89159-127">Textual description of the current object.</span></span>

<span data-ttu-id="89159-128">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="89159-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="89159-129">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="89159-129">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89159-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89159-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89159-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89159-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89159-132">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Résolutions de l’analyseur DMTF \| 002,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="89159-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="89159-133">Résolution horizontale, en pixels.</span><span class="sxs-lookup"><span data-stu-id="89159-133">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="89159-134">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="89159-134">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89159-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89159-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89159-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89159-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89159-137">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Résolutions de l’analyseur DMTF \| 002,7 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="89159-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="89159-138">Taux maximal d’actualisation quand une plage de taux est prise en charge aux résolutions spécifiées, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="89159-138">Maximum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="89159-139">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="89159-139">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89159-140">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89159-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89159-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89159-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89159-142">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Résolutions de l’analyseur DMTF \| 002,6 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="89159-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="89159-143">Taux d’actualisation minimal quand une plage de taux est prise en charge aux résolutions spécifiées, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="89159-143">Minimum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="89159-144">**NumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="89159-144">**NumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89159-145">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89159-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89159-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89159-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89159-147">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")</span><span class="sxs-lookup"><span data-stu-id="89159-147">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")</span></span>
</dt> </dl>

<span data-ttu-id="89159-148">Nombre de couleurs prises en charge à la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="89159-148">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="89159-149">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="89159-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="89159-150">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="89159-150">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89159-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89159-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89159-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89159-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89159-153">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Résolutions de l’analyseur DMTF \| 002,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="89159-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="89159-154">Fréquence d’actualisation, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="89159-154">Refresh rate, in hertz.</span></span> <span data-ttu-id="89159-155">Si une plage de taux est prise en charge, utilisez les propriétés **MinRefreshRate** et **MaxRefreshRate** et affectez la valeur 0 à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="89159-155">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="89159-156">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="89159-156">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89159-157">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89159-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89159-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89159-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89159-159">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Résolutions de l' \| analyseur DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="89159-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="89159-160">Mode d’analyse du fonctionnement du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="89159-160">Scan mode at which the controller operates.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89159-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="89159-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89159-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="89159-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="89159-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="89159-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="89159-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Opération non entrelacée** (4)</span><span class="sxs-lookup"><span data-stu-id="89159-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (4)</span></span>


</dt> <dd>

<span data-ttu-id="89159-165">Opération qui n’est pas entrelacée</span><span class="sxs-lookup"><span data-stu-id="89159-165">Noninterlaced operation</span></span>

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="89159-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Opération entrelacée** (5)</span><span class="sxs-lookup"><span data-stu-id="89159-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89159-167">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="89159-167">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89159-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89159-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89159-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89159-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89159-170">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("settingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="89159-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="89159-171">ID qui fait partie de la clé de l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="89159-171">An ID that serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="89159-172">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="89159-172">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89159-173">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89159-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89159-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89159-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89159-175">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Résolutions de l’analyseur DMTF \| 002,3 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="89159-175">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="89159-176">Résolution verticale du contrôleur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="89159-176">Controller's vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89159-177">Notes</span><span class="sxs-lookup"><span data-stu-id="89159-177">Remarks</span></span>

<span data-ttu-id="89159-178">WMI implémente la classe **CIM \_ VideoControllerResolution** .</span><span class="sxs-lookup"><span data-stu-id="89159-178">WMI implements the **CIM\_VideoControllerResolution** class.</span></span> <span data-ttu-id="89159-179">La **classe \_ VideoControllerResolution CIM** est une classe dynamique.</span><span class="sxs-lookup"><span data-stu-id="89159-179">The **CIM\_VideoControllerResolution** class is a dynamic class.</span></span>

<span data-ttu-id="89159-180">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="89159-180">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89159-181">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="89159-181">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="89159-182">Notez que cette classe est une classe de base.</span><span class="sxs-lookup"><span data-stu-id="89159-182">Note that this class is a base class.</span></span> <span data-ttu-id="89159-183">Si vous tentez d’accéder à votre contrôleur vidéo via WMI, vous souhaiterez peut-être utiliser [**Win32 \_ VideoController**](win32-videocontroller.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="89159-183">If you are attempting to access your video controller through WMI, you may wish to use [**Win32\_VideoController**](win32-videocontroller.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="89159-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89159-184">Requirements</span></span>



| <span data-ttu-id="89159-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89159-185">Requirement</span></span> | <span data-ttu-id="89159-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="89159-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89159-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89159-187">Minimum supported client</span></span><br/> | <span data-ttu-id="89159-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89159-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89159-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89159-189">Minimum supported server</span></span><br/> | <span data-ttu-id="89159-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89159-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89159-191">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="89159-191">Namespace</span></span><br/>                | <span data-ttu-id="89159-192">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="89159-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89159-193">MOF</span><span class="sxs-lookup"><span data-stu-id="89159-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89159-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89159-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89159-195">DLL</span><span class="sxs-lookup"><span data-stu-id="89159-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89159-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89159-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89159-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89159-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89159-198">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="89159-198">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

