---
description: Cette classe est la classe parente pour les événements de suivi de pile.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: StackWalk, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972183"
---
# <a name="stackwalk-class"></a><span data-ttu-id="0e2c0-103">StackWalk, classe</span><span class="sxs-lookup"><span data-stu-id="0e2c0-103">StackWalk class</span></span>

<span data-ttu-id="0e2c0-104">Cette classe est la classe parente pour les événements de suivi de pile.</span><span class="sxs-lookup"><span data-stu-id="0e2c0-104">This class is the parent class for stack tracing events.</span></span>

<span data-ttu-id="0e2c0-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0e2c0-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e2c0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e2c0-106">Syntax</span></span>

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="0e2c0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0e2c0-107">Members</span></span>

<span data-ttu-id="0e2c0-108">La classe **StackWalk** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="0e2c0-108">The **StackWalk** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e2c0-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0e2c0-109">Remarks</span></span>

<span data-ttu-id="0e2c0-110">Pour activer le suivi de pile des événements de noyau, appelez la fonction [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) et spécifiez les événements de noyau et les types pour lesquels vous souhaitez capturer la trace de la pile.</span><span class="sxs-lookup"><span data-stu-id="0e2c0-110">To enable stack tracing of kernel events, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function and specify the kernel events and types for which you want to capture the stack trace.</span></span> <span data-ttu-id="0e2c0-111">Pour activer le suivi de pile pour d’autres événements, définissez le membre **EnableProperty** de l' [**activation des \_ \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) sur **événement activer la trace de la \_ \_ \_ pile \_ de propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0e2c0-111">To enable stack tracing for other events, set the **EnableProperty** member of [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) to **EVENT\_ENABLE\_PROPERTY\_STACK\_TRACE**.</span></span>

<span data-ttu-id="0e2c0-112">Utilisez le type d’événement suivant pour identifier l’événement réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="0e2c0-112">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="0e2c0-113">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="0e2c0-113">Event type</span></span>           | <span data-ttu-id="0e2c0-114">Description</span><span class="sxs-lookup"><span data-stu-id="0e2c0-114">Description</span></span>                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e2c0-115">Valeur de type d’événement, 32</span><span class="sxs-lookup"><span data-stu-id="0e2c0-115">Event type value, 32</span></span> | <span data-ttu-id="0e2c0-116">Événement de suivi de pile.</span><span class="sxs-lookup"><span data-stu-id="0e2c0-116">Stack tracing event.</span></span> <span data-ttu-id="0e2c0-117">La classe MOF de l' [**\_ événement StackWalk**](stackwalk-event.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="0e2c0-117">The [**StackWalk\_Event**](stackwalk-event.md) MOF class defines the event data for this event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0e2c0-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0e2c0-118">Requirements</span></span>



| <span data-ttu-id="0e2c0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e2c0-119">Requirement</span></span> | <span data-ttu-id="0e2c0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e2c0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0e2c0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e2c0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e2c0-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e2c0-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0e2c0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e2c0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e2c0-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e2c0-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 
