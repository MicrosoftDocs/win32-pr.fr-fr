---
description: Spécifie la norme de réseau local sans fil 802,11 utilisée sur un réseau local sans fil.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Élément phyType (Connectivity)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519275"
---
# <a name="phytype-connectivity-element"></a><span data-ttu-id="6f808-103">Élément phyType (Connectivity)</span><span class="sxs-lookup"><span data-stu-id="6f808-103">phyType (connectivity) Element</span></span>

<span data-ttu-id="6f808-104">L’élément phyType (Connectivity) spécifie la norme de réseau local sans fil 802,11 utilisée sur un réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="6f808-104">The phyType (connectivity) element specifies the 802.11 wireless LAN standard used on a wireless LAN.</span></span>

<span data-ttu-id="6f808-105">Vous pouvez spécifier plusieurs **phyType** s.</span><span class="sxs-lookup"><span data-stu-id="6f808-105">You can specify multiple **phyType** s.</span></span> <span data-ttu-id="6f808-106">Si aucun **phyType** n’est spécifié, le profil peut être utilisé pour se connecter à n’importe quel **phyType**.</span><span class="sxs-lookup"><span data-stu-id="6f808-106">If no **phyType** is specified, the profile can be used to connect to any **phyType**.</span></span> <span data-ttu-id="6f808-107">La valeur « n » est uniquement prise en charge sur Windows Vista avec Service Pack 1 (SP1) et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6f808-107">The value "n" is only supported on Windows Vista with Service Pack 1 (SP1) and later versions of the operating system.</span></span>

<span data-ttu-id="6f808-108">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6f808-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="6f808-109">L’élément est défini par l’élément [**Connectivity**](wlan-profileschema-connectivity-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6f808-109">The element is defined by the [**connectivity**](wlan-profileschema-connectivity-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f808-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f808-110">Requirements</span></span>



| <span data-ttu-id="6f808-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f808-111">Requirement</span></span> | <span data-ttu-id="6f808-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f808-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6f808-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f808-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6f808-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f808-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6f808-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f808-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6f808-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f808-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f808-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f808-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f808-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="6f808-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6f808-119">**connectivité**</span><span class="sxs-lookup"><span data-stu-id="6f808-119">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

<span data-ttu-id="6f808-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="6f808-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6f808-121">**connectivité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="6f808-121">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




