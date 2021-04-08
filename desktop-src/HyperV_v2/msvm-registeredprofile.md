---
description: Décrit un ensemble de classes avec les propriétés et les méthodes requises, nécessaires pour gérer une entité réelle ou pour prendre en charge un scénario d’utilisation, de manière interopérable.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Classe Msvm_RegisteredProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7014687355524fbe10ff01869cac6c3fd35a894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034579"
---
# <a name="msvm_registeredprofile-class"></a><span data-ttu-id="f9b34-103">MSVM \_ RegisteredProfile, classe</span><span class="sxs-lookup"><span data-stu-id="f9b34-103">Msvm\_RegisteredProfile class</span></span>

<span data-ttu-id="f9b34-104">Décrit un ensemble de classes avec les propriétés et les méthodes requises, nécessaires pour gérer une entité réelle ou pour prendre en charge un scénario d’utilisation, de manière interopérable.</span><span class="sxs-lookup"><span data-stu-id="f9b34-104">Describes a set of classes with required properties and methods, necessary to manage a real-world entity or to support a usage scenario, in an interoperable fashion.</span></span>

<span data-ttu-id="f9b34-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f9b34-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b34-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9b34-106">Syntax</span></span>

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="f9b34-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f9b34-107">Members</span></span>

<span data-ttu-id="f9b34-108">La classe **MSVM \_ RegisteredProfile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f9b34-108">The **Msvm\_RegisteredProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="f9b34-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f9b34-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9b34-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f9b34-110">Properties</span></span>

<span data-ttu-id="f9b34-111">La classe **MSVM \_ RegisteredProfile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f9b34-111">The **Msvm\_RegisteredProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9b34-112">**AdvertiseTypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f9b34-112">**AdvertiseTypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b34-113">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="f9b34-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9b34-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b34-115">Tableau de chaînes qui fournit des informations supplémentaires relatives à la propriété **AdvertiseType** .</span><span class="sxs-lookup"><span data-stu-id="f9b34-115">An array of strings that provides additional information related to the **AdvertiseType** property.</span></span> <span data-ttu-id="f9b34-116">Une description doit être fournie lorsque le **AdvertiseType** est 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="f9b34-116">A description must be provided when the **AdvertiseType** is 1 (Other).</span></span> <span data-ttu-id="f9b34-117">Une entrée de ce tableau correspond au même index dans le tableau **AdvertiseTypes** .</span><span class="sxs-lookup"><span data-stu-id="f9b34-117">An entry in this array corresponds to the same index in the **AdvertiseTypes** array.</span></span> <span data-ttu-id="f9b34-118">Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f9b34-118">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f9b34-119">**AdvertiseTypes**</span><span class="sxs-lookup"><span data-stu-id="f9b34-119">**AdvertiseTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b34-120">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b34-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9b34-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b34-122">Spécifie la publication pour les informations de profil.</span><span class="sxs-lookup"><span data-stu-id="f9b34-122">Specifies the advertisement for the profile information.</span></span> <span data-ttu-id="f9b34-123">Il est utilisé par les services de publicité de l’infrastructure WBEM pour déterminer ce qui doit être publié, par le biais des mécanismes.</span><span class="sxs-lookup"><span data-stu-id="f9b34-123">It is used by the advertising services of the WBEM infrastructure to determine what should be advertised, through what mechanisms.</span></span> <span data-ttu-id="f9b34-124">La propriété est un tableau afin que le profil puisse être publié à l’aide de plusieurs mécanismes.</span><span class="sxs-lookup"><span data-stu-id="f9b34-124">The property is an array so that the profile can be advertised using several mechanisms.</span></span> <span data-ttu-id="f9b34-125">Si cette propriété est **null**, cela équivaut à spécifier la valeur 2 (non publiée).</span><span class="sxs-lookup"><span data-stu-id="f9b34-125">If this property is **Null**, this is equivalent to specifying the value 2 (Not Advertised).</span></span> <span data-ttu-id="f9b34-126">Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f9b34-126">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="f9b34-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b34-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Non publié** (2)</span><span class="sxs-lookup"><span data-stu-id="f9b34-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Not Advertised** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3)</span><span class="sxs-lookup"><span data-stu-id="f9b34-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b34-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f9b34-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b34-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f9b34-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9b34-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b34-133">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f9b34-133">A short description of the object.</span></span> <span data-ttu-id="f9b34-134">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f9b34-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b34-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="f9b34-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b34-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f9b34-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9b34-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b34-138">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="f9b34-138">A description of the object.</span></span> <span data-ttu-id="f9b34-139">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f9b34-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b34-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f9b34-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b34-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f9b34-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9b34-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b34-143">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f9b34-143">A display name for the object.</span></span> <span data-ttu-id="f9b34-144">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f9b34-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b34-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f9b34-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b34-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f9b34-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9b34-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-148">Qualificateurs : **clé**, **remplacement**</span><span class="sxs-lookup"><span data-stu-id="f9b34-148">Qualifiers: **Key**, **Override**</span></span>
</dt> </dl>

