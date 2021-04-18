---
title: Élément EapType (propriétés de l’utilisateur de base)
description: En savoir plus sur l’élément EapType. Cet élément capture la configuration spécifique à la méthode à l’intérieur de l’élément EAP. | Élément EapType (propriétés de l’utilisateur de base)
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
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
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106536435"
---
# <a name="eaptype-element-base-user-properties"></a><span data-ttu-id="383eb-106">Élément EapType (propriétés de l’utilisateur de base)</span><span class="sxs-lookup"><span data-stu-id="383eb-106">EapType element (base user properties)</span></span>

<span data-ttu-id="383eb-107">L’élément **EapType** capture la configuration spécifique à la méthode à l’intérieur de l’élément EAP.</span><span class="sxs-lookup"><span data-stu-id="383eb-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="383eb-108">Notes</span><span class="sxs-lookup"><span data-stu-id="383eb-108">Remarks</span></span>

<span data-ttu-id="383eb-109">L’élément **EapType** est abstrait ; chaque méthode doit définir et utiliser un élément dérivé dans les documents d’instance.</span><span class="sxs-lookup"><span data-stu-id="383eb-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="383eb-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="383eb-110">Requirements</span></span>



| <span data-ttu-id="383eb-111">Role</span><span class="sxs-lookup"><span data-stu-id="383eb-111">Role</span></span> | <span data-ttu-id="383eb-112">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="383eb-112">Minimum supported OS version</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="383eb-113">Client</span><span class="sxs-lookup"><span data-stu-id="383eb-113">Client</span></span><br/> | <span data-ttu-id="383eb-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="383eb-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="383eb-115">Serveur</span><span class="sxs-lookup"><span data-stu-id="383eb-115">Server</span></span><br/> | <span data-ttu-id="383eb-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="383eb-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="383eb-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="383eb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="383eb-118">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="383eb-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="383eb-119">Schéma baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="383eb-119">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





