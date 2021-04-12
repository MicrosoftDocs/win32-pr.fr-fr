---
description: 'En savoir plus sur : fonction JetGetSystemParameter'
title: JetGetSystemParameter fonction)
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210100"
---
# <a name="jetgetsystemparameter-function"></a><span data-ttu-id="6bc7b-103">JetGetSystemParameter fonction)</span><span class="sxs-lookup"><span data-stu-id="6bc7b-103">JetGetSystemParameter Function</span></span>


<span data-ttu-id="6bc7b-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="6bc7b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsystemparameter-function"></a><span data-ttu-id="6bc7b-105">JetGetSystemParameter fonction)</span><span class="sxs-lookup"><span data-stu-id="6bc7b-105">JetGetSystemParameter Function</span></span>

<span data-ttu-id="6bc7b-106">La fonction **JetGetSystemParameter** lit les nombreux paramètres de configuration du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-106">The **JetGetSystemParameter** function reads the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="6bc7b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bc7b-107">Parameters</span></span>

<span data-ttu-id="6bc7b-108">*instancié*</span><span class="sxs-lookup"><span data-stu-id="6bc7b-108">*instance*</span></span>

<span data-ttu-id="6bc7b-109">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-109">The instance to use for this call.</span></span>

<span data-ttu-id="6bc7b-110">Pour Windows 2000, ce paramètre est ignoré et doit toujours avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-110">For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="6bc7b-111">Pour Windows XP et versions ultérieures, ce paramètre est quelque peu surchargé.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-111">For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="6bc7b-112">Si le moteur fonctionne en mode hérité (mode de compatibilité Windows 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la **valeur null** ou peut contenir l’instance réelle retournée par [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="6bc7b-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="6bc7b-113">Dans les deux cas, tous les paramètres système sont lus à partir de cette instance.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="6bc7b-114">Si le moteur fonctionne en mode multi-instance, ce paramètre peut avoir la **valeur null** ou être un pointeur vers une instance créée à l’aide de [JetInit](./jetinit-function.md) ou [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="6bc7b-114">If the engine is operating in multi-instance mode, this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateInstance](./jetcreateinstance-function.md).</span></span> <span data-ttu-id="6bc7b-115">Lorsque ce paramètre a la **valeur null** , le paramètre global du système (ou par défaut) est lu.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="6bc7b-116">Lorsque ce paramètre est une instance, le paramètre système défini pour cette instance est Read.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="6bc7b-117">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6bc7b-117">*sesid*</span></span>

<span data-ttu-id="6bc7b-118">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-118">The session to use for this call.</span></span>

<span data-ttu-id="6bc7b-119">Lorsqu’il est spécifié, l’instance spécifiée est ignorée et l’instance associée à la session est utilisée.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-119">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="6bc7b-120">*paramid*</span><span class="sxs-lookup"><span data-stu-id="6bc7b-120">*paramid*</span></span>

<span data-ttu-id="6bc7b-121">ID du paramètre système qui sera lu.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-121">The ID of the system parameter that will be read.</span></span>

<span data-ttu-id="6bc7b-122">Pour obtenir la liste complète des paramètres système et leurs propriétés, consultez [paramètres système](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="6bc7b-122">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="6bc7b-123">*plParam*</span><span class="sxs-lookup"><span data-stu-id="6bc7b-123">*plParam*</span></span>

<span data-ttu-id="6bc7b-124">Mémoire tampon de sortie qui reçoit la valeur du paramètre système sélectionné si ce paramètre système est d’un type entier.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-124">The output buffer that receives the value of the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="6bc7b-125">*szParam*</span><span class="sxs-lookup"><span data-stu-id="6bc7b-125">*szParam*</span></span>

<span data-ttu-id="6bc7b-126">Mémoire tampon de sortie qui reçoit la valeur du paramètre système sélectionné si ce paramètre système est un type chaîne.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-126">The output buffer that receives the value of the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="6bc7b-127">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="6bc7b-127">*cbMax*</span></span>

<span data-ttu-id="6bc7b-128">Taille maximale, en octets, de la mémoire tampon de sortie de chaîne.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-128">The maximum size in bytes of the string output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="6bc7b-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6bc7b-129">Return Value</span></span>

<span data-ttu-id="6bc7b-130">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6bc7b-131">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6bc7b-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6bc7b-132">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6bc7b-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="6bc7b-133">Description</span><span class="sxs-lookup"><span data-stu-id="6bc7b-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bc7b-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6bc7b-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-135">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc7b-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6bc7b-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-137">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bc7b-138">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="6bc7b-138">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-139">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-139">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc7b-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6bc7b-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-141">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="6bc7b-142">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bc7b-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6bc7b-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-144">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="6bc7b-145">Cela peut se produire pour <strong>JetGetSystemParameter</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="6bc7b-145">This can happen for <strong>JetGetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="6bc7b-146">L’ID de paramètre système spécifié n’est pas valide ou n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-146">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="6bc7b-147">Le paramètre système spécifié requiert que la mémoire tampon de sortie entier soit fournie et que le pointeur de la mémoire tampon de sortie ait la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-147">The specified system parameter requires the integer output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="6bc7b-148">Le paramètre système spécifié requiert la spécification d’une mémoire tampon de sortie de chaîne et le pointeur de la mémoire tampon de sortie a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-148">The specified system parameter requires a string output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p>
<p><span data-ttu-id="6bc7b-149"><strong>Windows Vista :  </strong> Cela ne peut se produire que sur Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-149"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="6bc7b-150">Le paramètre système spécifié requiert la spécification d’une mémoire tampon de sortie de chaîne et la taille de cette mémoire tampon de sortie est trop petite pour accepter une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-150">The specified system parameter requires a string output buffer to be provided and the size of that output buffer is too small to accept a null terminated string.</span></span></p>
<p><span data-ttu-id="6bc7b-151"><strong>Windows Vista :  </strong> Cela ne peut se produire que sur Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-151"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="6bc7b-152">Le paramètre système spécifié ne peut pas être lu, car il est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-152">The specified system parameter cannot be read because it is write-only.</span></span></p></li>
<li><p><span data-ttu-id="6bc7b-153">Le paramètre système spécifié est global uniquement et une tentative a été effectuée pour lire une valeur spécifique à l’instance pour ce paramètre système.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-153">The specified system parameter is global only and an attempt was made to read an instance specific value for that system parameter.</span></span> <span data-ttu-id="6bc7b-154">Cela ne peut se produire que sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-154">This can only happen on Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="6bc7b-155">Le paramètre système spécifié est par instance uniquement et une tentative a été effectuée pour lire la valeur globale de ce paramètre système.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-155">The specified system parameter is per-instance only and an attempt was made to read the global value for that system parameter.</span></span> <span data-ttu-id="6bc7b-156">Cela ne peut se produire que sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-156">This can only happen on Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc7b-157">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6bc7b-157">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-158">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-158">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bc7b-159">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6bc7b-159">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-160">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-160">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc7b-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6bc7b-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-162">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bc7b-163">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="6bc7b-163">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-164">Le descripteur de session n’est pas valide ou fait référence à une session fermée.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-164">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="6bc7b-165">Cette erreur n’est pas retournée dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="6bc7b-166">Les handles ne sont validés qu’à titre d’effort optimal.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc7b-167">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="6bc7b-167">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-168">Le handle d’instance n’est pas valide ou fait référence à une instance qui a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-168">The instance handle is invalid or refers to an instance that has been shutdown.</span></span> <span data-ttu-id="6bc7b-169">Cette erreur n’est pas retournée dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-169">This error is not returned under all circumstances.</span></span> <span data-ttu-id="6bc7b-170">Les handles ne sont validés qu’à titre d’effort optimal.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-170">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="6bc7b-171"><strong>Windows Vista :  </strong> Cette erreur est renvoyée uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-171"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bc7b-172">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="6bc7b-172">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-173">L’opération s’est terminée correctement, mais la mémoire tampon de sortie était trop petite pour recevoir l’ensemble du paramètre système.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-173">The operation completed successfully, but the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="6bc7b-174">La mémoire tampon de sortie a été remplie avec la plus grande partie du paramètre système.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-174">The output buffer has been filled with as much of the system parameter setting as would fit.</span></span> <span data-ttu-id="6bc7b-175">Si la mémoire tampon de sortie a au moins un caractère de longueur, la chaîne de cette mémoire tampon de sortie se termine par une valeur null.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-175">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="6bc7b-176"><strong>Remarque  </strong> Cette erreur n’est pas renvoyée par toutes les mises en production.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-176"><strong>Note  </strong>This error is not returned by all releases.</span></span> <span data-ttu-id="6bc7b-177">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-177">Please see the Remarks section for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc7b-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="6bc7b-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="6bc7b-179">L’opération a échoué, car la mémoire tampon de sortie était trop petite pour recevoir l’ensemble du paramètre système.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-179">The operation failed because the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="6bc7b-180"><strong>Remarque  </strong> Cette erreur n’est pas retournée dans certains cas pour préserver la compatibilité des applications.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-180"><strong>Note  </strong>This error is not returned in some cases to preserve application compatibility.</span></span> <span data-ttu-id="6bc7b-181">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-181">Please see the Remarks section for more information.</span></span></p>
<p><span data-ttu-id="6bc7b-182"><strong>Windows Vista :  </strong> Cette erreur est renvoyée uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-182"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6bc7b-183">En cas de réussite, la mémoire tampon de sortie appropriée pour le paramètre système demandé sera définie sur la valeur de ce paramètre système.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-183">On success, the output buffer appropriate for the requested system parameter will be set to the value of that system parameter.</span></span>

<span data-ttu-id="6bc7b-184">En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-184">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6bc7b-185">Notes</span><span class="sxs-lookup"><span data-stu-id="6bc7b-185">Remarks</span></span>

<span data-ttu-id="6bc7b-186">Il existe un problème important dans cette API qui est présent dans toutes les versions.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-186">There is an important problem in this API that is present in all releases.</span></span> <span data-ttu-id="6bc7b-187">Si un paramètre système avec une valeur de chaîne est demandé et que la mémoire tampon de sortie est trop petite pour recevoir la totalité du paramètre système, JET_wrnBufferTruncated n’est pas retourné.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-187">If a system parameter with a string value is requested and the output buffer is too small to receive the entire system parameter setting, JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="6bc7b-188">JET_errSuccess est retourné à la place.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-188">JET_errSuccess is returned instead.</span></span> <span data-ttu-id="6bc7b-189">Si la longueur de la chaîne retournée est égale à la taille de la mémoire tampon de sortie inférieure au terminateur **null** , l’appelant doit réagir comme si JET_wrnBufferTruncated étaient retournés.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-189">If the length of the returned string is equal to the size of the output buffer less the **NULL** terminator, the caller should react as if JET_wrnBufferTruncated were returned.</span></span> <span data-ttu-id="6bc7b-190">Si une mémoire tampon de sortie de chaîne de taille zéro est spécifiée, l’appelant doit réagir comme si JET_errInvalidParameter étaient retournés.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-190">If a zero-sized string output buffer is specified, the caller should react as if JET_errInvalidParameter were returned.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6bc7b-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bc7b-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bc7b-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6bc7b-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6bc7b-193">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc7b-194"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="6bc7b-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6bc7b-195">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bc7b-196"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="6bc7b-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6bc7b-197">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc7b-198"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="6bc7b-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6bc7b-199">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bc7b-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6bc7b-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6bc7b-201">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6bc7b-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc7b-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6bc7b-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6bc7b-203">Implémenté en tant que <strong>JetGetSystemParameterW</strong> (Unicode) et <strong>JetGetSystemParameterA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6bc7b-203">Implemented as <strong>JetGetSystemParameterW</strong> (Unicode) and <strong>JetGetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6bc7b-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bc7b-204">See Also</span></span>

[<span data-ttu-id="6bc7b-205">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="6bc7b-205">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="6bc7b-206">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6bc7b-206">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6bc7b-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6bc7b-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="6bc7b-208">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6bc7b-208">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6bc7b-209">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="6bc7b-209">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="6bc7b-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="6bc7b-210">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="6bc7b-211">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6bc7b-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="6bc7b-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="6bc7b-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="6bc7b-213">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="6bc7b-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
