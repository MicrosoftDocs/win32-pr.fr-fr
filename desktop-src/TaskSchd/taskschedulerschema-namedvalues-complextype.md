---
title: Type complexe namedValues
description: Définit une paire nom-valeur dans laquelle le nom est associé à la valeur.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- Planificateur de tâches de type complexe namedValues
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742164"
---
# <a name="namedvalues-complex-type"></a><span data-ttu-id="3daf0-104">Type complexe namedValues</span><span class="sxs-lookup"><span data-stu-id="3daf0-104">namedValues Complex Type</span></span>

<span data-ttu-id="3daf0-105">Définit une paire nom-valeur dans laquelle le nom est associé à la valeur.</span><span class="sxs-lookup"><span data-stu-id="3daf0-105">Defines a name-value pair in which the name is associated with the value.</span></span>

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3daf0-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3daf0-106">Child elements</span></span>



| <span data-ttu-id="3daf0-107">Élément</span><span class="sxs-lookup"><span data-stu-id="3daf0-107">Element</span></span>                                                        | <span data-ttu-id="3daf0-108">Type</span><span class="sxs-lookup"><span data-stu-id="3daf0-108">Type</span></span>                                                | <span data-ttu-id="3daf0-109">Description</span><span class="sxs-lookup"><span data-stu-id="3daf0-109">Description</span></span>                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="3daf0-110">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3daf0-110">**Value**</span></span>](taskschedulerschema-value-namedvalues-element.md) | [<span data-ttu-id="3daf0-111">**namedValue**</span><span class="sxs-lookup"><span data-stu-id="3daf0-111">**namedValue**</span></span>](schema-namedvalue-complextype.md) | <span data-ttu-id="3daf0-112">Spécifie la valeur associée à un nom dans une paire nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="3daf0-112">Specifies the value that is associated with a name in a name-value pair.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3daf0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3daf0-113">Requirements</span></span>



| <span data-ttu-id="3daf0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3daf0-114">Requirement</span></span> | <span data-ttu-id="3daf0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3daf0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3daf0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3daf0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3daf0-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3daf0-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3daf0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3daf0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3daf0-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3daf0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





