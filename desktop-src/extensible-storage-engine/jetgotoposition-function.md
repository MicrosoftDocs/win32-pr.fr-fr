---
description: 'En savoir plus sur : fonction JetGotoPosition'
title: JetGotoPosition fonction)
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749717"
---
# <a name="jetgotoposition-function"></a><span data-ttu-id="7c182-103">JetGotoPosition fonction)</span><span class="sxs-lookup"><span data-stu-id="7c182-103">JetGotoPosition Function</span></span>


<span data-ttu-id="7c182-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="7c182-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotoposition-function"></a><span data-ttu-id="7c182-105">JetGotoPosition fonction)</span><span class="sxs-lookup"><span data-stu-id="7c182-105">JetGotoPosition Function</span></span>

<span data-ttu-id="7c182-106">La fonction **JetGotoPosition** déplace un curseur vers un nouvel emplacement qui est une fraction de la façon dont l’index actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="7c182-106">The **JetGotoPosition** function moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="7c182-107">La fraction est approximativement égale à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7c182-107">The fraction is approximately equal to the following:</span></span>

<span data-ttu-id="7c182-108">precpos- \> centriesLT/precpos- \> centriesTotal</span><span class="sxs-lookup"><span data-stu-id="7c182-108">precpos-\>centriesLT/precpos-\>centriesTotal</span></span>

<span data-ttu-id="7c182-109">Cette opération est exécutée en réponse à l’entrée de la boîte de défilement utilisateur qui est reçue quand l’utilisateur tente d’afficher des données qui démarrent de façon partielle via un jeu de données.</span><span class="sxs-lookup"><span data-stu-id="7c182-109">This operation is performed in response to user scroll box input that is received when the user attempts to show data that starts part way through a data set.</span></span>

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a><span data-ttu-id="7c182-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c182-110">Parameters</span></span>

<span data-ttu-id="7c182-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="7c182-111">*sesid*</span></span>

<span data-ttu-id="7c182-112">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="7c182-112">The session to use for this call.</span></span>

<span data-ttu-id="7c182-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="7c182-113">*tableid*</span></span>

<span data-ttu-id="7c182-114">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="7c182-114">The cursor to use for this call.</span></span>

<span data-ttu-id="7c182-115">*precpos*</span><span class="sxs-lookup"><span data-stu-id="7c182-115">*precpos*</span></span>

<span data-ttu-id="7c182-116">Description de la fraction à utiliser pour positionner le curseur dans l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="7c182-116">The description of the fraction to use in positioning the cursor in the current index.</span></span>

### <a name="return-value"></a><span data-ttu-id="7c182-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7c182-117">Return Value</span></span>

<span data-ttu-id="7c182-118">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="7c182-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7c182-119">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7c182-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c182-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7c182-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="7c182-121">Description</span><span class="sxs-lookup"><span data-stu-id="7c182-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c182-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7c182-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7c182-123">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="7c182-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c182-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7c182-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7c182-125">L’opération n’a pas pu se terminer, car toute activité sur l’instance associée à la session a cessé à la suite d’un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="7c182-125">The operation could not complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c182-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7c182-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7c182-127">L’opération n’a pas pu se terminer car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="7c182-127">The operation could not complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="7c182-128"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c182-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c182-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7c182-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7c182-130">Le precpos- &gt; cbStruct donné n’est pas une taille valide pour la structure <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> , ou precpos- &gt; centriesLT est supérieur à precpos- &gt; centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="7c182-130">The given precpos-&gt;cbStruct is not a valid size for the <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> structure, or precpos-&gt;centriesLT is greater than precpos-&gt;centriesTotal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c182-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7c182-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7c182-132">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="7c182-132">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c182-133">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="7c182-133">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="7c182-134">Cette erreur est retournée si l’index est vide.</span><span class="sxs-lookup"><span data-stu-id="7c182-134">This error will be returned if the index is empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c182-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7c182-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7c182-136">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="7c182-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c182-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="7c182-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="7c182-138">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="7c182-138">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="7c182-139"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c182-139"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c182-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7c182-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7c182-141">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="7c182-141">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7c182-142">Si cette fonction est réussie, le curseur est déplacé vers un enregistrement actif qui est une fraction de la façon dont la fraction est precpos- \> centriesLT divisée par precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="7c182-142">If this function succeeds, the cursor is moved to a current record that is a fraction of the way through the index where the fraction is precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="7c182-143">Si cette fonction échoue, l’emplacement du curseur reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="7c182-143">If this function fails, the cursor location is left unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7c182-144">Notes</span><span class="sxs-lookup"><span data-stu-id="7c182-144">Remarks</span></span>

<span data-ttu-id="7c182-145">Cette opération déplace le curseur de la table vers une position au point approximatif suivant : precpos- \> centriesLT divisé par precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="7c182-145">This operation moves the cursor through the table to a position at the following approximate point: precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="7c182-146">Lorsque des mises à jour se produisent en continu sur la table, les appels suivants avec le même [JET_RECPOS](./jet-recpos-structure.md) peuvent déplacer le curseur vers des positions différentes dans l’index, avant et après la position précédente.</span><span class="sxs-lookup"><span data-stu-id="7c182-146">When updates are occurring continuously on the table, subsequent calls with the same [JET_RECPOS](./jet-recpos-structure.md) can move the cursor to different positions in the index, both before and after the previous position.</span></span> <span data-ttu-id="7c182-147">L’isolation transactionnelle ne s’applique pas au positionnement dans [JET_RECPOS](./jet-recpos-structure.md) , car elle dépend des propriétés physiques de l’index qui ne sont pas des transactions isolées.</span><span class="sxs-lookup"><span data-stu-id="7c182-147">Transactional isolation does not apply to positioning through [JET_RECPOS](./jet-recpos-structure.md) since it depends on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="7c182-148">[JET_RECPOS](./jet-recpos-structure.md) ne doit pas être utilisé pour décrire un enregistrement dans une table ou pour repositionner un enregistrement à proximité d’un enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="7c182-148">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="7c182-149">Au lieu de cela, les signets d’un enregistrement existant doivent être récupérés après un **JetGotoPosition** initial, puis utilisés pour repositionner le même enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7c182-149">Instead, bookmarks for an existing record should be retrieved after an initial **JetGotoPosition** and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7c182-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c182-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c182-151"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7c182-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7c182-152">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="7c182-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c182-153"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="7c182-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7c182-154">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7c182-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c182-155"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="7c182-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7c182-156">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="7c182-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c182-157"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="7c182-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7c182-158">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7c182-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c182-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7c182-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7c182-160">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7c182-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7c182-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c182-161">See Also</span></span>

[<span data-ttu-id="7c182-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="7c182-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="7c182-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7c182-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7c182-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7c182-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7c182-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7c182-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7c182-166">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="7c182-166">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="7c182-167">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="7c182-167">JET_SETINFO</span></span>](./jet-setinfo-structure.md)
