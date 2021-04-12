---
description: Définit un type de chaîne pour les identificateurs de jeu de service (SSID).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: Type simple networkNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6b6463644e1bd174be256d51b34ae2ae4ad9ce07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952804"
---
# <a name="networknametype-simple-type"></a><span data-ttu-id="a4097-103">Type simple networkNameType</span><span class="sxs-lookup"><span data-stu-id="a4097-103">networkNameType Simple Type</span></span>

<span data-ttu-id="a4097-104">Le type simple networkNameType définit un type de chaîne pour les identificateurs de jeu de service (SSID).</span><span class="sxs-lookup"><span data-stu-id="a4097-104">The networkNameType simple type defines a string type for service set identifiers (SSIDs).</span></span> <span data-ttu-id="a4097-105">Un SSID est une chaîne d’au moins un caractère et de 32 caractères au maximum.</span><span class="sxs-lookup"><span data-stu-id="a4097-105">A SSID is a string that is at least one character long and at most 32 characters long.</span></span>

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="a4097-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4097-106">Requirements</span></span>



| <span data-ttu-id="a4097-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4097-107">Requirement</span></span> | <span data-ttu-id="a4097-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4097-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4097-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4097-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a4097-110">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4097-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4097-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4097-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a4097-112">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4097-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




