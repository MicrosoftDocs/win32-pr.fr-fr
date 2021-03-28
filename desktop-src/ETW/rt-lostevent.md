---
description: Cette classe de type d’événement est utilisée pour indiquer que les événements ont été perdus dans une session en temps réel. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: Classe RT_LostEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526385"
---
# <a name="rt_lostevent-class"></a><span data-ttu-id="d8406-104">RT \_ LostEvent, classe</span><span class="sxs-lookup"><span data-stu-id="d8406-104">RT\_LostEvent class</span></span>

<span data-ttu-id="d8406-105">Cette classe de type d’événement est utilisée pour indiquer que les événements ont été perdus dans une session en temps réel.</span><span class="sxs-lookup"><span data-stu-id="d8406-105">This event type class is used to indicate that events were lost in a real-time session.</span></span>

<span data-ttu-id="d8406-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="d8406-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8406-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8406-107">Syntax</span></span>

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a><span data-ttu-id="d8406-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d8406-108">Members</span></span>

<span data-ttu-id="d8406-109">La classe **RT \_ LostEvent** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="d8406-109">The **RT\_LostEvent** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8406-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d8406-110">Remarks</span></span>

<span data-ttu-id="d8406-111">Le type d’événement RTLostEvent indique qu’un ou plusieurs événements ont été perdus.</span><span class="sxs-lookup"><span data-stu-id="d8406-111">The RTLostEvent event type indicates that one or more events were lost.</span></span> <span data-ttu-id="d8406-112">Le type d’événement RTLostBuffer indique qu’une ou plusieurs mémoires tampons ont été perdues.</span><span class="sxs-lookup"><span data-stu-id="d8406-112">The RTLostBuffer event type indicates that one or more buffers were lost.</span></span> <span data-ttu-id="d8406-113">Les types d’événements RTLostEvent et RTLostBuffer sont remis avant le traitement des événements de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d8406-113">The RTLostEvent and RTLostBuffer event types are delivered before processing events from the buffer.</span></span>

<span data-ttu-id="d8406-114">RTLostFile indique que le fichier de stockage utilisé par le journal automatique pour capturer les événements a été perdu.</span><span class="sxs-lookup"><span data-stu-id="d8406-114">The RTLostFile indicates that the backing file used by the AutoLogger to capture events was lost.</span></span>

<span data-ttu-id="d8406-115">Le fait de perdre des événements dépend de la fréquence à laquelle les événements sont journalisés et du temps passé par le consommateur à traiter les événements.</span><span class="sxs-lookup"><span data-stu-id="d8406-115">Loosing events depends on the frequency with which the events are logged and how much time the consumer spends processing the events.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8406-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d8406-116">Requirements</span></span>



| <span data-ttu-id="d8406-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8406-117">Requirement</span></span> | <span data-ttu-id="d8406-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8406-118">Value</span></span> |
|-------------------------------------|------------------------------------------------|
| <span data-ttu-id="d8406-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8406-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d8406-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8406-120">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d8406-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8406-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d8406-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8406-122">None supported</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="d8406-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8406-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8406-124">**\_Événement perdu**</span><span class="sxs-lookup"><span data-stu-id="d8406-124">**Lost\_Event**</span></span>](lost-event.md)
</dt> </dl>

 

 




