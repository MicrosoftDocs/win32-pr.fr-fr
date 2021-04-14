---
description: 'En savoir plus sur : structure JET_UNICODEINDEX'
title: Structure JET_UNICODEINDEX
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: c4a2332551fb1f624b75e32596b2941d97ffa47d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104394279"
---
# <a name="jet_unicodeindex-structure"></a><span data-ttu-id="384f3-103">Structure JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="384f3-103">JET_UNICODEINDEX Structure</span></span>


<span data-ttu-id="384f3-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="384f3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_unicodeindex-structure"></a><span data-ttu-id="384f3-105">Structure JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="384f3-105">JET_UNICODEINDEX Structure</span></span>

<span data-ttu-id="384f3-106">La structure **JET_UNICODEINDEX** personnalise la manière dont les données Unicode sont normalisées lorsqu’un index est créé sur une colonne Unicode.</span><span class="sxs-lookup"><span data-stu-id="384f3-106">The **JET_UNICODEINDEX** structure customizes how Unicode data gets normalized when an index is created over a Unicode column.</span></span>

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a><span data-ttu-id="384f3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="384f3-107">Members</span></span>

<span data-ttu-id="384f3-108">**lcid**</span><span class="sxs-lookup"><span data-stu-id="384f3-108">**lcid**</span></span>

<span data-ttu-id="384f3-109">ID de paramètres régionaux à utiliser lors de la normalisation des données.</span><span class="sxs-lookup"><span data-stu-id="384f3-109">The Locale ID to use when normalizing the data.</span></span> <span data-ttu-id="384f3-110">Les paramètres régionaux peuvent être utilisés tant que le module linguistique approprié a été installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="384f3-110">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="384f3-111">La seule exception est que les paramètres régionaux de langue neutre (LCID de zéro) ne sont pas conformes.</span><span class="sxs-lookup"><span data-stu-id="384f3-111">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="384f3-112">**dwMapFlags**</span><span class="sxs-lookup"><span data-stu-id="384f3-112">**dwMapFlags**</span></span>

<span data-ttu-id="384f3-113">Ces indicateurs sont passés à [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) lorsque les données Unicode sont normalisées en une clé, ce qui permet aux indicateurs définis par l’utilisateur de remplacer la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="384f3-113">These flags get passed to [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) when Unicode data gets normalized to a key, which enables user-defined flags to override the default.</span></span>

<span data-ttu-id="384f3-114">**Windows 2000**: les deux seules valeurs autorisées pour **dwFlags** sont :</span><span class="sxs-lookup"><span data-stu-id="384f3-114">**Windows 2000**:  The only two legal values for **dwFlags** are:</span></span>

  - <span data-ttu-id="384f3-115">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)</span><span class="sxs-lookup"><span data-stu-id="384f3-115">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE )</span></span>

<!-- end list -->

  - <span data-ttu-id="384f3-116">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)</span><span class="sxs-lookup"><span data-stu-id="384f3-116">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH )</span></span>

<span data-ttu-id="384f3-117">**dwMapFlags** présente les restrictions suivantes.</span><span class="sxs-lookup"><span data-stu-id="384f3-117">**dwMapFlags** has the following restrictions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="384f3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="384f3-118">Value</span></span></p></th>
<th><p><span data-ttu-id="384f3-119">Signification</span><span class="sxs-lookup"><span data-stu-id="384f3-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="384f3-120">LCMAP_SORTKEY</span><span class="sxs-lookup"><span data-stu-id="384f3-120">LCMAP_SORTKEY</span></span></p></td>
<td><p><span data-ttu-id="384f3-121">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="384f3-121">Mandatory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="384f3-122">LCMAP_BYTEREV</span><span class="sxs-lookup"><span data-stu-id="384f3-122">LCMAP_BYTEREV</span></span></p></td>
<td><p><span data-ttu-id="384f3-123">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="384f3-123">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="384f3-124">NORM_IGNORECASE</span><span class="sxs-lookup"><span data-stu-id="384f3-124">NORM_IGNORECASE</span></span></p></td>
<td><p><span data-ttu-id="384f3-125">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="384f3-125">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="384f3-126">NORM_IGNORENONSPACE</span><span class="sxs-lookup"><span data-stu-id="384f3-126">NORM_IGNORENONSPACE</span></span></p></td>
<td><p><span data-ttu-id="384f3-127">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="384f3-127">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="384f3-128">NORM_IGNORESYMBOLS</span><span class="sxs-lookup"><span data-stu-id="384f3-128">NORM_IGNORESYMBOLS</span></span></p></td>
<td><p><span data-ttu-id="384f3-129">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="384f3-129">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="384f3-130">NORM_IGNOREKANATYPE</span><span class="sxs-lookup"><span data-stu-id="384f3-130">NORM_IGNOREKANATYPE</span></span></p></td>
<td><p><span data-ttu-id="384f3-131">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="384f3-131">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="384f3-132">NORM_IGNOREWIDTH</span><span class="sxs-lookup"><span data-stu-id="384f3-132">NORM_IGNOREWIDTH</span></span></p></td>
<td><p><span data-ttu-id="384f3-133">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="384f3-133">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="384f3-134">SORT_STRINGSORT</span><span class="sxs-lookup"><span data-stu-id="384f3-134">SORT_STRINGSORT</span></span></p></td>
<td><p><span data-ttu-id="384f3-135">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="384f3-135">Optional.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="384f3-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="384f3-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="384f3-137"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="384f3-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="384f3-138">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="384f3-138">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="384f3-139"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="384f3-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="384f3-140">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="384f3-140">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="384f3-141"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="384f3-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="384f3-142">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="384f3-142">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="384f3-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="384f3-143">See Also</span></span>

[<span data-ttu-id="384f3-144">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="384f3-144">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="384f3-145">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="384f3-145">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="384f3-146">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="384f3-146">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)
