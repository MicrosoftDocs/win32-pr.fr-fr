---
description: Contrôle le moment où un fournisseur d’événements est déchargé.
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: Classe __EventProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: c54ec47b1f67d96816cf24a6b6e0108ee0b1de70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203742"
---
# <a name="__eventprovidercachecontrol-class"></a><span data-ttu-id="ee80e-103">\_\_EventProviderCacheControl, classe</span><span class="sxs-lookup"><span data-stu-id="ee80e-103">\_\_EventProviderCacheControl class</span></span>

<span data-ttu-id="ee80e-104">La classe système **\_ \_ EventProviderCacheControl** contrôle le moment où un fournisseur d’événements est déchargé.</span><span class="sxs-lookup"><span data-stu-id="ee80e-104">The **\_\_EventProviderCacheControl** system class controls when an event provider is unloaded.</span></span> <span data-ttu-id="ee80e-105">Il se trouve uniquement dans l' \\ espace de noms racine.</span><span class="sxs-lookup"><span data-stu-id="ee80e-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="ee80e-106">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ee80e-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ee80e-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ee80e-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee80e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee80e-108">Syntax</span></span>

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="ee80e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ee80e-109">Members</span></span>

<span data-ttu-id="ee80e-110">La classe **\_ \_ EventProviderCacheControl** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ee80e-110">The **\_\_EventProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="ee80e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee80e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee80e-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee80e-112">Properties</span></span>

<span data-ttu-id="ee80e-113">La classe **\_ \_ EventProviderCacheControl** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ee80e-113">The **\_\_EventProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee80e-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="ee80e-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee80e-115">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ee80e-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ee80e-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee80e-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ee80e-117">Intervalle de temps après lequel Windows Management Instrumentation (WMI) libère un fournisseur d’événements.</span><span class="sxs-lookup"><span data-stu-id="ee80e-117">Time interval after Windows Management Instrumentation (WMI) releases an event provider.</span></span> <span data-ttu-id="ee80e-118">L’heure est au [format d’intervalle](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="ee80e-118">The time is in [interval format](interval-format.md).</span></span> <span data-ttu-id="ee80e-119">Le déchargement du fournisseur peut prendre jusqu’à deux fois l’intervalle spécifié.</span><span class="sxs-lookup"><span data-stu-id="ee80e-119">It may take up to twice the interval specified to unload the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee80e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ee80e-120">Remarks</span></span>

<span data-ttu-id="ee80e-121">La classe **\_ \_ EventProviderCacheControl** est dérivée de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="ee80e-121">The **\_\_EventProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span>

<span data-ttu-id="ee80e-122">Pour plus d’informations sur l’utilisation de cette classe, consultez [déchargement d’un fournisseur](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ee80e-122">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee80e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee80e-123">Requirements</span></span>



| <span data-ttu-id="ee80e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee80e-124">Requirement</span></span> | <span data-ttu-id="ee80e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee80e-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ee80e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee80e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ee80e-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee80e-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ee80e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee80e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ee80e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee80e-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ee80e-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ee80e-130">Namespace</span></span><br/>                | <span data-ttu-id="ee80e-131">Root</span><span class="sxs-lookup"><span data-stu-id="ee80e-131">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ee80e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee80e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee80e-133">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="ee80e-133">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="ee80e-134">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="ee80e-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

