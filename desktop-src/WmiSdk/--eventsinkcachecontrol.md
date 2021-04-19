---
description: Utilisé pour déterminer à quel moment WMI libère un pointeur IWbemUnboundObjectSink des fournisseurs de consommateur d’événements.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: Classe __EventSinkCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530735"
---
# <a name="__eventsinkcachecontrol-class"></a><span data-ttu-id="6cea9-103">\_\_EventSinkCacheControl, classe</span><span class="sxs-lookup"><span data-stu-id="6cea9-103">\_\_EventSinkCacheControl class</span></span>

<span data-ttu-id="6cea9-104">La classe système **\_ \_ EventSinkCacheControl** permet de déterminer à quel moment WMI libère le pointeur [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) d’un fournisseur de consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="6cea9-104">The **\_\_EventSinkCacheControl** system class is used to determine when WMI releases an event consumer provider's [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) pointer.</span></span> <span data-ttu-id="6cea9-105">La classe **\_ \_ EventSinkCacheControl** est une classe singleton.</span><span class="sxs-lookup"><span data-stu-id="6cea9-105">The **\_\_EventSinkCacheControl** class is a singleton class.</span></span> <span data-ttu-id="6cea9-106">Il se trouve uniquement dans l' \\ espace de noms racine.</span><span class="sxs-lookup"><span data-stu-id="6cea9-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="6cea9-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6cea9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6cea9-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6cea9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cea9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cea9-109">Syntax</span></span>

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="6cea9-110">Membres</span><span class="sxs-lookup"><span data-stu-id="6cea9-110">Members</span></span>

<span data-ttu-id="6cea9-111">La classe **\_ \_ EventSinkCacheControl** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6cea9-111">The **\_\_EventSinkCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="6cea9-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6cea9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6cea9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6cea9-113">Properties</span></span>

<span data-ttu-id="6cea9-114">La classe **\_ \_ EventSinkCacheControl** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6cea9-114">The **\_\_EventSinkCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6cea9-115">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="6cea9-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cea9-116">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6cea9-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6cea9-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6cea9-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6cea9-118">Intervalle de temps après lequel WMI libère un fournisseur d’événements.</span><span class="sxs-lookup"><span data-stu-id="6cea9-118">Time interval after which WMI releases an event provider.</span></span> <span data-ttu-id="6cea9-119">Le déchargement du fournisseur peut prendre jusqu’à deux fois l’intervalle spécifié.</span><span class="sxs-lookup"><span data-stu-id="6cea9-119">It can take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="6cea9-120">L’heure est au [format d’intervalle](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="6cea9-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cea9-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6cea9-121">Remarks</span></span>

<span data-ttu-id="6cea9-122">La classe **\_ \_ EventSinkCacheControl** est dérivée de [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="6cea9-122">The **\_\_EventSinkCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="6cea9-123">Pour plus d’informations sur l’utilisation de cette classe, consultez [déchargement d’un fournisseur](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6cea9-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cea9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cea9-124">Requirements</span></span>



| <span data-ttu-id="6cea9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cea9-125">Requirement</span></span> | <span data-ttu-id="6cea9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cea9-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6cea9-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cea9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6cea9-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6cea9-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6cea9-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cea9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6cea9-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cea9-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6cea9-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6cea9-131">Namespace</span></span><br/>                | <span data-ttu-id="6cea9-132">Root</span><span class="sxs-lookup"><span data-stu-id="6cea9-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="6cea9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cea9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cea9-134">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="6cea9-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




