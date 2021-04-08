---
title: Élément User
description: En savoir plus sur l’élément utilisateur. Cet élément n’est pas utilisé lors de l’utilisation de méthodes héritées via les API EAPHost.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- Élément utilisateur EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730364"
---
# <a name="user-element"></a><span data-ttu-id="ffe24-105">Élément User</span><span class="sxs-lookup"><span data-stu-id="ffe24-105">User Element</span></span>

<span data-ttu-id="ffe24-106">L’élément **User** n’est pas utilisé lors de l’utilisation de méthodes héritées via les API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="ffe24-106">The **User** element is not used when using legacy methods via the EAPHost APIs.</span></span>

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="ffe24-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ffe24-107">Child elements</span></span>



| <span data-ttu-id="ffe24-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ffe24-108">Element</span></span>                                                  | <span data-ttu-id="ffe24-109">Type</span><span class="sxs-lookup"><span data-stu-id="ffe24-109">Type</span></span> | <span data-ttu-id="ffe24-110">Description</span><span class="sxs-lookup"><span data-stu-id="ffe24-110">Description</span></span>                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="ffe24-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="ffe24-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md) |      | <span data-ttu-id="ffe24-112">Capture les informations d’identification spécifiques au type de méthode et à la méthode.</span><span class="sxs-lookup"><span data-stu-id="ffe24-112">Captures the method type and method specific credential information.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ffe24-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffe24-113">Requirements</span></span>



| <span data-ttu-id="ffe24-114">Role</span><span class="sxs-lookup"><span data-stu-id="ffe24-114">Role</span></span> | <span data-ttu-id="ffe24-115">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="ffe24-115">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="ffe24-116">Client</span><span class="sxs-lookup"><span data-stu-id="ffe24-116">Client</span></span><br/> | <span data-ttu-id="ffe24-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffe24-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ffe24-118">Serveur</span><span class="sxs-lookup"><span data-stu-id="ffe24-118">Server</span></span><br/> | <span data-ttu-id="ffe24-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffe24-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ffe24-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffe24-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe24-121">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="ffe24-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ffe24-122">Schéma eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ffe24-122">eapuserpropertiesv1 Schema</span></span>](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





