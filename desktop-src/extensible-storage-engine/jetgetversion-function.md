---
description: 'En savoir plus sur : fonction JetGetVersion'
title: JetGetVersion fonction)
TOCTitle: JetGetVersion Function
ms:assetid: f25c3639-ae2b-4357-9947-563ef3df72c6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294133(v=EXCHG.10)
ms:contentKeyID: 32765747
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetVersion
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38128358d814ea85cf087c270a65a3fada976e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210381"
---
# <a name="jetgetversion-function"></a><span data-ttu-id="ecf35-103">JetGetVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="ecf35-103">JetGetVersion Function</span></span>


<span data-ttu-id="ecf35-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="ecf35-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetversion-function"></a><span data-ttu-id="ecf35-105">JetGetVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="ecf35-105">JetGetVersion Function</span></span>

<span data-ttu-id="ecf35-106">La fonction **JetGetVersion** récupère la version du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="ecf35-106">The **JetGetVersion** function retrieves the version of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetVersion(
      __in          JET_SESID sesid,
      __out         unsigned long* pwVersion
    );
```

### <a name="parameters"></a><span data-ttu-id="ecf35-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecf35-107">Parameters</span></span>

<span data-ttu-id="ecf35-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ecf35-108">*sesid*</span></span>

<span data-ttu-id="ecf35-109">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="ecf35-109">The session to use for this call.</span></span>

<span data-ttu-id="ecf35-110">*pwVersion*</span><span class="sxs-lookup"><span data-stu-id="ecf35-110">*pwVersion*</span></span>

<span data-ttu-id="ecf35-111">Pointeur vers le numéro de version du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="ecf35-111">A pointer to the version number of the database engine.</span></span>

### <a name="return-value"></a><span data-ttu-id="ecf35-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ecf35-112">Return Value</span></span>

<span data-ttu-id="ecf35-113">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="ecf35-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ecf35-114">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ecf35-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ecf35-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ecf35-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="ecf35-116">Description</span><span class="sxs-lookup"><span data-stu-id="ecf35-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ecf35-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ecf35-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ecf35-118">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ecf35-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ecf35-119">Si cette fonction est exécutée correctement, la version du moteur de base de données est récupérée.</span><span class="sxs-lookup"><span data-stu-id="ecf35-119">If this function succeeds, the version of the database engine is retrieved.</span></span>

<span data-ttu-id="ecf35-120">Il n’existe aucun mode de défaillance connu.</span><span class="sxs-lookup"><span data-stu-id="ecf35-120">There are no known failure modes.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ecf35-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecf35-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ecf35-122"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ecf35-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ecf35-123">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="ecf35-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecf35-124"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="ecf35-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ecf35-125">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ecf35-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecf35-126"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="ecf35-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ecf35-127">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="ecf35-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecf35-128"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="ecf35-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ecf35-129">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ecf35-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecf35-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ecf35-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ecf35-131">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ecf35-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ecf35-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecf35-132">See Also</span></span>

[<span data-ttu-id="ecf35-133">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="ecf35-133">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="ecf35-134">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="ecf35-134">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="ecf35-135">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ecf35-135">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ecf35-136">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ecf35-136">JET_SESID</span></span>](./jet-sesid.md)
