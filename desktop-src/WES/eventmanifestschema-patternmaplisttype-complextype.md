---
title: Type complexe PatternMapListType
description: Non utilisé. Définit une liste de paires d’expressions régulières utilisées pour modifier la chaîne de message.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- PatternMapListType type complexe EventLog
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d1bb655dcf13c70fb989756cb9f5716301934c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317098"
---
# <a name="patternmaplisttype-complex-type"></a><span data-ttu-id="005ca-105">Type complexe PatternMapListType</span><span class="sxs-lookup"><span data-stu-id="005ca-105">PatternMapListType Complex Type</span></span>

<span data-ttu-id="005ca-106">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="005ca-106">Not used.</span></span> <span data-ttu-id="005ca-107">Définit une liste de paires d’expressions régulières utilisées pour modifier la chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="005ca-107">Defines a list of regular expression pairs that are used to alter the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="005ca-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="005ca-108">Child elements</span></span>



| <span data-ttu-id="005ca-109">Élément</span><span class="sxs-lookup"><span data-stu-id="005ca-109">Element</span></span>                                                                         | <span data-ttu-id="005ca-110">Type</span><span class="sxs-lookup"><span data-stu-id="005ca-110">Type</span></span>                                                                     | <span data-ttu-id="005ca-111">Description</span><span class="sxs-lookup"><span data-stu-id="005ca-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="005ca-112">**patternMap**</span><span class="sxs-lookup"><span data-stu-id="005ca-112">**patternMap**</span></span>](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [<span data-ttu-id="005ca-113">**PatternMapType**</span><span class="sxs-lookup"><span data-stu-id="005ca-113">**PatternMapType**</span></span>](eventmanifestschema-patternmaptype-complextype.md) | <span data-ttu-id="005ca-114">Définit un mappage entre deux expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="005ca-114">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="005ca-115">Une expression est utilisée pour rechercher une chaîne correspondante dans la chaîne de message, tandis que l’autre est utilisée pour modifier la chaîne avant que le service la replace dans la chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="005ca-115">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span> <span data-ttu-id="005ca-116">Le premier mappage de modèle qui correspond à est utilisé et les autres modèles ne sont pas essayés.</span><span class="sxs-lookup"><span data-stu-id="005ca-116">The first pattern mapping that matches is used and other patterns are not tried.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="005ca-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="005ca-117">Requirements</span></span>



| <span data-ttu-id="005ca-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="005ca-118">Requirement</span></span> | <span data-ttu-id="005ca-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="005ca-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="005ca-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="005ca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="005ca-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="005ca-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="005ca-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="005ca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="005ca-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="005ca-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





