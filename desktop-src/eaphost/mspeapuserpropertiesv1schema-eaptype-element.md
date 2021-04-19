---
title: Élément EapType (mspeapuserpropertiesv1schema)
description: Cet élément est un type dérivé de l’élément EapType du schéma baseeapuserpropertiesv1. Pour mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
keywords:
- Élément EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ccedc72baf3a677acc3a318895defbc97bb26287
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106534955"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a><span data-ttu-id="5c57b-105">Élément EapType (mspeapuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="5c57b-105">EapType Element (mspeapuserpropertiesv1schema)</span></span>

<span data-ttu-id="5c57b-106">L’élément **EapType** est un type dérivé de l’élément [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) du schéma [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="5c57b-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType
        "
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="5c57b-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5c57b-107">Child elements</span></span>



| <span data-ttu-id="5c57b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="5c57b-108">Element</span></span>                                                                               | <span data-ttu-id="5c57b-109">Type</span><span class="sxs-lookup"><span data-stu-id="5c57b-109">Type</span></span>                                                                                      | <span data-ttu-id="5c57b-110">Description</span><span class="sxs-lookup"><span data-stu-id="5c57b-110">Description</span></span>                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c57b-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="5c57b-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | <span data-ttu-id="5c57b-112">L’élément [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) identifie la méthode interne et les informations d’identification à utiliser avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5c57b-112">The [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) element identifies the inner method and the credentials to be used with that method.</span></span> <span data-ttu-id="5c57b-113">Lorsque la configuration PEAP est configurée pour l’accès invité PEAP, cet élément est absent.</span><span class="sxs-lookup"><span data-stu-id="5c57b-113">When PEAP configuration is configured for PEAP guest access, this element is absent.</span></span><br/>                                  |
| [<span data-ttu-id="5c57b-114">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="5c57b-114">**PeapExtensions**</span></span>](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [<span data-ttu-id="5c57b-115">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="5c57b-115">**PeapExtensionsType**</span></span>](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | <span data-ttu-id="5c57b-116">L’élément [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) active les améliorations futures du schéma.</span><span class="sxs-lookup"><span data-stu-id="5c57b-116">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <br/> <span data-ttu-id="5c57b-117">L’élément [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5c57b-117">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5c57b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c57b-118">Requirements</span></span>



| <span data-ttu-id="5c57b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c57b-119">Requirement</span></span> | <span data-ttu-id="5c57b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c57b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c57b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c57b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c57b-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c57b-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c57b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c57b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c57b-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c57b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c57b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c57b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c57b-126">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="5c57b-126">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5c57b-127">Schéma mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5c57b-127">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





