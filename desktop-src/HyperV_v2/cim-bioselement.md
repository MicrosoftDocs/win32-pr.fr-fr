---
description: Représente le logiciel de bas niveau qui est chargé dans un stockage non volatile et utilisé pour démarrer et configurer un système informatique (CIM CIM \_ ).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: Classe CIM_BIOSElement (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522832"
---
# <a name="cim_bioselement-class-hyper-v-management"></a><span data-ttu-id="ccc57-103">Classe CIM_BIOSElement (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ccc57-103">CIM_BIOSElement class (Hyper-V management)</span></span>

<span data-ttu-id="ccc57-104">Représente le logiciel de bas niveau qui est chargé dans un stockage non volatile et utilisé pour démarrer et configurer un système informatique ([**CIM CIM \_**](cim-computersystem.md)).</span><span class="sxs-lookup"><span data-stu-id="ccc57-104">Represents the low-level software that is loaded into non-volatile storage and used to start up and configure a computer system ([**CIM\_ComputerSystem**](cim-computersystem.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc57-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccc57-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a><span data-ttu-id="ccc57-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ccc57-106">Members</span></span>

<span data-ttu-id="ccc57-107">La classe **CIM \_ BIOSElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ccc57-107">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ccc57-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ccc57-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ccc57-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ccc57-109">Properties</span></span>

<span data-ttu-id="ccc57-110">La classe **CIM \_ BIOSElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ccc57-110">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ccc57-111">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="ccc57-111">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc57-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccc57-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccc57-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-114">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSElement**.**ListOfLanguages**")</span><span class="sxs-lookup"><span data-stu-id="ccc57-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSElement**.**ListOfLanguages**")</span></span>
</dt> </dl>

<span data-ttu-id="ccc57-115">Langue actuellement sélectionnée pour le BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccc57-115">The currently selected language for the BIOS.</span></span> <span data-ttu-id="ccc57-116">Ces informations peuvent être obtenues à partir de System Management BIOS (SMBIOS) à l’aide de l’attribut de langage actuel de la structure de type 13 à indexer dans la liste de chaînes qui suit la structure.</span><span class="sxs-lookup"><span data-stu-id="ccc57-116">This information can be obtained from the System Management BIOS (SMBIOS) using the Current Language attribute of the Type 13 structure to index into the string list that follows the structure.</span></span> <span data-ttu-id="ccc57-117">Cette propriété est mise en forme à l’aide du nom de langue ISO 639 et peut être suivie par le nom du secteur ISO 3166 et la méthode d’encodage.</span><span class="sxs-lookup"><span data-stu-id="ccc57-117">This property is formatted using the ISO 639 Language Name, and may be followed by the ISO 3166 Territory Name and the encoding method.</span></span>

</dd> <dt>

<span data-ttu-id="ccc57-118">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="ccc57-118">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc57-119">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ccc57-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccc57-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccc57-121">Liste des langues installables pour le BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccc57-121">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="ccc57-122">Ces informations peuvent être obtenues à partir de SMBIOS, à partir de la liste de chaînes qui suit la structure type 13.</span><span class="sxs-lookup"><span data-stu-id="ccc57-122">This information can be obtained from SMBIOS, from the string list that follows the Type 13 structure.</span></span> <span data-ttu-id="ccc57-123">Un nom de langue ISO 639 doit être utilisé pour spécifier les langues installables du BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccc57-123">An ISO 639 Language Name should be used to specify the BIOS' installable languages.</span></span> <span data-ttu-id="ccc57-124">Le nom du secteur ISO 3166 et la méthode d’encodage peuvent également être spécifiés, en suivant le nom de la langue.</span><span class="sxs-lookup"><span data-stu-id="ccc57-124">The ISO 3166 Territory Name and the encoding method may also be specified, following the Language Name.</span></span>

</dd> <dt>

<span data-ttu-id="ccc57-125">**LoadedEndingAddress**</span><span class="sxs-lookup"><span data-stu-id="ccc57-125">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc57-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ccc57-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccc57-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-128">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,6»)</span><span class="sxs-lookup"><span data-stu-id="ccc57-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="ccc57-129">Adresse de fin de la mémoire occupée par le BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccc57-129">The ending address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="ccc57-130">**LoadedStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="ccc57-130">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc57-131">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ccc57-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccc57-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-133">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,5»)</span><span class="sxs-lookup"><span data-stu-id="ccc57-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ccc57-134">Adresse de début de la mémoire occupée par le BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccc57-134">The starting address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="ccc57-135">**LoadUtilityInformation**</span><span class="sxs-lookup"><span data-stu-id="ccc57-135">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc57-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccc57-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccc57-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-138">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,7»)</span><span class="sxs-lookup"><span data-stu-id="ccc57-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="ccc57-139">Chaîne de forme libre qui décrit l’utilitaire Flash/chargement BIOS requis pour mettre à jour l’objet **CIM \_ BIOSElement** .</span><span class="sxs-lookup"><span data-stu-id="ccc57-139">A free form string that describes the BIOS flash/load utility that is required to update the **CIM\_BIOSElement** object.</span></span> <span data-ttu-id="ccc57-140">La version et d’autres informations peuvent être indiquées dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ccc57-140">Version and other information may be indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="ccc57-141">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="ccc57-141">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc57-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccc57-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccc57-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-144">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="ccc57-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="ccc57-145">Fabricant de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="ccc57-145">The manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="ccc57-146">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="ccc57-146">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc57-147">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ccc57-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccc57-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-149">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,9»)</span><span class="sxs-lookup"><span data-stu-id="ccc57-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="ccc57-150">True s’il s’agit du BIOS principal du système informatique ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="ccc57-150">True if this is the primary BIOS of the computer system; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="ccc57-151">**RegistryURIs**</span><span class="sxs-lookup"><span data-stu-id="ccc57-151">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc57-152">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ccc57-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccc57-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccc57-154">Emplacement de publication des registres des attributs BIOS auxquels l’implémentation du BIOS est conforme.</span><span class="sxs-lookup"><span data-stu-id="ccc57-154">The publication location of the BIOS attribute registries to which the BIOS implementation complies.</span></span>

</dd> <dt>

<span data-ttu-id="ccc57-155">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="ccc57-155">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc57-156">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ccc57-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccc57-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-158">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,8»)</span><span class="sxs-lookup"><span data-stu-id="ccc57-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="ccc57-159">Date à laquelle ce BIOS a été publié.</span><span class="sxs-lookup"><span data-stu-id="ccc57-159">The Date on which this BIOS was released.</span></span>

