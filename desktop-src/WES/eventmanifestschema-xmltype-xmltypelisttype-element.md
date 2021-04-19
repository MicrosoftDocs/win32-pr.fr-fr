---
title: Élément xmlType (XmlTypeListType)
description: Définit un type XML.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- élément de journal de l’élément xmlType
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511360"
---
# <a name="xmltype-xmltypelisttype-element"></a><span data-ttu-id="6e8dd-104">Élément xmlType (XmlTypeListType)</span><span class="sxs-lookup"><span data-stu-id="6e8dd-104">xmlType (XmlTypeListType) Element</span></span>

<span data-ttu-id="6e8dd-105">Définit un type XML.</span><span class="sxs-lookup"><span data-stu-id="6e8dd-105">Defines an XML type.</span></span>

``` syntax
<xs:element name="xmlType">
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
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="6e8dd-106">L’élément **xmlType** est défini par le type complexe [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8dd-106">The **xmlType** element is defined by the [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="6e8dd-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="6e8dd-107">Attributes</span></span>



| <span data-ttu-id="6e8dd-108">Nom</span><span class="sxs-lookup"><span data-stu-id="6e8dd-108">Name</span></span>   | <span data-ttu-id="6e8dd-109">Type</span><span class="sxs-lookup"><span data-stu-id="6e8dd-109">Type</span></span>      | <span data-ttu-id="6e8dd-110">Description</span><span class="sxs-lookup"><span data-stu-id="6e8dd-110">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8dd-111">name</span><span class="sxs-lookup"><span data-stu-id="6e8dd-111">name</span></span>   | <span data-ttu-id="6e8dd-112">**QName**</span><span class="sxs-lookup"><span data-stu-id="6e8dd-112">**QName**</span></span> | <span data-ttu-id="6e8dd-113">Nom du type de sortie.</span><span class="sxs-lookup"><span data-stu-id="6e8dd-113">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="6e8dd-114">symbole</span><span class="sxs-lookup"><span data-stu-id="6e8dd-114">symbol</span></span> | <span data-ttu-id="6e8dd-115">string</span><span class="sxs-lookup"><span data-stu-id="6e8dd-115">string</span></span>    | <span data-ttu-id="6e8dd-116">Symbole à utiliser pour référencer le type de sortie dans votre application.</span><span class="sxs-lookup"><span data-stu-id="6e8dd-116">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="6e8dd-117">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le type de sortie dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="6e8dd-117">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="6e8dd-118">value</span><span class="sxs-lookup"><span data-stu-id="6e8dd-118">value</span></span>  | <span data-ttu-id="6e8dd-119">string</span><span class="sxs-lookup"><span data-stu-id="6e8dd-119">string</span></span>    | <span data-ttu-id="6e8dd-120">Valeur entière qui identifie de façon unique le type de sortie dans la liste des types de sortie que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="6e8dd-120">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="6e8dd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e8dd-121">Requirements</span></span>



| <span data-ttu-id="6e8dd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e8dd-122">Requirement</span></span> | <span data-ttu-id="6e8dd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e8dd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6e8dd-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e8dd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6e8dd-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e8dd-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6e8dd-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e8dd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6e8dd-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e8dd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e8dd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e8dd-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e8dd-129">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="6e8dd-129">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="6e8dd-130">**xmlTypes (TypeListType)**</span><span class="sxs-lookup"><span data-stu-id="6e8dd-130">**xmlTypes (TypeListType)**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





