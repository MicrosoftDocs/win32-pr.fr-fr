---
title: Type complexe NamedQueryType
description: Non utilisé. Définit une liste de requêtes nommées qui interrogent la chaîne de message d’événement pour obtenir une valeur et effectuent une action spécifiée si elle est trouvée. | Type complexe NamedQueryType
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- NamedQueryType type complexe EventLog
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537217"
---
# <a name="namedquerytype-complex-type"></a><span data-ttu-id="231e1-106">Type complexe NamedQueryType</span><span class="sxs-lookup"><span data-stu-id="231e1-106">NamedQueryType Complex Type</span></span>

<span data-ttu-id="231e1-107">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="231e1-107">Not used.</span></span> <span data-ttu-id="231e1-108">Définit une liste de requêtes nommées qui interrogent la chaîne de message d’événement pour obtenir une valeur et effectuent une action spécifiée si elle est trouvée.</span><span class="sxs-lookup"><span data-stu-id="231e1-108">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span>

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="231e1-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="231e1-109">Child elements</span></span>



| <span data-ttu-id="231e1-110">Élément</span><span class="sxs-lookup"><span data-stu-id="231e1-110">Element</span></span>                                                                       | <span data-ttu-id="231e1-111">Type</span><span class="sxs-lookup"><span data-stu-id="231e1-111">Type</span></span>                                                                             | <span data-ttu-id="231e1-112">Description</span><span class="sxs-lookup"><span data-stu-id="231e1-112">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="231e1-113">**patternMaps**</span><span class="sxs-lookup"><span data-stu-id="231e1-113">**patternMaps**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md) | [<span data-ttu-id="231e1-114">**PatternMapListType**</span><span class="sxs-lookup"><span data-stu-id="231e1-114">**PatternMapListType**</span></span>](eventmanifestschema-patternmaplisttype-complextype.md) | <span data-ttu-id="231e1-115">Définit une liste de paires d’expressions régulières utilisées pour modifier la chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="231e1-115">Defines a list of regular expression pairs that are used to alter the message string.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="231e1-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="231e1-116">Examples</span></span>

<span data-ttu-id="231e1-117">L’exemple suivant montre comment utiliser l’élément [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="231e1-117">The following example shows how to use the [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) element.</span></span> <span data-ttu-id="231e1-118">Cet exemple prend le contenu de la chaîne de message et l’insère dans la chaîne https://www .*MessageString*. com.</span><span class="sxs-lookup"><span data-stu-id="231e1-118">This example takes the contents of the message string and inserts it into the string https://www.*messagestring*.com.</span></span> <span data-ttu-id="231e1-119">Il remplace ensuite la chaîne de message par le résultat.</span><span class="sxs-lookup"><span data-stu-id="231e1-119">It then replaces the message string with the result.</span></span> <span data-ttu-id="231e1-120">Par exemple, si la chaîne de message contient Microsoft, la requête remplacerait la chaîne de message Microsoft par https://www.Microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="231e1-120">For example, if the message string contained Microsoft, the query would replace the Microsoft message string with https://www.Microsoft.com.</span></span>


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a><span data-ttu-id="231e1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="231e1-121">Requirements</span></span>



| <span data-ttu-id="231e1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="231e1-122">Requirement</span></span> | <span data-ttu-id="231e1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="231e1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="231e1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="231e1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="231e1-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="231e1-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="231e1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="231e1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="231e1-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="231e1-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





