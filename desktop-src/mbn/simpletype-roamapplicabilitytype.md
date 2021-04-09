---
description: Le roamApplicabilityType décrit les conditions d’itinérance pour lesquelles un profil itinérant s’applique.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Type simple roamApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d81214ab5a44dcac60bb5e1a6accc81b0d0418
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862505"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span data-ttu-id="65860-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Type simple roamApplicabilityType</span><span class="sxs-lookup"><span data-stu-id="65860-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType Simple Type</span></span>

<span data-ttu-id="65860-104">Le roamApplicabilityType décrit les conditions d’itinérance pour lesquelles un profil itinérant s’applique.</span><span class="sxs-lookup"><span data-stu-id="65860-104">The roamApplicabilityType describes the roaming conditions for which a roaming profile applies.</span></span>

<span data-ttu-id="65860-105">Il s’agit d’un attribut plus expressif que [**roamControlType**](simpletype-roamcontroltype.md), et un profil doit utiliser **roamControlType** ou **roamApplicabilityType**, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="65860-105">This is a more expressive attribute than [**roamControlType**](simpletype-roamcontroltype.md), and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="65860-106">(Si un profil utilise les deux, les deux sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="65860-106">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="65860-107">Le résultat est l’intersection des deux.)</span><span class="sxs-lookup"><span data-stu-id="65860-107">The result is the intersection of the two.)</span></span>

<span data-ttu-id="65860-108">Utilisez cet attribut pour faire la distinction entre plusieurs profils avec des conditions d’itinérance disjointes, afin de spécifier des attributs de profil différents pour, par exemple, à l’emplacement d’hébergement et l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="65860-108">Use this attribute to differentiate between multiple profiles with disjoint roaming conditions, to specify different profile attributes for, for example, home versus roaming.</span></span>

<span data-ttu-id="65860-109">Il existe trois États d’inscription personnels/itinérants possibles :</span><span class="sxs-lookup"><span data-stu-id="65860-109">There are three possible home/roam registration states:</span></span>

-   <span data-ttu-id="65860-110">Page d’hébergement : inscrit sur le réseau privé</span><span class="sxs-lookup"><span data-stu-id="65860-110">Home: registered on the home network</span></span>
-   <span data-ttu-id="65860-111">Partenaire : inscrit sur un réseau étroitement affilié au réseau privé</span><span class="sxs-lookup"><span data-stu-id="65860-111">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="65860-112">Non partenaire : inscrit sur un réseau qui n’est pas étroitement affilié au réseau privé</span><span class="sxs-lookup"><span data-stu-id="65860-112">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="65860-113">La signification précise de « partenaire » varie en fonction du réseau, mais il représente une relation plus étroite avec des tarifs plus favorables qu’un partenaire non partenaire.</span><span class="sxs-lookup"><span data-stu-id="65860-113">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="65860-114">Cela peut être le cas si un opérateur basé sur une région a une organisation d’entreprise pour utiliser le réseau d’accès radio d’un autre opérateur en dehors de sa zone d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="65860-114">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="65860-115">Il peut également représenter la différence entre l’itinérance au sein d’une région (par exemple, l’UE) et l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="65860-115">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

``` syntax
<xs:simpleType name="roamApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="NonPartnerOnly"
         />
        <xs:enumeration
            value="PartnerOnly"
         />
        <xs:enumeration
            value="HomeOnly"
         />
        <xs:enumeration
            value="HomeAndPartner"
         />
        <xs:enumeration
            value="PartnerAndNonpartner"
         />
        <xs:enumeration
            value="AllRoaming"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="65860-116">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="65860-116">Enumeration values</span></span>

<span data-ttu-id="65860-117">Le type simple **roamApplicabilityType** définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="65860-117">The **roamApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65860-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="65860-118">Value</span></span></th>
<th><span data-ttu-id="65860-119">Description</span><span class="sxs-lookup"><span data-stu-id="65860-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65860-120">NonPartnerOnly</span><span class="sxs-lookup"><span data-stu-id="65860-120">NonPartnerOnly</span></span></td>
<td><p><span data-ttu-id="65860-121">Ce profil est utilisé uniquement lors de l’itinérance sur un réseau non partenaire</span><span class="sxs-lookup"><span data-stu-id="65860-121">This profile is used only when roaming on a non-partner network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65860-122">PartnerOnly</span><span class="sxs-lookup"><span data-stu-id="65860-122">PartnerOnly</span></span></td>
<td><p><span data-ttu-id="65860-123">Ce profil est utilisé uniquement lors de l’itinérance sur un réseau partenaire</span><span class="sxs-lookup"><span data-stu-id="65860-123">This profile is used only when roaming on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65860-124">HomeOnly</span><span class="sxs-lookup"><span data-stu-id="65860-124">HomeOnly</span></span></td>
<td><p><span data-ttu-id="65860-125">Ce profil est utilisé uniquement sur le réseau privé.</span><span class="sxs-lookup"><span data-stu-id="65860-125">This profile is used only when on the home network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65860-126">HomeAndPartner</span><span class="sxs-lookup"><span data-stu-id="65860-126">HomeAndPartner</span></span></td>
<td><p><span data-ttu-id="65860-127">Ce profil est utilisé uniquement quand vous êtes au bureau ou sur un réseau partenaire</span><span class="sxs-lookup"><span data-stu-id="65860-127">This profile is used only when at home or on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65860-128">PartnerAndNonpartner</span><span class="sxs-lookup"><span data-stu-id="65860-128">PartnerAndNonpartner</span></span></td>
<td><p><span data-ttu-id="65860-129">Ce profil est utilisé en cas de non-démarrage (itinérance sur n’importe quel réseau)</span><span class="sxs-lookup"><span data-stu-id="65860-129">This profile is used when not at home (roaming on any network)</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65860-130">AllRoaming</span><span class="sxs-lookup"><span data-stu-id="65860-130">AllRoaming</span></span></td>
<td><p><span data-ttu-id="65860-131">Ce profil est utilisé sur tous les réseaux</span><span class="sxs-lookup"><span data-stu-id="65860-131">This profile is used on all networks</span></span></p></td>
</tr>
</tbody>
</table>

 

 



