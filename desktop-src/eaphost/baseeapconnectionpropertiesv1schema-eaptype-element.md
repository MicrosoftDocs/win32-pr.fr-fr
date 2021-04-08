---
title: Élément EapType (propriété de connexion de schéma v1)
description: En savoir plus sur l’élément EapType. Cet élément capture la configuration spécifique à la méthode à l’intérieur de l’élément EAP. | Élément EapType (propriété de connexion de schéma v1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
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
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761660"
---
# <a name="eaptype-element-v1-schema-connection-property"></a><span data-ttu-id="8fa6b-106">Élément EapType (propriété de connexion de schéma v1)</span><span class="sxs-lookup"><span data-stu-id="8fa6b-106">EapType Element (v1 schema connection property)</span></span>

<span data-ttu-id="8fa6b-107">L’élément **EapType** capture la configuration spécifique à la méthode à l’intérieur de l’élément EAP.</span><span class="sxs-lookup"><span data-stu-id="8fa6b-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="8fa6b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="8fa6b-108">Remarks</span></span>

<span data-ttu-id="8fa6b-109">L’élément **EapType** est abstrait ; chaque méthode doit définir et utiliser un élément dérivé dans les documents d’instance.</span><span class="sxs-lookup"><span data-stu-id="8fa6b-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fa6b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fa6b-110">Requirements</span></span>



| <span data-ttu-id="8fa6b-111">Role</span><span class="sxs-lookup"><span data-stu-id="8fa6b-111">Role</span></span> | <span data-ttu-id="8fa6b-112">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="8fa6b-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="8fa6b-113">Client</span><span class="sxs-lookup"><span data-stu-id="8fa6b-113">Client</span></span><br/> | <span data-ttu-id="8fa6b-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fa6b-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8fa6b-115">Serveur</span><span class="sxs-lookup"><span data-stu-id="8fa6b-115">Server</span></span><br/> | <span data-ttu-id="8fa6b-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fa6b-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8fa6b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fa6b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fa6b-118">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="8fa6b-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="8fa6b-119">Schéma baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="8fa6b-119">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





