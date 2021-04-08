---
title: Type complexe BitMapValueType
description: Définit le mappage entre une valeur de bit et une valeur de chaîne. | Type complexe BitMapValueType
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- BitMapValueType type complexe EventLog
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953646"
---
# <a name="bitmapvaluetype-complex-type"></a><span data-ttu-id="87812-105">Type complexe BitMapValueType</span><span class="sxs-lookup"><span data-stu-id="87812-105">BitMapValueType Complex Type</span></span>

<span data-ttu-id="87812-106">Définit le mappage entre une valeur de bit et une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="87812-106">Defines the mapping between a bit value and a string value.</span></span>

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
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

## <a name="attributes"></a><span data-ttu-id="87812-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="87812-107">Attributes</span></span>



| <span data-ttu-id="87812-108">Nom</span><span class="sxs-lookup"><span data-stu-id="87812-108">Name</span></span>    | <span data-ttu-id="87812-109">Type</span><span class="sxs-lookup"><span data-stu-id="87812-109">Type</span></span>                                                              | <span data-ttu-id="87812-110">Description</span><span class="sxs-lookup"><span data-stu-id="87812-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87812-111">message</span><span class="sxs-lookup"><span data-stu-id="87812-111">message</span></span> | [<span data-ttu-id="87812-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="87812-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="87812-113">Valeur de chaîne localisée dans laquelle la valeur de bit est mappée.</span><span class="sxs-lookup"><span data-stu-id="87812-113">The localized string value to which the bit value maps.</span></span> <span data-ttu-id="87812-114">La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.</span><span class="sxs-lookup"><span data-stu-id="87812-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                  |
| <span data-ttu-id="87812-115">symbole</span><span class="sxs-lookup"><span data-stu-id="87812-115">symbol</span></span>  | [<span data-ttu-id="87812-116">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="87812-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="87812-117">Symbole à utiliser pour référencer la carte dans votre application.</span><span class="sxs-lookup"><span data-stu-id="87812-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="87812-118">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le mappage dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="87812-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="87812-119">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="87812-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="87812-120">value</span><span class="sxs-lookup"><span data-stu-id="87812-120">value</span></span>   | [<span data-ttu-id="87812-121">**HexInt32Type**</span><span class="sxs-lookup"><span data-stu-id="87812-121">**HexInt32Type**</span></span>](eventmanifestschema-hex32type-simpletype.md)  | <span data-ttu-id="87812-122">Valeur de bit à mapper à la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="87812-122">The bit value to map to the string value.</span></span> <span data-ttu-id="87812-123">Vous devez spécifier un nombre hexadécimal pour lequel un seul bit est défini.</span><span class="sxs-lookup"><span data-stu-id="87812-123">You must specify a hexadecimal number that has a single bit set.</span></span><br/>                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="87812-124">Notes</span><span class="sxs-lookup"><span data-stu-id="87812-124">Remarks</span></span>

<span data-ttu-id="87812-125">Mappe une valeur hexadécimale (le nombre doit être précédé de 0x) avec un seul bit défini sur un nom.</span><span class="sxs-lookup"><span data-stu-id="87812-125">Maps a hexadecimal value (the number must be preceded by 0x) with a single bit set to a name.</span></span>

## <a name="requirements"></a><span data-ttu-id="87812-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87812-126">Requirements</span></span>



| <span data-ttu-id="87812-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87812-127">Requirement</span></span> | <span data-ttu-id="87812-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="87812-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87812-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87812-129">Minimum supported client</span></span><br/> | <span data-ttu-id="87812-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87812-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="87812-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87812-131">Minimum supported server</span></span><br/> | <span data-ttu-id="87812-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87812-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





