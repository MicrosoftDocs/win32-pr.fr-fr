---
description: La classe est la classe de base abstraite pour les classes utilisées pour déterminer quand WMI doit libérer un objet COM (Component Object Model).
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: Classe __CacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522073"
---
# <a name="__cachecontrol-class"></a><span data-ttu-id="5104f-103">\_\_CacheControl, classe</span><span class="sxs-lookup"><span data-stu-id="5104f-103">\_\_CacheControl class</span></span>

<span data-ttu-id="5104f-104">La classe système **\_ \_ CacheControl** est la classe de base abstraite pour les classes utilisées pour déterminer quand WMI doit libérer un objet COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="5104f-104">The **\_\_CacheControl** system class is the abstract base class for classes that are used to determine when WMI should release a Component Object Model (COM) object.</span></span> <span data-ttu-id="5104f-105">Les instances de cette classe ne sont jamais créées.</span><span class="sxs-lookup"><span data-stu-id="5104f-105">Instances of this class are never created.</span></span> <span data-ttu-id="5104f-106">La classe **\_ \_ CacheControl** se trouve uniquement dans l’espace de noms racine.</span><span class="sxs-lookup"><span data-stu-id="5104f-106">The **\_\_CacheControl** class is located only in the root namespace.</span></span> <span data-ttu-id="5104f-107">Pour plus d’informations sur l’utilisation de cette classe, consultez [déchargement d’un fournisseur](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5104f-107">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

<span data-ttu-id="5104f-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5104f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5104f-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5104f-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5104f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5104f-110">Syntax</span></span>

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a><span data-ttu-id="5104f-111">Membres</span><span class="sxs-lookup"><span data-stu-id="5104f-111">Members</span></span>

<span data-ttu-id="5104f-112">La classe **\_ \_ CacheControl** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="5104f-112">The **\_\_CacheControl** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="5104f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5104f-113">Remarks</span></span>

<span data-ttu-id="5104f-114">La classe **\_ \_ CacheControl** est dérivée de [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="5104f-114">The **\_\_CacheControl** class is derived from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5104f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5104f-115">Requirements</span></span>



| <span data-ttu-id="5104f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5104f-116">Requirement</span></span> | <span data-ttu-id="5104f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5104f-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5104f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5104f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5104f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5104f-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5104f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5104f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5104f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5104f-121">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5104f-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5104f-122">Namespace</span></span><br/>                | <span data-ttu-id="5104f-123">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="5104f-123">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5104f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5104f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5104f-125">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="5104f-125">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="5104f-126">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="5104f-126">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5104f-127">**\_\_EventConsumerProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="5104f-127">**\_\_EventConsumerProviderCacheControl**</span></span>](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="5104f-128">**\_\_EventProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="5104f-128">**\_\_EventProviderCacheControl**</span></span>](--eventprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="5104f-129">**\_\_EventSinkCacheControl**</span><span class="sxs-lookup"><span data-stu-id="5104f-129">**\_\_EventSinkCacheControl**</span></span>](--eventsinkcachecontrol.md)
</dt> <dt>

[<span data-ttu-id="5104f-130">**\_\_ObjectProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="5104f-130">**\_\_ObjectProviderCacheControl**</span></span>](--objectprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="5104f-131">\_\_PropertyProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="5104f-131">\_\_PropertyProviderCacheControl</span></span>](--propertyprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="5104f-132">Déchargement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="5104f-132">Unloading a Provider</span></span>](unloading-a-provider.md)
</dt> </dl>

 

