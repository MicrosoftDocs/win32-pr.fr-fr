---
title: Type complexe PatternMapValueType
description: Non utilisé. Définit les expressions régulières utilisées pour rechercher une chaîne correspondante dans la chaîne de message et la modifier.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- PatternMapValueType type complexe EventLog
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739732"
---
# <a name="patternmapvaluetype-complex-type"></a><span data-ttu-id="0f18e-105">Type complexe PatternMapValueType</span><span class="sxs-lookup"><span data-stu-id="0f18e-105">PatternMapValueType Complex Type</span></span>

<span data-ttu-id="0f18e-106">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="0f18e-106">Not used.</span></span> <span data-ttu-id="0f18e-107">Définit les expressions régulières utilisées pour rechercher une chaîne correspondante dans la chaîne de message et la modifier.</span><span class="sxs-lookup"><span data-stu-id="0f18e-107">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span>

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="0f18e-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="0f18e-108">Attributes</span></span>



| <span data-ttu-id="0f18e-109">Nom</span><span class="sxs-lookup"><span data-stu-id="0f18e-109">Name</span></span>  | <span data-ttu-id="0f18e-110">Type</span><span class="sxs-lookup"><span data-stu-id="0f18e-110">Type</span></span>   | <span data-ttu-id="0f18e-111">Description</span><span class="sxs-lookup"><span data-stu-id="0f18e-111">Description</span></span>                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f18e-112">name</span><span class="sxs-lookup"><span data-stu-id="0f18e-112">name</span></span>  | <span data-ttu-id="0f18e-113">string</span><span class="sxs-lookup"><span data-stu-id="0f18e-113">string</span></span> | <span data-ttu-id="0f18e-114">Expression régulière utilisée pour rechercher une chaîne correspondante dans la chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="0f18e-114">The regular expression used to find a matching string in the message string.</span></span><br/>                   |
| <span data-ttu-id="0f18e-115">value</span><span class="sxs-lookup"><span data-stu-id="0f18e-115">value</span></span> | <span data-ttu-id="0f18e-116">string</span><span class="sxs-lookup"><span data-stu-id="0f18e-116">string</span></span> | <span data-ttu-id="0f18e-117">Expression régulière utilisée pour modifier la chaîne correspondante trouvée dans la chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="0f18e-117">The regular expression used to alter the matching string that was found in the message string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0f18e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f18e-118">Requirements</span></span>



| <span data-ttu-id="0f18e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f18e-119">Requirement</span></span> | <span data-ttu-id="0f18e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f18e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f18e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f18e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f18e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f18e-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0f18e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f18e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f18e-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f18e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





