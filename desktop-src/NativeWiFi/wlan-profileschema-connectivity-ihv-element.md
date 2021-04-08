---
description: Contient des paramètres de connectivité liés aux IHV. Elle n’est pas implémentée actuellement.
ms.assetid: d943e82a-8660-4df7-8f5c-42ed83f17313
title: Élément Connectivity (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 257addbcbd721e5930405e3954dcb348f367af93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753749"
---
# <a name="connectivity-ihv-element"></a><span data-ttu-id="0e9db-104">Élément Connectivity (IHV)</span><span class="sxs-lookup"><span data-stu-id="0e9db-104">connectivity (IHV) Element</span></span>

<span data-ttu-id="0e9db-105">L’élément Connectivity (IHV) contient des paramètres de connectivité liés aux IHV.</span><span class="sxs-lookup"><span data-stu-id="0e9db-105">The connectivity (IHV) element contains IHV-related connectivity settings.</span></span> <span data-ttu-id="0e9db-106">Elle n’est pas implémentée actuellement.</span><span class="sxs-lookup"><span data-stu-id="0e9db-106">It is not currently implemented.</span></span>

<span data-ttu-id="0e9db-107">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0e9db-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="0e9db-108">L’élément est défini par l’élément [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0e9db-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9db-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e9db-109">Requirements</span></span>



| <span data-ttu-id="0e9db-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e9db-110">Requirement</span></span> | <span data-ttu-id="0e9db-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e9db-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e9db-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e9db-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9db-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e9db-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e9db-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e9db-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9db-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e9db-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e9db-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e9db-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e9db-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="0e9db-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0e9db-118">**FABRICANTS**</span><span class="sxs-lookup"><span data-stu-id="0e9db-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="0e9db-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="0e9db-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0e9db-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="0e9db-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




