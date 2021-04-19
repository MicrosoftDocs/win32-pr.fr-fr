---
description: La \_ classe CIM VideoBIOSFeature représente les fonctionnalités du logiciel de bas niveau utilisé pour configurer et accéder au contrôleur vidéo et à l’affichage d’un système informatique.
ms.assetid: a12ca387-5b12-487f-84fd-381afe266338
ms.tgt_platform: multiple
title: Classe CIM_VideoBIOSFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeature
- CIM_VideoBIOSFeature.Caption
- CIM_VideoBIOSFeature.CharacteristicDescriptions
- CIM_VideoBIOSFeature.Characteristics
- CIM_VideoBIOSFeature.Description
- CIM_VideoBIOSFeature.IdentifyingNumber
- CIM_VideoBIOSFeature.InstallDate
- CIM_VideoBIOSFeature.Name
- CIM_VideoBIOSFeature.ProductName
- CIM_VideoBIOSFeature.Status
- CIM_VideoBIOSFeature.Vendor
- CIM_VideoBIOSFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45f9fd2feabdcd1f9e650e7e7a913a394e8ef67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514343"
---
# <a name="cim_videobiosfeature-class"></a><span data-ttu-id="870ec-103">\_Classe CIM VideoBIOSFeature</span><span class="sxs-lookup"><span data-stu-id="870ec-103">CIM\_VideoBIOSFeature class</span></span>

<span data-ttu-id="870ec-104">La classe **CIM \_ VideoBIOSFeature** représente les fonctionnalités du logiciel de bas niveau utilisé pour configurer et accéder au contrôleur vidéo et à l’affichage d’un système informatique.</span><span class="sxs-lookup"><span data-stu-id="870ec-104">The **CIM\_VideoBIOSFeature** class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="870ec-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="870ec-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="870ec-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="870ec-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="870ec-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="870ec-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="870ec-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="870ec-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="870ec-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="870ec-109">Syntax</span></span>

