---
description: ProfileCreationType (dans ModemDMConfigProfile)
MS-HAID: WWAN\_profile\_v4.element\_1\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (dans ModemDMConfigProfile)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b755840d0308ec2d7a7bba5896b0cf67b7b61198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862514"
---
# <a name="span-idwwan_profile_v4element_1_profilecreationtypespanprofilecreationtype-in-modemdmconfigprofile"></a><span data-ttu-id="43ec0-103"><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (dans ModemDMConfigProfile)</span><span class="sxs-lookup"><span data-stu-id="43ec0-103"><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (in ModemDMConfigProfile)</span></span>

<span data-ttu-id="43ec0-104">Spécifie comment ce profil de DM de modem a été créé.</span><span class="sxs-lookup"><span data-stu-id="43ec0-104">Specifies how this modem DM profile was created.</span></span>

<span data-ttu-id="43ec0-105">Cette valeur est utilisée pour déterminer si un utilisateur peut supprimer le profil.</span><span class="sxs-lookup"><span data-stu-id="43ec0-105">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="43ec0-106">Les utilisateurs peuvent uniquement supprimer des profils **UserProvisioned** .</span><span class="sxs-lookup"><span data-stu-id="43ec0-106">Users can only delete **UserProvisioned** profiles.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="43ec0-107">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="43ec0-107">Element hierarchy</span></span>

[<ModemDMConfigProfile>](element-modemdmconfigprofile.md)  
**<ProfileCreationType>**

## <a name="syntax"></a><span data-ttu-id="43ec0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43ec0-108">Syntax</span></span>

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="43ec0-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="43ec0-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="43ec0-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="43ec0-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="43ec0-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="43ec0-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="43ec0-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="43ec0-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="43ec0-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="43ec0-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="43ec0-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="43ec0-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43ec0-115">Élément parent</span><span class="sxs-lookup"><span data-stu-id="43ec0-115">Parent Element</span></span></th>
<th><span data-ttu-id="43ec0-116">Description</span><span class="sxs-lookup"><span data-stu-id="43ec0-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43ec0-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="43ec0-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="43ec0-118">Profil de configuration DM du modem.</span><span class="sxs-lookup"><span data-stu-id="43ec0-118">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="related-elements"></a><span data-ttu-id="43ec0-119">Éléments apparentés</span><span class="sxs-lookup"><span data-stu-id="43ec0-119">Related elements</span></span>

<span data-ttu-id="43ec0-120">Les éléments suivants portent le même nom que celui-ci, mais ils ont un contenu ou des attributs différents :</span><span class="sxs-lookup"><span data-stu-id="43ec0-120">The following elements have the same name as this one, but different content or attributes:</span></span>

-   <span data-ttu-id="43ec0-121">**[ProfileCreationType (dans MBNProfileExt)](element-profilecreationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="43ec0-121">**[ProfileCreationType (in MBNProfileExt)](element-profilecreationtype.md)**</span></span>

## <a name="requirements"></a><span data-ttu-id="43ec0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43ec0-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43ec0-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="43ec0-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



