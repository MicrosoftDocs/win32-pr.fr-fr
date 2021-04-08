---
description: 'En savoir plus sur : structure JET_LOGTIME'
title: Structure JET_LOGTIME
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762427"
---
# <a name="jet_logtime-structure"></a><span data-ttu-id="aa611-103">Structure JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="aa611-103">JET_LOGTIME Structure</span></span>


<span data-ttu-id="aa611-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="aa611-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_logtime-structure"></a><span data-ttu-id="aa611-105">Structure JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="aa611-105">JET_LOGTIME Structure</span></span>

<span data-ttu-id="aa611-106">La structure **JET_LOGTIME** contient les éléments de la date et de l’heure d’un événement.</span><span class="sxs-lookup"><span data-stu-id="aa611-106">The **JET_LOGTIME** structure holds elements of the date and time of an event.</span></span>

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a><span data-ttu-id="aa611-107">Membres</span><span class="sxs-lookup"><span data-stu-id="aa611-107">Members</span></span>

<span data-ttu-id="aa611-108">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="aa611-108">**bSeconds**</span></span>

<span data-ttu-id="aa611-109">Heure de l’événement, en secondes.</span><span class="sxs-lookup"><span data-stu-id="aa611-109">The time of the event in seconds.</span></span> <span data-ttu-id="aa611-110">Cette valeur peut être comprise entre 0 et 59.</span><span class="sxs-lookup"><span data-stu-id="aa611-110">This value can be 0 to 59.</span></span> <span data-ttu-id="aa611-111">la valeur 0 est utilisée lorsque la structure a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="aa611-111">0 is used when the structure is null.</span></span>

<span data-ttu-id="aa611-112">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="aa611-112">**bMinutes**</span></span>

<span data-ttu-id="aa611-113">Heure de l’événement, en minutes.</span><span class="sxs-lookup"><span data-stu-id="aa611-113">The time of the event in minutes.</span></span> <span data-ttu-id="aa611-114">Cette valeur peut être comprise entre 0 et 59.</span><span class="sxs-lookup"><span data-stu-id="aa611-114">This value can be 0 to 59.</span></span> <span data-ttu-id="aa611-115">la valeur 0 est utilisée lorsque la structure a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="aa611-115">0 is used when the structure is null.</span></span>

<span data-ttu-id="aa611-116">**bHours**</span><span class="sxs-lookup"><span data-stu-id="aa611-116">**bHours**</span></span>

<span data-ttu-id="aa611-117">Heure de l’événement, en heures.</span><span class="sxs-lookup"><span data-stu-id="aa611-117">The time of the event in hours.</span></span> <span data-ttu-id="aa611-118">Cette valeur peut être comprise entre 0 et 23.</span><span class="sxs-lookup"><span data-stu-id="aa611-118">This value can be 0 to 23.</span></span> <span data-ttu-id="aa611-119">la valeur 0 est utilisée lorsque la structure a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="aa611-119">0 is used when the structure is null.</span></span>

<span data-ttu-id="aa611-120">**bDay**</span><span class="sxs-lookup"><span data-stu-id="aa611-120">**bDay**</span></span>

<span data-ttu-id="aa611-121">Jour du mois de l’événement.</span><span class="sxs-lookup"><span data-stu-id="aa611-121">The day of the month of the event.</span></span> <span data-ttu-id="aa611-122">Cette valeur peut être comprise entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="aa611-122">This value can be 0 to 31.</span></span> <span data-ttu-id="aa611-123">la valeur 0 est utilisée lorsque la structure a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="aa611-123">0 is used when the structure is null.</span></span>

<span data-ttu-id="aa611-124">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="aa611-124">**bMonth**</span></span>

<span data-ttu-id="aa611-125">Mois de l’année de l’événement.</span><span class="sxs-lookup"><span data-stu-id="aa611-125">The month of the year of the event.</span></span> <span data-ttu-id="aa611-126">Cette valeur peut être comprise entre 0 et 12.</span><span class="sxs-lookup"><span data-stu-id="aa611-126">This value can be 0 to 12.</span></span> <span data-ttu-id="aa611-127">la valeur 0 est utilisée lorsque la structure a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="aa611-127">0 is used when the structure is null.</span></span>

<span data-ttu-id="aa611-128">**bYear**</span><span class="sxs-lookup"><span data-stu-id="aa611-128">**bYear**</span></span>

<span data-ttu-id="aa611-129">Année de l’événement (décalage par 1900).</span><span class="sxs-lookup"><span data-stu-id="aa611-129">The year of the event (offset by 1900).</span></span> <span data-ttu-id="aa611-130">Pour obtenir l’année réelle, ajoutez 1900 à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="aa611-130">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="aa611-131">la valeur 0 est utilisée lorsque la structure a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="aa611-131">0 is used when the structure is null.</span></span>

<span data-ttu-id="aa611-132">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="aa611-132">**bFiller1**</span></span>

<span data-ttu-id="aa611-133">Ce champ doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="aa611-133">This field should be ignored.</span></span>

<span data-ttu-id="aa611-134">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="aa611-134">**fTimeIsUTC**</span></span>

<span data-ttu-id="aa611-135">L’heure est au format UTC.</span><span class="sxs-lookup"><span data-stu-id="aa611-135">The time is in UTC format.</span></span>

<span data-ttu-id="aa611-136">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="aa611-136">**fUnused**</span></span>

<span data-ttu-id="aa611-137">Ce champ doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="aa611-137">This field should be ignored.</span></span>

<span data-ttu-id="aa611-138">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="aa611-138">**bFiller2**</span></span>

<span data-ttu-id="aa611-139">Ce champ doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="aa611-139">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="aa611-140">Notes</span><span class="sxs-lookup"><span data-stu-id="aa611-140">Remarks</span></span>

<span data-ttu-id="aa611-141">Cette structure est principalement destinée à être utilisée dans le débogage.</span><span class="sxs-lookup"><span data-stu-id="aa611-141">This structure is meant primarily for usage in debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="aa611-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa611-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa611-143"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="aa611-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aa611-144">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="aa611-144">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa611-145"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="aa611-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aa611-146">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="aa611-146">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa611-147"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="aa611-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aa611-148">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="aa611-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="aa611-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa611-149">See Also</span></span>

[<span data-ttu-id="aa611-150">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="aa611-150">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
