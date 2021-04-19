---
description: Contient une hexBinary de 3 octets qui identifie le IHV.
ms.assetid: 0b2e73fb-df3a-48c4-b38d-970c37de46eb
title: Élément OUI (OUIHeader)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUI
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 49a9cceffb308c64c8d1addf7c257b422751661f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538848"
---
# <a name="oui-ouiheader-element"></a><span data-ttu-id="fbf9a-103">Élément OUI (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="fbf9a-103">OUI (OUIHeader) Element</span></span>

<span data-ttu-id="fbf9a-104">L’élément OUI (OUIHeader) contient un élément hexBinary de 3 octets qui identifie le IHV.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-104">The OUI (OUIHeader) element contains a 3 byte hexBinary that identifies the IHV.</span></span>

<span data-ttu-id="fbf9a-105">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="fbf9a-106">L’élément est défini par l’élément [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf9a-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf9a-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbf9a-107">Requirements</span></span>



| <span data-ttu-id="fbf9a-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbf9a-108">Requirement</span></span> | <span data-ttu-id="fbf9a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbf9a-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fbf9a-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf9a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf9a-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbf9a-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fbf9a-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf9a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf9a-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbf9a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbf9a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbf9a-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="fbf9a-115">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="fbf9a-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fbf9a-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="fbf9a-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="fbf9a-117">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="fbf9a-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fbf9a-118">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="fbf9a-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




