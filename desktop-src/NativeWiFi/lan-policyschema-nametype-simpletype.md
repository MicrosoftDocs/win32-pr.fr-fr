---
description: Définit un type de chaîne pour le nom ou la description d’un profil de stratégie de réseau local câblé.
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
title: type simple nameType (LAN_policy)
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
ms.openlocfilehash: 702ee6340fa3d03217c884a48625d3a38be4ad9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952393"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="36a5b-103">type simple nameType (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="36a5b-103">nameType simple type (LAN_policy)</span></span>

<span data-ttu-id="36a5b-104">Le type simple nameType définit un type de chaîne pour le nom ou la description d’un profil de stratégie de réseau local câblé.</span><span class="sxs-lookup"><span data-stu-id="36a5b-104">The nameType simple type defines a string type for either the name or the description of a wired LAN policy profile.</span></span> <span data-ttu-id="36a5b-105">Les noms et les descriptions sont des chaînes d’au moins un caractère et de 255 caractères de long.</span><span class="sxs-lookup"><span data-stu-id="36a5b-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="36a5b-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36a5b-106">Requirements</span></span>



| <span data-ttu-id="36a5b-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36a5b-107">Requirement</span></span> | <span data-ttu-id="36a5b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="36a5b-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="36a5b-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36a5b-109">Minimum supported client</span></span><br/> | <span data-ttu-id="36a5b-110">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36a5b-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="36a5b-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36a5b-111">Minimum supported server</span></span><br/> | <span data-ttu-id="36a5b-112">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36a5b-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




