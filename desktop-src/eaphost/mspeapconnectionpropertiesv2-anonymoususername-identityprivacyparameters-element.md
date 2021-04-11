---
title: Élément AnonymousUserName (IdentityPrivacyParameters)
description: Contient une identité anonyme utilisée à la place de la véritable identification d’un utilisateur. Il est envoyé au cours de la première phase de l’authentification PEAP lorsque l’identité est envoyée en texte brut.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- Élément AnonymousUserName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384944"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a><span data-ttu-id="571f3-105">Élément AnonymousUserName (IdentityPrivacyParameters)</span><span class="sxs-lookup"><span data-stu-id="571f3-105">AnonymousUserName (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="571f3-106">L’élément **AnonymousUserName (IdentityPrivacyParameters)** contient une identité anonyme utilisée à la place de la véritable identification d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="571f3-106">The **AnonymousUserName (IdentityPrivacyParameters)** element contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="571f3-107">Il est envoyé au cours de la première phase de l’authentification PEAP lorsque l' **identité** est envoyée en texte brut.</span><span class="sxs-lookup"><span data-stu-id="571f3-107">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span>

<span data-ttu-id="571f3-108">L’utilisation de l’identité anonyme est déterminée par l’élément [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="571f3-108">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

<span data-ttu-id="571f3-109">L’élément **AnonymousUserName** est défini par [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="571f3-109">The **AnonymousUserName** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="571f3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="571f3-110">Remarks</span></span>

<span data-ttu-id="571f3-111">L’élément **AnonymousUserName** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="571f3-111">The **AnonymousUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="571f3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="571f3-112">Requirements</span></span>



| <span data-ttu-id="571f3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="571f3-113">Requirement</span></span> | <span data-ttu-id="571f3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="571f3-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="571f3-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="571f3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="571f3-116">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="571f3-116">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="571f3-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="571f3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="571f3-118">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="571f3-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="571f3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="571f3-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="571f3-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="571f3-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="571f3-121">IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="571f3-121">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="571f3-122">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="571f3-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="571f3-123">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="571f3-123">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="571f3-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="571f3-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="571f3-125">Schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="571f3-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="571f3-126">Éléments de schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="571f3-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





