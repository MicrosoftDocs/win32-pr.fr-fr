---
title: Type complexe ComplexDataType
description: Définit une structure qui contient un ou plusieurs éléments de données.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- ComplexDataType type complexe EventLog
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512414"
---
# <a name="complexdatatype-complex-type"></a><span data-ttu-id="b977c-104">Type complexe ComplexDataType</span><span class="sxs-lookup"><span data-stu-id="b977c-104">ComplexDataType Complex Type</span></span>

<span data-ttu-id="b977c-105">Définit une structure qui contient un ou plusieurs éléments de données.</span><span class="sxs-lookup"><span data-stu-id="b977c-105">Defines a structure that contains one or more data items.</span></span>

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b977c-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b977c-106">Child elements</span></span>



| <span data-ttu-id="b977c-107">Élément</span><span class="sxs-lookup"><span data-stu-id="b977c-107">Element</span></span>                                                  | <span data-ttu-id="b977c-108">Type</span><span class="sxs-lookup"><span data-stu-id="b977c-108">Type</span></span>                                                      | <span data-ttu-id="b977c-109">Description</span><span class="sxs-lookup"><span data-stu-id="b977c-109">Description</span></span>                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b977c-110">**Métadonnée**</span><span class="sxs-lookup"><span data-stu-id="b977c-110">**Data**</span></span>](eventschema-data-complexdatatype-element.md) | [<span data-ttu-id="b977c-111">**DataType**</span><span class="sxs-lookup"><span data-stu-id="b977c-111">**DataType**</span></span>](eventschema-datafieldtype-complextype.md) | <span data-ttu-id="b977c-112">Liste des éléments de données de la structure.</span><span class="sxs-lookup"><span data-stu-id="b977c-112">The list of data items in the structure.</span></span> <span data-ttu-id="b977c-113">La liste des éléments se trouve dans le même ordre que celui défini dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="b977c-113">The list of items are in the same order as defined in the template.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="b977c-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="b977c-114">Attributes</span></span>



| <span data-ttu-id="b977c-115">Nom</span><span class="sxs-lookup"><span data-stu-id="b977c-115">Name</span></span> | <span data-ttu-id="b977c-116">Type</span><span class="sxs-lookup"><span data-stu-id="b977c-116">Type</span></span>   | <span data-ttu-id="b977c-117">Description</span><span class="sxs-lookup"><span data-stu-id="b977c-117">Description</span></span>                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b977c-118">Nom</span><span class="sxs-lookup"><span data-stu-id="b977c-118">Name</span></span> | <span data-ttu-id="b977c-119">string</span><span class="sxs-lookup"><span data-stu-id="b977c-119">string</span></span> | <span data-ttu-id="b977c-120">Nom de la structure.</span><span class="sxs-lookup"><span data-stu-id="b977c-120">The name of the structure.</span></span> <span data-ttu-id="b977c-121">Il s’agit du nom qui est spécifié lorsque vous avez défini la structure dans le modèle (consultez le type complexe [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="b977c-121">This is the name that is specified when you defined the structure in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b977c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b977c-122">Remarks</span></span>

<span data-ttu-id="b977c-123">La fonction [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) restitue le contenu d’une structure sous la forme d’un objet blob binaire ; la fonction ne rend pas les éléments de données individuels de la structure.</span><span class="sxs-lookup"><span data-stu-id="b977c-123">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders the contents of a structure as a binary blob; the function does not render the individual data items of the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b977c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b977c-124">Requirements</span></span>



| <span data-ttu-id="b977c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b977c-125">Requirement</span></span> | <span data-ttu-id="b977c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b977c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b977c-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b977c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b977c-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b977c-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b977c-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b977c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b977c-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b977c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





