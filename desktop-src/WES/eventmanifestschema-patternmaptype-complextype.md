---
title: Type complexe PatternMapType
description: Non utilisé. Définit un mappage entre deux expressions régulières. Une expression est utilisée pour rechercher une chaîne correspondante dans la chaîne de message, tandis que l’autre est utilisée pour modifier la chaîne avant que le service la replace dans la chaîne de message.
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- PatternMapType type complexe EventLog
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465758"
---
# <a name="patternmaptype-complex-type"></a><span data-ttu-id="71dcf-106">Type complexe PatternMapType</span><span class="sxs-lookup"><span data-stu-id="71dcf-106">PatternMapType Complex Type</span></span>

<span data-ttu-id="71dcf-107">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="71dcf-107">Not used.</span></span> <span data-ttu-id="71dcf-108">Définit un mappage entre deux expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="71dcf-108">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="71dcf-109">Une expression est utilisée pour rechercher une chaîne correspondante dans la chaîne de message, tandis que l’autre est utilisée pour modifier la chaîne avant que le service la replace dans la chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="71dcf-109">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="71dcf-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="71dcf-110">Child elements</span></span>



| <span data-ttu-id="71dcf-111">Élément</span><span class="sxs-lookup"><span data-stu-id="71dcf-111">Element</span></span>                                                       | <span data-ttu-id="71dcf-112">Type</span><span class="sxs-lookup"><span data-stu-id="71dcf-112">Type</span></span>                                                                               | <span data-ttu-id="71dcf-113">Description</span><span class="sxs-lookup"><span data-stu-id="71dcf-113">Description</span></span>                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71dcf-114">**canal**</span><span class="sxs-lookup"><span data-stu-id="71dcf-114">**map**</span></span>](eventmanifestschema-map-patternmaptype-element.md) | [<span data-ttu-id="71dcf-115">**PatternMapValueType**</span><span class="sxs-lookup"><span data-stu-id="71dcf-115">**PatternMapValueType**</span></span>](eventmanifestschema-patternmapvaluetype-complextype.md) | <span data-ttu-id="71dcf-116">Définit les expressions régulières utilisées pour rechercher une chaîne correspondante dans la chaîne de message et la modifier.</span><span class="sxs-lookup"><span data-stu-id="71dcf-116">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="71dcf-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="71dcf-117">Attributes</span></span>



| <span data-ttu-id="71dcf-118">Nom</span><span class="sxs-lookup"><span data-stu-id="71dcf-118">Name</span></span>   | <span data-ttu-id="71dcf-119">Type</span><span class="sxs-lookup"><span data-stu-id="71dcf-119">Type</span></span>                                                              | <span data-ttu-id="71dcf-120">Description</span><span class="sxs-lookup"><span data-stu-id="71dcf-120">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71dcf-121">format</span><span class="sxs-lookup"><span data-stu-id="71dcf-121">format</span></span> | <span data-ttu-id="71dcf-122">anyURI</span><span class="sxs-lookup"><span data-stu-id="71dcf-122">anyURI</span></span>                                                            | <span data-ttu-id="71dcf-123">Moteur d’expression régulière à utiliser.</span><span class="sxs-lookup"><span data-stu-id="71dcf-123">The regular expression engine to use.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="71dcf-124">name</span><span class="sxs-lookup"><span data-stu-id="71dcf-124">name</span></span>   | <span data-ttu-id="71dcf-125">**QName**</span><span class="sxs-lookup"><span data-stu-id="71dcf-125">**QName**</span></span>                                                         | <span data-ttu-id="71dcf-126">Nom de la carte de modèle.</span><span class="sxs-lookup"><span data-stu-id="71dcf-126">The name of the pattern map.</span></span> <span data-ttu-id="71dcf-127">Utilisez le nom dans un élément de données pour référencer les mappages.</span><span class="sxs-lookup"><span data-stu-id="71dcf-127">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="71dcf-128">symbole</span><span class="sxs-lookup"><span data-stu-id="71dcf-128">symbol</span></span> | [<span data-ttu-id="71dcf-129">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="71dcf-129">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="71dcf-130">Symbole à utiliser pour référencer les mappages dans votre application.</span><span class="sxs-lookup"><span data-stu-id="71dcf-130">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="71dcf-131">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le mappage dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="71dcf-131">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="71dcf-132">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="71dcf-132">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="71dcf-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71dcf-133">Requirements</span></span>



| <span data-ttu-id="71dcf-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71dcf-134">Requirement</span></span> | <span data-ttu-id="71dcf-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="71dcf-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="71dcf-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71dcf-136">Minimum supported client</span></span><br/> | <span data-ttu-id="71dcf-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71dcf-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="71dcf-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71dcf-138">Minimum supported server</span></span><br/> | <span data-ttu-id="71dcf-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71dcf-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





