---
description: Vous pouvez surveiller les statistiques des objets lors de l’exécution d’une application. En procédant ainsi, vous pouvez ajuster les caractéristiques du pool d’objets pour obtenir l’équilibre entre les performances et les ressources que vous aimeriez avoir.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Analyse des statistiques des objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317857"
---
# <a name="monitoring-object-statistics"></a><span data-ttu-id="65eaf-104">Analyse des statistiques des objets</span><span class="sxs-lookup"><span data-stu-id="65eaf-104">Monitoring Object Statistics</span></span>

<span data-ttu-id="65eaf-105">Vous pouvez surveiller les statistiques des objets lors de l’exécution d’une application.</span><span class="sxs-lookup"><span data-stu-id="65eaf-105">You can monitor object statistics as an application runs.</span></span> <span data-ttu-id="65eaf-106">En procédant ainsi, vous pouvez ajuster les caractéristiques du pool d’objets pour obtenir l’équilibre entre les performances et les ressources que vous aimeriez avoir.</span><span class="sxs-lookup"><span data-stu-id="65eaf-106">By doing so, you can fine-tune the object pool characteristics to achieve the balance in performance and resources that you would like to have.</span></span>

<span data-ttu-id="65eaf-107">Vous pouvez surveiller l’état de tous les objets qui sont configurés pour prendre en charge les statistiques d’objets et les rapports d’événements.</span><span class="sxs-lookup"><span data-stu-id="65eaf-107">You can monitor status for any objects that are configured to support object statistics and event reporting.</span></span> <span data-ttu-id="65eaf-108">L’activation des statistiques d’objets a une légère baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="65eaf-108">Enabling object statistics has a very slight performance overhead.</span></span>

<span data-ttu-id="65eaf-109">**Pour activer les statistiques d’objets**</span><span class="sxs-lookup"><span data-stu-id="65eaf-109">**To enable object statistics**</span></span>

1.  <span data-ttu-id="65eaf-110">Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="65eaf-110">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="65eaf-111">Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **activation** .</span><span class="sxs-lookup"><span data-stu-id="65eaf-111">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="65eaf-112">Pour activer les statistiques d’objet pour le composant, sous **contexte d’activation**, activez la case à cocher le **composant prend en charge les événements et les statistiques** .</span><span class="sxs-lookup"><span data-stu-id="65eaf-112">To enable object statistics for the component, under **Activation Context**, select the **Component supports events and statistics** check box.</span></span>

<span data-ttu-id="65eaf-113">**Pour surveiller l’état des objets**</span><span class="sxs-lookup"><span data-stu-id="65eaf-113">**To monitor object status**</span></span>

1.  <span data-ttu-id="65eaf-114">Dans l’arborescence de la console de l’outil d’administration Services de composants, ouvrez le dossier de l’application qui comprend les composants que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="65eaf-114">In the console tree of the Component Services administrative tool, open the folder for the application that includes the components you want to monitor.</span></span>

2.  <span data-ttu-id="65eaf-115">Cliquez avec le bouton droit sur le dossier **composants** , pointez sur **affichage**, puis cliquez sur **affichage des États**.</span><span class="sxs-lookup"><span data-stu-id="65eaf-115">Right-click the **Components** folder, point to **View**, and then click **Status View**.</span></span> <span data-ttu-id="65eaf-116">Le volet d’informations affiche désormais l’affichage de l’État pour tous les composants de l’application.</span><span class="sxs-lookup"><span data-stu-id="65eaf-116">The details pane now displays the status view for all components in the application.</span></span> <span data-ttu-id="65eaf-117">Le tableau suivant décrit les six colonnes de la vue d’État.</span><span class="sxs-lookup"><span data-stu-id="65eaf-117">The following table describes the six columns in the status view.</span></span>

    

    | <span data-ttu-id="65eaf-118">Colonne</span><span class="sxs-lookup"><span data-stu-id="65eaf-118">Column</span></span>                        | <span data-ttu-id="65eaf-119">Description</span><span class="sxs-lookup"><span data-stu-id="65eaf-119">Description</span></span>                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="65eaf-120">**ProgID**</span><span class="sxs-lookup"><span data-stu-id="65eaf-120">**ProgID**</span></span><br/>         | <span data-ttu-id="65eaf-121">Identifie un composant spécifique.</span><span class="sxs-lookup"><span data-stu-id="65eaf-121">Identifies a specific component.</span></span><br/>                                                                                                                                                                                |
    | <span data-ttu-id="65eaf-122">**Objets**</span><span class="sxs-lookup"><span data-stu-id="65eaf-122">**Objects**</span></span><br/>        | <span data-ttu-id="65eaf-123">Affiche le nombre d’objets actuellement détenus par les références du client.</span><span class="sxs-lookup"><span data-stu-id="65eaf-123">Shows the number of objects that are currently held by client references.</span></span><br/>                                                                                                                                       |
    | <span data-ttu-id="65eaf-124">**Activat**</span><span class="sxs-lookup"><span data-stu-id="65eaf-124">**Activated**</span></span><br/>      | <span data-ttu-id="65eaf-125">Affiche le nombre d’objets actuellement activés.</span><span class="sxs-lookup"><span data-stu-id="65eaf-125">Shows the number of objects that are currently activated.</span></span> <br/>                                                                                                                                                      |
    | <span data-ttu-id="65eaf-126">**Mis en pool**</span><span class="sxs-lookup"><span data-stu-id="65eaf-126">**Pooled**</span></span><br/>         | <span data-ttu-id="65eaf-127">Affiche le nombre total d’objets créés par le pool, y compris les objets en cours d’utilisation et les objets qui sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="65eaf-127">Shows the total number of objects created by the pool, including objects that are in use and objects that are deactivated.</span></span><br/>                                                                                      |
    | <span data-ttu-id="65eaf-128">**Dans l’appel**</span><span class="sxs-lookup"><span data-stu-id="65eaf-128">**In Call**</span></span><br/>        | <span data-ttu-id="65eaf-129">Identifie des objets dans l’appel.</span><span class="sxs-lookup"><span data-stu-id="65eaf-129">Identifies objects in call.</span></span><br/>                                                                                                                                                                                     |
    | <span data-ttu-id="65eaf-130">**Durée de l’appel (MS)**</span><span class="sxs-lookup"><span data-stu-id="65eaf-130">**Call Time (ms)**</span></span><br/> | <span data-ttu-id="65eaf-131">Affiche la durée moyenne de l’appel (en millisecondes) des appels de méthode effectués au cours des 20 dernières secondes (jusqu’à 20 appels).</span><span class="sxs-lookup"><span data-stu-id="65eaf-131">Shows the average call duration (in milliseconds) of method calls made in the last 20 seconds (up to 20 calls).</span></span> <span data-ttu-id="65eaf-132">L’heure de l’appel est mesurée au niveau de l’objet et n’inclut pas le temps utilisé pour traverser le réseau.</span><span class="sxs-lookup"><span data-stu-id="65eaf-132">Call time is measured at the object and does not include the time used to traverse the network.</span></span><br/> |

    

     

## <a name="related-topics"></a><span data-ttu-id="65eaf-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65eaf-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65eaf-134">Configuration d’un composant à regrouper</span><span class="sxs-lookup"><span data-stu-id="65eaf-134">Configuring a Component to Be Pooled</span></span>](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




