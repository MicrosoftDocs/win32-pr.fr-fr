---
description: 'En savoir plus sur : structure JET_DBINFOMISC4'
title: Structure JET_DBINFOMISC4
TOCTitle: JET_DBINFOMISC4 Structure
ms:assetid: 63f446bc-98b7-4a60-9575-d6b4757fb0fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269269(v=EXCHG.10)
ms:contentKeyID: 32765571
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e2242b1e419c4834a2a1843165e1c9a2ad1f2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517438"
---
# <a name="jet_dbinfomisc4-structure"></a><span data-ttu-id="99f0c-103">Structure JET_DBINFOMISC4</span><span class="sxs-lookup"><span data-stu-id="99f0c-103">JET_DBINFOMISC4 Structure</span></span>


<span data-ttu-id="99f0c-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="99f0c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc4-structure"></a><span data-ttu-id="99f0c-105">Structure JET_DBINFOMISC4</span><span class="sxs-lookup"><span data-stu-id="99f0c-105">JET_DBINFOMISC4 Structure</span></span>

<span data-ttu-id="99f0c-106">La structure **JET_DBINFOMISC4** contient diverses informations sur une base de données.</span><span class="sxs-lookup"><span data-stu-id="99f0c-106">The **JET_DBINFOMISC4** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="99f0c-107">Il s’agit des informations contenues dans l’en-tête de base de données.</span><span class="sxs-lookup"><span data-stu-id="99f0c-107">This is the information that is contained in the database header.</span></span>

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
      JET_BKINFO bkinfoCopyPrev;
      JET_BKINFO bkinfoDiffPrev;
    } JET_DBINFOMISC4;
