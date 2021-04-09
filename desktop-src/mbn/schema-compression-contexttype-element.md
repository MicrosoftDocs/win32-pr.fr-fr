---
description: Spécifie si la compression sera utilisée au niveau de la liaison de données pour l’en-tête et le transfert de données.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Élément compression (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862762"
---
# <a name="compression-contexttype-element"></a><span data-ttu-id="f9579-103">Élément compression (contextType)</span><span class="sxs-lookup"><span data-stu-id="f9579-103">Compression (contextType) Element</span></span>

<span data-ttu-id="f9579-104">L’élément **compression (ContextType)** spécifie si la compression est utilisée au niveau de la liaison de données pour l’en-tête et le transfert de données.</span><span class="sxs-lookup"><span data-stu-id="f9579-104">The **Compression (contextType)** element specifies if compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="f9579-105">Cet élément peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f9579-105">This element can be one of the following values.</span></span>

| <span data-ttu-id="f9579-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9579-106">Value</span></span>     | <span data-ttu-id="f9579-107">Signification</span><span class="sxs-lookup"><span data-stu-id="f9579-107">Meaning</span></span>                       |
|-----------|-------------------------------|
| <span data-ttu-id="f9579-108">RENDRE</span><span class="sxs-lookup"><span data-stu-id="f9579-108">"ENABLE"</span></span>  | <span data-ttu-id="f9579-109">La compression sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="f9579-109">Compression will be used.</span></span>     |
| <span data-ttu-id="f9579-110">DÉSACTIVE</span><span class="sxs-lookup"><span data-stu-id="f9579-110">"DISABLE"</span></span> | <span data-ttu-id="f9579-111">La compression n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="f9579-111">Compression will not be used.</span></span> |



 

<span data-ttu-id="f9579-112">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="f9579-112">This element is optional.</span></span> <span data-ttu-id="f9579-113">Si cet élément n’est pas spécifié, le système haut débit mobile n’utilise pas la compression.</span><span class="sxs-lookup"><span data-stu-id="f9579-113">If this element is not specified, then the Mobile Broadband system will not use compression.</span></span>

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="f9579-114">L’élément **compression** est défini par le type complexe [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f9579-114">The **Compression** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9579-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9579-115">Requirements</span></span>



| <span data-ttu-id="f9579-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9579-116">Requirement</span></span> | <span data-ttu-id="f9579-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9579-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f9579-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9579-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9579-119">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f9579-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f9579-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9579-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9579-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9579-121">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="f9579-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9579-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9579-123">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="f9579-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f9579-124">**contextType**</span><span class="sxs-lookup"><span data-stu-id="f9579-124">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="f9579-125">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="f9579-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f9579-126">**Contexte (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="f9579-126">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




