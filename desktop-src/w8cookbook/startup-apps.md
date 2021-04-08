---
title: Applications de démarrage
description: Applications de démarrage
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- application de démarrage
- tâche en arrière-plan
- Exécuter la clé
- RunOnce
- dossier de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734629"
---
# <a name="startup-apps"></a><span data-ttu-id="82722-108">Applications de démarrage</span><span class="sxs-lookup"><span data-stu-id="82722-108">Startup apps</span></span>

## <a name="platform"></a><span data-ttu-id="82722-109">Plateforme</span><span class="sxs-lookup"><span data-stu-id="82722-109">Platform</span></span>

<span data-ttu-id="82722-110">**Clients**   Windows 8</span><span class="sxs-lookup"><span data-stu-id="82722-110">**Clients**   Windows 8</span></span>  


## <a name="description"></a><span data-ttu-id="82722-111">Description</span><span class="sxs-lookup"><span data-stu-id="82722-111">Description</span></span>

<span data-ttu-id="82722-112">L’un des grands résultats de Windows est la capacité à illuminer différents facteurs de forme, des ordinateurs de bureau traditionnels et des ordinateurs portables aux tablettes de faible puissance.</span><span class="sxs-lookup"><span data-stu-id="82722-112">One of the big bets with Windows is the ability to light up various form factors, from the traditional desktops and laptops to low-powered tablets.</span></span> <span data-ttu-id="82722-113">Pour s’assurer que nos clients mutuels bénéficient d’une expérience remarquable sur n’importe quel facteur de forme qu’ils choisissent avec Windows, deux mesures de réussite clés qui doivent être traitées sont une autonomie de batterie accrue et une excellente réactivité du PC.</span><span class="sxs-lookup"><span data-stu-id="82722-113">To ensure that our mutual customers have a great experience on any form factor they choose with Windows, two key success metrics that need to be addressed are increased battery life and excellent PC responsiveness.</span></span> <span data-ttu-id="82722-114">Pour y parvenir, des améliorations ont été apportées dans plusieurs domaines de Windows, notamment le cycle de vie des processus, les États de veille et les applications de démarrage (applications avec lancement automatisé après le démarrage de l’ordinateur).</span><span class="sxs-lookup"><span data-stu-id="82722-114">In order to achieve these, improvements have been made in multiple areas of Windows including process life cycle, sleep states and startup apps (apps with automated launch after machine boot).</span></span> <span data-ttu-id="82722-115">Cette rubrique met en évidence certains des impacts des applications de démarrage sur un appareil Windows, et fournit des conseils aux développeurs (ISV/IHV) et aux OEM pour repenser les modèles d’utilisation des applications de démarrage afin d’améliorer la durée de vie et la réactivité de la batterie pour nos clients mutuels.</span><span class="sxs-lookup"><span data-stu-id="82722-115">This topic highlights some of the impacts that startup apps have on a Windows device, and provides guidance to developers (ISV/IHV) and OEMs to rethink the usage patterns of startup apps in order to improve battery life and responsiveness for our mutual customers.</span></span> <span data-ttu-id="82722-116">Elle décrit également les modifications apportées à Windows, qui permettent aux utilisateurs de déterminer les applications de démarrage qui sont réellement en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="82722-116">It also describes the changes in Windows that put users in control of determining which of the startup apps actually get to execute.</span></span>

