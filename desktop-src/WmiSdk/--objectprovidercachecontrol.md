---
description: Contrôle quand une classe ou un fournisseur d’instance est déchargé.
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: Classe __ObjectProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 53cfaa69afead4f436879f128a4d42e50d36fe67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535566"
---
# <a name="__objectprovidercachecontrol-class"></a><span data-ttu-id="de94b-103">\_\_ObjectProviderCacheControl, classe</span><span class="sxs-lookup"><span data-stu-id="de94b-103">\_\_ObjectProviderCacheControl class</span></span>

<span data-ttu-id="de94b-104">La classe système **\_ \_ ObjectProviderCacheControl** contrôle quand une classe ou un fournisseur d’instance est déchargé.</span><span class="sxs-lookup"><span data-stu-id="de94b-104">The **\_\_ObjectProviderCacheControl** system class controls when a class or instance provider is unloaded.</span></span> <span data-ttu-id="de94b-105">Il se trouve uniquement dans l' \\ espace de noms racine.</span><span class="sxs-lookup"><span data-stu-id="de94b-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="de94b-106">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="de94b-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="de94b-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="de94b-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="de94b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de94b-108">Syntax</span></span>

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="de94b-109">Membres</span><span class="sxs-lookup"><span data-stu-id="de94b-109">Members</span></span>

<span data-ttu-id="de94b-110">La classe **\_ \_ ObjectProviderCacheControl** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="de94b-110">The **\_\_ObjectProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="de94b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de94b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de94b-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de94b-112">Properties</span></span>

<span data-ttu-id="de94b-113">La classe **\_ \_ ObjectProviderCacheControl** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="de94b-113">The **\_\_ObjectProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de94b-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="de94b-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de94b-115">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="de94b-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="de94b-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de94b-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="de94b-117">Intervalle de temps après lequel WMI libère une instance, une classe ou un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="de94b-117">Time interval after which WMI releases an instance, class, or method provider.</span></span> <span data-ttu-id="de94b-118">L’heure est au [format d’intervalle](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="de94b-118">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de94b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="de94b-119">Remarks</span></span>

<span data-ttu-id="de94b-120">La classe **\_ \_ ObjectProviderCacheControl** est dérivée de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="de94b-120">The **\_\_ObjectProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="de94b-121">Pour plus d’informations sur l’utilisation de cette classe, consultez [déchargement d’un fournisseur](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="de94b-121">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de94b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de94b-122">Requirements</span></span>



| <span data-ttu-id="de94b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de94b-123">Requirement</span></span> | <span data-ttu-id="de94b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="de94b-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="de94b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de94b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="de94b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de94b-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="de94b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de94b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="de94b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de94b-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="de94b-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="de94b-129">Namespace</span></span><br/>                | <span data-ttu-id="de94b-130">Root</span><span class="sxs-lookup"><span data-stu-id="de94b-130">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="de94b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de94b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de94b-132">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="de94b-132">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="de94b-133">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="de94b-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="de94b-134">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="de94b-134">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

