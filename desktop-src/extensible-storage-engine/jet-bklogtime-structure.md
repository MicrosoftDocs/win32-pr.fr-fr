---
description: 'En savoir plus sur : structure JET_BKLOGTIME'
title: Structure JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519480"
---
# <a name="jet_bklogtime-structure"></a><span data-ttu-id="67414-103">Structure JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="67414-103">JET_BKLOGTIME Structure</span></span>


<span data-ttu-id="67414-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="67414-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bklogtime-structure"></a><span data-ttu-id="67414-105">Structure JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="67414-105">JET_BKLOGTIME Structure</span></span>

<span data-ttu-id="67414-106">La structure **JET_BKLOGTIME** contient les éléments de date et d’heure d’un événement.</span><span class="sxs-lookup"><span data-stu-id="67414-106">The **JET_BKLOGTIME** structure holds the date and time elements of an event.</span></span> <span data-ttu-id="67414-107">Il s’agit d’une extension de [JET_LOGTIME](./jet-logtime-structure.md).</span><span class="sxs-lookup"><span data-stu-id="67414-107">It is an extension of [JET_LOGTIME](./jet-logtime-structure.md).</span></span>

<span data-ttu-id="67414-108">**Windows Vista : JET_BKLOGTIME** est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67414-108">**Windows Vista:  JET_BKLOGTIME** is introduced in Windows Vista.</span></span>

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a><span data-ttu-id="67414-109">Membres</span><span class="sxs-lookup"><span data-stu-id="67414-109">Members</span></span>

<span data-ttu-id="67414-110">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="67414-110">**bSeconds**</span></span>

<span data-ttu-id="67414-111">Heure de l’événement, en secondes.</span><span class="sxs-lookup"><span data-stu-id="67414-111">The time of the event in seconds.</span></span> <span data-ttu-id="67414-112">La valeur peut être comprise entre 0 (zéro) et 60.</span><span class="sxs-lookup"><span data-stu-id="67414-112">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="67414-113">0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».</span><span class="sxs-lookup"><span data-stu-id="67414-113">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="67414-114">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="67414-114">**bMinutes**</span></span>

<span data-ttu-id="67414-115">Heure de l’événement, en minutes.</span><span class="sxs-lookup"><span data-stu-id="67414-115">The time of the event in minutes.</span></span> <span data-ttu-id="67414-116">La valeur peut être comprise entre 0 (zéro) et 60.</span><span class="sxs-lookup"><span data-stu-id="67414-116">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="67414-117">0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».</span><span class="sxs-lookup"><span data-stu-id="67414-117">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="67414-118">**bHours**</span><span class="sxs-lookup"><span data-stu-id="67414-118">**bHours**</span></span>

<span data-ttu-id="67414-119">Heure de l’événement, en heures.</span><span class="sxs-lookup"><span data-stu-id="67414-119">The time of the event in hours.</span></span> <span data-ttu-id="67414-120">La valeur peut être comprise entre 0 (zéro) et 24.</span><span class="sxs-lookup"><span data-stu-id="67414-120">This can be 0 (zero) to 24.</span></span> <span data-ttu-id="67414-121">0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».</span><span class="sxs-lookup"><span data-stu-id="67414-121">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="67414-122">**bDay**</span><span class="sxs-lookup"><span data-stu-id="67414-122">**bDay**</span></span>

<span data-ttu-id="67414-123">Jour du mois de l’événement.</span><span class="sxs-lookup"><span data-stu-id="67414-123">The day of the month of the event.</span></span> <span data-ttu-id="67414-124">La valeur peut être comprise entre 0 (zéro) et 31.</span><span class="sxs-lookup"><span data-stu-id="67414-124">This can be 0 (zero) to 31.</span></span> <span data-ttu-id="67414-125">0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».</span><span class="sxs-lookup"><span data-stu-id="67414-125">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="67414-126">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="67414-126">**bMonth**</span></span>

<span data-ttu-id="67414-127">Mois de l’année de l’événement.</span><span class="sxs-lookup"><span data-stu-id="67414-127">The month of the year of the event.</span></span> <span data-ttu-id="67414-128">La valeur peut être comprise entre 0 (zéro) et 12.</span><span class="sxs-lookup"><span data-stu-id="67414-128">This can be 0 (zero) to 12.</span></span> <span data-ttu-id="67414-129">0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».</span><span class="sxs-lookup"><span data-stu-id="67414-129">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="67414-130">**bYear**</span><span class="sxs-lookup"><span data-stu-id="67414-130">**bYear**</span></span>

<span data-ttu-id="67414-131">Année (décalage par 1900) de l’événement.</span><span class="sxs-lookup"><span data-stu-id="67414-131">The year (offset by 1900) of the event.</span></span> <span data-ttu-id="67414-132">Pour obtenir l’année réelle, ajoutez 1900 à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="67414-132">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="67414-133">0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».</span><span class="sxs-lookup"><span data-stu-id="67414-133">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="67414-134">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="67414-134">**bFiller1**</span></span>

<span data-ttu-id="67414-135">Ce champ doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="67414-135">This field should be ignored.</span></span>

<span data-ttu-id="67414-136">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="67414-136">**fTimeIsUTC**</span></span>

<span data-ttu-id="67414-137">L’heure est au format UTC.</span><span class="sxs-lookup"><span data-stu-id="67414-137">The time is in UTC format.</span></span>

<span data-ttu-id="67414-138">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="67414-138">**fUnused**</span></span>

<span data-ttu-id="67414-139">Ce champ doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="67414-139">This field should be ignored.</span></span>

<span data-ttu-id="67414-140">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="67414-140">**bFiller2**</span></span>

<span data-ttu-id="67414-141">Ce champ doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="67414-141">This field should be ignored.</span></span>

<span data-ttu-id="67414-142">**fOSSnapshot**</span><span class="sxs-lookup"><span data-stu-id="67414-142">**fOSSnapshot**</span></span>

<span data-ttu-id="67414-143">Si cet événement est une sauvegarde, cet indicateur contient l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="67414-143">If this event is a backup, this flag contains one of the following possible values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67414-144">Nom</span><span class="sxs-lookup"><span data-stu-id="67414-144">Name</span></span></p></th>
<th><p><span data-ttu-id="67414-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="67414-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67414-146">sauvegarde en continu</span><span class="sxs-lookup"><span data-stu-id="67414-146">streaming backup</span></span></p></td>
<td><p><span data-ttu-id="67414-147">0 (zéro)</span><span class="sxs-lookup"><span data-stu-id="67414-147">0 (zero)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67414-148">sauvegarde d’instantané</span><span class="sxs-lookup"><span data-stu-id="67414-148">snapshot backup</span></span></p></td>
<td><p><span data-ttu-id="67414-149">1</span><span class="sxs-lookup"><span data-stu-id="67414-149">1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="67414-150">**fReserved**</span><span class="sxs-lookup"><span data-stu-id="67414-150">**fReserved**</span></span>

<span data-ttu-id="67414-151">Ce champ doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="67414-151">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="67414-152">Notes</span><span class="sxs-lookup"><span data-stu-id="67414-152">Remarks</span></span>

<span data-ttu-id="67414-153">Cette structure est utilisée lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="67414-153">This structure is used when debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="67414-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67414-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67414-155"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="67414-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="67414-156">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67414-156">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67414-157"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="67414-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="67414-158">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="67414-158">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67414-159"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="67414-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="67414-160">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="67414-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="67414-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67414-161">See Also</span></span>

[<span data-ttu-id="67414-162">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="67414-162">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="67414-163">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="67414-163">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
