---
description: Détermine quand WMI doit libérer un fournisseur de consommateur d’événements.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545150"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a><span data-ttu-id="e45ee-103">\_\_EventConsumerProviderCacheControl, classe</span><span class="sxs-lookup"><span data-stu-id="e45ee-103">\_\_EventConsumerProviderCacheControl class</span></span>

<span data-ttu-id="e45ee-104">La classe système **\_ \_ EventConsumerProviderCacheControl** détermine quand WMI doit libérer un fournisseur de consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="e45ee-104">The **\_\_EventConsumerProviderCacheControl** system class determines when WMI should release an event consumer provider.</span></span> <span data-ttu-id="e45ee-105">La classe **\_ \_ EventConsumerProviderCacheControl** est une classe singleton.</span><span class="sxs-lookup"><span data-stu-id="e45ee-105">The **\_\_EventConsumerProviderCacheControl** class is a singleton class.</span></span> <span data-ttu-id="e45ee-106">Il se trouve uniquement dans l' \\ espace de noms racine.</span><span class="sxs-lookup"><span data-stu-id="e45ee-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="e45ee-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e45ee-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e45ee-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e45ee-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e45ee-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e45ee-109">Syntax</span></span>

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="e45ee-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e45ee-110">Members</span></span>

<span data-ttu-id="e45ee-111">La classe **\_ \_ EventConsumerProviderCacheControl** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e45ee-111">The **\_\_EventConsumerProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="e45ee-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e45ee-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e45ee-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e45ee-113">Properties</span></span>

<span data-ttu-id="e45ee-114">La classe **\_ \_ EventConsumerProviderCacheControl** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e45ee-114">The **\_\_EventConsumerProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e45ee-115">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="e45ee-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e45ee-116">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e45ee-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e45ee-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e45ee-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e45ee-118">Intervalle de temps après lequel WMI libère un fournisseur de consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="e45ee-118">Time interval after which WMI releases an event consumer provider.</span></span> <span data-ttu-id="e45ee-119">Le déchargement du fournisseur peut prendre jusqu’à deux fois l’intervalle spécifié.</span><span class="sxs-lookup"><span data-stu-id="e45ee-119">It may take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="e45ee-120">L’heure est au [format d’intervalle](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="e45ee-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e45ee-121">Notes</span><span class="sxs-lookup"><span data-stu-id="e45ee-121">Remarks</span></span>

<span data-ttu-id="e45ee-122">La classe **\_ \_ EventConsumerProviderCacheControl** est dérivée de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="e45ee-122">The **\_\_EventConsumerProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="e45ee-123">Pour plus d’informations sur l’utilisation de cette classe, consultez [déchargement d’un fournisseur](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e45ee-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e45ee-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e45ee-124">Requirements</span></span>



| <span data-ttu-id="e45ee-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e45ee-125">Requirement</span></span> | <span data-ttu-id="e45ee-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e45ee-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e45ee-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e45ee-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e45ee-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e45ee-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e45ee-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e45ee-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e45ee-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e45ee-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e45ee-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e45ee-131">Namespace</span></span><br/>                | <span data-ttu-id="e45ee-132">Root</span><span class="sxs-lookup"><span data-stu-id="e45ee-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="e45ee-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e45ee-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e45ee-134">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="e45ee-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




