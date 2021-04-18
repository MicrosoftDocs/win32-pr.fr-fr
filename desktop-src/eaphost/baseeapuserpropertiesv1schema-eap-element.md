---
title: Élément EAP (propriété utilisateur)
description: En savoir plus sur l’élément EAP. Cet élément capture le type de méthode sélectionné et la configuration spécifique à la méthode. | Élément EAP (propriété utilisateur)
ms.assetid: 4adef133-1d18-444a-baa3-5419b8cbe298
keywords:
- Élément EAP EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23f00b5162ddb42efd9fae759bab1ea47efc04dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522922"
---
# <a name="eap-element-user-property"></a><span data-ttu-id="b8500-106">Élément EAP (propriété utilisateur)</span><span class="sxs-lookup"><span data-stu-id="b8500-106">Eap element (user property)</span></span>

<span data-ttu-id="b8500-107">L’élément **EAP** capture le type de méthode sélectionné et la configuration spécifique à la méthode.</span><span class="sxs-lookup"><span data-stu-id="b8500-107">The **Eap** element captures the method type selected and method-specific configuration.</span></span>

``` syntax
<xs:element name="Eap"
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="b8500-108">Notes</span><span class="sxs-lookup"><span data-stu-id="b8500-108">Remarks</span></span>

<span data-ttu-id="b8500-109">La méthode peut définir les éléments constitutifs à l’intérieur de l’élément **EAP** .</span><span class="sxs-lookup"><span data-stu-id="b8500-109">The method can define the constituent elements inside the **Eap** element.</span></span> <span data-ttu-id="b8500-110">La méthode effectue également une validation de schéma sur les éléments dans **EAP**.</span><span class="sxs-lookup"><span data-stu-id="b8500-110">The method also performs schema validation on the elements in **Eap**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8500-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8500-111">Requirements</span></span>



| <span data-ttu-id="b8500-112">Role</span><span class="sxs-lookup"><span data-stu-id="b8500-112">Role</span></span> | <span data-ttu-id="b8500-113">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="b8500-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="b8500-114">Client</span><span class="sxs-lookup"><span data-stu-id="b8500-114">Client</span></span><br/> | <span data-ttu-id="b8500-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8500-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8500-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="b8500-116">Server</span></span><br/> | <span data-ttu-id="b8500-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8500-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8500-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8500-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8500-119">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="b8500-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b8500-120">Schéma baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b8500-120">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





