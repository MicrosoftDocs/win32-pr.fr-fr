---
description: 'En savoir plus sur : fichiers ESE (Extensible Storage Engine)'
title: Fichiers ESE (Extensible Storage Engine)
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523124"
---
# <a name="extensible-storage-engine-files"></a><span data-ttu-id="c27af-103">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="c27af-103">Extensible Storage Engine Files</span></span>


<span data-ttu-id="c27af-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c27af-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-files"></a><span data-ttu-id="c27af-105">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="c27af-105">Extensible Storage Engine Files</span></span>

<span data-ttu-id="c27af-106">Le moteur de stockage extensible utilise les types de fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="c27af-106">The Extensible Storage Engine uses the following types of files:</span></span>

- [<span data-ttu-id="c27af-107">Fichiers du journal des transactions</span><span class="sxs-lookup"><span data-stu-id="c27af-107">Transaction Log Files</span></span>](#transaction-log-files)

- [<span data-ttu-id="c27af-108">Fichiers journaux des transactions temporaires</span><span class="sxs-lookup"><span data-stu-id="c27af-108">Temporary Transaction Log Files</span></span>](#temporary-transaction-log-files)

- [<span data-ttu-id="c27af-109">Fichiers journaux des transactions réservés</span><span class="sxs-lookup"><span data-stu-id="c27af-109">Reserved Transaction Log Files</span></span>](#reserved-transaction-log-files)

- [<span data-ttu-id="c27af-110">Fichiers de point de contrôle</span><span class="sxs-lookup"><span data-stu-id="c27af-110">Checkpoint Files</span></span>](#checkpoint-files)

- [<span data-ttu-id="c27af-111">Fichiers de base de données</span><span class="sxs-lookup"><span data-stu-id="c27af-111">Database Files</span></span>](#database-files)

- [<span data-ttu-id="c27af-112">Bases de données temporaires</span><span class="sxs-lookup"><span data-stu-id="c27af-112">Temporary Databases</span></span>](#temporary-databases)

- [<span data-ttu-id="c27af-113">Vider les fichiers de mappage</span><span class="sxs-lookup"><span data-stu-id="c27af-113">Flush Map Files</span></span>](#flush-map-files)

<span data-ttu-id="c27af-114">Ce tableau contient une vue d’ensemble des noms de fichiers de données qui sont gérés par ESE.</span><span class="sxs-lookup"><span data-stu-id="c27af-114">This table contains an overview of the data file names that are managed by ESE.</span></span> <span data-ttu-id="c27af-115">Pour Windows Vista et versions ultérieures, le paramètre JET_paramLegacyNames a un impact sur les noms de fichiers utilisés.</span><span class="sxs-lookup"><span data-stu-id="c27af-115">For Windows Vista and later, the JET_paramLegacyNames setting impacts the file names that are used.</span></span>

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p><span data-ttu-id="c27af-116">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="c27af-116">Operating System</span></span></p>
    </th>
    <th>
      <p><span data-ttu-id="c27af-117">Windows Server 2003 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="c27af-117">Windows Server 2003 and earlier</span></span><br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p><span data-ttu-id="c27af-118">Windows Vista et versions ultérieures (client)</span><span class="sxs-lookup"><span data-stu-id="c27af-118">Windows Vista and later (client)</span></span> <br />
<span data-ttu-id="c27af-119">Windows Server 2008 et versions ultérieures (serveur)</span><span class="sxs-lookup"><span data-stu-id="c27af-119">Windows Server 2008 and later (server)</span></span>
</p>
    </th>
    <th>
      <p><span data-ttu-id="c27af-120">Mise à jour anniversaire Windows 10 et versions ultérieures (client)</span><span class="sxs-lookup"><span data-stu-id="c27af-120">Windows 10 Anniversary Update and later (client)</span></span> <br />
<span data-ttu-id="c27af-121">Windows Server 2016 et versions ultérieures (serveur)</span><span class="sxs-lookup"><span data-stu-id="c27af-121">Windows Server 2016 and later (server)</span></span>
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="c27af-122">
        <strong>Paramètre JET_paramLegacyNames</strong>
      </span><span class="sxs-lookup"><span data-stu-id="c27af-122">
        <strong>JET_paramLegacyNames setting</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-123">
        <strong>NON APPLICABLE</strong>
      </span><span class="sxs-lookup"><span data-stu-id="c27af-123">
        <strong>N/A</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-124">
        <strong>Aucun</strong>
      </span><span class="sxs-lookup"><span data-stu-id="c27af-124">
        <strong>None</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-125">
        <strong>JET_bitESE98FileNames</strong>
      </span><span class="sxs-lookup"><span data-stu-id="c27af-125">
        <strong>JET_bitESE98FileNames</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-126">
        <strong>Identique à Windows Vista/Server 2008</strong>
      </span><span class="sxs-lookup"><span data-stu-id="c27af-126">
        <strong>Same as Windows Vista/Server 2008</strong>
      </span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="c27af-127">Journal actuel</span><span class="sxs-lookup"><span data-stu-id="c27af-127">Current Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-128">&lt;inst &gt; . log</span><span class="sxs-lookup"><span data-stu-id="c27af-128">&lt;inst&gt;.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-129">&lt;inst &gt; . JTX</span><span class="sxs-lookup"><span data-stu-id="c27af-129">&lt;inst&gt;.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-130">&lt;inst &gt; . log</span><span class="sxs-lookup"><span data-stu-id="c27af-130">&lt;inst&gt;.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="c27af-131">Journal de pré-initialisation</span><span class="sxs-lookup"><span data-stu-id="c27af-131">Pre-Init Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-132">&lt;inst &gt; tmp. log</span><span class="sxs-lookup"><span data-stu-id="c27af-132">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-133">&lt;inst &gt; tmp. JTX</span><span class="sxs-lookup"><span data-stu-id="c27af-133">&lt;inst&gt;tmp.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-134">&lt;inst &gt; tmp. log</span><span class="sxs-lookup"><span data-stu-id="c27af-134">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="c27af-135">Journaux pivotés</span><span class="sxs-lookup"><span data-stu-id="c27af-135">Rotated Logs</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-136">&lt;inst &gt; xxxxx. log</span><span class="sxs-lookup"><span data-stu-id="c27af-136">&lt;inst&gt;XXXXX.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-137">&lt;inst &gt; xxxxx. JTX après fffff basculer vers &lt; inst &gt; xxxxxxxx. JTX</span><span class="sxs-lookup"><span data-stu-id="c27af-137">&lt;inst&gt;XXXXX.jtx after FFFFF switch to &lt;inst&gt;XXXXXXXX.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-138">&lt;inst &gt; xxxxx. log après fffff basculer vers &lt; inst &gt; xxxxxxxx. log.</span><span class="sxs-lookup"><span data-stu-id="c27af-138">&lt;inst&gt;XXXXX.log after FFFFF switch to &lt;inst&gt;XXXXXXXX.log.</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="c27af-139">
        <a href="gg294069(v=exchg.10).md">Fichiers de point de contrôle</a>
      </span><span class="sxs-lookup"><span data-stu-id="c27af-139">
        <a href="gg294069(v=exchg.10).md">Checkpoint Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-140">&lt;inst &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="c27af-140">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-141">&lt;inst &gt; . JCP</span><span class="sxs-lookup"><span data-stu-id="c27af-141">&lt;inst&gt;.jcp</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-142">&lt;inst &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="c27af-142">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="c27af-143">
        <a href="gg294069(v=exchg.10).md">Bases de données temporaires</a>
      </span><span class="sxs-lookup"><span data-stu-id="c27af-143">
        <a href="gg294069(v=exchg.10).md">Temporary Databases</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-144">&lt;nom de fichier de base de fichiers Temp &gt; par défaut : tmp. edb</span><span class="sxs-lookup"><span data-stu-id="c27af-144">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-145">&lt;nom de fichier de base de fichiers Temp &gt; par défaut : tmp. edb</span><span class="sxs-lookup"><span data-stu-id="c27af-145">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-146">&lt;nom de fichier de base de fichiers Temp &gt; par défaut : tmp. edb</span><span class="sxs-lookup"><span data-stu-id="c27af-146">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="c27af-147">
        <a href="gg294069(v=exchg.10).md">Fichiers journaux des transactions réservés</a>
      </span><span class="sxs-lookup"><span data-stu-id="c27af-147">
        <a href="gg294069(v=exchg.10).md">Reserved Transaction Log Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-148">Res1. log &amp; res2. log</span><span class="sxs-lookup"><span data-stu-id="c27af-148">res1.log &amp; res2.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-149">&lt;inst &gt; RESXXXXX. jrs</span><span class="sxs-lookup"><span data-stu-id="c27af-149">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
    <td colspan="2">
      <p><span data-ttu-id="c27af-150">&lt;inst &gt; RESXXXXX. jrs</span><span class="sxs-lookup"><span data-stu-id="c27af-150">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="c27af-151">
        <a href="gg294069(v=exchg.10).md">Fichiers de base de données</a>
      </span><span class="sxs-lookup"><span data-stu-id="c27af-151">
        <a href="gg294069(v=exchg.10).md">Database Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-152">&lt;nom du fichier de base de fichiers&gt;</span><span class="sxs-lookup"><span data-stu-id="c27af-152">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-153">&lt;nom du fichier de base de fichiers&gt;</span><span class="sxs-lookup"><span data-stu-id="c27af-153">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-154">&lt;nom du fichier de base de fichiers&gt;</span><span class="sxs-lookup"><span data-stu-id="c27af-154">&lt;db file name&gt;</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="c27af-155">
        <a href="gg294069(v=exchg.10).md">Vider les fichiers de mappage</a>
      </span><span class="sxs-lookup"><span data-stu-id="c27af-155">
        <a href="gg294069(v=exchg.10).md">Flush Map Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-156">N/A</span><span class="sxs-lookup"><span data-stu-id="c27af-156">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-157">N/A</span><span class="sxs-lookup"><span data-stu-id="c27af-157">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-158">N/A</span><span class="sxs-lookup"><span data-stu-id="c27af-158">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="c27af-159">&lt;nom du fichier de base de fichiers sans extension &gt; . jfm</span><span class="sxs-lookup"><span data-stu-id="c27af-159">&lt;db file name without extension&gt;.jfm</span></span></p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a><span data-ttu-id="c27af-160">Fichiers du journal des transactions</span><span class="sxs-lookup"><span data-stu-id="c27af-160">Transaction Log Files</span></span>

<span data-ttu-id="c27af-161">Les fichiers journaux des transactions contiennent des opérations sur les fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-161">Transaction log files contain operations on database files.</span></span> <span data-ttu-id="c27af-162">Ils contiennent suffisamment d’informations pour amener une base de données à un État logiquement cohérent après un arrêt inattendu du processus ou un arrêt du système.</span><span class="sxs-lookup"><span data-stu-id="c27af-162">They contain enough information to bring a database to a logically consistent state after an unexpected process termination or system shutdown.</span></span>

<span data-ttu-id="c27af-163">Les noms des fichiers journaux sont dépendants d’un nom de base à trois lettres, qui peut être défini avec [JET_paramBaseName](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c27af-163">The names of the log files are dependent on a three-letter base name, which can be set with [JET_paramBaseName](./transaction-log-parameters.md).</span></span> <span data-ttu-id="c27af-164">Les exemples ci-dessous utilisent le nom de base « edb », car il s’agit du nom de base par défaut.</span><span class="sxs-lookup"><span data-stu-id="c27af-164">The examples below use a base name of "edb", because that is the default base name.</span></span> <span data-ttu-id="c27af-165">L’extension pour les fichiers journaux des transactions est. log ou. JTX selon que la JET_bitESE98FileNames est définie dans le paramètre JET_paramLegacyFileNames.</span><span class="sxs-lookup"><span data-stu-id="c27af-165">The extension for the transaction log files will be either .log or .jtx depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter.</span></span> <span data-ttu-id="c27af-166">Pour plus d’informations, consultez [paramètres système du moteur de stockage extensible](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c27af-166">For more information, see [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="c27af-167">Les fichiers journaux des transactions sont nommés \<base\> \<generation-number\> . log, en commençant par 1.</span><span class="sxs-lookup"><span data-stu-id="c27af-167">Transaction log files are named \<base\>\<generation-number\>.log, beginning with 1.</span></span> <span data-ttu-id="c27af-168">Le numéro de génération de journal est au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="c27af-168">The log generation number is in hexadecimal format.</span></span> <span data-ttu-id="c27af-169">Par exemple, edb00001. log est le premier journal et edb000ff. log est le journal 255th.</span><span class="sxs-lookup"><span data-stu-id="c27af-169">For example, edb00001.log is the first log, and edb000ff.log is the 255th log.</span></span> <span data-ttu-id="c27af-170">Les fichiers journaux comportent cinq chiffres hexadécimaux dans le nom du fichier journal, jusqu’à ce que le fichier journal 1048576th, à partir duquel les fichiers journaux commencent à être nommés dans un format 11,3 (par exemple, edb00100000. log).</span><span class="sxs-lookup"><span data-stu-id="c27af-170">The log files have five hexadecimal digits in the log file name, until the 1048576th log file, at which point the log files start being named in an 11.3 format (for example, edb00100000.log).</span></span> <span data-ttu-id="c27af-171">\<base\>. log est toujours le fichier journal en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c27af-171">\<base\>.log is always the log file that is currently being used.</span></span> <span data-ttu-id="c27af-172">Si le moteur de base de données n’est pas actif, la génération du fichier Edb. log peut être identifiée à l’aide de la commande suivante : **esentutl.exe-ml edb. log**.</span><span class="sxs-lookup"><span data-stu-id="c27af-172">If the database engine is not active, the generation of edb.log can be identified using the following command: **esentutl.exe -ml edb.log**.</span></span>

<span data-ttu-id="c27af-173">Bien que les fichiers journaux des transactions aient le. L’extension de journal est couramment associée à des fichiers texte, les fichiers journaux de transactions sont au format binaire et ne doivent jamais être modifiés par un utilisateur. Les opérations de base de données sont écrites en premier dans le journal.</span><span class="sxs-lookup"><span data-stu-id="c27af-173">Although transaction log files have the .LOG extension commonly associated with text files, transaction log files are in a binary format and should never be edited by a user.Database operations are written to the log first.</span></span> <span data-ttu-id="c27af-174">Les données peuvent être écrites dans le fichier de base de données ultérieurement ; peut-être immédiatement, potentiellement plus tard.</span><span class="sxs-lookup"><span data-stu-id="c27af-174">The data can be written to the database file later; possibly immediately, potentially much later.</span></span> <span data-ttu-id="c27af-175">En cas de processus inattendu ou d’arrêt du système, les opérations sont toujours présentes dans les fichiers journaux, et les transactions incomplètes peuvent être annulées.</span><span class="sxs-lookup"><span data-stu-id="c27af-175">In the event of unexpected process or system termination, the operations are still present in the log files, and incomplete transactions can be rolled back.</span></span> <span data-ttu-id="c27af-176">La relecture des fichiers journaux de transactions est appelée *récupération conditionnelle* et est effectuée automatiquement quand [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="c27af-176">The act of replaying transaction log files is called *soft recovery*, and it is done automatically when [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md) is called.</span></span> <span data-ttu-id="c27af-177">La récupération logicielle peut également être effectuée manuellement avec l’option « -r » du programme Esentutl.exe.</span><span class="sxs-lookup"><span data-stu-id="c27af-177">Soft recovery can also be performed manually with the "-r" option of the Esentutl.exe program.</span></span> <span data-ttu-id="c27af-178">La relecture des fichiers journaux des transactions sur une base de données restaurée à partir d’une sauvegarde est appelée *récupération matérielle*.</span><span class="sxs-lookup"><span data-stu-id="c27af-178">The act of replaying transaction log files on a database that is restored from a backup is called *hard recovery*.</span></span>

<span data-ttu-id="c27af-179">Les fichiers journaux ont une taille fixe et peuvent être personnalisés avec [JET_paramLogFileSize](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c27af-179">Log files are of a fixed size, customizable with [JET_paramLogFileSize](./transaction-log-parameters.md).</span></span> <span data-ttu-id="c27af-180">Lorsque le fichier journal actuel (c’est-à-dire edb. log) est rempli, il est renommé en \<base\> \<generation-number\> . log et un nouveau fichier journal des transactions est nécessaire dans le flux du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="c27af-180">When the current log file (that is, edb.log) gets filled, it gets renamed to \<base\>\<generation-number\>.log, and a new transaction log file is needed in the transaction log stream.</span></span>

<span data-ttu-id="c27af-181">Chaque instance de base de données est associée à une seule séquence de fichier journal.</span><span class="sxs-lookup"><span data-stu-id="c27af-181">Each database instance has a single log file sequence associated with it.</span></span> <span data-ttu-id="c27af-182">Windows XP a introduit [JetCreateInstance](./jetcreateinstance-function.md), ce qui permet à plusieurs séquences de fichiers du journal des transactions d’être utilisées par un processus unique.</span><span class="sxs-lookup"><span data-stu-id="c27af-182">Windows XP introduced [JetCreateInstance](./jetcreateinstance-function.md), allowing multiple transaction log file sequences to be used by a single process.</span></span> <span data-ttu-id="c27af-183">Toutefois, plusieurs séquences de fichiers du journal des transactions ne peuvent pas exister dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="c27af-183">Multiple transaction log file sequences cannot exist in the same directory, however.</span></span>

<span data-ttu-id="c27af-184">Les fichiers du journal des transactions ne doivent jamais être manipulés manuellement, renommés, déplacés ou supprimés, car l’altération des données peut en résulter.</span><span class="sxs-lookup"><span data-stu-id="c27af-184">Transaction log files should almost never be manually manipulated, renamed, moved, or deleted because data corruption can result.</span></span>

<span data-ttu-id="c27af-185">Les fichiers journaux des transactions seront supprimés par le moteur de base de données lors d’une sauvegarde complète (consultez [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)) ou pendant des opérations normales, si l’enregistrement circulaire est activé.</span><span class="sxs-lookup"><span data-stu-id="c27af-185">Transaction log files will be deleted by the database engine during a full backup (see [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)), or during normal operations, if circular logging is enabled.</span></span>

<span data-ttu-id="c27af-186">Une fois qu’un fichier journal de transactions est plein, le moteur de base de données doit créer un nouveau fichier journal.</span><span class="sxs-lookup"><span data-stu-id="c27af-186">After a transaction log file is filled up, the database engine needs to create a new log file.</span></span> <span data-ttu-id="c27af-187">La journalisation circulaire est un moyen par lequel les fichiers journaux peuvent être automatiquement nettoyés par le moteur de base de données lorsqu’ils ne sont plus nécessaires pour la récupération après incident.</span><span class="sxs-lookup"><span data-stu-id="c27af-187">Circular logging is a means by which log files can be automatically cleaned up by the database engine when they are no longer required for crash recovery.</span></span> <span data-ttu-id="c27af-188">Ce processus est une alternative à la suppression des fichiers journaux en tant que produit par le biais d’une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="c27af-188">This process is an alternative to removing log files as a by-product of performing a backup.</span></span> <span data-ttu-id="c27af-189">La journalisation circulaire peut être contrôlée à l’aide du paramètre système [JET_paramCircularLog](./transaction-log-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="c27af-189">Circular logging can be controlled with the [JET_paramCircularLog](./transaction-log-parameters.md) system parameter.</span></span> <span data-ttu-id="c27af-190">Les fichiers journaux des transactions ne doivent pas être supprimés à l’aide d’une autre méthode.</span><span class="sxs-lookup"><span data-stu-id="c27af-190">Transaction log files should not be deleted using any other method.</span></span>

### <a name="temporary-transaction-log-files"></a><span data-ttu-id="c27af-191">Fichiers journaux des transactions temporaires</span><span class="sxs-lookup"><span data-stu-id="c27af-191">Temporary Transaction Log Files</span></span>

<span data-ttu-id="c27af-192">Lorsque edb. log se remplit, ESE doit créer un nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="c27af-192">When edb.log fills up, ESE needs to create a new file.</span></span> <span data-ttu-id="c27af-193">Le nouveau fichier de transaction de journal est connu sous le nom de fichier journal temporaire des transactions, avant son utilisation par ESE.</span><span class="sxs-lookup"><span data-stu-id="c27af-193">The new log transaction file is known as a temporary transaction log file prior to its use by ESE.</span></span>

<span data-ttu-id="c27af-194">Lorsqu’un nouveau fichier journal est créé et sa taille étendue, il s’appelle \<base\> tmp. log.</span><span class="sxs-lookup"><span data-stu-id="c27af-194">While a new log file is created and its size extended, it will be called \<base\>tmp.log.</span></span> <span data-ttu-id="c27af-195">La création d’un nouveau fichier peut être une opération potentiellement coûteuse, de sorte que le moteur ESE crée le prochain fichier journal de manière proactive en tant que tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c27af-195">Creating a new file can be a potentially costly operation, so ESE will create the next log file proactively as a background task.</span></span>

<span data-ttu-id="c27af-196">Étant donné que le fichier journal temporaire des transactions est créé en prévision de la nécessité d’un nouveau fichier journal des transactions, il ne contient aucune information utile.</span><span class="sxs-lookup"><span data-stu-id="c27af-196">Because the temporary transaction log file is created in anticipation of need for a new transaction log file, it does not contain any useful information.</span></span>

### <a name="reserved-transaction-log-files"></a><span data-ttu-id="c27af-197">Fichiers journaux des transactions réservés</span><span class="sxs-lookup"><span data-stu-id="c27af-197">Reserved Transaction Log Files</span></span>

<span data-ttu-id="c27af-198">Les fichiers journaux de transactions réservés sont créés lorsque le moteur commence à autoriser la journalisation des opérations importantes pour obtenir un arrêt correct.</span><span class="sxs-lookup"><span data-stu-id="c27af-198">The reserved transaction log files are created when the engine starts to allow important operations to be logged to get a clean shutdown.</span></span>

<span data-ttu-id="c27af-199">**Windows Vista :** Dans Windows Vista et versions ultérieures, les fichiers journaux de transactions réservés sont nommés \<base\> RESXXXXX. jrs.</span><span class="sxs-lookup"><span data-stu-id="c27af-199">**Windows Vista:** In Windows Vista and later, the Reserved Transaction Log Files are named \<base\>RESXXXXX.jrs.</span></span>

<span data-ttu-id="c27af-200">**Windows Server 2003 :** Dans Windows Server 2003 et versions antérieures, les fichiers journaux de transactions réservés sont nommés Res1. log et res2. log.</span><span class="sxs-lookup"><span data-stu-id="c27af-200">**Windows Server 2003:** In Windows Server 2003 and earlier, The Reserved Transaction Log Files are named res1.log and res2.log.</span></span>

<span data-ttu-id="c27af-201">Lorsque le moteur de base de données ne dispose plus de suffisamment d’espace disque, il ne peut pas créer de nouveau fichier journal.</span><span class="sxs-lookup"><span data-stu-id="c27af-201">When the database engine runs out of disk space it cannot create a new log file.</span></span> <span data-ttu-id="c27af-202">La chose la plus sûre consiste à arrêter correctement, mais certaines opérations (telles que les opérations de restauration) doivent toujours être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="c27af-202">The safest thing to do is to shut down cleanly, but some operations (such as rollback operations) must still be logged.</span></span> <span data-ttu-id="c27af-203">La plupart des opérations de base de données échoueront au cours de cette phase.</span><span class="sxs-lookup"><span data-stu-id="c27af-203">Most database operations will fail during this stage.</span></span>

<span data-ttu-id="c27af-204">Étant donné que les fichiers journaux de transactions réservés sont créés en prévision des besoins en matière de fichiers journaux de transactions dans un scénario hors disque, ils ne contiennent pas d’informations utiles.</span><span class="sxs-lookup"><span data-stu-id="c27af-204">Because the reserved transaction log files are created in anticipation of need for transaction log files in an out-of-disk scenario, they do not contain any useful information.</span></span>

### <a name="checkpoint-files"></a><span data-ttu-id="c27af-205">fichiers de point de contrôle</span><span class="sxs-lookup"><span data-stu-id="c27af-205">Checkpoint Files</span></span>

<span data-ttu-id="c27af-206">Le fichier de point de contrôle stocke le point de contrôle pour une séquence particulière de fichier journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="c27af-206">The checkpoint file stores the checkpoint for a particular transaction log file sequence.</span></span> <span data-ttu-id="c27af-207">Le fichier de point de contrôle se nomme \<base\> . chk ou \<base\> . JCP, selon que la JET_bitESE98FileNames est définie dans le paramètre JET_paramLegacyFileNames, et que son emplacement est donné par [JET_paramSystemPath](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c27af-207">The checkpoint file is named \<base\>.chk or \<base\>.jcp, depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter, and its location is given by [JET_paramSystemPath](./transaction-log-parameters.md).</span></span>

<span data-ttu-id="c27af-208">Les opérations de base de données sont d’abord écrites dans les fichiers journaux, puis mises en cache en mémoire.</span><span class="sxs-lookup"><span data-stu-id="c27af-208">Database operations are first written to the log files and then cached in memory.</span></span> <span data-ttu-id="c27af-209">À un moment ultérieur, les opérations sont écrites dans le fichier de base de données, mais pour des raisons de performances, l’ordre dans lequel les opérations sont écrites dans le fichier de base de données peut ne pas correspondre à l’ordre dans lequel elles ont été journalisées à l’origine.</span><span class="sxs-lookup"><span data-stu-id="c27af-209">At some later point, the operations get written to the database file, but for performance reasons, the order in which operations are written to the database file might not match the order in which they were originally logged.</span></span> <span data-ttu-id="c27af-210">Les opérations écrites dans le fichier journal des transactions sont dans l’un des deux États suivants :</span><span class="sxs-lookup"><span data-stu-id="c27af-210">Operations written to the transaction log file will be in one of two states:</span></span>

  - <span data-ttu-id="c27af-211">Écrit dans le fichier journal des transactions et dans le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-211">Written to the transaction log file and the database file.</span></span>

  - <span data-ttu-id="c27af-212">Écrit dans le fichier journal des transactions et n’est pas encore écrit dans le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-212">Written to the transaction log file and not yet written to the database file.</span></span>

<span data-ttu-id="c27af-213">De nombreuses opérations de base de données peuvent être stockées dans un seul fichier journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="c27af-213">Many database operations can be stored in a single transaction log file.</span></span> <span data-ttu-id="c27af-214">Un fichier journal donné peut comporter les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c27af-214">A given log file can consist of the following items:</span></span>

  - <span data-ttu-id="c27af-215">Toutes les opérations écrites dans le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-215">All operations written to the database file.</span></span>

  - <span data-ttu-id="c27af-216">Aucune opération n’est écrite dans le fichier de base de données</span><span class="sxs-lookup"><span data-stu-id="c27af-216">No operations written to the database file</span></span>

  - <span data-ttu-id="c27af-217">Une combinaison d’opérations écrites dans le fichier de base de données et les opérations qui n’ont pas encore été écrites dans le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-217">A mix of operations written to the database file and operations not yet written to the database file.</span></span>

<span data-ttu-id="c27af-218">Le point de contrôle fait référence au point dans le temps dans le flux du journal des transactions où toutes les opérations antérieures au point de contrôle ont été écrites dans le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-218">The checkpoint refers to the point in time in the transaction log stream where all operations prior to the checkpoint have been written to the database file.</span></span> <span data-ttu-id="c27af-219">Il n’existe aucune garantie quant aux opérations qui se produisent après le point de contrôle ; certains peuvent être en mémoire et d’autres peuvent être écrits dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-219">There is no guarantee about the operations that occur after the checkpoint; some might be in memory, and some might be written to the database.</span></span>

<span data-ttu-id="c27af-220">Étant donné que toutes les opérations dans les fichiers journaux avant le point de contrôle sont représentées dans le fichier de base de données, seuls les fichiers journaux des transactions situés après le point de contrôle sont nécessaires à la récupération logicielle afin d’amener une base de données particulière dans un état propre.</span><span class="sxs-lookup"><span data-stu-id="c27af-220">Since all the operations in the log files prior to the checkpoint are represented in the database file, only the transaction log files after the checkpoint are needed for soft recovery to bring a particular database into a clean state.</span></span>

### <a name="database-files"></a><span data-ttu-id="c27af-221">Fichiers de base de données</span><span class="sxs-lookup"><span data-stu-id="c27af-221">Database Files</span></span>

<span data-ttu-id="c27af-222">Le fichier de base de données contient le schéma de toutes les tables de la base de données, les enregistrements de toutes les tables de la base de données et les index sur les tables.</span><span class="sxs-lookup"><span data-stu-id="c27af-222">The database file contains the schema for all of the tables in the database, the records for all of the tables in the database, and the indexes over the tables.</span></span> <span data-ttu-id="c27af-223">Son emplacement est fourni à l’aide de [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md)ou [JetAttachDatabase2](./jetattachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="c27af-223">Its location is given using [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md), or [JetAttachDatabase2](./jetattachdatabase2-function.md).</span></span>

<span data-ttu-id="c27af-224">Une base de données est arrêtée proprement uniquement après un appel réussi à [JetTerm](./jetterm-function.md) ou [JetTerm2](./jetterm2-function.md).</span><span class="sxs-lookup"><span data-stu-id="c27af-224">A database is cleanly shut down only after a successful call to [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="c27af-225">Le programme Esentutl.exe peut détecter si une base de données est arrêtée proprement avec l’option « -MH ».</span><span class="sxs-lookup"><span data-stu-id="c27af-225">The Esentutl.exe program can detect whether a database is shut down cleanly with the "-mh" option.</span></span> <span data-ttu-id="c27af-226">Par exemple, « esentutl.exe-MH Sample. edb » lira l’en-tête de base de données d’une base de données nommée Sample. edb et imprime l’état de Sample. edb.</span><span class="sxs-lookup"><span data-stu-id="c27af-226">For example, "esentutl.exe -mh sample.edb" will read the database header of a database named sample.edb, and print out the state of sample.edb.</span></span> <span data-ttu-id="c27af-227">Il peut imprimer « État : arrêt correct » ou « État : arrêt intempestif ».</span><span class="sxs-lookup"><span data-stu-id="c27af-227">It may print out "State: Clean Shutdown" or "State: Dirty Shutdown".</span></span>

<span data-ttu-id="c27af-228">Une base de données qui n’a pas été correctement arrêtée est dans un état d’arrêt intempestif.</span><span class="sxs-lookup"><span data-stu-id="c27af-228">A database that has not been cleanly shut down is in a dirty shutdown state.</span></span> <span data-ttu-id="c27af-229">Avant Windows XP, cet État était appelé *incohérent*.</span><span class="sxs-lookup"><span data-stu-id="c27af-229">Prior to Windows XP, this state was called *inconsistent*.</span></span> <span data-ttu-id="c27af-230">Une base de données incorrecte (incohérente) peut être placée dans un état propre avec la récupération logicielle.</span><span class="sxs-lookup"><span data-stu-id="c27af-230">A dirty (inconsistent) database can be brought to a clean state with soft recovery.</span></span> <span data-ttu-id="c27af-231">Une base de données endommagée n’est pas la même chose qu’une base de données modifiée (« incohérente »).</span><span class="sxs-lookup"><span data-stu-id="c27af-231">A corrupt database is not the same as a dirty ("inconsistent") database.</span></span>

<span data-ttu-id="c27af-232">Une base de données endommagée fait référence à une altération physique ou logique, et ne peut pas être corrigée avec la récupération logicielle.</span><span class="sxs-lookup"><span data-stu-id="c27af-232">A corrupt database refers to a physical or logical corruption, and cannot be fixed with soft recovery.</span></span> <span data-ttu-id="c27af-233">Les altérations physiques peuvent être des retournements de bits, qui sont souvent détectés par les sommes de contrôle sur les pages de la base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-233">Physical corruptions can be bit flips, which will frequently be caught by the checksums on the database pages.</span></span> <span data-ttu-id="c27af-234">Un checksum en échec dans un fichier de base de données se manifeste comme une erreur de JET_errReadVerifyFailure.</span><span class="sxs-lookup"><span data-stu-id="c27af-234">A failed checksum in a database file manifests itself as a JET_errReadVerifyFailure error.</span></span>

<span data-ttu-id="c27af-235">Seules les bases de données correctement arrêtées peuvent être déplacées ou renommées en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="c27af-235">Only cleanly shut down databases can be safely moved around or renamed.</span></span> <span data-ttu-id="c27af-236">Si une base de données n’a pas été arrêtée proprement, elle ne peut pas être déplacée ou renommée automatiquement en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="c27af-236">If a database was not cleanly shut down, it cannot be automatically safely moved or renamed.</span></span>

<span data-ttu-id="c27af-237">Plusieurs bases de données peuvent être associées à une seule séquence de fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="c27af-237">Multiple databases can be associated with a single transaction log file sequence.</span></span>

### <a name="temporary-databases"></a><span data-ttu-id="c27af-238">Bases de données temporaires</span><span class="sxs-lookup"><span data-stu-id="c27af-238">Temporary Databases</span></span>

<span data-ttu-id="c27af-239">La base de données temporaire est utilisée comme magasin de stockage pour temptables et elle est également utilisée lors de la création d’index.</span><span class="sxs-lookup"><span data-stu-id="c27af-239">The temporary database is used as a backing store for temptables and it is also used when creating indices.</span></span>

<span data-ttu-id="c27af-240">Le nom et l’emplacement sont configurés avec [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c27af-240">The name and location is configured with [JET_paramTempPath](./temporary-database-parameters.md).</span></span>

<span data-ttu-id="c27af-241">Les Temptables sont créés avec [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="c27af-241">Temptables are created with [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span> <span data-ttu-id="c27af-242">Elles sont également créées par certains appels d’API et utilisées pour retourner les informations de schéma (par exemple, [JetGetIndexInfo](./jetgetindexinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="c27af-242">They are also created by some API calls and used to return schema information (such as [JetGetIndexInfo](./jetgetindexinfo-function.md)).</span></span>

## <a name="flush-map-files"></a><span data-ttu-id="c27af-243">Vider les fichiers de mappage</span><span class="sxs-lookup"><span data-stu-id="c27af-243">Flush Map Files</span></span>

<span data-ttu-id="c27af-244">À partir de la mise à jour anniversaire Windows 10 (client) et de Windows Server 2016 (serveur), ESE a ajouté un niveau supplémentaire de protection contre les écritures perdues (ou les vidages perdus) 1, ce qui lui permet de détecter de tels événements interprocessus initialization2.</span><span class="sxs-lookup"><span data-stu-id="c27af-244">Starting with the Windows 10 Anniversary Update (client) and Windows Server 2016 (server), ESE added an additional level of protection against lost writes (or lost flushes) 1, allowing it to detect such events cross-process re-initialization2.</span></span> <span data-ttu-id="c27af-245">Cette fonctionnalité requiert la conservation des métadonnées dans un fichier distinct appelé « vidage du mappage ».</span><span class="sxs-lookup"><span data-stu-id="c27af-245">This feature requires persisting metadata to a separate file called a "flush map" file.</span></span>

<span data-ttu-id="c27af-246">Un fichier de mappage de vidage est créé pour chaque fichier de base de données et se trouve dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="c27af-246">One flush map file is created for each database file, and is located in the same directory.</span></span> <span data-ttu-id="c27af-247">Le fichier est nommé de la même façon que le fichier de base de données, mais avec une extension différente.</span><span class="sxs-lookup"><span data-stu-id="c27af-247">The file is named similarly to the database file, but with a different extension.</span></span> <span data-ttu-id="c27af-248">Par exemple, si l’application cliente crée une base de données avec le chemin d’accès complet C : \\ mydirectory \\ MyDabatase. edb, son fichier de mappage de vidage correspondant est c : \\ mydirectory \\ MyDabatase. jfm.</span><span class="sxs-lookup"><span data-stu-id="c27af-248">For example, if the client application creates a database with the full path C:\\MyDirectory\\MyDabatase.edb, its corresponding flush map file is C:\\MyDirectory\\MyDabatase.jfm.</span></span>

<span data-ttu-id="c27af-249">Cette amélioration introduit deux conditions requises pour le nom des fichiers de base de données :</span><span class="sxs-lookup"><span data-stu-id="c27af-249">This enhancement introduces two requirements for how database files must be named:</span></span>

  - <span data-ttu-id="c27af-250">Deux bases de données dans le même répertoire ne doivent pas avoir le même nom de fichier avec des extensions différentes.</span><span class="sxs-lookup"><span data-stu-id="c27af-250">Two databases in the same directory must not have the same filename with different extensions.</span></span> <span data-ttu-id="c27af-251">Par exemple : C : \\ mydirectory \\ MyDabatase. DB1 et c : \\ mydirectory \\ MyDabatase. DB2.</span><span class="sxs-lookup"><span data-stu-id="c27af-251">For example: C:\\MyDirectory\\MyDabatase.db1 and C:\\MyDirectory\\MyDabatase.db2.</span></span>

  - <span data-ttu-id="c27af-252">2 \.</span><span class="sxs-lookup"><span data-stu-id="c27af-252">2\.</span></span> <span data-ttu-id="c27af-253">Une base de données ne doit pas avoir une extension. jfm.</span><span class="sxs-lookup"><span data-stu-id="c27af-253">A database must not have a .jfm extension.</span></span>

<span data-ttu-id="c27af-254">Lorsque vous copiez ou déplacez manuellement un fichier de base de données, le fichier de mappage de vidage correspondant doit également être copié ou déplacé vers le même répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="c27af-254">When you manually copy or move a database file, its corresponding flush map file should also be, respectively, copied or moved to the same destination directory.</span></span> <span data-ttu-id="c27af-255">Si un fichier de mappage de vidage n’est pas présent au moment d’une nouvelle pièce jointe de base de données (par le biais de [JetAttachDatabase](./jetattachdatabase-function.md), un nouveau fichier est créé et rempli à la demande à mesure que des pages sont lues à partir de la base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-255">If a flush map file is not present at the time of a new database attachment (via [JetAttachDatabase](./jetattachdatabase-function.md), a new one will be created and re-populated on-demand as pages are read in from the database.</span></span> <span data-ttu-id="c27af-256">La combinaison d’une base de données incompatible et de fichiers de mappage de vidage est gérée par ESE et force la suppression et la recréation de la carte de vidage incompatible.</span><span class="sxs-lookup"><span data-stu-id="c27af-256">Mixing mismatching database and flush map files is handled by ESE, and forces the mismatched flush map to be deleted and re-created from scratch.</span></span>

<span data-ttu-id="c27af-257">La taille d’un fichier de mappage de vidage est directement proportionnelle à son fichier de base de données associé et approximativement égale à (toutes les tailles en octets, le résultat doit être arrondi au multiple suivant de 8 192) :</span><span class="sxs-lookup"><span data-stu-id="c27af-257">The size of a flush map file is directly proportional to its associated database file and approximately equal to (all sizes in bytes, result must be rounded up to the next multiple of 8,192):</span></span>

`8,192 + ((<database file size> / <database page size>) / 4)`

<span data-ttu-id="c27af-258">Par exemple : pour une base de données de 1,5 Go utilisant une taille de page de 32 Ko, la taille approximative du mappage de vidage est de 24 576 octets (ou 24KB).</span><span class="sxs-lookup"><span data-stu-id="c27af-258">For example: for a 1.5GB database using a 32KB page size, the approximate size of the flush map is 24,576 bytes (or 24KB).</span></span>

<span data-ttu-id="c27af-259">Le fichier de mappage de vidage doit être actualisé au fur et à mesure que les pages de la base de données sont vidées.</span><span class="sxs-lookup"><span data-stu-id="c27af-259">The flush map file needs to be refreshed as database pages are flushed.</span></span> <span data-ttu-id="c27af-260">Si la journalisation transactionnelle est activée (par exemple, [JET_paramRecovery](./transaction-log-parameters.md) définie sur « on », valeur par défaut), l’actualisation du mappage de vidage est effectuée lorsque l’application cliente modifie la base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-260">If transactional logging is enabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "on", the default), refreshing the flush map is performed as the client application makes modifications to the database.</span></span> <span data-ttu-id="c27af-261">En moyenne, l’ensemble du mappage de vidage est écrit sur le support non volatile une fois tous les 20% des [JET_paramCheckpointDepthMax](./database-cache-parameters.md) de la valeur (en octets) des journaux transactionnels générés.</span><span class="sxs-lookup"><span data-stu-id="c27af-261">On average, the entire flush map is written to the non-volatile media once for every 20% of [JET_paramCheckpointDepthMax](./database-cache-parameters.md) -worth (in bytes) of transactional logs generated.</span></span> <span data-ttu-id="c27af-262">Le nombre d’opérations d’écriture dépend de la répartition des modifications dans l’ensemble de la base de données.</span><span class="sxs-lookup"><span data-stu-id="c27af-262">The number of write operations depends on how distributed throughout the database the modifications are.</span></span> <span data-ttu-id="c27af-263">Mais elle est au plus approximative (toutes les tailles en octets) :</span><span class="sxs-lookup"><span data-stu-id="c27af-263">But it is at most, approximately (all sizes in bytes):</span></span>

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

<span data-ttu-id="c27af-264">Si la journalisation transactionnelle est désactivée (par exemple, [JET_paramRecovery](./transaction-log-parameters.md) défini sur « désactivé »), le mappage de vidage est actualisé une seule fois lorsque la base de données est explicitement détachée proprement (via [JetDetachDatabase](./jetdetachdatabase-function.md), ou détaché de manière implicite en mettant fin à l’instance ESE associée (via l’une des fonctions [JetTerm](./jetterm-function.md) , tant que [JET_bitTermDirty](./jetterm2-function.md) n’est pas passé).</span><span class="sxs-lookup"><span data-stu-id="c27af-264">If transactional logging is disabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "off"), the flush map gets refreshed only once when the database is explicitly detached cleanly (via [JetDetachDatabase](./jetdetachdatabase-function.md), or implicitly detached cleanly by terminating its associated ESE instance (via any of the [JetTerm](./jetterm-function.md) functions, as long as [JET_bitTermDirty](./jetterm2-function.md) is not passed).</span></span>

<span data-ttu-id="c27af-265">1 une perte d’écriture (ou un vidage perdu) est définie comme une opération d’écriture qui renvoie correctement depuis le système d’exploitation vers le moteur de base de données ESE, mais les données réelles ne sont jamais conservées dans le fichier de base de données du média non volatile.</span><span class="sxs-lookup"><span data-stu-id="c27af-265">1 A lost write (or lost flush) is defined as a write operation that returns successfully from the operating system to the ESE database engine but the actual data never gets persisted to the database file in the non-volatile media.</span></span> <span data-ttu-id="c27af-266">Cela est généralement dû à une pile de stockage défectueuse ou mal configurée (logiciel ou matériel).</span><span class="sxs-lookup"><span data-stu-id="c27af-266">It is usually caused by a malfunctioning or misconfigured storage stack (software or hardware).</span></span> <span data-ttu-id="c27af-267">Les applications clientes peuvent recevoir une erreur [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) des fonctions ESE qui nécessitent la lecture des données de la base de données si les données se trouvent dans une région qui a subi un événement d’écriture perdu.</span><span class="sxs-lookup"><span data-stu-id="c27af-267">Client applications may receive a [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) error from ESE functions that require reading data from the database if the data is located in a region that underwent a lost write event.</span></span>

<span data-ttu-id="c27af-268">2 la possibilité de détecter les écritures perdues au cours de la durée de vie d’un processus est présente depuis Windows 8 (client) et Windows Server 2012 (serveur).</span><span class="sxs-lookup"><span data-stu-id="c27af-268">2 The ability to detect lost writes within a process's lifetime has been present since Windows 8 (client) and Windows Server 2012 (server).</span></span>
