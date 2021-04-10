---
title: DisableUserPromptForServerValidation (ServerValidationParameters)
description: En savoir plus sur l’élément DisableUserPromptForServerValidation (ServerValidationParameters). Elle indique si la validation du serveur doit être demandée à l’utilisateur. | DisableUserPromptForServerValidation (ServerValidationParameters)
ms.assetid: d1c2f334-286b-4aac-b723-806b90fc7b1f
keywords:
- Élément DisableUserPromptForServerValidation EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 368b2593b3c55ef571e3f1892634318e54447643
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211456"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-tls"></a><span data-ttu-id="ee925-106">DisableUserPromptForServerValidation (ServerValidationParameters), élément (TLS)</span><span class="sxs-lookup"><span data-stu-id="ee925-106">DisableUserPromptForServerValidation (ServerValidationParameters) element (TLS)</span></span>

<span data-ttu-id="ee925-107">L’élément **DisableUserPromptForServerValidation (ServerValidationParameters)** indique si la validation du serveur doit être demandée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ee925-107">The **DisableUserPromptForServerValidation (ServerValidationParameters)** element indicates whether the user should be asked for server validation.</span></span>

<span data-ttu-id="ee925-108">Si **DisableUserPromptForServerValidation** a la valeur true, EAP-TLS effectue la validation du serveur sans entrée d’utilisateur ; Si la validation échoue, l’authentification EAP-TLS échoue.</span><span class="sxs-lookup"><span data-stu-id="ee925-108">If **DisableUserPromptForServerValidation** is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <span data-ttu-id="ee925-109">Si **DisableUserPromptForServerValidation** a la valeur false, l’utilisateur est invité à fournir un certificat ou un nom de serveur validé, ou une autorité de certification racine.</span><span class="sxs-lookup"><span data-stu-id="ee925-109">If **DisableUserPromptForServerValidation** is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span>

<span data-ttu-id="ee925-110">L’élément **DisableUserPromptForServerValidation** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="ee925-110">The **DisableUserPromptForServerValidation** element is optional.</span></span>

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

<span data-ttu-id="ee925-111">L’élément **DisableUserPromptForServerValidation** est défini par le type complexe [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ee925-111">The **DisableUserPromptForServerValidation** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee925-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee925-112">Requirements</span></span>



| <span data-ttu-id="ee925-113">Role</span><span class="sxs-lookup"><span data-stu-id="ee925-113">Role</span></span> | <span data-ttu-id="ee925-114">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="ee925-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="ee925-115">Client</span><span class="sxs-lookup"><span data-stu-id="ee925-115">Client</span></span><br/> | <span data-ttu-id="ee925-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee925-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee925-117">Serveur</span><span class="sxs-lookup"><span data-stu-id="ee925-117">Server</span></span><br/> | <span data-ttu-id="ee925-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee925-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee925-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee925-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee925-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="ee925-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ee925-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="ee925-121">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="ee925-122">**Éléments parents immédiats possibles dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="ee925-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ee925-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="ee925-123">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="ee925-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ee925-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="ee925-125">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="ee925-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ee925-126">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ee925-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ee925-127">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ee925-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





