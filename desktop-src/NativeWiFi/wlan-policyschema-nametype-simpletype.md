---
description: Définit un type de chaîne pour le nom ou la description d’un profil de stratégie de réseau local sans fil.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: Type simple nameType (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542984"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="ad69f-103">Type simple nameType (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="ad69f-103">nameType Simple Type (LAN_policy)</span></span>

<span data-ttu-id="ad69f-104">Le type simple nameType définit un type de chaîne pour le nom ou la description d’un profil de stratégie de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="ad69f-104">The nameType simple type defines a string type for either the name or the description of a wireless LAN policy profile.</span></span> <span data-ttu-id="ad69f-105">Les noms et les descriptions sont des chaînes d’au moins un caractère et de 255 caractères de long.</span><span class="sxs-lookup"><span data-stu-id="ad69f-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
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
```

## <a name="requirements"></a><span data-ttu-id="ad69f-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad69f-106">Requirements</span></span>



| <span data-ttu-id="ad69f-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad69f-107">Requirement</span></span> | <span data-ttu-id="ad69f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad69f-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad69f-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad69f-109">Minimum supported client</span></span><br/> | <span data-ttu-id="ad69f-110">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad69f-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ad69f-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad69f-111">Minimum supported server</span></span><br/> | <span data-ttu-id="ad69f-112">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad69f-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




