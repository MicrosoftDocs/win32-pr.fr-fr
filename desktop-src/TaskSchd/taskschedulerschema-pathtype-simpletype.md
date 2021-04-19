---
title: Type simple pathType
description: Définit le nombre minimal et maximal de caractères pour une chaîne qui définit un chemin d’accès de fichier.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- Planificateur de tâches de type simple pathType
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516100"
---
# <a name="pathtype-simple-type"></a><span data-ttu-id="56ef1-104">Type simple pathType</span><span class="sxs-lookup"><span data-stu-id="56ef1-104">pathType Simple Type</span></span>

<span data-ttu-id="56ef1-105">Définit le nombre minimal et maximal de caractères pour une chaîne qui définit un chemin d’accès de fichier.</span><span class="sxs-lookup"><span data-stu-id="56ef1-105">Defines the minimum and maximum number of characters for a string that defines a file path.</span></span> <span data-ttu-id="56ef1-106">Le chemin d’accès ne peut pas être une chaîne vide et doit être inférieur à 260 caractères.</span><span class="sxs-lookup"><span data-stu-id="56ef1-106">The path cannot be an empty string, and must be less than 260 characters.</span></span>

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="56ef1-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56ef1-107">Requirements</span></span>



| <span data-ttu-id="56ef1-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56ef1-108">Requirement</span></span> | <span data-ttu-id="56ef1-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="56ef1-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="56ef1-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56ef1-110">Minimum supported client</span></span><br/> | <span data-ttu-id="56ef1-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56ef1-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="56ef1-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56ef1-112">Minimum supported server</span></span><br/> | <span data-ttu-id="56ef1-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56ef1-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





