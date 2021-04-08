---
description: 'En savoir plus sur : constantes de handle non valides'
title: Constantes de handle non valides
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035140"
---
# <a name="invalid-handle-constants"></a><span data-ttu-id="953e3-103">Constantes de handle non valides</span><span class="sxs-lookup"><span data-stu-id="953e3-103">Invalid Handle Constants</span></span>


<span data-ttu-id="953e3-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="953e3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="invalid-handle-constants"></a><span data-ttu-id="953e3-105">Constantes de handle non valides</span><span class="sxs-lookup"><span data-stu-id="953e3-105">Invalid Handle Constants</span></span>

<span data-ttu-id="953e3-106">Les constantes suivantes indiquent des handles non valides pour différents aspects de ESE.</span><span class="sxs-lookup"><span data-stu-id="953e3-106">The following constants indicate invalid handles for different aspects of ESE.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="953e3-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="953e3-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="953e3-108">Description</span><span class="sxs-lookup"><span data-stu-id="953e3-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="953e3-109">JET_instanceNil</span><span class="sxs-lookup"><span data-stu-id="953e3-109">JET_instanceNil</span></span><br />
<span data-ttu-id="953e3-110">(~ (JET_INSTANCE) 0)</span><span class="sxs-lookup"><span data-stu-id="953e3-110">(~(JET_INSTANCE)0)</span></span></p></td>
<td><p><span data-ttu-id="953e3-111">Handle non valide pour une instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="953e3-111">An invalid handle for a database instance.</span></span><br /><span data-ttu-id="953e3-112">
<strong>Windows XP :</strong> Introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="953e3-112">
<strong>Windows XP:</strong> Introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="953e3-113">JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="953e3-113">JET_sesidNil</span></span><br />
<span data-ttu-id="953e3-114">(~ (JET_SESID) 0)</span><span class="sxs-lookup"><span data-stu-id="953e3-114">(~(JET_SESID)0)</span></span></p></td>
<td><p><span data-ttu-id="953e3-115">Handle non valide pour un ID de session.</span><span class="sxs-lookup"><span data-stu-id="953e3-115">An invalid handle for a session ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="953e3-116">JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="953e3-116">JET_tableidNil</span></span><br />
<span data-ttu-id="953e3-117">(~ (JET_TABLEID) 0)</span><span class="sxs-lookup"><span data-stu-id="953e3-117">(~(JET_TABLEID)0)</span></span></p></td>
<td><p><span data-ttu-id="953e3-118">Handle non valide pour un ID de table.</span><span class="sxs-lookup"><span data-stu-id="953e3-118">An invalid handle for a table ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="953e3-119">JET_bitNil</span><span class="sxs-lookup"><span data-stu-id="953e3-119">JET_bitNil</span></span><br />
<span data-ttu-id="953e3-120">((JET_GRBIT) 0)</span><span class="sxs-lookup"><span data-stu-id="953e3-120">((JET_GRBIT)0)</span></span></p></td>
<td><p><span data-ttu-id="953e3-121">Handle non valide pour un groupe de bits.</span><span class="sxs-lookup"><span data-stu-id="953e3-121">An invalid handle for a group of bits.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="953e3-122">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="953e3-122">JET_LSNil</span></span><br />
<span data-ttu-id="953e3-123">(~ (JET_LS) 0)</span><span class="sxs-lookup"><span data-stu-id="953e3-123">(~(JET_LS)0)</span></span></p></td>
<td><p><span data-ttu-id="953e3-124">Handle non valide pour le stockage local.</span><span class="sxs-lookup"><span data-stu-id="953e3-124">An invalid handle for the Local Storage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="953e3-125">JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="953e3-125">JET_dbidNil</span></span><br />
<span data-ttu-id="953e3-126">((JET_DBID) 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="953e3-126">((JET_DBID) 0xFFFFFFFF)</span></span></p></td>
<td><p><span data-ttu-id="953e3-127">Handle non valide pour l’ID de base de données.</span><span class="sxs-lookup"><span data-stu-id="953e3-127">An invalid handle for the database ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="953e3-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="953e3-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="953e3-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="953e3-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="953e3-130">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="953e3-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="953e3-131"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="953e3-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="953e3-132">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="953e3-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="953e3-133"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="953e3-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="953e3-134">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="953e3-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

