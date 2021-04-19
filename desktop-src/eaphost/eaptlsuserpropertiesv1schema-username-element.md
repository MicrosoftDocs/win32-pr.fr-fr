---
title: Élément username (TLS)
description: En savoir plus sur l’élément username. Cet élément capture le nom d’utilisateur à envoyer dans la réponse EAP-Identity.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Élément username EAPHost
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
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106511513"
---
# <a name="username-element-tls"></a><span data-ttu-id="ac21f-105">Élément username (TLS)</span><span class="sxs-lookup"><span data-stu-id="ac21f-105">Username element (TLS)</span></span>

<span data-ttu-id="ac21f-106">L’élément **username** capture le nom d’utilisateur à envoyer dans la réponse EAP-Identity.</span><span class="sxs-lookup"><span data-stu-id="ac21f-106">The **Username** element captures the user name to be sent in the EAP-Identity response.</span></span>

<span data-ttu-id="ac21f-107">Si l’élément **username** est absent, EAP-TLS utilise le nom figurant dans le certificat auquel il est fait appel dans l’élément [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ac21f-107">If the **Username** element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a><span data-ttu-id="ac21f-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac21f-108">Requirements</span></span>



| <span data-ttu-id="ac21f-109">Role</span><span class="sxs-lookup"><span data-stu-id="ac21f-109">Role</span></span> | <span data-ttu-id="ac21f-110">Versions de système d’exploitation minimales prises en charge</span><span class="sxs-lookup"><span data-stu-id="ac21f-110">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="ac21f-111">Client</span><span class="sxs-lookup"><span data-stu-id="ac21f-111">Client</span></span><br/> | <span data-ttu-id="ac21f-112">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac21f-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ac21f-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="ac21f-113">Server</span></span><br/> | <span data-ttu-id="ac21f-114">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac21f-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac21f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac21f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac21f-116">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="ac21f-116">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ac21f-117">Schéma eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ac21f-117">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





