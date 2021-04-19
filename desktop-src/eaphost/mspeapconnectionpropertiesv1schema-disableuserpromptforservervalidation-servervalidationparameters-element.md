---
title: Élément DisableUserPromptForServerValidation (PEAP)
description: En savoir plus sur l’élément DisableUserPromptForServerValidation (ServerValidationParameters). Elle indique si la validation du serveur doit être demandée à l’utilisateur. | Élément DisableUserPromptForServerValidation (PEAP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
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
ms.openlocfilehash: 168ce6e371495901f2ed93fb69b605a807bc363c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524813"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a><span data-ttu-id="feb1f-106">DisableUserPromptForServerValidation (ServerValidationParameters), élément (PEAP)</span><span class="sxs-lookup"><span data-stu-id="feb1f-106">DisableUserPromptForServerValidation (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="feb1f-107">L’élément **DisableUserPromptForServerValidation (ServerValidationParameters)** indique si la validation du serveur doit être demandée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="feb1f-107">The **DisableUserPromptForServerValidation (ServerValidationParameters)** element indicates whether the user should be asked for server validation.</span></span>

<span data-ttu-id="feb1f-108">Si **DisableUserPromptForServerValidation** a la valeur true, EAP-TLS effectue la validation du serveur sans entrée d’utilisateur ; Si la validation échoue, l’authentification EAP-TLS échoue.</span><span class="sxs-lookup"><span data-stu-id="feb1f-108">If **DisableUserPromptForServerValidation** is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <span data-ttu-id="feb1f-109">Si **DisableUserPromptForServerValidation** a la valeur false, l’utilisateur est invité à fournir un certificat ou un nom de serveur validé, ou une autorité de certification racine.</span><span class="sxs-lookup"><span data-stu-id="feb1f-109">If **DisableUserPromptForServerValidation** is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span>

<span data-ttu-id="feb1f-110">L’élément **DisableUserPromptForServerValidation** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="feb1f-110">The **DisableUserPromptForServerValidation** element is optional.</span></span>

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

<span data-ttu-id="feb1f-111">L’élément **DisableUserPromptForServerValidation** est défini par le type complexe [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="feb1f-111">The **DisableUserPromptForServerValidation** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb1f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="feb1f-112">Requirements</span></span>



| <span data-ttu-id="feb1f-113">Role</span><span class="sxs-lookup"><span data-stu-id="feb1f-113">Role</span></span> | <span data-ttu-id="feb1f-114">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="feb1f-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="feb1f-115">Client</span><span class="sxs-lookup"><span data-stu-id="feb1f-115">Client</span></span><br/> | <span data-ttu-id="feb1f-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="feb1f-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="feb1f-117">Serveur</span><span class="sxs-lookup"><span data-stu-id="feb1f-117">Server</span></span><br/> | <span data-ttu-id="feb1f-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="feb1f-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="feb1f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="feb1f-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="feb1f-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="feb1f-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="feb1f-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="feb1f-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="feb1f-122">**Éléments parents immédiats possibles dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="feb1f-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="feb1f-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="feb1f-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="feb1f-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="feb1f-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="feb1f-125">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="feb1f-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="feb1f-126">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="feb1f-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="feb1f-127">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="feb1f-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





