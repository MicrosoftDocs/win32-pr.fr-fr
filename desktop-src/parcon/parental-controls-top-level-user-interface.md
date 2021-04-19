---
description: Contrôle parental Top-Level interface utilisateur
ms.assetid: c6dfd3bc-191f-42d1-b9de-cc85a2da0a99
title: Contrôle parental Top-Level interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321475097e25b812aca8d1e65f8b88843ebb1055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529867"
---
# <a name="parental-controls-top-level-user-interface"></a><span data-ttu-id="b187a-103">Contrôle parental Top-Level interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="b187a-103">Parental Controls Top-Level User Interface</span></span>

<span data-ttu-id="b187a-104">Le lien fort entre la sécurité des familles et les comptes d’utilisateurs Windows a entraîné une catégorie combinée qui apparaît comme **comptes d’utilisateur et sécurité des familles** dans le panneau de configuration pour les références de Windows Vista orientées consommateur.</span><span class="sxs-lookup"><span data-stu-id="b187a-104">The strong link between Family Safety and Windows user accounts has driven a combined category appearing as **User Accounts and Family Safety** in Control Panel for consumer-oriented SKUs of Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="b187a-105">La catégorie apparaît en tant que **comptes d’utilisateurs** lorsqu’un ordinateur avec la fonctionnalité de jonction de domaine est joint.</span><span class="sxs-lookup"><span data-stu-id="b187a-105">The category will appear as **User Accounts** when a computer with domain-join capability is joined.</span></span>

 

<span data-ttu-id="b187a-106">Si un compte d’utilisateur standard n’a pas encore été configuré pour l’utilisateur contrôlé, un lien dans le panneau de configuration fournit un flux de travail simple pour ajouter un nouveau compte contrôlé de manière parente.</span><span class="sxs-lookup"><span data-stu-id="b187a-106">If a standard user account has not yet been set up for the controlled user, a link in Control Panel provides a simple workflow for adding a new parentally controlled account.</span></span>

<span data-ttu-id="b187a-107">Une fois qu’un compte est créé, le panneau de configuration du contrôle parental expose les fonctionnalités de niveau supérieur pour l’utilisateur contrôlé.</span><span class="sxs-lookup"><span data-stu-id="b187a-107">After an account is created, the Parental Controls Control Panel exposes the top-level user-facing functionality for the controlled user.</span></span> <span data-ttu-id="b187a-108">Html</span><span class="sxs-lookup"><span data-stu-id="b187a-108">Elements:</span></span>

-   <span data-ttu-id="b187a-109">Options globales de contrôle parental pour les cases d’option.</span><span class="sxs-lookup"><span data-stu-id="b187a-109">Overall Parental Controls restrictions on or off radio buttons.</span></span>
-   <span data-ttu-id="b187a-110">Cases d’option de contrôle de l’activité indépendante.</span><span class="sxs-lookup"><span data-stu-id="b187a-110">Independent Activity Reporting on or off control radio buttons.</span></span>
-   <span data-ttu-id="b187a-111">Une section de paramètres avec le lien restrictions Web implémentées par Microsoft, qui est indiquée de manière conditionnelle, et les types de restrictions implémentés principaux de Microsoft en mode hors connexion sont affichés.</span><span class="sxs-lookup"><span data-stu-id="b187a-111">A Settings section with the Microsoft-implemented Web Restrictions link conditionally shown, and available core offline Microsoft-implemented restrictions types shown.</span></span>
-   <span data-ttu-id="b187a-112">Une autre zone de paramètres qui s’affiche si les extensions d’interface utilisateur sont inscrites par Microsoft ou par des tiers.</span><span class="sxs-lookup"><span data-stu-id="b187a-112">A More Settings area that appears if User Interface extensions are registered by Microsoft or third parties.</span></span>
-   <span data-ttu-id="b187a-113">Zone d’état résumé qui indique le nom d’utilisateur et la vignette, le lien Afficher les rapports d’activité et l’état des paramètres de contrôle parental.</span><span class="sxs-lookup"><span data-stu-id="b187a-113">A summary status area showing the user name and tile, the View activity reports link, and the state of Parental Controls settings.</span></span> <span data-ttu-id="b187a-114">Si la valeur est on, l’affichage comprend le niveau du paramètre de filtre de contenu Web (si le filtre Microsoft est actif) ou le nom du filtre en cas de remplacement par une extension tierce, ainsi que l’état des paramètres hors connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b187a-114">If on, the display includes the Web Content Filter setting level (if the Microsoft filter is active) or filter name if overridden by a third-party extension, and state of offline settings for the user.</span></span>

<span data-ttu-id="b187a-115">La case d’option Activer le contrôle parental global est définie initialement à l’état désactivé.</span><span class="sxs-lookup"><span data-stu-id="b187a-115">The overall Parental Controls enable radio button is initially set to the off state.</span></span> <span data-ttu-id="b187a-116">Lorsqu’il est activé par un administrateur, la création de rapports d’activité est également activée par défaut, mais peut être désactivée indépendamment.</span><span class="sxs-lookup"><span data-stu-id="b187a-116">When turned on by an administrator, Activity Reporting will also be on by default, but may be turned off independently.</span></span> <span data-ttu-id="b187a-117">Comme avec presque tous les paramètres du contrôle parental, la configuration peut être effectuée par programme par le biais des API disponibles.</span><span class="sxs-lookup"><span data-stu-id="b187a-117">As with nearly all settings in Parental Controls, configuration may be performed programmatically through the available APIs.</span></span>

 

 



