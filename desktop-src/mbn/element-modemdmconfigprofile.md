---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f4593d1b55b4c95a2ec185fe5545ad7eb04141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543658"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span data-ttu-id="1bd30-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span><span class="sxs-lookup"><span data-stu-id="1bd30-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span></span>

<span data-ttu-id="1bd30-104">Profil de configuration DM du modem.</span><span class="sxs-lookup"><span data-stu-id="1bd30-104">Modem DM configuration profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="1bd30-105">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="1bd30-105">Element hierarchy</span></span>

**<ModemDMConfigProfile>**

## <a name="syntax"></a><span data-ttu-id="1bd30-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bd30-106">Syntax</span></span>

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a><span data-ttu-id="1bd30-107">Clé</span><span class="sxs-lookup"><span data-stu-id="1bd30-107">Key</span></span>

<span data-ttu-id="1bd30-108">`?`   facultatif (zéro ou un)</span><span class="sxs-lookup"><span data-stu-id="1bd30-108">`?`   optional (zero or one)</span></span>

<span data-ttu-id="1bd30-109">`*`   facultatif (zéro, un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="1bd30-109">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="1bd30-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1bd30-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="1bd30-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="1bd30-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="1bd30-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="1bd30-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="1bd30-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1bd30-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1bd30-114">Élément enfant</span><span class="sxs-lookup"><span data-stu-id="1bd30-114">Child Element</span></span></th>
<th><span data-ttu-id="1bd30-115">Description</span><span class="sxs-lookup"><span data-stu-id="1bd30-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1bd30-116"><a href="element-1-adminenable.md">AdminEnable</a></span><span class="sxs-lookup"><span data-stu-id="1bd30-116"><a href="element-1-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="1bd30-117">Spécifie si le profil est activé de manière administrative. Il s’agit d’un nouvel élément pour v4.</span><span class="sxs-lookup"><span data-stu-id="1bd30-117">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1bd30-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span><span class="sxs-lookup"><span data-stu-id="1bd30-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="1bd30-119">Spécifie si le profil est contrôlé par un itinérance administrative.</span><span class="sxs-lookup"><span data-stu-id="1bd30-119">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="1bd30-120">Cet élément est une nouveauté pour v4.</span><span class="sxs-lookup"><span data-stu-id="1bd30-120">This element is new for v4.</span></span> <span data-ttu-id="1bd30-121">La valeur de cet élément est une valeur <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1bd30-121">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="1bd30-122">Il s’agit d’un élément facultatif ; Si aucune valeur n’est spécifiée, <strong>AllRoamAllowed</strong> est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="1bd30-122">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1bd30-123"><a href="element-1-apnid.md">ApnID</a></span><span class="sxs-lookup"><span data-stu-id="1bd30-123"><a href="element-1-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="1bd30-124">ID APN associé à ce profil. Cet élément est une nouveauté de V4 et il est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1bd30-124">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1bd30-125"><a href="element-1-context.md">Contexte</a></span><span class="sxs-lookup"><span data-stu-id="1bd30-125"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="1bd30-126">Spécifie les paramètres requis pour établir une connexion de données.</span><span class="sxs-lookup"><span data-stu-id="1bd30-126">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1bd30-127"><a href="element-1-name.md">Nom</a></span><span class="sxs-lookup"><span data-stu-id="1bd30-127"><a href="element-1-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="1bd30-128">Nom du profil.</span><span class="sxs-lookup"><span data-stu-id="1bd30-128">The name of the profile.</span></span> <span data-ttu-id="1bd30-129">Pour plus d’informations, consultez la documentation de l’élément de <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nom</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="1bd30-129">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1bd30-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span><span class="sxs-lookup"><span data-stu-id="1bd30-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span></span></td>
<td><p><span data-ttu-id="1bd30-131">ID de connexion OEM pour la configuration DM du modem.</span><span class="sxs-lookup"><span data-stu-id="1bd30-131">The OEM connection ID for the modem DM configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1bd30-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (dans ModemDMConfigProfile)</a></span><span class="sxs-lookup"><span data-stu-id="1bd30-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></span></span></td>
<td><p><span data-ttu-id="1bd30-133">Spécifie comment ce profil de DM de modem a été créé.</span><span class="sxs-lookup"><span data-stu-id="1bd30-133">Specifies how this modem DM profile was created.</span></span></p>
<p><span data-ttu-id="1bd30-134">Cette valeur est utilisée pour déterminer si un utilisateur peut supprimer le profil.</span><span class="sxs-lookup"><span data-stu-id="1bd30-134">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="1bd30-135">Les utilisateurs peuvent uniquement supprimer des profils <strong>UserProvisioned</strong> .</span><span class="sxs-lookup"><span data-stu-id="1bd30-135">Users can only delete <strong>UserProvisioned</strong> profiles.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1bd30-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span><span class="sxs-lookup"><span data-stu-id="1bd30-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="1bd30-137">Spécifie que ce profil est actif uniquement lorsque la condition d’itinérance actuelle est celle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1bd30-137">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="1bd30-138">Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="1bd30-138">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="1bd30-139">La valeur de cet élément doit être une valeur <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valide.</span><span class="sxs-lookup"><span data-stu-id="1bd30-139">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1bd30-140"><a href="element-1-simiccid.md">SimIccID</a></span><span class="sxs-lookup"><span data-stu-id="1bd30-140"><a href="element-1-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="1bd30-141">Numéro de identifcation SIM pour les appareils GSM.</span><span class="sxs-lookup"><span data-stu-id="1bd30-141">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="1bd30-142">Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="1bd30-142">For more details , see the documentation for the v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="1bd30-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1bd30-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="1bd30-144">Cet élément (document) le plus à l’extérieur ne peut pas être contenu dans d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="1bd30-144">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bd30-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bd30-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bd30-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1bd30-146">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



