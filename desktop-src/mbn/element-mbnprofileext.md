---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318489"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span data-ttu-id="45348-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span><span class="sxs-lookup"><span data-stu-id="45348-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span></span>

<span data-ttu-id="45348-104">L’élément **MBNProfileExt** est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="45348-104">The **MBNProfileExt** element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="45348-105">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="45348-105">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span>

<span data-ttu-id="45348-106">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="45348-106">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="45348-107">Utilisez l’élément enfant [**ProfileConditionedOn**](element-profileconditionedon.md) de **MBNProfileExt** pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="45348-107">Use the [**ProfileConditionedOn**](element-profileconditionedon.md) child element of **MBNProfileExt** to specify which operating conditions make a particular profile the active profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="45348-108">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="45348-108">Element hierarchy</span></span>

**<MBNProfileExt>**

## <a name="syntax"></a><span data-ttu-id="45348-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45348-109">Syntax</span></span>

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a><span data-ttu-id="45348-110">Clé</span><span class="sxs-lookup"><span data-stu-id="45348-110">Key</span></span>

<span data-ttu-id="45348-111">`?`   facultatif (zéro ou un)</span><span class="sxs-lookup"><span data-stu-id="45348-111">`?`   optional (zero or one)</span></span>

<span data-ttu-id="45348-112">`*`   facultatif (zéro, un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="45348-112">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="45348-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="45348-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="45348-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="45348-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="45348-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="45348-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="45348-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="45348-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45348-117">Élément enfant</span><span class="sxs-lookup"><span data-stu-id="45348-117">Child Element</span></span></th>
<th><span data-ttu-id="45348-118">Description</span><span class="sxs-lookup"><span data-stu-id="45348-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45348-119"><a href="element-adminenable.md">AdminEnable</a></span><span class="sxs-lookup"><span data-stu-id="45348-119"><a href="element-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="45348-120">Spécifie si le profil est activé de manière administrative. Il s’agit d’un nouvel élément pour v4.</span><span class="sxs-lookup"><span data-stu-id="45348-120">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45348-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span><span class="sxs-lookup"><span data-stu-id="45348-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="45348-122">Spécifie si le profil est contrôlé par un itinérance administrative.</span><span class="sxs-lookup"><span data-stu-id="45348-122">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="45348-123">Cet élément est une nouveauté pour v4.</span><span class="sxs-lookup"><span data-stu-id="45348-123">This element is new for v4.</span></span> <span data-ttu-id="45348-124">La valeur de cet élément est une valeur <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="45348-124">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="45348-125">Il s’agit d’un élément facultatif ; Si aucune valeur n’est spécifiée, <strong>AllRoamAllowed</strong> est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="45348-125">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45348-126"><a href="element-apnid.md">ApnID</a></span><span class="sxs-lookup"><span data-stu-id="45348-126"><a href="element-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="45348-127">ID APN associé à ce profil. Cet élément est une nouveauté de V4 et il est facultatif.</span><span class="sxs-lookup"><span data-stu-id="45348-127">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45348-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span><span class="sxs-lookup"><span data-stu-id="45348-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span></span></td>
<td><p><span data-ttu-id="45348-129">Spécifie si l’appareil haut débit mobile se connecte automatiquement à un réseau.</span><span class="sxs-lookup"><span data-stu-id="45348-129">Specifies whether the Mobile Broadband device will automatically connect to a network.</span></span></p>
<p><span data-ttu-id="45348-130">Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="45348-130">For more information, see the documentation for the v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45348-131"><a href="element-connectionmode.md">ConnectionMode</a></span><span class="sxs-lookup"><span data-stu-id="45348-131"><a href="element-connectionmode.md">ConnectionMode</a></span></span></td>
<td><p><span data-ttu-id="45348-132">Spécifie le paramètre de connexion automatique à utiliser pour un appareil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="45348-132">Specifies the auto connection setting to be used for a Mobile Broadband device.</span></span></p>
<p><span data-ttu-id="45348-133">Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="45348-133">For more information, see the documentation for the v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45348-134"><a href="element-context.md">Contexte</a></span><span class="sxs-lookup"><span data-stu-id="45348-134"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="45348-135">Spécifie les paramètres requis pour établir une connexion de données.</span><span class="sxs-lookup"><span data-stu-id="45348-135">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45348-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span><span class="sxs-lookup"><span data-stu-id="45348-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span></span></td>
<td><p><span data-ttu-id="45348-137">Spécifie une liste de fournisseurs de réseau préférés lors de l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="45348-137">Specifies a list of preferred network providers when roaming.</span></span></p>
<p><span data-ttu-id="45348-138">Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="45348-138">For details, see the documentation for the v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45348-139"><a href="element-description.md">Description</a></span><span class="sxs-lookup"><span data-stu-id="45348-139"><a href="element-description.md">Description</a></span></span></td>
<td><p><span data-ttu-id="45348-140">Description du profil.</span><span class="sxs-lookup"><span data-stu-id="45348-140">A description of the profile.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45348-141"><a href="element-homeprovidername.md">HomeProviderName</a></span><span class="sxs-lookup"><span data-stu-id="45348-141"><a href="element-homeprovidername.md">HomeProviderName</a></span></span></td>
<td><p><span data-ttu-id="45348-142">Nom du fournisseur d’hébergement pour la carte SIM/le périphérique donné.</span><span class="sxs-lookup"><span data-stu-id="45348-142">The name of the home provider for the given SIM/Device.</span></span> <span data-ttu-id="45348-143">Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="45348-143">For more information, see the documentation for the v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45348-144"><a href="element-iconfilepath.md">ICONFilePath</a></span><span class="sxs-lookup"><span data-stu-id="45348-144"><a href="element-iconfilepath.md">ICONFilePath</a></span></span></td>
<td><p><span data-ttu-id="45348-145">Chemin d’accès au fichier d’icône pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="45348-145">The path to the icon file for the connection.</span></span> <span data-ttu-id="45348-146">L’interface utilisateur de la connexion au système d’exploitation affiche l’icône lorsqu’une connexion est établie à l’aide de ce profil.</span><span class="sxs-lookup"><span data-stu-id="45348-146">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span></p>
<p><span data-ttu-id="45348-147">Pour plus d’informations sur l’utilisation de cet élément, consultez la documentation v1 pour <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="45348-147">For more details on using this element, see the v1 documentation for <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45348-148"><a href="element-isdefault.md">IsDefault</a></span><span class="sxs-lookup"><span data-stu-id="45348-148"><a href="element-isdefault.md">IsDefault</a></span></span></td>
<td><p><span data-ttu-id="45348-149">Spécifie si ce profil est le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="45348-149">Specifies whether this profile is the default profile.</span></span></p>
<p><span data-ttu-id="45348-150">Pour plus d’informations sur cet élément, consultez la documentation v1 pour <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="45348-150">For more detail on this element, see the v1 documentation for <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45348-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span><span class="sxs-lookup"><span data-stu-id="45348-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span></span></td>
<td><p><span data-ttu-id="45348-152">Spécifie que ce profil est exclusif à d’autres profils du ou des mêmes jeux de profils. Cet élément est une nouveauté pour v4.</span><span class="sxs-lookup"><span data-stu-id="45348-152">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45348-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span><span class="sxs-lookup"><span data-stu-id="45348-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span></span></td>
<td><p><span data-ttu-id="45348-154">Spécifie que ce profil est un profil de contexte PDP supplémentaire à long terme. Si la valeur de cet élément est <strong>true</strong>, <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> doit également être défini sur <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="45348-154">Specifies that this profile is a long-standing additional PDP context profile.If the value of this element is <strong>true</strong>, then <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must also be set to <strong>true</strong>.</span></span> <span data-ttu-id="45348-155">Il s’agit d’un nouvel élément pour v4.</span><span class="sxs-lookup"><span data-stu-id="45348-155">This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45348-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span><span class="sxs-lookup"><span data-stu-id="45348-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span></span></td>
<td><p><span data-ttu-id="45348-157">Spécifie que ce profil ne doit être utilisé que pour l’approvisionnement. Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="45348-157">Specifies that this profile is to be used for provisioning only.Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="45348-158">Cet élément est une nouveauté pour v4.</span><span class="sxs-lookup"><span data-stu-id="45348-158">This element is new for v4.</span></span></p>
<p><span data-ttu-id="45348-159">Si <strong>IsProvisioningProfile</strong> a la valeur true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> doit avoir la valeur false et <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> doit être manuel.</span><span class="sxs-lookup"><span data-stu-id="45348-159">If <strong>IsProvisioningProfile</strong> is true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> must be false, and <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> must be manual.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45348-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="45348-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="45348-161">Informations de configuration pour le service de messagerie multimédia (MMS).</span><span class="sxs-lookup"><span data-stu-id="45348-161">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="45348-162">En plus de définir les éléments de configuration dans cet élément, un profil MMS doit avoir les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="45348-162">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="45348-163">Son élément <a href="element-name.md"><strong>Name</strong></a> doit contenir un nom unique à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="45348-163">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="45348-164">Son <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> doit avoir la valeur <strong>UserProvisioned</strong>.</span><span class="sxs-lookup"><span data-stu-id="45348-164">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="45348-165">Son <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> doit contenir le ICCID de la carte SIM auquel ce profil est destiné.</span><span class="sxs-lookup"><span data-stu-id="45348-165">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="45348-166">Son <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> doit être défini sur <strong>Manuel</strong>.</span><span class="sxs-lookup"><span data-stu-id="45348-166">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="45348-167">Son <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> doit contenir le GUID du groupe d’objet MMS.</span><span class="sxs-lookup"><span data-stu-id="45348-167">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="45348-168">Son <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> doit avoir la valeur <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="45348-168">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45348-169"><a href="element-name.md">Nom</a></span><span class="sxs-lookup"><span data-stu-id="45348-169"><a href="element-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="45348-170">Nom du profil.</span><span class="sxs-lookup"><span data-stu-id="45348-170">The name of the profile.</span></span> <span data-ttu-id="45348-171">Pour plus d’informations, consultez la documentation de l’élément de <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nom</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="45348-171">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45348-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="45348-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="45348-173">Spécifie les conditions qui doivent être satisfaites pour qu’un profil soit applicable.</span><span class="sxs-lookup"><span data-stu-id="45348-173">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="45348-174">Cet élément est une nouveauté pour v4.</span><span class="sxs-lookup"><span data-stu-id="45348-174">This element is new for v4.</span></span> <span data-ttu-id="45348-175">Elle vous permet de spécifier plusieurs profils qui s’appliquent dans différentes conditions, et pour que le profil approprié soit utilisé automatiquement lorsqu’il est applicable.</span><span class="sxs-lookup"><span data-stu-id="45348-175">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="45348-176">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="45348-176">This element is optional.</span></span> <span data-ttu-id="45348-177">Si vous ne le spécifiez pas, le profil est toujours applicable en ce qui concerne les conditions indiquées.</span><span class="sxs-lookup"><span data-stu-id="45348-177">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45348-178"><a href="element-profilecreationtype.md">ProfileCreationType (dans MBNProfileExt)</a></span><span class="sxs-lookup"><span data-stu-id="45348-178"><a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a></span></span></td>
<td><p><span data-ttu-id="45348-179">Spécifie le créateur du profil.</span><span class="sxs-lookup"><span data-stu-id="45348-179">Specifies the creator of the profile.</span></span></p>
<p><span data-ttu-id="45348-180">Pour plus d’informations sur cet élément, consultez la documentation de l’élément <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="45348-180">For more information about this element, see the documentation for the v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45348-181"><a href="element-purposegroups.md">PurposeGroups</a></span><span class="sxs-lookup"><span data-stu-id="45348-181"><a href="element-purposegroups.md">PurposeGroups</a></span></span></td>
<td><p><span data-ttu-id="45348-182">Liste facultative de groupes de profils, où chaque groupe comprend des profils utilisés dans un but commun.</span><span class="sxs-lookup"><span data-stu-id="45348-182">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span></p>
<p><span data-ttu-id="45348-183">Cet élément est une nouveauté pour v4 du schéma.</span><span class="sxs-lookup"><span data-stu-id="45348-183">This element is new for v4 of the schema.</span></span></p>
<p><span data-ttu-id="45348-184">Un profil peut être listé dans plusieurs groupes.</span><span class="sxs-lookup"><span data-stu-id="45348-184">One profile can be listed in multiple groups.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45348-185"><a href="element-simiccid.md">SimIccID</a></span><span class="sxs-lookup"><span data-stu-id="45348-185"><a href="element-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="45348-186">Numéro de identifcation SIM pour les appareils GSM.</span><span class="sxs-lookup"><span data-stu-id="45348-186">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="45348-187">Pour plus d’informations, consultez la documentation de l’élément <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="45348-187">For more details , see the documentation for the v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45348-188"><a href="element-subscriberid.md">Abonné</a></span><span class="sxs-lookup"><span data-stu-id="45348-188"><a href="element-subscriberid.md">SubscriberID</a></span></span></td>
<td><p><span data-ttu-id="45348-189">Identifie l’identificateur unique du profil.</span><span class="sxs-lookup"><span data-stu-id="45348-189">Identifies the unique identifier of the profile.</span></span></p>
<p><span data-ttu-id="45348-190">Pour un réseau GSM, il doit contenir le IMSI (identité de l’abonné mobile international) de la carte SIM et des appareils CDMA. il doit contenir la valeur minimale (numéro d’identification mobile) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45348-190">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span></p>
<p><span data-ttu-id="45348-191">Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>abonné</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="45348-191">For more information, see the documentation for the v1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="45348-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="45348-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="45348-193">Cet élément (document) le plus à l’extérieur ne peut pas être contenu dans d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="45348-193">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="45348-194">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45348-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45348-195">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45348-195">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
