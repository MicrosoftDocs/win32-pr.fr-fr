---
description: MmsMaximumMessageSize
MS-HAID: WWAN\_profile\_v4.element\_MmsMaximumMessageSize
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsMaximumMessageSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5b020e7fd6ad4f39bd488c3af0ef14a3aab1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201542"
---
# <a name="span-idwwan_profile_v4element_mmsmaximummessagesizespanmmsmaximummessagesize"></a><span data-ttu-id="816e8-103"><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>MmsMaximumMessageSize</span><span class="sxs-lookup"><span data-stu-id="816e8-103"><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>MmsMaximumMessageSize</span></span>

<span data-ttu-id="816e8-104">Spécifie la taille maximale, en kilo-octets, des messages MMS.</span><span class="sxs-lookup"><span data-stu-id="816e8-104">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="816e8-105">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="816e8-105">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="816e8-106">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="816e8-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmsMaximumMessageSize>**

## <a name="syntax"></a><span data-ttu-id="816e8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="816e8-107">Syntax</span></span>

``` syntax
<MmsMaximumMessageSize>

  nonNegativeInteger

</MmsMaximumMessageSize>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="816e8-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="816e8-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="816e8-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="816e8-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="816e8-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="816e8-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="816e8-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="816e8-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="816e8-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="816e8-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="816e8-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="816e8-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="816e8-114">Élément parent</span><span class="sxs-lookup"><span data-stu-id="816e8-114">Parent Element</span></span></th>
<th><span data-ttu-id="816e8-115">Description</span><span class="sxs-lookup"><span data-stu-id="816e8-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="816e8-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="816e8-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="816e8-117">Informations de configuration pour le service de messagerie multimédia (MMS).</span><span class="sxs-lookup"><span data-stu-id="816e8-117">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="816e8-118">En plus de définir les éléments de configuration dans cet élément, un profil MMS doit avoir les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="816e8-118">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="816e8-119">Son élément <a href="element-name.md"><strong>Name</strong></a> doit contenir un nom unique à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="816e8-119">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="816e8-120">Son <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> doit avoir la valeur <strong>UserProvisioned</strong>.</span><span class="sxs-lookup"><span data-stu-id="816e8-120">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="816e8-121">Son <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> doit contenir le ICCID de la carte SIM auquel ce profil est destiné.</span><span class="sxs-lookup"><span data-stu-id="816e8-121">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="816e8-122">Son <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> doit être défini sur <strong>Manuel</strong>.</span><span class="sxs-lookup"><span data-stu-id="816e8-122">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="816e8-123">Son <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> doit contenir le GUID du groupe d’objet MMS.</span><span class="sxs-lookup"><span data-stu-id="816e8-123">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="816e8-124">Son <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> doit avoir la valeur <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="816e8-124">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="816e8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="816e8-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="816e8-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="816e8-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
