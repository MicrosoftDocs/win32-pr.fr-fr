---
title: Élément Identity
description: En savoir plus sur l’élément d’identité EAPHost. Cet élément capture l’identité utilisée pour l’authentification.
ms.assetid: 464979f0-6a2b-43e7-a207-2fbd1e2e5f51
keywords:
- Identity, élément EAPHost
topic_type:
- apiref
api_name:
- Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 485d576155d5ac63df2776016f3aafabf8c18c25
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463726"
---
# <a name="identity-element"></a><span data-ttu-id="82ad2-105">Élément Identity</span><span class="sxs-lookup"><span data-stu-id="82ad2-105">Identity Element</span></span>

<span data-ttu-id="82ad2-106">L’élément **Identity** capture l’identité utilisée pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="82ad2-106">The **Identity** element captures the identity used for authentication.</span></span>

``` syntax
<xs:element name="Identity"
    type="string"
 />
```

## <a name="remarks"></a><span data-ttu-id="82ad2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="82ad2-107">Remarks</span></span>

<span data-ttu-id="82ad2-108">L’élément **Identity** est abstrait ; chaque méthode doit définir et utiliser un élément dérivé dans les documents d’instance.</span><span class="sxs-lookup"><span data-stu-id="82ad2-108">The **Identity** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ad2-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82ad2-109">Requirements</span></span>



| <span data-ttu-id="82ad2-110">Role</span><span class="sxs-lookup"><span data-stu-id="82ad2-110">Role</span></span> | <span data-ttu-id="82ad2-111">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="82ad2-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="82ad2-112">Client</span><span class="sxs-lookup"><span data-stu-id="82ad2-112">Client</span></span><br/> | <span data-ttu-id="82ad2-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82ad2-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="82ad2-114">Serveur</span><span class="sxs-lookup"><span data-stu-id="82ad2-114">Server</span></span><br/> | <span data-ttu-id="82ad2-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82ad2-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82ad2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82ad2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ad2-117">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="82ad2-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="82ad2-118">Schéma baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="82ad2-118">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





