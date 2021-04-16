---
description: Liste d’identificateurs de domaine NAI (Network Access identifier).
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: Élément NAIRealm (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a7c8fcf85bd23c13f0e7501d59c3db62c2bf82f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527790"
---
# <a name="nairealm-hotspot2-element"></a><span data-ttu-id="2f171-103">Élément NAIRealm (Hotspot2)</span><span class="sxs-lookup"><span data-stu-id="2f171-103">NAIRealm (Hotspot2) Element</span></span>

<span data-ttu-id="2f171-104">Liste d’identificateurs de domaine NAI (Network Access identifier).</span><span class="sxs-lookup"><span data-stu-id="2f171-104">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="2f171-105">Les entrées de cette liste sont généralement de la forme `user@domain` .</span><span class="sxs-lookup"><span data-stu-id="2f171-105">Entries in this list are usually of the form `user@domain`.</span></span> <span data-ttu-id="2f171-106">La liste de domaines NAI est la méthode recommandée pour identifier la plupart des opérateurs non mobiles tels que MSO, les opérateurs câblés et les lieux publics.</span><span class="sxs-lookup"><span data-stu-id="2f171-106">The NAI Realm list is the preferred method to identify most non-mobile operators like MSOs, wireline operators, and public venues.</span></span>

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="255"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="2f171-107">L’élément est défini par l’élément [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2f171-107">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2f171-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2f171-108">Child elements</span></span>



| <span data-ttu-id="2f171-109">Élément</span><span class="sxs-lookup"><span data-stu-id="2f171-109">Element</span></span> | <span data-ttu-id="2f171-110">Type</span><span class="sxs-lookup"><span data-stu-id="2f171-110">Type</span></span> | <span data-ttu-id="2f171-111">Description</span><span class="sxs-lookup"><span data-stu-id="2f171-111">Description</span></span>                                                   |
|---------|------|---------------------------------------------------------------|
| <span data-ttu-id="2f171-112">name</span><span class="sxs-lookup"><span data-stu-id="2f171-112">name</span></span>    |      | <span data-ttu-id="2f171-113">Identificateur de domaine unique.</span><span class="sxs-lookup"><span data-stu-id="2f171-113">A single realm identifier.</span></span> <span data-ttu-id="2f171-114">Généralement du formulaire `user@domain` .</span><span class="sxs-lookup"><span data-stu-id="2f171-114">Usually of the form `user@domain`.</span></span> |



 

 



