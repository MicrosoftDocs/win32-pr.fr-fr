---
title: Type complexe TemplateListType
description: Définit une liste de modèles qui spécifient les données à inclure avec les événements. | Type complexe TemplateListType
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- TemplateListType type complexe EventLog
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60b31fd88d05f00229f27a616a29483a29bd49d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761779"
---
# <a name="templatelisttype-complex-type"></a><span data-ttu-id="640cd-105">Type complexe TemplateListType</span><span class="sxs-lookup"><span data-stu-id="640cd-105">TemplateListType Complex Type</span></span>

<span data-ttu-id="640cd-106">Définit une liste de modèles qui spécifient les données à inclure avec les événements.</span><span class="sxs-lookup"><span data-stu-id="640cd-106">Defines a list of templates that specify the data to include with the events.</span></span>

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="640cd-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="640cd-107">Child elements</span></span>



| <span data-ttu-id="640cd-108">Élément</span><span class="sxs-lookup"><span data-stu-id="640cd-108">Element</span></span>                                                                   | <span data-ttu-id="640cd-109">Type</span><span class="sxs-lookup"><span data-stu-id="640cd-109">Type</span></span>                                                                         | <span data-ttu-id="640cd-110">Description</span><span class="sxs-lookup"><span data-stu-id="640cd-110">Description</span></span>                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="640cd-111">**modèle**</span><span class="sxs-lookup"><span data-stu-id="640cd-111">**template**</span></span>](eventmanifestschema-template-templatelisttype-element.md) | [<span data-ttu-id="640cd-112">**TemplateItemType**</span><span class="sxs-lookup"><span data-stu-id="640cd-112">**TemplateItemType**</span></span>](eventmanifestschema-templateitemtype-complextype.md) | <span data-ttu-id="640cd-113">Modèle qui définit les données à inclure avec un événement.</span><span class="sxs-lookup"><span data-stu-id="640cd-113">A template that defines the data to include with an event.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="640cd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="640cd-114">Requirements</span></span>



| <span data-ttu-id="640cd-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="640cd-115">Requirement</span></span> | <span data-ttu-id="640cd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="640cd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="640cd-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="640cd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="640cd-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="640cd-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="640cd-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="640cd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="640cd-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="640cd-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





