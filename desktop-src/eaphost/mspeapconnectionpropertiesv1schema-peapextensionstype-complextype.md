---
title: Type complexe PeapExtensionsType
description: Contient des améliorations de schéma apportées à Windows 7. Les futures améliorations du schéma seront gérées par PeapExtensionsTypeV2.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- PeapExtensionsType type complexe EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742844"
---
# <a name="peapextensionstype-complex-type"></a><span data-ttu-id="a634a-105">Type complexe PeapExtensionsType</span><span class="sxs-lookup"><span data-stu-id="a634a-105">PeapExtensionsType Complex Type</span></span>

<span data-ttu-id="a634a-106">Le type complexe **PeapExtensionsType** contient des améliorations de schéma effectuées dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a634a-106">The **PeapExtensionsType** complex type contains schema enhancements made in Windows 7.</span></span> <span data-ttu-id="a634a-107">Les futures améliorations du schéma seront gérées par [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="a634a-107">Future schema enhancements will be handled by [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a634a-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a634a-108">Child elements</span></span>



| <span data-ttu-id="a634a-109">Élément</span><span class="sxs-lookup"><span data-stu-id="a634a-109">Element</span></span>                                                                                                                               | <span data-ttu-id="a634a-110">Type</span><span class="sxs-lookup"><span data-stu-id="a634a-110">Type</span></span> | <span data-ttu-id="a634a-111">Description</span><span class="sxs-lookup"><span data-stu-id="a634a-111">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a634a-112">**extendedPeap:PerformServerValidation**</span><span class="sxs-lookup"><span data-stu-id="a634a-112">**extendedPeap:PerformServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | <span data-ttu-id="a634a-113">Windows 7 et versions ultérieures : indique si la validation du serveur est effectuée.</span><span class="sxs-lookup"><span data-stu-id="a634a-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                          |
| [<span data-ttu-id="a634a-114">**extendedPeap:AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="a634a-114">**extendedPeap:AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | <span data-ttu-id="a634a-115">Windows 7 et versions ultérieures : indique si le nom d’un serveur est lu.</span><span class="sxs-lookup"><span data-stu-id="a634a-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                            |
| [<span data-ttu-id="a634a-116">**extendedPeap:IdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="a634a-116">**extendedPeap:IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | <span data-ttu-id="a634a-117">Windows 7 et versions ultérieures : indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.</span><span class="sxs-lookup"><span data-stu-id="a634a-117">Windows 7 and later: indicates whether a user's true identity or an anonymous identity is sent.</span></span><br/> |
| [<span data-ttu-id="a634a-118">**extendedPeap:PeapExtensionsV2**</span><span class="sxs-lookup"><span data-stu-id="a634a-118">**extendedPeap:PeapExtensionsV2**</span></span>](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | <span data-ttu-id="a634a-119">Windows 7 et versions ultérieures : active les améliorations futures du schéma.</span><span class="sxs-lookup"><span data-stu-id="a634a-119">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                 |



## <a name="remarks"></a><span data-ttu-id="a634a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a634a-120">Remarks</span></span>

<span data-ttu-id="a634a-121">L’élément **PeapExtensionsType** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a634a-121">The **PeapExtensionsType** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="a634a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a634a-122">Requirements</span></span>



| <span data-ttu-id="a634a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a634a-123">Requirement</span></span> | <span data-ttu-id="a634a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a634a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a634a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a634a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a634a-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a634a-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a634a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a634a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a634a-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a634a-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a634a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a634a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a634a-130">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="a634a-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a634a-131">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a634a-131">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="a634a-132">Types complexes de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a634a-132">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





