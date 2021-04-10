---
title: Type complexe InputTypeListType
description: Définit une liste de types d’entrée.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- InputTypeListType type complexe EventLog
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106036"
---
# <a name="inputtypelisttype-complex-type"></a><span data-ttu-id="46357-104">Type complexe InputTypeListType</span><span class="sxs-lookup"><span data-stu-id="46357-104">InputTypeListType Complex Type</span></span>

<span data-ttu-id="46357-105">Définit une liste de types d’entrée.</span><span class="sxs-lookup"><span data-stu-id="46357-105">Defines a list of input types.</span></span>

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="46357-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="46357-106">Child elements</span></span>



| <span data-ttu-id="46357-107">Élément</span><span class="sxs-lookup"><span data-stu-id="46357-107">Element</span></span>                                                                | <span data-ttu-id="46357-108">Type</span><span class="sxs-lookup"><span data-stu-id="46357-108">Type</span></span>                                                           | <span data-ttu-id="46357-109">Description</span><span class="sxs-lookup"><span data-stu-id="46357-109">Description</span></span>                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="46357-110">**InType**</span><span class="sxs-lookup"><span data-stu-id="46357-110">**inType**</span></span>](eventmanifestschema-intype-inputtypelisttype-element.md) | [<span data-ttu-id="46357-111">**InputType**</span><span class="sxs-lookup"><span data-stu-id="46357-111">**InputType**</span></span>](eventmanifestschema-inputtype-complextype.md) | <span data-ttu-id="46357-112">Définit un type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="46357-112">Defines an input type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="46357-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46357-113">Requirements</span></span>



| <span data-ttu-id="46357-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46357-114">Requirement</span></span> | <span data-ttu-id="46357-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="46357-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46357-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46357-116">Minimum supported client</span></span><br/> | <span data-ttu-id="46357-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46357-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46357-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46357-118">Minimum supported server</span></span><br/> | <span data-ttu-id="46357-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46357-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