<span data-ttu-id="82722-117">Les applications du Windows Store sont conçues pour adhérer à de nouvelles normes de consommation et de réactivité de la batterie, et Windows gère leur cycle de vie en les suspendant et/ou en les terminant.</span><span class="sxs-lookup"><span data-stu-id="82722-117">Windows Store apps are designed to adhere to new standards of battery consumption and responsiveness, and Windows manages their life cycle by suspending and/or terminating them.</span></span> <span data-ttu-id="82722-118">Toutefois, les applications de bureau conçues pour des versions antérieures de Windows n’ont pas nécessairement été conçues pour préserver la durée de vie de la batterie ou être sensibles à l’activité des utilisateurs, et peuvent affecter la réactivité du système (par exemple, lorsqu’une application envoie une pulsation normale de 1 seconde pour vérifier les mises à jour</span><span class="sxs-lookup"><span data-stu-id="82722-118">However, desktop apps designed for prior Windows versions have not necessarily been designed to preserve battery life or be sensitive to user activity, and can affect system responsiveness (for example, when an app sends a regular 1-second heartbeat to check for updates, or pre-allocates memory upfront in case it needs it later).</span></span> <span data-ttu-id="82722-119">Cela peut créer une expérience médiocre pour l’utilisateur qui achète un Tablet PC Windows avec une durée de vie de batterie longue et des semaines de secours, mais découvre que la durée de vie de la batterie des tablettes n’atteint pas ces objectifs.</span><span class="sxs-lookup"><span data-stu-id="82722-119">This can create a poor experience for the user who buys a Windows tablet PC with a long battery life expectancy and weeks of standby, but discovers the tablet s battery life does not achieve these goals.</span></span> <span data-ttu-id="82722-120">En outre, étant donné que les applications de démarrage s’exécutent en arrière-plan, le nombre d’applications en cours d’exécution sur le système peut être beaucoup plus important que ce que l’utilisateur sait et affecter la réactivité du système.</span><span class="sxs-lookup"><span data-stu-id="82722-120">Also, since startup apps run in the background, the number of apps running on the system can be significantly more than what the user is aware of and affect system responsiveness.</span></span> <span data-ttu-id="82722-121">Les applications de démarrage sont classées pour inclure celles tirant parti de ces mécanismes pour démarrer :</span><span class="sxs-lookup"><span data-stu-id="82722-121">Startup apps are classified to include those leveraging these mechanisms to start:</span></span>

-   <span data-ttu-id="82722-122">Exécuter des clés de Registre (HKLM, HKCU, nœuds WOW64 inclus)</span><span class="sxs-lookup"><span data-stu-id="82722-122">Run registry keys (HKLM, HKCU, wow64 nodes included)</span></span>
-   <span data-ttu-id="82722-123">Clés de Registre RunOnce</span><span class="sxs-lookup"><span data-stu-id="82722-123">RunOnce registry keys</span></span>
-   <span data-ttu-id="82722-124">Dossiers de démarrage dans le menu Démarrer pour les emplacements publics et par utilisateur</span><span class="sxs-lookup"><span data-stu-id="82722-124">Startup folders under the start menu for per user and public locations</span></span>

<span data-ttu-id="82722-125">De nouvelles fonctionnalités ont été ajoutées à Windows pour s’assurer que les utilisateurs finaux sont toujours en contrôle des applications qui s’exécutent sur leurs systèmes.</span><span class="sxs-lookup"><span data-stu-id="82722-125">New functionality has been added to Windows to ensure that end users are always in control of the apps that run on their systems.</span></span> <span data-ttu-id="82722-126">L’onglet démarrage du gestionnaire des tâches affiche une liste des applications de démarrage, ainsi que des contrôles qui permettent aux utilisateurs de désactiver les applications de démarrage.</span><span class="sxs-lookup"><span data-stu-id="82722-126">The Startup tab in Task Manager shows a list of startup apps, along with controls that allow users to disable startup apps.</span></span> <span data-ttu-id="82722-127">Pour aider les utilisateurs à déterminer les éléments à désactiver, le gestionnaire des tâches affiche une mesure de chaque impact sur les applications de démarrage.</span><span class="sxs-lookup"><span data-stu-id="82722-127">To help users determine what to disable, Task Manager displays a measure of each startup app s impact.</span></span> <span data-ttu-id="82722-128">L’impact est évalué en fonction de l’utilisation du processeur et du disque de l’application au démarrage.</span><span class="sxs-lookup"><span data-stu-id="82722-128">Impact is assessed based on an app s CPU and disk usage at startup.</span></span> <span data-ttu-id="82722-129">Les valeurs d’impact sont déterminées en appliquant les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="82722-129">Impact values are determined by applying these criteria:</span></span>

-   <span data-ttu-id="82722-130">**Impact élevé**   Applications qui utilisent plus de 1 seconde du temps processeur ou plus de 3 Mo d’e/s disque au démarrage</span><span class="sxs-lookup"><span data-stu-id="82722-130">**High impact**   Apps that use more than 1 second of CPU time or more than 3 MB of disk I/O at startup</span></span>
-   <span data-ttu-id="82722-131">**Impact moyen**   Applications qui utilisent 300 ms-1000 ms du temps processeur ou 300 Ko-3 Mo d’e/s disque</span><span class="sxs-lookup"><span data-stu-id="82722-131">**Medium impact**   Apps that use 300 ms - 1000 ms of CPU time or 300 KB - 3 MB of disk I/O</span></span>
-   <span data-ttu-id="82722-132">**Impact faible**   Applications qui utilisent moins de 300 ms de temps processeur et moins de 300 Ko d’e/s disque</span><span class="sxs-lookup"><span data-stu-id="82722-132">**Low impact**   Apps that use less than 300 ms of CPU time and less than 300 KB of disk I/O</span></span>

<span data-ttu-id="82722-133">Microsoft fournit des outils pour aider les développeurs d’applications à évaluer, analyser et prendre des mesures pour réduire leur impact sur le démarrage et améliorer l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82722-133">Microsoft provides tools to help app developers assess, analyze and take steps to reduce their startup impact and improve the user experience.</span></span> <span data-ttu-id="82722-134">Le kit de déploiement et d’évaluation offre la possibilité d’exécuter une évaluation des performances de démarrage et de mesurer l’impact des applications qui s’exécutent au démarrage.</span><span class="sxs-lookup"><span data-stu-id="82722-134">The Assessment and Deployment Kit provides the ability to run a boot performance assessment and measure the impact of apps that run at startup.</span></span> <span data-ttu-id="82722-135">Les résultats de l’évaluation contiennent des informations détaillées sur l’analyse et la correction, le cas échéant, pour les composants les plus importants au démarrage de Windows.</span><span class="sxs-lookup"><span data-stu-id="82722-135">The assessment results contain detailed analysis and remediation info where applicable, for the top-impacting components at Windows startup.</span></span> <span data-ttu-id="82722-136">À l’aide de l’analyseur de performances Windows, les développeurs d’applications peuvent effectuer une analyse détaillée afin de déterminer la cause racine de l’impact sur les performances et d’améliorer les performances de démarrage de Windows.</span><span class="sxs-lookup"><span data-stu-id="82722-136">Using the Windows Performance Analyzer, app developers can perform deep analysis to find the root cause of the performance impact and improve Windows startup performance.</span></span> <span data-ttu-id="82722-137">Installez le Kit Windows ADK à partir d' [ici](/previous-versions/windows/hh825494(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="82722-137">Install the Windows ADK from [here](/previous-versions/windows/hh825494(v=win.10)).</span></span>

## <a name="guidance"></a><span data-ttu-id="82722-138">Assistance</span><span class="sxs-lookup"><span data-stu-id="82722-138">Guidance</span></span>

<span data-ttu-id="82722-139">Les applications de démarrage s’étendent sur plusieurs catégories, comme décrit dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="82722-139">Startup apps span multiple categories as described in the table below.</span></span> <span data-ttu-id="82722-140">Un ensemble de recommandations pour les développeurs est mappé aux catégories d’applications de démarrage à aligner avec les modifications fonctionnelles de Windows décrites ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="82722-140">A set of recommendations for developers is mapped to the categories of startup apps to align with the Windows functional changes described above.</span></span>



<span data-ttu-id="82722-141">Catégories d’applications de démarrage</span><span class="sxs-lookup"><span data-stu-id="82722-141">Startup Apps Categories</span></span>

<span data-ttu-id="82722-142">Description</span><span class="sxs-lookup"><span data-stu-id="82722-142">Description</span></span>

<span data-ttu-id="82722-143">Recommandation</span><span class="sxs-lookup"><span data-stu-id="82722-143">Recommendation</span></span>

<span data-ttu-id="82722-144">**Programmes**</span><span class="sxs-lookup"><span data-stu-id="82722-144">**Updaters**</span></span>

<span data-ttu-id="82722-145">Surveiller et mettre à jour les utilisateurs pour les mises à jour en ligne</span><span class="sxs-lookup"><span data-stu-id="82722-145">Monitor and update users for online updates</span></span>

<span data-ttu-id="82722-146">**Tâche de maintenance**</span><span class="sxs-lookup"><span data-stu-id="82722-146">**Maintenance Task**</span></span>

> [!Note]  
> <span data-ttu-id="82722-147">Toutes les mises à jour doivent être des tâches de maintenance, sans aucune exigence d’interaction avec l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82722-147">All updates should be maintenance tasks, without any UI interaction requirements.</span></span> <span data-ttu-id="82722-148">Les applications doivent simplement se mettre à jour en mode silencieux, et restaurer en cas d’échec</span><span class="sxs-lookup"><span data-stu-id="82722-148">Apps should just update themselves quietly, and rollback on failure</span></span>

<br/>

<span data-ttu-id="82722-149">$ {ROWSPAN2} $**assistance matérielle**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="82722-149">${ROWSPAN2}$**Hardware Assistance**${REMOVE}$</span></span>  

<span data-ttu-id="82722-150">Autres points d’accès</span><span class="sxs-lookup"><span data-stu-id="82722-150">Alternative Access Points</span></span>

<span data-ttu-id="82722-151">Fournir un accès aux fonctionnalités et applications Windows accessibles via d’autres points d’accès dans Windows</span><span class="sxs-lookup"><span data-stu-id="82722-151">Provide access to Windows features and apps that are accessible via other access points in Windows</span></span>

<span data-ttu-id="82722-152">**Remove**</span><span class="sxs-lookup"><span data-stu-id="82722-152">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="82722-153">La clé est de réduire les fonctionnalités en double qui existent dans Windows</span><span class="sxs-lookup"><span data-stu-id="82722-153">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="82722-154">Notificateurs</span><span class="sxs-lookup"><span data-stu-id="82722-154">Notifiers</span></span>

<span data-ttu-id="82722-155">Fournir aux utilisateurs des notifications concernant leurs appareils</span><span class="sxs-lookup"><span data-stu-id="82722-155">Provide users with notifications regarding their devices</span></span>

<span data-ttu-id="82722-156">**Remove**</span><span class="sxs-lookup"><span data-stu-id="82722-156">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="82722-157">Windows fournit des notifications aux utilisateurs sur leurs appareils</span><span class="sxs-lookup"><span data-stu-id="82722-157">Windows provides notifications to users about their devices</span></span>

<br/>

<span data-ttu-id="82722-158">**Pré-lanceurs**</span><span class="sxs-lookup"><span data-stu-id="82722-158">**Pre-launchers**</span></span>

<span data-ttu-id="82722-159">Certaines activités préliminaires requises par les applications sont déchargées dans une application de démarrage pendant la connexion de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="82722-159">Some of preliminary activities needed by apps is offloaded to a startup app during user login</span></span>

<span data-ttu-id="82722-160">**Remove**</span><span class="sxs-lookup"><span data-stu-id="82722-160">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="82722-161">Windows 8 est optimisé pour une expérience rapide des lancements d’applications.</span><span class="sxs-lookup"><span data-stu-id="82722-161">Windows 8 is optimized for a fast experience for app launches.</span></span>

<br/>

<span data-ttu-id="82722-162">$ {ROWSPAN4} $**utilitaire**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="82722-162">${ROWSPAN4}$**Utility**${REMOVE}$</span></span>  

<span data-ttu-id="82722-163">Synchronisation de PC</span><span class="sxs-lookup"><span data-stu-id="82722-163">PC Sync</span></span>

<span data-ttu-id="82722-164">Fournir des fonctionnalités de synchronisation sur plusieurs systèmes</span><span class="sxs-lookup"><span data-stu-id="82722-164">Provide sync functionality across multiple systems</span></span>

<span data-ttu-id="82722-165">**Démarrage** (mises à jour potentielles dans la version bêta)</span><span class="sxs-lookup"><span data-stu-id="82722-165">**Startup** (Potential updates in Beta)</span></span>

<span data-ttu-id="82722-166">Sauvegarde et récupération</span><span class="sxs-lookup"><span data-stu-id="82722-166">Backup & Recovery</span></span>

<span data-ttu-id="82722-167">Point d’entrée pour enregistrer et restaurer l’état des fichiers, des paramètres ou des systèmes entiers</span><span class="sxs-lookup"><span data-stu-id="82722-167">Entry point to save and restore the state of files, settings, or entire systems</span></span>

<span data-ttu-id="82722-168">**Application du Windows Store pour l’interfaçage avec les utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="82722-168">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="82722-169">Télémétrie</span><span class="sxs-lookup"><span data-stu-id="82722-169">Telemetry</span></span>

<span data-ttu-id="82722-170">Collecter et envoyer des informations sur l’environnement et l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="82722-170">Collect and send info about the user experience and environment</span></span>

<span data-ttu-id="82722-171">**Tâche de maintenance**</span><span class="sxs-lookup"><span data-stu-id="82722-171">**Maintenance Task**</span></span>

<span data-ttu-id="82722-172">Surveillance de PC</span><span class="sxs-lookup"><span data-stu-id="82722-172">PC Monitoring</span></span>

<span data-ttu-id="82722-173">Fournir une surveillance de l’état du système non sollicité et des notifications qui dupliquent les fonctionnalités existantes de la boîte de réception</span><span class="sxs-lookup"><span data-stu-id="82722-173">Provide unsolicited system state monitoring and notifications that duplicate existing inbox functionality</span></span>

<span data-ttu-id="82722-174">**Remove**</span><span class="sxs-lookup"><span data-stu-id="82722-174">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="82722-175">La clé est de réduire les fonctionnalités en double qui existent dans Windows</span><span class="sxs-lookup"><span data-stu-id="82722-175">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="82722-176">$ {ROWSPAN2} $**sécurité**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="82722-176">${ROWSPAN2}$**Security**${REMOVE}$</span></span>  

<span data-ttu-id="82722-177">Filtres de & de contrôle parental</span><span class="sxs-lookup"><span data-stu-id="82722-177">Parental Control & Filters</span></span>

<span data-ttu-id="82722-178">Appliquer les règles et restrictions établies pour l’accès Internet et l’utilisation</span><span class="sxs-lookup"><span data-stu-id="82722-178">Enforce rules and restrictions established for Internet access and usage</span></span>

<span data-ttu-id="82722-179">**Startup**</span><span class="sxs-lookup"><span data-stu-id="82722-179">**Startup**</span></span>

<span data-ttu-id="82722-180">Configuration et gestion</span><span class="sxs-lookup"><span data-stu-id="82722-180">Configuration & Management</span></span>

<span data-ttu-id="82722-181">Autoriser les utilisateurs à contrôler les options de diagnostic et de correction pour l’analyse de la sécurité du système notifier les utilisateurs des découvertes et des actions de sécurité</span><span class="sxs-lookup"><span data-stu-id="82722-181">Allow users to control diagnostic and remediation options for system security monitoring Notify users of findings and security actions</span></span>

<span data-ttu-id="82722-182">**Application du Windows Store pour l’interfaçage avec les utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="82722-182">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="82722-183">**Communication & Internet** (mi & VoIP)</span><span class="sxs-lookup"><span data-stu-id="82722-183">**Communication & Internet** (IM & VoIP)</span></span>

<span data-ttu-id="82722-184">Envoyer et recevoir des messages et des appels</span><span class="sxs-lookup"><span data-stu-id="82722-184">Send and receive messages and calls</span></span>

<span data-ttu-id="82722-185">**Application du Windows Store**</span><span class="sxs-lookup"><span data-stu-id="82722-185">**Windows Store app**</span></span>

<span data-ttu-id="82722-186">**Musique & MP3**</span><span class="sxs-lookup"><span data-stu-id="82722-186">**Music & MP3**</span></span>

<span data-ttu-id="82722-187">Lire, stocker et gérer la musique</span><span class="sxs-lookup"><span data-stu-id="82722-187">Play, store, and manage music</span></span>

<span data-ttu-id="82722-188">**Application du Windows Store**</span><span class="sxs-lookup"><span data-stu-id="82722-188">**Windows Store app**</span></span>

<span data-ttu-id="82722-189">**Vidéo photo &**</span><span class="sxs-lookup"><span data-stu-id="82722-189">**Photo & Video**</span></span>

<span data-ttu-id="82722-190">Détection, enregistrement, rendu, stockage et gestion des photos et des vidéos</span><span class="sxs-lookup"><span data-stu-id="82722-190">Detect, record, render, store and manage photos and videos</span></span>

<span data-ttu-id="82722-191">**Application du Windows Store**</span><span class="sxs-lookup"><span data-stu-id="82722-191">**Windows Store app**</span></span>

<span data-ttu-id="82722-192">**Jeux de PC**</span><span class="sxs-lookup"><span data-stu-id="82722-192">**PC Gaming**</span></span>

<span data-ttu-id="82722-193">Lancer des jeux dans différents domaines</span><span class="sxs-lookup"><span data-stu-id="82722-193">Launch games across various domains</span></span>

<span data-ttu-id="82722-194">**Application du Windows Store**</span><span class="sxs-lookup"><span data-stu-id="82722-194">**Windows Store app**</span></span>

<span data-ttu-id="82722-195">**Vente incitative &**</span><span class="sxs-lookup"><span data-stu-id="82722-195">**Upsell & Advertisement**</span></span>

<span data-ttu-id="82722-196">Attirer l’attention sur les biens et services disponibles à l’achat</span><span class="sxs-lookup"><span data-stu-id="82722-196">Draw attention to goods and services available for purchase</span></span>

<span data-ttu-id="82722-197">**Remove**</span><span class="sxs-lookup"><span data-stu-id="82722-197">**Remove**</span></span>



 

> [!Note]  
> <span data-ttu-id="82722-198">Les instructions relatives aux applications d’accessibilité sont couvertes par des enmissionsments directs distincts avec les éditeurs de logiciels indépendants.</span><span class="sxs-lookup"><span data-stu-id="82722-198">Accessibility apps guidelines are covered by separate direct engagements with ISVs.</span></span> <span data-ttu-id="82722-199">Pour plus d’informations, consultez [*programmation pour faciliter l’accès*](../winauto/ease-of-access---assistive-technology-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="82722-199">See [*Programming for Ease of Access*](../winauto/ease-of-access---assistive-technology-registration.md) for details.</span></span>

 

<span data-ttu-id="82722-200">**Applications du Windows Store**</span><span class="sxs-lookup"><span data-stu-id="82722-200">**Windows Store apps**</span></span>

<span data-ttu-id="82722-201">Les applications du Windows Store améliorent l’expérience utilisateur en introduisant un espace Windows avec de nouvelles coordonnées : un nouveau modèle d’application, une nouvelle interface utilisateur et un Windows Store.</span><span class="sxs-lookup"><span data-stu-id="82722-201">Windows Store apps enhance the user experience by introducing a Windows space with new coordinates: a new app model, a new user interface, and a Windows Store.</span></span> <span data-ttu-id="82722-202">Ces options d’infrastructure de langue et de présentation sont disponibles pour le développement d’applications du Windows Store :</span><span class="sxs-lookup"><span data-stu-id="82722-202">These language and presentation framework options are available for developing Windows Store apps:</span></span>

-   <span data-ttu-id="82722-203">HTML/JavaScript/CSS</span><span class="sxs-lookup"><span data-stu-id="82722-203">HTML/JavaScript/CSS</span></span>
-   <span data-ttu-id="82722-204">XAML/C #</span><span class="sxs-lookup"><span data-stu-id="82722-204">XAML/C#</span></span>
-   <span data-ttu-id="82722-205">XAML/C++</span><span class="sxs-lookup"><span data-stu-id="82722-205">XAML/C++</span></span>

<span data-ttu-id="82722-206">Les informations agrégées pour le développement d’applications du Windows Store sont disponibles dans le [Centre de développement Windows](https://msdn.microsoft.com/windows/apps/).</span><span class="sxs-lookup"><span data-stu-id="82722-206">Aggregated info for developing Windows Store apps is available at the [Windows Dev Center](https://msdn.microsoft.com/windows/apps/).</span></span>

<span data-ttu-id="82722-207">Exemples :</span><span class="sxs-lookup"><span data-stu-id="82722-207">Examples:</span></span>

-   <span data-ttu-id="82722-208">[Développement de jeux Windows Store](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="82722-208">[Developing Windows Store games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="82722-209">[Développement d’une application Windows Store qui utilise des médias](/previous-versions/windows/apps/hh465132(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="82722-209">[Developing Windows Store app that use Media](/previous-versions/windows/apps/hh465132(v=win.10))</span></span>

<span data-ttu-id="82722-210">**Tâches de maintenance automatiques**</span><span class="sxs-lookup"><span data-stu-id="82722-210">**Automatic maintenance tasks**</span></span>

<span data-ttu-id="82722-211">L’activité en arrière-plan périodique doit être conçue comme des tâches de maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="82722-211">Periodic background activity should be designed as Automatic Maintenance tasks.</span></span> <span data-ttu-id="82722-212">Celles-ci sont planifiées au temps d’inactivité du système pour augmenter la réactivité et l’efficacité énergétique des PC Windows.</span><span class="sxs-lookup"><span data-stu-id="82722-212">These are scheduled at system idle time to increase the responsiveness and energy efficiency of Windows PCs.</span></span> <span data-ttu-id="82722-213">Les tâches de maintenance peuvent être créées et configurées par une application de bureau au moment de l’installation, à l’aide du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="82722-213">Maintenance tasks can be created and configured by a desktop app at install time, using the desktop SDK.</span></span> <span data-ttu-id="82722-214">Pour plus d’informations, consultez la rubrique maintenance automatique suivante.</span><span class="sxs-lookup"><span data-stu-id="82722-214">See the Automatic Maintenance topic that follows for details.</span></span>

## <a name="resources"></a><span data-ttu-id="82722-215">Ressources</span><span class="sxs-lookup"><span data-stu-id="82722-215">Resources</span></span>

-   [<span data-ttu-id="82722-216">Instructions d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="82722-216">Accessibility Guidelines</span></span>](../winauto/ease-of-access---assistive-technology-registration.md)
-   [<span data-ttu-id="82722-217">Centre de développement Windows</span><span class="sxs-lookup"><span data-stu-id="82722-217">Windows Dev Center</span></span>](https://msdn.microsoft.com/windows/apps/)
-   <span data-ttu-id="82722-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="82722-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span></span>

 

