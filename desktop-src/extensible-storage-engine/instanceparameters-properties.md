---
description: 'En savoir plus sur les propriétés suivantes : InstanceParameters'
title: Propriétés InstanceParameters
TOCTitle: InstanceParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55103291
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0ac2b8aa959b8fa07f06e2de86dcfc173bab15ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559899"
---
# <a name="instanceparameters-properties"></a><span data-ttu-id="41427-103">Propriétés InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="41427-103">InstanceParameters properties</span></span>

<span data-ttu-id="41427-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="41427-104">Include protected members</span></span>  
<span data-ttu-id="41427-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="41427-105">Include inherited members</span></span>  

<span data-ttu-id="41427-106">Le type [InstanceParameters](./instanceparameters-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="41427-106">The [InstanceParameters](./instanceparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="41427-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="41427-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="41427-108">Nom</span><span class="sxs-lookup"><span data-stu-id="41427-108">Name</span></span></th>
<th><span data-ttu-id="41427-109">Description</span><span class="sxs-lookup"><span data-stu-id="41427-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span><span class="sxs-lookup"><span data-stu-id="41427-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span></span></td>
<td><span data-ttu-id="41427-112">Obtient ou définit le chemin d’accès relatif ou absolu du système de fichiers d’un dossier dans lequel la récupération après incident ou une opération de restauration peut trouver les bases de données référencées dans le journal des transactions dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="41427-112">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span><span class="sxs-lookup"><span data-stu-id="41427-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span></span></td>
<td><span data-ttu-id="41427-115">Obtient ou définit le préfixe à trois lettres utilisé pour la plupart des fichiers utilisés par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="41427-115">Gets or sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="41427-116">Par exemple, le fichier de point de contrôle est appelé EDB. CHK par défaut, car EDB est le nom de base par défaut.</span><span class="sxs-lookup"><span data-stu-id="41427-116">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="41427-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="41427-119">Obtient ou définit une valeur donnant le nombre de ressources de l’arborescence B + mises en cache par l’instance après que les tables qu’elles représentent ont été fermées par l’application.</span><span class="sxs-lookup"><span data-stu-id="41427-119">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="41427-120">Des valeurs élevées pour ce paramètre forcent le moteur de base de données à utiliser plus de mémoire, mais augmentent la vitesse avec laquelle un grand nombre de tables peut être ouvert de façon aléatoire par l’application.</span><span class="sxs-lookup"><span data-stu-id="41427-120">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="41427-121">Cela est utile pour les applications qui ont un schéma avec un très grand nombre de tables.</span><span class="sxs-lookup"><span data-stu-id="41427-121">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="41427-122">Pris en charge sur Windows Vista et les autres.</span><span class="sxs-lookup"><span data-stu-id="41427-122">Supported on Windows Vista and up.</span></span> <span data-ttu-id="41427-123">Ignoré sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="41427-123">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span><span class="sxs-lookup"><span data-stu-id="41427-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span></span></td>
<td><span data-ttu-id="41427-126">Obtient ou définit la propriété par instance pour les priorités relatives du cache (par défaut = 100).</span><span class="sxs-lookup"><span data-stu-id="41427-126">Gets or sets the per-instance property for relative cache priorities (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span><span class="sxs-lookup"><span data-stu-id="41427-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span></span></td>
<td><span data-ttu-id="41427-129">Obtient ou définit le seuil en octets pour le nombre de fichiers journaux des transactions qui doivent être relus après un incident.</span><span class="sxs-lookup"><span data-stu-id="41427-129">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="41427-130">Si la journalisation circulaire est activée à l’aide de CircularLog, ce paramètre contrôle également la quantité approximative de fichiers du journal des transactions qui seront conservés sur le disque.</span><span class="sxs-lookup"><span data-stu-id="41427-130">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span><span class="sxs-lookup"><span data-stu-id="41427-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span></span></td>
<td><span data-ttu-id="41427-133">Obtient ou définit une valeur indiquant si la journalisation circulaire est activée.</span><span class="sxs-lookup"><span data-stu-id="41427-133">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="41427-134">Lorsque la journalisation circulaire est désactivée, tous les fichiers journaux des transactions générés sont conservés sur le disque jusqu’à ce qu’ils ne soient plus nécessaires, car une sauvegarde complète de la base de données a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="41427-134">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="41427-135">Lorsque la journalisation circulaire est activée, seuls les fichiers journaux des transactions qui sont plus récents que le point de contrôle actuel sont conservés sur le disque.</span><span class="sxs-lookup"><span data-stu-id="41427-135">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="41427-136">L’avantage de ce mode est que les sauvegardes ne sont pas nécessaires pour supprimer les anciens fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="41427-136">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span><span class="sxs-lookup"><span data-stu-id="41427-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span></span></td>
<td><span data-ttu-id="41427-139">Obtient ou définit une valeur indiquant si JetInit échoue lorsque le moteur de base de données est configuré pour démarrer à l’aide des fichiers du journal des transactions sur un disque d’une taille différente de celle configurée.</span><span class="sxs-lookup"><span data-stu-id="41427-139">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="41427-140">Normalement, <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> récupère les bases de données, mais échoue avec <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> pour indiquer que la taille du fichier journal n’est pas correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="41427-140">Normally, <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> will successfully recover the databases but will fail with <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="41427-141">Toutefois, lorsque ce paramètre est défini sur true, le moteur de base de données supprime silencieusement tous les anciens fichiers journaux, puis démarre un nouvel ensemble de fichiers journaux de transactions à l’aide de la taille de fichier journal configurée.</span><span class="sxs-lookup"><span data-stu-id="41427-141">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="41427-142">Ce paramètre est utile lorsque l’application souhaite modifier en toute transparence la taille du fichier journal des transactions, tout en continuant à travailler de manière transparente dans les scénarios de mise à niveau et de restauration.</span><span class="sxs-lookup"><span data-stu-id="41427-142">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span><span class="sxs-lookup"><span data-stu-id="41427-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span></span></td>
<td><span data-ttu-id="41427-145">Obtient ou définit une valeur indiquant si ESENT crée sans assistance des dossiers manquants dans ses chemins d’accès de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="41427-145">Gets or sets a value indicating whether ESENT will silently create folders that are missing in its filesystem paths.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span><span class="sxs-lookup"><span data-stu-id="41427-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span></span></td>
<td><span data-ttu-id="41427-148">Obtient ou définit le nombre de pages qui sont ajoutées à un fichier de base de données chaque fois qu’il doit croître pour accueillir davantage de données.</span><span class="sxs-lookup"><span data-stu-id="41427-148">Gets or sets the number of pages that are added to a database file each time it needs to grow to accommodate more data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span><span class="sxs-lookup"><span data-stu-id="41427-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span></span></td>
<td><span data-ttu-id="41427-151">Obtient ou définit l’intervalle maximal, en secondes, pour permettre à l’analyse de la base de données de se terminer.</span><span class="sxs-lookup"><span data-stu-id="41427-151">Gets or sets the maximum interval to allow the database scan to finish, in seconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span><span class="sxs-lookup"><span data-stu-id="41427-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span></span></td>
<td><span data-ttu-id="41427-154">Obtient ou définit l’intervalle minimal de répétition de l’analyse de la base de données, en secondes.</span><span class="sxs-lookup"><span data-stu-id="41427-154">Gets or sets the minimum interval to repeat the database scan, in seconds.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span><span class="sxs-lookup"><span data-stu-id="41427-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span></span></td>
<td><span data-ttu-id="41427-157">Obtient ou définit la limitation de l’analyse de la base de données, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="41427-157">Gets or sets the throttling of the database scan, in milliseconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span><span class="sxs-lookup"><span data-stu-id="41427-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span></span></td>
<td><span data-ttu-id="41427-160">Obtient ou définit une valeur indiquant si la maintenance de la base de données doit s’exécuter pendant la récupération.</span><span class="sxs-lookup"><span data-stu-id="41427-160">Gets or sets a value indicating whether Database Maintenance should run during recovery.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span><span class="sxs-lookup"><span data-stu-id="41427-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span></span></td>
<td><span data-ttu-id="41427-163">Obtient ou définit une valeur indiquant si la sérialisation de la maintenance de la base de données est activée pour les bases de données qui partagent le même disque.</span><span class="sxs-lookup"><span data-stu-id="41427-163">Gets or sets a value indicating whether database Maintenance serialization is enabled for databases sharing the same disk.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span><span class="sxs-lookup"><span data-stu-id="41427-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span></span></td>
<td><span data-ttu-id="41427-166">Obtient ou définit une valeur indiquant si <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> doit vérifier les index qui ont été générés à l’aide d’une version antérieure de la bibliothèque NLS dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="41427-166">Gets or sets a value indicating whether <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> will check for indexes that were build using an older version of the NLS library in the operating system.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span><span class="sxs-lookup"><span data-stu-id="41427-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span></span></td>
<td><span data-ttu-id="41427-169">Obtient ou définit une valeur indiquant si la défragmentation en ligne est activée.</span><span class="sxs-lookup"><span data-stu-id="41427-169">Gets or sets a value indicating whether online defragmentation is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span><span class="sxs-lookup"><span data-stu-id="41427-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span></span></td>
<td><span data-ttu-id="41427-172">Obtient ou définit une chaîne spécifique à l’application qui sera ajoutée à tous les messages du journal des événements émis par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="41427-172">Gets or sets an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="41427-173">Cela permet de corréler facilement les messages du journal des événements avec l’application source.</span><span class="sxs-lookup"><span data-stu-id="41427-173">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="41427-174">Par défaut, le nom de l’exécutable de l’application hôte sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="41427-174">By default the host application executable name will be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span><span class="sxs-lookup"><span data-stu-id="41427-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span></span></td>
<td><span data-ttu-id="41427-177">Obtient ou définit le nom du journal des événements que le moteur de base de données utilise pour ses messages de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="41427-177">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="41427-178">Par défaut, tous les messages du journal des événements sont envoyés dans le journal des événements de l’application.</span><span class="sxs-lookup"><span data-stu-id="41427-178">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="41427-179">Si le nom de la clé de registre d’un autre journal des événements est configuré, les messages du journal des événements y seront à la place.</span><span class="sxs-lookup"><span data-stu-id="41427-179">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span><span class="sxs-lookup"><span data-stu-id="41427-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span></span></td>
<td><span data-ttu-id="41427-182">Obtient ou définit la quantité de mémoire utilisée pour mettre en cache les enregistrements de journal avant leur écriture dans le fichier journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="41427-182">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="41427-183">L’unité de ce paramètre correspond à la taille de secteur du volume qui contient les fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="41427-183">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="41427-184">La taille des secteurs étant presque toujours de 512 octets, il est possible de supposer en toute sécurité la taille de l’unité.</span><span class="sxs-lookup"><span data-stu-id="41427-184">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="41427-185">Ce paramètre a un impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="41427-185">This parameter has an impact on performance.</span></span> <span data-ttu-id="41427-186">Lorsque le moteur de base de données subit une charge de mise à jour importante, cette mémoire tampon peut être entièrement très rapide.</span><span class="sxs-lookup"><span data-stu-id="41427-186">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="41427-187">Une plus grande taille de cache pour le fichier journal des transactions est essentielle pour garantir une bonne performance des mises à jour dans une condition de charge élevée.</span><span class="sxs-lookup"><span data-stu-id="41427-187">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="41427-188">La valeur par défaut est trop petite pour ce cas.</span><span class="sxs-lookup"><span data-stu-id="41427-188">The default is known to be too small for this case.</span></span> <span data-ttu-id="41427-189">Ne définissez pas ce paramètre sur un nombre de mémoires tampons plus grand (en octets) que la moitié de la taille d’un fichier journal de transactions.</span><span class="sxs-lookup"><span data-stu-id="41427-189">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-191"><a href="dn350991(v=exchg.10).md">Répertoire</a></span><span class="sxs-lookup"><span data-stu-id="41427-191"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span></span></td>
<td><span data-ttu-id="41427-192">Obtient ou définit le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra les journaux des transactions pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="41427-192">Gets or sets the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span><span class="sxs-lookup"><span data-stu-id="41427-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span></span></td>
<td><span data-ttu-id="41427-195">Obtient ou définit la taille des fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="41427-195">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="41427-196">Ce paramètre doit être défini en unités de 1024 octets (par exemple, un paramètre de 2048 donne des fichiers journaux de 2 Mo).</span><span class="sxs-lookup"><span data-stu-id="41427-196">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span><span class="sxs-lookup"><span data-stu-id="41427-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span></span></td>
<td><span data-ttu-id="41427-199">Obtient ou définit le nombre de ressources de curseur réservées pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="41427-199">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="41427-200">Une ressource de curseur correspond directement à un JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="41427-200">A cursor resource directly corresponds to a JET_TABLEID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span><span class="sxs-lookup"><span data-stu-id="41427-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span></span></td>
<td><span data-ttu-id="41427-203">Obtient ou définit le nombre de ressources de l’arborescence B + réservées pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="41427-203">Gets or sets the number of B+ Tree resources reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span><span class="sxs-lookup"><span data-stu-id="41427-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span></span></td>
<td><span data-ttu-id="41427-206">Obtient ou définit le nombre de ressources de sessions réservées pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="41427-206">Gets or sets the number of sessions resources reserved for this instance.</span></span> <span data-ttu-id="41427-207">Une ressource de session correspond directement à un JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="41427-207">A session resource directly corresponds to a JET_SESID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span><span class="sxs-lookup"><span data-stu-id="41427-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span></span></td>
<td><span data-ttu-id="41427-210">Obtient ou définit le nombre de ressources de table temporaire à utiliser par une instance.</span><span class="sxs-lookup"><span data-stu-id="41427-210">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="41427-211">Ce paramètre affecte le nombre de tables temporaires qui peuvent être utilisées en même temps.</span><span class="sxs-lookup"><span data-stu-id="41427-211">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="41427-212">Si ce paramètre système est défini à zéro, aucune base de données temporaire n’est créée et toute activité nécessitant l’utilisation de la base de données temporaire échoue.</span><span class="sxs-lookup"><span data-stu-id="41427-212">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="41427-213">Ce paramètre peut être utile pour éviter les e/s nécessaires à la création de la base de données temporaire si elle est connue qu’elle ne sera pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="41427-213">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span><span class="sxs-lookup"><span data-stu-id="41427-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span></span></td>
<td><span data-ttu-id="41427-216">Obtient ou définit le pourcentage de la Banque des versions qui peut être utilisée par la plus ancienne transaction avant <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (valeur par défaut = 100).</span><span class="sxs-lookup"><span data-stu-id="41427-216">Gets or sets the percentage of version store that can be used by oldest transaction before <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span><span class="sxs-lookup"><span data-stu-id="41427-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span></span></td>
<td><span data-ttu-id="41427-219">Obtient ou définit le nombre maximal de pages de la Banque des versions réservées pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="41427-219">Gets or sets the maximum number of version store pages reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span><span class="sxs-lookup"><span data-stu-id="41427-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span></span></td>
<td><span data-ttu-id="41427-222">Obtient ou définit une valeur indiquant si les messages du journal des événements d’information qui seraient normalement générés par le moteur de base de données seront supprimés.</span><span class="sxs-lookup"><span data-stu-id="41427-222">Gets or sets a value indicating whether informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span><span class="sxs-lookup"><span data-stu-id="41427-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span></span></td>
<td><span data-ttu-id="41427-225">Obtient ou définit une valeur indiquant si une seule base de données peut être ouverte à l’aide de JetOpenDatabase par une session donnée à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="41427-225">Gets or sets a value indicating whether only one database is allowed to be opened using JetOpenDatabase by a given session at one time.</span></span> <span data-ttu-id="41427-226">La base de données temporaire est exclue de cette restriction.</span><span class="sxs-lookup"><span data-stu-id="41427-226">The temporary database is excluded from this restriction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span><span class="sxs-lookup"><span data-stu-id="41427-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span></span></td>
<td><span data-ttu-id="41427-229">Obtient ou définit la taille initiale de la base de données temporaire.</span><span class="sxs-lookup"><span data-stu-id="41427-229">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="41427-230">La taille est dans les pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="41427-230">The size is in database pages.</span></span> <span data-ttu-id="41427-231">Une taille de zéro indique que la taille par défaut d’une base de données ordinaire doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="41427-231">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="41427-232">Il est souvent souhaitable que les petites applications configurent la base de données temporaire aussi petite que possible.</span><span class="sxs-lookup"><span data-stu-id="41427-232">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="41427-233">La définition de ce paramètre sur <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> permet d’obtenir la plus petite base de données temporaire possible.</span><span class="sxs-lookup"><span data-stu-id="41427-233">Setting this parameter to <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> will achieve the smallest temporary database possible.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span><span class="sxs-lookup"><span data-stu-id="41427-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span></span></td>
<td><span data-ttu-id="41427-236">Obtient ou définit le nombre préféré de pages de la Banque des versions réservées pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="41427-236">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="41427-237">Si la taille de la Banque des versions dépasse ce seuil, toutes les informations qui sont utilisées uniquement pour les tâches en arrière-plan facultatives, telles que la récupération de l’espace supprimé dans la base de données, sont sacrifiées pour conserver de l’espace pour les informations transactionnelles.</span><span class="sxs-lookup"><span data-stu-id="41427-237">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span><span class="sxs-lookup"><span data-stu-id="41427-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span></span></td>
<td><span data-ttu-id="41427-240">Obtient ou définit le nombre maximal d’opérations d’e/s distribuées pour un usage donné.</span><span class="sxs-lookup"><span data-stu-id="41427-240">Gets or sets the maximum number of I/O operations dispatched for a given purpose.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-242"><a href="dn350981(v=exchg.10).md">Récupération</a></span><span class="sxs-lookup"><span data-stu-id="41427-242"><a href="dn350981(v=exchg.10).md">Recovery</a></span></span></td>
<td><span data-ttu-id="41427-243">Obtient ou définit une valeur indiquant si la récupération sur incident est activée.</span><span class="sxs-lookup"><span data-stu-id="41427-243">Gets or sets a value indicating whether crash recovery is on.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span><span class="sxs-lookup"><span data-stu-id="41427-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span></span></td>
<td><span data-ttu-id="41427-246">Obtient ou définit le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra le fichier de point de contrôle de l’instance.</span><span class="sxs-lookup"><span data-stu-id="41427-246">Gets or sets the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span><span class="sxs-lookup"><span data-stu-id="41427-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span></span></td>
<td><span data-ttu-id="41427-249">Obtient ou définit le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra la base de données temporaire de l’instance.</span><span class="sxs-lookup"><span data-stu-id="41427-249">Gets or sets the relative or absolute file system path of the folder that will contain the temporary database for the instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span><span class="sxs-lookup"><span data-stu-id="41427-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span></span></td>
<td><span data-ttu-id="41427-252">Obtient ou définit le nombre d’éléments de travail de nettoyage en arrière-plan qui peuvent être mis en file d’attente dans le pool de threads du moteur de base de données à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="41427-252">Gets or sets the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="41427-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span><span class="sxs-lookup"><span data-stu-id="41427-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span></span></td>
<td><span data-ttu-id="41427-255">Obtient ou définit le nombre de journaux pour lesquels esent diffère le vidage de base de données.</span><span class="sxs-lookup"><span data-stu-id="41427-255">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="41427-256">Cela peut être utilisé pour augmenter la capacité de récupération de base de données en cas de perte de fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="41427-256">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="41427-257">Pris en charge sur Windows 7 et les autres.</span><span class="sxs-lookup"><span data-stu-id="41427-257">Supported on Windows 7 and up.</span></span> <span data-ttu-id="41427-258">Ignoré sur Windows XP, Windows Server 2003, Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="41427-258">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="41427-259">Haut</span><span class="sxs-lookup"><span data-stu-id="41427-259">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="41427-260">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41427-260">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="41427-261">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="41427-261">Reference</span></span>

[<span data-ttu-id="41427-262">InstanceParameters, classe</span><span class="sxs-lookup"><span data-stu-id="41427-262">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="41427-263">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="41427-263">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
