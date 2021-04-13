---
description: 'En savoir plus sur : fonction JetInit'
title: Fonction JetInit
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323462"
---
# <a name="jetinit-function"></a><span data-ttu-id="b6a34-103">Fonction JetInit</span><span class="sxs-lookup"><span data-stu-id="b6a34-103">JetInit Function</span></span>


<span data-ttu-id="b6a34-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="b6a34-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit-function"></a><span data-ttu-id="b6a34-105">Fonction JetInit</span><span class="sxs-lookup"><span data-stu-id="b6a34-105">JetInit Function</span></span>

<span data-ttu-id="b6a34-106">La fonction **JetInit** met le moteur de base de données dans un État où il peut prendre en charge l’utilisation des fichiers de base de données par l’application.</span><span class="sxs-lookup"><span data-stu-id="b6a34-106">The **JetInit** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="b6a34-107">Le moteur doit déjà être correctement configuré pour l’initialisation à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="b6a34-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="b6a34-108">La récupération après incident de la base de données s’effectue automatiquement dans le cadre du processus d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="b6a34-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a><span data-ttu-id="b6a34-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6a34-109">Parameters</span></span>

<span data-ttu-id="b6a34-110">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="b6a34-110">*pinstance*</span></span>

<span data-ttu-id="b6a34-111">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="b6a34-111">The instance to use for this call.</span></span>

<span data-ttu-id="b6a34-112">Pour Windows 2000, ce paramètre est ignoré et doit toujours avoir la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="b6a34-112">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="b6a34-113">Pour Windows XP et versions ultérieures, l’utilisation de ce paramètre dépend du mode de fonctionnement du moteur.</span><span class="sxs-lookup"><span data-stu-id="b6a34-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="b6a34-114">Si le moteur fonctionne en mode hérité (mode de compatibilité Windows 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la valeur NULL ou il peut avoir la valeur d’une mémoire tampon de sortie valide qui retourne le handle d’instance global créé comme effet secondaire de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="b6a34-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="b6a34-115">La valeur de cette mémoire tampon de sortie doit être NULL ou JET_instanceNil.</span><span class="sxs-lookup"><span data-stu-id="b6a34-115">This output buffer must be set to NULL or JET_instanceNil.</span></span> <span data-ttu-id="b6a34-116">Ce handle d’instance peut ensuite être passé à toute autre fonction qui utilise une instance.</span><span class="sxs-lookup"><span data-stu-id="b6a34-116">This instance handle can then be passed to any other function that uses an instance.</span></span> <span data-ttu-id="b6a34-117">Si le moteur fonctionne en mode multi-instance, ce paramètre doit être défini sur une mémoire tampon d’entrée valide qui contient le handle d’instance retourné par l’instance de fonction [JetCreateInstance](./jetcreateinstance-function.md) en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="b6a34-117">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function instance that is being initialized.</span></span>


#### <a name="remarks"></a><span data-ttu-id="b6a34-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b6a34-118">Remarks</span></span>

