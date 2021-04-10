---
title: Élément patternMap (PatternMapListType)
description: Définit un mappage entre deux expressions régulières. Une expression est utilisée pour rechercher une chaîne correspondante dans la chaîne de message, tandis que l’autre est utilisée pour modifier la chaîne avant que le service la replace dans la chaîne de message.
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- EventLog, élément patternMap
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032288"
---
# <a name="patternmap-patternmaplisttype-element"></a><span data-ttu-id="2053e-105">Élément patternMap (PatternMapListType)</span><span class="sxs-lookup"><span data-stu-id="2053e-105">patternMap (PatternMapListType) Element</span></span>

<span data-ttu-id="2053e-106">Définit un mappage entre deux expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="2053e-106">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="2053e-107">Une expression est utilisée pour rechercher une chaîne correspondante dans la chaîne de message, tandis que l’autre est utilisée pour modifier la chaîne avant que le service la replace dans la chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="2053e-107">One expression is used to find a matching string in the message string, and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

<span data-ttu-id="2053e-108">L’élément **patternMap** est défini par le type complexe [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2053e-108">The **patternMap** element is defined by the [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2053e-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2053e-109">Requirements</span></span>



| <span data-ttu-id="2053e-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2053e-110">Requirement</span></span> | <span data-ttu-id="2053e-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="2053e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2053e-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2053e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2053e-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2053e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2053e-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2053e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2053e-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2053e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2053e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2053e-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="2053e-117">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="2053e-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="2053e-118">**patternMaps (NamedQueryType)**</span><span class="sxs-lookup"><span data-stu-id="2053e-118">**patternMaps (NamedQueryType)**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





