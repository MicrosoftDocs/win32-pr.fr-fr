---
description: Décrit comment le profil contrôle l’itinérance.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Type simple roamControlType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911e379773e7d8eabfb7a1524b1a21ba16718a53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514199"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span data-ttu-id="2607c-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Type simple roamControlType</span><span class="sxs-lookup"><span data-stu-id="2607c-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamControlType Simple Type</span></span>

<span data-ttu-id="2607c-104">Décrit comment le profil contrôle l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="2607c-104">Describes how the profile controls roaming.</span></span>

<span data-ttu-id="2607c-105">Il existe deux États d’inscription itinérants possibles :</span><span class="sxs-lookup"><span data-stu-id="2607c-105">There are two possible roam registration states:</span></span>

-   <span data-ttu-id="2607c-106">Partenaire : inscrit sur un réseau étroitement affilié au réseau privé</span><span class="sxs-lookup"><span data-stu-id="2607c-106">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="2607c-107">Non partenaire : inscrit sur un réseau qui n’est pas étroitement affilié au réseau privé</span><span class="sxs-lookup"><span data-stu-id="2607c-107">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="2607c-108">La signification précise de « partenaire » varie en fonction du réseau, mais il représente une relation plus étroite avec des tarifs plus favorables qu’un partenaire non partenaire.</span><span class="sxs-lookup"><span data-stu-id="2607c-108">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="2607c-109">Cela peut être le cas si un opérateur basé sur une région a une organisation d’entreprise pour utiliser le réseau d’accès radio d’un autre opérateur en dehors de sa zone d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="2607c-109">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="2607c-110">Il peut également représenter la différence entre l’itinérance au sein d’une région (par exemple, l’UE) et l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="2607c-110">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

<span data-ttu-id="2607c-111">Notez que [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) est un attribut plus expressif que **roamControlType**, et qu’un profil doit utiliser **roamControlType** ou **roamApplicabilityType**, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="2607c-111">Note that [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) is a more expressive attribute than **roamControlType**, and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="2607c-112">(Si un profil utilise les deux, les deux sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="2607c-112">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="2607c-113">Le résultat est l’intersection des deux.)</span><span class="sxs-lookup"><span data-stu-id="2607c-113">The result is the intersection of the two.)</span></span>

``` syntax
<xs:simpleType name="roamControlType">
    <xs:restriction>
        <xs:enumeration
            value="AllRoamAllowed"
         />
        <xs:enumeration
            value="PartnerRoamAllowed"
         />
        <xs:enumeration
            value="NoRoamAllowed"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="2607c-114">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="2607c-114">Enumeration values</span></span>

<span data-ttu-id="2607c-115">Le type simple **roamControlType** définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2607c-115">The **roamControlType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2607c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2607c-116">Value</span></span></th>
<th><span data-ttu-id="2607c-117">Description</span><span class="sxs-lookup"><span data-stu-id="2607c-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2607c-118">AllRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="2607c-118">AllRoamAllowed</span></span></td>
<td><p><span data-ttu-id="2607c-119">L’itinérance est autorisée sur les réseaux partenaires et non-partenaires.</span><span class="sxs-lookup"><span data-stu-id="2607c-119">Roaming is allowed on Partner and Non-Partner networks.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2607c-120">PartnerRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="2607c-120">PartnerRoamAllowed</span></span></td>
<td><p><span data-ttu-id="2607c-121">L’itinérance est autorisée uniquement sur les réseaux partenaires.</span><span class="sxs-lookup"><span data-stu-id="2607c-121">Roaming is allowed only on Partner networks.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2607c-122">NoRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="2607c-122">NoRoamAllowed</span></span></td>
<td><p><span data-ttu-id="2607c-123">Aucune itinérance n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="2607c-123">No roaming is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



