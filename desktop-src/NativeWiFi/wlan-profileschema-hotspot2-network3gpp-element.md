---
description: Liste des ID PLMN (public Land Mobile Network).
ms.assetid: 2e5e23c0-e98f-48f8-97b8-c5f88c80c51e
title: Élément Network3GPP (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network3GPP
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7e19a7ccbc1579eb02ed47da82afe1eeaf8fed53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524514"
---
# <a name="network3gpp-hotspot2-element"></a><span data-ttu-id="4df8b-103">Élément Network3GPP (Hotspot2)</span><span class="sxs-lookup"><span data-stu-id="4df8b-103">Network3GPP (Hotspot2) Element</span></span>

<span data-ttu-id="4df8b-104">Liste des ID PLMN (public Land Mobile Network).</span><span class="sxs-lookup"><span data-stu-id="4df8b-104">A list of Public Land Mobile Network (PLMN) IDs.</span></span>

``` syntax
<xs:element name="Network3GPP"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="PLMNID"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="5"
                         />
                        <xs:maxLength
                            value="6"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="4df8b-105">L’élément est défini par l’élément [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4df8b-105">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4df8b-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4df8b-106">Child elements</span></span>



| <span data-ttu-id="4df8b-107">Élément</span><span class="sxs-lookup"><span data-stu-id="4df8b-107">Element</span></span> | <span data-ttu-id="4df8b-108">Type</span><span class="sxs-lookup"><span data-stu-id="4df8b-108">Type</span></span> | <span data-ttu-id="4df8b-109">Description</span><span class="sxs-lookup"><span data-stu-id="4df8b-109">Description</span></span>                                                                                                             |
|---------|------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df8b-110">PLMNID</span><span class="sxs-lookup"><span data-stu-id="4df8b-110">PLMNID</span></span>  |      | <span data-ttu-id="4df8b-111">ID PLMN individuel.</span><span class="sxs-lookup"><span data-stu-id="4df8b-111">An individual PLMN ID.</span></span> <span data-ttu-id="4df8b-112">Il s’agit d’un nombre décimal à 5 ou 6 chiffres correspondant au MCC/MNC d’un réseau 3GPP.</span><span class="sxs-lookup"><span data-stu-id="4df8b-112">This is a 5 or 6 digit decimal number corresponding to the MCC/MNC of a 3GPP network.</span></span><br/> |



 

 




