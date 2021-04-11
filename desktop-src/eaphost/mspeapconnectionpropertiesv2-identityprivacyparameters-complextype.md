---
title: Type complexe IdentityPrivacyParameters
description: Contient des informations sur l’utilisation de l’identité anonyme pendant l’authentification PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101137"
---
# <a name="identityprivacyparameters-complex-type"></a><span data-ttu-id="11c7c-103">Type complexe IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="11c7c-103">IdentityPrivacyParameters Complex Type</span></span>

<span data-ttu-id="11c7c-104">Le type complexe **IdentityPrivacyParameters** contient des informations sur l’utilisation de l’identité anonyme pendant l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="11c7c-104">The **IdentityPrivacyParameters** complex type contains information about anonymous identity usage during PEAP authentication.</span></span>


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| <span data-ttu-id="11c7c-105">Élément</span><span class="sxs-lookup"><span data-stu-id="11c7c-105">Element</span></span>                                                                                                               | <span data-ttu-id="11c7c-106">Type</span><span class="sxs-lookup"><span data-stu-id="11c7c-106">Type</span></span>    | <span data-ttu-id="11c7c-107">Description</span><span class="sxs-lookup"><span data-stu-id="11c7c-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11c7c-108">**EnableIdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="11c7c-108">**EnableIdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | <span data-ttu-id="11c7c-109">boolean</span><span class="sxs-lookup"><span data-stu-id="11c7c-109">boolean</span></span> | <span data-ttu-id="11c7c-110">Indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.</span><span class="sxs-lookup"><span data-stu-id="11c7c-110">Indicates whether a user's true identity or an anonymous identity is sent.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="11c7c-111">**AnonymousUserName**</span><span class="sxs-lookup"><span data-stu-id="11c7c-111">**AnonymousUserName**</span></span>](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | <span data-ttu-id="11c7c-112">string</span><span class="sxs-lookup"><span data-stu-id="11c7c-112">string</span></span>  | <span data-ttu-id="11c7c-113">contient une identité anonyme utilisée à la place de la véritable identification d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="11c7c-113">contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="11c7c-114">Il est envoyé au cours de la première phase de l’authentification PEAP lorsque l' **identité** est envoyée en texte brut.</span><span class="sxs-lookup"><span data-stu-id="11c7c-114">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span> <span data-ttu-id="11c7c-115">L’utilisation de l’identité anonyme est déterminée par l’élément [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="11c7c-115">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="11c7c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="11c7c-116">Remarks</span></span>

<span data-ttu-id="11c7c-117">L’élément IdentityPrivacyParameters est facultatif.</span><span class="sxs-lookup"><span data-stu-id="11c7c-117">The IdentityPrivacyParameters element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11c7c-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11c7c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11c7c-119">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="11c7c-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="11c7c-120">Schéma mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="11c7c-120">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="11c7c-121">Types complexes mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="11c7c-121">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




