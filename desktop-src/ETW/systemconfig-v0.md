---
description: 'Classe SystemConfig_V0 : cette classe est la classe parente pour les événements de configuration matérielle. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: 9da1a7ec-89b5-462b-a336-544e4b7adf96
title: Classe SystemConfig_V0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0
api_type:
- NA
api_location: ''
ms.openlocfilehash: 24f0c579f4fb9c947ea02ff677cd433da3103cfc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105907"
---
# <a name="systemconfig_v0-class"></a><span data-ttu-id="e7296-104">SystemConfig \_ v0 (classe)</span><span class="sxs-lookup"><span data-stu-id="e7296-104">SystemConfig\_V0 class</span></span>

<span data-ttu-id="e7296-105">Cette classe est la classe parente pour les événements de configuration matérielle.</span><span class="sxs-lookup"><span data-stu-id="e7296-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="e7296-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="e7296-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7296-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7296-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="e7296-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e7296-108">Members</span></span>

<span data-ttu-id="e7296-109">La classe **SystemConfig \_ v0** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="e7296-109">The **SystemConfig\_V0** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7296-110">Notes </span><span class="sxs-lookup"><span data-stu-id="e7296-110">Remarks</span></span>

<span data-ttu-id="e7296-111">Pour les événements de configuration matérielle sur Windows XP, consultez la classe [**HWConfig**](hwconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="e7296-111">For hardware configuration events on Windows XP, see the [**HWConfig**](hwconfig.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7296-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7296-112">Requirements</span></span>



| <span data-ttu-id="e7296-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7296-113">Requirement</span></span> | <span data-ttu-id="e7296-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7296-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7296-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7296-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e7296-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7296-116">None supported</span></span><br/>                            |
| <span data-ttu-id="e7296-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7296-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e7296-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7296-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7296-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7296-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7296-120">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="e7296-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="e7296-121">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="e7296-121">**SystemConfig**</span></span>](systemconfig.md)
</dt> <dt>

[<span data-ttu-id="e7296-122">**\_Processeur SystemConfig v0 \_**</span><span class="sxs-lookup"><span data-stu-id="e7296-122">**SystemConfig\_V0\_CPU**</span></span>](systemconfig-v0-cpu.md)
</dt> <dt>

[<span data-ttu-id="e7296-123">**SystemConfig \_ v0 \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="e7296-123">**SystemConfig\_V0\_LogDisk**</span></span>](systemconfig-v0-logdisk.md)
</dt> <dt>

[<span data-ttu-id="e7296-124">**\_ \_ Carte réseau SystemConfig v0**</span><span class="sxs-lookup"><span data-stu-id="e7296-124">**SystemConfig\_V0\_NIC**</span></span>](systemconfig-v0-nic.md)
</dt> <dt>

[<span data-ttu-id="e7296-125">**SystemConfig \_ v0 \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="e7296-125">**SystemConfig\_V0\_PhyDisk**</span></span>](systemconfig-v0-phydisk.md)
</dt> <dt>

[<span data-ttu-id="e7296-126">**SystemConfig \_ v0 \_**</span><span class="sxs-lookup"><span data-stu-id="e7296-126">**SystemConfig\_V0\_Power**</span></span>](systemconfig-v0-power.md)
</dt> <dt>

[<span data-ttu-id="e7296-127">**\_Services SystemConfig v0 \_**</span><span class="sxs-lookup"><span data-stu-id="e7296-127">**SystemConfig\_V0\_Services**</span></span>](systemconfig-v0-services.md)
</dt> <dt>

[<span data-ttu-id="e7296-128">**\_Vidéo SystemConfig v0 \_**</span><span class="sxs-lookup"><span data-stu-id="e7296-128">**SystemConfig\_V0\_Video**</span></span>](systemconfig-v0-video.md)
</dt> </dl>

 

 




