---
title: Type complexe XmlTypeListType
description: Définit une liste de types de sortie que le service utilise pour déterminer comment restituer un type de données d’entrée.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- XmlTypeListType type complexe EventLog
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317294"
---
# <a name="xmltypelisttype-complex-type"></a><span data-ttu-id="04ee8-104">Type complexe XmlTypeListType</span><span class="sxs-lookup"><span data-stu-id="04ee8-104">XmlTypeListType Complex Type</span></span>

<span data-ttu-id="04ee8-105">Définit une liste de types de sortie que le service utilise pour déterminer comment restituer un type de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="04ee8-105">Defines a list output types that the service uses to determine how to render an input data type.</span></span>

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension
                        base="XmlType"
                    >
                        <xs:attribute name="name"
                            type="QName"
                            use="required"
                         />
                        <xs:attribute name="value"
                            type="string"
                            use="required"
                         />
                        <xs:attribute name="symbol"
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="04ee8-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="04ee8-106">Child elements</span></span>



| <span data-ttu-id="04ee8-107">Élément</span><span class="sxs-lookup"><span data-stu-id="04ee8-107">Element</span></span>                                                                | <span data-ttu-id="04ee8-108">Type</span><span class="sxs-lookup"><span data-stu-id="04ee8-108">Type</span></span> | <span data-ttu-id="04ee8-109">Description</span><span class="sxs-lookup"><span data-stu-id="04ee8-109">Description</span></span>                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [<span data-ttu-id="04ee8-110">**xmlType**</span><span class="sxs-lookup"><span data-stu-id="04ee8-110">**xmlType**</span></span>](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | <span data-ttu-id="04ee8-111">Définit un type XML.</span><span class="sxs-lookup"><span data-stu-id="04ee8-111">Defines an XML type.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="04ee8-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="04ee8-112">Attributes</span></span>



| <span data-ttu-id="04ee8-113">Nom</span><span class="sxs-lookup"><span data-stu-id="04ee8-113">Name</span></span>   | <span data-ttu-id="04ee8-114">Type</span><span class="sxs-lookup"><span data-stu-id="04ee8-114">Type</span></span>                                                              | <span data-ttu-id="04ee8-115">Description</span><span class="sxs-lookup"><span data-stu-id="04ee8-115">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04ee8-116">name</span><span class="sxs-lookup"><span data-stu-id="04ee8-116">name</span></span>   | <span data-ttu-id="04ee8-117">**QName**</span><span class="sxs-lookup"><span data-stu-id="04ee8-117">**QName**</span></span>                                                         | <span data-ttu-id="04ee8-118">Nom du type de sortie.</span><span class="sxs-lookup"><span data-stu-id="04ee8-118">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="04ee8-119">symbole</span><span class="sxs-lookup"><span data-stu-id="04ee8-119">symbol</span></span> | [<span data-ttu-id="04ee8-120">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="04ee8-120">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="04ee8-121">Symbole à utiliser pour référencer le type de sortie dans votre application.</span><span class="sxs-lookup"><span data-stu-id="04ee8-121">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="04ee8-122">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le type de sortie dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="04ee8-122">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="04ee8-123">value</span><span class="sxs-lookup"><span data-stu-id="04ee8-123">value</span></span>  | <span data-ttu-id="04ee8-124">string</span><span class="sxs-lookup"><span data-stu-id="04ee8-124">string</span></span>                                                            | <span data-ttu-id="04ee8-125">Valeur entière qui identifie de façon unique le type de sortie dans la liste des types de sortie que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="04ee8-125">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="04ee8-126">Notes</span><span class="sxs-lookup"><span data-stu-id="04ee8-126">Remarks</span></span>

<span data-ttu-id="04ee8-127">Le \\ fichier include \\Winmeta.xml, inclus dans le SDK Windows, contient une liste de types de sortie prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="04ee8-127">The \\Include\\Winmeta.xml file, which is included in the Windows SDK, contains a list of predefined output types.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ee8-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04ee8-128">Requirements</span></span>



| <span data-ttu-id="04ee8-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04ee8-129">Requirement</span></span> | <span data-ttu-id="04ee8-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="04ee8-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="04ee8-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04ee8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="04ee8-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04ee8-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04ee8-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04ee8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="04ee8-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04ee8-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





