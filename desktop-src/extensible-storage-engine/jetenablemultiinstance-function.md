---
description: 'En savoir plus sur : fonction JetEnableMultiInstance'
title: JetEnableMultiInstance fonction)
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535704"
---
# <a name="jetenablemultiinstance-function"></a><span data-ttu-id="f3878-103">JetEnableMultiInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="f3878-103">JetEnableMultiInstance Function</span></span>


<span data-ttu-id="f3878-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f3878-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenablemultiinstance-function"></a><span data-ttu-id="f3878-105">JetEnableMultiInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="f3878-105">JetEnableMultiInstance Function</span></span>

<span data-ttu-id="f3878-106">La fonction **JetEnableMultiInstance** configure le moteur de base de données pour une utilisation avec plusieurs instances dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="f3878-106">The **JetEnableMultiInstance** function configures the database engine for use with multiple instances in the same process.</span></span> <span data-ttu-id="f3878-107">Un tableau facultatif de paramètres système globaux est disponible pour le premier appelant, ce qui permet la modification du mode multi-instance.</span><span class="sxs-lookup"><span data-stu-id="f3878-107">An optional array of global system parameters is available to the first caller allowing for the change to multi-instance mode.</span></span>

<span data-ttu-id="f3878-108">**Windows XP : JetEnableMultiInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f3878-108">**Windows XP:  JetEnableMultiInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a><span data-ttu-id="f3878-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3878-109">Parameters</span></span>

<span data-ttu-id="f3878-110">*psetsysparam*</span><span class="sxs-lookup"><span data-stu-id="f3878-110">*psetsysparam*</span></span>

<span data-ttu-id="f3878-111">Tableau de paramètres système globaux à définir si et seulement si le moteur passe en mode multi-instance à la suite de cet appel.</span><span class="sxs-lookup"><span data-stu-id="f3878-111">An array of global system parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="f3878-112">Si *csetsysparam* est égal à zéro, *psetsysparam* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f3878-112">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="f3878-113">*csetsysparam*</span><span class="sxs-lookup"><span data-stu-id="f3878-113">*csetsysparam*</span></span>

<span data-ttu-id="f3878-114">Nombre d’éléments pour le tableau de paramètres globaux à définir si et seulement si le moteur passe en mode multi-instance à la suite de cet appel.</span><span class="sxs-lookup"><span data-stu-id="f3878-114">The count of elements for the array of global parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="f3878-115">Si *csetsysparam* est égal à zéro, *psetsysparam* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f3878-115">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="f3878-116">*pcsetsucceed*</span><span class="sxs-lookup"><span data-stu-id="f3878-116">*pcsetsucceed*</span></span>

<span data-ttu-id="f3878-117">Pointeur vers le nombre de paramètres système globaux qui ont été correctement configurés à la suite de cet appel.</span><span class="sxs-lookup"><span data-stu-id="f3878-117">A pointer to the count of global system parameters that were successfully configured as a result of this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="f3878-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3878-118">Return Value</span></span>

