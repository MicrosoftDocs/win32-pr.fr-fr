---
title: Élément EapType (eaptlsconnectionpropertiesv1schema)
description: Cet élément est un type dérivé de l’élément EapType du schéma BaseEapConnectionProperties. Pour eaptlsconnectionpropertiesv1schema.
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
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
ms.openlocfilehash: b74341d9b1fdd9121f1d67e2a941d931be049e0f
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106539317"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a><span data-ttu-id="59611-105">Élément EapType (eaptlsconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="59611-105">EapType element (eaptlsconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="59611-106">L’élément **EapType** est un type dérivé de l’élément [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) du schéma [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="59611-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="59611-107">Cet élément **EapType** dérivé contient les éléments suivants : [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)et [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span><span class="sxs-lookup"><span data-stu-id="59611-107">This derived **EapType** element contains the following elements: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md), and [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span></span>

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
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="59611-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="59611-108">Child elements</span></span>



| <span data-ttu-id="59611-109">Élément</span><span class="sxs-lookup"><span data-stu-id="59611-109">Element</span></span>                                                                                                                               | <span data-ttu-id="59611-110">Type</span><span class="sxs-lookup"><span data-stu-id="59611-110">Type</span></span>                                                                                                              | <span data-ttu-id="59611-111">Description</span><span class="sxs-lookup"><span data-stu-id="59611-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59611-112">**extendedTLS: PerformServerValidation**</span><span class="sxs-lookup"><span data-stu-id="59611-112">**extendedTLS: PerformServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | <span data-ttu-id="59611-113">Windows 7 et versions ultérieures : indique si la validation du serveur est effectuée.</span><span class="sxs-lookup"><span data-stu-id="59611-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="59611-114">**extendedTLS: AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="59611-114">**extendedTLS: AcceptServerName**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | <span data-ttu-id="59611-115">Windows 7 et versions ultérieures : indique si le nom d’un serveur est lu.</span><span class="sxs-lookup"><span data-stu-id="59611-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="59611-116">**extendedTLS: TLSExtensions**</span><span class="sxs-lookup"><span data-stu-id="59611-116">**extendedTLS: TLSExtensions**</span></span>](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | <span data-ttu-id="59611-117">Windows 7 et versions ultérieures : active les améliorations futures du schéma.</span><span class="sxs-lookup"><span data-stu-id="59611-117">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="59611-118">**CredentialsSource**</span><span class="sxs-lookup"><span data-stu-id="59611-118">**CredentialsSource**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [<span data-ttu-id="59611-119">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="59611-119">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | <span data-ttu-id="59611-120">Contient des informations sur l’emplacement du certificat EAP-TLS (EAP Transport Level Security).</span><span class="sxs-lookup"><span data-stu-id="59611-120">Contains information about the location of the EAP Transport Level Security (EAP-TLS) certificate.</span></span> <br/> <span data-ttu-id="59611-121">L’élément [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="59611-121">The [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="59611-122">**DifferentUsername**</span><span class="sxs-lookup"><span data-stu-id="59611-122">**DifferentUsername**</span></span>](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | <span data-ttu-id="59611-123">boolean</span><span class="sxs-lookup"><span data-stu-id="59611-123">boolean</span></span>                                                                                                           | <span data-ttu-id="59611-124">Détermine le nom d’utilisateur que doit utiliser EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="59611-124">Determines which user name EAP-TLS is to use.</span></span> <br/> <span data-ttu-id="59611-125">Si l’élément [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) a la **valeur true**, EAP-TLS doit utiliser un nom d’utilisateur différent du nom qui s’affiche sur le certificat.</span><span class="sxs-lookup"><span data-stu-id="59611-125">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **TRUE**, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="59611-126">Si l’élément [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) a la **valeur false**, EAP-TLS utilise le nom d’utilisateur qui apparaît sur le certificat.</span><span class="sxs-lookup"><span data-stu-id="59611-126">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **FALSE**, EAP-TLS uses the user name that appears on the certificate.</span></span><br/> <span data-ttu-id="59611-127">L’élément [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="59611-127">The [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is optional.</span></span> <br/> |
| [<span data-ttu-id="59611-128">**ServerValidation**</span><span class="sxs-lookup"><span data-stu-id="59611-128">**ServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [<span data-ttu-id="59611-129">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="59611-129">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | <span data-ttu-id="59611-130">Contient des informations sur la façon d’effectuer la validation du serveur.</span><span class="sxs-lookup"><span data-stu-id="59611-130">Contains information about how to perform server validation.</span></span> <span data-ttu-id="59611-131">L’élément [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="59611-131">The [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="59611-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59611-132">Requirements</span></span>



| <span data-ttu-id="59611-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59611-133">Requirement</span></span> | <span data-ttu-id="59611-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="59611-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59611-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59611-135">Minimum supported client</span></span><br/> | <span data-ttu-id="59611-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59611-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59611-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59611-137">Minimum supported server</span></span><br/> | <span data-ttu-id="59611-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59611-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59611-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59611-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59611-140">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="59611-140">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="59611-141">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="59611-141">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="59611-142">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="59611-142">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





