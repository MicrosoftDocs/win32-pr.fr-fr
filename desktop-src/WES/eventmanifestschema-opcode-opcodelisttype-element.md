---
title: Élément opcode (OpcodeListType)
description: Contient une valeur numérique qui identifie l’activité ou un point dans une activité que l’application a exécutée lorsqu’elle a déclenché l’événement (par exemple, initialisation ou fermeture).
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- OpCode, élément EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106027"
---
# <a name="opcode-opcodelisttype-element"></a><span data-ttu-id="ee397-104">Élément opcode (OpcodeListType)</span><span class="sxs-lookup"><span data-stu-id="ee397-104">opcode (OpcodeListType) Element</span></span>

<span data-ttu-id="ee397-105">Contient une valeur numérique qui identifie l’activité ou un point dans une activité que l’application a exécutée lorsqu’elle a déclenché l’événement (par exemple, initialisation ou fermeture).</span><span class="sxs-lookup"><span data-stu-id="ee397-105">Contains a numeric value that identifies the activity or a point within an activity that the application was performing when it raised the event (for example, initialization or closing).</span></span>

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

<span data-ttu-id="ee397-106">L’élément **opcode** est défini par le type complexe [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ee397-106">The **opcode** element is defined by the [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee397-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee397-107">Requirements</span></span>



| <span data-ttu-id="ee397-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee397-108">Requirement</span></span> | <span data-ttu-id="ee397-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee397-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee397-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee397-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ee397-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee397-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee397-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee397-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ee397-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee397-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee397-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee397-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee397-115">**Éléments parents**</span><span class="sxs-lookup"><span data-stu-id="ee397-115">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="ee397-116">**OpCodes (TaskType)**</span><span class="sxs-lookup"><span data-stu-id="ee397-116">**opcodes (TaskType)**</span></span>](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[<span data-ttu-id="ee397-117">**OpCodes (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="ee397-117">**opcodes (ProviderType)**</span></span>](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="ee397-118">**OpCodes (type de données)**</span><span class="sxs-lookup"><span data-stu-id="ee397-118">**opcodes (MetadataType)**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





