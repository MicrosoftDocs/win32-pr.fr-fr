---
title: Élément EapType (eaptlsuserpropertiesv1schema)
description: Cet élément est un type dérivé de l’élément EapType du schéma baseeapuserpropertiesv1. Pour eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
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
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106545719"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a><span data-ttu-id="3f62c-105">Élément EapType (eaptlsuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="3f62c-105">EapType element (eaptlsuserpropertiesv1schema)</span></span>

<span data-ttu-id="3f62c-106">L’élément **EapType** est un type dérivé de l’élément [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) du schéma [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="3f62c-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="3f62c-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3f62c-107">Child elements</span></span>



| <span data-ttu-id="3f62c-108">Élément</span><span class="sxs-lookup"><span data-stu-id="3f62c-108">Element</span></span>                                                                   | <span data-ttu-id="3f62c-109">Type</span><span class="sxs-lookup"><span data-stu-id="3f62c-109">Type</span></span>      | <span data-ttu-id="3f62c-110">Description</span><span class="sxs-lookup"><span data-stu-id="3f62c-110">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f62c-111">**Nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="3f62c-111">**Username**</span></span>](eaptlsuserpropertiesv1schema-username-element.md)         |           | <span data-ttu-id="3f62c-112">Capture le nom d’utilisateur à envoyer dans la réponse EAP-Identity.</span><span class="sxs-lookup"><span data-stu-id="3f62c-112">Captures the user name to be sent in the EAP-Identity response.</span></span> <span data-ttu-id="3f62c-113">Si l’élément [**username**](eaptlsuserpropertiesv1schema-username-element.md) est absent, EAP-TLS utilise le nom figurant dans le certificat auquel il est fait appel dans l’élément [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3f62c-113">If the [**Username**](eaptlsuserpropertiesv1schema-username-element.md) element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span><br/> |
| [<span data-ttu-id="3f62c-114">**UserCert**</span><span class="sxs-lookup"><span data-stu-id="3f62c-114">**UserCert**</span></span>](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | <span data-ttu-id="3f62c-115">hexBinary</span><span class="sxs-lookup"><span data-stu-id="3f62c-115">hexBinary</span></span> | <span data-ttu-id="3f62c-116">Fait référence au hachage SHA-1 du certificat qui doit être utilisé pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="3f62c-116">Refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span><br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a><span data-ttu-id="3f62c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3f62c-117">Remarks</span></span>

<span data-ttu-id="3f62c-118">L’élément **processContents** active les futures améliorations du schéma.</span><span class="sxs-lookup"><span data-stu-id="3f62c-118">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="3f62c-119">L’élément **processContents** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="3f62c-119">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f62c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f62c-120">Requirements</span></span>



| <span data-ttu-id="3f62c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f62c-121">Requirement</span></span> | <span data-ttu-id="3f62c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f62c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f62c-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f62c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3f62c-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f62c-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f62c-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f62c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3f62c-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f62c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f62c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f62c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f62c-128">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="3f62c-128">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3f62c-129">Schéma eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3f62c-129">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





