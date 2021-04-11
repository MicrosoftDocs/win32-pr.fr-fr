---
description: 'En savoir plus sur : JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201227"
---
# <a name="jet_snt"></a><span data-ttu-id="ad45d-103">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="ad45d-103">JET_SNT</span></span>


<span data-ttu-id="ad45d-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="ad45d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snt"></a><span data-ttu-id="ad45d-105">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="ad45d-105">JET_SNT</span></span>

<span data-ttu-id="ad45d-106">Le [JET_SNT]() groupe de constantes décrit les points de la progression d’une opération sur laquelle les informations sont demandées dans un appel à la fonction de rappel [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ad45d-106">The [JET_SNT]() group of constants describe the points of the progress of an operation about which information is requested in a call to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad45d-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="ad45d-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="ad45d-108">Description</span><span class="sxs-lookup"><span data-stu-id="ad45d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad45d-109">JET_sntBegin</span><span class="sxs-lookup"><span data-stu-id="ad45d-109">JET_sntBegin</span></span><br />
<span data-ttu-id="ad45d-110">5</span><span class="sxs-lookup"><span data-stu-id="ad45d-110">5</span></span></p></td>
<td><p><span data-ttu-id="ad45d-111">Début d’une opération</span><span class="sxs-lookup"><span data-stu-id="ad45d-111">The beginning of an operation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad45d-112">JET_sntRequirements</span><span class="sxs-lookup"><span data-stu-id="ad45d-112">JET_sntRequirements</span></span><br />
<span data-ttu-id="ad45d-113">7</span><span class="sxs-lookup"><span data-stu-id="ad45d-113">7</span></span></p></td>
<td><p><span data-ttu-id="ad45d-114">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ad45d-114">Not supported.</span></span></p>
<p><span data-ttu-id="ad45d-115"><strong>Serveur Windows 2000 :</strong>  L’opération est démarrée.</span><span class="sxs-lookup"><span data-stu-id="ad45d-115"><strong>Windows 2000 Server:</strong>  The operation is started.</span></span> <span data-ttu-id="ad45d-116">Dans ce cas, le dernier paramètre de la fonction de rappel doit être un pointeur valide vers une structure de <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> qui indique le nombre total d’unités à exécuter.</span><span class="sxs-lookup"><span data-stu-id="ad45d-116">In this case, the last parameter of the callback function should be a valid pointer to a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure indicating the total number of units to be executed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad45d-117">JET_sntProgress</span><span class="sxs-lookup"><span data-stu-id="ad45d-117">JET_sntProgress</span></span><br />
<span data-ttu-id="ad45d-118">0</span><span class="sxs-lookup"><span data-stu-id="ad45d-118">0</span></span></p></td>
<td><p><span data-ttu-id="ad45d-119">Nombre d’unités terminées et nombre d’unités encore à effectuer.</span><span class="sxs-lookup"><span data-stu-id="ad45d-119">The number of units completed and number of units yet to be done.</span></span> <span data-ttu-id="ad45d-120">Ces informations sont retournées dans les membres d’une structure <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> .</span><span class="sxs-lookup"><span data-stu-id="ad45d-120">This information is returned in the members of a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad45d-121">JET_sntComplete</span><span class="sxs-lookup"><span data-stu-id="ad45d-121">JET_sntComplete</span></span><br />
<span data-ttu-id="ad45d-122">6</span><span class="sxs-lookup"><span data-stu-id="ad45d-122">6</span></span></p></td>
<td><p><span data-ttu-id="ad45d-123">Achèvement d’une opération.</span><span class="sxs-lookup"><span data-stu-id="ad45d-123">The completion of an operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad45d-124">JET_sntFail</span><span class="sxs-lookup"><span data-stu-id="ad45d-124">JET_sntFail</span></span><br />
<span data-ttu-id="ad45d-125">3</span><span class="sxs-lookup"><span data-stu-id="ad45d-125">3</span></span></p></td>
<td><p><span data-ttu-id="ad45d-126">L’échec d’une opération.</span><span class="sxs-lookup"><span data-stu-id="ad45d-126">The failure of an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad45d-127">JET_sntRecoveryStep</span><span class="sxs-lookup"><span data-stu-id="ad45d-127">JET_sntRecoveryStep</span></span><br />
<span data-ttu-id="ad45d-128">8</span><span class="sxs-lookup"><span data-stu-id="ad45d-128">8</span></span></p></td>
<td><p><span data-ttu-id="ad45d-129">Contrôle de récupération d’une opération.</span><span class="sxs-lookup"><span data-stu-id="ad45d-129">The recovery control of an operation.</span></span></p>
<div class="alert">

> [!NOTE]
> <P><span data-ttu-id="ad45d-130">Cette valeur ne s’applique pas aux versions du système d’exploitation Windows à compter de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ad45d-130">This value is not applicable to versions of the Windows operating system starting with Windows 8.</span></span></P>


</div></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="ad45d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad45d-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad45d-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ad45d-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ad45d-133">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="ad45d-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad45d-134"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="ad45d-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ad45d-135">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ad45d-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad45d-136"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="ad45d-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ad45d-137">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="ad45d-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ad45d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad45d-138">See Also</span></span>

[<span data-ttu-id="ad45d-139">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="ad45d-139">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="ad45d-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="ad45d-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="ad45d-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="ad45d-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)
