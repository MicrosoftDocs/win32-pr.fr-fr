---
description: Classe parente pour les événements d’en-tête de journal. Cette classe est toujours la première classe de trace d’événements envoyée à un consommateur (cet événement n’est pas envoyé aux consommateurs en temps réel). La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: EventTraceEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972207"
---
# <a name="eventtraceevent-class"></a><span data-ttu-id="62f7d-105">EventTraceEvent, classe</span><span class="sxs-lookup"><span data-stu-id="62f7d-105">EventTraceEvent class</span></span>

<span data-ttu-id="62f7d-106">Classe parente pour les événements d’en-tête de journal.</span><span class="sxs-lookup"><span data-stu-id="62f7d-106">The parent class for log header events.</span></span> <span data-ttu-id="62f7d-107">Cette classe est toujours la première classe de trace d’événements envoyée à un consommateur (cet événement n’est pas envoyé aux consommateurs en temps réel).</span><span class="sxs-lookup"><span data-stu-id="62f7d-107">This class is always the first event trace class sent to a consumer (this event is not sent to real-time consumers).</span></span>

<span data-ttu-id="62f7d-108">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="62f7d-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f7d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62f7d-109">Syntax</span></span>

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="62f7d-110">Membres</span><span class="sxs-lookup"><span data-stu-id="62f7d-110">Members</span></span>

<span data-ttu-id="62f7d-111">La classe **EventTraceEvent** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="62f7d-111">The **EventTraceEvent** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="62f7d-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="62f7d-112">Requirements</span></span>



| <span data-ttu-id="62f7d-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62f7d-113">Requirement</span></span> | <span data-ttu-id="62f7d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="62f7d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="62f7d-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62f7d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="62f7d-116">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62f7d-116">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="62f7d-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62f7d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="62f7d-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62f7d-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62f7d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62f7d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f7d-120">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="62f7d-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="62f7d-121">**\_En-tête EventTrace**</span><span class="sxs-lookup"><span data-stu-id="62f7d-121">**EventTrace\_Header**</span></span>](eventtrace-header.md)
</dt> </dl>

 

 