```

### <a name="members"></a><span data-ttu-id="99f0c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="99f0c-108">Members</span></span>

<span data-ttu-id="99f0c-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="99f0c-109">**ulVersion**</span></span>

<span data-ttu-id="99f0c-110">Version native du moteur de base de données qui a créé la base de données.</span><span class="sxs-lookup"><span data-stu-id="99f0c-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="99f0c-111">Consultez [JetGetVersion](./jetgetversion-function.md) pour récupérer la version native du moteur de base de données actuel.</span><span class="sxs-lookup"><span data-stu-id="99f0c-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="99f0c-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="99f0c-112">**ulUpdate**</span></span>

<span data-ttu-id="99f0c-113">Effectue le suivi des mises à jour incrémentielles du format de base de données qui sont à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="99f0c-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99f0c-114">ulVersion, ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="99f0c-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="99f0c-115">Signification</span><span class="sxs-lookup"><span data-stu-id="99f0c-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="99f0c-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="99f0c-117">Format bêta du système d’exploitation d’origine (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="99f0c-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="99f0c-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="99f0c-119">Ajoutez des colonnes dans le catalogue pour l’indexation conditionnelle et l’ancienne (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="99f0c-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="99f0c-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="99f0c-121">Ajoutez l’indicateur fLocalizedText dans IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="99f0c-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="99f0c-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="99f0c-123">Ajoutez des SPLIT_BUFFER à des pages racine de l’arborescence d’espace (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="99f0c-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="99f0c-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="99f0c-125">Rétablissez la révision pour que ESE97 reste compatible avec les versions ultérieures (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="99f0c-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="99f0c-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="99f0c-127">Ajoutez de nouvelles colonnes avec balises au catalogue ( &quot; CallbackData &quot; et &quot; CallbackDependencies &quot; ).</span><span class="sxs-lookup"><span data-stu-id="99f0c-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="99f0c-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="99f0c-129">Prise en charge de SLV : signSLV, fSLVExists dans l’en-tête de base de connaissances (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="99f0c-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="99f0c-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="99f0c-131">Nouvelle arborescence d’espace SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="99f0c-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="99f0c-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="99f0c-133">Table d’espace SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="99f0c-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="99f0c-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="99f0c-135">IDXSEG de 4 octets (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="99f0c-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="99f0c-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="99f0c-137">Nouveau format de colonne de modèle (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="99f0c-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="99f0c-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="99f0c-139">Colonnes de modèle triées (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="99f0c-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-140">0x620, A</span><span class="sxs-lookup"><span data-stu-id="99f0c-140">0x620,A</span></span></p></td>
<td><p><span data-ttu-id="99f0c-141">Base de code fusionné (3/26/2003).</span><span class="sxs-lookup"><span data-stu-id="99f0c-141">Merged code base (3/26/2003).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-142">0x620, B</span><span class="sxs-lookup"><span data-stu-id="99f0c-142">0x620,B</span></span></p></td>
<td><p><span data-ttu-id="99f0c-143">Nouveau format de somme de contrôle (1/08/2004).</span><span class="sxs-lookup"><span data-stu-id="99f0c-143">New checksum format (1/08/2004).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-144">0x620, C</span><span class="sxs-lookup"><span data-stu-id="99f0c-144">0x620,C</span></span></p></td>
<td><p><span data-ttu-id="99f0c-145">Augmentation de la longueur maximale de la clé à 1000/2000 octets pour les pages de 4/8 Ko (1/15/2004).</span><span class="sxs-lookup"><span data-stu-id="99f0c-145">Increased max key length to 1000/2000 bytes for 4/8kb pages (1/15/2004).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-146">0x620, D</span><span class="sxs-lookup"><span data-stu-id="99f0c-146">0x620,D</span></span></p></td>
<td><p><span data-ttu-id="99f0c-147">Indicateurs d’espace de catalogue, space_header. v2 (7/15/2007).</span><span class="sxs-lookup"><span data-stu-id="99f0c-147">Catalog space hints, space_header.v2 (7/15/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-148">0x620, E</span><span class="sxs-lookup"><span data-stu-id="99f0c-148">0x620,E</span></span></p></td>
<td><p><span data-ttu-id="99f0c-149">Ajoutez un nouveau format de nœud/extension au gestionnaire d’espace, utilisez-le pour les pools d’espace réservés (8/9/2007).</span><span class="sxs-lookup"><span data-stu-id="99f0c-149">Add new node/extent format to space manager, use it for reserved pools of space (8/9/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-150">0x620, F</span><span class="sxs-lookup"><span data-stu-id="99f0c-150">0x620,F</span></span></p></td>
<td><p><span data-ttu-id="99f0c-151">Compression pour les valeurs longues intrinsèques (10/30/2007).</span><span class="sxs-lookup"><span data-stu-id="99f0c-151">Compression for intrinsic long-values (10/30/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-152">0x620, 10</span><span class="sxs-lookup"><span data-stu-id="99f0c-152">0x620,10</span></span></p></td>
<td><p><span data-ttu-id="99f0c-153">Compression pour les valeurs Long séparées (12/05/2007).</span><span class="sxs-lookup"><span data-stu-id="99f0c-153">Compression for separated long-values (12/05/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-154">0x620, 11</span><span class="sxs-lookup"><span data-stu-id="99f0c-154">0x620,11</span></span></p></td>
<td><p><span data-ttu-id="99f0c-155">Nouvelle taille de segment VL pour les pages de grande taille (12/29/2007).</span><span class="sxs-lookup"><span data-stu-id="99f0c-155">New LV chunk size for large pages (12/29/2007).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="99f0c-156">**signDb**</span><span class="sxs-lookup"><span data-stu-id="99f0c-156">**signDb**</span></span>

<span data-ttu-id="99f0c-157">Signature de la base de données (y compris l’heure de création).</span><span class="sxs-lookup"><span data-stu-id="99f0c-157">Signature of the database (including creation time).</span></span> <span data-ttu-id="99f0c-158">Cette structure est de 28 octets.</span><span class="sxs-lookup"><span data-stu-id="99f0c-158">This structure is 28 bytes.</span></span>

<span data-ttu-id="99f0c-159">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="99f0c-159">**dbstate**</span></span>

<span data-ttu-id="99f0c-160">Il s’agit de l’état de la base de données.</span><span class="sxs-lookup"><span data-stu-id="99f0c-160">This is the database state.</span></span>

<span data-ttu-id="99f0c-161">Les options suivantes sont disponibles pour ce membre.</span><span class="sxs-lookup"><span data-stu-id="99f0c-161">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99f0c-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="99f0c-162">Value</span></span></p></th>
<th><p><span data-ttu-id="99f0c-163">Signification</span><span class="sxs-lookup"><span data-stu-id="99f0c-163">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-164">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="99f0c-164">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="99f0c-165">1</span><span class="sxs-lookup"><span data-stu-id="99f0c-165">1</span></span></p></td>
<td><p><span data-ttu-id="99f0c-166">La base de données vient d’être créée.</span><span class="sxs-lookup"><span data-stu-id="99f0c-166">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-167">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="99f0c-167">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="99f0c-168">2</span><span class="sxs-lookup"><span data-stu-id="99f0c-168">2</span></span></p></td>
<td><p><span data-ttu-id="99f0c-169">La base de données nécessite une récupération matérielle ou logicielle pour être utilisable ou déplaçable.</span><span class="sxs-lookup"><span data-stu-id="99f0c-169">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="99f0c-170">L’un ne doit pas essayer de déplacer des bases de données dans cet État.</span><span class="sxs-lookup"><span data-stu-id="99f0c-170">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-171">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="99f0c-171">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="99f0c-172">3</span><span class="sxs-lookup"><span data-stu-id="99f0c-172">3</span></span></p></td>
<td><p><span data-ttu-id="99f0c-173">La base de données est dans un état propre.</span><span class="sxs-lookup"><span data-stu-id="99f0c-173">The database is in a clean state.</span></span> <span data-ttu-id="99f0c-174">La base de données peut être jointe sans aucun fichier journal.</span><span class="sxs-lookup"><span data-stu-id="99f0c-174">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-175">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="99f0c-175">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="99f0c-176">4</span><span class="sxs-lookup"><span data-stu-id="99f0c-176">4</span></span></p></td>
<td><p><span data-ttu-id="99f0c-177">La base de données est en cours de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="99f0c-177">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-178">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="99f0c-178">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="99f0c-179">5</span><span class="sxs-lookup"><span data-stu-id="99f0c-179">5</span></span></p></td>
<td><p><span data-ttu-id="99f0c-180">Internes.</span><span class="sxs-lookup"><span data-stu-id="99f0c-180">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="99f0c-181">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="99f0c-181">**lgposConsistent**</span></span>

<span data-ttu-id="99f0c-182">NULL si la base de données est dans un état modifié.</span><span class="sxs-lookup"><span data-stu-id="99f0c-182">Null if the database is in a dirty state.</span></span> <span data-ttu-id="99f0c-183">Il s’agit de la position du journal qui a été utilisée lors du dernier enregistrement de la base de données dans un état d’arrêt normal.</span><span class="sxs-lookup"><span data-stu-id="99f0c-183">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="99f0c-184">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="99f0c-184">**logtimeConsistent**</span></span>

<span data-ttu-id="99f0c-185">NULL si la base de données est dans un état modifié.</span><span class="sxs-lookup"><span data-stu-id="99f0c-185">Null if the database is in a dirty state.</span></span> <span data-ttu-id="99f0c-186">Il s’agit de l’heure à laquelle la base de données a été ramenée dans un état d’arrêt normal.</span><span class="sxs-lookup"><span data-stu-id="99f0c-186">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="99f0c-187">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="99f0c-187">**logtimeAttach**</span></span>

<span data-ttu-id="99f0c-188">Heure à laquelle la base de données a été attachée pour la dernière fois à [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="99f0c-188">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="99f0c-189">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="99f0c-189">**lgposAttach**</span></span>

<span data-ttu-id="99f0c-190">Position du journal qui a été utilisée lors de la dernière connexion de la base de données à [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="99f0c-190">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="99f0c-191">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="99f0c-191">**logtimeDetach**</span></span>

<span data-ttu-id="99f0c-192">Heure à laquelle la base de données a été détachée pour la dernière fois avec [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="99f0c-192">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="99f0c-193">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="99f0c-193">**lgposDetach**</span></span>

<span data-ttu-id="99f0c-194">Position du journal qui a été utilisée lors du dernier détachement de la base de données avec [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="99f0c-194">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="99f0c-195">**signLog**</span><span class="sxs-lookup"><span data-stu-id="99f0c-195">**signLog**</span></span>

<span data-ttu-id="99f0c-196">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="99f0c-196">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="99f0c-197">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="99f0c-197">**bkinfoFullPrev**</span></span>

<span data-ttu-id="99f0c-198">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="99f0c-198">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="99f0c-199">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="99f0c-199">**bkinfoIncPrev**</span></span>

<span data-ttu-id="99f0c-200">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="99f0c-200">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="99f0c-201">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="99f0c-201">**bkinfoFullCur**</span></span>

<span data-ttu-id="99f0c-202">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="99f0c-202">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="99f0c-203">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="99f0c-203">**fShadowingDisabled**</span></span>

<span data-ttu-id="99f0c-204">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="99f0c-204">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="99f0c-205">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="99f0c-205">**fUpgradeDb**</span></span>

<span data-ttu-id="99f0c-206">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="99f0c-206">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="99f0c-207">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="99f0c-207">**dwMajorVersion**</span></span>

<span data-ttu-id="99f0c-208">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="99f0c-208">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="99f0c-209">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="99f0c-209">Used for updating indexes.</span></span>

<span data-ttu-id="99f0c-210">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="99f0c-210">**dwMinorVersion**</span></span>

<span data-ttu-id="99f0c-211">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="99f0c-211">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="99f0c-212">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="99f0c-212">Used for updating indexes.</span></span>

<span data-ttu-id="99f0c-213">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="99f0c-213">**dwBuildNumber**</span></span>

<span data-ttu-id="99f0c-214">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="99f0c-214">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="99f0c-215">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="99f0c-215">Used for updating indexes.</span></span>

<span data-ttu-id="99f0c-216">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="99f0c-216">**lSPNumber**</span></span>

<span data-ttu-id="99f0c-217">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="99f0c-217">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="99f0c-218">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="99f0c-218">Used for updating indexes.</span></span>

<span data-ttu-id="99f0c-219">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="99f0c-219">**cbPageSize**</span></span>

<span data-ttu-id="99f0c-220">Taille de la page de base de données.</span><span class="sxs-lookup"><span data-stu-id="99f0c-220">Database page size.</span></span> <span data-ttu-id="99f0c-221">0 signifie que la taille de la page est de 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="99f0c-221">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="99f0c-222">Cette valeur est récupérée uniquement si JET_DbInfoMisc a été passé à [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="99f0c-222">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

<span data-ttu-id="99f0c-223">**genMinRequired**</span><span class="sxs-lookup"><span data-stu-id="99f0c-223">**genMinRequired**</span></span>

<span data-ttu-id="99f0c-224">Représente la génération de journal minimale requise pour relire les journaux.</span><span class="sxs-lookup"><span data-stu-id="99f0c-224">Represents the minimum log generation required for replaying the logs.</span></span> <span data-ttu-id="99f0c-225">Elle est généralement utilisée comme génération de point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="99f0c-225">This is typically used as the checkpoint generation.</span></span>

<span data-ttu-id="99f0c-226">**genMaxRequired**</span><span class="sxs-lookup"><span data-stu-id="99f0c-226">**genMaxRequired**</span></span>

<span data-ttu-id="99f0c-227">Représente la génération de journal maximale requise pour relire les journaux.</span><span class="sxs-lookup"><span data-stu-id="99f0c-227">Represents the maximum log generation required for replaying the logs.</span></span>

<span data-ttu-id="99f0c-228">**logtimeGenMaxCreate**</span><span class="sxs-lookup"><span data-stu-id="99f0c-228">**logtimeGenMaxCreate**</span></span>

<span data-ttu-id="99f0c-229">Représente la date et l’heure de création du fichier journal genMax.</span><span class="sxs-lookup"><span data-stu-id="99f0c-229">Represents the creation date and time of the genMax log file.</span></span>

<span data-ttu-id="99f0c-230">**ulRepairCount**</span><span class="sxs-lookup"><span data-stu-id="99f0c-230">**ulRepairCount**</span></span>

<span data-ttu-id="99f0c-231">Nombre de fois où une réparation a été appelée sur cette base de données.</span><span class="sxs-lookup"><span data-stu-id="99f0c-231">The number of times a repair has been called on this database.</span></span>

<span data-ttu-id="99f0c-232">**logtimeRepair**</span><span class="sxs-lookup"><span data-stu-id="99f0c-232">**logtimeRepair**</span></span>

<span data-ttu-id="99f0c-233">Représente la date et l’heure de la dernière réparation effectuée.</span><span class="sxs-lookup"><span data-stu-id="99f0c-233">Represents the date and time the last repair was run.</span></span>

<span data-ttu-id="99f0c-234">**ulRepairCountOld**</span><span class="sxs-lookup"><span data-stu-id="99f0c-234">**ulRepairCountOld**</span></span>

<span data-ttu-id="99f0c-235">Nombre de fois où la réparation a été exécutée sur cette base de données avant la dernière défragmentation.</span><span class="sxs-lookup"><span data-stu-id="99f0c-235">The number of times the repair had been run on this database before the last defragmentation.</span></span>

<span data-ttu-id="99f0c-236">**ulECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="99f0c-236">**ulECCFixSuccess**</span></span>

<span data-ttu-id="99f0c-237">Nombre de fois qu’une erreur d’un bit a été résolue et a généré une bonne page.</span><span class="sxs-lookup"><span data-stu-id="99f0c-237">The number of times a one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="99f0c-238">**logtimeECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="99f0c-238">**logtimeECCFixSuccess**</span></span>

<span data-ttu-id="99f0c-239">Représente la date et l’heure auxquelles la dernière erreur de bit a été résolue et a donné lieu à une bonne page.</span><span class="sxs-lookup"><span data-stu-id="99f0c-239">Represents the date and time the last one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="99f0c-240">**ulECCFixSuccessOld**</span><span class="sxs-lookup"><span data-stu-id="99f0c-240">**ulECCFixSuccessOld**</span></span>

<span data-ttu-id="99f0c-241">Représente le nombre de fois qu’une erreur de bit a été résolue et a donné lieu à une bonne page avant la dernière réparation.</span><span class="sxs-lookup"><span data-stu-id="99f0c-241">Represents the number of times a one bit error was fixed and resulted in a good page before last repair.</span></span>

<span data-ttu-id="99f0c-242">**ulECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="99f0c-242">**ulECCFixFail**</span></span>

<span data-ttu-id="99f0c-243">Nombre de fois qu’une erreur de bit a été résolue et a entraîné une mauvaise page.</span><span class="sxs-lookup"><span data-stu-id="99f0c-243">The number of times a one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="99f0c-244">**logtimeECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="99f0c-244">**logtimeECCFixFail**</span></span>

<span data-ttu-id="99f0c-245">Représente la date et l’heure auxquelles la dernière erreur de bit a été résolue et a entraîné une page incorrecte.</span><span class="sxs-lookup"><span data-stu-id="99f0c-245">Represents the date and time the last one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="99f0c-246">**ulECCFixFailOld**</span><span class="sxs-lookup"><span data-stu-id="99f0c-246">**ulECCFixFailOld**</span></span>

<span data-ttu-id="99f0c-247">Nombre de fois qu’une erreur de bit a été résolue et a entraîné une mauvaise page avant la dernière réparation.</span><span class="sxs-lookup"><span data-stu-id="99f0c-247">The number of times a one bit error was fixed and resulted in a bad page before last repair.</span></span>

<span data-ttu-id="99f0c-248">**ulBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="99f0c-248">**ulBadChecksum**</span></span>

<span data-ttu-id="99f0c-249">Nombre de fois qu’une erreur ECC/checksum non corrigeable a été détectée.</span><span class="sxs-lookup"><span data-stu-id="99f0c-249">The number of times a non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="99f0c-250">**logtimeBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="99f0c-250">**logtimeBadChecksum**</span></span>

<span data-ttu-id="99f0c-251">Représente la date et l’heure de la dernière erreur ECC/checksum non corrigeable.</span><span class="sxs-lookup"><span data-stu-id="99f0c-251">Represents the date and time the last non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="99f0c-252">**ulBadChecksumOld**</span><span class="sxs-lookup"><span data-stu-id="99f0c-252">**ulBadChecksumOld**</span></span>

<span data-ttu-id="99f0c-253">Nombre de fois qu’une erreur ECC/checksum non réparable a été détectée avant la dernière réparation.</span><span class="sxs-lookup"><span data-stu-id="99f0c-253">The number of times a non-correctable ECC/checksum error was found before last repair.</span></span>

<span data-ttu-id="99f0c-254">**genCommitted**</span><span class="sxs-lookup"><span data-stu-id="99f0c-254">**genCommitted**</span></span>

<span data-ttu-id="99f0c-255">Nombre maximal de générations de journaux validées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="99f0c-255">The maximum number of log generations committed to the database.</span></span> <span data-ttu-id="99f0c-256">En général, génération de journal en cours.</span><span class="sxs-lookup"><span data-stu-id="99f0c-256">Typically the current log generation.</span></span>

<span data-ttu-id="99f0c-257">**bkinfoCopyPrev**</span><span class="sxs-lookup"><span data-stu-id="99f0c-257">**bkinfoCopyPrev**</span></span>

<span data-ttu-id="99f0c-258">Dernière sauvegarde de copie réussie.</span><span class="sxs-lookup"><span data-stu-id="99f0c-258">The last successful Copy backup.</span></span>

<span data-ttu-id="99f0c-259">**bkinfoDiffPrev**</span><span class="sxs-lookup"><span data-stu-id="99f0c-259">**bkinfoDiffPrev**</span></span>

<span data-ttu-id="99f0c-260">Dernière sauvegarde différentielle réussie.</span><span class="sxs-lookup"><span data-stu-id="99f0c-260">The last successful Differential backup.</span></span> <span data-ttu-id="99f0c-261">Cette valeur est réinitialisée lorsque bkinfoFullPrev est défini.</span><span class="sxs-lookup"><span data-stu-id="99f0c-261">This value is reset when bkinfoFullPrev is set.</span></span>

### <a name="requirements"></a><span data-ttu-id="99f0c-262">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99f0c-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-263"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="99f0c-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="99f0c-264">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="99f0c-264">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f0c-265"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="99f0c-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="99f0c-266">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="99f0c-266">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f0c-267"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="99f0c-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="99f0c-268">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="99f0c-268">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="99f0c-269">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99f0c-269">See Also</span></span>

[<span data-ttu-id="99f0c-270">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="99f0c-270">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="99f0c-271">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="99f0c-271">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="99f0c-272">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="99f0c-272">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="99f0c-273">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="99f0c-273">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="99f0c-274">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="99f0c-274">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="99f0c-275">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="99f0c-275">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
