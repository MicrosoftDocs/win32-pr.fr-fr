---
title: Type simple versionType
description: Définit un modèle qui spécifie une version d’une tâche.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- Planificateur de tâches de type simple versionType
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317170"
---
# <a name="versiontype-simple-type"></a><span data-ttu-id="55953-104">Type simple versionType</span><span class="sxs-lookup"><span data-stu-id="55953-104">versionType Simple Type</span></span>

<span data-ttu-id="55953-105">Définit un modèle qui spécifie une version d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="55953-105">Defines a pattern that specifies a version of a task.</span></span>

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="55953-106">Modèles</span><span class="sxs-lookup"><span data-stu-id="55953-106">Patterns</span></span>

<span data-ttu-id="55953-107">Le type simple **versionType** est une **chaîne** qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="55953-107">The **versionType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\d+(\.\d+){1,3}`

    <span data-ttu-id="55953-108">Double suivi d’un, deux ou trois doubles.</span><span class="sxs-lookup"><span data-stu-id="55953-108">A double followed by one, two, or three doubles.</span></span> <span data-ttu-id="55953-109">Par exemple, 1,2 ou 1.2.3.</span><span class="sxs-lookup"><span data-stu-id="55953-109">For example, 1.2, or 1.2.3.</span></span>

## <a name="requirements"></a><span data-ttu-id="55953-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55953-110">Requirements</span></span>



| <span data-ttu-id="55953-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55953-111">Requirement</span></span> | <span data-ttu-id="55953-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="55953-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55953-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55953-113">Minimum supported client</span></span><br/> | <span data-ttu-id="55953-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55953-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="55953-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55953-115">Minimum supported server</span></span><br/> | <span data-ttu-id="55953-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55953-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





