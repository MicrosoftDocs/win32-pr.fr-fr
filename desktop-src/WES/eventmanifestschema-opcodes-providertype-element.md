---
title: OpCodes (ProviderType), élément
description: Définit une liste d’OpCodes que vous pouvez utiliser pour regrouper des événements au sein d’une tâche. | OpCodes (ProviderType), élément
ms.assetid: 28f67c43-053d-42e6-81eb-2353cc3898af
keywords:
- OpCodes, élément EventLog
topic_type:
- apiref
api_name:
- opcodes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b551f1158e58cb671a0fb872f73eabec1b29de33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531479"
---
# <a name="opcodes-providertype-element"></a><span data-ttu-id="84bf5-105">OpCodes (ProviderType), élément</span><span class="sxs-lookup"><span data-stu-id="84bf5-105">opcodes (ProviderType) Element</span></span>

<span data-ttu-id="84bf5-106">Définit une liste d’OpCodes que vous pouvez utiliser pour regrouper des événements au sein d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="84bf5-106">Defines a list of opcodes that you can use to group events within a task.</span></span>

``` syntax
<xs:element name="opcodes"
    type="OpcodeListType"
 />
```

<span data-ttu-id="84bf5-107">L’élément **OpCodes** est défini par le type complexe [**ProviderType**](eventmanifestschema-providertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="84bf5-107">The **opcodes** element is defined by the [**ProviderType**](eventmanifestschema-providertype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="84bf5-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84bf5-108">Requirements</span></span>



| <span data-ttu-id="84bf5-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84bf5-109">Requirement</span></span> | <span data-ttu-id="84bf5-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="84bf5-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="84bf5-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84bf5-111">Minimum supported client</span></span><br/> | <span data-ttu-id="84bf5-112">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84bf5-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="84bf5-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84bf5-113">Minimum supported server</span></span><br/> | <span data-ttu-id="84bf5-114">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84bf5-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84bf5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84bf5-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="84bf5-116">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="84bf5-116">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="84bf5-117">**fournisseur (EventsType)**</span><span class="sxs-lookup"><span data-stu-id="84bf5-117">**provider (EventsType)**</span></span>](eventmanifestschema-provider-eventstype-element.md)
</dt> </dl>

 

 