<span data-ttu-id="f9b34-149">Chaîne qui identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="f9b34-149">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f9b34-150">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f9b34-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f9b34-151">**OtherRegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="f9b34-151">**OtherRegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b34-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f9b34-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9b34-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-154">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="f9b34-154">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f9b34-155">Chaîne qui fournit une description de l’organisation lorsque **RegisteredOrganization** contient 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="f9b34-155">A string that provides a description of the organization when **RegisteredOrganization** contains 1 (Other).</span></span> <span data-ttu-id="f9b34-156">Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f9b34-156">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f9b34-157">**RegisteredName**</span><span class="sxs-lookup"><span data-stu-id="f9b34-157">**RegisteredName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b34-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f9b34-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9b34-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-160">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="f9b34-160">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f9b34-161">Nom de ce profil inscrit.</span><span class="sxs-lookup"><span data-stu-id="f9b34-161">The name of this registered profile.</span></span> <span data-ttu-id="f9b34-162">Étant donné que plusieurs versions peuvent exister pour le même **RegisteredName**, la combinaison de **RegisteredName**, **RegisteredOrganization** et **RegisteredVersion** doit identifier de façon unique le profil inscrit au sein de l’étendue de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f9b34-162">Since multiple versions can exist for the same **RegisteredName**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="f9b34-163">Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f9b34-163">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f9b34-164">**RegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="f9b34-164">**RegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b34-165">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9b34-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9b34-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b34-167">Organisation qui définit ce profil.</span><span class="sxs-lookup"><span data-stu-id="f9b34-167">The organization that defines this profile.</span></span> <span data-ttu-id="f9b34-168">Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f9b34-168">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="f9b34-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f9b34-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span><span class="sxs-lookup"><span data-stu-id="f9b34-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span><span class="sxs-lookup"><span data-stu-id="f9b34-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium pour l’innovation des services** (4)</span><span class="sxs-lookup"><span data-stu-id="f9b34-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium for Service Innovation** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-173"><span id="FAST"></span><span id="fast"></span>**Rapide** (5)</span><span class="sxs-lookup"><span data-stu-id="f9b34-173"><span id="FAST"></span><span id="fast"></span>**FAST** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6)</span><span class="sxs-lookup"><span data-stu-id="f9b34-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7)</span><span class="sxs-lookup"><span data-stu-id="f9b34-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span><span class="sxs-lookup"><span data-stu-id="f9b34-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span><span class="sxs-lookup"><span data-stu-id="f9b34-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10-Nord-Ouest de l’efficacité énergétique** (10)</span><span class="sxs-lookup"><span data-stu-id="f9b34-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10 Northwest Energy Efficiency Alliance** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span><span class="sxs-lookup"><span data-stu-id="f9b34-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**Forum TM** (12)</span><span class="sxs-lookup"><span data-stu-id="f9b34-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM Forum** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**Groupe ouvert** (13)</span><span class="sxs-lookup"><span data-stu-id="f9b34-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**The Open Group** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span><span class="sxs-lookup"><span data-stu-id="f9b34-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span><span class="sxs-lookup"><span data-stu-id="f9b34-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span><span class="sxs-lookup"><span data-stu-id="f9b34-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span><span class="sxs-lookup"><span data-stu-id="f9b34-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span><span class="sxs-lookup"><span data-stu-id="f9b34-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span><span class="sxs-lookup"><span data-stu-id="f9b34-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)</span><span class="sxs-lookup"><span data-stu-id="f9b34-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**Quadrillage vert** (21)</span><span class="sxs-lookup"><span data-stu-id="f9b34-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**The Green Grid** (21)</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="f9b34-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="f9b34-191">)</span><span class="sxs-lookup"><span data-stu-id="f9b34-191">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9b34-192">**RegisteredVersion**</span><span class="sxs-lookup"><span data-stu-id="f9b34-192">**RegisteredVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9b34-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f9b34-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9b34-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9b34-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9b34-195">Version de ce profil.</span><span class="sxs-lookup"><span data-stu-id="f9b34-195">The version of this profile.</span></span> <span data-ttu-id="f9b34-196">La chaîne doit se présenter sous la forme : "*M*. *N*. *U*» où :</span><span class="sxs-lookup"><span data-stu-id="f9b34-196">The string must be in the form: "*M*.*N*.*U*" Where:</span></span>

-   <span data-ttu-id="f9b34-197">*M* est la version principale (au format numérique) décrivant la création ou la dernière modification du profil.</span><span class="sxs-lookup"><span data-stu-id="f9b34-197">*M* is the major version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="f9b34-198">*N* est la version mineure (au format numérique) décrivant la création ou la dernière modification du profil.</span><span class="sxs-lookup"><span data-stu-id="f9b34-198">*N* is the minor version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="f9b34-199">*U* est la mise à jour (au format numérique) décrivant la création ou la dernière modification du profil.</span><span class="sxs-lookup"><span data-stu-id="f9b34-199">*U* is the update (in numeric form) describing the profile's creation or last modification.</span></span>

<span data-ttu-id="f9b34-200">Cette propriété est héritée de la [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f9b34-200">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9b34-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9b34-201">Requirements</span></span>



| <span data-ttu-id="f9b34-202">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9b34-202">Requirement</span></span> | <span data-ttu-id="f9b34-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9b34-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b34-204">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9b34-204">Minimum supported client</span></span><br/> | <span data-ttu-id="f9b34-205">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9b34-205">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f9b34-206">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9b34-206">Minimum supported server</span></span><br/> | <span data-ttu-id="f9b34-207">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9b34-207">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f9b34-208">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f9b34-208">Namespace</span></span><br/>                | <span data-ttu-id="f9b34-209">\\Interop racine</span><span class="sxs-lookup"><span data-stu-id="f9b34-209">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="f9b34-210">MOF</span><span class="sxs-lookup"><span data-stu-id="f9b34-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9b34-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9b34-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9b34-212">DLL</span><span class="sxs-lookup"><span data-stu-id="f9b34-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9b34-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f9b34-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

