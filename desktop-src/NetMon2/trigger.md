---
description: La structure du DÉCLENCHEur indique une action que le pilote doit prendre à un moment donné.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Structure de DÉCLENCHEur (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528270"
---
# <a name="trigger-structure"></a><span data-ttu-id="3ae38-103">Structure de DÉCLENCHEur</span><span class="sxs-lookup"><span data-stu-id="3ae38-103">TRIGGER structure</span></span>

<span data-ttu-id="3ae38-104">La structure du **déclencheur** indique une action que le pilote doit prendre à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="3ae38-104">The **TRIGGER** structure indicates an action to be taken by the driver at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae38-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ae38-105">Syntax</span></span>


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a><span data-ttu-id="3ae38-106">Membres</span><span class="sxs-lookup"><span data-stu-id="3ae38-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ae38-107">**TriggerActive**</span><span class="sxs-lookup"><span data-stu-id="3ae38-107">**TriggerActive**</span></span>
</dt> <dd>

<span data-ttu-id="3ae38-108">Valeur booléenne qui détermine si le pilote doit faire l’objet d’une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="3ae38-108">A Boolean value that determines if the trigger should be paid attention to by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="3ae38-109">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="3ae38-109">**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="3ae38-110">Code d’opération du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="3ae38-110">The op code of the trigger.</span></span>

</dd> <dt>

<span data-ttu-id="3ae38-111">**TriggerAction**</span><span class="sxs-lookup"><span data-stu-id="3ae38-111">**TriggerAction**</span></span>
</dt> <dd>

<span data-ttu-id="3ae38-112">Action que le déclencheur doit exécuter s’il est déclenché.</span><span class="sxs-lookup"><span data-stu-id="3ae38-112">Action that the trigger is to take if it is fired.</span></span>

</dd> <dt>

<span data-ttu-id="3ae38-113">**TriggerFlags**</span><span class="sxs-lookup"><span data-stu-id="3ae38-113">**TriggerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="3ae38-114">Indicateurs de déclencheur.</span><span class="sxs-lookup"><span data-stu-id="3ae38-114">Trigger flags.</span></span>

</dd> <dt>

<span data-ttu-id="3ae38-115">**TriggerPatternMatch**</span><span class="sxs-lookup"><span data-stu-id="3ae38-115">**TriggerPatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="3ae38-116">Le modèle de déclencheur correspond.</span><span class="sxs-lookup"><span data-stu-id="3ae38-116">The trigger pattern match.</span></span>

</dd> <dt>

<span data-ttu-id="3ae38-117">**TriggerBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3ae38-117">**TriggerBufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="3ae38-118">Taille de la mémoire tampon du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="3ae38-118">Trigger buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="3ae38-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="3ae38-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="3ae38-120">Réservé.</span><span class="sxs-lookup"><span data-stu-id="3ae38-120">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ae38-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ae38-121">Requirements</span></span>



| <span data-ttu-id="3ae38-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ae38-122">Requirement</span></span> | <span data-ttu-id="3ae38-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ae38-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae38-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ae38-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae38-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ae38-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3ae38-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ae38-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae38-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ae38-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3ae38-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ae38-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ae38-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ae38-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




