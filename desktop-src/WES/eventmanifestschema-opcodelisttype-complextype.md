---
title: Type complexe OpcodeListType
description: Définit une liste d’OpCodes utilisés pour identifier les opérations d’un composant de l’application.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- OpcodeListType type complexe EventLog
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dce0942ef0268f50b25987a6be0fd4fffeebd614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465182"
---
# <a name="opcodelisttype-complex-type"></a><span data-ttu-id="db9ef-104">Type complexe OpcodeListType</span><span class="sxs-lookup"><span data-stu-id="db9ef-104">OpcodeListType Complex Type</span></span>

<span data-ttu-id="db9ef-105">Définit une liste d’OpCodes utilisés pour identifier les opérations d’un composant de l’application.</span><span class="sxs-lookup"><span data-stu-id="db9ef-105">Defines a list of opcodes that are used to identify the operations of a component of the application.</span></span>

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="db9ef-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="db9ef-106">Child elements</span></span>



| <span data-ttu-id="db9ef-107">Élément</span><span class="sxs-lookup"><span data-stu-id="db9ef-107">Element</span></span>                                                             | <span data-ttu-id="db9ef-108">Type</span><span class="sxs-lookup"><span data-stu-id="db9ef-108">Type</span></span>                                                             | <span data-ttu-id="db9ef-109">Description</span><span class="sxs-lookup"><span data-stu-id="db9ef-109">Description</span></span>                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="db9ef-110">**OpCode**</span><span class="sxs-lookup"><span data-stu-id="db9ef-110">**opcode**</span></span>](eventmanifestschema-opcode-opcodelisttype-element.md) | [<span data-ttu-id="db9ef-111">**OpcodeType**</span><span class="sxs-lookup"><span data-stu-id="db9ef-111">**OpcodeType**</span></span>](eventmanifestschema-opcodetype-complextype.md) | <span data-ttu-id="db9ef-112">Définit une opération dans un composant de l’application.</span><span class="sxs-lookup"><span data-stu-id="db9ef-112">Defines an operation within a component of the application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="db9ef-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db9ef-113">Requirements</span></span>



| <span data-ttu-id="db9ef-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db9ef-114">Requirement</span></span> | <span data-ttu-id="db9ef-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="db9ef-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="db9ef-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db9ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db9ef-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db9ef-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="db9ef-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db9ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db9ef-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db9ef-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





