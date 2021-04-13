---
title: Type complexe DataType (Journal des événements Windows)
description: Définit un élément de données.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- Type de données type complexe EventLog
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317398"
---
# <a name="datatype-complex-type"></a><span data-ttu-id="fc423-104">Type complexe DataType</span><span class="sxs-lookup"><span data-stu-id="fc423-104">DataType Complex Type</span></span>

<span data-ttu-id="fc423-105">Définit un élément de données.</span><span class="sxs-lookup"><span data-stu-id="fc423-105">Defines a data item.</span></span>

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="fc423-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="fc423-106">Attributes</span></span>



| <span data-ttu-id="fc423-107">Nom</span><span class="sxs-lookup"><span data-stu-id="fc423-107">Name</span></span> | <span data-ttu-id="fc423-108">Type</span><span class="sxs-lookup"><span data-stu-id="fc423-108">Type</span></span>   | <span data-ttu-id="fc423-109">Description</span><span class="sxs-lookup"><span data-stu-id="fc423-109">Description</span></span>                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc423-110">Nom</span><span class="sxs-lookup"><span data-stu-id="fc423-110">Name</span></span> | <span data-ttu-id="fc423-111">string</span><span class="sxs-lookup"><span data-stu-id="fc423-111">string</span></span> | <span data-ttu-id="fc423-112">Nom d’un élément de données qui a été défini dans le modèle (consultez le type complexe [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="fc423-112">The name of a data item that was defined in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |
| <span data-ttu-id="fc423-113">Type</span><span class="sxs-lookup"><span data-stu-id="fc423-113">Type</span></span> | <span data-ttu-id="fc423-114">QName</span><span class="sxs-lookup"><span data-stu-id="fc423-114">QName</span></span>  | <span data-ttu-id="fc423-115">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="fc423-115">Not used.</span></span><br/>                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="fc423-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fc423-116">Remarks</span></span>

<span data-ttu-id="fc423-117">L’élément de données peut être un élément de données de niveau supérieur ou un élément de données dans une structure.</span><span class="sxs-lookup"><span data-stu-id="fc423-117">The data item can be a top-level data item or a data item in a structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc423-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc423-118">Requirements</span></span>



| <span data-ttu-id="fc423-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc423-119">Requirement</span></span> | <span data-ttu-id="fc423-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc423-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc423-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc423-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fc423-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc423-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc423-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc423-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fc423-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc423-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





