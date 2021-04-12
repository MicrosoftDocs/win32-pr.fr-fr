---
title: Type simple nonEmptyStringType
description: Définit les valeurs utilisées pour une chaîne de texte non vide.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- Planificateur de tâches de type simple nonEmptyString
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384908"
---
# <a name="nonemptystringtype-simple-type"></a><span data-ttu-id="7913f-104">Type simple nonEmptyStringType</span><span class="sxs-lookup"><span data-stu-id="7913f-104">nonEmptyStringType Simple Type</span></span>

<span data-ttu-id="7913f-105">Définit les valeurs utilisées pour une chaîne de texte non vide.</span><span class="sxs-lookup"><span data-stu-id="7913f-105">Defines the values used for a non-empty string of text.</span></span>

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="7913f-106">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="7913f-106">Enumeration values</span></span>

<span data-ttu-id="7913f-107">Le type simple **nonEmptyString** définit la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="7913f-107">The **nonEmptyString** simple type defines the following value.</span></span>



| <span data-ttu-id="7913f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7913f-108">Value</span></span> | <span data-ttu-id="7913f-109">Description</span><span class="sxs-lookup"><span data-stu-id="7913f-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="7913f-110">1</span><span class="sxs-lookup"><span data-stu-id="7913f-110">1</span></span>     | <span data-ttu-id="7913f-111">La chaîne contient au moins un caractère.</span><span class="sxs-lookup"><span data-stu-id="7913f-111">The string contains at least one character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7913f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7913f-112">Requirements</span></span>



| <span data-ttu-id="7913f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7913f-113">Requirement</span></span> | <span data-ttu-id="7913f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7913f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7913f-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7913f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7913f-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7913f-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7913f-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7913f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7913f-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7913f-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





