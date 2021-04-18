---
description: 'En savoir plus sur les propriétés : SystemParameters'
title: Propriétés SystemParameters
TOCTitle: SystemParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55104035
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 12e18b6c045758c8e9fd7ffb91f728c78dcf2e24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558425"
---
# <a name="systemparameters-properties"></a><span data-ttu-id="8102a-103">Propriétés SystemParameters</span><span class="sxs-lookup"><span data-stu-id="8102a-103">SystemParameters properties</span></span>

<span data-ttu-id="8102a-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="8102a-104">Include protected members</span></span>  
<span data-ttu-id="8102a-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="8102a-105">Include inherited members</span></span>  

<span data-ttu-id="8102a-106">Le type [SystemParameters](./systemparameters-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="8102a-106">The [SystemParameters](./systemparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="8102a-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8102a-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="8102a-108">Nom</span><span class="sxs-lookup"><span data-stu-id="8102a-108">Name</span></span></th>
<th><span data-ttu-id="8102a-109">Description</span><span class="sxs-lookup"><span data-stu-id="8102a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-112"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span><span class="sxs-lookup"><span data-stu-id="8102a-112"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span></span></td>
<td><span data-ttu-id="8102a-113">Obtient la taille maximale d’un signet.</span><span class="sxs-lookup"><span data-stu-id="8102a-113">Gets the maximum size of a bookmark.</span></span> <span data-ttu-id="8102a-114"><a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span><span class="sxs-lookup"><span data-stu-id="8102a-114"><a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-117"><a href="dn351214(v=exchg.10).md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="8102a-117"><a href="dn351214(v=exchg.10).md">CacheSize</a></span></span></td>
<td><span data-ttu-id="8102a-118">Obtient ou définit la taille du cache de base de données dans les pages.</span><span class="sxs-lookup"><span data-stu-id="8102a-118">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="8102a-119">Par défaut, le cache de base de données ajuste automatiquement sa taille, la définition de cette propriété sur une valeur différente de zéro entraîne l’ajustement du cache à la taille cible.</span><span class="sxs-lookup"><span data-stu-id="8102a-119">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-122"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span><span class="sxs-lookup"><span data-stu-id="8102a-122"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span></span></td>
<td><span data-ttu-id="8102a-123">Obtient ou définit la taille maximale du cache de la page de base de données.</span><span class="sxs-lookup"><span data-stu-id="8102a-123">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="8102a-124">La taille est dans les pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="8102a-124">The size is in database pages.</span></span> <span data-ttu-id="8102a-125">Si ce paramètre est laissé à sa valeur par défaut, la taille maximale du cache sera définie sur la taille de la mémoire physique lors de l’appel de JetInit.</span><span class="sxs-lookup"><span data-stu-id="8102a-125">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-128"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span><span class="sxs-lookup"><span data-stu-id="8102a-128"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span></span></td>
<td><span data-ttu-id="8102a-129">Obtient ou définit la taille minimale du cache de la page de base de données, dans les pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="8102a-129">Gets or sets the minimum size of the database page cache, in database pages.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-132"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="8102a-132"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span></span></td>
<td><span data-ttu-id="8102a-133">Obtient le nombre maximal de composants dans une clé de tri ou d’index.</span><span class="sxs-lookup"><span data-stu-id="8102a-133">Gets the maximum number of components in a sort or index key.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-136"><a href="dn351218(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="8102a-136"><a href="dn351218(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="8102a-137">Obtient ou définit une valeur qui spécifie les valeurs par défaut pour l’ensemble des paramètres système.</span><span class="sxs-lookup"><span data-stu-id="8102a-137">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="8102a-138">Quand ce paramètre est défini sur une configuration spécifique, toutes les valeurs des paramètres système sont réinitialisées à leurs valeurs par défaut pour cette configuration.</span><span class="sxs-lookup"><span data-stu-id="8102a-138">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="8102a-139">Si la configuration est définie pour une instance spécifique, les valeurs par défaut des paramètres système globaux ne sont pas réinitialisées.</span><span class="sxs-lookup"><span data-stu-id="8102a-139">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="8102a-140">Petite configuration (0) : le moteur de base de données est optimisé pour l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="8102a-140">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="8102a-141">Configuration héritée (1) : le moteur de base de données a ses valeurs par défaut traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="8102a-141">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="8102a-142">Pris en charge sur Windows Vista et les autres.</span><span class="sxs-lookup"><span data-stu-id="8102a-142">Supported on Windows Vista and up.</span></span> <span data-ttu-id="8102a-143">Ignoré sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8102a-143">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-146"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span><span class="sxs-lookup"><span data-stu-id="8102a-146"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span></span></td>
<td><span data-ttu-id="8102a-147">Obtient ou définit la taille des pages de base de données, en octets.</span><span class="sxs-lookup"><span data-stu-id="8102a-147">Gets or sets the size of the database pages, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-150"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="8102a-150"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="8102a-151">Obtient ou définit une valeur indiquant si le moteur de base de données accepte ou rejette les modifications apportées à un sous-ensemble des paramètres système.</span><span class="sxs-lookup"><span data-stu-id="8102a-151">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="8102a-152">Ce paramètre est utilisé conjointement avec la <a href="dn351218(v=exchg.10).md">configuration</a> pour empêcher la définition de certains paramètres système à partir des valeurs par défaut de la configuration sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8102a-152">This parameter is used in conjunction with <a href="dn351218(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="8102a-153">Pris en charge sur Windows Vista et les autres.</span><span class="sxs-lookup"><span data-stu-id="8102a-153">Supported on Windows Vista and up.</span></span> <span data-ttu-id="8102a-154">Ignoré sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8102a-154">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-157"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="8102a-157"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="8102a-158">Obtient ou définit une valeur indiquant si le moteur de base de données doit utiliser le cache de fichiers du système d’exploitation pour tous les fichiers managés.</span><span class="sxs-lookup"><span data-stu-id="8102a-158">Gets or sets a value indicating whether the database engine should use the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-161"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="8102a-161"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="8102a-162">Obtient ou définit une valeur indiquant si le moteur de base de données doit utiliser des e/s de fichier mappées en mémoire pour les fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="8102a-162">Gets or sets a value indicating whether the database engine should use memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-165"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span><span class="sxs-lookup"><span data-stu-id="8102a-165"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span></span></td>
<td><span data-ttu-id="8102a-166">Obtient ou définit le niveau de détail des messages EventLog émis dans le journal des événements par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="8102a-166">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="8102a-167">Des numéros plus élevés entraînent des messages EventLog plus détaillés.</span><span class="sxs-lookup"><span data-stu-id="8102a-167">Higher numbers will result in more detailed eventlog messages.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-170"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span><span class="sxs-lookup"><span data-stu-id="8102a-170"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span></span></td>
<td><span data-ttu-id="8102a-171">Obtient ou définit l’encodage de la valeur à utiliser avec les exceptions générées dans JET.</span><span class="sxs-lookup"><span data-stu-id="8102a-171">Gets or sets the value encoding what to do with exceptions generated within JET.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-174"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span><span class="sxs-lookup"><span data-stu-id="8102a-174"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span></span></td>
<td><span data-ttu-id="8102a-175">Obtient ou définit l’ensemble des actions à effectuer sur IOs qui apparaissent bloquées.</span><span class="sxs-lookup"><span data-stu-id="8102a-175">Gets or sets the set of actions to be taken on IOs that appear hung.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-178"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span><span class="sxs-lookup"><span data-stu-id="8102a-178"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span></span></td>
<td><span data-ttu-id="8102a-179">Obtient ou définit le seuil pour ce qui est considéré comme une e/s bloquée qui doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="8102a-179">Gets or sets the threshold for what is considered a hung IO that should be acted upon.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-182"><a href="dn351156(v=exchg.10).md">La plupart des</a></span><span class="sxs-lookup"><span data-stu-id="8102a-182"><a href="dn351156(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="8102a-183">Obtient la taille de clé maximale.</span><span class="sxs-lookup"><span data-stu-id="8102a-183">Gets the maximum key size.</span></span> <span data-ttu-id="8102a-184">Cela dépend de la version esent et de la taille de page de la base de données.</span><span class="sxs-lookup"><span data-stu-id="8102a-184">This depends on the Esent version and database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-187"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="8102a-187"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="8102a-188">Obtient ou définit la compatibilité descendante avec les conventions d’affectation des noms de fichiers des versions antérieures du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="8102a-188">Gets or sets backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-191"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span><span class="sxs-lookup"><span data-stu-id="8102a-191"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span></span></td>
<td><span data-ttu-id="8102a-192">Obtient la taille des segments LV.</span><span class="sxs-lookup"><span data-stu-id="8102a-192">Gets the lv chunks size.</span></span> <span data-ttu-id="8102a-193">Cela dépend de la taille de la page de base de données.</span><span class="sxs-lookup"><span data-stu-id="8102a-193">This depends on the database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-196"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span><span class="sxs-lookup"><span data-stu-id="8102a-196"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span></span></td>
<td><span data-ttu-id="8102a-197">Obtient ou définit le nombre maximal d’instances qui peuvent être créées.</span><span class="sxs-lookup"><span data-stu-id="8102a-197">Gets or sets the maximum number of instances that can be created.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-200"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span><span class="sxs-lookup"><span data-stu-id="8102a-200"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span></span></td>
<td><span data-ttu-id="8102a-201">Obtient ou définit la plus petite quantité de données qui doivent être compressées avec la compression Xpress.</span><span class="sxs-lookup"><span data-stu-id="8102a-201">Gets or sets the smallest amount of data that should be compressed with xpress compression.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-204"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span><span class="sxs-lookup"><span data-stu-id="8102a-204"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span></span></td>
<td><span data-ttu-id="8102a-205">Ce paramètre contrôle le nombre d’e/s de fichier de base de données qui peuvent être mises en file d’attente par disque dans le système d’exploitation hôte à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="8102a-205">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="8102a-206">Une valeur plus élevée pour ce paramètre peut améliorer considérablement les performances d’une application de base de données volumineuse.</span><span class="sxs-lookup"><span data-stu-id="8102a-206">A larger value for this parameter can significantly help the performance of a large database application.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-209"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span><span class="sxs-lookup"><span data-stu-id="8102a-209"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span></span></td>
<td><span data-ttu-id="8102a-210">Obtient ou définit le nom convivial de cette instance du processus.</span><span class="sxs-lookup"><span data-stu-id="8102a-210">Gets or sets the friendly name for this instance of the process.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-213"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="8102a-213"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span></span></td>
<td><span data-ttu-id="8102a-214">Obtient ou définit le seuil auquel le cache de la page de base de données commence à supprimer les pages du cache pour libérer de l’espace pour les pages qui ne sont pas mises en cache.</span><span class="sxs-lookup"><span data-stu-id="8102a-214">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="8102a-215">Lorsque le nombre de tampons de page dans le cache descend sous ce seuil, un processus en arrière-plan est démarré pour réapprovisionner ce pool de mémoires tampons disponibles.</span><span class="sxs-lookup"><span data-stu-id="8102a-215">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="8102a-216">Ce seuil est toujours relatif à la taille maximale du cache définie par JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="8102a-216">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="8102a-217">Ce seuil doit également toujours être inférieur au seuil d’arrêt défini par JET_paramStopFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="8102a-217">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="8102a-218">La hauteur de distance du seuil de démarrage détermine le temps de réponse que le cache de page de la base de données doit avoir pour produire des tampons disponibles avant que l’application en ait besoin.</span><span class="sxs-lookup"><span data-stu-id="8102a-218">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="8102a-219">Un seuil de démarrage élevé donnera plus de temps au processus en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8102a-219">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="8102a-220">Toutefois, un seuil de démarrage élevé implique un seuil d’arrêt plus élevé et réduit la taille effective du cache des pages de la base de données.</span><span class="sxs-lookup"><span data-stu-id="8102a-220">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="8102a-223"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="8102a-223"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span></span></td>
<td><span data-ttu-id="8102a-224">Obtient ou définit le seuil auquel le cache de la page de base de données met fin à la suppression des pages du cache pour libérer de l’espace pour les pages qui ne sont pas mises en cache.</span><span class="sxs-lookup"><span data-stu-id="8102a-224">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="8102a-225">Lorsque le nombre de tampons de page dans le cache dépasse ce seuil, le processus en arrière-plan qui a démarré pour réapprovisionner ce pool de mémoires tampons disponibles est arrêté.</span><span class="sxs-lookup"><span data-stu-id="8102a-225">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="8102a-226">Ce seuil est toujours relatif à la taille maximale du cache définie par JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="8102a-226">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="8102a-227">Ce seuil doit également être toujours supérieur au seuil de démarrage défini par JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="8102a-227">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="8102a-228">La distance entre le seuil de démarrage et le seuil d’arrêt affecte l’efficacité avec laquelle les pages de base de données sont vidées par le processus en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8102a-228">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="8102a-229">Un plus grand fossé rendra plus probable l’Association des écritures aux pages voisines.</span><span class="sxs-lookup"><span data-stu-id="8102a-229">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="8102a-230">Toutefois, un seuil d’arrêt élevé réduit la taille effective du cache des pages de la base de données.</span><span class="sxs-lookup"><span data-stu-id="8102a-230">However, a high stop threshold will reduce the effective size of the database page cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8102a-231">Haut</span><span class="sxs-lookup"><span data-stu-id="8102a-231">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="8102a-232">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8102a-232">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8102a-233">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8102a-233">Reference</span></span>

[<span data-ttu-id="8102a-234">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="8102a-234">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="8102a-235">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8102a-235">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
