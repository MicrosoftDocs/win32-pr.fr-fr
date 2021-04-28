---
description: Meilleures pratiques pour l’efficacité énergétique
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Meilleures pratiques pour l’efficacité énergétique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d9a348b9df49531358de2db50acc0936622c36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088387"
---
# <a name="best-practices-for-energy-efficiency"></a><span data-ttu-id="e0172-103">Meilleures pratiques pour l’efficacité énergétique</span><span class="sxs-lookup"><span data-stu-id="e0172-103">Best Practices for Energy Efficiency</span></span>

## <a name="platform"></a><span data-ttu-id="e0172-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="e0172-104">Platform</span></span>

 <span data-ttu-id="e0172-105">**Clients** – Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="e0172-105">**Clients** – Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="e0172-106">Description</span><span class="sxs-lookup"><span data-stu-id="e0172-106">Description</span></span>

<span data-ttu-id="e0172-107">Les ordinateurs portables Windows doivent satisfaire aux exigences réglementaires en matière d’efficacité énergétique, telles que celles du programme Energy Star de l’Agence de protection environnementale (EPA) États-Unis.</span><span class="sxs-lookup"><span data-stu-id="e0172-107">Windows-based laptops must meet energy efficiency regulatory requirements such as those of the United States Environmental Protection Agency (EPA) Energy Star program.</span></span> <span data-ttu-id="e0172-108">En outre, les enquêtes montrent que la durée de vie de la batterie est plus longue que celle des ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="e0172-108">Furthermore, surveys have shown that longer battery life continues to be what consumers most want and need in laptops.</span></span> <span data-ttu-id="e0172-109">Pour répondre aux demandes des consommateurs, les ordinateurs portables Windows doivent continuellement avancer dans les domaines suivants :</span><span class="sxs-lookup"><span data-stu-id="e0172-109">To meet consumer demands, Windows laptops must continually advance in the following areas:</span></span>

-   <span data-ttu-id="e0172-110">Efficacité énergétique dans tous les scénarios d’utilisation, y compris les charges de travail inactives, la productivité des DVD et les supports, ainsi que les tests de performances du secteur</span><span class="sxs-lookup"><span data-stu-id="e0172-110">Energy efficiency in all usage scenarios, including idle, productivity workloads, DVD and media playback, and industry benchmarks</span></span>
-   <span data-ttu-id="e0172-111">Autonomie de la batterie d’un ordinateur portable — pour les plateformes matérielles et pour Windows</span><span class="sxs-lookup"><span data-stu-id="e0172-111">Mobile PC battery life—for hardware platforms and for Windows</span></span>

<span data-ttu-id="e0172-112">La plate-forme Windows est très fiable et permet d’accélérer les performances.</span><span class="sxs-lookup"><span data-stu-id="e0172-112">The Windows platform is highly reliable and enables fast on-and-off performance.</span></span> <span data-ttu-id="e0172-113">Toutefois, les extensions fournies avec les systèmes d’ordinateurs portables, telles que les services, les applets de barre d’état système, les pilotes et autres logiciels, peuvent affecter considérablement les performances, la fiabilité et l’efficacité énergétique.</span><span class="sxs-lookup"><span data-stu-id="e0172-113">However, extensions provided with mobile PC systems, such as services, system tray applets, drivers, and other software, can significantly affect performance, reliability, and energy efficiency.</span></span>

<span data-ttu-id="e0172-114">L’efficacité énergétique est un problème complexe, avec les facteurs affectés par et affectant tous les éléments de l’écosystème du PC.</span><span class="sxs-lookup"><span data-stu-id="e0172-114">Energy efficiency is a complex problem, with factors affected by and affecting all elements of the PC ecosystem.</span></span> <span data-ttu-id="e0172-115">Des améliorations mineures dans plusieurs scénarios peuvent améliorer l’efficacité énergétique, mais une application, un appareil ou une fonctionnalité système à performances médiocres peut augmenter considérablement la consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="e0172-115">Small enhancements across multiple scenarios can improve energy efficiency, but a single poorly performing application, device, or system feature can increase energy consumption significantly.</span></span>

