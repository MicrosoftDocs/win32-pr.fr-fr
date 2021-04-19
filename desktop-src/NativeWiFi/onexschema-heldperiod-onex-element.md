---
description: Spécifie la durée, en secondes, pendant laquelle un client ne tentera pas de nouveau l’authentification après l’échec d’une tentative d’authentification.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: Élément heldPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527637"
---
# <a name="heldperiod-onex-element"></a><span data-ttu-id="ac739-103">Élément heldPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="ac739-103">heldPeriod (OneX) Element</span></span>

<span data-ttu-id="ac739-104">L’élément heldPeriod (OneX) spécifie la durée, en secondes, pendant laquelle un client ne tentera pas de nouveau l’authentification après l’échec d’une tentative d’authentification.</span><span class="sxs-lookup"><span data-stu-id="ac739-104">The heldPeriod (OneX) element specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span>

<span data-ttu-id="ac739-105">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="ac739-105">This element is optional.</span></span> <span data-ttu-id="ac739-106">Quand heldPeriod n’est pas spécifié dans un profil, une valeur de 1 seconde est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ac739-106">When heldPeriod is not specified in a profile, a value of 1 second is used.</span></span>

<span data-ttu-id="ac739-107">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="ac739-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ac739-108">L’élément **heldPeriod** est défini par l’élément [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ac739-108">The **heldPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac739-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac739-109">Requirements</span></span>



| <span data-ttu-id="ac739-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac739-110">Requirement</span></span> | <span data-ttu-id="ac739-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac739-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ac739-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac739-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ac739-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac739-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ac739-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac739-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ac739-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac739-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac739-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac739-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="ac739-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="ac739-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ac739-118">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="ac739-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="ac739-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="ac739-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ac739-120">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="ac739-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




