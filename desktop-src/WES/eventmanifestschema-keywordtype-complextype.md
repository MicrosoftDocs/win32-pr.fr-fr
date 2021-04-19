---
title: Type complexe KeywordType
description: Définit un mot clé qui identifie une catégorie d’événements. | Type complexe KeywordType
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- KeywordType type complexe EventLog
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106529244"
---
# <a name="keywordtype-complex-type"></a><span data-ttu-id="35c4b-105">Type complexe KeywordType</span><span class="sxs-lookup"><span data-stu-id="35c4b-105">KeywordType Complex Type</span></span>

<span data-ttu-id="35c4b-106">Définit un mot clé qui identifie une catégorie d’événements.</span><span class="sxs-lookup"><span data-stu-id="35c4b-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="35c4b-107">Un mot clé est une balise que vous attachez à un événement pour regrouper des événements en fonction de leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="35c4b-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="35c4b-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="35c4b-108">Attributes</span></span>



| <span data-ttu-id="35c4b-109">Nom</span><span class="sxs-lookup"><span data-stu-id="35c4b-109">Name</span></span>    | <span data-ttu-id="35c4b-110">Type</span><span class="sxs-lookup"><span data-stu-id="35c4b-110">Type</span></span>                                                              | <span data-ttu-id="35c4b-111">Description</span><span class="sxs-lookup"><span data-stu-id="35c4b-111">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c4b-112">masque</span><span class="sxs-lookup"><span data-stu-id="35c4b-112">mask</span></span>    | [<span data-ttu-id="35c4b-113">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="35c4b-113">**HexInt64Type**</span></span>](eventmanifestschema-hex64type-simpletype.md)  | <span data-ttu-id="35c4b-114">Masque de bits qui ne doit avoir qu’un seul bit défini.</span><span class="sxs-lookup"><span data-stu-id="35c4b-114">A bitmask that must have only a single bit set.</span></span> <span data-ttu-id="35c4b-115">Le bit représente une catégorie d’événements (par exemple, des événements de lecture ou des événements d’écriture).</span><span class="sxs-lookup"><span data-stu-id="35c4b-115">The bit represents a category of events (for example, read events or write events).</span></span> <span data-ttu-id="35c4b-116">Vous pouvez spécifier des valeurs de bit dans la plage comprise entre 0x0000000000000001 et 0x0000800000000000 (bits 0 à 47).</span><span class="sxs-lookup"><span data-stu-id="35c4b-116">You can specify bit values in the range from 0x0000000000000001 through 0x0000800000000000 (bits 0 through 47).</span></span><br/>                                                         |
| <span data-ttu-id="35c4b-117">message</span><span class="sxs-lookup"><span data-stu-id="35c4b-117">message</span></span> | [<span data-ttu-id="35c4b-118">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="35c4b-118">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="35c4b-119">Nom complet localisé du mot clé.</span><span class="sxs-lookup"><span data-stu-id="35c4b-119">The localized display name for the keyword.</span></span> <span data-ttu-id="35c4b-120">La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.</span><span class="sxs-lookup"><span data-stu-id="35c4b-120">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                                                                                       |
| <span data-ttu-id="35c4b-121">name</span><span class="sxs-lookup"><span data-stu-id="35c4b-121">name</span></span>    | <span data-ttu-id="35c4b-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="35c4b-122">**QName**</span></span>                                                         | <span data-ttu-id="35c4b-123">Nom du mot clé.</span><span class="sxs-lookup"><span data-stu-id="35c4b-123">The name of the keyword.</span></span> <span data-ttu-id="35c4b-124">Le nom doit être unique dans la liste des mots clés définis par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="35c4b-124">The name must be unique within the list of keywords that the provider defines.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="35c4b-125">symbole</span><span class="sxs-lookup"><span data-stu-id="35c4b-125">symbol</span></span>  | [<span data-ttu-id="35c4b-126">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="35c4b-126">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="35c4b-127">Symbole à utiliser pour référencer le mot clé dans votre application.</span><span class="sxs-lookup"><span data-stu-id="35c4b-127">The symbol to use to reference the keyword in your application.</span></span> <span data-ttu-id="35c4b-128">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le mot clé dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="35c4b-128">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the keyword in the header file that the compiler generates.</span></span> <span data-ttu-id="35c4b-129">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="35c4b-129">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="35c4b-130">Notes</span><span class="sxs-lookup"><span data-stu-id="35c4b-130">Remarks</span></span>

<span data-ttu-id="35c4b-131">Le fichier Winmeta.xml inclus dans le SDK Windows contient une liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="35c4b-131">The Winmeta.xml file that is included in the Windows SDK contains a list of keywords.</span></span> <span data-ttu-id="35c4b-132">Ces mots clés sont réservés et ne doivent pas être utilisés.</span><span class="sxs-lookup"><span data-stu-id="35c4b-132">These keywords are reserved and should not be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="35c4b-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35c4b-133">Requirements</span></span>



| <span data-ttu-id="35c4b-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35c4b-134">Requirement</span></span> | <span data-ttu-id="35c4b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="35c4b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35c4b-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35c4b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="35c4b-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35c4b-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="35c4b-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35c4b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="35c4b-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35c4b-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





