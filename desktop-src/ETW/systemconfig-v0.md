---
description: Cette classe est la classe parente pour les événements de configuration matérielle. La syntaxe suivante est simplifiée à partir du code MOF.
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
ms.openlocfilehash: 92d77d1ad3effdd2bf22a7df8112187b27666238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864250"
---
# <a name="systemconfig_v0-class"></a><span data-ttu-id="125b3-104">SystemConfig \_ v0 (classe)</span><span class="sxs-lookup"><span data-stu-id="125b3-104">SystemConfig\_V0 class</span></span>

<span data-ttu-id="125b3-105">Cette classe est la classe parente pour les événements de configuration matérielle.</span><span class="sxs-lookup"><span data-stu-id="125b3-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="125b3-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="125b3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="125b3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="125b3-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="125b3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="125b3-108">Members</span></span>

<span data-ttu-id="125b3-109">La classe **SystemConfig \_ v0** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="125b3-109">The **SystemConfig\_V0** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="125b3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="125b3-110">Remarks</span></span>

<span data-ttu-id="125b3-111">Pour les événements de configuration matérielle sur Windows XP, consultez la classe [**HWConfig**](hwconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="125b3-111">For hardware configuration events on Windows XP, see the [**HWConfig**](hwconfig.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="125b3-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="125b3-112">Requirements</span></span>



| <span data-ttu-id="125b3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="125b3-113">Requirement</span></span> | <span data-ttu-id="125b3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="125b3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="125b3-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="125b3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="125b3-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="125b3-116">None supported</span></span><br/>                            |
| <span data-ttu-id="125b3-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="125b3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="125b3-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="125b3-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="125b3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="125b3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="125b3-120">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="125b3-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="125b3-121">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="125b3-121">**SystemConfig**</span></span>](systemconfig.md)
</dt> <dt>

[<span data-ttu-id="125b3-122">**\_Processeur SystemConfig v0 \_**</span><span class="sxs-lookup"><span data-stu-id="125b3-122">**SystemConfig\_V0\_CPU**</span></span>](systemconfig-v0-cpu.md)
</dt> <dt>

[<span data-ttu-id="125b3-123">**SystemConfig \_ v0 \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="125b3-123">**SystemConfig\_V0\_LogDisk**</span></span>](systemconfig-v0-logdisk.md)
</dt> <dt>

[<span data-ttu-id="125b3-124">**\_ \_ Carte réseau SystemConfig v0**</span><span class="sxs-lookup"><span data-stu-id="125b3-124">**SystemConfig\_V0\_NIC**</span></span>](systemconfig-v0-nic.md)
</dt> <dt>

[<span data-ttu-id="125b3-125">**SystemConfig \_ v0 \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="125b3-125">**SystemConfig\_V0\_PhyDisk**</span></span>](systemconfig-v0-phydisk.md)
</dt> <dt>

[<span data-ttu-id="125b3-126">**SystemConfig \_ v0 \_**</span><span class="sxs-lookup"><span data-stu-id="125b3-126">**SystemConfig\_V0\_Power**</span></span>](systemconfig-v0-power.md)
</dt> <dt>

[<span data-ttu-id="125b3-127">**\_Services SystemConfig v0 \_**</span><span class="sxs-lookup"><span data-stu-id="125b3-127">**SystemConfig\_V0\_Services**</span></span>](systemconfig-v0-services.md)
</dt> <dt>

[<span data-ttu-id="125b3-128">**\_Vidéo SystemConfig v0 \_**</span><span class="sxs-lookup"><span data-stu-id="125b3-128">**SystemConfig\_V0\_Video**</span></span>](systemconfig-v0-video.md)
</dt> </dl>

 

 




