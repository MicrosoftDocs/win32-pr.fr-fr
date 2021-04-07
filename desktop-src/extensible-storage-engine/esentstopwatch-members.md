---
description: 'En savoir plus sur les éléments suivants : EsentStopwatch'
title: Membres EsentStopwatch
TOCTitle: EsentStopwatch members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch_members(v=EXCHG.10)
ms:contentKeyID: 55102990
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 36f9d619e104b7d271782c3765adea744beb950e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757989"
---
# <a name="esentstopwatch-members"></a><span data-ttu-id="cdc1b-103">Membres EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="cdc1b-103">EsentStopwatch members</span></span>

<span data-ttu-id="cdc1b-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="cdc1b-104">Include protected members</span></span>  
<span data-ttu-id="cdc1b-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="cdc1b-105">Include inherited members</span></span>  

<span data-ttu-id="cdc1b-106">Fournit un ensemble de méthodes et de propriétés que vous pouvez utiliser pour mesurer les statistiques de travail ESENT d’un thread.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-106">Provides a set of methods and properties that you can use to measure ESENT work statistics for a thread.</span></span> <span data-ttu-id="cdc1b-107">Si la version actuelle de ESENT ne prend pas en charge [JetGetThreadStats (JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) , toutes les statistiques esent seront 0.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-107">If the current version of ESENT doesn't support [JetGetThreadStats(JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) then all ESENT statistics will be 0.</span></span>

<span data-ttu-id="cdc1b-108">Le type [EsentStopwatch](./esentstopwatch-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-108">The [EsentStopwatch](./esentstopwatch-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="cdc1b-109">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="cdc1b-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="cdc1b-110">Nom</span><span class="sxs-lookup"><span data-stu-id="cdc1b-110">Name</span></span></th>
<th><span data-ttu-id="cdc1b-111">Description</span><span class="sxs-lookup"><span data-stu-id="cdc1b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="cdc1b-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdc1b-114">Haut</span><span class="sxs-lookup"><span data-stu-id="cdc1b-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="cdc1b-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cdc1b-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="cdc1b-116">Nom</span><span class="sxs-lookup"><span data-stu-id="cdc1b-116">Name</span></span></th>
<th><span data-ttu-id="cdc1b-117">Description</span><span class="sxs-lookup"><span data-stu-id="cdc1b-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="cdc1b-119"><a href="dn334934(v=exchg.10).md">Temps écoulé</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-119"><a href="dn334934(v=exchg.10).md">Elapsed</a></span></span></td>
<td><span data-ttu-id="cdc1b-120">Obtient le temps total écoulé mesuré par l'instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-120">Gets the total elapsed time measured by the current instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="cdc1b-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span></span></td>
<td><span data-ttu-id="cdc1b-123">Obtient une valeur indiquant si le minuteur EsentStopwatch est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-123">Gets a value indicating whether the EsentStopwatch timer is running.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="cdc1b-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span></span></td>
<td><span data-ttu-id="cdc1b-126">Obtient le nombre total de statistiques de travail ESENT mesurées par l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-126">Gets the total ESENT work stats measured by the current instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdc1b-127">Haut</span><span class="sxs-lookup"><span data-stu-id="cdc1b-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="cdc1b-128">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cdc1b-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="cdc1b-129">Nom</span><span class="sxs-lookup"><span data-stu-id="cdc1b-129">Name</span></span></th>
<th><span data-ttu-id="cdc1b-130">Description</span><span class="sxs-lookup"><span data-stu-id="cdc1b-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="cdc1b-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="cdc1b-133">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="cdc1b-133">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="cdc1b-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="cdc1b-136">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="cdc1b-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="cdc1b-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="cdc1b-139">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="cdc1b-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="cdc1b-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="cdc1b-142">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="cdc1b-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="cdc1b-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="cdc1b-145">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="cdc1b-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="cdc1b-147"><a href="dn334869(v=exchg.10).md">Réinitialiser</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-147"><a href="dn334869(v=exchg.10).md">Reset</a></span></span></td>
<td><span data-ttu-id="cdc1b-148">Arrête la mesure de l’intervalle de temps et réinitialise les statistiques des threads.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-148">Stops time interval measurement and resets the thread statistics.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="cdc1b-150"><a href="dn334931(v=exchg.10).md">Start</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-150"><a href="dn334931(v=exchg.10).md">Start</a></span></span></td>
<td><span data-ttu-id="cdc1b-151">Commence à mesurer le travail ESENT.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-151">Starts measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="cdc1b-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span></span></td>
<td><span data-ttu-id="cdc1b-155">Initialise une nouvelle instance EsentStopwatch et commence à mesurer le temps écoulé.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-155">Initializes a new EsentStopwatch instance and starts measuring elapsed time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="cdc1b-157"><a href="dn334932(v=exchg.10).md">Stop</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-157"><a href="dn334932(v=exchg.10).md">Stop</a></span></span></td>
<td><span data-ttu-id="cdc1b-158">Arrête la mesure du travail ESENT.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-158">Stops measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="cdc1b-160"><a href="dn334873(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="cdc1b-160"><a href="dn334873(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="cdc1b-161">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="/dotnet/api/system.diagnostics.stopwatch">chronomètre</a>en cours.</span><span class="sxs-lookup"><span data-stu-id="cdc1b-161">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="/dotnet/api/system.diagnostics.stopwatch">Stopwatch</a>.</span></span> <span data-ttu-id="cdc1b-162">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="cdc1b-162">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdc1b-163">Haut</span><span class="sxs-lookup"><span data-stu-id="cdc1b-163">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="cdc1b-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdc1b-164">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cdc1b-165">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="cdc1b-165">Reference</span></span>

[<span data-ttu-id="cdc1b-166">EsentStopwatch, classe</span><span class="sxs-lookup"><span data-stu-id="cdc1b-166">EsentStopwatch class</span></span>](./esentstopwatch-class.md)

[<span data-ttu-id="cdc1b-167">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cdc1b-167">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
