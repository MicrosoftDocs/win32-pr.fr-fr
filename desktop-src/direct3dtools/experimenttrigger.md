---
description: Représente des informations sur le déclencheur d’expérimentation.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ExperimentTrigger, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846213"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span data-ttu-id="59177-103"><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger, structure</span><span class="sxs-lookup"><span data-stu-id="59177-103"><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger structure</span></span>

<span data-ttu-id="59177-104">Représente des informations sur le déclencheur d’expérimentation.</span><span class="sxs-lookup"><span data-stu-id="59177-104">Represents experiment trigger information.</span></span>

## <a name="syntax"></a><span data-ttu-id="59177-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59177-105">Syntax</span></span>


```C++
} ExperimentTrigger;
```

## <a name="members"></a><span data-ttu-id="59177-106">Membres</span><span class="sxs-lookup"><span data-stu-id="59177-106">Members</span></span>

<span data-ttu-id="59177-107">**type**</span><span class="sxs-lookup"><span data-stu-id="59177-107">**type**</span></span>  
<span data-ttu-id="59177-108">Type d’expérimentation (capture) déclenché.</span><span class="sxs-lookup"><span data-stu-id="59177-108">The kind of experiment (capture) triggered.</span></span>

<span data-ttu-id="59177-109">**key**</span><span class="sxs-lookup"><span data-stu-id="59177-109">**key**</span></span>  
<span data-ttu-id="59177-110">Lorsque le type est égal à EXPERIMENTTRIGGERTYPE :: KEY, la clé utilisée pour déclencher la capture.</span><span class="sxs-lookup"><span data-stu-id="59177-110">When type is equal to EXPERIMENTTRIGGERTYPE::KEY, the key used to trigger capture.</span></span>

<span data-ttu-id="59177-111">**frameNumber**</span><span class="sxs-lookup"><span data-stu-id="59177-111">**frameNumber**</span></span>  
<span data-ttu-id="59177-112">Lorsque le type est égal à EXPERIMENTTRIGGERTYPE :: FRAMENUMBER, numéro de frame qui déclenchera la capture.</span><span class="sxs-lookup"><span data-stu-id="59177-112">When type is equal to EXPERIMENTTRIGGERTYPE::FRAMENUMBER, the frame number that will trigger capture.</span></span>

<span data-ttu-id="59177-113">**captureCount**</span><span class="sxs-lookup"><span data-stu-id="59177-113">**captureCount**</span></span>  
<span data-ttu-id="59177-114">Nombre de frames séquentiels à capturer.</span><span class="sxs-lookup"><span data-stu-id="59177-114">The number of sequential frames to capture.</span></span>

<span data-ttu-id="59177-115">**actionIID**</span><span class="sxs-lookup"><span data-stu-id="59177-115">**actionIID**</span></span>  
<span data-ttu-id="59177-116">ID de l’événement d’action (capture d’écran, capture de frame, etc.).</span><span class="sxs-lookup"><span data-stu-id="59177-116">The ID of the action event (screenshot, frame capture, etc).</span></span>

<span data-ttu-id="59177-117">**actionPlayload**</span><span class="sxs-lookup"><span data-stu-id="59177-117">**actionPlayload**</span></span>  
<span data-ttu-id="59177-118">Pointeur vers la charge utile d’événement d’action.</span><span class="sxs-lookup"><span data-stu-id="59177-118">A pointer to the action event payload.</span></span>

## <a name="requirements"></a><span data-ttu-id="59177-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59177-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="59177-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="59177-120">Header</span></span></p></td><td><span data-ttu-id="59177-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="59177-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



