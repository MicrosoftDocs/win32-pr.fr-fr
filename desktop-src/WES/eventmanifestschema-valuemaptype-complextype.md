---
title: Type complexe ValueMapType
description: Définit une liste de mappages nom/valeur entre les valeurs entières et les valeurs de chaîne.
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- ValueMapType type complexe EventLog
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28fde51466ba506802c8dbc5379f1628fd943fa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739716"
---
# <a name="valuemaptype-complex-type"></a><span data-ttu-id="bedaa-104">Type complexe ValueMapType</span><span class="sxs-lookup"><span data-stu-id="bedaa-104">ValueMapType Complex Type</span></span>

<span data-ttu-id="bedaa-105">Définit une liste de mappages nom/valeur entre les valeurs entières et les valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="bedaa-105">Defines a list of name/value mappings between integer values and string values.</span></span>

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="bedaa-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bedaa-106">Child elements</span></span>



| <span data-ttu-id="bedaa-107">Élément</span><span class="sxs-lookup"><span data-stu-id="bedaa-107">Element</span></span>                                                     | <span data-ttu-id="bedaa-108">Type</span><span class="sxs-lookup"><span data-stu-id="bedaa-108">Type</span></span>                                                                           | <span data-ttu-id="bedaa-109">Description</span><span class="sxs-lookup"><span data-stu-id="bedaa-109">Description</span></span>                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="bedaa-110">**canal**</span><span class="sxs-lookup"><span data-stu-id="bedaa-110">**map**</span></span>](eventmanifestschema-map-valuemaptype-element.md) | [<span data-ttu-id="bedaa-111">**ValueMapValueType**</span><span class="sxs-lookup"><span data-stu-id="bedaa-111">**ValueMapValueType**</span></span>](eventmanifestschema-valuemapvaluetype-complextype.md) | <span data-ttu-id="bedaa-112">Définit le mappage entre une valeur entière et une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="bedaa-112">Defines the mapping between an integer value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="bedaa-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="bedaa-113">Attributes</span></span>



| <span data-ttu-id="bedaa-114">Nom</span><span class="sxs-lookup"><span data-stu-id="bedaa-114">Name</span></span>   | <span data-ttu-id="bedaa-115">Type</span><span class="sxs-lookup"><span data-stu-id="bedaa-115">Type</span></span>                                                              | <span data-ttu-id="bedaa-116">Description</span><span class="sxs-lookup"><span data-stu-id="bedaa-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bedaa-117">name</span><span class="sxs-lookup"><span data-stu-id="bedaa-117">name</span></span>   | <span data-ttu-id="bedaa-118">string</span><span class="sxs-lookup"><span data-stu-id="bedaa-118">string</span></span>                                                            | <span data-ttu-id="bedaa-119">Nom de la carte de valeur.</span><span class="sxs-lookup"><span data-stu-id="bedaa-119">The name of the value map.</span></span> <span data-ttu-id="bedaa-120">Utilisez le nom dans un élément de données pour référencer les mappages.</span><span class="sxs-lookup"><span data-stu-id="bedaa-120">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                     |
| <span data-ttu-id="bedaa-121">symbole</span><span class="sxs-lookup"><span data-stu-id="bedaa-121">symbol</span></span> | [<span data-ttu-id="bedaa-122">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="bedaa-122">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="bedaa-123">Symbole à utiliser pour référencer les mappages dans votre application.</span><span class="sxs-lookup"><span data-stu-id="bedaa-123">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="bedaa-124">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le mappage dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="bedaa-124">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="bedaa-125">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="bedaa-125">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bedaa-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bedaa-126">Requirements</span></span>



| <span data-ttu-id="bedaa-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bedaa-127">Requirement</span></span> | <span data-ttu-id="bedaa-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bedaa-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bedaa-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bedaa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bedaa-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bedaa-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bedaa-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bedaa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bedaa-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bedaa-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





