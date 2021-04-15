---
description: 'En savoir plus sur : structure JET_DBINFOMISC'
title: Structure JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
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
ms.openlocfilehash: 649e16e956e5dcd272e6201f779cdddd352a7bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525053"
---
# <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="5ceb1-103">Structure JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="5ceb1-103">JET_DBINFOMISC Structure</span></span>


<span data-ttu-id="5ceb1-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="5ceb1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="5ceb1-105">Structure JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="5ceb1-105">JET_DBINFOMISC Structure</span></span>

<span data-ttu-id="5ceb1-106">La structure **JET_DBINFOMISC** contient diverses informations sur une base de données.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-106">The **JET_DBINFOMISC** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="5ceb1-107">Il s’agit des informations contenues dans l’en-tête de base de données.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-107">This is the information that is contained in the database header.</span></span>

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
    } JET_DBINFOMISC;
```

### <a name="members"></a><span data-ttu-id="5ceb1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5ceb1-108">Members</span></span>

<span data-ttu-id="5ceb1-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-109">**ulVersion**</span></span>

<span data-ttu-id="5ceb1-110">Version native du moteur de base de données qui a créé la base de données.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="5ceb1-111">Consultez [JetGetVersion](./jetgetversion-function.md) pour récupérer la version native du moteur de base de données actuel.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="5ceb1-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-112">**ulUpdate**</span></span>

<span data-ttu-id="5ceb1-113">Effectue le suivi des mises à jour incrémentielles du format de base de données qui sont à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ceb1-114">ulVersion, ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="5ceb1-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="5ceb1-115">Signification</span><span class="sxs-lookup"><span data-stu-id="5ceb1-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="5ceb1-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-117">Format bêta du système d’exploitation d’origine (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ceb1-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="5ceb1-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-119">Ajoutez des colonnes dans le catalogue pour l’indexation conditionnelle et l’ancienne (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="5ceb1-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-121">Ajoutez l’indicateur fLocalizedText dans IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ceb1-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="5ceb1-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-123">Ajoutez des SPLIT_BUFFER à des pages racine de l’arborescence d’espace (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="5ceb1-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-125">Rétablissez la révision pour que ESE97 reste compatible avec les versions ultérieures (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ceb1-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="5ceb1-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-127">Ajoutez de nouvelles colonnes avec balises au catalogue ( &quot; CallbackData &quot; et &quot; CallbackDependencies &quot; ).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="5ceb1-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-129">Prise en charge de SLV : signSLV, fSLVExists dans l’en-tête de base de connaissances (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ceb1-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="5ceb1-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-131">Nouvelle arborescence d’espace SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="5ceb1-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-133">Table d’espace SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ceb1-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="5ceb1-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-135">IDXSEG de 4 octets (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="5ceb1-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-137">Nouveau format de colonne de modèle (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ceb1-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="5ceb1-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-139">Colonnes de modèle triées (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-140">0x623, 0</span><span class="sxs-lookup"><span data-stu-id="5ceb1-140">0x623,0</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-141">Nouveau gestionnaire d’espace (5/15/99).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-141">New Space Manager (5/15/99).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5ceb1-142">**signDb**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-142">**signDb**</span></span>

<span data-ttu-id="5ceb1-143">Signature de la base de données (y compris l’heure de création).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-143">Signature of the database (including creation time).</span></span> <span data-ttu-id="5ceb1-144">Cette structure est de 28 octets.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-144">This structure is 28 bytes.</span></span>

<span data-ttu-id="5ceb1-145">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-145">**dbstate**</span></span>

<span data-ttu-id="5ceb1-146">Il s’agit de l’état de la base de données.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-146">This is the database state.</span></span>

<span data-ttu-id="5ceb1-147">Les options suivantes sont disponibles pour ce membre.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-147">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ceb1-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ceb1-148">Value</span></span></p></th>
<th><p><span data-ttu-id="5ceb1-149">Signification</span><span class="sxs-lookup"><span data-stu-id="5ceb1-149">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-150">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="5ceb1-150">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="5ceb1-151">1</span><span class="sxs-lookup"><span data-stu-id="5ceb1-151">1</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-152">La base de données vient d’être créée.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-152">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ceb1-153">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="5ceb1-153">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="5ceb1-154">2</span><span class="sxs-lookup"><span data-stu-id="5ceb1-154">2</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-155">La base de données nécessite une récupération matérielle ou logicielle pour être utilisable ou déplaçable.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-155">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="5ceb1-156">L’un ne doit pas essayer de déplacer des bases de données dans cet État.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-156">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-157">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="5ceb1-157">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="5ceb1-158">3</span><span class="sxs-lookup"><span data-stu-id="5ceb1-158">3</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-159">La base de données est dans un état propre.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-159">The database is in a clean state.</span></span> <span data-ttu-id="5ceb1-160">La base de données peut être jointe sans aucun fichier journal.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-160">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ceb1-161">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="5ceb1-161">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="5ceb1-162">4</span><span class="sxs-lookup"><span data-stu-id="5ceb1-162">4</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-163">La base de données est en cours de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-163">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-164">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="5ceb1-164">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="5ceb1-165">5</span><span class="sxs-lookup"><span data-stu-id="5ceb1-165">5</span></span></p></td>
<td><p><span data-ttu-id="5ceb1-166">Internes.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-166">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5ceb1-167">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-167">**lgposConsistent**</span></span>

<span data-ttu-id="5ceb1-168">NULL si la base de données est dans un état modifié.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-168">Null if the database is in a dirty state.</span></span> <span data-ttu-id="5ceb1-169">Il s’agit de la position du journal qui a été utilisée lors du dernier enregistrement de la base de données dans un état d’arrêt normal.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-169">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="5ceb1-170">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-170">**logtimeConsistent**</span></span>

<span data-ttu-id="5ceb1-171">NULL si la base de données est dans un état modifié.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-171">Null if the database is in a dirty state.</span></span> <span data-ttu-id="5ceb1-172">Il s’agit de l’heure à laquelle la base de données a été ramenée dans un état d’arrêt normal.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-172">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="5ceb1-173">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-173">**logtimeAttach**</span></span>

<span data-ttu-id="5ceb1-174">Heure à laquelle la base de données a été attachée pour la dernière fois à [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-174">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="5ceb1-175">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-175">**lgposAttach**</span></span>

<span data-ttu-id="5ceb1-176">Position du journal qui a été utilisée lors de la dernière connexion de la base de données à [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-176">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="5ceb1-177">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-177">**logtimeDetach**</span></span>

<span data-ttu-id="5ceb1-178">Heure à laquelle la base de données a été détachée pour la dernière fois avec [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-178">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="5ceb1-179">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-179">**lgposDetach**</span></span>

<span data-ttu-id="5ceb1-180">Position du journal qui a été utilisée lors du dernier détachement de la base de données avec [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-180">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="5ceb1-181">**signLog**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-181">**signLog**</span></span>

<span data-ttu-id="5ceb1-182">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-182">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="5ceb1-183">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-183">**bkinfoFullPrev**</span></span>

<span data-ttu-id="5ceb1-184">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-184">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="5ceb1-185">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-185">**bkinfoIncPrev**</span></span>

<span data-ttu-id="5ceb1-186">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-186">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="5ceb1-187">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-187">**bkinfoFullCur**</span></span>

<span data-ttu-id="5ceb1-188">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-188">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="5ceb1-189">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-189">**fShadowingDisabled**</span></span>

<span data-ttu-id="5ceb1-190">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-190">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="5ceb1-191">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-191">**fUpgradeDb**</span></span>

<span data-ttu-id="5ceb1-192">Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-192">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="5ceb1-193">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-193">**dwMajorVersion**</span></span>

<span data-ttu-id="5ceb1-194">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-194">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="5ceb1-195">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-195">Used for updating indexes.</span></span>

<span data-ttu-id="5ceb1-196">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-196">**dwMinorVersion**</span></span>

<span data-ttu-id="5ceb1-197">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-197">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="5ceb1-198">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-198">Used for updating indexes.</span></span>

<span data-ttu-id="5ceb1-199">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-199">**dwBuildNumber**</span></span>

<span data-ttu-id="5ceb1-200">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-200">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="5ceb1-201">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-201">Used for updating indexes.</span></span>

<span data-ttu-id="5ceb1-202">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-202">**lSPNumber**</span></span>

<span data-ttu-id="5ceb1-203">Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-203">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="5ceb1-204">Utilisé pour la mise à jour des index.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-204">Used for updating indexes.</span></span>

<span data-ttu-id="5ceb1-205">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="5ceb1-205">**cbPageSize**</span></span>

<span data-ttu-id="5ceb1-206">Taille de la page de base de données.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-206">Database page size.</span></span> <span data-ttu-id="5ceb1-207">0 signifie que la taille de la page est de 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-207">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="5ceb1-208">Cette valeur est récupérée uniquement si JET_DbInfoMisc a été passé à [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="5ceb1-208">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="5ceb1-209">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ceb1-209">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-210"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5ceb1-210"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5ceb1-211">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-211">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ceb1-212"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="5ceb1-212"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5ceb1-213">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-213">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ceb1-214"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="5ceb1-214"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5ceb1-215">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="5ceb1-215">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5ceb1-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ceb1-216">See Also</span></span>

[<span data-ttu-id="5ceb1-217">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="5ceb1-217">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="5ceb1-218">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="5ceb1-218">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="5ceb1-219">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="5ceb1-219">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="5ceb1-220">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="5ceb1-220">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="5ceb1-221">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="5ceb1-221">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="5ceb1-222">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="5ceb1-222">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
