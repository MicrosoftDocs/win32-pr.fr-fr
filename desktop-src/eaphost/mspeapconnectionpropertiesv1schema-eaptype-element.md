---
title: Élément EapType (mspeapconnectionpropertiesv1schema)
description: Cet élément est un type dérivé de l’élément EapType du schéma BaseEapConnectionProperties. Pour mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
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
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106533526"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a><span data-ttu-id="1087c-105">Élément EapType (mspeapconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="1087c-105">EapType element (mspeapconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="1087c-106">L’élément **EapType** est un type dérivé de l’élément [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) du schéma [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="1087c-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="1087c-107">Cet élément **EapType** dérivé contient les éléments suivants : [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) et [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span><span class="sxs-lookup"><span data-stu-id="1087c-107">This derived **EapType** element contains the following elements: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) and [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span></span>

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
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="1087c-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1087c-108">Child elements</span></span>



| <span data-ttu-id="1087c-109">Élément</span><span class="sxs-lookup"><span data-stu-id="1087c-109">Element</span></span>                                                                                                     | <span data-ttu-id="1087c-110">Type</span><span class="sxs-lookup"><span data-stu-id="1087c-110">Type</span></span>                                                                                                            | <span data-ttu-id="1087c-111">Description</span><span class="sxs-lookup"><span data-stu-id="1087c-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1087c-112">**EAP**</span><span class="sxs-lookup"><span data-stu-id="1087c-112">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | <span data-ttu-id="1087c-113">Décrit la méthode interne et la configuration de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1087c-113">Describes the inner method and the method configuration.</span></span> <span data-ttu-id="1087c-114">Si l’élément [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) a la valeur true, l’élément [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) doit être présent.</span><span class="sxs-lookup"><span data-stu-id="1087c-114">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present.</span></span> <span data-ttu-id="1087c-115">Si l’élément [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) a la valeur false, l’élément [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) doit être absent.</span><span class="sxs-lookup"><span data-stu-id="1087c-115">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is FALSE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be absent.</span></span><br/>           |
| [<span data-ttu-id="1087c-116">**EnableQuarantineChecks**</span><span class="sxs-lookup"><span data-stu-id="1087c-116">**EnableQuarantineChecks**</span></span>](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | <span data-ttu-id="1087c-117">boolean</span><span class="sxs-lookup"><span data-stu-id="1087c-117">boolean</span></span>                                                                                                         | <span data-ttu-id="1087c-118">Indique s’il faut effectuer des vérifications de la protection d’accès réseau (NAP).</span><span class="sxs-lookup"><span data-stu-id="1087c-118">Indicates whether to perform Network Access Protection (NAP) checks.</span></span> <span data-ttu-id="1087c-119">Si l’élément [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) a la valeur true, PEAP effectue des vérifications NAP. Si la valeur FALSe, PEAP n’effectue pas de vérifications NAP.</span><span class="sxs-lookup"><span data-stu-id="1087c-119">If the [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is TRUE, then PEAP will perform NAP checks; if FALSE PEAP will not perform NAP checks.</span></span> <span data-ttu-id="1087c-120">L’élément [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1087c-120">The [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is optional.</span></span><br/>                                                                                |
| [<span data-ttu-id="1087c-121">**FastReconnect**</span><span class="sxs-lookup"><span data-stu-id="1087c-121">**FastReconnect**</span></span>](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | <span data-ttu-id="1087c-122">boolean</span><span class="sxs-lookup"><span data-stu-id="1087c-122">boolean</span></span>                                                                                                         | <span data-ttu-id="1087c-123">Indique s’il faut effectuer une reconnexion rapide.</span><span class="sxs-lookup"><span data-stu-id="1087c-123">Indicates whether to perform a fast reconnect.</span></span> <span data-ttu-id="1087c-124">Si l’élément [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) a la valeur true, PEAP tente d’effectuer une reconnexion rapide ; Si la valeur est FALSe, PEAP effectue l’authentification complète.</span><span class="sxs-lookup"><span data-stu-id="1087c-124">If the [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="1087c-125">L’élément [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1087c-125">The [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="1087c-126">**IdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="1087c-126">**IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [<span data-ttu-id="1087c-127">**IdentityPrivacyParameters**</span><span class="sxs-lookup"><span data-stu-id="1087c-127">**IdentityPrivacyParameters**</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | <span data-ttu-id="1087c-128">Windows 7 ou version ultérieure : indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.</span><span class="sxs-lookup"><span data-stu-id="1087c-128">Windows 7 or later: Indicates whether a user's true identity or an anonymous identity is sent.</span></span> <span data-ttu-id="1087c-129">L’élément [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1087c-129">The [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="1087c-130">**InnerEapOptional**</span><span class="sxs-lookup"><span data-stu-id="1087c-130">**InnerEapOptional**</span></span>](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | <span data-ttu-id="1087c-131">boolean</span><span class="sxs-lookup"><span data-stu-id="1087c-131">boolean</span></span>                                                                                                         | <span data-ttu-id="1087c-132">Indique s’il faut effectuer l’accès invité.</span><span class="sxs-lookup"><span data-stu-id="1087c-132">Indicates whether to perform GUEST access.</span></span> <span data-ttu-id="1087c-133">Si l’élément [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) a la valeur true, l’élément [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) doit être présent et décrire la méthode interne et sa configuration. Si la valeur est FALSe, PEAP effectue un accès invité.</span><span class="sxs-lookup"><span data-stu-id="1087c-133">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and its configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="1087c-134">L’élément [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1087c-134">The [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is optional.</span></span><br/>            |
| [<span data-ttu-id="1087c-135">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="1087c-135">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [<span data-ttu-id="1087c-136">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="1087c-136">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | <span data-ttu-id="1087c-137">L’élément [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) active les améliorations futures du schéma.</span><span class="sxs-lookup"><span data-stu-id="1087c-137">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <span data-ttu-id="1087c-138">L’élément [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1087c-138">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="1087c-139">**RequireCryptoBinding**</span><span class="sxs-lookup"><span data-stu-id="1087c-139">**RequireCryptoBinding**</span></span>](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | <span data-ttu-id="1087c-140">boolean</span><span class="sxs-lookup"><span data-stu-id="1087c-140">boolean</span></span>                                                                                                         | <span data-ttu-id="1087c-141">Indique s’il faut s’authentifier auprès des serveurs qui prennent en charge TLV.</span><span class="sxs-lookup"><span data-stu-id="1087c-141">Indicates whether to authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="1087c-142">Si l’élément [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) a la valeur true, PEAP s’authentifie auprès des serveurs qui ne prennent pas en charge TLV ; Si la valeur est FALSe, PEAP s’authentifie uniquement avec les serveurs qui prennent en charge TLV.</span><span class="sxs-lookup"><span data-stu-id="1087c-142">If the [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="1087c-143">L’élément [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1087c-143">The [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="1087c-144">**ServerValidation**</span><span class="sxs-lookup"><span data-stu-id="1087c-144">**ServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [<span data-ttu-id="1087c-145">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="1087c-145">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | <span data-ttu-id="1087c-146">Contient des informations sur la façon d’effectuer la validation du serveur.</span><span class="sxs-lookup"><span data-stu-id="1087c-146">Contains information about how to perform server validation.</span></span> <span data-ttu-id="1087c-147">L’élément [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1087c-147">The [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="1087c-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1087c-148">Requirements</span></span>



| <span data-ttu-id="1087c-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1087c-149">Requirement</span></span> | <span data-ttu-id="1087c-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="1087c-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1087c-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1087c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="1087c-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1087c-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1087c-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1087c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="1087c-154">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1087c-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1087c-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1087c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1087c-156">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="1087c-156">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1087c-157">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1087c-157">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="1087c-158">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1087c-158">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





