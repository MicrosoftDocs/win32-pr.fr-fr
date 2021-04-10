---
title: Type complexe principalsType
description: Définit l’élément enfant de l’élément principal.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- Planificateur de tâches de type complexe principalsType
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56cd26a4dff31ce86b218e5a4a2662d678327625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941765"
---
# <a name="principalstype-complex-type"></a><span data-ttu-id="a674f-104">Type complexe principalsType</span><span class="sxs-lookup"><span data-stu-id="a674f-104">principalsType Complex Type</span></span>

<span data-ttu-id="a674f-105">Définit l’élément enfant de l’élément [**principal**](taskschedulerschema-principals-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a674f-105">Defines the child element for the [**Principals**](taskschedulerschema-principals-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a674f-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a674f-106">Child elements</span></span>



| <span data-ttu-id="a674f-107">Élément</span><span class="sxs-lookup"><span data-stu-id="a674f-107">Element</span></span>                                                                  | <span data-ttu-id="a674f-108">Type</span><span class="sxs-lookup"><span data-stu-id="a674f-108">Type</span></span>                                                                   | <span data-ttu-id="a674f-109">Description</span><span class="sxs-lookup"><span data-stu-id="a674f-109">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="a674f-110">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="a674f-110">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="a674f-111">**principalType**</span><span class="sxs-lookup"><span data-stu-id="a674f-111">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="a674f-112">Spécifie les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="a674f-112">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a674f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a674f-113">Requirements</span></span>



| <span data-ttu-id="a674f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a674f-114">Requirement</span></span> | <span data-ttu-id="a674f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a674f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a674f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a674f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a674f-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a674f-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a674f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a674f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a674f-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a674f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





