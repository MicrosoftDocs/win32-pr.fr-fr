---
title: Type complexe BaseEapParameters-propriétés de l’utilisateur
description: Définit l’élément qui a spécifié la méthode héritée sélectionnée et les informations d’identification spécifiques à la méthode.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106527967"
---
# <a name="baseeapparameters-complex-type---user-properties"></a><span data-ttu-id="63936-104">Type complexe BaseEapParameters-propriétés de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="63936-104">BaseEapParameters Complex Type - User properties</span></span>

<span data-ttu-id="63936-105">Le type complexe **BaseEapParameters** définit l’élément qui a spécifié la méthode héritée sélectionnée et les informations d’identification spécifiques à la méthode.</span><span class="sxs-lookup"><span data-stu-id="63936-105">The **BaseEapParameters** complex type defines the element that specified the legacy method selected and method-specific credentials.</span></span>

<span data-ttu-id="63936-106">La méthode peut définir les éléments constitutifs à l’intérieur de **BaseEapParameters**; la méthode effectue également une validation de schéma sur les éléments dans **BaseEapParameters**.</span><span class="sxs-lookup"><span data-stu-id="63936-106">The method can define the constituent elements inside **BaseEapParameters**; the method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="63936-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="63936-107">Child elements</span></span>



| <span data-ttu-id="63936-108">Élément</span><span class="sxs-lookup"><span data-stu-id="63936-108">Element</span></span>                                                                      | <span data-ttu-id="63936-109">Type</span><span class="sxs-lookup"><span data-stu-id="63936-109">Type</span></span>    | <span data-ttu-id="63936-110">Description</span><span class="sxs-lookup"><span data-stu-id="63936-110">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63936-111">**Type**</span><span class="sxs-lookup"><span data-stu-id="63936-111">**Type**</span></span>](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="63936-112">entier</span><span class="sxs-lookup"><span data-stu-id="63936-112">integer</span></span> | <span data-ttu-id="63936-113">Définit l’élément d’espace réservé pour le type de méthode sélectionné et les informations d’identification spécifiques à la méthode.</span><span class="sxs-lookup"><span data-stu-id="63936-113">Defines the placeholder element for the method type selected and method specific credentials.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="63936-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63936-114">Requirements</span></span>



| <span data-ttu-id="63936-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63936-115">Requirement</span></span> | <span data-ttu-id="63936-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="63936-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63936-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63936-117">Minimum supported client</span></span><br/> | <span data-ttu-id="63936-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63936-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63936-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63936-119">Minimum supported server</span></span><br/> | <span data-ttu-id="63936-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63936-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63936-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63936-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63936-122">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="63936-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="63936-123">Schéma baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="63936-123">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





