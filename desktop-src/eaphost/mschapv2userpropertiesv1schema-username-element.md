---
title: Élément username (CHAP)
description: En savoir plus sur l’élément username, qui identifie l’utilisateur en cours d’authentification. Consultez un exemple de syntaxe et affichez des ressources supplémentaires disponibles.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
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
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941365"
---
# <a name="username-element-chap"></a><span data-ttu-id="d9f42-105">Élément username (CHAP)</span><span class="sxs-lookup"><span data-stu-id="d9f42-105">Username element (CHAP)</span></span>

<span data-ttu-id="d9f42-106">L’élément **username** identifie l’utilisateur authentifié.</span><span class="sxs-lookup"><span data-stu-id="d9f42-106">The **Username** element identifies the user being authenticated.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a><span data-ttu-id="d9f42-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d9f42-107">Remarks</span></span>

<span data-ttu-id="d9f42-108">Si l’élément **username** n’est pas présent, le nom d’utilisateur est obtenu à partir de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="d9f42-108">If the **Username** element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="d9f42-109">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="d9f42-109">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f42-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9f42-110">Requirements</span></span>



| <span data-ttu-id="d9f42-111">Role</span><span class="sxs-lookup"><span data-stu-id="d9f42-111">Role</span></span> | <span data-ttu-id="d9f42-112">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="d9f42-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="d9f42-113">Client</span><span class="sxs-lookup"><span data-stu-id="d9f42-113">Client</span></span><br/> | <span data-ttu-id="d9f42-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9f42-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d9f42-115">Serveur</span><span class="sxs-lookup"><span data-stu-id="d9f42-115">Server</span></span><br/> | <span data-ttu-id="d9f42-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9f42-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9f42-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9f42-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f42-118">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="d9f42-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d9f42-119">Schéma mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="d9f42-119">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





