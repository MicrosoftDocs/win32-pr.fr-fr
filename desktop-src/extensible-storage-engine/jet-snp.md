---
description: 'En savoir plus sur : JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516207"
---
# <a name="jet_snp"></a><span data-ttu-id="0868e-103">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="0868e-103">JET_SNP</span></span>


<span data-ttu-id="0868e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="0868e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snp"></a><span data-ttu-id="0868e-105">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="0868e-105">JET_SNP</span></span>

<span data-ttu-id="0868e-106">Le **JET_SNP** groupe de constantes décrit le type de l’opération pour laquelle des informations de progression doivent être obtenues.</span><span class="sxs-lookup"><span data-stu-id="0868e-106">The **JET_SNP** group of constants describe the type of the operation for which progress information is to be obtained.</span></span> <span data-ttu-id="0868e-107">Ces constantes sont utilisées comme paramètre *SNP* de la fonction de rappel [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0868e-107">These constants are used as the *snp* parameter of the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0868e-108">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="0868e-108">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="0868e-109">Description</span><span class="sxs-lookup"><span data-stu-id="0868e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0868e-110">JET_snpRepair</span><span class="sxs-lookup"><span data-stu-id="0868e-110">JET_snpRepair</span></span><br />
<span data-ttu-id="0868e-111">2</span><span class="sxs-lookup"><span data-stu-id="0868e-111">2</span></span></p></td>
<td><p><span data-ttu-id="0868e-112">Le rappel est destiné à une opération de réparation.</span><span class="sxs-lookup"><span data-stu-id="0868e-112">The callback is for a repair operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0868e-113">JET_snpCompact</span><span class="sxs-lookup"><span data-stu-id="0868e-113">JET_snpCompact</span></span><br />
<span data-ttu-id="0868e-114">4</span><span class="sxs-lookup"><span data-stu-id="0868e-114">4</span></span></p></td>
<td><p><span data-ttu-id="0868e-115">Le rappel est destiné à la défragmentation de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0868e-115">The callback is for database defragmentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0868e-116">JET_snpRestore</span><span class="sxs-lookup"><span data-stu-id="0868e-116">JET_snpRestore</span></span><br />
<span data-ttu-id="0868e-117">8</span><span class="sxs-lookup"><span data-stu-id="0868e-117">8</span></span></p></td>
<td><p><span data-ttu-id="0868e-118">Le rappel est destiné à une opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="0868e-118">The callback is for a restore operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0868e-119">JET_snpBackup</span><span class="sxs-lookup"><span data-stu-id="0868e-119">JET_snpBackup</span></span><br />
<span data-ttu-id="0868e-120">9</span><span class="sxs-lookup"><span data-stu-id="0868e-120">9</span></span></p></td>
<td><p><span data-ttu-id="0868e-121">Le rappel est destiné à une opération de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="0868e-121">The callback is for a backup operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0868e-122">JET_snpUpgrade</span><span class="sxs-lookup"><span data-stu-id="0868e-122">JET_snpUpgrade</span></span><br />
<span data-ttu-id="0868e-123">10</span><span class="sxs-lookup"><span data-stu-id="0868e-123">10</span></span></p></td>
<td><p><span data-ttu-id="0868e-124">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0868e-124">Not supported.</span></span></p>
<p><span data-ttu-id="0868e-125"><strong>Windows 2000 :</strong>  Le rappel est destiné à l’opération de mise à niveau du format de base de données.</span><span class="sxs-lookup"><span data-stu-id="0868e-125"><strong>Windows 2000:</strong>  The callback is for the database format upgrade operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0868e-126">JET_snpScrub</span><span class="sxs-lookup"><span data-stu-id="0868e-126">JET_snpScrub</span></span><br />
<span data-ttu-id="0868e-127">11</span><span class="sxs-lookup"><span data-stu-id="0868e-127">11</span></span></p></td>
<td><p><span data-ttu-id="0868e-128">Le rappel est destiné à une opération de mise à zéro de base de données (c’est-à-dire de nettoyage).</span><span class="sxs-lookup"><span data-stu-id="0868e-128">The callback is for a database zeroing (that is, scrubbing) operation.</span></span></p>
<p><span data-ttu-id="0868e-129"><strong>Serveur Windows server 2003 et windows 2000 :</strong>  Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0868e-129"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0868e-130">JET_snpUpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="0868e-130">JET_snpUpgradeRecordFormat</span></span><br />
<span data-ttu-id="0868e-131">12</span><span class="sxs-lookup"><span data-stu-id="0868e-131">12</span></span></p></td>
<td><p><span data-ttu-id="0868e-132">Le rappel est destiné au processus de mise à niveau du format d’enregistrement de toutes les pages de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0868e-132">The callback is for the process of upgrading the record format of all database pages.</span></span></p>
<p><span data-ttu-id="0868e-133"><strong>Serveur Windows server 2003 et windows 2000 :</strong>  Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0868e-133"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="0868e-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0868e-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0868e-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0868e-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0868e-136">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="0868e-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0868e-137"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="0868e-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0868e-138">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0868e-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0868e-139"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="0868e-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0868e-140">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="0868e-140">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0868e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0868e-141">See Also</span></span>

[<span data-ttu-id="0868e-142">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="0868e-142">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="0868e-143">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="0868e-143">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="0868e-144">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="0868e-144">JET_SNT</span></span>](./jet-snt.md)
