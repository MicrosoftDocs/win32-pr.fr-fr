---
title: Type complexe ServerValidationParameters (TLS)
description: En savoir plus sur le type complexe ServerValidationParameters. Ce type contient des informations sur la façon d’effectuer la validation du serveur. | Type complexe ServerValidationParameters (TLS)
ms.assetid: 7a35c7f5-4cab-43d5-87dc-a4020811d3a9
keywords:
- ServerValidationParameters type complexe EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edebffd1f2023dd6f460505dc033e4505df338d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106543556"
---
# <a name="servervalidationparameters-complex-type-tls"></a><span data-ttu-id="a4acf-106">Type complexe ServerValidationParameters (TLS)</span><span class="sxs-lookup"><span data-stu-id="a4acf-106">ServerValidationParameters Complex Type (TLS)</span></span>

<span data-ttu-id="a4acf-107">Le type complexe **ServerValidationParameters** contient des informations sur la façon d’effectuer la validation du serveur.</span><span class="sxs-lookup"><span data-stu-id="a4acf-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="string"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a4acf-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a4acf-108">Child elements</span></span>



| <span data-ttu-id="a4acf-109">Élément</span><span class="sxs-lookup"><span data-stu-id="a4acf-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="a4acf-110">Type</span><span class="sxs-lookup"><span data-stu-id="a4acf-110">Type</span></span>      | <span data-ttu-id="a4acf-111">Description</span><span class="sxs-lookup"><span data-stu-id="a4acf-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4acf-112">**DisableUserPromptForServerValidation**</span><span class="sxs-lookup"><span data-stu-id="a4acf-112">**DisableUserPromptForServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="a4acf-113">boolean</span><span class="sxs-lookup"><span data-stu-id="a4acf-113">boolean</span></span>   | <span data-ttu-id="a4acf-114">Indique si la validation du serveur doit être demandée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a4acf-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="a4acf-115">Si [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) a la valeur true, EAP-TLS effectue la validation du serveur sans entrée d’utilisateur ; Si la validation échoue, l’authentification EAP-TLS échoue.</span><span class="sxs-lookup"><span data-stu-id="a4acf-115">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <br/> <span data-ttu-id="a4acf-116">Si [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) a la valeur false, l’utilisateur est invité à fournir un certificat ou un nom de serveur validé, ou une autorité de certification racine.</span><span class="sxs-lookup"><span data-stu-id="a4acf-116">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span><br/> <span data-ttu-id="a4acf-117">L’élément [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a4acf-117">The [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="a4acf-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="a4acf-118">**ServerNames**</span></span>](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="a4acf-119">string</span><span class="sxs-lookup"><span data-stu-id="a4acf-119">string</span></span>    | <span data-ttu-id="a4acf-120">Représente une liste de serveurs approuvés par le client.</span><span class="sxs-lookup"><span data-stu-id="a4acf-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="a4acf-121">Chaque nom de serveur est délimité par des points-virgules et peut être représenté par des expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="a4acf-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span><br/> <span data-ttu-id="a4acf-122">L’élément [**serverNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a4acf-122">The [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="a4acf-123">**TrustedRootCA**</span><span class="sxs-lookup"><span data-stu-id="a4acf-123">**TrustedRootCA**</span></span>](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="a4acf-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="a4acf-124">hexBinary</span></span> | <span data-ttu-id="a4acf-125">Capture l’impression Thumb des autorités de certification racines approuvées par le client.</span><span class="sxs-lookup"><span data-stu-id="a4acf-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="a4acf-126">L’impression Thumb est une chaîne hexadécimale qui contient le hachage SHA-1 du certificat.</span><span class="sxs-lookup"><span data-stu-id="a4acf-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="a4acf-127">L’élément [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a4acf-127">The [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="a4acf-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4acf-128">Requirements</span></span>



| <span data-ttu-id="a4acf-129">Role</span><span class="sxs-lookup"><span data-stu-id="a4acf-129">Role</span></span> | <span data-ttu-id="a4acf-130">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="a4acf-130">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="a4acf-131">Client</span><span class="sxs-lookup"><span data-stu-id="a4acf-131">Client</span></span><br/> | <span data-ttu-id="a4acf-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4acf-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4acf-133">Serveur</span><span class="sxs-lookup"><span data-stu-id="a4acf-133">Server</span></span><br/> | <span data-ttu-id="a4acf-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4acf-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4acf-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4acf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4acf-136">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="a4acf-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a4acf-137">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a4acf-137">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="a4acf-138">Types complexes de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a4acf-138">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





