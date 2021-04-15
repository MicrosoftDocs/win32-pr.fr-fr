---
description: 'En savoir plus sur : fonction JetCloseDatabase'
title: JetCloseDatabase fonction)
TOCTitle: JetCloseDatabase Function
ms:assetid: e17a05dd-c30b-4e8f-8538-91a65e8052d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294123(v=EXCHG.10)
ms:contentKeyID: 32765737
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9088e0ebc3b4778d6968c999afc238e49fb2f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524970"
---
# <a name="jetclosedatabase-function"></a><span data-ttu-id="7c157-103">JetCloseDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="7c157-103">JetCloseDatabase Function</span></span>


<span data-ttu-id="7c157-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="7c157-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosedatabase-function"></a><span data-ttu-id="7c157-105">JetCloseDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="7c157-105">JetCloseDatabase Function</span></span>

<span data-ttu-id="7c157-106">La fonction **JetCloseDatabase** ferme un fichier de base de données qui a été ouvert précédemment avec [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="7c157-106">The **JetCloseDatabase** function closes a database file that was previously opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7c157-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c157-107">Parameters</span></span>

<span data-ttu-id="7c157-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="7c157-108">*sesid*</span></span>

<span data-ttu-id="7c157-109">Contexte de session de base de données qui sera utilisé pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="7c157-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="7c157-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="7c157-110">*dbid*</span></span>

<span data-ttu-id="7c157-111">Base de données à fermer.</span><span class="sxs-lookup"><span data-stu-id="7c157-111">The database to be closed.</span></span>

<span data-ttu-id="7c157-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7c157-112">*grbit*</span></span>

<span data-ttu-id="7c157-113">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="7c157-113">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="7c157-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7c157-114">Return Value</span></span>

<span data-ttu-id="7c157-115">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="7c157-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7c157-116">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7c157-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c157-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7c157-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="7c157-118">Description</span><span class="sxs-lookup"><span data-stu-id="7c157-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c157-119">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="7c157-119">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="7c157-120">La base de données n’a pas été ouverte précédemment.</span><span class="sxs-lookup"><span data-stu-id="7c157-120">The database was not previously opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c157-121">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="7c157-121">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="7c157-122">Le paramètre <em>dbid</em> n’était pas un identificateur de base de données valide.</span><span class="sxs-lookup"><span data-stu-id="7c157-122">The <em>dbid</em> parameter was not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c157-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7c157-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7c157-124">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="7c157-124">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="7c157-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c157-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c157-126"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7c157-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7c157-127">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="7c157-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c157-128"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="7c157-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7c157-129">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7c157-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c157-130"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="7c157-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7c157-131">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="7c157-131">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c157-132"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="7c157-132"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7c157-133">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7c157-133">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c157-134"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7c157-134"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7c157-135">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7c157-135">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7c157-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c157-136">See Also</span></span>

[<span data-ttu-id="7c157-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7c157-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7c157-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7c157-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7c157-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7c157-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7c157-140">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7c157-140">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7c157-141">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="7c157-141">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="7c157-142">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="7c157-142">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="7c157-143">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="7c157-143">JetOpenDatabase</span></span>](./jetopendatabase-function.md)
