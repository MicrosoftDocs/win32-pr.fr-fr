---
description: Énumération qui décrit le type de connexion réseau où un profil est applicable.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Type simple iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80013fa21574221de24a7fc8309e4459a80ad670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526614"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span data-ttu-id="900cf-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Type simple iwlanApplicabilityType</span><span class="sxs-lookup"><span data-stu-id="900cf-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>iwlanApplicabilityType Simple Type</span></span>

<span data-ttu-id="900cf-104">Énumération qui décrit le type de connexion réseau où un profil est applicable.</span><span class="sxs-lookup"><span data-stu-id="900cf-104">Enumeration that describes the kind of network connection where a profile is applicable.</span></span>

``` syntax
<xs:simpleType name="iwlanApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="CellularOnly"
         />
        <xs:enumeration
            value="CellularAndIwlan"
         />
        <xs:enumeration
            value="IwlanOnly"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="900cf-105">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="900cf-105">Enumeration values</span></span>

<span data-ttu-id="900cf-106">Le type simple **iwlanApplicabilityType** définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="900cf-106">The **iwlanApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="900cf-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="900cf-107">Value</span></span></th>
<th><span data-ttu-id="900cf-108">Description</span><span class="sxs-lookup"><span data-stu-id="900cf-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="900cf-109">CellularOnly</span><span class="sxs-lookup"><span data-stu-id="900cf-109">CellularOnly</span></span></td>
<td><p><span data-ttu-id="900cf-110">Le profil est valide uniquement pour les connexions au réseau cellulaire.</span><span class="sxs-lookup"><span data-stu-id="900cf-110">Profile is valid for cellular network connections only.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="900cf-111">CellularAndIwlan</span><span class="sxs-lookup"><span data-stu-id="900cf-111">CellularAndIwlan</span></span></td>
<td><p><span data-ttu-id="900cf-112">Le profil est valide pour les connexions mobiles ou Wi-Fi déchargées.</span><span class="sxs-lookup"><span data-stu-id="900cf-112">Profile is valid for cellular or Wi-Fi offloaded connections.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="900cf-113">IwlanOnly</span><span class="sxs-lookup"><span data-stu-id="900cf-113">IwlanOnly</span></span></td>
<td><p><span data-ttu-id="900cf-114">Le profil est valide uniquement pour les connexions Wi-Fi déchargées.</span><span class="sxs-lookup"><span data-stu-id="900cf-114">Profile is valid for Wi-Fi offloaded connections only.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



