---
title: Type complexe ServerValidationParameters (PEAP)
description: En savoir plus sur le type complexe ServerValidationParameters. Ce type contient des informations sur la façon d’effectuer la validation du serveur. | Type complexe ServerValidationParameters (PEAP)
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
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
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953540"
---
# <a name="servervalidationparameters-complex-type-peap"></a><span data-ttu-id="2ba83-106">Type complexe ServerValidationParameters (PEAP)</span><span class="sxs-lookup"><span data-stu-id="2ba83-106">ServerValidationParameters complex type (PEAP)</span></span>

<span data-ttu-id="2ba83-107">Le type complexe **ServerValidationParameters** contient des informations sur la façon d’effectuer la validation du serveur.</span><span class="sxs-lookup"><span data-stu-id="2ba83-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2ba83-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2ba83-108">Child elements</span></span>



| <span data-ttu-id="2ba83-109">Élément</span><span class="sxs-lookup"><span data-stu-id="2ba83-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="2ba83-110">Type</span><span class="sxs-lookup"><span data-stu-id="2ba83-110">Type</span></span>        | <span data-ttu-id="2ba83-111">Description</span><span class="sxs-lookup"><span data-stu-id="2ba83-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ba83-112">**DisableUserPromptForServerValidation**</span><span class="sxs-lookup"><span data-stu-id="2ba83-112">**DisableUserPromptForServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="2ba83-113">boolean</span><span class="sxs-lookup"><span data-stu-id="2ba83-113">boolean</span></span>     | <span data-ttu-id="2ba83-114">Indique si la validation du serveur doit être demandée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ba83-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="2ba83-115">Si [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) a la valeur true, PEAP effectue la validation du serveur sans entrée d’utilisateur ; en cas d’échec de la validation, l’authentification PEAP échoue.</span><span class="sxs-lookup"><span data-stu-id="2ba83-115">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then PEAP performs the server validation without user input; if the validation fails, PEAP fails the authentication.</span></span><br/> <span data-ttu-id="2ba83-116">Si [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) a la valeur false, l’utilisateur est invité à fournir un certificat ou un nom de serveur validé, ou une autorité de certification racine (ca).</span><span class="sxs-lookup"><span data-stu-id="2ba83-116">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certification authority (CA).</span></span><br/> <span data-ttu-id="2ba83-117">L’élément [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="2ba83-117">The [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="2ba83-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="2ba83-118">**ServerNames**</span></span>](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="2ba83-119">complexType</span><span class="sxs-lookup"><span data-stu-id="2ba83-119">complextype</span></span> | <span data-ttu-id="2ba83-120">Représente une liste de serveurs approuvés par le client.</span><span class="sxs-lookup"><span data-stu-id="2ba83-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="2ba83-121">Chaque nom de serveur est délimité par des points-virgules et peut être représenté par des expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="2ba83-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <br/> <span data-ttu-id="2ba83-122">L’élément [**serverNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="2ba83-122">The [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="2ba83-123">**TrustedRootCA**</span><span class="sxs-lookup"><span data-stu-id="2ba83-123">**TrustedRootCA**</span></span>](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="2ba83-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="2ba83-124">hexBinary</span></span>   | <span data-ttu-id="2ba83-125">Capture l’impression Thumb des autorités de certification racines approuvées par le client.</span><span class="sxs-lookup"><span data-stu-id="2ba83-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="2ba83-126">L’impression Thumb est une chaîne hexadécimale qui contient le hachage SHA-1 du certificat.</span><span class="sxs-lookup"><span data-stu-id="2ba83-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="2ba83-127">L’élément [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="2ba83-127">The [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a><span data-ttu-id="2ba83-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="2ba83-128">Attributes</span></span>



| <span data-ttu-id="2ba83-129">Nom</span><span class="sxs-lookup"><span data-stu-id="2ba83-129">Name</span></span>                    | <span data-ttu-id="2ba83-130">Type</span><span class="sxs-lookup"><span data-stu-id="2ba83-130">Type</span></span>    | <span data-ttu-id="2ba83-131">Description</span><span class="sxs-lookup"><span data-stu-id="2ba83-131">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba83-132">PerformServerValidation</span><span class="sxs-lookup"><span data-stu-id="2ba83-132">PerformServerValidation</span></span> | <span data-ttu-id="2ba83-133">boolean</span><span class="sxs-lookup"><span data-stu-id="2ba83-133">boolean</span></span> | <span data-ttu-id="2ba83-134">Windows 7 ou version ultérieure : indique si la validation du serveur est effectuée.</span><span class="sxs-lookup"><span data-stu-id="2ba83-134">Windows 7 or later: Indicates whether server validation is performed.</span></span> <span data-ttu-id="2ba83-135">L’élément [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="2ba83-135">The [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2ba83-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ba83-136">Requirements</span></span>



| <span data-ttu-id="2ba83-137">Role</span><span class="sxs-lookup"><span data-stu-id="2ba83-137">Role</span></span> | <span data-ttu-id="2ba83-138">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="2ba83-138">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="2ba83-139">Client</span><span class="sxs-lookup"><span data-stu-id="2ba83-139">Client</span></span><br/> | <span data-ttu-id="2ba83-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ba83-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2ba83-141">Serveur</span><span class="sxs-lookup"><span data-stu-id="2ba83-141">Server</span></span><br/> | <span data-ttu-id="2ba83-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ba83-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ba83-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ba83-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba83-144">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="2ba83-144">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2ba83-145">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2ba83-145">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="2ba83-146">Types complexes de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2ba83-146">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="2ba83-147">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="2ba83-147">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





