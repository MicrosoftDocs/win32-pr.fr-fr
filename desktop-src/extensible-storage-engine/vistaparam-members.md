---
description: 'En savoir plus sur les éléments suivants : VistaParam'
title: Membres VistaParam (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: VistaParam members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_members(v=EXCHG.10)
ms:contentKeyID: 55104333
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c56c8ad3a64eb08654ee893e86683e95e32af443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861929"
---
# <a name="vistaparam-members"></a><span data-ttu-id="a1a07-103">Membres VistaParam</span><span class="sxs-lookup"><span data-stu-id="a1a07-103">VistaParam members</span></span>

<span data-ttu-id="a1a07-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="a1a07-104">Include protected members</span></span>  
<span data-ttu-id="a1a07-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="a1a07-105">Include inherited members</span></span>  

<span data-ttu-id="a1a07-106">Paramètres système qui ont été ajoutés à la version Vista d’ESENT.</span><span class="sxs-lookup"><span data-stu-id="a1a07-106">System parameters that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="a1a07-107">Le type [VistaParam](./vistaparam-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="a1a07-107">The [VistaParam](./vistaparam-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="a1a07-108">Champs</span><span class="sxs-lookup"><span data-stu-id="a1a07-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a1a07-109">Nom</span><span class="sxs-lookup"><span data-stu-id="a1a07-109">Name</span></span></th>
<th><span data-ttu-id="a1a07-110">Description</span><span class="sxs-lookup"><span data-stu-id="a1a07-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-113"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-113"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="a1a07-114">Ce paramètre contrôle le nombre de ressources de l’arborescence B + mises en cache par l’instance une fois que les tables qu’elles représentent ont été fermées par l’application.</span><span class="sxs-lookup"><span data-stu-id="a1a07-114">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="a1a07-115">Des valeurs élevées pour ce paramètre forcent le moteur de base de données à utiliser plus de mémoire, mais augmentent la vitesse avec laquelle un grand nombre de tables peut être ouvert de façon aléatoire par l’application.</span><span class="sxs-lookup"><span data-stu-id="a1a07-115">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="a1a07-116">Cela est utile pour les applications qui ont un schéma avec un très grand nombre de tables.</span><span class="sxs-lookup"><span data-stu-id="a1a07-116">This is useful for applications that have a schema with a very large number of tables.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-119"><a href="dn335289(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-119"><a href="dn335289(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="a1a07-120">Ce paramètre expose plusieurs jeux de valeurs par défaut pour l’ensemble des paramètres système.</span><span class="sxs-lookup"><span data-stu-id="a1a07-120">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="a1a07-121">Quand ce paramètre est défini sur une configuration spécifique, toutes les valeurs des paramètres système sont réinitialisées à leurs valeurs par défaut pour cette configuration.</span><span class="sxs-lookup"><span data-stu-id="a1a07-121">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="a1a07-122">Si la configuration est définie pour une instance spécifique, les valeurs par défaut des paramètres système globaux ne sont pas réinitialisées.</span><span class="sxs-lookup"><span data-stu-id="a1a07-122">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="a1a07-123">Petite configuration (0) : le moteur de base de données est optimisé pour l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="a1a07-123">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="a1a07-124">Configuration héritée (1) : le moteur de base de données a ses valeurs par défaut traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="a1a07-124">Legacy Configuration (1): The database engine has its traditional defaults.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-127"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-127"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="a1a07-128">Ce paramètre est utilisé pour contrôler le moment où le moteur de base de données accepte ou rejette les modifications apportées à un sous-ensemble des paramètres système.</span><span class="sxs-lookup"><span data-stu-id="a1a07-128">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="a1a07-129">Ce paramètre est utilisé conjointement avec la <a href="dn335289(v=exchg.10).md">configuration</a> pour empêcher la définition de certains paramètres système à partir des valeurs par défaut de la configuration sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a1a07-129">This parameter is used in conjunction with <a href="dn335289(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-132"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-132"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="a1a07-133">Activez l’utilisation du cache de fichiers du système d’exploitation pour tous les fichiers gérés.</span><span class="sxs-lookup"><span data-stu-id="a1a07-133">Enable the use of the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-136"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-136"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="a1a07-137">Activez l’utilisation des e/s de fichier mappées en mémoire pour les fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="a1a07-137">Enable the use of memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-140"><a href="dn335292(v=exchg.10).md">La plupart des</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-140"><a href="dn335292(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="a1a07-141">Ce paramètre en lecture seule indique la longueur de clé d’index maximale autorisée qui peut être sélectionnée pour la taille de page de la base de données actuelle (telle que configurée par <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="a1a07-141">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-144"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-144"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="a1a07-145">Ce paramètre offre une compatibilité descendante avec les conventions d’affectation des noms de fichiers des versions antérieures du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="a1a07-145">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-148"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-148"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span></span></td>
<td><span data-ttu-id="a1a07-149">Définissez le nom associé à la classe de table 10.</span><span class="sxs-lookup"><span data-stu-id="a1a07-149">Set the name associated with table class 10.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-152"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-152"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span></span></td>
<td><span data-ttu-id="a1a07-153">Définissez le nom associé à la classe de table 11.</span><span class="sxs-lookup"><span data-stu-id="a1a07-153">Set the name associated with table class 11.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-156"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-156"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span></span></td>
<td><span data-ttu-id="a1a07-157">Définissez le nom associé à la classe de table 12.</span><span class="sxs-lookup"><span data-stu-id="a1a07-157">Set the name associated with table class 12.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-160"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-160"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span></span></td>
<td><span data-ttu-id="a1a07-161">Définissez le nom associé à la classe de table 13.</span><span class="sxs-lookup"><span data-stu-id="a1a07-161">Set the name associated with table class 13.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-164"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-164"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span></span></td>
<td><span data-ttu-id="a1a07-165">Définissez le nom associé à la classe de table 14.</span><span class="sxs-lookup"><span data-stu-id="a1a07-165">Set the name associated with table class 14.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-168"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-168"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span></span></td>
<td><span data-ttu-id="a1a07-169">Définissez le nom associé à la classe de table 15.</span><span class="sxs-lookup"><span data-stu-id="a1a07-169">Set the name associated with table class 15.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-172"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-172"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span></span></td>
<td><span data-ttu-id="a1a07-173">Définissez le nom associé à la classe de table 1.</span><span class="sxs-lookup"><span data-stu-id="a1a07-173">Set the name associated with table class 1.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-176"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-176"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span></span></td>
<td><span data-ttu-id="a1a07-177">Définissez le nom associé à la classe de table 2.</span><span class="sxs-lookup"><span data-stu-id="a1a07-177">Set the name associated with table class 2.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-180"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-180"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span></span></td>
<td><span data-ttu-id="a1a07-181">Définissez le nom associé à la classe de table 3.</span><span class="sxs-lookup"><span data-stu-id="a1a07-181">Set the name associated with table class 3.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-184"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-184"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span></span></td>
<td><span data-ttu-id="a1a07-185">Définissez le nom associé à la classe de table 4.</span><span class="sxs-lookup"><span data-stu-id="a1a07-185">Set the name associated with table class 4.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-188"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-188"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span></span></td>
<td><span data-ttu-id="a1a07-189">Définissez le nom associé à la classe de table 5.</span><span class="sxs-lookup"><span data-stu-id="a1a07-189">Set the name associated with table class 5.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-192"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-192"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span></span></td>
<td><span data-ttu-id="a1a07-193">Définissez le nom associé à la classe de table 6.</span><span class="sxs-lookup"><span data-stu-id="a1a07-193">Set the name associated with table class 6.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-196"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-196"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span></span></td>
<td><span data-ttu-id="a1a07-197">Définissez le nom associé à la classe de table 7.</span><span class="sxs-lookup"><span data-stu-id="a1a07-197">Set the name associated with table class 7.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-200"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-200"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span></span></td>
<td><span data-ttu-id="a1a07-201">Définissez le nom associé à la classe de table 8.</span><span class="sxs-lookup"><span data-stu-id="a1a07-201">Set the name associated with table class 8.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="a1a07-204"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span><span class="sxs-lookup"><span data-stu-id="a1a07-204"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span></span></td>
<td><span data-ttu-id="a1a07-205">Définissez le nom associé à la classe de table 9.</span><span class="sxs-lookup"><span data-stu-id="a1a07-205">Set the name associated with table class 9.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1a07-206">Haut</span><span class="sxs-lookup"><span data-stu-id="a1a07-206">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a1a07-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1a07-207">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a1a07-208">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a1a07-208">Reference</span></span>

[<span data-ttu-id="a1a07-209">VistaParam, classe</span><span class="sxs-lookup"><span data-stu-id="a1a07-209">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="a1a07-210">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="a1a07-210">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
