---
description: 'En savoir plus sur : structure JET_DBINFOMISC2'
title: Structure JET_DBINFOMISC2
TOCTitle: JET_DBINFOMISC2 Structure
ms:assetid: c62e87ca-c02c-4d6f-a1e6-f80d022c6aad
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294085(v=EXCHG.10)
ms:contentKeyID: 32765700
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cf47565a199bd17df47fb6962a1d174454dbe39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515608"
---
# <a name="jet_dbinfomisc2-structure"></a><span data-ttu-id="6391e-103">Structure JET_DBINFOMISC2</span><span class="sxs-lookup"><span data-stu-id="6391e-103">JET_DBINFOMISC2 Structure</span></span>


<span data-ttu-id="6391e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="6391e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc2-structure"></a><span data-ttu-id="6391e-105">Structure JET_DBINFOMISC2</span><span class="sxs-lookup"><span data-stu-id="6391e-105">JET_DBINFOMISC2 Structure</span></span>

<span data-ttu-id="6391e-106">La structure **JET_DBINFOMISC2** contient diverses informations sur une base de données.</span><span class="sxs-lookup"><span data-stu-id="6391e-106">The **JET_DBINFOMISC2** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="6391e-107">Il s’agit des informations contenues dans l’en-tête de base de données.</span><span class="sxs-lookup"><span data-stu-id="6391e-107">This is the information that is contained in the database header.</span></span>

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
    } JET_DBINFOMISC2;
