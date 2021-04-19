---
title: Type complexe TypeListType
description: Définit les types utilisés dans le manifeste.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- TypeListType type complexe EventLog
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509736"
---
# <a name="typelisttype-complex-type"></a><span data-ttu-id="8bf69-104">Type complexe TypeListType</span><span class="sxs-lookup"><span data-stu-id="8bf69-104">TypeListType Complex Type</span></span>

<span data-ttu-id="8bf69-105">Définit les types utilisés dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="8bf69-105">Defines the types that are used in the manifest.</span></span>

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8bf69-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8bf69-106">Child elements</span></span>



| <span data-ttu-id="8bf69-107">Élément</span><span class="sxs-lookup"><span data-stu-id="8bf69-107">Element</span></span>                                                               | <span data-ttu-id="8bf69-108">Type</span><span class="sxs-lookup"><span data-stu-id="8bf69-108">Type</span></span>                                                                           | <span data-ttu-id="8bf69-109">Description</span><span class="sxs-lookup"><span data-stu-id="8bf69-109">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bf69-110">**intypés**</span><span class="sxs-lookup"><span data-stu-id="8bf69-110">**inTypes**</span></span>](eventmanifestschema-intypes-typelisttype-element.md)   | [<span data-ttu-id="8bf69-111">**InputTypeListType**</span><span class="sxs-lookup"><span data-stu-id="8bf69-111">**InputTypeListType**</span></span>](eventmanifestschema-inputtypelisttype-complextype.md) | <span data-ttu-id="8bf69-112">Définit une liste de types de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8bf69-112">Defines a list of input data types.</span></span><br/>                                                              |
| [<span data-ttu-id="8bf69-113">**xmlTypes**</span><span class="sxs-lookup"><span data-stu-id="8bf69-113">**xmlTypes**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md) | [<span data-ttu-id="8bf69-114">**XmlTypeListType**</span><span class="sxs-lookup"><span data-stu-id="8bf69-114">**XmlTypeListType**</span></span>](eventmanifestschema-xmltypelisttype-complextype.md)     | <span data-ttu-id="8bf69-115">Définit une liste de types de sortie que le service utilise pour déterminer comment restituer un type de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8bf69-115">Defines a list output types that the service uses to determine how to render an input data type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8bf69-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bf69-116">Requirements</span></span>



| <span data-ttu-id="8bf69-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bf69-117">Requirement</span></span> | <span data-ttu-id="8bf69-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bf69-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8bf69-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bf69-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf69-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bf69-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8bf69-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bf69-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf69-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bf69-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





