---
title: Type simple LengthType
description: Définit un type de longueur utilisé pour spécifier le nombre d’octets ou de caractères dans un élément de données de longueur variable, tel que des données binaires ou une chaîne ANSI ou Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Journal des types simples LengthType
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317458"
---
# <a name="lengthtype-simple-type"></a><span data-ttu-id="7e9e0-104">Type simple LengthType</span><span class="sxs-lookup"><span data-stu-id="7e9e0-104">LengthType Simple Type</span></span>

<span data-ttu-id="7e9e0-105">Définit un type de longueur utilisé pour spécifier le nombre d’octets ou de caractères dans un élément de données de longueur variable, tel que des données binaires ou une chaîne ANSI ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-105">Defines a length type that is used to specify the number of bytes or characters in a variable length data item such as binary data or an ANSI or Unicode string.</span></span> <span data-ttu-id="7e9e0-106">La valeur peut être spécifiée en tant que valeur XS : unsignedShort ou en tant que chaîne qui fait référence au nom du nœud d’élément de données qui contient la valeur Short non signée.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsigned short value.</span></span>

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="7e9e0-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e9e0-107">Requirements</span></span>



| <span data-ttu-id="7e9e0-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e9e0-108">Requirement</span></span> | <span data-ttu-id="7e9e0-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e9e0-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e9e0-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e9e0-110">Minimum supported client</span></span><br/> | <span data-ttu-id="7e9e0-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e9e0-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7e9e0-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e9e0-112">Minimum supported server</span></span><br/> | <span data-ttu-id="7e9e0-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e9e0-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





