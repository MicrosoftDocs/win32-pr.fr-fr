---
description: La \_ structure d’événement Update met à jour les événements. Cette structure est repassée à l’application appelante via la procédure de rappel de l’état de l’événement par le NPP.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: Structure de UPDATE_EVENT (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517022"
---
# <a name="update_event-structure"></a><span data-ttu-id="e2faf-104">METTRE à jour la \_ structure d’événement</span><span class="sxs-lookup"><span data-stu-id="e2faf-104">UPDATE\_EVENT structure</span></span>

<span data-ttu-id="e2faf-105">La structure d' **\_ événement Update** met à jour les événements.</span><span class="sxs-lookup"><span data-stu-id="e2faf-105">The **UPDATE\_EVENT** structure updates events.</span></span> <span data-ttu-id="e2faf-106">Cette structure est repassée à l’application appelante via la procédure de rappel de l’état de l’événement par le NPP.</span><span class="sxs-lookup"><span data-stu-id="e2faf-106">This structure is passed back to the calling application via the event status callback procedure by the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2faf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2faf-107">Syntax</span></span>


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a><span data-ttu-id="e2faf-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e2faf-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2faf-109">**Event**</span><span class="sxs-lookup"><span data-stu-id="e2faf-109">**Event**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-110">Événement réel en cours d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e2faf-110">Actual event being recorded.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-111">**Action**</span><span class="sxs-lookup"><span data-stu-id="e2faf-111">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-112">Action entreprise.</span><span class="sxs-lookup"><span data-stu-id="e2faf-112">The action taken.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-113">**État**</span><span class="sxs-lookup"><span data-stu-id="e2faf-113">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-114">Indication de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="e2faf-114">Network status indication.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-115">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e2faf-115">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-116">Variable de compteur auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="e2faf-116">Auxiliary counter variable.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-117">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="e2faf-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-118">Événements marqués, en microsecondes.</span><span class="sxs-lookup"><span data-stu-id="e2faf-118">The marked events, in microseconds.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-119">**lpUserContext**</span><span class="sxs-lookup"><span data-stu-id="e2faf-119">**lpUserContext**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-120">Contexte utilisateur donné par l’application.</span><span class="sxs-lookup"><span data-stu-id="e2faf-120">User context given by the application.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-121">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="e2faf-121">**lpReserved**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-122">Utilisation d’un pilote ou d’un NAL.</span><span class="sxs-lookup"><span data-stu-id="e2faf-122">Driver or NAL use.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-123">**FramesDropped**</span><span class="sxs-lookup"><span data-stu-id="e2faf-123">**FramesDropped**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-124">Frames RTF supprimés dans la mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e2faf-124">RTF frames dropped in the specified buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="e2faf-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-126">Aucune donnée n’est renvoyée avec cette option de commutateur.</span><span class="sxs-lookup"><span data-stu-id="e2faf-126">No data comes back with this switch option.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-127">**lpFrameTable**</span><span class="sxs-lookup"><span data-stu-id="e2faf-127">**lpFrameTable**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-128">RTF uniquement.</span><span class="sxs-lookup"><span data-stu-id="e2faf-128">RTF only.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-129">**lpPacketQueue**</span><span class="sxs-lookup"><span data-stu-id="e2faf-129">**lpPacketQueue**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-130">Pour les transmissions.</span><span class="sxs-lookup"><span data-stu-id="e2faf-130">For transmits.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-131">**SecurityResponse**</span><span class="sxs-lookup"><span data-stu-id="e2faf-131">**SecurityResponse**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-132">Réponse du moniteur de sécurité à distance.</span><span class="sxs-lookup"><span data-stu-id="e2faf-132">Remote security monitor response.</span></span>

</dd> <dt>

<span data-ttu-id="e2faf-133">**lpFinalStats**</span><span class="sxs-lookup"><span data-stu-id="e2faf-133">**lpFinalStats**</span></span>
</dt> <dd>

<span data-ttu-id="e2faf-134">Cela n’est fourni que pour les arrêts non liés à la sécurité (par exemple, les déclencheurs).</span><span class="sxs-lookup"><span data-stu-id="e2faf-134">This is only filled in on non-security related stops (for example, triggers).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2faf-135">Notes</span><span class="sxs-lookup"><span data-stu-id="e2faf-135">Remarks</span></span>

<span data-ttu-id="e2faf-136">Les utilisateurs C++ doivent noter que la déclaration pour ce rappel doit se trouver dans la partie publique du fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e2faf-136">C++ users should note that the declaration for this callback should be in the public part of the header file:</span></span>

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

<span data-ttu-id="e2faf-137">L’implémentation doit être dans la section protégée du fichier. cpp :</span><span class="sxs-lookup"><span data-stu-id="e2faf-137">The implementation should be in the protected section of the .cpp file:</span></span>

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a><span data-ttu-id="e2faf-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2faf-138">Requirements</span></span>



| <span data-ttu-id="e2faf-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2faf-139">Requirement</span></span> | <span data-ttu-id="e2faf-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2faf-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e2faf-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2faf-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e2faf-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2faf-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e2faf-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2faf-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e2faf-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2faf-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e2faf-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2faf-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2faf-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2faf-146"><dt>Netmon.h</dt></span></span> </dl> |



 

 