<span data-ttu-id="b6a34-119">Une instance doit être initialisée avec un appel à **JetInit** avant de pouvoir être utilisée par une autre chose que [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="b6a34-119">An instance must be initialized with a call to **JetInit** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="b6a34-120">Une instance est détruite par un appel à la fonction [JetTerm](./jetterm-function.md) , même si cette instance n’a jamais été initialisée à l’aide de **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="b6a34-120">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using **JetInit**.</span></span> <span data-ttu-id="b6a34-121">Une instance est l’unité de récupérabilité pour le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="b6a34-121">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="b6a34-122">Il contrôle le cycle de vie de tous les fichiers utilisés pour protéger l’intégrité des données dans un ensemble de fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="b6a34-122">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="b6a34-123">Ces fichiers incluent le fichier de point de contrôle et les fichiers journaux des transactions.</span><span class="sxs-lookup"><span data-stu-id="b6a34-123">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="b6a34-124">Le nombre maximal d’instances qui peuvent être créées à un moment donné est contrôlé par [JET_paramMaxInstances](./resource-parameters.md), qui peut être configurée par un appel à [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="b6a34-124">The maximum number of instances that can be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="b6a34-125">Lorsque le moteur de base de données est initialisé pour la première fois, **JetInit** crée un ensemble initial de fichiers pour prendre en charge cette instance.</span><span class="sxs-lookup"><span data-stu-id="b6a34-125">When the database engine is initialized for the first time, **JetInit** will create an initial set of files to support that instance.</span></span> <span data-ttu-id="b6a34-126">Ces fichiers incluent un fichier de point de contrôle (nommé \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), un ensemble de fichiers journaux de transactions réservés (nommés RES1. LOG et RES2. LOG), un fichier journal de transactions initial (nommé \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) et un fichier de base de données temporaire (nommé d’après [JET_paramTempPath](./temporary-database-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="b6a34-126">These files include a checkpoint file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.CHK), a set of reserved transaction log files (named RES1.LOG and RES2.LOG), an initial transaction log file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.LOG), and a temporary database file (named according to [JET_paramTempPath](./temporary-database-parameters.md)).</span></span> <span data-ttu-id="b6a34-127">Si [JET_paramRecovery](./transaction-log-parameters.md) est défini sur « désactivé », le fichier de point de contrôle et les fichiers journaux ne seront pas créés.</span><span class="sxs-lookup"><span data-stu-id="b6a34-127">If [JET_paramRecovery](./transaction-log-parameters.md) is set to "Off" then the checkpoint file and log files will not be created.</span></span> <span data-ttu-id="b6a34-128">Si [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) a la valeur zéro, le fichier de base de données temporaire ne sera pas créé.</span><span class="sxs-lookup"><span data-stu-id="b6a34-128">If [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) is set to zero then the temporary database file will not be created.</span></span> <span data-ttu-id="b6a34-129">Ces fichiers représentent la quantité d’espace disque d’une instance et doivent être gérés avec précaution.</span><span class="sxs-lookup"><span data-stu-id="b6a34-129">These files represent the on disk footprint of an instance and must be managed with care.</span></span> <span data-ttu-id="b6a34-130">Si ces fichiers sont endommagés individuellement ou par rapport à un autre, les données stockées dans les bases de données associées à l’instance peuvent être perdues.</span><span class="sxs-lookup"><span data-stu-id="b6a34-130">If these files are corrupted individually or with respect to one another then the data stored in the databases associated with the instance may be lost.</span></span>

<span data-ttu-id="b6a34-131">Lorsque le moteur de base de données est initialisé avec un ensemble existant de fichiers journaux de transactions, ces fichiers sont inspectés pour voir si la première version de l’instance a subi un incident.</span><span class="sxs-lookup"><span data-stu-id="b6a34-131">When the database engine is initialized with an existing set of transaction log files then those files will be inspected to see if the previous incarnation of the instance suffered from a crash.</span></span> <span data-ttu-id="b6a34-132">En cas de détection d’un incident, la récupération après incident est automatiquement effectuée.</span><span class="sxs-lookup"><span data-stu-id="b6a34-132">If a crash is detected then crash recovery will automatically be performed.</span></span> <span data-ttu-id="b6a34-133">Ce processus va reconstruire les bases de données attachées à l’instance au cours de la version précédente du moteur et enregistrer les modifications dans les fichiers de la base de données.</span><span class="sxs-lookup"><span data-stu-id="b6a34-133">This process will reconstruct the databases attached to the instance during the previous incarnation of the engine and save the changes back to the database files.</span></span> <span data-ttu-id="b6a34-134">Le résultat sera celui des bases de données qui sont cohérentes avec les transactions.</span><span class="sxs-lookup"><span data-stu-id="b6a34-134">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="b6a34-135">Ce processus peut prendre un certain temps si le nombre de fichiers du journal des transactions à relire sur les bases de données est important.</span><span class="sxs-lookup"><span data-stu-id="b6a34-135">It is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="b6a34-136">En raison du fait que **JetInit** effectue la récupération après incident, presque toutes les erreurs du moteur de base de données peuvent être retournées en cas de défaillance.</span><span class="sxs-lookup"><span data-stu-id="b6a34-136">Due to the fact that **JetInit** performs crash recovery, it is possible for almost any database engine error to be returned in the event of a failure.</span></span> <span data-ttu-id="b6a34-137">Dans la pratique, la plupart des erreurs rencontrées dans le déploiement se répartissent en deux catégories : la corruption des données et la gestion des fichiers.</span><span class="sxs-lookup"><span data-stu-id="b6a34-137">In practice, most of the errors seen in deployment fall into two categories: data corruption and file mismanagement.</span></span> <span data-ttu-id="b6a34-138">Les données endommagées se manifestent le plus souvent dans les erreurs suivantes ou similaires :</span><span class="sxs-lookup"><span data-stu-id="b6a34-138">Data corruption will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="b6a34-139">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="b6a34-139">JET_errReadVerifyFailure</span></span>

  - <span data-ttu-id="b6a34-140">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="b6a34-140">JET_errLogFileCorrupt</span></span>

  - <span data-ttu-id="b6a34-141">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="b6a34-141">JET_errCheckpointCorrupt</span></span>

<span data-ttu-id="b6a34-142">Ces erreurs sont presque toujours dues à des problèmes matériels et ne peuvent donc pas être évitées.</span><span class="sxs-lookup"><span data-stu-id="b6a34-142">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="b6a34-143">La gestion des erreurs de fichier se manifeste le plus souvent dans les erreurs suivantes ou similaires :</span><span class="sxs-lookup"><span data-stu-id="b6a34-143">File mismanagement will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="b6a34-144">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="b6a34-144">JET_errMissingLogFile</span></span>

  - <span data-ttu-id="b6a34-145">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="b6a34-145">JET_errAttachedDatabaseMismatch</span></span>

  - <span data-ttu-id="b6a34-146">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b6a34-146">JET_errDatabaseSharingViolation</span></span>

  - <span data-ttu-id="b6a34-147">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="b6a34-147">JET_errInvalidLogSequence</span></span>

<span data-ttu-id="b6a34-148">Si la récupération s’exécute sur un ensemble de journaux, pour lesquels toutes les bases de données ne sont pas présentes (ce qui renvoie l’erreur JET_errAttachedDatabaseMismatch dans des conditions normales), et que le client souhaite que la récupération se poursuive malgré les bases de données manquantes, le JET_ bitReplayIgnoreMissingDB peut être utilisé pour poursuivre la récupération des bases de données disponibles.</span><span class="sxs-lookup"><span data-stu-id="b6a34-148">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB can be used to continue recovery for the available databases.</span></span> <span data-ttu-id="b6a34-149">Ces erreurs sont empêchables par l’application.</span><span class="sxs-lookup"><span data-stu-id="b6a34-149">These errors are preventable by the application.</span></span> <span data-ttu-id="b6a34-150">L’application doit veiller à protéger le référentiel de ces fichiers contre les manipulations en dehors des forces, telles que l’utilisateur ou d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="b6a34-150">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="b6a34-151">Si l’application souhaite détruire entièrement une instance, tous les fichiers associés à l’instance doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="b6a34-151">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="b6a34-152">Celles-ci incluent le fichier de point de contrôle, les fichiers journaux des transactions et les fichiers de base de données attachés à l’instance.</span><span class="sxs-lookup"><span data-stu-id="b6a34-152">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="b6a34-153">La fonction **JetInit** se comporte différemment, en ce qui concerne les fichiers de base de données attachés à l’instance, entre Windows 2000 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b6a34-153">The **JetInit** function behaves differently, with respect to database files attached to the instance, between Windows 2000 and later releases.</span></span>

<span data-ttu-id="b6a34-154">**Windows 2000 :**  Dans Windows 2000, toute base de données attachée à l’instance pendant une version précédente de cette instance reste attachée à l’instance une fois que **JetInit** s’est terminé avec succès.</span><span class="sxs-lookup"><span data-stu-id="b6a34-154">**Windows 2000:**  In Windows 2000, any database attached to the instance during a previous incarnation of that instance remains attached to the instance after **JetInit** completes successfully.</span></span> <span data-ttu-id="b6a34-155">Il n’est pas nécessaire d’appeler [JetAttachDatabase](./jetattachdatabase-function.md) après **JetInit** pour vous assurer de l’accès ultérieur à la base de données.</span><span class="sxs-lookup"><span data-stu-id="b6a34-155">It is not necessary to call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit** to insure later database access.</span></span> <span data-ttu-id="b6a34-156">Si la fonction [JetAttachDatabase](./jetattachdatabase-function.md) est appelée après la fonction **JetInit** , le JET_wrnDatabaseAttached avertissement est retourné.</span><span class="sxs-lookup"><span data-stu-id="b6a34-156">If the [JetAttachDatabase](./jetattachdatabase-function.md) function is called after the **JetInit** function, the JET_wrnDatabaseAttached warning will be returned.</span></span> <span data-ttu-id="b6a34-157">Cet avertissement indique que la pièce jointe de la base de données a été conservée et peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="b6a34-157">This warning indicates that the database attachment was preserved and can be ignored.</span></span>

<span data-ttu-id="b6a34-158">**Windows XP :**  Dans Windows XP et versions ultérieures, toutes les bases de données sont automatiquement détachées de l’instance par **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="b6a34-158">**Windows XP:**  In Windows XP and later releases, all databases are automatically detached from the instance by **JetInit**.</span></span> <span data-ttu-id="b6a34-159">Cela signifie que [JetAttachDatabase](./jetattachdatabase-function.md) doit toujours être appelé après **JetInit** dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="b6a34-159">This means that [JetAttachDatabase](./jetattachdatabase-function.md) must always be called after **JetInit** in this case.</span></span>

<span data-ttu-id="b6a34-160">Toute application écrite pour s’exécuter sur Windows 2000 et les versions ultérieures doit toujours appeler [JetAttachDatabase](./jetattachdatabase-function.md) après **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="b6a34-160">Any application written to run on Windows 2000 and on later releases must always call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit**.</span></span> <span data-ttu-id="b6a34-161">Si l’application s’exécute sur Windows 2000, elle doit s’attendre à voir JET_wrnDatabaseAttached dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="b6a34-161">If the application runs on Windows 2000 then it must expect to see JET_wrnDatabaseAttached in some cases.</span></span> <span data-ttu-id="b6a34-162">Pour plus d’informations, consultez [JetAttachDatabase](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a34-162">See [JetAttachDatabase](./jetattachdatabase-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b6a34-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6a34-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6a34-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b6a34-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b6a34-165">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="b6a34-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6a34-166"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="b6a34-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b6a34-167">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b6a34-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6a34-168"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="b6a34-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b6a34-169">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="b6a34-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6a34-170"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="b6a34-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b6a34-171">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b6a34-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6a34-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b6a34-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b6a34-173">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b6a34-173">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b6a34-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6a34-174">See Also</span></span>

[<span data-ttu-id="b6a34-175">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="b6a34-175">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="b6a34-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b6a34-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b6a34-177">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b6a34-177">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b6a34-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b6a34-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b6a34-179">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="b6a34-179">JET_paramMaxTemporaryTables</span></span>](./temporary-database-parameters.md)  
[<span data-ttu-id="b6a34-180">JET_paramRecovery</span><span class="sxs-lookup"><span data-stu-id="b6a34-180">JET_paramRecovery</span></span>](./transaction-log-parameters.md)  
[<span data-ttu-id="b6a34-181">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="b6a34-181">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="b6a34-182">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="b6a34-182">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="b6a34-183">JetInit3</span><span class="sxs-lookup"><span data-stu-id="b6a34-183">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="b6a34-184">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="b6a34-184">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
