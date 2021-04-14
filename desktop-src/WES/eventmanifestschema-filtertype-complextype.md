---
title: FilterType (type complexe)
description: Définit un filtre de données utilisé par une session pour filtrer les événements en fonction des données d’événement.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- FilterType, type complexe EventLog
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467014"
---
# <a name="filtertype-complex-type"></a><span data-ttu-id="94a5f-104">FilterType (type complexe)</span><span class="sxs-lookup"><span data-stu-id="94a5f-104">FilterType Complex Type</span></span>

<span data-ttu-id="94a5f-105">Définit un filtre de données utilisé par une session pour filtrer les événements en fonction des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="94a5f-105">Defines a data filter that a session uses to filter events based on event data.</span></span>

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="94a5f-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="94a5f-106">Attributes</span></span>



| <span data-ttu-id="94a5f-107">Nom</span><span class="sxs-lookup"><span data-stu-id="94a5f-107">Name</span></span>    | <span data-ttu-id="94a5f-108">Type</span><span class="sxs-lookup"><span data-stu-id="94a5f-108">Type</span></span>                                                              | <span data-ttu-id="94a5f-109">Description</span><span class="sxs-lookup"><span data-stu-id="94a5f-109">Description</span></span>                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a5f-110">message</span><span class="sxs-lookup"><span data-stu-id="94a5f-110">message</span></span> | [<span data-ttu-id="94a5f-111">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="94a5f-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="94a5f-112">Description localisée du filtre.</span><span class="sxs-lookup"><span data-stu-id="94a5f-112">The localized description for the filter.</span></span> <span data-ttu-id="94a5f-113">La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.</span><span class="sxs-lookup"><span data-stu-id="94a5f-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                   |
| <span data-ttu-id="94a5f-114">name</span><span class="sxs-lookup"><span data-stu-id="94a5f-114">name</span></span>    | <span data-ttu-id="94a5f-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="94a5f-115">**QName**</span></span>                                                         | <span data-ttu-id="94a5f-116">Nom qui identifie le filtre.</span><span class="sxs-lookup"><span data-stu-id="94a5f-116">A name that identifies the filter.</span></span><br/>                                                                                                                                                                                                    |
| <span data-ttu-id="94a5f-117">symbole</span><span class="sxs-lookup"><span data-stu-id="94a5f-117">symbol</span></span>  | [<span data-ttu-id="94a5f-118">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="94a5f-118">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="94a5f-119">Symbole à utiliser pour référencer le filtre dans votre application.</span><span class="sxs-lookup"><span data-stu-id="94a5f-119">The symbol to use to reference the filter in your application.</span></span> <span data-ttu-id="94a5f-120">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le filtre dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="94a5f-120">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the filter in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="94a5f-121">tid</span><span class="sxs-lookup"><span data-stu-id="94a5f-121">tid</span></span>     | <span data-ttu-id="94a5f-122">token</span><span class="sxs-lookup"><span data-stu-id="94a5f-122">token</span></span>                                                             | <span data-ttu-id="94a5f-123">Identificateur de modèle qui décrit les données de filtre que la session transmet au fournisseur lorsqu’elle active le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="94a5f-123">A template identifier that describes the filter data that the session passes to the provider when it enables the provider.</span></span><br/>                                                                                                            |
| <span data-ttu-id="94a5f-124">value</span><span class="sxs-lookup"><span data-stu-id="94a5f-124">value</span></span>   | [<span data-ttu-id="94a5f-125">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="94a5f-125">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="94a5f-126">Valeur entière qui identifie de façon unique le filtre dans la liste des filtres que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="94a5f-126">An integer value that uniquely identifies the filter within the list of filters that you define.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="94a5f-127">version</span><span class="sxs-lookup"><span data-stu-id="94a5f-127">version</span></span> | [<span data-ttu-id="94a5f-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="94a5f-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="94a5f-129">Valeur entière qui identifie cette version du filtre.</span><span class="sxs-lookup"><span data-stu-id="94a5f-129">An integer value that identifies this version of the filter.</span></span> <span data-ttu-id="94a5f-130">S’il n’est pas spécifié, la valeur est zéro.</span><span class="sxs-lookup"><span data-stu-id="94a5f-130">If not specified, the value is zero.</span></span><br/>                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="94a5f-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94a5f-131">Requirements</span></span>



| <span data-ttu-id="94a5f-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94a5f-132">Requirement</span></span> | <span data-ttu-id="94a5f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="94a5f-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="94a5f-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94a5f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="94a5f-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94a5f-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="94a5f-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94a5f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="94a5f-137">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94a5f-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





