---
description: 'En savoir plus sur : JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106522400"
---
# <a name="jet_err"></a><span data-ttu-id="e594c-103">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e594c-103">JET_ERR</span></span>


<span data-ttu-id="e594c-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="e594c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_err"></a><span data-ttu-id="e594c-105">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e594c-105">JET_ERR</span></span>

<span data-ttu-id="e594c-106">Le type de données **JET_ERR** contient un [code d’erreur ESE (Extensible Storage Engine](./extensible-storage-engine-error-codes.md)).</span><span class="sxs-lookup"><span data-stu-id="e594c-106">The **JET_ERR** data type contains an [Extensible Storage Engine error code](./extensible-storage-engine-error-codes.md).</span></span>

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a><span data-ttu-id="e594c-107">Types de données</span><span class="sxs-lookup"><span data-stu-id="e594c-107">Data Types</span></span>

<span data-ttu-id="e594c-108">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e594c-108">JET_ERR</span></span>

<span data-ttu-id="e594c-109">Une valeur zéro (correspondant à JET_errSuccess) indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e594c-109">A zero value (corresponding to JET_errSuccess) indicates that the call succeeded.</span></span> <span data-ttu-id="e594c-110">Une valeur positive indique qu’une condition non irrécupérable s’est produite lors d’un appel de réussite.</span><span class="sxs-lookup"><span data-stu-id="e594c-110">A positive value warns of a non-fatal condition that occurred during an otherwise successful call.</span></span> <span data-ttu-id="e594c-111">Une valeur négative indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="e594c-111">A negative value indicates that the call failed.</span></span>

### <a name="remarks"></a><span data-ttu-id="e594c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e594c-112">Remarks</span></span>

<span data-ttu-id="e594c-113">Pour plus d’informations sur le renvoi d’erreurs en tant que HRESULT, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="e594c-113">For information about returning errors as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="e594c-114">Pour plus d’informations sur les indicateurs permettant de configurer la base de données afin de gérer les erreurs, consultez [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e594c-114">For information about flags for configuring the database to handle errors, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="e594c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e594c-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e594c-116"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e594c-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e594c-117">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="e594c-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e594c-118"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="e594c-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e594c-119">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e594c-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e594c-120"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="e594c-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e594c-121">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="e594c-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e594c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e594c-122">See Also</span></span>

[<span data-ttu-id="e594c-123">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="e594c-123">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="e594c-124">Codes d’erreur du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="e594c-124">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="e594c-125">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="e594c-125">Error Handling Parameters</span></span>](./error-handling-parameters.md)
