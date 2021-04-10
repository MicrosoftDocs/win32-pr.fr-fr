---
description: La \_ classe CIM MonitorResolution représente la relation entre les résolutions horizontales et verticales, ainsi que la fréquence d’actualisation et le mode d’analyse d’un moniteur d’ordinateur de bureau. Les valeurs sont spécifiées dans l’objet de contrôleur vidéo.
ms.assetid: 064620dd-2d92-42d0-9167-35867830a077
ms.tgt_platform: multiple
title: Classe CIM_MonitorResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorResolution
- CIM_MonitorResolution.Caption
- CIM_MonitorResolution.Description
- CIM_MonitorResolution.SettingID
- CIM_MonitorResolution.HorizontalResolution
- CIM_MonitorResolution.MaxRefreshRate
- CIM_MonitorResolution.MinRefreshRate
- CIM_MonitorResolution.RefreshRate
- CIM_MonitorResolution.ScanMode
- CIM_MonitorResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b359a2e7eccf31b32aced8a2ea9f85fb6dc48b7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950720"
---
# <a name="cim_monitorresolution-class"></a><span data-ttu-id="c7030-104">\_Classe CIM MonitorResolution</span><span class="sxs-lookup"><span data-stu-id="c7030-104">CIM\_MonitorResolution class</span></span>

<span data-ttu-id="c7030-105">La classe **CIM \_ MonitorResolution** représente la relation entre les résolutions horizontales et verticales, ainsi que la fréquence d’actualisation et le mode d’analyse d’un moniteur d’ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="c7030-105">The **CIM\_MonitorResolution** class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="c7030-106">Les valeurs sont spécifiées dans l’objet de contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="c7030-106">Values are specified in the video controller object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7030-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="c7030-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c7030-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c7030-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c7030-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c7030-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c7030-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c7030-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7030-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7030-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEC-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="c7030-112">Membres</span><span class="sxs-lookup"><span data-stu-id="c7030-112">Members</span></span>

<span data-ttu-id="c7030-113">La classe **CIM \_ MonitorResolution** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c7030-113">The **CIM\_MonitorResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="c7030-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c7030-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7030-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c7030-115">Properties</span></span>

<span data-ttu-id="c7030-116">La classe **CIM \_ MonitorResolution** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c7030-116">The **CIM\_MonitorResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7030-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c7030-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7030-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c7030-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7030-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7030-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7030-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c7030-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c7030-121">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="c7030-121">Short textual description of the current object.</span></span>

<span data-ttu-id="c7030-122">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="c7030-122">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7030-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="c7030-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7030-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c7030-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7030-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7030-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7030-126">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="c7030-126">Textual description of the current object.</span></span>

<span data-ttu-id="c7030-127">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="c7030-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7030-128">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="c7030-128">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7030-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7030-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7030-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7030-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7030-131">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Résolutions de l’analyseur DMTF \| 002,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="c7030-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="c7030-132">Résolution horizontale du moniteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="c7030-132">Monitor's horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c7030-133">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="c7030-133">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7030-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7030-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7030-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7030-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7030-136">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Résolutions de l’analyseur DMTF \| 002,7 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="c7030-136">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="c7030-137">Taux de rafraîchissement maximal du moniteur, en Hertz, quand une plage de tarifs est prise en charge au niveau des résolutions spécifiées.</span><span class="sxs-lookup"><span data-stu-id="c7030-137">Monitor's maximum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="c7030-138">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="c7030-138">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7030-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7030-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7030-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7030-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7030-141">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Résolutions de l’analyseur DMTF \| 002,6 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="c7030-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="c7030-142">Taux de rafraîchissement minimal du moniteur, en Hertz, quand une plage de tarifs est prise en charge aux résolutions spécifiées.</span><span class="sxs-lookup"><span data-stu-id="c7030-142">Monitor's minimum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="c7030-143">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="c7030-143">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7030-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7030-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7030-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7030-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7030-146">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Résolutions de l’analyseur DMTF \| 002,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="c7030-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="c7030-147">Fréquence d’actualisation du moniteur, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="c7030-147">Monitor's refresh rate, in hertz.</span></span> <span data-ttu-id="c7030-148">Si une plage de taux est prise en charge, utilisez les propriétés **MinRefreshRate** et **MaxRefreshRate** et affectez la valeur 0 à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c7030-148">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="c7030-149">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="c7030-149">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7030-150">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7030-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7030-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7030-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7030-152">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Résolutions de l' \| analyseur DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="c7030-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="c7030-153">Mode d’analyse utilisé par le moniteur.</span><span class="sxs-lookup"><span data-stu-id="c7030-153">Scan mode that the monitor uses.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7030-154">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c7030-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7030-155">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="c7030-155">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c7030-156">**Non pris en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="c7030-156">**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="c7030-157">**Opération non entrelacée** (4)</span><span class="sxs-lookup"><span data-stu-id="c7030-157">**Non-Interlaced Operation** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="c7030-158">**Opération entrelacée** (5)</span><span class="sxs-lookup"><span data-stu-id="c7030-158">**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7030-159">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="c7030-159">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7030-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c7030-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7030-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7030-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7030-162">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("settingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c7030-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7030-163">Fait partie de la clé de l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="c7030-163">Serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="c7030-164">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="c7030-164">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7030-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7030-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7030-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7030-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7030-167">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Résolutions de l’analyseur DMTF \| 002,3 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="c7030-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="c7030-168">Résolution verticale du moniteur en pixels.</span><span class="sxs-lookup"><span data-stu-id="c7030-168">Monitor's vertical resolution in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7030-169">Notes</span><span class="sxs-lookup"><span data-stu-id="c7030-169">Remarks</span></span>

<span data-ttu-id="c7030-170">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="c7030-170">WMI does not implement this class.</span></span>

<span data-ttu-id="c7030-171">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="c7030-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c7030-172">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="c7030-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7030-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7030-173">Requirements</span></span>



| <span data-ttu-id="c7030-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7030-174">Requirement</span></span> | <span data-ttu-id="c7030-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7030-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7030-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7030-176">Minimum supported client</span></span><br/> | <span data-ttu-id="c7030-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7030-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7030-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7030-178">Minimum supported server</span></span><br/> | <span data-ttu-id="c7030-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7030-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7030-180">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c7030-180">Namespace</span></span><br/>                | <span data-ttu-id="c7030-181">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c7030-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c7030-182">MOF</span><span class="sxs-lookup"><span data-stu-id="c7030-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7030-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7030-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7030-184">DLL</span><span class="sxs-lookup"><span data-stu-id="c7030-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7030-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7030-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7030-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7030-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7030-187">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="c7030-187">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

