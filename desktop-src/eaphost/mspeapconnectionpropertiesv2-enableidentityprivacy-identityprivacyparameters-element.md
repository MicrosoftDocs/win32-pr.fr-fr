---
title: Élément EnableIdentityPrivacy (IdentityPrivacyParameters)
description: Indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée. | Élément EnableIdentityPrivacy (IdentityPrivacyParameters)
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- Élément EnableIdentityPrivacy EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322485"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a><span data-ttu-id="076e0-105">Élément EnableIdentityPrivacy (IdentityPrivacyParameters)</span><span class="sxs-lookup"><span data-stu-id="076e0-105">EnableIdentityPrivacy (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="076e0-106">L’élément **EnableIdentityPrivacy (IdentityPrivacyParameters)** indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.</span><span class="sxs-lookup"><span data-stu-id="076e0-106">The **EnableIdentityPrivacy (IdentityPrivacyParameters)** element Indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="076e0-107">L’élément **EnableIdentityPrivacy** est défini par [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="076e0-107">The **EnableIdentityPrivacy** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="076e0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="076e0-108">Remarks</span></span>

<span data-ttu-id="076e0-109">L’élément **EnableIdentityPrivacy** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="076e0-109">The **EnableIdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="076e0-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="076e0-110">Requirements</span></span>



| <span data-ttu-id="076e0-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="076e0-111">Requirement</span></span> | <span data-ttu-id="076e0-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="076e0-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="076e0-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="076e0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="076e0-114">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="076e0-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="076e0-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="076e0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="076e0-116">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="076e0-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="076e0-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="076e0-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="076e0-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="076e0-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="076e0-119">IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="076e0-119">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="076e0-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="076e0-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="076e0-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="076e0-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="076e0-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="076e0-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="076e0-123">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="076e0-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="076e0-124">Schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="076e0-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="076e0-125">Éléments de schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="076e0-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





