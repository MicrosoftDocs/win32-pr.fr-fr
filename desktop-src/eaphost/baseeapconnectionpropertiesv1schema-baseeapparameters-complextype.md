---
title: Type complexe BaseEapParameters-propriétés de connexion
description: Définit l’élément d’espace réservé pour le type de méthode et la configuration spécifique à la méthode.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- BaseEapParameters type complexe EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106538563"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a><span data-ttu-id="07716-104">Type complexe BaseEapParameters-propriétés de connexion</span><span class="sxs-lookup"><span data-stu-id="07716-104">BaseEapParameters Complex Type - Connection properties</span></span>

<span data-ttu-id="07716-105">Le type complexe **BaseEapParameters** définit l’élément d’espace réservé pour le type de méthode et la configuration spécifique à la méthode.</span><span class="sxs-lookup"><span data-stu-id="07716-105">The **BaseEapParameters** complex type defines the placeholder element for method type and method-specific configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="07716-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="07716-106">Child elements</span></span>



| <span data-ttu-id="07716-107">Élément</span><span class="sxs-lookup"><span data-stu-id="07716-107">Element</span></span>                                                                            | <span data-ttu-id="07716-108">Type</span><span class="sxs-lookup"><span data-stu-id="07716-108">Type</span></span>    | <span data-ttu-id="07716-109">Description</span><span class="sxs-lookup"><span data-stu-id="07716-109">Description</span></span>                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [<span data-ttu-id="07716-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="07716-110">**Type**</span></span>](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="07716-111">entier</span><span class="sxs-lookup"><span data-stu-id="07716-111">integer</span></span> | <span data-ttu-id="07716-112">Une instance de schéma est autorisée ici.</span><span class="sxs-lookup"><span data-stu-id="07716-112">Any schema instance is allowed here.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="07716-113">Notes</span><span class="sxs-lookup"><span data-stu-id="07716-113">Remarks</span></span>

<span data-ttu-id="07716-114">Dans **BaseEapParameters** , la méthode peut définir les éléments constitutifs.</span><span class="sxs-lookup"><span data-stu-id="07716-114">In **BaseEapParameters** the method can define the constituent elements.</span></span> <span data-ttu-id="07716-115">La méthode effectue également une validation de schéma sur les éléments dans **BaseEapParameters**.</span><span class="sxs-lookup"><span data-stu-id="07716-115">The method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07716-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07716-116">Requirements</span></span>



| <span data-ttu-id="07716-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07716-117">Requirement</span></span> | <span data-ttu-id="07716-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="07716-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07716-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07716-119">Minimum supported client</span></span><br/> | <span data-ttu-id="07716-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07716-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07716-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07716-121">Minimum supported server</span></span><br/> | <span data-ttu-id="07716-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07716-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07716-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07716-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07716-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="07716-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="07716-125">Schéma baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="07716-125">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





