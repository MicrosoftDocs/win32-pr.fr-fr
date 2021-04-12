---
description: 'En savoir plus sur : énumération JET_ERRCAT'
title: Énumération JET_ERRCAT (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203146"
---
# <a name="jet_errcat-enumeration"></a><span data-ttu-id="82bf2-103">Énumération JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="82bf2-103">JET_ERRCAT enumeration</span></span>

<span data-ttu-id="82bf2-104">Catégorie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="82bf2-104">The error category.</span></span> <span data-ttu-id="82bf2-105">La hiérarchie est la suivante : JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//problèmes d’e/s incorrects, peuvent être temporaires ou non.</span><span class="sxs-lookup"><span data-stu-id="82bf2-105">The hierarchy is as follows: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // bad IO issues, may or may not be transient.</span></span> <span data-ttu-id="82bf2-106">| |--JET_errcatResource | |--JET_errcatMemory//mémoire insuffisante (toutes les variantes) | |--JET_errcatQuota | |--JET_errcatDisk//espace disque insuffisant (toutes les variantes) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//est généralement dû à une mauvaise utilisation de l’utilisateur | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete</span><span class="sxs-lookup"><span data-stu-id="82bf2-106">| |-- JET_errcatResource | |-- JET_errcatMemory // out of memory (all variants) | |-- JET_errcatQuota | |-- JET_errcatDisk // out of disk space (all variants) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // typically caused by user Mishandling | |-- JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete</span></span>

<span data-ttu-id="82bf2-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82bf2-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="82bf2-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82bf2-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82bf2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82bf2-109">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a><span data-ttu-id="82bf2-110">Membres</span><span class="sxs-lookup"><span data-stu-id="82bf2-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="82bf2-111">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="82bf2-111">Member name</span></span></th>
<th><span data-ttu-id="82bf2-112">Description</span><span class="sxs-lookup"><span data-stu-id="82bf2-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82bf2-113">Unknown</span><span class="sxs-lookup"><span data-stu-id="82bf2-113">Unknown</span></span></td>
<td><span data-ttu-id="82bf2-114">Catégorie inconnue.</span><span class="sxs-lookup"><span data-stu-id="82bf2-114">Unknown category.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82bf2-115">Error</span><span class="sxs-lookup"><span data-stu-id="82bf2-115">Error</span></span></td>
<td><span data-ttu-id="82bf2-116">Catégorie générique.</span><span class="sxs-lookup"><span data-stu-id="82bf2-116">A generic category.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82bf2-117">Opération</span><span class="sxs-lookup"><span data-stu-id="82bf2-117">Operation</span></span></td>
<td><span data-ttu-id="82bf2-118">Erreurs qui peuvent généralement se produire à tout moment en raison de conditions incontrôlables.</span><span class="sxs-lookup"><span data-stu-id="82bf2-118">Errors that can usually happen any time due to uncontrollable conditions.</span></span> <span data-ttu-id="82bf2-119">Souvent temporaire, mais pas toujours.</span><span class="sxs-lookup"><span data-stu-id="82bf2-119">Frequently temporary, but not always.</span></span> <span data-ttu-id="82bf2-120">Récupération : réessayez probablement ou Informez l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="82bf2-120">Recovery: Probably retry, or eventually inform the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82bf2-121">Erreur irrécupérable</span><span class="sxs-lookup"><span data-stu-id="82bf2-121">Fatal</span></span></td>
<td><span data-ttu-id="82bf2-122">Cette erreur de tri se produit uniquement lorsque le moteur ESE rencontre une condition d’erreur trop grave, que nous ne pouvons pas continuer dans une méthode sécurisée (souvent transactionnelle) et plutôt que des données endommagées. nous générons des erreurs de cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="82bf2-122">This sort error happens only when ESE encounters an error condition so grave, that we can not continue on in a safe (often transactional) way, and rather than corrupt data we throw errors of this category.</span></span> <span data-ttu-id="82bf2-123">Récupération : redémarrez l’instance ou le processus.</span><span class="sxs-lookup"><span data-stu-id="82bf2-123">Recovery: Restart the instance or process.</span></span> <span data-ttu-id="82bf2-124">Si le problème persiste, Informez l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="82bf2-124">If the problem persists inform the operator.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82bf2-125">IO</span><span class="sxs-lookup"><span data-stu-id="82bf2-125">IO</span></span></td>
<td><span data-ttu-id="82bf2-126">O des erreurs proviennent du système d’exploitation et sont hors du contrôle ESE, ce type d’erreur est peut-être temporaire.</span><span class="sxs-lookup"><span data-stu-id="82bf2-126">O errors come from the OS, and are out of ESE's control, this sort of error is possibly temporary, possibly not.</span></span> <span data-ttu-id="82bf2-127">Récupération : nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="82bf2-127">Recovery: Retry.</span></span> <span data-ttu-id="82bf2-128">Si elle n’est pas résolue, demandez à l’opérateur à propos du problème de disque.</span><span class="sxs-lookup"><span data-stu-id="82bf2-128">If not resolved, ask operator about disk issue.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82bf2-129">Ressource</span><span class="sxs-lookup"><span data-stu-id="82bf2-129">Resource</span></span></td>
<td><span data-ttu-id="82bf2-130">Il s’agit d’une catégorie qui indique l’une des nombreuses conditions d’insuffisance de ressources potentielles.</span><span class="sxs-lookup"><span data-stu-id="82bf2-130">This is a category that indicates one of many potential out-of-resource conditions.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82bf2-131">Mémoire</span><span class="sxs-lookup"><span data-stu-id="82bf2-131">Memory</span></span></td>
<td><span data-ttu-id="82bf2-132">Condition de mémoire insuffisante classique.</span><span class="sxs-lookup"><span data-stu-id="82bf2-132">Classic out of memory condition.</span></span> <span data-ttu-id="82bf2-133">Récupération : attendez un moment et réessayez, libérez de la mémoire ou quittez.</span><span class="sxs-lookup"><span data-stu-id="82bf2-133">Recovery: Wait a while and retry, free up memory, or quit.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82bf2-134">Quota</span><span class="sxs-lookup"><span data-stu-id="82bf2-134">Quota</span></span></td>
<td><span data-ttu-id="82bf2-135">Certaines &quot; &quot; ressources spécialisées se trouvent dans des pools d’une certaine taille, ce qui facilite la détection des fuites de ces ressources.</span><span class="sxs-lookup"><span data-stu-id="82bf2-135">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span> <span data-ttu-id="82bf2-136">Récupération : peut nécessiter des modifications de code mineures.</span><span class="sxs-lookup"><span data-stu-id="82bf2-136">Recovery: Might require some minor code changes.</span></span> <span data-ttu-id="82bf2-137">Votre application doit avoir une action de débogage uniquement, telle qu’une assertion, sur ces conditions afin de les détecter pendant le développement.</span><span class="sxs-lookup"><span data-stu-id="82bf2-137">Your application should have a debug only action, such as an Assert, on these conditions in order to detect them during development.</span></span> <span data-ttu-id="82bf2-138">Pour le code de vente au détail, nous vous recommandons de traiter cette erreur comme une erreur de catégorie mémoire et de réessayer, de libérer de la mémoire ou de quitter l’opération.</span><span class="sxs-lookup"><span data-stu-id="82bf2-138">For retail code, we recommend that you treat this error like the Memory category error and either retry, free up memory, or quit the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82bf2-139">Disque</span><span class="sxs-lookup"><span data-stu-id="82bf2-139">Disk</span></span></td>
<td><span data-ttu-id="82bf2-140">Conditions de disque insuffisant.</span><span class="sxs-lookup"><span data-stu-id="82bf2-140">Out of disk conditions.</span></span> <span data-ttu-id="82bf2-141">Récupération : peut réessayer plus tard dans l’espoir que de l’espace est disponible, ou demander à l’opérateur de libérer de l’espace disque.</span><span class="sxs-lookup"><span data-stu-id="82bf2-141">Recovery: Can retry later in the hope more space is available, or ask the operator to free some disk space.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82bf2-142">Données</span><span class="sxs-lookup"><span data-stu-id="82bf2-142">Data</span></span></td>
<td><span data-ttu-id="82bf2-143">Erreur liée aux données.</span><span class="sxs-lookup"><span data-stu-id="82bf2-143">A data-related error.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82bf2-144">Altération</span><span class="sxs-lookup"><span data-stu-id="82bf2-144">Corruption</span></span></td>
<td><span data-ttu-id="82bf2-145">Mon disque dur est à la maison.</span><span class="sxs-lookup"><span data-stu-id="82bf2-145">My hard drive ate my homework.</span></span> <span data-ttu-id="82bf2-146">Problèmes d’altération classiques, souvent permanents sans action corrective.</span><span class="sxs-lookup"><span data-stu-id="82bf2-146">Classic corruption issues, frequently permanent without corrective action.</span></span> <span data-ttu-id="82bf2-147">Récupération : restaurer à partir de la sauvegarde, peut-être l’opération de réparation des utilitaires ESE (qui ne restaure que les données qui sont conservées/perdues). En outre, dans le cas de la récupération (JetInit), il est possible d’effectuer une récupération en autorisant la perte de données.</span><span class="sxs-lookup"><span data-stu-id="82bf2-147">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy) .Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82bf2-148">Incohérent</span><span class="sxs-lookup"><span data-stu-id="82bf2-148">Inconsistent</span></span></td>
<td><span data-ttu-id="82bf2-149">Cela est similaire à un endommagement dans le fait que la base de données et/ou les fichiers journaux sont dans un état incohérent et non réconciliable les uns avec les autres.</span><span class="sxs-lookup"><span data-stu-id="82bf2-149">This is similar to Corruption in that the database and/or log files are in a state that is inconsistent and unreconcilable with each other.</span></span> <span data-ttu-id="82bf2-150">Cela est souvent dû à une mauvaise gestion des applications/administrateurs.</span><span class="sxs-lookup"><span data-stu-id="82bf2-150">Often this is caused by application/administrator mishandling.</span></span> <span data-ttu-id="82bf2-151">Récupération : restaurer à partir de la sauvegarde, peut-être l’opération de réparation des utilitaires ESE (qui ne restaure que les données qui sont conservées/perdues).</span><span class="sxs-lookup"><span data-stu-id="82bf2-151">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy).</span></span> <span data-ttu-id="82bf2-152">En outre, dans le cas de la récupération (JetInit), il est possible d’effectuer une récupération en autorisant la perte de données.</span><span class="sxs-lookup"><span data-stu-id="82bf2-152">Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82bf2-153">Fragmentation</span><span class="sxs-lookup"><span data-stu-id="82bf2-153">Fragmentation</span></span></td>
<td><span data-ttu-id="82bf2-154">Il s’agit d’une classe d’erreurs dans laquelle certaines ressources internes persistantes ont été exécutées. Récupération : pour les erreurs de base de données, la défragmentation hors connexion permet de corriger le problème. pour les fichiers journaux, _commencez_ par récupérer toutes les bases de données attachées à un arrêt correct, puis supprimez tous les fichiers journaux et le point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="82bf2-154">This is a class of errors where some persisted internal resource ran out. Recovery: For database errors, offline defragmentation will rectify the problem, for the log files _first_ recover all attached databases to a clean shutdown, and then delete all the log files and checkpoint.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82bf2-155">MobileVBActiveX</span><span class="sxs-lookup"><span data-stu-id="82bf2-155">Api</span></span></td>
<td><span data-ttu-id="82bf2-156">Conteneur pour l’utilisation et l’État.</span><span class="sxs-lookup"><span data-stu-id="82bf2-156">A container for Usage and State.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82bf2-157">Utilisation</span><span class="sxs-lookup"><span data-stu-id="82bf2-157">Usage</span></span></td>
<td><span data-ttu-id="82bf2-158">Erreur d’utilisation classique, ce qui signifie que le code client n’a pas transmis d’arguments corrects à l’API JET.</span><span class="sxs-lookup"><span data-stu-id="82bf2-158">Classic usage error, this means the client code did not pass correct arguments to the JET API.</span></span> <span data-ttu-id="82bf2-159">Cette erreur ne sera probablement pas déplacée avec une nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="82bf2-159">This error will likely not go away with retry.</span></span> <span data-ttu-id="82bf2-160">Récupération : en général, le code client doit déclarer () que cette classe d’erreurs n’est pas retournée, de sorte que les problèmes peuvent être détectés pendant le développement.</span><span class="sxs-lookup"><span data-stu-id="82bf2-160">Recovery: Generally speaking client code should Assert() this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="82bf2-161">Dans la version commerciale, l’application aura probablement peu d’options, mais pour retourner le problème à l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="82bf2-161">In retail, the app will probably have little option but to return the issue up to the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82bf2-162">State</span><span class="sxs-lookup"><span data-stu-id="82bf2-162">State</span></span></td>
<td><span data-ttu-id="82bf2-163">Il s’agit de la classification des différents signaux que l’API peut renvoyer décrivent l’état de la base de données, un cas classique est JET_errRecordNotFound qui peut être retourné par JetSeek () lorsque l’enregistrement que vous avez demandé n’a pas été trouvé.</span><span class="sxs-lookup"><span data-stu-id="82bf2-163">This is the classification for different signals the API could return describe the state of the database, a classic case is JET_errRecordNotFound which can be returned by JetSeek() when the record you asked for was not found.</span></span> <span data-ttu-id="82bf2-164">La récupération : pas vraiment pertinente, dépend beaucoup de l’API.</span><span class="sxs-lookup"><span data-stu-id="82bf2-164">Recovery: Not really relevant, depends greatly on the API.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="82bf2-165">Obsolète</span><span class="sxs-lookup"><span data-stu-id="82bf2-165">Obsolete</span></span></td>
<td><span data-ttu-id="82bf2-166">L’erreur est reconnue comme une erreur valide, mais elle n’est pas censée être retournée par cette version de l’API.</span><span class="sxs-lookup"><span data-stu-id="82bf2-166">The error is recognized as a valid error, but is not expected to be returned by this version of the API.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="82bf2-167">Max</span><span class="sxs-lookup"><span data-stu-id="82bf2-167">Max</span></span></td>
<td><span data-ttu-id="82bf2-168">Valeur maximale de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="82bf2-168">The maximum value for the enum.</span></span> <span data-ttu-id="82bf2-169">Cela ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="82bf2-169">This should not be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="82bf2-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82bf2-170">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82bf2-171">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="82bf2-171">Reference</span></span>

[<span data-ttu-id="82bf2-172">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="82bf2-172">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
