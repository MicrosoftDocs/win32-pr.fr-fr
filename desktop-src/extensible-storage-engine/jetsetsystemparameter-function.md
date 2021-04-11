---
description: 'En savoir plus sur : fonction JetSetSystemParameter'
title: JetSetSystemParameter fonction)
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201592"
---
# <a name="jetsetsystemparameter-function"></a><span data-ttu-id="56b38-103">JetSetSystemParameter fonction)</span><span class="sxs-lookup"><span data-stu-id="56b38-103">JetSetSystemParameter Function</span></span>


<span data-ttu-id="56b38-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="56b38-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsystemparameter-function"></a><span data-ttu-id="56b38-105">JetSetSystemParameter fonction)</span><span class="sxs-lookup"><span data-stu-id="56b38-105">JetSetSystemParameter Function</span></span>

<span data-ttu-id="56b38-106">La fonction **JetSetSystemParameter** est utilisée pour définir les nombreux paramètres de configuration du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="56b38-106">The **JetSetSystemParameter** function is used to set the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a><span data-ttu-id="56b38-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56b38-107">Parameters</span></span>

<span data-ttu-id="56b38-108">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="56b38-108">*pinstance*</span></span>

<span data-ttu-id="56b38-109">Spécifie l’instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="56b38-109">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="56b38-110">**Windows 2000 :**  Pour Windows 2000, ce paramètre est ignoré et doit toujours avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="56b38-110">**Windows 2000:**  For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="56b38-111">**Windows XP :**  Pour Windows XP et versions ultérieures, ce paramètre est quelque peu surchargé.</span><span class="sxs-lookup"><span data-stu-id="56b38-111">**Windows XP:**  For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="56b38-112">Si le moteur fonctionne en mode hérité (mode de compatibilité de Windows 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la **valeur null** ou peut contenir l’instance réelle retournée par [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="56b38-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="56b38-113">Dans les deux cas, tous les paramètres système sont lus à partir de cette instance.</span><span class="sxs-lookup"><span data-stu-id="56b38-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="56b38-114">Si le moteur fonctionne en mode multi-instance, ce paramètre peut avoir la **valeur null** ou être un pointeur vers une instance créée à l’aide de [JetInit](./jetinit-function.md) ou [JetCreateIndex](./jetcreateindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="56b38-114">If the engine is operating in multi-instance mode, then this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateIndex](./jetcreateindex-function.md).</span></span> <span data-ttu-id="56b38-115">Lorsque ce paramètre a la **valeur null** , le paramètre global du système (ou par défaut) est lu.</span><span class="sxs-lookup"><span data-stu-id="56b38-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="56b38-116">Lorsque ce paramètre est une instance, le paramètre système défini pour cette instance est Read.</span><span class="sxs-lookup"><span data-stu-id="56b38-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="56b38-117">Même s’il s’agit d’un paramètre de sortie techniquement, cette API ne modifie jamais le contenu de la mémoire tampon fournie.</span><span class="sxs-lookup"><span data-stu-id="56b38-117">Even though this is technically an out parameter, this API never modifies the contents of the provided buffer.</span></span>

<span data-ttu-id="56b38-118">*sesid*</span><span class="sxs-lookup"><span data-stu-id="56b38-118">*sesid*</span></span>

<span data-ttu-id="56b38-119">Spécifie la session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="56b38-119">Specifies the session to use for this call.</span></span>

<span data-ttu-id="56b38-120">Lorsqu’il est spécifié, l’instance spécifiée est ignorée et l’instance associée à la session est utilisée.</span><span class="sxs-lookup"><span data-stu-id="56b38-120">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="56b38-121">*paramid*</span><span class="sxs-lookup"><span data-stu-id="56b38-121">*paramid*</span></span>

<span data-ttu-id="56b38-122">ID du paramètre système qui sera défini.</span><span class="sxs-lookup"><span data-stu-id="56b38-122">The ID of the system parameter that will be set.</span></span> <span data-ttu-id="56b38-123">Pour obtenir la liste complète des paramètres système et leurs propriétés, consultez [paramètres système](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="56b38-123">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="56b38-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56b38-124">*lParam*</span></span>

<span data-ttu-id="56b38-125">Fournit la valeur à définir pour le paramètre système sélectionné si ce paramètre système est d’un type entier.</span><span class="sxs-lookup"><span data-stu-id="56b38-125">Provides the value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="56b38-126">*szParam*</span><span class="sxs-lookup"><span data-stu-id="56b38-126">*szParam*</span></span>

<span data-ttu-id="56b38-127">Fournit la valeur du paramètre système sélectionné si ce paramètre système est de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="56b38-127">Provides the value for the selected system parameter if that system parameter is of a string type.</span></span>

### <a name="return-value"></a><span data-ttu-id="56b38-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="56b38-128">Return Value</span></span>

<span data-ttu-id="56b38-129">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="56b38-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="56b38-130">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="56b38-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56b38-131">Code de retour</span><span class="sxs-lookup"><span data-stu-id="56b38-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="56b38-132">Description</span><span class="sxs-lookup"><span data-stu-id="56b38-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56b38-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="56b38-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="56b38-134">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="56b38-134">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="56b38-135"><strong>Windows Vista :</strong>  Sur Windows Vista et les versions ultérieures, la réussite peut être retournée sans modification de la valeur du paramètre du système.</span><span class="sxs-lookup"><span data-stu-id="56b38-135"><strong>Windows Vista:</strong>  On Windows Vista and later releases, success can be returned without a change to the system parameter's value.</span></span> <span data-ttu-id="56b38-136">Pour plus d’informations, consultez le paramètre système JET_paramEnableAdvanced dans la rubrique <a href="gg269346(v=exchg.10).md">méta-paramètres</a> .</span><span class="sxs-lookup"><span data-stu-id="56b38-136">See the JET_paramEnableAdvanced system parameter in the <a href="gg269346(v=exchg.10).md">Meta Parameters</a> topic for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b38-137">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="56b38-137">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="56b38-138">L’instance a été initialisée à l’aide d’un appel à <a href="gg294068(v=exchg.10).md">JetInit</a> et cette opération ne peut pas être exécutée en conséquence.</span><span class="sxs-lookup"><span data-stu-id="56b38-138">The instance has been initialized using a call to <a href="gg294068(v=exchg.10).md">JetInit</a> and this operation cannot be performed as a result.</span></span> <span data-ttu-id="56b38-139">Cela peut se produire pour <strong>JetSetSystemParameter</strong> quand une tentative est faite pour configurer un paramètre système après qu’une modification de sa valeur ne peut pas affecter l’état du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="56b38-139">This can happen for <strong>JetSetSystemParameter</strong> when an attempt is made to configure a system parameter after a change in its value cannot affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b38-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="56b38-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="56b38-141">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="56b38-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b38-142">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="56b38-142">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="56b38-143">Les paramètres d’index de tuple spécifiés ne sont pas conformes.</span><span class="sxs-lookup"><span data-stu-id="56b38-143">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="56b38-144">Cette erreur peut être retournée par <strong>JetSetSystemParameter</strong> uniquement lorsque vous définissez <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>ou <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> sur une valeur non conforme.</span><span class="sxs-lookup"><span data-stu-id="56b38-144">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="56b38-145"><strong>Windows XP et Windows Server 2003 :</strong>  Cela ne peut se produire que sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56b38-145"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b38-146">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="56b38-146">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="56b38-147">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="56b38-147">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b38-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="56b38-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="56b38-149">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="56b38-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="56b38-150"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="56b38-150"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b38-151">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="56b38-151">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="56b38-152">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="56b38-152">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="56b38-153">Cela peut se produire pour <strong>JetSetSystemParameter</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="56b38-153">This can happen for <strong>JetSetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="56b38-154">L’ID de paramètre système spécifié n’est pas valide ou n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="56b38-154">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="56b38-155">Une tentative a été effectuée pour définir un paramètre système à valeur de chaîne avec une chaîne dont la longueur était en dehors de la plage autorisée pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="56b38-155">An attempt was made to set a string-valued system parameter with a string whose length was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="56b38-156">Une tentative a été effectuée pour définir un paramètre système à valeur de chaîne avec un chemin d’accès de fichier où la longueur de sa représentation de chemin d’accès absolu était en dehors de la plage autorisée pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="56b38-156">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p>
<p><span data-ttu-id="56b38-157"><strong>Windows Vista :</strong>  Cela ne peut se produire que sur Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="56b38-157"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="56b38-158">Une tentative a été effectuée pour définir un paramètre système de valeur entière avec un entier qui se trouvait en dehors de la plage autorisée pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="56b38-158">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="56b38-159">Une tentative a été effectuée pour définir JET_paramUnicodeIndexDefault avec un pointeur de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> <strong>null</strong> , un LCID non valide ou un jeu d’indicateurs LCMapString non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="56b38-159">An attempt was made to set JET_paramUnicodeIndexDefault with a <strong>NULL</strong> <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of LCMapString flags.</span></span></p>
<p><span data-ttu-id="56b38-160"><strong>Windows Vista :</strong>  Cela ne peut se produire que sur Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="56b38-160"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="56b38-161">Impossible de définir le paramètre système spécifié, car il est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="56b38-161">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="56b38-162">Une tentative de définition d’un paramètre système a été effectuée après l’appel de <a href="gg294068(v=exchg.10).md">JetInit</a> , le moteur de base de données est en mode d’instance unique et aucune session n’a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="56b38-162">An attempt was made to set a system parameter after <a href="gg294068(v=exchg.10).md">JetInit</a> was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p>
<p><span data-ttu-id="56b38-163"><strong>Windows XP et Windows Server 2003 :</strong>  Cela ne peut se produire que sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56b38-163"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="56b38-164">Le paramètre système spécifié est global uniquement et une tentative a été effectuée pour définir une valeur spécifique à une instance pour ce paramètre système.</span><span class="sxs-lookup"><span data-stu-id="56b38-164">The specified system parameter is global only and an attempt was made to set an instance specific value for that system parameter.</span></span></p>
<p><span data-ttu-id="56b38-165"><strong>Windows XP et Windows Server 2003 :</strong>  Cela ne peut se produire que sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56b38-165"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="56b38-166">Le paramètre système spécifié est par instance uniquement et une tentative de définition de la valeur globale pour ce paramètre système a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="56b38-166">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p>
<p><span data-ttu-id="56b38-167"><strong>Windows XP et Windows Server 2003 :</strong>  Cela ne peut se produire que sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56b38-167"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b38-168">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="56b38-168">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="56b38-169">Le chemin d’accès au système de fichiers spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="56b38-169">The specified file system path was invalid.</span></span> <span data-ttu-id="56b38-170">Cette erreur peut être retournée par <strong>JetSetSystemParameter</strong> uniquement lors de la définition des paramètres système qui représentent les chemins d’accès du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="56b38-170">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="56b38-171">Par exemple, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> peut retourner cette erreur.</span><span class="sxs-lookup"><span data-stu-id="56b38-171">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> may return this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b38-172">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="56b38-172">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="56b38-173">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="56b38-173">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b38-174">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="56b38-174">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="56b38-175">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="56b38-175">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b38-176">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="56b38-176">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="56b38-177">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="56b38-177">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b38-178">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="56b38-178">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="56b38-179">Le descripteur de session n’est pas valide ou fait référence à une session fermée.</span><span class="sxs-lookup"><span data-stu-id="56b38-179">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="56b38-180">Cette erreur n’est pas retournée dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="56b38-180">This error is not returned under all circumstances.</span></span> <span data-ttu-id="56b38-181">Les handles ne sont validés qu’à titre d’effort optimal.</span><span class="sxs-lookup"><span data-stu-id="56b38-181">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b38-182">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="56b38-182">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="56b38-183">Le handle d’instance n’est pas valide ou fait référence à une instance qui a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="56b38-183">The instance handle is invalid or refers to an instance that has been shutdown.</span></span></p>
<p><span data-ttu-id="56b38-184">Cette erreur n’est pas retournée dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="56b38-184">This error is not returned under all circumstances.</span></span> <span data-ttu-id="56b38-185">Les handles ne sont validés qu’à titre d’effort optimal.</span><span class="sxs-lookup"><span data-stu-id="56b38-185">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="56b38-186"><strong>Windows Vista :</strong>  Cette erreur est renvoyée uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="56b38-186"><strong>Windows Vista:</strong>  This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56b38-187">En cas de réussite, le paramètre du paramètre système est défini sur la valeur fournie.</span><span class="sxs-lookup"><span data-stu-id="56b38-187">On success, the setting for the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="56b38-188">En cas d’échec, le paramètre du paramètre système reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="56b38-188">On failure, the setting for the system parameter will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="56b38-189">Notes</span><span class="sxs-lookup"><span data-stu-id="56b38-189">Remarks</span></span>

<span data-ttu-id="56b38-190">**JetSetSystemParameter** effectue une tâche médiocre de validation du paramètre choisi pour chaque paramètre système.</span><span class="sxs-lookup"><span data-stu-id="56b38-190">**JetSetSystemParameter** does a poor job of validating the chosen setting for each system parameter.</span></span> <span data-ttu-id="56b38-191">Vous devez veiller à ne pas compter sur cette validation pour appliquer les bons paramètres.</span><span class="sxs-lookup"><span data-stu-id="56b38-191">Care must be taken to not rely on this validation to enforce good settings.</span></span> <span data-ttu-id="56b38-192">Veuillez prêter une attention particulière à la description de chaque paramètre système et suivez ces instructions pour un paramètre système correct.</span><span class="sxs-lookup"><span data-stu-id="56b38-192">Please pay close attention to the description of each system parameter and follow those guidelines for a good system parameter setting.</span></span>

<span data-ttu-id="56b38-193">Il existe un ensemble de paramètres système qui doivent toujours être définis pour garantir que le moteur de base de données fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="56b38-193">There are a set of system parameters that should always be set to guarantee that the database engine works as intended.</span></span> <span data-ttu-id="56b38-194">Plus précisément, tous les paramètres système qui affectent la disposition physique des fichiers utilisés par le moteur de base de données doivent toujours être définis.</span><span class="sxs-lookup"><span data-stu-id="56b38-194">Specifically, any system parameters that affect the physical layout of the files used by the database engine should always be set.</span></span> <span data-ttu-id="56b38-195">Pour plus d’informations, consultez [paramètres système](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="56b38-195">For more information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="56b38-196">Chaque paramètre système a une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="56b38-196">Every system parameter has a default value.</span></span> <span data-ttu-id="56b38-197">Ces valeurs par défaut ont évolué au fil du temps et sont relativement arbitraires.</span><span class="sxs-lookup"><span data-stu-id="56b38-197">These default values have evolved over time and are quite arbitrary.</span></span> <span data-ttu-id="56b38-198">Il est fortement recommandé qu’une application évalue toutes les valeurs par défaut pour s’assurer qu’elles sont appropriées.</span><span class="sxs-lookup"><span data-stu-id="56b38-198">It is highly recommended that an application evaluate all the default values to ensure that they are appropriate.</span></span> <span data-ttu-id="56b38-199">S’ils ne sont pas appropriés, ils doivent être configurés par l’application.</span><span class="sxs-lookup"><span data-stu-id="56b38-199">If they are not appropriate, then they should be configured by the application.</span></span> <span data-ttu-id="56b38-200">Cela est important, car un grand nombre de ces paramètres peuvent avoir un impact considérable sur la fiabilité, les performances et l’utilisation des ressources du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="56b38-200">This is important as many of these parameters can greatly impact the reliability, performance, and resource utilization of the database engine.</span></span>

#### <a name="requirements"></a><span data-ttu-id="56b38-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56b38-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56b38-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="56b38-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="56b38-203">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="56b38-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b38-204"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="56b38-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="56b38-205">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="56b38-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b38-206"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="56b38-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="56b38-207">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="56b38-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b38-208"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="56b38-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="56b38-209">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="56b38-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56b38-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="56b38-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="56b38-211">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="56b38-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56b38-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="56b38-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="56b38-213">Implémenté en tant que <strong>JetSetSystemParameterW</strong> (Unicode) et <strong>JetSetSystemParameterA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="56b38-213">Implemented as <strong>JetSetSystemParameterW</strong> (Unicode) and <strong>JetSetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="56b38-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56b38-214">See Also</span></span>

[<span data-ttu-id="56b38-215">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="56b38-215">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="56b38-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="56b38-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="56b38-217">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="56b38-217">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="56b38-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="56b38-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="56b38-219">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="56b38-219">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="56b38-220">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="56b38-220">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="56b38-221">JetInit</span><span class="sxs-lookup"><span data-stu-id="56b38-221">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="56b38-222">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="56b38-222">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
