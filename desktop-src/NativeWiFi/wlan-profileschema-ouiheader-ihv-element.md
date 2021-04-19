---
description: Identifie le IHV.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Élément OUIHeader (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a31feb123e31489c751b7844e06d5c344278778e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515630"
---
# <a name="ouiheader-ihv-element"></a><span data-ttu-id="ee4ac-103">Élément OUIHeader (IHV)</span><span class="sxs-lookup"><span data-stu-id="ee4ac-103">OUIHeader (IHV) Element</span></span>

<span data-ttu-id="ee4ac-104">L’élément OUIHeader (IHV) identifie le IHV.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-104">The OUIHeader (IHV) element identifies the IHV.</span></span>

<span data-ttu-id="ee4ac-105">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="3"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="type">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="1"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="ee4ac-106">L’élément est défini par l’élément [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ee4ac-106">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ee4ac-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ee4ac-107">Child elements</span></span>



| <span data-ttu-id="ee4ac-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ee4ac-108">Element</span></span>                                                   | <span data-ttu-id="ee4ac-109">Type</span><span class="sxs-lookup"><span data-stu-id="ee4ac-109">Type</span></span> | <span data-ttu-id="ee4ac-110">Description</span><span class="sxs-lookup"><span data-stu-id="ee4ac-110">Description</span></span>                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee4ac-111">**OUI**</span><span class="sxs-lookup"><span data-stu-id="ee4ac-111">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)   |      | <span data-ttu-id="ee4ac-112">Contient une hexBinary de 3 octets qui identifie le IHV.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-112">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                            |
| [<span data-ttu-id="ee4ac-113">**entrer**</span><span class="sxs-lookup"><span data-stu-id="ee4ac-113">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md) |      | <span data-ttu-id="ee4ac-114">Contient une valeur hexBinary de 1 octet qui est utilisée pour différencier les cartes réseau par le même IHV.</span><span class="sxs-lookup"><span data-stu-id="ee4ac-114">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ee4ac-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee4ac-115">Requirements</span></span>



| <span data-ttu-id="ee4ac-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee4ac-116">Requirement</span></span> | <span data-ttu-id="ee4ac-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee4ac-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee4ac-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee4ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4ac-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee4ac-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee4ac-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee4ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4ac-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee4ac-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee4ac-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee4ac-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee4ac-123">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="ee4ac-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ee4ac-124">**FABRICANTS**</span><span class="sxs-lookup"><span data-stu-id="ee4ac-124">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="ee4ac-125">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="ee4ac-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ee4ac-126">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ee4ac-126">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