<span data-ttu-id="e0172-116">Le matériel et les périphériques constituent la base de l’efficacité énergétique.</span><span class="sxs-lookup"><span data-stu-id="e0172-116">Hardware and devices form the foundation for energy efficiency.</span></span> <span data-ttu-id="e0172-117">Toutefois, les logiciels d’application et de service doivent également être efficaces pour permettre au système d’atteindre une autonomie de batterie optimale.</span><span class="sxs-lookup"><span data-stu-id="e0172-117">However, application and service software must also be efficient to allow the system to achieve optimal battery life.</span></span> <span data-ttu-id="e0172-118">Chaque composant logiciel sur le système, y compris le système d’exploitation et les applications et services à valeur ajoutée, doit respecter les règles de performances de base.</span><span class="sxs-lookup"><span data-stu-id="e0172-118">Each software component on the system, including the operating system and value-added applications and services, must conform to basic efficiency guidelines.</span></span> <span data-ttu-id="e0172-119">Une application ou un service à dysfonctionnement unique peut éliminer tout gain d’efficacité énergétique que le dernier processeur, les périphériques ou le matériel de la plateforme ont atteint.</span><span class="sxs-lookup"><span data-stu-id="e0172-119">A single misbehaving application or service can eliminate any energy efficiency gains that the latest processor, devices, or platform hardware achieved.</span></span> <span data-ttu-id="e0172-120">Pour plus d’informations sur la durée de vie de la batterie et l’efficacité énergétique, reportez-vous au [Guide des solutions de durée de vie des batteries](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#).</span><span class="sxs-lookup"><span data-stu-id="e0172-120">For more detailed information regarding battery life and energy efficiency please refer to the [Battery Life Solutions Guide](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#).</span></span>

<span data-ttu-id="e0172-121">Les principaux problèmes et les composants qui affectent la durée de vie de la batterie sur un ordinateur portable sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e0172-121">The principle issues and components that affect battery life in a mobile PC are:</span></span>

<span data-ttu-id="e0172-122">**Caractéristiques de la batterie**</span><span class="sxs-lookup"><span data-stu-id="e0172-122">**Battery Characteristics**</span></span>

-   <span data-ttu-id="e0172-123">La taille, le type et la qualité de la capacité de la batterie affectent la durée de vie de la batterie</span><span class="sxs-lookup"><span data-stu-id="e0172-123">Size, type, and quality of battery capacity affect battery life</span></span>
-   <span data-ttu-id="e0172-124">Plus la batterie est grande, plus l’alimentation est grande</span><span class="sxs-lookup"><span data-stu-id="e0172-124">The larger the battery, the greater the power supply</span></span>
-   <span data-ttu-id="e0172-125">Les batteries plus grandes sont plus chères et plus lourdes ; les utilisateurs préfèrent les systèmes plus légers</span><span class="sxs-lookup"><span data-stu-id="e0172-125">Larger batteries are more expensive and heavier; users prefer lighter systems</span></span>

<span data-ttu-id="e0172-126">**Composants matériels**</span><span class="sxs-lookup"><span data-stu-id="e0172-126">**Hardware Components**</span></span>

-   <span data-ttu-id="e0172-127">Fréquence et profondeur auxquelles le matériel peut entrer dans des États d’alimentation inférieurs</span><span class="sxs-lookup"><span data-stu-id="e0172-127">Frequency and depth to which hardware can enter lower power states</span></span>
-   <span data-ttu-id="e0172-128">Prise en charge matérielle des États de faible consommation d’énergie</span><span class="sxs-lookup"><span data-stu-id="e0172-128">Hardware support of lower power states</span></span>
-   <span data-ttu-id="e0172-129">Optimisation du pilote pour l’efficacité énergétique</span><span class="sxs-lookup"><span data-stu-id="e0172-129">Driver optimization for energy efficiency</span></span>

<span data-ttu-id="e0172-130">**Système d’exploitation-gestion de l’alimentation dirigée**</span><span class="sxs-lookup"><span data-stu-id="e0172-130">**Operating System–Directed Power Management**</span></span>

-   <span data-ttu-id="e0172-131">Efficacité du code Windows en temps de chargement et en mode inactif</span><span class="sxs-lookup"><span data-stu-id="e0172-131">Efficiency of Windows code while under a load versus while idle</span></span>
-   <span data-ttu-id="e0172-132">Niveau de coopération de tous les composants avec la gestion de l’alimentation dirigée vers Windows</span><span class="sxs-lookup"><span data-stu-id="e0172-132">Cooperation level of all components with Windows-directed power management</span></span>
-   <span data-ttu-id="e0172-133">Configuration appropriée du système d’exploitation pour optimiser la gestion de l’alimentation via les paramètres de stratégie d’alimentation</span><span class="sxs-lookup"><span data-stu-id="e0172-133">Proper configuration of the operating system to optimize for power management through power policy settings</span></span>

<span data-ttu-id="e0172-134">**Logiciels et services d’application**</span><span class="sxs-lookup"><span data-stu-id="e0172-134">**Application Software and Services**</span></span>

-   <span data-ttu-id="e0172-135">Efficacité des applications, des pilotes et des services tout en étant sous une charge et en mode inactif</span><span class="sxs-lookup"><span data-stu-id="e0172-135">Efficiency of applications, drivers, and services while under a load versus while idle</span></span>
-   <span data-ttu-id="e0172-136">Niveau de coopération des applications avec Windows – gestion de l’alimentation dirigée</span><span class="sxs-lookup"><span data-stu-id="e0172-136">Cooperation level of applications with Windows–directed power management</span></span>
-   <span data-ttu-id="e0172-137">Remise des logiciels du système ou des appareils pour qu’ils soient en état d’inactivité faible</span><span class="sxs-lookup"><span data-stu-id="e0172-137">Software allowance of the system or devices to enter into low-power idle states</span></span>

<span data-ttu-id="e0172-138">Une application ou un composant de service unique peut empêcher un système de réaliser une autonomie de batterie optimale.</span><span class="sxs-lookup"><span data-stu-id="e0172-138">A single application or service component can prevent a system from realizing optimal battery life.</span></span> <span data-ttu-id="e0172-139">Bien que Windows fournisse de nombreuses options de configuration de l’alimentation, les logiciels préinstallés ou les paramètres de stratégie d’alimentation sur de nombreux systèmes ne sont pas optimisés pour la plateforme matérielle de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="e0172-139">Although Windows provides many power configuration options, preinstalled software or power policy settings on many systems are not optimized for the host hardware platform.</span></span>

<span data-ttu-id="e0172-140">Une méthode courante pour évaluer l’impact sur la durée de vie de la batterie des logiciels préinstallés consiste à comparer la consommation énergétique du système avec une installation propre de Windows et une installation Windows qui comprend des logiciels et des services à valeur ajoutée.</span><span class="sxs-lookup"><span data-stu-id="e0172-140">A common method for evaluating the battery-life impact of preinstalled software is to compare the power consumption of the system with a clean installation of Windows versus a Windows installation that includes value-added software and services.</span></span> <span data-ttu-id="e0172-141">Bien qu’une nouvelle installation ne représente pas la plateforme standard que les fabricants d’ordinateurs OEM livrent aux clients, la comparaison de la consommation d’énergie peut fournir un aperçu de l’efficacité énergétique des logiciels préinstallés.</span><span class="sxs-lookup"><span data-stu-id="e0172-141">Although a clean installation does not represent the typical platform that OEMs ship to customers, the power consumption comparison can provide insight into the energy-efficiency of preinstalled software.</span></span>

## <a name="best-practices"></a><span data-ttu-id="e0172-142">Bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="e0172-142">Best Practices</span></span>

<span data-ttu-id="e0172-143">Pour vous assurer que votre application est optimisée sur les plateformes Windows, suivez ces meilleures pratiques quand vous concevez des applications ou des services :</span><span class="sxs-lookup"><span data-stu-id="e0172-143">To ensure that your application is optimized on Windows platforms, follow these best practices when you design applications or services:</span></span>

-   <span data-ttu-id="e0172-144">**Évitez d’utiliser des minuteries périodiques à haute résolution**</span><span class="sxs-lookup"><span data-stu-id="e0172-144">**Avoid use of high-resolution periodic timers**</span></span>

<dl> <span data-ttu-id="e0172-145">Utilisation de minuteries périodiques haute résolution (</span><span class="sxs-lookup"><span data-stu-id="e0172-145">Using high-resolution periodic timers (</span></span><10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   <span data-ttu-id="e0172-146">**Investir dans des optimisations de performances**</span><span class="sxs-lookup"><span data-stu-id="e0172-146">**Invest in performance optimizations**</span></span>

<dl> <span data-ttu-id="e0172-147">Chaque optimisation des performances est une optimisation de la durée de vie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="e0172-147">Every performance optimization is a battery life optimization.</span></span> <span data-ttu-id="e0172-148">Les réductions des ressources requises, telles que l’utilisation de temps processeur réduit ou de lectures de disque par lot/cluster, permettent au matériel système de devenir inactif et de passer en mode faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="e0172-148">Reductions in required resources, such as using less processor time or batching/clustering disk reads, allow system hardware to become idle and enter low-power modes.</span></span>  
</dl>

-   <span data-ttu-id="e0172-149">**Ajuster à la stratégie d’alimentation de l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e0172-149">**Adjust to user power policy**</span></span>

<dl> <span data-ttu-id="e0172-150">Windows Vista et les versions ultérieures permettent à l’utilisateur de choisir facilement les économies d’énergie globales ou le comportement des performances du système.</span><span class="sxs-lookup"><span data-stu-id="e0172-150">Windows Vista and later make it easy for the user to choose the overall power-savings or performance behavior of the system.</span></span> <span data-ttu-id="e0172-151">Votre application doit répondre aux modifications apportées à la stratégie d’alimentation et réduire l’utilisation des ressources ou améliorer les performances en conséquence.</span><span class="sxs-lookup"><span data-stu-id="e0172-151">Your application should respond to changes in power policy and reduce resource usage or increase performance accordingly.</span></span> <span data-ttu-id="e0172-152">Par exemple, une application doit désactiver l’activité en arrière-plan, telle que l’indexation ou l’analyse du système lorsque l’utilisateur a sélectionné un mode de gestion de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="e0172-152">For example, an application should disable background activity such as indexing or system scanning when the user has selected a Power Saver power plan.</span></span>  
</dl>

-   <span data-ttu-id="e0172-153">**Réduire l’utilisation des ressources lorsque le système est alimenté par batterie**</span><span class="sxs-lookup"><span data-stu-id="e0172-153">**Reduce resource usage when the system is on battery power**</span></span>

<dl> <span data-ttu-id="e0172-154">Votre application doit réduire son utilisation des ressources (par exemple, la fréquence de mise à jour en arrière-plan) quand le système est alimenté par batterie.</span><span class="sxs-lookup"><span data-stu-id="e0172-154">Your application should reduce its resource usage - such as background update frequency - when the system is on battery power.</span></span>  
</dl>

-   <span data-ttu-id="e0172-155">**Ne pas afficher dans l’affichage lorsqu’il est désactivé**</span><span class="sxs-lookup"><span data-stu-id="e0172-155">**Do not render to the display when it is off**</span></span>

<dl> <span data-ttu-id="e0172-156">L’affichage du système peut être désactivé pour les économies d’énergie.</span><span class="sxs-lookup"><span data-stu-id="e0172-156">The system display might be off for power savings.</span></span> <span data-ttu-id="e0172-157">Votre application ne doit pas effectuer de rendu graphique inutile lorsque l’affichage est désactivé, car cela gaspille les ressources système et la puissance.</span><span class="sxs-lookup"><span data-stu-id="e0172-157">Your application should not perform unnecessary graphics rendering when the display is off because this wastes system resources and power.</span></span>  
</dl>

-   <span data-ttu-id="e0172-158">**Éviter l’interrogation et la rotation dans des boucles serrées**</span><span class="sxs-lookup"><span data-stu-id="e0172-158">**Avoid polling and spinning in tight loops**</span></span>

<dl> <span data-ttu-id="e0172-159">Une utilisation intensive du processeur réduit l’efficacité des technologies de gestion de l’alimentation du processeur, telles que les États d’inactivité du processeur et les États des performances du processeur.</span><span class="sxs-lookup"><span data-stu-id="e0172-159">Heavy processor usage reduces the effectiveness of processor power-management technologies such as processor idle states and processor performance states.</span></span>  
</dl>

-   <span data-ttu-id="e0172-160">**N’empêchez pas le système de désactiver l’affichage ou le ralenti pour le mettre en veille**</span><span class="sxs-lookup"><span data-stu-id="e0172-160">**Do not prevent the system from turning off the display or idling to sleep**</span></span>

<dl> <span data-ttu-id="e0172-161">Votre application doit faire des demandes d’alimentation judicieuses avec l’API SetThreadExecutionState.</span><span class="sxs-lookup"><span data-stu-id="e0172-161">Your application should make judicious power requests with the SetThreadExecutionState API.</span></span> <span data-ttu-id="e0172-162">Le système doit effectuer ces requêtes uniquement lorsque les opérations critiques doivent retarder l’arrêt de l’affichage ou l’entrée automatique en mode veille.</span><span class="sxs-lookup"><span data-stu-id="e0172-162">The system should make these requests only when critical operations must delay the system from powering off the display or automatically entering sleep.</span></span>  
</dl>

-   <span data-ttu-id="e0172-163">**Répondre aux événements courants de gestion de l’alimentation**</span><span class="sxs-lookup"><span data-stu-id="e0172-163">**Respond to common power-management events**</span></span>

<dl> <span data-ttu-id="e0172-164">Votre application doit s’inscrire aux événements de gestion de l’alimentation courants et y répondre, tels que les modifications de source d’alimentation du système et les notifications de mise sous tension et de mise hors tension pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="e0172-164">Your application should register for and respond to common power-management events, such as system power-source changes and power-on and power-off notifications for the display.</span></span>  
</dl>

-   <span data-ttu-id="e0172-165">**N’activez pas la journalisation du débogage par défaut ; Utilisez à la place Suivi d’v nements pour Windows**</span><span class="sxs-lookup"><span data-stu-id="e0172-165">**Do not enable debug logging by default; use Event Tracing for Windows instead**</span></span>

<dl> <span data-ttu-id="e0172-166">La journalisation de débogage périodique peut empêcher la rotation du disque.</span><span class="sxs-lookup"><span data-stu-id="e0172-166">Periodic debug logging can prevent disk spin-down.</span></span>  
</dl>

## <a name="links-to-other-resources"></a><span data-ttu-id="e0172-167">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="e0172-167">Links to Other Resources</span></span>

-   [<span data-ttu-id="e0172-168">Guide des solutions de durée de vie de la batterie</span><span class="sxs-lookup"><span data-stu-id="e0172-168">Battery Life Solutions Guide</span></span>](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [<span data-ttu-id="e0172-169">Portail d’efficacité énergétique</span><span class="sxs-lookup"><span data-stu-id="e0172-169">Energy Efficiency Portal</span></span>](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [<span data-ttu-id="e0172-170">Windows Performance Toolkit</span><span class="sxs-lookup"><span data-stu-id="e0172-170">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



