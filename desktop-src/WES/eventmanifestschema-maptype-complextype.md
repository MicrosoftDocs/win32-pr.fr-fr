---
title: Type complexe MapType
description: Définit une liste de paires nom/valeur.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- MapType type complexe EventLog
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740389"
---
# <a name="maptype-complex-type"></a><span data-ttu-id="6b0a5-104">Type complexe MapType</span><span class="sxs-lookup"><span data-stu-id="6b0a5-104">MapType Complex Type</span></span>

<span data-ttu-id="6b0a5-105">Définit une liste de paires nom/valeur.</span><span class="sxs-lookup"><span data-stu-id="6b0a5-105">Defines a list of name/value pairs.</span></span>

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6b0a5-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6b0a5-106">Child elements</span></span>



| <span data-ttu-id="6b0a5-107">Élément</span><span class="sxs-lookup"><span data-stu-id="6b0a5-107">Element</span></span>                                                          | <span data-ttu-id="6b0a5-108">Type</span><span class="sxs-lookup"><span data-stu-id="6b0a5-108">Type</span></span>                                                                 | <span data-ttu-id="6b0a5-109">Description</span><span class="sxs-lookup"><span data-stu-id="6b0a5-109">Description</span></span>                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b0a5-110">**Pixels**</span><span class="sxs-lookup"><span data-stu-id="6b0a5-110">**bitMap**</span></span>](eventmanifestschema-bitmap-maptype-element.md)     | [<span data-ttu-id="6b0a5-111">**BitMapType**</span><span class="sxs-lookup"><span data-stu-id="6b0a5-111">**BitMapType**</span></span>](eventmanifestschema-bitmaptype-complextype.md)     | <span data-ttu-id="6b0a5-112">Définit une liste de paires nom/valeur qui mappent les valeurs de bit et les valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="6b0a5-112">Defines a list of name/value pairs that map bit values and string values.</span></span><br/>     |
| [<span data-ttu-id="6b0a5-113">**valueMap**</span><span class="sxs-lookup"><span data-stu-id="6b0a5-113">**valueMap**</span></span>](eventmanifestschema-valuemap-maptype-element.md) | [<span data-ttu-id="6b0a5-114">**ValueMapType**</span><span class="sxs-lookup"><span data-stu-id="6b0a5-114">**ValueMapType**</span></span>](eventmanifestschema-valuemaptype-complextype.md) | <span data-ttu-id="6b0a5-115">Définit une liste de paires nom/valeur qui mappent des valeurs entières et des valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="6b0a5-115">Defines a list of name/value pairs that map integer values and string values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6b0a5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6b0a5-116">Remarks</span></span>

<span data-ttu-id="6b0a5-117">En général, vous créez des mappages pour fournir des valeurs de chaîne énumérées pour les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="6b0a5-117">Typically, you create maps to provide enumerated string values for event data.</span></span>

## <a name="examples"></a><span data-ttu-id="6b0a5-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="6b0a5-118">Examples</span></span>

<span data-ttu-id="6b0a5-119">L’exemple suivant montre comment spécifier un mappage de valeur et une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="6b0a5-119">The following example shows how to specify a value map and bitmap.</span></span>


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a><span data-ttu-id="6b0a5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b0a5-120">Requirements</span></span>



| <span data-ttu-id="6b0a5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b0a5-121">Requirement</span></span> | <span data-ttu-id="6b0a5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b0a5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6b0a5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b0a5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0a5-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b0a5-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6b0a5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b0a5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0a5-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b0a5-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





