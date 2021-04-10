---
description: MmsConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb98506476558ed0e39df11bab4b9446de4fd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201399"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span data-ttu-id="7677a-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span><span class="sxs-lookup"><span data-stu-id="7677a-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span></span>

<span data-ttu-id="7677a-104">Informations de configuration pour le service de messagerie multimédia (MMS).</span><span class="sxs-lookup"><span data-stu-id="7677a-104">Configuration information for Multimedia Messaging Service (MMS).</span></span>

<span data-ttu-id="7677a-105">En plus de définir les éléments de configuration dans cet élément, un profil MMS doit avoir les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="7677a-105">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span>

-   <span data-ttu-id="7677a-106">Son élément [**Name**](element-name.md) doit contenir un nom unique à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="7677a-106">Its [**Name**](element-name.md) element must contain a system-wide unique name.</span></span>
-   <span data-ttu-id="7677a-107">Son [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) doit avoir la valeur **UserProvisioned**.</span><span class="sxs-lookup"><span data-stu-id="7677a-107">Its [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) must be set to **UserProvisioned**.</span></span>
-   <span data-ttu-id="7677a-108">Son [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) doit contenir le ICCID de la carte SIM auquel ce profil est destiné.</span><span class="sxs-lookup"><span data-stu-id="7677a-108">Its [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) must contain the ICCID of the SIM that this profile is intended for.</span></span>
-   <span data-ttu-id="7677a-109">Son [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) doit être défini sur **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="7677a-109">Its [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) must be set to **Manual**.</span></span>
-   <span data-ttu-id="7677a-110">Son [**PurposeGroupGuid**](element-purposegroupguid.md) doit contenir le GUID du groupe d’objet MMS.</span><span class="sxs-lookup"><span data-stu-id="7677a-110">Its [**PurposeGroupGuid**](element-purposegroupguid.md) must contain the GUID for MMS purpose group.</span></span>
-   <span data-ttu-id="7677a-111">Son [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) doit avoir la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="7677a-111">Its [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) must be set to **true**.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="7677a-112">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="7677a-112">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<MmsConfiguration>**

## <a name="syntax"></a><span data-ttu-id="7677a-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7677a-113">Syntax</span></span>

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
```

### <a name="key"></a><span data-ttu-id="7677a-114">Clé</span><span class="sxs-lookup"><span data-stu-id="7677a-114">Key</span></span>

<span data-ttu-id="7677a-115">`?`   facultatif (zéro ou un)</span><span class="sxs-lookup"><span data-stu-id="7677a-115">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="7677a-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7677a-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="7677a-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="7677a-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="7677a-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="7677a-118">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="7677a-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7677a-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7677a-120">Élément enfant</span><span class="sxs-lookup"><span data-stu-id="7677a-120">Child Element</span></span></th>
<th><span data-ttu-id="7677a-121">Description</span><span class="sxs-lookup"><span data-stu-id="7677a-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7677a-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span><span class="sxs-lookup"><span data-stu-id="7677a-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span></span></td>
<td><p><span data-ttu-id="7677a-123">Spécifie la taille maximale, en kilo-octets, des messages MMS.</span><span class="sxs-lookup"><span data-stu-id="7677a-123">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="7677a-124">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7677a-124">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7677a-125"><a href="element-mmscport.md">MmscPort</a></span><span class="sxs-lookup"><span data-stu-id="7677a-125"><a href="element-mmscport.md">MmscPort</a></span></span></td>
<td><p><span data-ttu-id="7677a-126">Spécifie le numéro de port du serveur MMSC pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7677a-126">Specifies the port number of the MMSC server for the device.</span></span> <span data-ttu-id="7677a-127">Spécifiez 0 pour indiquer qu’aucun port spécifique n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="7677a-127">Specify 0 to indicate that no specific port is specified.</span></span> <span data-ttu-id="7677a-128">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7677a-128">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7677a-129"><a href="element-mmscurl.md">MmscUrl</a></span><span class="sxs-lookup"><span data-stu-id="7677a-129"><a href="element-mmscurl.md">MmscUrl</a></span></span></td>
<td><p><span data-ttu-id="7677a-130">Spécifie l’URL du serveur MMSC pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7677a-130">Specifies the URL of the MMSC server for the device.</span></span> <span data-ttu-id="7677a-131">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7677a-131">Optional.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="7677a-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7677a-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7677a-133">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7677a-133">Parent Element</span></span></th>
<th><span data-ttu-id="7677a-134">Description</span><span class="sxs-lookup"><span data-stu-id="7677a-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7677a-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="7677a-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="7677a-136">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="7677a-136">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="7677a-137">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="7677a-137">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="7677a-138">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="7677a-138">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="7677a-139">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="7677a-139">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="7677a-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7677a-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7677a-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7677a-141">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
