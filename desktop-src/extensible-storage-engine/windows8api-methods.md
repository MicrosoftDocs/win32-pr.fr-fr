---
description: 'En savoir plus sur les méthodes suivantes : Windows8Api'
title: Méthodes Windows8Api (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: Windows8Api methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api_methods(v=EXCHG.10)
ms:contentKeyID: 55104457
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d8eb8b822affcbf41c375f7ef23b6a71d03afc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566079"
---
# <a name="windows8api-methods"></a><span data-ttu-id="6706e-103">Méthodes Windows8Api</span><span class="sxs-lookup"><span data-stu-id="6706e-103">Windows8Api methods</span></span>

<span data-ttu-id="6706e-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="6706e-104">Include protected members</span></span>  
<span data-ttu-id="6706e-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="6706e-105">Include inherited members</span></span>  

<span data-ttu-id="6706e-106">Le type [Windows8Api](./windows8api-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="6706e-106">The [Windows8Api](./windows8api-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="6706e-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6706e-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6706e-108">Nom</span><span class="sxs-lookup"><span data-stu-id="6706e-108">Name</span></span></th>
<th><span data-ttu-id="6706e-109">Description</span><span class="sxs-lookup"><span data-stu-id="6706e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-112"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span><span class="sxs-lookup"><span data-stu-id="6706e-112"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span></span></td>
<td><span data-ttu-id="6706e-113">Fait en sorte qu’une session entre dans une transaction ou crée un nouveau point d’enregistrement dans une transaction existante.</span><span class="sxs-lookup"><span data-stu-id="6706e-113">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-116"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span><span class="sxs-lookup"><span data-stu-id="6706e-116"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span></span></td>
<td><span data-ttu-id="6706e-117">Valide les modifications apportées à l’état de la base de données pendant le point d’enregistrement en cours et les migre vers le point d’enregistrement précédent.</span><span class="sxs-lookup"><span data-stu-id="6706e-117">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="6706e-118">Si le point d’enregistrement le plus à l’extérieur est validé, les modifications apportées pendant ce point d’enregistrement sont validées à l’état de la base de données et la session quitte la transaction.</span><span class="sxs-lookup"><span data-stu-id="6706e-118">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-121"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span><span class="sxs-lookup"><span data-stu-id="6706e-121"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span></span></td>
<td><span data-ttu-id="6706e-122">Crée des index sur des données dans une base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="6706e-122">Creates indexes over data in an ESE database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-125"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span><span class="sxs-lookup"><span data-stu-id="6706e-125"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span></span></td>
<td><span data-ttu-id="6706e-126">Crée une table, ajoute des colonnes et des index sur cette table.</span><span class="sxs-lookup"><span data-stu-id="6706e-126">Creates a table, adds columns, and indices on that table.</span></span> <span data-ttu-id="6706e-127"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID, JET_DBID, JET_TABLECREATE)</a></span><span class="sxs-lookup"><span data-stu-id="6706e-127"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</a></span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-130"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span><span class="sxs-lookup"><span data-stu-id="6706e-130"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span></span></td>
<td><span data-ttu-id="6706e-131">Obtient des informations étendues sur une erreur.</span><span class="sxs-lookup"><span data-stu-id="6706e-131">Gets extended information about an error.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-134"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span><span class="sxs-lookup"><span data-stu-id="6706e-134"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span></span></td>
<td><span data-ttu-id="6706e-135">Crée une table temporaire avec un index unique.</span><span class="sxs-lookup"><span data-stu-id="6706e-135">Creates a temporary table with a single index.</span></span> <span data-ttu-id="6706e-136">Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="6706e-136">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="6706e-137">Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile.</span><span class="sxs-lookup"><span data-stu-id="6706e-137">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="6706e-138">Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.</span><span class="sxs-lookup"><span data-stu-id="6706e-138">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="6706e-139">Consultez également <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot; API. JetOpenTempTable2 &quot; , <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span><span class="sxs-lookup"><span data-stu-id="6706e-139">Also see <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot;Api.JetOpenTempTable2&quot;, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span></span> <span data-ttu-id="6706e-140"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span><span class="sxs-lookup"><span data-stu-id="6706e-140"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-143"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span><span class="sxs-lookup"><span data-stu-id="6706e-143"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="6706e-144">Si les enregistrements avec les plages de clés spécifiées ne se trouvent pas dans le cache des tampons, lancez des lectures asynchrones pour placer les enregistrements dans le cache des tampons de la base de données.</span><span class="sxs-lookup"><span data-stu-id="6706e-144">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-147"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span><span class="sxs-lookup"><span data-stu-id="6706e-147"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span></span></td>
<td><span data-ttu-id="6706e-148">Redimensionne une base de données actuellement ouverte.</span><span class="sxs-lookup"><span data-stu-id="6706e-148">Resizes a currently open database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-151"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span><span class="sxs-lookup"><span data-stu-id="6706e-151"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span></span></td>
<td><span data-ttu-id="6706e-152">Définissez un tableau de filtres simples pour <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="6706e-152">Set an array of simple filters for <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-155"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span><span class="sxs-lookup"><span data-stu-id="6706e-155"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span></span></td>
<td><span data-ttu-id="6706e-156">Définit un paramètre sur l’état de session fourni, utilisé pour la durée de vie de cette session ou jusqu’à la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="6706e-156">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-159"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span><span class="sxs-lookup"><span data-stu-id="6706e-159"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span></span></td>
<td><span data-ttu-id="6706e-160">Prépare une instance pour l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="6706e-160">Prepares an instance for termination.</span></span> <span data-ttu-id="6706e-161">Peut également être utilisé pour reprendre une suspension précédente.</span><span class="sxs-lookup"><span data-stu-id="6706e-161">Can also be used to resume a previous quiescing.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-164"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span><span class="sxs-lookup"><span data-stu-id="6706e-164"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="6706e-165">Si les enregistrements avec les plages de clés spécifiées ne se trouvent pas dans le cache des tampons, lancez des lectures asynchrones pour placer les enregistrements dans le cache des tampons de la base de données.</span><span class="sxs-lookup"><span data-stu-id="6706e-165">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="6706e-168"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span><span class="sxs-lookup"><span data-stu-id="6706e-168"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span></span></td>
<td><span data-ttu-id="6706e-169">Si les enregistrements avec les plages de clés spécifiées ne sont pas dans le cache des tampons, démarrez les lectures asynchrones pour placer les enregistrements dans le cache des tampons de la base de données.</span><span class="sxs-lookup"><span data-stu-id="6706e-169">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6706e-170">Haut</span><span class="sxs-lookup"><span data-stu-id="6706e-170">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="6706e-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6706e-171">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6706e-172">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6706e-172">Reference</span></span>

[<span data-ttu-id="6706e-173">Windows8Api, classe</span><span class="sxs-lookup"><span data-stu-id="6706e-173">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="6706e-174">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="6706e-174">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
