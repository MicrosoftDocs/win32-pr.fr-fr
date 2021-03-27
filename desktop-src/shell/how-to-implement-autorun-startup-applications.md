---
description: Il n’existe essentiellement aucune contrainte sur la façon d’écrire une application de démarrage de l’exécution automatique.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Comment implémenter des applications de démarrage AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951941"
---
# <a name="how-to-implement-autorun-startup-applications"></a><span data-ttu-id="b00d2-103">Comment implémenter des applications de démarrage AutoRun</span><span class="sxs-lookup"><span data-stu-id="b00d2-103">How to Implement AutoRun Startup Applications</span></span>

<span data-ttu-id="b00d2-104">Il n’existe essentiellement aucune contrainte sur la façon d’écrire une application de démarrage de l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="b00d2-104">There are essentially no constraints on how to write an AutoRun startup application.</span></span> <span data-ttu-id="b00d2-105">Vous pouvez implémenter l’application de démarrage pour effectuer toutes les tâches nécessaires à l’installation, à la désinstallation, à la configuration ou à l’exécution de votre application.</span><span class="sxs-lookup"><span data-stu-id="b00d2-105">You can implement the startup application to do whatever you find necessary to install, uninstall, configure, or run your application.</span></span> <span data-ttu-id="b00d2-106">Toutefois, les conseils suivants fournissent des instructions pour l’implémentation d’une application de démarrage automatique efficace.</span><span class="sxs-lookup"><span data-stu-id="b00d2-106">However, the following tips provide some guidelines to implementing an effective AutoRun startup application.</span></span>

## <a name="instructions"></a><span data-ttu-id="b00d2-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="b00d2-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="b00d2-108">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="b00d2-108">Step 1:</span></span>

<span data-ttu-id="b00d2-109">Assurez-vous que les utilisateurs reçoivent des commentaires le plus rapidement possible après avoir inséré un disque d’exécution automatique dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="b00d2-109">Make sure that users receive feedback as soon as possible after they insert an AutoRun disc into the drive.</span></span> <span data-ttu-id="b00d2-110">Les applications de démarrage doivent être des petits programmes qui se chargent rapidement.</span><span class="sxs-lookup"><span data-stu-id="b00d2-110">Startup applications should be small programs that load quickly.</span></span> <span data-ttu-id="b00d2-111">Ils doivent identifier clairement l’application et fournir un moyen simple d’annuler l’opération.</span><span class="sxs-lookup"><span data-stu-id="b00d2-111">They should clearly identify the application and provide an easy way to cancel the operation.</span></span>

### <a name="step-2"></a><span data-ttu-id="b00d2-112">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="b00d2-112">Step 2:</span></span>

<span data-ttu-id="b00d2-113">Vérifiez si le programme est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="b00d2-113">Check to see if the program is already installed.</span></span> <span data-ttu-id="b00d2-114">Si ce n’est pas le cas, l’étape suivante sera probablement la procédure d’installation.</span><span class="sxs-lookup"><span data-stu-id="b00d2-114">If not, the next step will probably be the setup procedure.</span></span> <span data-ttu-id="b00d2-115">L’application de démarrage peut tirer parti du temps que l’utilisateur passe à lire la boîte de dialogue en démarrant un autre thread pour commencer le chargement du code d’installation.</span><span class="sxs-lookup"><span data-stu-id="b00d2-115">The startup application can take advantage of the time the user spends reading the dialog box by starting another thread to begin loading the setup code.</span></span> <span data-ttu-id="b00d2-116">Au moment où l’utilisateur clique sur **OK**, votre programme d’installation sera déjà en partie s’il n’est pas entièrement chargé.</span><span class="sxs-lookup"><span data-stu-id="b00d2-116">By the time the user clicks **OK**, your setup program will already be partly if not fully loaded.</span></span> <span data-ttu-id="b00d2-117">Cette approche réduit considérablement la perception de l’utilisateur quant au temps nécessaire au chargement de votre application.</span><span class="sxs-lookup"><span data-stu-id="b00d2-117">This approach significantly reduces the user's perception of the amount of time it takes to load your application.</span></span>

> [!Note]  
> <span data-ttu-id="b00d2-118">En règle générale, la partie initiale de l’application de démarrage présente aux utilisateurs une interface utilisateur, telle qu’une boîte de dialogue, en leur demandant comment ils souhaitent continuer.</span><span class="sxs-lookup"><span data-stu-id="b00d2-118">Typically, the initial part of the startup application presents users with a user interface, such as a dialog box, asking them how they would like to proceed.</span></span>

 

