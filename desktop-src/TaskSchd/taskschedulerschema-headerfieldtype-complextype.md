---
title: Type complexe headerFieldType
description: Définit les éléments utilisés pour créer un champ d’en-tête dans un message électronique.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- Planificateur de tâches de type complexe headerFieldType
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512155"
---
# <a name="headerfieldtype-complex-type"></a><span data-ttu-id="63ef6-104">Type complexe headerFieldType</span><span class="sxs-lookup"><span data-stu-id="63ef6-104">headerFieldType Complex Type</span></span>

<span data-ttu-id="63ef6-105">Définit les éléments utilisés pour créer un champ d’en-tête dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="63ef6-105">Defines the elements that are used to create a header field in an email message.</span></span>

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="63ef6-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="63ef6-106">Child elements</span></span>



| <span data-ttu-id="63ef6-107">Élément</span><span class="sxs-lookup"><span data-stu-id="63ef6-107">Element</span></span>                                                            | <span data-ttu-id="63ef6-108">Type</span><span class="sxs-lookup"><span data-stu-id="63ef6-108">Type</span></span>                                                                    | <span data-ttu-id="63ef6-109">Description</span><span class="sxs-lookup"><span data-stu-id="63ef6-109">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="63ef6-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="63ef6-110">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="63ef6-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="63ef6-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="63ef6-112">Spécifie le nom du champ d’en-tête dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="63ef6-112">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="63ef6-113">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="63ef6-113">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="63ef6-114">**string**</span><span class="sxs-lookup"><span data-stu-id="63ef6-114">**string**</span></span>                                                              | <span data-ttu-id="63ef6-115">Spécifie la valeur d’un champ d’en-tête dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="63ef6-115">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="63ef6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63ef6-116">Requirements</span></span>



| <span data-ttu-id="63ef6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63ef6-117">Requirement</span></span> | <span data-ttu-id="63ef6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="63ef6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63ef6-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63ef6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="63ef6-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63ef6-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63ef6-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63ef6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="63ef6-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63ef6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





