---
description: Contrôle le cache lorsqu’un fournisseur de propriétés est déchargé.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: Classe __PropertyProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203162"
---
# <a name="__propertyprovidercachecontrol-class"></a><span data-ttu-id="8cbd7-103">\_\_PropertyProviderCacheControl, classe</span><span class="sxs-lookup"><span data-stu-id="8cbd7-103">\_\_PropertyProviderCacheControl class</span></span>

<span data-ttu-id="8cbd7-104">La classe **\_ \_ PropertyProviderCacheControl** contrôle le cache lorsqu’un fournisseur de propriétés est déchargé.</span><span class="sxs-lookup"><span data-stu-id="8cbd7-104">The **\_\_PropertyProviderCacheControl** class controls the cache when a property provider is unloaded.</span></span> <span data-ttu-id="8cbd7-105">Cette classe existe uniquement dans l' \\ espace de noms racine.</span><span class="sxs-lookup"><span data-stu-id="8cbd7-105">This class exists only in the \\root namespace.</span></span>

<span data-ttu-id="8cbd7-106">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8cbd7-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8cbd7-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8cbd7-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cbd7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cbd7-108">Syntax</span></span>

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="8cbd7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8cbd7-109">Members</span></span>

<span data-ttu-id="8cbd7-110">La classe **\_ \_ PropertyProviderCacheControl** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8cbd7-110">The **\_\_PropertyProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="8cbd7-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8cbd7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8cbd7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8cbd7-112">Properties</span></span>

<span data-ttu-id="8cbd7-113">La classe **\_ \_ PropertyProviderCacheControl** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8cbd7-113">The **\_\_PropertyProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8cbd7-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="8cbd7-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd7-115">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8cbd7-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd7-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8cbd7-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8cbd7-117">Intervalle de temps après la libération par WMI d’un fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8cbd7-117">Time interval after WMI releases a property provider.</span></span> <span data-ttu-id="8cbd7-118">L’heure est au format intervalle.</span><span class="sxs-lookup"><span data-stu-id="8cbd7-118">The time is in the interval format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cbd7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8cbd7-119">Remarks</span></span>

<span data-ttu-id="8cbd7-120">La classe **\_ \_ PropertyProviderCacheControl** est dérivée de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="8cbd7-120">The **\_\_PropertyProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="8cbd7-121">Pour plus d’informations, consultez [déchargement d’un fournisseur](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8cbd7-121">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8cbd7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cbd7-122">Requirements</span></span>



| <span data-ttu-id="8cbd7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cbd7-123">Requirement</span></span> | <span data-ttu-id="8cbd7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cbd7-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8cbd7-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cbd7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8cbd7-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cbd7-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8cbd7-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cbd7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8cbd7-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cbd7-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8cbd7-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8cbd7-129">Namespace</span></span><br/>                | <span data-ttu-id="8cbd7-130">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="8cbd7-130">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8cbd7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cbd7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cbd7-132">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="8cbd7-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