</dd> <dt>

<span data-ttu-id="ccc57-160">**Version**</span><span class="sxs-lookup"><span data-stu-id="ccc57-160">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc57-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccc57-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccc57-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc57-163">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,3»)</span><span class="sxs-lookup"><span data-stu-id="ccc57-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="ccc57-164">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ccc57-164">The version of the operation.</span></span> <span data-ttu-id="ccc57-165">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ccc57-165">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="ccc57-166">*<major>*.*<minor>*.*<revision>*</span><span class="sxs-lookup"><span data-stu-id="ccc57-166">*<major>*.*<minor>*.*<revision>*</span></span>
-   <span data-ttu-id="ccc57-167">*<major>*.*<minor><letter><revision>*</span><span class="sxs-lookup"><span data-stu-id="ccc57-167">*<major>*.*<minor><letter><revision>*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccc57-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccc57-168">Requirements</span></span>



| <span data-ttu-id="ccc57-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccc57-169">Requirement</span></span> | <span data-ttu-id="ccc57-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccc57-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc57-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccc57-171">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc57-172">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ccc57-172">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ccc57-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccc57-173">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc57-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ccc57-174">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ccc57-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ccc57-175">Namespace</span></span><br/>                | <span data-ttu-id="ccc57-176">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ccc57-176">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ccc57-177">MOF</span><span class="sxs-lookup"><span data-stu-id="ccc57-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccc57-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ccc57-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ccc57-179">DLL</span><span class="sxs-lookup"><span data-stu-id="ccc57-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccc57-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ccc57-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ccc57-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccc57-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc57-182">**\_SOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ccc57-182">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

