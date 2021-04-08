---
description: Contient une valeur hexBinary de 1 octet qui est utilisée pour différencier les cartes réseau créées par le même IHV.
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: Élément type (OUIHeader)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 12637e5a70409166e5a31aa0fc98f4df1b9f6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866029"
---
# <a name="type-ouiheader-element"></a><span data-ttu-id="b157a-103">Élément type (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="b157a-103">type (OUIHeader) Element</span></span>

<span data-ttu-id="b157a-104">L’élément type (OUIHeader) contient une valeur hexBinary de 1 octet qui est utilisée pour différencier les cartes réseau effectuées par le même IHV.</span><span class="sxs-lookup"><span data-stu-id="b157a-104">The type (OUIHeader) element contains a 1-byte hexBinary that is used to differentiate between NICs made by the same IHV.</span></span>

<span data-ttu-id="b157a-105">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b157a-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="b157a-106">L’élément est défini par l’élément [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b157a-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b157a-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b157a-107">Requirements</span></span>



| <span data-ttu-id="b157a-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b157a-108">Requirement</span></span> | <span data-ttu-id="b157a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b157a-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b157a-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b157a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="b157a-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b157a-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b157a-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b157a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="b157a-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b157a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b157a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b157a-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="b157a-115">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="b157a-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b157a-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="b157a-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="b157a-117">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="b157a-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b157a-118">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="b157a-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