```

### <a name="members"></a><span data-ttu-id="6391e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6391e-108">Members</span></span>

<span data-ttu-id="6391e-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="6391e-109">**ulVersion**</span></span>

<span data-ttu-id="6391e-110">Version native du moteur de base de données qui a créé la base de données.</span><span class="sxs-lookup"><span data-stu-id="6391e-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="6391e-111">Consultez [JetGetVersion](./jetgetversion-function.md) pour récupérer la version native du moteur de base de données actuel.</span><span class="sxs-lookup"><span data-stu-id="6391e-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="6391e-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="6391e-112">**ulUpdate**</span></span>

<span data-ttu-id="6391e-113">Effectue le suivi des mises à jour incrémentielles du format de base de données qui sont à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="6391e-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6391e-114">ulVersion, ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="6391e-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="6391e-115">Signification</span><span class="sxs-lookup"><span data-stu-id="6391e-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6391e-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="6391e-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="6391e-117">Format bêta du système d’exploitation d’origine (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="6391e-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="6391e-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="6391e-119">Ajoutez des colonnes dans le catalogue pour l’indexation conditionnelle et l’ancienne (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="6391e-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="6391e-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="6391e-121">Ajoutez l’indicateur fLocalizedText dans IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="6391e-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="6391e-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="6391e-123">Ajoutez des SPLIT_BUFFER à des pages racine de l’arborescence d’espace (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="6391e-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="6391e-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="6391e-125">Rétablissez la révision pour que ESE97 reste compatible avec les versions ultérieures (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="6391e-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="6391e-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="6391e-127">Ajoutez de nouvelles colonnes avec balises au catalogue ( &quot; CallbackData &quot; et &quot; CallbackDependencies &quot; ).</span><span class="sxs-lookup"><span data-stu-id="6391e-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="6391e-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="6391e-129">Prise en charge de SLV : signSLV, fSLVExists dans l’en-tête de base de connaissances (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="6391e-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="6391e-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="6391e-131">Nouvelle arborescence d’espace SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="6391e-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="6391e-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="6391e-133">Table d’espace SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="6391e-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="6391e-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="6391e-135">IDXSEG de 4 octets (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="6391e-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="6391e-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="6391e-137">Nouveau format de colonne de modèle (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="6391e-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="6391e-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="6391e-139">Colonnes de modèle triées (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="6391e-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-140">0x620, A</span><span class="sxs-lookup"><span data-stu-id="6391e-140">0x620,A</span></span></p></td>
<td><p><span data-ttu-id="6391e-141">Base de code fusionné (3/26/2003).</span><span class="sxs-lookup"><span data-stu-id="6391e-141">Merged code base (3/26/2003).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-142">0x620, B</span><span class="sxs-lookup"><span data-stu-id="6391e-142">0x620,B</span></span></p></td>
<td><p><span data-ttu-id="6391e-143">Nouveau format de somme de contrôle (1/08/2004).</span><span class="sxs-lookup"><span data-stu-id="6391e-143">New checksum format (1/08/2004).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-144">0x620, C</span><span class="sxs-lookup"><span data-stu-id="6391e-144">0x620,C</span></span></p></td>
<td><p><span data-ttu-id="6391e-145">Augmentation de la longueur maximale de la clé à 1000/2000 octets pour les pages de 4/8 Ko (1/15/2004).</span><span class="sxs-lookup"><span data-stu-id="6391e-145">Increased max key length to 1000/2000 bytes for 4/8kb pages (1/15/2004).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-146">0x620, D</span><span class="sxs-lookup"><span data-stu-id="6391e-146">0x620,D</span></span></p></td>
<td><p><span data-ttu-id="6391e-147">Indicateurs d’espace de catalogue, space_header. v2 (7/15/2007).</span><span class="sxs-lookup"><span data-stu-id="6391e-147">Catalog space hints, space_header.v2 (7/15/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-148">0x620, E</span><span class="sxs-lookup"><span data-stu-id="6391e-148">0x620,E</span></span></p></td>
<td><p><span data-ttu-id="6391e-149">Ajoutez un nouveau format de nœud/extension au gestionnaire d’espace, utilisez-le pour les pools d’espace réservés (8/9/2007).</span><span class="sxs-lookup"><span data-stu-id="6391e-149">Add new node/extent format to space manager, use it for reserved pools of space (8/9/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-150">0x620, F</span><span class="sxs-lookup"><span data-stu-id="6391e-150">0x620,F</span></span></p></td>
<td><p><span data-ttu-id="6391e-151">Compression pour les valeurs longues intrinsèques (10/30/2007).</span><span class="sxs-lookup"><span data-stu-id="6391e-151">Compression for intrinsic long-values (10/30/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-152">0x620, 10</span><span class="sxs-lookup"><span data-stu-id="6391e-152">0x620,10</span></span></p></td>
<td><p><span data-ttu-id="6391e-153">Compression pour les valeurs Long séparées (12/05/2007).</span><span class="sxs-lookup"><span data-stu-id="6391e-153">Compression for separated long-values (12/05/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-154">0x620, 11</span><span class="sxs-lookup"><span data-stu-id="6391e-154">0x620,11</span></span></p></td>
<td><p><span data-ttu-id="6391e-155">Nouvelle taille de segment VL pour les pages de grande taille (12/29/2007).</span><span class="sxs-lookup"><span data-stu-id="6391e-155">New LV chunk size for large pages (12/29/2007).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6391e-156">**signDb**</span><span class="sxs-lookup"><span data-stu-id="6391e-156">**signDb**</span></span>

<span data-ttu-id="6391e-157">Signature de la base de données (y compris l’heure de création).</span><span class="sxs-lookup"><span data-stu-id="6391e-157">Signature of the database (including creation time).</span></span> <span data-ttu-id="6391e-158">Cette structure est de 28 octets.</span><span class="sxs-lookup"><span data-stu-id="6391e-158">This structure is 28 bytes.</span></span>

<span data-ttu-id="6391e-159">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="6391e-159">**dbstate**</span></span>

<span data-ttu-id="6391e-160">Il s’agit de l’état de la base de données.</span><span class="sxs-lookup"><span data-stu-id="6391e-160">This is the database state.</span></span>

<span data-ttu-id="6391e-161">Les options suivantes sont disponibles pour ce membre.</span><span class="sxs-lookup"><span data-stu-id="6391e-161">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6391e-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="6391e-162">Value</span></span></p></th>
<th><p><span data-ttu-id="6391e-163">Signification</span><span class="sxs-lookup"><span data-stu-id="6391e-163">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6391e-164">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="6391e-164">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="6391e-165">1</span><span class="sxs-lookup"><span data-stu-id="6391e-165">1</span></span></p></td>
<td><p><span data-ttu-id="6391e-166">La base de données vient d’être créée.</span><span class="sxs-lookup"><span data-stu-id="6391e-166">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-167">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="6391e-167">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="6391e-168">2</span><span class="sxs-lookup"><span data-stu-id="6391e-168">2</span></span></p></td>
<td><p><span data-ttu-id="6391e-169">La base de données nécessite une récupération matérielle ou logicielle pour être utilisable ou déplaçable.</span><span class="sxs-lookup"><span data-stu-id="6391e-169">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="6391e-170">L’un ne doit pas essayer de déplacer des bases de données dans cet État.</span><span class="sxs-lookup"><span data-stu-id="6391e-170">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-171">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="6391e-171">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="6391e-172">3</span><span class="sxs-lookup"><span data-stu-id="6391e-172">3</span></span></p></td>
<td><p><span data-ttu-id="6391e-173">La base de données est dans un état propre.</span><span class="sxs-lookup"><span data-stu-id="6391e-173">The database is in a clean state.</span></span> <span data-ttu-id="6391e-174">La base de données peut être jointe sans aucun fichier journal.</span><span class="sxs-lookup"><span data-stu-id="6391e-174">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-175">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="6391e-175">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="6391e-176">4</span><span class="sxs-lookup"><span data-stu-id="6391e-176">4</span></span></p></td>
<td><p><span data-ttu-id="6391e-177">La base de données est en cours de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="6391e-177">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-178">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="6391e-178">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="6391e-179">5</span><span class="sxs-lookup"><span data-stu-id="6391e-179">5</span></span></p></td>
<td><p><span data-ttu-id="6391e-180">Internes.</span><span class="sxs-lookup"><span data-stu-id="6391e-180">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6391e-181">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="6391e-181">**lgposConsistent**</span></span>

<span data-ttu-id="6391e-182">NULL si la base de données est dans un état modifié.</span><span class="sxs-lookup"><span data-stu-id="6391e-182">Null if the database is in a dirty state.</span></span> <span data-ttu-id="6391e-183">Il s’agit de la position du journal qui a été utilisée lors du dernier enregistrement de la base de données dans un état d’arrêt normal.</span><span class="sxs-lookup"><span data-stu-id="6391e-183">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="6391e-184">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="6391e-184">**logtimeConsistent**</span></span>

<span data-ttu-id="6391e-185">NULL si la base de données est dans un état modifié.</span><span class="sxs-lookup"><span data-stu-id="6391e-185">Null if the database is in a dirty state.</span></span> <span data-ttu-id="6391e-186">Il s’agit de l’heure à laquelle la base de données a été ramenée dans un état d’arrêt normal.</span><span class="sxs-lookup"><span data-stu-id="6391e-186">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="6391e-187">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="6391e-187">**logtimeAttach**</span></span>

<span data-ttu-id="6391e-188">Heure à laquelle la base de données a été attachée pour la dernière fois à [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="6391e-188">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="6391e-189">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="6391e-189">**lgposAttach**</span></span>

<span data-ttu-id="6391e-190">Position du journal qui a été utilisée lors de la dernière connexion de la base de données à [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="6391e-190">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="6391e-191">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="6391e-191">**logtimeDetach**</span></span>

<span data-ttu-id="6391e-192">Heure à laquelle la base de données a été détachée pour la dernière fois avec [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="6391e-192">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="6391e-193">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="6391e-193">**lgposDetach**</span></span>

<span data-ttu-id="6391e-194">Position du journal qui a été utilisée lors du dernier détachement de la base de données avec [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="6391e-194">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="6391e-195">**signLog**</span><span class="sxs-lookup"><span data-stu-id="6391e-195">**signLog**</span></span>

<span data-ttu-id="6391e-196">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="6391e-196">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="6391e-197">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="6391e-197">**bkinfoFullPrev**</span></span>

<span data-ttu-id="6391e-198">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="6391e-198">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="6391e-199">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="6391e-199">**bkinfoIncPrev**</span></span>

<span data-ttu-id="6391e-200">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="6391e-200">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="6391e-201">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="6391e-201">**bkinfoFullCur**</span></span>

<span data-ttu-id="6391e-202">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="6391e-202">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="6391e-203">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="6391e-203">**fShadowingDisabled**</span></span>

<span data-ttu-id="6391e-204">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="6391e-204">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="6391e-205">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="6391e-205">**fUpgradeDb**</span></span>

<span data-ttu-id="6391e-206">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="6391e-206">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="6391e-207">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="6391e-207">**dwMajorVersion**</span></span>

<span data-ttu-id="6391e-208">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6391e-208">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="6391e-209">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="6391e-209">Used for updating indexes.</span></span>

<span data-ttu-id="6391e-210">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="6391e-210">**dwMinorVersion**</span></span>

<span data-ttu-id="6391e-211">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6391e-211">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="6391e-212">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="6391e-212">Used for updating indexes.</span></span>

<span data-ttu-id="6391e-213">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="6391e-213">**dwBuildNumber**</span></span>

<span data-ttu-id="6391e-214">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6391e-214">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="6391e-215">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="6391e-215">Used for updating indexes.</span></span>

<span data-ttu-id="6391e-216">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="6391e-216">**lSPNumber**</span></span>

<span data-ttu-id="6391e-217">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6391e-217">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="6391e-218">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="6391e-218">Used for updating indexes.</span></span>

<span data-ttu-id="6391e-219">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="6391e-219">**cbPageSize**</span></span>

<span data-ttu-id="6391e-220">Taille de la page de base de données.</span><span class="sxs-lookup"><span data-stu-id="6391e-220">Database page size.</span></span> <span data-ttu-id="6391e-221">0 signifie que la taille de la page est de 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="6391e-221">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="6391e-222">Cette valeur est récupérée uniquement si JET_DbInfoMisc a été passé à [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="6391e-222">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

<span data-ttu-id="6391e-223">**genMinRequired**</span><span class="sxs-lookup"><span data-stu-id="6391e-223">**genMinRequired**</span></span>

<span data-ttu-id="6391e-224">Représente la génération de journal minimale requise pour relire les journaux.</span><span class="sxs-lookup"><span data-stu-id="6391e-224">Represents the minimum log generation required for replaying the logs.</span></span> <span data-ttu-id="6391e-225">Elle est généralement utilisée comme génération de point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6391e-225">This is typically used as the checkpoint generation.</span></span>

<span data-ttu-id="6391e-226">**genMaxRequired**</span><span class="sxs-lookup"><span data-stu-id="6391e-226">**genMaxRequired**</span></span>

<span data-ttu-id="6391e-227">Représente la génération de journal maximale requise pour relire les journaux.</span><span class="sxs-lookup"><span data-stu-id="6391e-227">Represents the maximum log generation required for replaying the logs.</span></span>

<span data-ttu-id="6391e-228">**logtimeGenMaxCreate**</span><span class="sxs-lookup"><span data-stu-id="6391e-228">**logtimeGenMaxCreate**</span></span>

<span data-ttu-id="6391e-229">Représente la date et l’heure de création du fichier journal genMax.</span><span class="sxs-lookup"><span data-stu-id="6391e-229">Represents the creation date and time of the genMax log file.</span></span>

<span data-ttu-id="6391e-230">**ulRepairCount**</span><span class="sxs-lookup"><span data-stu-id="6391e-230">**ulRepairCount**</span></span>

<span data-ttu-id="6391e-231">Nombre de fois où une réparation a été appelée sur cette base de données.</span><span class="sxs-lookup"><span data-stu-id="6391e-231">The number of times a repair has been called on this database.</span></span>

<span data-ttu-id="6391e-232">**logtimeRepair**</span><span class="sxs-lookup"><span data-stu-id="6391e-232">**logtimeRepair**</span></span>

<span data-ttu-id="6391e-233">Représente la date et l’heure de la dernière réparation effectuée.</span><span class="sxs-lookup"><span data-stu-id="6391e-233">Represents the date and time the last repair was run.</span></span>

<span data-ttu-id="6391e-234">**ulRepairCountOld**</span><span class="sxs-lookup"><span data-stu-id="6391e-234">**ulRepairCountOld**</span></span>

<span data-ttu-id="6391e-235">Nombre de fois où la réparation a été exécutée sur cette base de données avant la dernière défragmentation.</span><span class="sxs-lookup"><span data-stu-id="6391e-235">The number of times the repair had been run on this database before the last defragmentation.</span></span>

<span data-ttu-id="6391e-236">**ulECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="6391e-236">**ulECCFixSuccess**</span></span>

<span data-ttu-id="6391e-237">Nombre de fois qu’une erreur d’un bit a été résolue et a généré une bonne page.</span><span class="sxs-lookup"><span data-stu-id="6391e-237">The number of times a one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="6391e-238">**logtimeECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="6391e-238">**logtimeECCFixSuccess**</span></span>

<span data-ttu-id="6391e-239">Représente la date et l’heure auxquelles la dernière erreur de bit a été résolue et a donné lieu à une bonne page.</span><span class="sxs-lookup"><span data-stu-id="6391e-239">Represents the date and time the last one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="6391e-240">**ulECCFixSuccessOld**</span><span class="sxs-lookup"><span data-stu-id="6391e-240">**ulECCFixSuccessOld**</span></span>

<span data-ttu-id="6391e-241">Représente le nombre de fois qu’une erreur de bit a été résolue et a donné lieu à une bonne page avant la dernière réparation.</span><span class="sxs-lookup"><span data-stu-id="6391e-241">Represents the number of times a one bit error was fixed and resulted in a good page before last repair.</span></span>

<span data-ttu-id="6391e-242">**ulECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="6391e-242">**ulECCFixFail**</span></span>

<span data-ttu-id="6391e-243">Nombre de fois qu’une erreur de bit a été résolue et a entraîné une mauvaise page.</span><span class="sxs-lookup"><span data-stu-id="6391e-243">The number of times a one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="6391e-244">**logtimeECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="6391e-244">**logtimeECCFixFail**</span></span>

<span data-ttu-id="6391e-245">Représente la date et l’heure auxquelles la dernière erreur de bit a été résolue et a entraîné une page incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6391e-245">Represents the date and time the last one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="6391e-246">**ulECCFixFailOld**</span><span class="sxs-lookup"><span data-stu-id="6391e-246">**ulECCFixFailOld**</span></span>

<span data-ttu-id="6391e-247">Nombre de fois qu’une erreur de bit a été résolue et a entraîné une mauvaise page avant la dernière réparation.</span><span class="sxs-lookup"><span data-stu-id="6391e-247">The number of times a one bit error was fixed and resulted in a bad page before last repair.</span></span>

<span data-ttu-id="6391e-248">**ulBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="6391e-248">**ulBadChecksum**</span></span>

<span data-ttu-id="6391e-249">Nombre de fois qu’une erreur ECC/checksum non corrigeable a été détectée.</span><span class="sxs-lookup"><span data-stu-id="6391e-249">The number of times a non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="6391e-250">**logtimeBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="6391e-250">**logtimeBadChecksum**</span></span>

<span data-ttu-id="6391e-251">Représente la date et l’heure de la dernière erreur ECC/checksum non corrigeable.</span><span class="sxs-lookup"><span data-stu-id="6391e-251">Represents the date and time the last non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="6391e-252">**ulBadChecksumOld**</span><span class="sxs-lookup"><span data-stu-id="6391e-252">**ulBadChecksumOld**</span></span>

<span data-ttu-id="6391e-253">Nombre de fois qu’une erreur ECC/checksum non réparable a été détectée avant la dernière réparation.</span><span class="sxs-lookup"><span data-stu-id="6391e-253">The number of times a non-correctable ECC/checksum error was found before last repair.</span></span>

### <a name="requirements"></a><span data-ttu-id="6391e-254">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6391e-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6391e-255"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6391e-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6391e-256">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="6391e-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6391e-257"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="6391e-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6391e-258">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6391e-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6391e-259"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="6391e-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6391e-260">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="6391e-260">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6391e-261">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6391e-261">See Also</span></span>

[<span data-ttu-id="6391e-262">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="6391e-262">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="6391e-263">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="6391e-263">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="6391e-264">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="6391e-264">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="6391e-265">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="6391e-265">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="6391e-266">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="6391e-266">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="6391e-267">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="6391e-267">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