``` syntax
[UUID("{BAE20634-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="870ec-110">Membres</span><span class="sxs-lookup"><span data-stu-id="870ec-110">Members</span></span>

<span data-ttu-id="870ec-111">La classe **CIM \_ VideoBIOSFeature** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="870ec-111">The **CIM\_VideoBIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="870ec-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="870ec-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="870ec-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="870ec-113">Properties</span></span>

<span data-ttu-id="870ec-114">La classe **CIM \_ VideoBIOSFeature** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="870ec-114">The **CIM\_VideoBIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="870ec-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="870ec-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="870ec-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="870ec-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="870ec-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="870ec-119">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="870ec-119">Short textual description of the object.</span></span>

<span data-ttu-id="870ec-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="870ec-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="870ec-121">**CharacteristicDescriptions**</span><span class="sxs-lookup"><span data-stu-id="870ec-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-122">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="870ec-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="870ec-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-124">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video BIOS caractéristique \| 001,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**.**Caractéristiques**»)</span><span class="sxs-lookup"><span data-stu-id="870ec-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="870ec-125">Chaînes de forme libre qui fournissent des descriptions détaillées des fonctionnalités vidéo du BIOS indiquées dans le tableau **caractéristiques** .</span><span class="sxs-lookup"><span data-stu-id="870ec-125">Free-form strings that provide detailed descriptions for the video BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="870ec-126">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de **caractéristiques** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="870ec-126">Each entry of this array is related to the entry in the **Characteristics** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="870ec-127">**Caractéristiques**</span><span class="sxs-lookup"><span data-stu-id="870ec-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-128">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="870ec-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="870ec-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-130">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video BIOS caractéristique \| 001,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**.**CharacteristicDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="870ec-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="870ec-131">Fonctionnalités prises en charge par le BIOS vidéo.</span><span class="sxs-lookup"><span data-stu-id="870ec-131">Features supported by the video BIOS.</span></span> <span data-ttu-id="870ec-132">Par exemple, la prise en charge de la gestion de l’alimentation VESA ou de l’occultation du BIOS vidéo peut être indiquée.</span><span class="sxs-lookup"><span data-stu-id="870ec-132">For example, support for VESA power management or video BIOS shadowing could be indicated.</span></span> <span data-ttu-id="870ec-133">La valeur 3 (« Unknown ») n’est pas valide dans le schéma CIM, car elle indique qu’aucune fonctionnalité BIOS n’est prise en charge dans DMI.</span><span class="sxs-lookup"><span data-stu-id="870ec-133">The value 3 ("Unknown") is not valid in the CIM schema since it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="870ec-134">Dans ce cas, l’objet ne doit pas être instancié.</span><span class="sxs-lookup"><span data-stu-id="870ec-134">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="870ec-135">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="870ec-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="870ec-136">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="870ec-136">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="870ec-137">**Non défini** (3)</span><span class="sxs-lookup"><span data-stu-id="870ec-137">**Undefined** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Video_BIOS"></span><span id="standard_video_bios"></span><span id="STANDARD_VIDEO_BIOS"></span>

<span data-ttu-id="870ec-138">**BIOS vidéo standard** (4)</span><span class="sxs-lookup"><span data-stu-id="870ec-138">**Standard Video BIOS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_BIOS_Extensions_Supported"></span><span id="vesa_bios_extensions_supported"></span><span id="VESA_BIOS_EXTENSIONS_SUPPORTED"></span>

<span data-ttu-id="870ec-139">**Extensions BIOS VESA prises en charge** (5)</span><span class="sxs-lookup"><span data-stu-id="870ec-139">**VESA BIOS Extensions Supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Power_Management_Supported"></span><span id="vesa_power_management_supported"></span><span id="VESA_POWER_MANAGEMENT_SUPPORTED"></span>

<span data-ttu-id="870ec-140">**Gestion de l’alimentation VESA prise en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="870ec-140">**VESA Power Management Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Display_Data_Channel_Supported"></span><span id="vesa_display_data_channel_supported"></span><span id="VESA_DISPLAY_DATA_CHANNEL_SUPPORTED"></span>

<span data-ttu-id="870ec-141">**Canal de données d’affichage VESA pris en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="870ec-141">**VESA Display Data Channel Supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Shadowing_Allowed"></span><span id="video_bios_shadowing_allowed"></span><span id="VIDEO_BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="870ec-142">**Masquage vidéo du BIOS autorisé** (8)</span><span class="sxs-lookup"><span data-stu-id="870ec-142">**Video BIOS Shadowing Allowed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Upgradeable"></span><span id="video_bios_upgradeable"></span><span id="VIDEO_BIOS_UPGRADEABLE"></span>

<span data-ttu-id="870ec-143">Mise à **niveau du BIOS vidéo** (9)</span><span class="sxs-lookup"><span data-stu-id="870ec-143">**Video BIOS Upgradeable** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="870ec-144">**Description**</span><span class="sxs-lookup"><span data-stu-id="870ec-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="870ec-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="870ec-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-147">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="870ec-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="870ec-148">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="870ec-148">Textual description of the object.</span></span>

<span data-ttu-id="870ec-149">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="870ec-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="870ec-150">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="870ec-150">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="870ec-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="870ec-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-153">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="870ec-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="870ec-154">Identification du produit, telle qu’un numéro de série sur un logiciel ou un numéro gravé sur une puce matérielle.</span><span class="sxs-lookup"><span data-stu-id="870ec-154">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span> <span data-ttu-id="870ec-155">Cette propriété est héritée de la [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="870ec-155">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="870ec-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="870ec-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-157">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="870ec-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="870ec-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-159">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="870ec-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="870ec-160">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="870ec-160">Date and time the object was installed.</span></span> <span data-ttu-id="870ec-161">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="870ec-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="870ec-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="870ec-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="870ec-163">**Nom**</span><span class="sxs-lookup"><span data-stu-id="870ec-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="870ec-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="870ec-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-166">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="870ec-166">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="870ec-167">Étiquette par laquelle l’objet est connu en dehors du système de traitement des données.</span><span class="sxs-lookup"><span data-stu-id="870ec-167">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="870ec-168">Cette étiquette est un nom qui identifie de façon unique l’élément dans le contexte de l’espace de noms de l’élément.</span><span class="sxs-lookup"><span data-stu-id="870ec-168">This label is a name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="870ec-169">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="870ec-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="870ec-170">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="870ec-170">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="870ec-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="870ec-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-173">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="870ec-173">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="870ec-174">Nom de produit couramment utilisé.</span><span class="sxs-lookup"><span data-stu-id="870ec-174">Commonly used product name.</span></span>

<span data-ttu-id="870ec-175">Cette propriété est héritée de la [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="870ec-175">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="870ec-176">**État**</span><span class="sxs-lookup"><span data-stu-id="870ec-176">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="870ec-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="870ec-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-179">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="870ec-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="870ec-180">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="870ec-180">Current status of the object.</span></span> <span data-ttu-id="870ec-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="870ec-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="870ec-182">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="870ec-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="870ec-183">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="870ec-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="870ec-184">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="870ec-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="870ec-185">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="870ec-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="870ec-186">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="870ec-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="870ec-187">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="870ec-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="870ec-188">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="870ec-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="870ec-189">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="870ec-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="870ec-190">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="870ec-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="870ec-191">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="870ec-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="870ec-192">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="870ec-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="870ec-193">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="870ec-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="870ec-194">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="870ec-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="870ec-195">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="870ec-195">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="870ec-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="870ec-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-198">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**Vendor**»), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« DMTF \| ComponentID \| 001,1 »)</span><span class="sxs-lookup"><span data-stu-id="870ec-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="870ec-199">Nom du fournisseur du produit, qui correspond à la propriété **Vendor** dans l’objet Product de la solution DMTF Exchange standard (y).</span><span class="sxs-lookup"><span data-stu-id="870ec-199">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard (SES).</span></span>

<span data-ttu-id="870ec-200">Cette propriété est héritée de la [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="870ec-200">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="870ec-201">**Version**</span><span class="sxs-lookup"><span data-stu-id="870ec-201">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="870ec-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="870ec-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="870ec-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="870ec-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="870ec-204">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**Version**"), [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="870ec-204">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="870ec-205">Les informations de version du produit, qui correspondent à la propriété **version** dans l’objet Product de la sa DMTF.</span><span class="sxs-lookup"><span data-stu-id="870ec-205">Product version information, which corresponds to the **Version** property in the product object of the DMTF SES.</span></span>

<span data-ttu-id="870ec-206">Cette propriété est héritée de la [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="870ec-206">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="870ec-207">Notes</span><span class="sxs-lookup"><span data-stu-id="870ec-207">Remarks</span></span>

<span data-ttu-id="870ec-208">La classe **CIM \_ VideoBIOSFeature** est dérivée de [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="870ec-208">The **CIM\_VideoBIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="870ec-209">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="870ec-209">WMI does not implement this class.</span></span>

<span data-ttu-id="870ec-210">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="870ec-210">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="870ec-211">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="870ec-211">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="870ec-212">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="870ec-212">Requirements</span></span>



| <span data-ttu-id="870ec-213">Condition requise</span><span class="sxs-lookup"><span data-stu-id="870ec-213">Requirement</span></span> | <span data-ttu-id="870ec-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="870ec-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="870ec-215">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="870ec-215">Minimum supported client</span></span><br/> | <span data-ttu-id="870ec-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="870ec-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="870ec-217">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="870ec-217">Minimum supported server</span></span><br/> | <span data-ttu-id="870ec-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="870ec-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="870ec-219">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="870ec-219">Namespace</span></span><br/>                | <span data-ttu-id="870ec-220">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="870ec-220">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="870ec-221">MOF</span><span class="sxs-lookup"><span data-stu-id="870ec-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="870ec-222"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="870ec-222"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="870ec-223">DLL</span><span class="sxs-lookup"><span data-stu-id="870ec-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="870ec-224"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="870ec-224"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="870ec-225">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="870ec-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="870ec-226">**\_SOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="870ec-226">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