<span data-ttu-id="f3878-119">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="f3878-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f3878-120">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f3878-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3878-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f3878-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="f3878-122">Description</span><span class="sxs-lookup"><span data-stu-id="f3878-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3878-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f3878-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f3878-124">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f3878-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3878-125">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="f3878-125">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="f3878-126">Les paramètres d’index de tuple spécifiés ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="f3878-126">The specified tuple index parameters were not allowed.</span></span> <span data-ttu-id="f3878-127">Cette erreur peut être retournée par <strong>JetEnableMultiInstance</strong> uniquement lorsque vous définissez <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>ou <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> sur une valeur non conforme.</span><span class="sxs-lookup"><span data-stu-id="f3878-127">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="f3878-128"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f3878-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3878-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="f3878-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="f3878-130">Le chemin d’accès au système de fichiers spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f3878-130">The specified file system path was invalid.</span></span> <span data-ttu-id="f3878-131">Cette erreur peut être retournée par <strong>JetEnableMultiInstance</strong> uniquement lors de la définition des paramètres système qui représentent les chemins d’accès du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f3878-131">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="f3878-132">Par exemple, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> pouvez retourner cette erreur.</span><span class="sxs-lookup"><span data-stu-id="f3878-132">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> can return this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3878-133">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="f3878-133">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="f3878-134">L’opération a échoué, car elle n’est pas conforme lorsque le moteur de base de données fonctionne en mode d’instance unique (mode de compatibilité Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="f3878-134">The operation failed because it is illegal when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3878-135">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="f3878-135">JET_errSystemParamsAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="f3878-136"><strong>JetEnableMultiInstance</strong> a échoué, car le moteur est déjà en mode multi-instance.</span><span class="sxs-lookup"><span data-stu-id="f3878-136"><strong>JetEnableMultiInstance</strong> failed because the engine is already in multi-instance mode.</span></span></p>
<p><span data-ttu-id="f3878-137"><strong>Remarque  </strong> Cela se produit même si aucun paramètre système n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="f3878-137"><strong>Note  </strong>This will happen even if no system parameters are specified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3878-138">Si cette fonction fonctionne, le moteur de base de données sera configuré pour s’exécuter en mode multi-instance.</span><span class="sxs-lookup"><span data-stu-id="f3878-138">If this function succeeds, the database engine will be configured to run in multi-instance mode.</span></span> <span data-ttu-id="f3878-139">Le moteur a été configuré avec succès avec la liste facultative de paramètres système globaux.</span><span class="sxs-lookup"><span data-stu-id="f3878-139">The engine was also successfully configured with the optional list of global system parameters.</span></span>

<span data-ttu-id="f3878-140">Si cette fonction échoue, le moteur de base de données reste dans le mode actuel.</span><span class="sxs-lookup"><span data-stu-id="f3878-140">If this function fails, the database engine will remain in the current mode.</span></span> <span data-ttu-id="f3878-141">Si *pcsetsucceed* est différent de zéro, ce nombre de paramètres système restera défini.</span><span class="sxs-lookup"><span data-stu-id="f3878-141">If *pcsetsucceed* is non-zero, that number of system parameters will remain set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f3878-142">Notes</span><span class="sxs-lookup"><span data-stu-id="f3878-142">Remarks</span></span>

<span data-ttu-id="f3878-143">Cette fonction doit être utilisée uniquement si l’application doit configurer de manière atomique un ensemble donné de paramètres système lors de la configuration du moteur de base de données pour une utilisation dans un scénario multi-utilisateur dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="f3878-143">This function should only be used if the application must configure a given set of system parameters atomically when setting up the database engine for use in a multi-user scenario in the same process.</span></span> <span data-ttu-id="f3878-144">Si une autre méthode de synchronisation est disponible, il est préférable d’appeler [JetCreateInstance](./jetcreateinstance-function.md) et [JetSetSystemParameter](./jetsetsystemparameter-function.md) séparément.</span><span class="sxs-lookup"><span data-stu-id="f3878-144">If another method of synchronization is available, it is preferable to call [JetCreateInstance](./jetcreateinstance-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) separately.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f3878-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3878-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3878-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f3878-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f3878-147">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f3878-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3878-148"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f3878-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f3878-149">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f3878-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3878-150"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f3878-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f3878-151">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f3878-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3878-152"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="f3878-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f3878-153">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f3878-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3878-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f3878-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f3878-155">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f3878-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3878-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f3878-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f3878-157">Implémenté en tant que <strong>JetEnableMultiInstanceW</strong> (Unicode) et <strong>JetEnableMultiInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f3878-157">Implemented as <strong>JetEnableMultiInstanceW</strong> (Unicode) and <strong>JetEnableMultiInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f3878-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3878-158">See Also</span></span>

[<span data-ttu-id="f3878-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f3878-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f3878-160">JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="f3878-160">JET_SETSYSPARAM</span></span>](./jet-setsysparam-structure.md)  
[<span data-ttu-id="f3878-161">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="f3878-161">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="f3878-162">JetInit</span><span class="sxs-lookup"><span data-stu-id="f3878-162">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="f3878-163">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="f3878-163">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
