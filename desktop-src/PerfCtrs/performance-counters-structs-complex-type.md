---
description: Définit une liste de structures qui contiennent des valeurs de compteur.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Type complexe structs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542941"
---
# <a name="structs-complex-type"></a><span data-ttu-id="da26d-103">Type complexe structs</span><span class="sxs-lookup"><span data-stu-id="da26d-103">structs Complex Type</span></span>

<span data-ttu-id="da26d-104">Définit une liste de structures qui contiennent des valeurs de compteur.</span><span class="sxs-lookup"><span data-stu-id="da26d-104">Defines a list of structures that contain counter values.</span></span>

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="da26d-105">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="da26d-105">Child elements</span></span>



| <span data-ttu-id="da26d-106">Élément</span><span class="sxs-lookup"><span data-stu-id="da26d-106">Element</span></span>    | <span data-ttu-id="da26d-107">Type</span><span class="sxs-lookup"><span data-stu-id="da26d-107">Type</span></span>                                                           | <span data-ttu-id="da26d-108">Description</span><span class="sxs-lookup"><span data-stu-id="da26d-108">Description</span></span>                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="da26d-109">**modélis**</span><span class="sxs-lookup"><span data-stu-id="da26d-109">**struct**</span></span> | [<span data-ttu-id="da26d-110">**homme : struct**</span><span class="sxs-lookup"><span data-stu-id="da26d-110">**man:struct**</span></span>](performance-counters-struct-complex-type.md) | <span data-ttu-id="da26d-111">Nom d’une structure qui contient des valeurs de compteur.</span><span class="sxs-lookup"><span data-stu-id="da26d-111">The name of a structure that contains counter values.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="da26d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da26d-112">Requirements</span></span>



| <span data-ttu-id="da26d-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da26d-113">Requirement</span></span> | <span data-ttu-id="da26d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="da26d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da26d-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da26d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="da26d-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da26d-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da26d-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da26d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="da26d-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da26d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




