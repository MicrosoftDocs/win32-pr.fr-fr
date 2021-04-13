---
description: 'En savoir plus sur les éléments suivants : InstanceParameters'
title: Membres InstanceParameters
TOCTitle: InstanceParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_members(v=EXCHG.10)
ms:contentKeyID: 55103286
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8d52035b7473c17f9278a0343d12d957b2970349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555312"
---
# <a name="instanceparameters-members"></a>Membres InstanceParameters

Inclure les membres protégés  
Inclure les membres hérités  

Cette classe fournit des propriétés permettant de définir et d’extraire des paramètres système sur une instance ESENT. Cette classe fournit des propriétés statiques pour définir et récupérer des paramètres système ESENT par instance.

Le type [InstanceParameters](./instanceparameters-class.md) expose les membres suivants.

## <a name="constructors"></a>Constructeurs

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350965(v=exchg.10).md">InstanceParameters</a></td>
<td>Initialise une nouvelle instance de la classe InstanceParameters.</td>
</tr>
</tbody>
</table>


Haut

## <a name="properties"></a>Propriétés

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></td>
<td>Obtient ou définit le chemin d’accès relatif ou absolu du système de fichiers d’un dossier dans lequel la récupération après incident ou une opération de restauration peut trouver les bases de données référencées dans le journal des transactions dans le dossier spécifié.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350972(v=exchg.10).md">BaseName</a></td>
<td>Obtient ou définit le préfixe à trois lettres utilisé pour la plupart des fichiers utilisés par le moteur de base de données. Par exemple, le fichier de point de contrôle est appelé EDB. CHK par défaut, car EDB est le nom de base par défaut.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></td>
<td>Obtient ou définit une valeur donnant le nombre de ressources de l’arborescence B + mises en cache par l’instance après que les tables qu’elles représentent ont été fermées par l’application. Des valeurs élevées pour ce paramètre forcent le moteur de base de données à utiliser plus de mémoire, mais augmentent la vitesse avec laquelle un grand nombre de tables peut être ouvert de façon aléatoire par l’application. Cela est utile pour les applications qui ont un schéma avec un très grand nombre de tables. Pris en charge sur Windows Vista et les autres. Ignoré sur Windows XP et Windows Server 2003.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350974(v=exchg.10).md">CachePriority</a></td>
<td>Obtient ou définit la propriété par instance pour les priorités relatives du cache (par défaut = 100).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></td>
<td>Obtient ou définit le seuil en octets pour le nombre de fichiers journaux des transactions qui doivent être relus après un incident. Si la journalisation circulaire est activée à l’aide de CircularLog, ce paramètre contrôle également la quantité approximative de fichiers du journal des transactions qui seront conservés sur le disque.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350977(v=exchg.10).md">CircularLog</a></td>
<td>Obtient ou définit une valeur indiquant si la journalisation circulaire est activée. Lorsque la journalisation circulaire est désactivée, tous les fichiers journaux des transactions générés sont conservés sur le disque jusqu’à ce qu’ils ne soient plus nécessaires, car une sauvegarde complète de la base de données a été effectuée. Lorsque la journalisation circulaire est activée, seuls les fichiers journaux des transactions qui sont plus récents que le point de contrôle actuel sont conservés sur le disque. L’avantage de ce mode est que les sauvegardes ne sont pas nécessaires pour supprimer les anciens fichiers du journal des transactions.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></td>
<td>Obtient ou définit une valeur indiquant si JetInit échoue lorsque le moteur de base de données est configuré pour démarrer à l’aide des fichiers du journal des transactions sur un disque d’une taille différente de celle configurée. Normalement, <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> récupère les bases de données, mais échoue avec <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> pour indiquer que la taille du fichier journal n’est pas correctement configurée. Toutefois, lorsque ce paramètre est défini sur true, le moteur de base de données supprime silencieusement tous les anciens fichiers journaux, puis démarre un nouvel ensemble de fichiers journaux de transactions à l’aide de la taille de fichier journal configurée. Ce paramètre est utile lorsque l’application souhaite modifier en toute transparence la taille du fichier journal des transactions, tout en continuant à travailler de manière transparente dans les scénarios de mise à niveau et de restauration.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></td>
<td>Obtient ou définit une valeur indiquant si ESENT crée sans assistance des dossiers manquants dans ses chemins d’accès de système de fichiers.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></td>
<td>Obtient ou définit le nombre de pages qui sont ajoutées à un fichier de base de données chaque fois qu’il doit croître pour accueillir davantage de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></td>
<td>Obtient ou définit l’intervalle maximal, en secondes, pour permettre à l’analyse de la base de données de se terminer.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></td>
<td>Obtient ou définit l’intervalle minimal de répétition de l’analyse de la base de données, en secondes.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></td>
<td>Obtient ou définit la limitation de l’analyse de la base de données, en millisecondes.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></td>
<td>Obtient ou définit une valeur indiquant si la maintenance de la base de données doit s’exécuter pendant la récupération.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></td>
<td>Obtient ou définit une valeur indiquant si la sérialisation de la maintenance de la base de données est activée pour les bases de données qui partagent le même disque.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></td>
<td>Obtient ou définit une valeur indiquant si <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> doit vérifier les index qui ont été générés à l’aide d’une version antérieure de la bibliothèque NLS dans le système d’exploitation.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></td>
<td>Obtient ou définit une valeur indiquant si la défragmentation en ligne est activée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350988(v=exchg.10).md">EventSource</a></td>
<td>Obtient ou définit une chaîne spécifique à l’application qui sera ajoutée à tous les messages du journal des événements émis par le moteur de base de données. Cela permet de corréler facilement les messages du journal des événements avec l’application source. Par défaut, le nom de l’exécutable de l’application hôte sera utilisé.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350966(v=exchg.10).md">EventSourceKey</a></td>
<td>Obtient ou définit le nom du journal des événements que le moteur de base de données utilise pour ses messages de journal des événements. Par défaut, tous les messages du journal des événements sont envoyés dans le journal des événements de l’application. Si le nom de la clé de registre d’un autre journal des événements est configuré, les messages du journal des événements y seront à la place.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350968(v=exchg.10).md">LogBuffers</a></td>
<td>Obtient ou définit la quantité de mémoire utilisée pour mettre en cache les enregistrements de journal avant leur écriture dans le fichier journal des transactions. L’unité de ce paramètre correspond à la taille de secteur du volume qui contient les fichiers du journal des transactions. La taille des secteurs étant presque toujours de 512 octets, il est possible de supposer en toute sécurité la taille de l’unité. Ce paramètre a un impact sur les performances. Lorsque le moteur de base de données subit une charge de mise à jour importante, cette mémoire tampon peut être entièrement très rapide. Une plus grande taille de cache pour le fichier journal des transactions est essentielle pour garantir une bonne performance des mises à jour dans une condition de charge élevée. La valeur par défaut est trop petite pour ce cas. Ne définissez pas ce paramètre sur un nombre de mémoires tampons plus grand (en octets) que la moitié de la taille d’un fichier journal de transactions.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350991(v=exchg.10).md">Répertoire</a></td>
<td>Obtient ou définit le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra les journaux des transactions pour l’instance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350969(v=exchg.10).md">LogFileSize</a></td>
<td>Obtient ou définit la taille des fichiers du journal des transactions. Ce paramètre doit être défini en unités de 1024 octets (par exemple, un paramètre de 2048 donne des fichiers journaux de 2 Mo).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350993(v=exchg.10).md">MaxCursors</a></td>
<td>Obtient ou définit le nombre de ressources de curseur réservées pour cette instance. Une ressource de curseur correspond directement à un JET_TABLEID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></td>
<td>Obtient ou définit le nombre de ressources de l’arborescence B + réservées pour cette instance.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350994(v=exchg.10).md">MaxSessions</a></td>
<td>Obtient ou définit le nombre de ressources de sessions réservées pour cette instance. Une ressource de session correspond directement à un JET_SESID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></td>
<td>Obtient ou définit le nombre de ressources de table temporaire à utiliser par une instance. Ce paramètre affecte le nombre de tables temporaires qui peuvent être utilisées en même temps. Si ce paramètre système est défini à zéro, aucune base de données temporaire n’est créée et toute activité nécessitant l’utilisation de la base de données temporaire échoue. Ce paramètre peut être utile pour éviter les e/s nécessaires à la création de la base de données temporaire si elle est connue qu’elle ne sera pas utilisée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></td>
<td>Obtient ou définit le pourcentage de la Banque des versions qui peut être utilisée par la plus ancienne transaction avant <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (valeur par défaut = 100).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350975(v=exchg.10).md">MaxVerPages</a></td>
<td>Obtient ou définit le nombre maximal de pages de la Banque des versions réservées pour cette instance.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></td>
<td>Obtient ou définit une valeur indiquant si les messages du journal des événements d’information qui seraient normalement générés par le moteur de base de données seront supprimés.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></td>
<td>Obtient ou définit une valeur indiquant si une seule base de données peut être ouverte à l’aide de JetOpenDatabase par une session donnée à un moment donné. La base de données temporaire est exclue de cette restriction.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></td>
<td>Obtient ou définit la taille initiale de la base de données temporaire. La taille est dans les pages de base de données. Une taille de zéro indique que la taille par défaut d’une base de données ordinaire doit être utilisée. Il est souvent souhaitable que les petites applications configurent la base de données temporaire aussi petite que possible. La définition de ce paramètre sur <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> permet d’obtenir la plus petite base de données temporaire possible.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></td>
<td>Obtient ou définit le nombre préféré de pages de la Banque des versions réservées pour cette instance. Si la taille de la Banque des versions dépasse ce seuil, toutes les informations qui sont utilisées uniquement pour les tâches en arrière-plan facultatives, telles que la récupération de l’espace supprimé dans la base de données, sont sacrifiées pour conserver de l’espace pour les informations transactionnelles.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></td>
<td>Obtient ou définit le nombre maximal d’opérations d’e/s distribuées pour un usage donné.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350981(v=exchg.10).md">Récupération</a></td>
<td>Obtient ou définit une valeur indiquant si la récupération sur incident est activée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351007(v=exchg.10).md">SystemDirectory</a></td>
<td>Obtient ou définit le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra le fichier de point de contrôle de l’instance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350983(v=exchg.10).md">TempDirectory</a></td>
<td>Obtient ou définit le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra la base de données temporaire de l’instance.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></td>
<td>Obtient ou définit le nombre d’éléments de travail de nettoyage en arrière-plan qui peuvent être mis en file d’attente dans le pool de threads du moteur de base de données à un moment donné.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350985(v=exchg.10).md">WaypointLatency</a></td>
<td>Obtient ou définit le nombre de journaux pour lesquels esent diffère le vidage de base de données. Cela peut être utilisé pour augmenter la capacité de récupération de base de données en cas de perte de fichiers journaux. Pris en charge sur Windows 7 et les autres. Ignoré sur Windows XP, Windows Server 2003, Windows Vista et Windows Server 2008.</td>
</tr>
</tbody>
</table>


Haut

## <a name="methods"></a>Méthodes

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350967(v=exchg.10).md">ToString</a></td>
<td>Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn350942(v=exchg.10).md">InstanceParameters</a>actuel. (Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
