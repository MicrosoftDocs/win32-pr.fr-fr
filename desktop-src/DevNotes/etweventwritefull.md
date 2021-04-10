---
description: Écrit un événement complet dans une session.
title: EtwEventWriteFull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950739"
---
# <a name="etweventwritefull-function"></a><span data-ttu-id="b6ce5-103">EtwEventWriteFull fonction)</span><span class="sxs-lookup"><span data-stu-id="b6ce5-103">EtwEventWriteFull function</span></span>

<span data-ttu-id="b6ce5-104">[La fonction EtwEventWriteFull et les structures qu’elle retourne sont internes au système d’exploitation et sujettes à changement d’une version de Windows à une autre.]</span><span class="sxs-lookup"><span data-stu-id="b6ce5-104">[The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="b6ce5-105">Écrit un événement complet dans une session.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-105">Writes a full event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ce5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6ce5-106">Syntax</span></span>

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="b6ce5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6ce5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ce5-108">*RegHandle*</span><span class="sxs-lookup"><span data-stu-id="b6ce5-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="b6ce5-109">RegHandle pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="b6ce5-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="b6ce5-110">*EventDescriptor*</span></span> 
</dt> <dd>

<span data-ttu-id="b6ce5-111">Descripteur d’événement de l’événement à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-111">Event Descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="b6ce5-112">*EventProperty*</span><span class="sxs-lookup"><span data-stu-id="b6ce5-112">*EventProperty*</span></span>
</dt> <dd>

<span data-ttu-id="b6ce5-113">Indicateur donné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-113">Flag given by the user.</span></span>

</dd> <dt>

<span data-ttu-id="b6ce5-114">*ActivityId*</span><span class="sxs-lookup"><span data-stu-id="b6ce5-114">*ActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="b6ce5-115">ID d’activité.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-115">Activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="b6ce5-116">*RelatedActivityId*</span><span class="sxs-lookup"><span data-stu-id="b6ce5-116">*RelatedActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="b6ce5-117">ID d’activité associé.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-117">Related activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="b6ce5-118">*UserDataCount*</span><span class="sxs-lookup"><span data-stu-id="b6ce5-118">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="b6ce5-119">Nombre d’éléments de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-119">The number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="b6ce5-120">*UserData*</span><span class="sxs-lookup"><span data-stu-id="b6ce5-120">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="b6ce5-121">Pointeur vers un tableau d’éléments de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-121">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6ce5-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6ce5-122">Return value</span></span>

<span data-ttu-id="b6ce5-123">Code d’erreur Win32.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-123">A Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6ce5-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b6ce5-124">Remarks</span></span>

<span data-ttu-id="b6ce5-125">La fonction EtwEventWriteFull et les structures qu’elle retourne sont internes au système d’exploitation et peuvent être modifiées d’une version de Windows à une autre.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-125">The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="b6ce5-126">Pour maintenir la compatibilité de votre application, il est préférable d’utiliser à la place des fonctions publiques.</span><span class="sxs-lookup"><span data-stu-id="b6ce5-126">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>


## <a name="requirements"></a><span data-ttu-id="b6ce5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6ce5-127">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b6ce5-128">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="b6ce5-128">**Target Platform**</span></span> | <span data-ttu-id="b6ce5-129">Windows</span><span class="sxs-lookup"><span data-stu-id="b6ce5-129">Windows</span></span> |
| <span data-ttu-id="b6ce5-130">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="b6ce5-130">**Header**</span></span> | <span data-ttu-id="b6ce5-131">ntetw. h</span><span class="sxs-lookup"><span data-stu-id="b6ce5-131">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="b6ce5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6ce5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ce5-133">EventWrite</span><span class="sxs-lookup"><span data-stu-id="b6ce5-133">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="b6ce5-134">EventWriteEx</span><span class="sxs-lookup"><span data-stu-id="b6ce5-134">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
