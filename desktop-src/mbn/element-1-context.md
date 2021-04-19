---
description: '\/Contexte ModemDMConfigProfile (v4)'
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Contexte (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 133f48d9c9a1c9dd9f0e04f59d5e35478caa9227
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106521796"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span data-ttu-id="d8553-103"><span id="WWAN_profile_v4.element_1_Context"></span>\/Contexte ModemDMConfigProfile (v4)</span><span class="sxs-lookup"><span data-stu-id="d8553-103"><span id="WWAN_profile_v4.element_1_Context"></span>ModemDMConfigProfile\/Context (v4)</span></span>

<span data-ttu-id="d8553-104">Spécifie les paramètres requis pour établir une connexion de données.</span><span class="sxs-lookup"><span data-stu-id="d8553-104">Specifies the parameters required to establish a data connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="d8553-105">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="d8553-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a><span data-ttu-id="d8553-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8553-106">Syntax</span></span>

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a><span data-ttu-id="d8553-107">Clé</span><span class="sxs-lookup"><span data-stu-id="d8553-107">Key</span></span>

<span data-ttu-id="d8553-108">`?`   facultatif (zéro ou un)</span><span class="sxs-lookup"><span data-stu-id="d8553-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="d8553-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d8553-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="d8553-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="d8553-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="d8553-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="d8553-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="d8553-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d8553-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8553-113">Élément enfant</span><span class="sxs-lookup"><span data-stu-id="d8553-113">Child Element</span></span></th>
<th><span data-ttu-id="d8553-114">Description</span><span class="sxs-lookup"><span data-stu-id="d8553-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8553-115"><a href="element-1-accessstring.md">AccessString</a></span><span class="sxs-lookup"><span data-stu-id="d8553-115"><a href="element-1-accessstring.md">AccessString</a></span></span></td>
<td><p><span data-ttu-id="d8553-116">Identifie l’APN ou la chaîne de numérotation à utiliser pour établir une connexion de données.</span><span class="sxs-lookup"><span data-stu-id="d8553-116">Identifies the APN or dial string to be used to establish a data connection.</span></span></p>
<p><span data-ttu-id="d8553-117">Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="d8553-117">For more information, see the documentation for the v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8553-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span><span class="sxs-lookup"><span data-stu-id="d8553-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span></span></td>
<td><p><span data-ttu-id="d8553-119">>Spécifie le protocole d’authentification à utiliser pour l’activation d’un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="d8553-119">>Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span></p>
<p><span data-ttu-id="d8553-120">Notez que, dans v4, une nouvelle valeur d’énumération est disponible pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="d8553-120">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="d8553-121">La <strong>sélection SELECT</strong> signifie qu’un protocole d’authentification doit être choisi par des couches inférieures.</span><span class="sxs-lookup"><span data-stu-id="d8553-121"><strong>AutoSelection</strong> means that an auth protocol is to be picked by lower layer(s).</span></span></p>
<p><span data-ttu-id="d8553-122">Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="d8553-122">For further information, see the documentation for the v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d8553-123"><a href="element-1-compression.md">Compression</a></span><span class="sxs-lookup"><span data-stu-id="d8553-123"><a href="element-1-compression.md">Compression</a></span></span></td>
<td><p><span data-ttu-id="d8553-124">Spécifie si la compression est utilisée au niveau de la liaison de données pour l’en-tête et le transfert de données.</span><span class="sxs-lookup"><span data-stu-id="d8553-124">Specifies whether compression will be used at the data link for header and data transfer.</span></span></p>
<p><span data-ttu-id="d8553-125">Pour plus d’informations, consultez la documentation de l’élément de <a href="../mbn/schema-compression-contexttype-element.md"><strong>compression</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="d8553-125">For more information, see the documentation for the v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8553-126"><a href="element-1-iptype.md">IPType</a></span><span class="sxs-lookup"><span data-stu-id="d8553-126"><a href="element-1-iptype.md">IPType</a></span></span></td>
<td><p><span data-ttu-id="d8553-127">Spécifie le type d’IP à utiliser sur cette connexion de données.</span><span class="sxs-lookup"><span data-stu-id="d8553-127">Specifies the IP type to be used on this data connection.</span></span></p>
<p><span data-ttu-id="d8553-128">Cet élément est une nouveauté de v4 du schéma.</span><span class="sxs-lookup"><span data-stu-id="d8553-128">This element is new in v4 of the schema.</span></span> <span data-ttu-id="d8553-129">L’élément peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8553-129">The element can have one of the following values.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d8553-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8553-130">Value</span></span></th>
<th><span data-ttu-id="d8553-131">Signification</span><span class="sxs-lookup"><span data-stu-id="d8553-131">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8553-132">Default</span><span class="sxs-lookup"><span data-stu-id="d8553-132">Default</span></span></td>
<td><span data-ttu-id="d8553-133">Le type d’adresse IP doit être choisi par la ou les couches inférieures</span><span class="sxs-lookup"><span data-stu-id="d8553-133">IP type is to be picked by lower layer(s)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8553-134">IPv4</span><span class="sxs-lookup"><span data-stu-id="d8553-134">IPv4</span></span></td>
<td><span data-ttu-id="d8553-135">Utiliser IPv4</span><span class="sxs-lookup"><span data-stu-id="d8553-135">Use IPv4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d8553-136">IPv6</span><span class="sxs-lookup"><span data-stu-id="d8553-136">IPv6</span></span></td>
<td><span data-ttu-id="d8553-137">Utiliser IPv6</span><span class="sxs-lookup"><span data-stu-id="d8553-137">Use IPv6</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8553-138">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="d8553-138">IPv4v6</span></span></td>
<td><span data-ttu-id="d8553-139">Utilisez IPv4 et/ou IPv6, comme disponible.</span><span class="sxs-lookup"><span data-stu-id="d8553-139">Use IPv4 and/or IPv6, as available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d8553-140">XLAT</span><span class="sxs-lookup"><span data-stu-id="d8553-140">XLAT</span></span></td>
<td><span data-ttu-id="d8553-141">Utiliser 464XLAT pour transférer des réseaux IPv4 sur des réseaux IPv6</span><span class="sxs-lookup"><span data-stu-id="d8553-141">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d8553-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="d8553-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="d8553-143">Informations d’identification d’ouverture de session pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="d8553-143">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="d8553-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d8553-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8553-145">Élément parent</span><span class="sxs-lookup"><span data-stu-id="d8553-145">Parent Element</span></span></th>
<th><span data-ttu-id="d8553-146">Description</span><span class="sxs-lookup"><span data-stu-id="d8553-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8553-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="d8553-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="d8553-148">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="d8553-148">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="d8553-149">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="d8553-149">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="d8553-150">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="d8553-150">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="d8553-151">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="d8553-151">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8553-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="d8553-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="d8553-153">Profil de configuration DM du modem.</span><span class="sxs-lookup"><span data-stu-id="d8553-153">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="d8553-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8553-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8553-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8553-155">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



