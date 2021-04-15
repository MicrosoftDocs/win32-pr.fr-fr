---
title: Type complexe ValueMapValueType
description: Définit le mappage entre une valeur entière et une valeur de chaîne. | Type complexe ValueMapValueType
ms.assetid: 8fd3b3ed-5b62-4e2e-b6f9-8e1bf6d83a35
keywords:
- ValueMapValueType type complexe EventLog
topic_type:
- apiref
api_name:
- ValueMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 197eb7e402068f541dc5a385eca14a631de2488c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393915"
---
# <a name="valuemapvaluetype-complex-type"></a><span data-ttu-id="cfab5-105">Type complexe ValueMapValueType</span><span class="sxs-lookup"><span data-stu-id="cfab5-105">ValueMapValueType Complex Type</span></span>

<span data-ttu-id="cfab5-106">Définit le mappage entre une valeur entière et une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="cfab5-106">Defines the mapping between an integer value and a string value.</span></span>

``` syntax
<xs:complexType name="ValueMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="cfab5-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="cfab5-107">Attributes</span></span>



| <span data-ttu-id="cfab5-108">Nom</span><span class="sxs-lookup"><span data-stu-id="cfab5-108">Name</span></span>    | <span data-ttu-id="cfab5-109">Type</span><span class="sxs-lookup"><span data-stu-id="cfab5-109">Type</span></span>                                                              | <span data-ttu-id="cfab5-110">Description</span><span class="sxs-lookup"><span data-stu-id="cfab5-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfab5-111">message</span><span class="sxs-lookup"><span data-stu-id="cfab5-111">message</span></span> | [<span data-ttu-id="cfab5-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="cfab5-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="cfab5-113">Valeur de chaîne localisée à laquelle la valeur entière est mappée.</span><span class="sxs-lookup"><span data-stu-id="cfab5-113">The localized string value to which the integer value maps.</span></span> <span data-ttu-id="cfab5-114">La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.</span><span class="sxs-lookup"><span data-stu-id="cfab5-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                              |
| <span data-ttu-id="cfab5-115">symbole</span><span class="sxs-lookup"><span data-stu-id="cfab5-115">symbol</span></span>  | [<span data-ttu-id="cfab5-116">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="cfab5-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="cfab5-117">Symbole à utiliser pour référencer la carte dans votre application.</span><span class="sxs-lookup"><span data-stu-id="cfab5-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="cfab5-118">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le mappage dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="cfab5-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="cfab5-119">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="cfab5-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="cfab5-120">value</span><span class="sxs-lookup"><span data-stu-id="cfab5-120">value</span></span>   | [<span data-ttu-id="cfab5-121">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="cfab5-121">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="cfab5-122">Valeur entière à mapper à la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="cfab5-122">The integer value to map to the string value.</span></span><br/>                                                                                                                                                                                                                                                       |



## <a name="requirements"></a><span data-ttu-id="cfab5-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfab5-123">Requirements</span></span>



| <span data-ttu-id="cfab5-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfab5-124">Requirement</span></span> | <span data-ttu-id="cfab5-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfab5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cfab5-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfab5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cfab5-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfab5-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cfab5-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfab5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cfab5-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfab5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