### <a name="step-3"></a><span data-ttu-id="b00d2-119">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="b00d2-119">Step 3:</span></span>

<span data-ttu-id="b00d2-120">Démarrez un autre thread pour commencer à charger le code de l’application afin de réduire le temps d’attente pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b00d2-120">Start another thread to begin loading application code to shorten the waiting time for the user.</span></span> <span data-ttu-id="b00d2-121">Si l’application a déjà été installée, l’utilisateur a probablement inséré le disque pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="b00d2-121">If the application has already been installed, the user probably inserted the disk to run the application.</span></span>

### <a name="step-4"></a><span data-ttu-id="b00d2-122">Étape 4 :</span><span class="sxs-lookup"><span data-stu-id="b00d2-122">Step 4:</span></span>

<span data-ttu-id="b00d2-123">Utilisez les indications suivantes pour réduire l’utilisation du disque dur :</span><span class="sxs-lookup"><span data-stu-id="b00d2-123">Use the following hints to minimize hard disk usage:</span></span>

-   <span data-ttu-id="b00d2-124">Conservez au minimum le nombre de fichiers qui doivent se trouver sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="b00d2-124">Keep the number of files that must be on the hard disk to a minimum.</span></span> <span data-ttu-id="b00d2-125">Ils doivent être limités aux fichiers essentiels pour exécuter le programme ou qui prennent un temps de lecture beaucoup plus important à partir du média.</span><span class="sxs-lookup"><span data-stu-id="b00d2-125">They should be restricted to files that are essential to running the program or that would take an unacceptably large amount of time to read from the media.</span></span>
-   <span data-ttu-id="b00d2-126">Dans de nombreux cas, l’installation de fichiers non essentiels sur le disque dur n’est pas nécessaire, mais peut fournir des avantages tels que l’augmentation des performances.</span><span class="sxs-lookup"><span data-stu-id="b00d2-126">In many cases, installing nonessential files on the hard disk is not necessary, but might provide benefits such as increased performance.</span></span> <span data-ttu-id="b00d2-127">Donnez à l’utilisateur la possibilité de décider comment effectuer le compromis entre les coûts et les avantages du stockage sur disque dur.</span><span class="sxs-lookup"><span data-stu-id="b00d2-127">Give the user the option of deciding how to make the trade-off between the costs and benefits of hard disk storage.</span></span>
-   <span data-ttu-id="b00d2-128">Fournir un moyen de désinstaller tous les composants qui ont été placés sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="b00d2-128">Provide a way to uninstall any components that were placed on the hard disk.</span></span>
-   <span data-ttu-id="b00d2-129">Si votre application met en cache des données, donnez-lui un contrôle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b00d2-129">If your application caches data, give the user some control over it.</span></span> <span data-ttu-id="b00d2-130">Incluez les options dans l’application de démarrage, telles que la définition d’une limite sur la quantité maximale de données mises en cache qui seront stockées sur le disque dur, ou la suppression des données mises en cache par l’application lorsqu’elle se termine.</span><span class="sxs-lookup"><span data-stu-id="b00d2-130">Include options in the startup application such as setting a limit on the maximum amount of cached data that will be stored on the hard disk, or having the application discard any cached data when it terminates.</span></span>

### <a name="step-5"></a><span data-ttu-id="b00d2-131">Étape 5 :</span><span class="sxs-lookup"><span data-stu-id="b00d2-131">Step 5:</span></span>

<span data-ttu-id="b00d2-132">Désactivez l’exécution automatique si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b00d2-132">Disable Autorun if needed.</span></span> <span data-ttu-id="b00d2-133">L’exécution automatique peut être supprimée par programmation ou désactivée entièrement avec le registre, même si un support a un fichier autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="b00d2-133">AutoRun can be suppressed programmatically or disabled entirely with the registry, even when a medium has an Autorun.inf file.</span></span> <span data-ttu-id="b00d2-134">Pour plus d’informations [, consultez Activation et désactivation de l’exécution automatique](autoplay-reg.md) .</span><span class="sxs-lookup"><span data-stu-id="b00d2-134">See [Enabling and Disabling AutoRun](autoplay-reg.md) for more information.</span></span>

 

 



