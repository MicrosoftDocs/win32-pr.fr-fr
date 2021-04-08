---
title: Utilisation de Moniteur réseau pour afficher les fichiers ETL
description: Moniteur réseau 3,3 permet aux utilisateurs d’analyser, de filtrer et d’afficher un fichier ETL (à l’aide de Windows Vista ou version ultérieure).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "103953289"
---
# <a name="using-network-monitor-to-view-etl-files"></a><span data-ttu-id="2067c-103">Utilisation de Moniteur réseau pour afficher les fichiers ETL</span><span class="sxs-lookup"><span data-stu-id="2067c-103">Using Network Monitor to View ETL Files</span></span>

<span data-ttu-id="2067c-104">[Moniteur réseau 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) permet aux utilisateurs d’analyser, de filtrer et d’afficher un fichier ETL (à l’aide de Windows Vista ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="2067c-104">[Network Monitor 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) enables users to parse, filter, and view an ETL file (using Windows Vista or later).</span></span> <span data-ttu-id="2067c-105">(Si vous utilisez Moniteur réseau 3,2, vous devrez télécharger et installer des analyseurs supplémentaires à partir de [CodePlex](https://www.codeplex.com/NMParsers) pour afficher les événements de suivi réseau.)</span><span class="sxs-lookup"><span data-stu-id="2067c-105">(If using Network Monitor 3.2, you will need to download and install additional parsers from [CodePlex](https://www.codeplex.com/NMParsers) in order to render the network tracing events.)</span></span>

<span data-ttu-id="2067c-106">Les fichiers ETL corrélés regroupent les événements pertinents ensemble.</span><span class="sxs-lookup"><span data-stu-id="2067c-106">Correlated ETL files group the relevant events together.</span></span> <span data-ttu-id="2067c-107">Le défilement ci-dessous montre un fichier corrélé ouvert dans Moniteur réseau, avec la conversation activée.</span><span class="sxs-lookup"><span data-stu-id="2067c-107">The illlustration below shows a correlated file opened in Network Monitor, with conversation enabled.</span></span>

![Capture d’écran montrant le Moniteur réseau, avec les événements corrélés mis en surbrillance dans la fenêtre de gauche et les UTEvent mis en surbrillance dans la liste déroulante.](images/ut-netmon1.png)

<span data-ttu-id="2067c-109">Les événements corrélés sont regroupés par activité dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="2067c-109">Correlated events are grouped by activity in the left pane.</span></span> <span data-ttu-id="2067c-110">Vous pouvez sélectionner un événement dans le volet Résumé des frames, puis cliquer avec le bouton droit pour sélectionner la conversation au niveau de l’événement réseau.</span><span class="sxs-lookup"><span data-stu-id="2067c-110">You can select an event in the Frame Summary pane, then right-click to select the conversation at the network event level.</span></span> <span data-ttu-id="2067c-111">Une activité associée s’affiche dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="2067c-111">This will display a related activity in the left pane.</span></span>

<span data-ttu-id="2067c-112">La sélection d’une activité particulière dans le volet gauche et son développement affichent la liste des fournisseurs pour les événements corrélés.</span><span class="sxs-lookup"><span data-stu-id="2067c-112">Selecting a particular activity from the left pane and expanding it will show the list of providers for the correlated events.</span></span>

![Capture d’écran montrant le Moniteur réseau avec une activité sélectionnée dans le volet gauche et des événements correspondant à cet événement dans le volet droit.](images/ut-netmon2.png)

<span data-ttu-id="2067c-114">Lorsque vous sélectionnez un fournisseur spécifique dans le volet gauche, une liste d’événements spécifiques à ce fournisseur et à cette activité s’affiche dans le volet Résumé des frames.</span><span class="sxs-lookup"><span data-stu-id="2067c-114">When you select a specific provider in the left pane, a list of events specific to that provider and activity will be displayed in the Frame Summary pane.</span></span>

![Capture d’écran montrant un fournisseur spécifique sélectionné dans le volet gauche et une liste d’événements spécifiques au fournisseur mis en surbrillance dans le volet supérieur droit.](images/ut-netmon3.png)

<span data-ttu-id="2067c-116">Les filtres peuvent être appliqués dans Moniteur réseau pour faciliter l’affichage et la recherche des événements ou des paquets appropriés.</span><span class="sxs-lookup"><span data-stu-id="2067c-116">Filters can be applied in Network Monitor to make it easier to view and find the right events or packet.</span></span> <span data-ttu-id="2067c-117">Par exemple, vous pouvez appliquer un filtre aux événements d’erreur sélectionnés (par exemple, **UTEvent. Header. Descriptor. Level = = 2**) pour les afficher dans une certaine couleur.</span><span class="sxs-lookup"><span data-stu-id="2067c-117">For example, you can apply a filter to selected error events (for example, **UTEvent.Header.Descriptor.Level == 2**) to display them in a certain color.</span></span>

![Capture d’écran montrant la boîte de dialogue Modifier le filtre de couleurs.](images/ut-netmon4.png)

<span data-ttu-id="2067c-119">Des filtres peuvent également être appliqués pour marquer des fournisseurs différents dans des couleurs différentes afin de faciliter l’affichage des résultats.</span><span class="sxs-lookup"><span data-stu-id="2067c-119">Filters can also be applied to mark different providers in different colors so that the results are easier to view.</span></span>

![Capture d’écran montrant un exemple de différents fournisseurs marqués dans des couleurs différentes.](images/ut-netmon5.png)

<span data-ttu-id="2067c-121">Pour appliquer un filtre, cliquez sur **ColorFilters** dans le menu **filtres** .</span><span class="sxs-lookup"><span data-stu-id="2067c-121">To apply a filter, click **ColorFilters** on the **Filters** menu.</span></span>

<span data-ttu-id="2067c-122">Le tableau suivant présente quelques exemples de filtres utiles.</span><span class="sxs-lookup"><span data-stu-id="2067c-122">The following table shows some examples of useful filters.</span></span>



| <span data-ttu-id="2067c-123">Filtrer</span><span class="sxs-lookup"><span data-stu-id="2067c-123">Filter</span></span>                                                                        | <span data-ttu-id="2067c-124">Description</span><span class="sxs-lookup"><span data-stu-id="2067c-124">Description</span></span>                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2067c-125">UTEvent. Header. Descriptor. Level = = 2</span><span class="sxs-lookup"><span data-stu-id="2067c-125">UTEvent.Header.Descriptor.Level == 2</span></span>                                          | <span data-ttu-id="2067c-126">Filtre uniquement les événements d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2067c-126">Filters only error events.</span></span>                                        |
| <span data-ttu-id="2067c-127">UTEvent. Header. Descriptor. Level = = 3</span><span class="sxs-lookup"><span data-stu-id="2067c-127">UTEvent.Header.Descriptor.Level == 3</span></span>                                          | <span data-ttu-id="2067c-128">Filtre uniquement les événements d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="2067c-128">Filters only warning events.</span></span>                                      |
| <span data-ttu-id="2067c-129">UTEvent.Header.Descriptor.Id = = 2001</span><span class="sxs-lookup"><span data-stu-id="2067c-129">UTEvent.Header.Descriptor.Id == 2001</span></span>                                          | <span data-ttu-id="2067c-130">Filtre uniquement les événements avec l’ID d’événement 2001.</span><span class="sxs-lookup"><span data-stu-id="2067c-130">Filters only events with event ID 2001.</span></span>                           |
| <span data-ttu-id="2067c-131">\_MICROSOFTWINDOWSWLANAUTOCONFIG WLAN</span><span class="sxs-lookup"><span data-stu-id="2067c-131">WLAN\_MicrosoftWindowsWLANAutoConfig</span></span>                                          | <span data-ttu-id="2067c-132">Filtre uniquement les événements du service WLAN.</span><span class="sxs-lookup"><span data-stu-id="2067c-132">Filters only events from WLAN service.</span></span>                            |
| <span data-ttu-id="2067c-133">N802 \_ MicrosoftWindowsNWiFi</span><span class="sxs-lookup"><span data-stu-id="2067c-133">N802\_MicrosoftWindowsNWiFi</span></span>                                                   | <span data-ttu-id="2067c-134">Filtre uniquement les événements du pilote Wi-Fi natif.</span><span class="sxs-lookup"><span data-stu-id="2067c-134">Filters only events from the Native Wifi driver.</span></span>                  |
| <span data-ttu-id="2067c-135">WLAN \_ MICROSOFTWINDOWSWLANAUTOCONFIG et UTEvent.Header.Descriptor.ID = = 2001</span><span class="sxs-lookup"><span data-stu-id="2067c-135">WLAN\_MicrosoftWindowsWLANAutoConfig AND UTEvent.Header.Descriptor.Id == 2001</span></span> | <span data-ttu-id="2067c-136">Filtre uniquement les événements avec l’ID d’événement 2001 émis à partir du service WLAN.</span><span class="sxs-lookup"><span data-stu-id="2067c-136">Filters only events with event ID 2001 emitted from WLAN service.</span></span> |



 

 

 




