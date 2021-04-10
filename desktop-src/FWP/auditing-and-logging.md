---
title: Audit
description: La plateforme de filtrage Windows (WFP) permet d’auditer les événements liés aux pare-feu et IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "103941533"
---
# <a name="auditing"></a><span data-ttu-id="b7bc6-103">Audit</span><span class="sxs-lookup"><span data-stu-id="b7bc6-103">Auditing</span></span>

<span data-ttu-id="b7bc6-104">La plateforme de filtrage Windows (WFP) permet d’auditer les événements liés au pare-feu et à IPsec.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-104">The Windows Filtering Platform (WFP) provides auditing of firewall and IPsec related events.</span></span> <span data-ttu-id="b7bc6-105">Ces événements sont stockés dans le journal de sécurité système.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-105">These events are stored in the system security log.</span></span>

<span data-ttu-id="b7bc6-106">Les événements audités sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-106">The audited events are as follows.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7bc6-107">Catégorie d’audit</span><span class="sxs-lookup"><span data-stu-id="b7bc6-107">Auditing category</span></span></th>
<th><span data-ttu-id="b7bc6-108">Sous-catégorie d’audit</span><span class="sxs-lookup"><span data-stu-id="b7bc6-108">Auditing subcategory</span></span></th>
<th><span data-ttu-id="b7bc6-109">Événements audités</span><span class="sxs-lookup"><span data-stu-id="b7bc6-109">Audited events</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7bc6-110">Modification de stratégie</span><span class="sxs-lookup"><span data-stu-id="b7bc6-110">Policy Change</span></span><br/> <span data-ttu-id="b7bc6-111">{6997984D-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-111">{6997984D-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="b7bc6-112">Filtrage de la modification de stratégie de plateforme</span><span class="sxs-lookup"><span data-stu-id="b7bc6-112">Filtering Platform Policy Change</span></span><br/> <span data-ttu-id="b7bc6-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="b7bc6-114">Les nombres représentent les ID d’événements tels qu’ils sont affichés par observateur d’événements (eventvwr.exe).</span><span class="sxs-lookup"><span data-stu-id="b7bc6-114">The numbers represent the Event IDs as displayed by Event Viewer (eventvwr.exe).</span></span>
</blockquote>
<br/> <span data-ttu-id="b7bc6-115">Ajout et suppression d’objets WFP :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-115">WFP object addition and removal:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc6-116">légende persistante 5440 ajoutée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-116">5440 Persistent callout added</span></span></li>
<li><span data-ttu-id="b7bc6-117">5441-temps de démarrage ou filtre persistant ajouté</span><span class="sxs-lookup"><span data-stu-id="b7bc6-117">5441 Boot-time or persistent filter added</span></span></li>
<li><span data-ttu-id="b7bc6-118">5442 fournisseur persistant ajouté</span><span class="sxs-lookup"><span data-stu-id="b7bc6-118">5442 Persistent provider added</span></span></li>
<li><span data-ttu-id="b7bc6-119">5443 contexte du fournisseur persistant ajouté</span><span class="sxs-lookup"><span data-stu-id="b7bc6-119">5443 Persistent provider context added</span></span></li>
<li><span data-ttu-id="b7bc6-120">5444 sous-couche persistante ajoutée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-120">5444 Persistent sub-layer added</span></span></li>
<li><span data-ttu-id="b7bc6-121">5446 ajout ou suppression d’un appel au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="b7bc6-121">5446 Run-time callout added or removed</span></span></li>
<li><span data-ttu-id="b7bc6-122">5447 filtre au moment de l’exécution ajouté ou supprimé</span><span class="sxs-lookup"><span data-stu-id="b7bc6-122">5447 Run-time filter added or removed</span></span></li>
<li><span data-ttu-id="b7bc6-123">5448 fournisseur d’exécution ajouté ou supprimé</span><span class="sxs-lookup"><span data-stu-id="b7bc6-123">5448 Run-time provider added or removed</span></span></li>
<li><span data-ttu-id="b7bc6-124">5449 contexte du fournisseur au moment de l’exécution ajouté ou supprimé</span><span class="sxs-lookup"><span data-stu-id="b7bc6-124">5449 Run-time provider context added or removed</span></span></li>
<li><span data-ttu-id="b7bc6-125">sous-couche d’exécution 5450 ajoutée ou supprimée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-125">5450 Run-time sub-layer added or removed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc6-126">Accès aux objets</span><span class="sxs-lookup"><span data-stu-id="b7bc6-126">Object Access</span></span><br/> <span data-ttu-id="b7bc6-127">{6997984A-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-127">{6997984A-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="b7bc6-128">Filtrage de la suppression de paquets de plateforme</span><span class="sxs-lookup"><span data-stu-id="b7bc6-128">Filtering Platform Packet Drop</span></span> <br/> <span data-ttu-id="b7bc6-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="b7bc6-130">Paquets supprimés par WFP :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-130">Packets dropped by WFP:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc6-131">paquet 5152 abandonné</span><span class="sxs-lookup"><span data-stu-id="b7bc6-131">5152 Packet dropped</span></span></li>
<li><span data-ttu-id="b7bc6-132">5153 paquet refusé</span><span class="sxs-lookup"><span data-stu-id="b7bc6-132">5153 Packet vetoed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc6-133">Accès aux objets</span><span class="sxs-lookup"><span data-stu-id="b7bc6-133">Object Access</span></span><br/></td>
<td><span data-ttu-id="b7bc6-134">Filtrage de la connexion de plateforme</span><span class="sxs-lookup"><span data-stu-id="b7bc6-134">Filtering Platform Connection</span></span> <br/> <span data-ttu-id="b7bc6-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="b7bc6-136">Connexions autorisées et bloquées :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-136">Allowed and blocked connections:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc6-137">5154 écoute autorisée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-137">5154 Listen permitted</span></span></li>
<li><span data-ttu-id="b7bc6-138">5155 écoute bloquée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-138">5155 Listen blocked</span></span></li>
<li><span data-ttu-id="b7bc6-139">5156 connexion autorisée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-139">5156 Connection permitted</span></span></li>
<li><span data-ttu-id="b7bc6-140">5157 connexion bloquée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-140">5157 Connection blocked</span></span></li>
<li><span data-ttu-id="b7bc6-141">5158 liaison autorisée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-141">5158 Bind permitted</span></span></li>
<li><span data-ttu-id="b7bc6-142">liaison 5159 bloquée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-142">5159 Bind blocked</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="b7bc6-143">Les connexions autorisées n’auditent pas toujours l’ID du filtre associé.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-143">Permitted connections do not always audit the ID of the associated filter.</span></span> <span data-ttu-id="b7bc6-144">Le FilterID pour TCP sera égal à 0, sauf si un sous-ensemble de ces conditions de filtrage est utilisé : UserID, AppID, Protocol, port distant.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-144">The FilterID for TCP will be 0 unless a subset of these filtering conditions are used: UserID, AppID, Protocol, Remote Port.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc6-145">Accès aux objets</span><span class="sxs-lookup"><span data-stu-id="b7bc6-145">Object Access</span></span><br/></td>
<td><span data-ttu-id="b7bc6-146">Autres événements d’accès aux objets</span><span class="sxs-lookup"><span data-stu-id="b7bc6-146">Other Object Access Events</span></span><br/> <span data-ttu-id="b7bc6-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="b7bc6-148">Cette sous-catégorie active un grand nombre d’audits.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-148">This subcategory enables many audits.</span></span> <span data-ttu-id="b7bc6-149">Les audits spécifiques à WFP sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-149">WFP specific audits are listed below.</span></span>
</blockquote>
<br/> <span data-ttu-id="b7bc6-150">État de prévention du déni de service :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-150">Denial of Service prevention status:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc6-151">5148 mode de prévention DoS WFP démarré</span><span class="sxs-lookup"><span data-stu-id="b7bc6-151">5148 WFP DoS prevention mode started</span></span></li>
<li><span data-ttu-id="b7bc6-152">5149 mode de prévention DoS WFP arrêté</span><span class="sxs-lookup"><span data-stu-id="b7bc6-152">5149 WFP DoS prevention mode stopped</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc6-153">Ouverture/fermeture de session</span><span class="sxs-lookup"><span data-stu-id="b7bc6-153">Logon/Logoff</span></span><br/> <span data-ttu-id="b7bc6-154">{69979849-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-154">{69979849-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="b7bc6-155">Mode principal IPsec</span><span class="sxs-lookup"><span data-stu-id="b7bc6-155">IPsec Main Mode</span></span><br/> <span data-ttu-id="b7bc6-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="b7bc6-157">Négociation en mode principal IKE et AuthIP :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-157">IKE and AuthIP Main Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc6-158">4650, 4651 Association de sécurité établie</span><span class="sxs-lookup"><span data-stu-id="b7bc6-158">4650, 4651 Security association established</span></span></li>
<li><span data-ttu-id="b7bc6-159">4652, échec de la négociation 4653</span><span class="sxs-lookup"><span data-stu-id="b7bc6-159">4652, 4653 Negotiation failed</span></span></li>
<li><span data-ttu-id="b7bc6-160">4655 Association de sécurité terminée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-160">4655 Security association ended</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc6-161">Ouverture/fermeture de session</span><span class="sxs-lookup"><span data-stu-id="b7bc6-161">Logon/Logoff</span></span><br/></td>
<td><span data-ttu-id="b7bc6-162">Mode rapide IPsec</span><span class="sxs-lookup"><span data-stu-id="b7bc6-162">IPsec Quick Mode</span></span> <br/> <span data-ttu-id="b7bc6-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="b7bc6-164">Négociation en mode rapide IKE et AuthIP :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-164">IKE and AuthIP Quick Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc6-165">5451 Association de sécurité établie</span><span class="sxs-lookup"><span data-stu-id="b7bc6-165">5451 Security association established</span></span></li>
<li><span data-ttu-id="b7bc6-166">5452 Association de sécurité terminée</span><span class="sxs-lookup"><span data-stu-id="b7bc6-166">5452 Security association ended</span></span></li>
<li><span data-ttu-id="b7bc6-167">échec de la négociation 4654</span><span class="sxs-lookup"><span data-stu-id="b7bc6-167">4654 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc6-168">Ouverture/fermeture de session</span><span class="sxs-lookup"><span data-stu-id="b7bc6-168">Logon/Logoff</span></span> <br/></td>
<td><span data-ttu-id="b7bc6-169">Mode étendu IPsec</span><span class="sxs-lookup"><span data-stu-id="b7bc6-169">IPsec Extended Mode</span></span><br/> <span data-ttu-id="b7bc6-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="b7bc6-171">Négociation en mode étendu AuthIP :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-171">AuthIP Extended Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc6-172">4978 paquet de négociation non valide</span><span class="sxs-lookup"><span data-stu-id="b7bc6-172">4978 Invalid negotiation packet</span></span></li>
<li><span data-ttu-id="b7bc6-173">4979, 4980, 4981, 4982 Association de sécurité établie</span><span class="sxs-lookup"><span data-stu-id="b7bc6-173">4979, 4980, 4981, 4982 Security association established</span></span></li>
<li><span data-ttu-id="b7bc6-174">4983, échec de la négociation 4984</span><span class="sxs-lookup"><span data-stu-id="b7bc6-174">4983, 4984 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc6-175">Système</span><span class="sxs-lookup"><span data-stu-id="b7bc6-175">System</span></span><br/> <span data-ttu-id="b7bc6-176">{69979848-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-176">{69979848-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="b7bc6-177">Pilote IPsec</span><span class="sxs-lookup"><span data-stu-id="b7bc6-177">IPsec Driver</span></span><br/> <span data-ttu-id="b7bc6-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="b7bc6-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="b7bc6-179">Paquets ignorés par le pilote IPsec :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-179">Packets dropped by the IPsec driver:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc6-180">4963 paquet de texte en clair entrant supprimé</span><span class="sxs-lookup"><span data-stu-id="b7bc6-180">4963 Inbound clear text packet dropped</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b7bc6-181">Par défaut, l’audit pour WFP est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-181">By default, auditing for WFP is disabled.</span></span>

<span data-ttu-id="b7bc6-182">L’audit peut être activé par catégorie par le biais du composant logiciel enfichable MMC de l’éditeur d’objets stratégie de groupe, du composant logiciel enfichable MMC stratégie de sécurité locale ou de la commande auditpol.exe.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-182">Auditing can be enabled on a per-category basis through either the Group Policy Object Editor MMC snap-in, the Local Security Policy MMC snap-in, or the auditpol.exe command.</span></span>

<span data-ttu-id="b7bc6-183">Par exemple, pour activer l’audit des événements de modification de stratégie, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-183">For example, to enable the auditing of Policy Change events you may:</span></span>

-   <span data-ttu-id="b7bc6-184">Utiliser l’éditeur d’objets stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b7bc6-184">Use the Group Policy Object Editor</span></span>

    1.  <span data-ttu-id="b7bc6-185">Exécutez **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-185">Run **gpedit.msc**.</span></span>
    2.  <span data-ttu-id="b7bc6-186">Développez stratégie de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-186">Expand Local Computer Policy.</span></span>
    3.  <span data-ttu-id="b7bc6-187">Développez Configuration de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-187">Expand Computer Configuration.</span></span>
    4.  <span data-ttu-id="b7bc6-188">Développez Paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-188">Expand Windows Settings.</span></span>
    5.  <span data-ttu-id="b7bc6-189">Développez Paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-189">Expand Security Settings.</span></span>
    6.  <span data-ttu-id="b7bc6-190">Développez Stratégies locales.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-190">Expand Local Policies.</span></span>
    7.  <span data-ttu-id="b7bc6-191">Cliquez sur stratégie d’audit.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-191">Click Audit Policy.</span></span>
    8.  <span data-ttu-id="b7bc6-192">Double-cliquez sur auditer la modification de la stratégie pour lancer la boîte de dialogue Propriétés.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-192">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    9.  <span data-ttu-id="b7bc6-193">Consultez les cases à cocher réussite et échec.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-193">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="b7bc6-194">Utiliser la stratégie de sécurité locale</span><span class="sxs-lookup"><span data-stu-id="b7bc6-194">Use the Local Security Policy</span></span>

    1.  <span data-ttu-id="b7bc6-195">Exécutez **secpol. msc**.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-195">Run **secpol.msc**.</span></span>
    2.  <span data-ttu-id="b7bc6-196">Développez Stratégies locales.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-196">Expand Local Policies.</span></span>
    3.  <span data-ttu-id="b7bc6-197">Cliquez sur stratégie d’audit.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-197">Click Audit Policy.</span></span>
    4.  <span data-ttu-id="b7bc6-198">Double-cliquez sur auditer la modification de la stratégie pour lancer la boîte de dialogue Propriétés.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-198">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    5.  <span data-ttu-id="b7bc6-199">Consultez les cases à cocher réussite et échec.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-199">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="b7bc6-200">Utilisez la commande auditpol.exe</span><span class="sxs-lookup"><span data-stu-id="b7bc6-200">Use the auditpol.exe command</span></span>

    -   <span data-ttu-id="b7bc6-201">**Auditpol/Set/Category : « modification de la stratégie »/Success : Enable/Failure : Enable**</span><span class="sxs-lookup"><span data-stu-id="b7bc6-201">**auditpol /set /category:"Policy Change" /success:enable /failure:enable**</span></span>

<span data-ttu-id="b7bc6-202">L’audit peut être activé sur une base par sous-catégorie uniquement par le biais de la commande auditpol.exe.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-202">Auditing can be enabled on a per-subcategory basis only through the auditpol.exe command.</span></span>

<span data-ttu-id="b7bc6-203">Les noms de catégorie et de sous-catégorie d’audit sont localisés.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-203">The auditing category and subcategory names are localized.</span></span> <span data-ttu-id="b7bc6-204">Pour éviter la localisation des scripts d’audit, les GUID correspondants peuvent être utilisés à la place des noms.</span><span class="sxs-lookup"><span data-stu-id="b7bc6-204">To avoid localization for auditing scripts, the corresponding GUIDs may be used in place of the names.</span></span>

<span data-ttu-id="b7bc6-205">Par exemple, pour activer l’audit des événements de modification de stratégie de plateforme de filtrage, vous pouvez utiliser l’une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7bc6-205">For example, to enable the auditing of Filtering Platform Policy Change events you may use either one of the following commands:</span></span>

-   <span data-ttu-id="b7bc6-206">**Auditpol/Set/Subcategory : « filtrage de la stratégie de plateforme de filtrage »/Success : Enable/Failure : Enable**</span><span class="sxs-lookup"><span data-stu-id="b7bc6-206">**auditpol /set /subcategory:"Filtering Platform Policy Change" /success:enable /failure:enable**</span></span>
-   <span data-ttu-id="b7bc6-207">**Auditpol/Set/Subcategory : « {0CCE9233-69AE-11D9-BED3-505054503030} »/Success : Enable/Failure : Enable**</span><span class="sxs-lookup"><span data-stu-id="b7bc6-207">**auditpol /set /subcategory:"{0CCE9233-69AE-11D9-BED3-505054503030}" /success:enable /failure:enable**</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7bc6-208">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7bc6-208">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b7bc6-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="b7bc6-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="b7bc6-210">[Journal des événements](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b7bc6-210">[Event Log](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="b7bc6-211">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b7bc6-211">Group Policy</span></span>](/windows/deployment/deploy-whats-new)
</dt> </dl>

