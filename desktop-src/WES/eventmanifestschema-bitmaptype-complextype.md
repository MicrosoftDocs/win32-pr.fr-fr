---
title: Type complexe BitMapType
description: Définit une liste de mappages nom/valeur entre les valeurs de bits et les valeurs de chaîne.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- BitMapType type complexe EventLog
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466974"
---
# <a name="bitmaptype-complex-type"></a><span data-ttu-id="66c9e-104">Type complexe BitMapType</span><span class="sxs-lookup"><span data-stu-id="66c9e-104">BitMapType Complex Type</span></span>

<span data-ttu-id="66c9e-105">Définit une liste de mappages nom/valeur entre les valeurs de bits et les valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="66c9e-105">Defines a list of name/value mappings between bit values and string values.</span></span>

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="66c9e-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="66c9e-106">Child elements</span></span>



| <span data-ttu-id="66c9e-107">Élément</span><span class="sxs-lookup"><span data-stu-id="66c9e-107">Element</span></span>                                                   | <span data-ttu-id="66c9e-108">Type</span><span class="sxs-lookup"><span data-stu-id="66c9e-108">Type</span></span>                                                                       | <span data-ttu-id="66c9e-109">Description</span><span class="sxs-lookup"><span data-stu-id="66c9e-109">Description</span></span>                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="66c9e-110">**canal**</span><span class="sxs-lookup"><span data-stu-id="66c9e-110">**map**</span></span>](eventmanifestschema-map-bitmaptype-element.md) | [<span data-ttu-id="66c9e-111">**BitMapValueType**</span><span class="sxs-lookup"><span data-stu-id="66c9e-111">**BitMapValueType**</span></span>](eventmanifestschema-bitmapvaluetype-complextype.md) | <span data-ttu-id="66c9e-112">Définit le mappage entre une valeur de bit et une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="66c9e-112">Defines the mapping between a bit value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="66c9e-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="66c9e-113">Attributes</span></span>



| <span data-ttu-id="66c9e-114">Nom</span><span class="sxs-lookup"><span data-stu-id="66c9e-114">Name</span></span>   | <span data-ttu-id="66c9e-115">Type</span><span class="sxs-lookup"><span data-stu-id="66c9e-115">Type</span></span>                                                              | <span data-ttu-id="66c9e-116">Description</span><span class="sxs-lookup"><span data-stu-id="66c9e-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66c9e-117">name</span><span class="sxs-lookup"><span data-stu-id="66c9e-117">name</span></span>   | <span data-ttu-id="66c9e-118">string</span><span class="sxs-lookup"><span data-stu-id="66c9e-118">string</span></span>                                                            | <span data-ttu-id="66c9e-119">Nom de l'image bitmap.</span><span class="sxs-lookup"><span data-stu-id="66c9e-119">The name of the bitmap.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="66c9e-120">symbole</span><span class="sxs-lookup"><span data-stu-id="66c9e-120">symbol</span></span> | [<span data-ttu-id="66c9e-121">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="66c9e-121">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="66c9e-122">Symbole à utiliser pour référencer les mappages dans votre application.</span><span class="sxs-lookup"><span data-stu-id="66c9e-122">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="66c9e-123">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le mappage dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="66c9e-123">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="66c9e-124">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="66c9e-124">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="66c9e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66c9e-125">Requirements</span></span>



| <span data-ttu-id="66c9e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66c9e-126">Requirement</span></span> | <span data-ttu-id="66c9e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="66c9e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="66c9e-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66c9e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66c9e-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66c9e-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="66c9e-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66c9e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66c9e-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66c9e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





