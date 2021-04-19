---
title: Élément Binary (TemplateItemType)
description: Contient les données binaires fournies par l’API du journal des événements.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- élément binaire EventLog
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517320"
---
# <a name="binary-templateitemtype-element"></a><span data-ttu-id="042a9-104">Élément Binary (TemplateItemType)</span><span class="sxs-lookup"><span data-stu-id="042a9-104">binary (TemplateItemType) Element</span></span>

<span data-ttu-id="042a9-105">Contient les données binaires fournies par l’API du [Journal des événements](/windows/desktop/EventLog/event-logging) .</span><span class="sxs-lookup"><span data-stu-id="042a9-105">Contains the binary data that is supplied by the [Event Log](/windows/desktop/EventLog/event-logging) API.</span></span>

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="042a9-106">L’élément **binaire** est défini par le type complexe [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="042a9-106">The **binary** element is defined by the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="042a9-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="042a9-107">Attributes</span></span>



| <span data-ttu-id="042a9-108">Nom</span><span class="sxs-lookup"><span data-stu-id="042a9-108">Name</span></span> | <span data-ttu-id="042a9-109">Type</span><span class="sxs-lookup"><span data-stu-id="042a9-109">Type</span></span>   | <span data-ttu-id="042a9-110">Description</span><span class="sxs-lookup"><span data-stu-id="042a9-110">Description</span></span>                                          |
|------|--------|------------------------------------------------------|
| <span data-ttu-id="042a9-111">name</span><span class="sxs-lookup"><span data-stu-id="042a9-111">name</span></span> | <span data-ttu-id="042a9-112">string</span><span class="sxs-lookup"><span data-stu-id="042a9-112">string</span></span> | <span data-ttu-id="042a9-113">Nom associé aux données binaires.</span><span class="sxs-lookup"><span data-stu-id="042a9-113">The name associated with the binary data.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="042a9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="042a9-114">Requirements</span></span>



| <span data-ttu-id="042a9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="042a9-115">Requirement</span></span> | <span data-ttu-id="042a9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="042a9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="042a9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="042a9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="042a9-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="042a9-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="042a9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="042a9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="042a9-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="042a9-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="042a9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="042a9-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="042a9-122">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="042a9-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="042a9-123">**modèle (TemplateListType)**</span><span class="sxs-lookup"><span data-stu-id="042a9-123">**template (TemplateListType)**</span></span>](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

