---
description: Le fait de cliquer sur exécuter des experts dans la fenêtre experts de l’interface utilisateur du Moniteur réseau démarre les experts sélectionnés pour le fichier de capture et appelle la fonction exécuter. Une fois démarré, l’expert analyse le fichier de capture à l’aide de plusieurs fonctions de cadre d’experts.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Démarrer et exécuter des experts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539745"
---
# <a name="starting-and-running-experts"></a><span data-ttu-id="aacf8-104">Démarrer et exécuter des experts</span><span class="sxs-lookup"><span data-stu-id="aacf8-104">Starting and Running Experts</span></span>

<span data-ttu-id="aacf8-105">Le fait de cliquer sur **exécuter des experts** dans la fenêtre experts de l’interface utilisateur du moniteur réseau démarre les experts sélectionnés pour le fichier de capture et appelle la fonction [**exécuter**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="aacf8-105">Clicking **Run Experts** from the Experts window of the Network Monitor UI starts the experts selected for the capture file and calls the [**Run**](run.md) function.</span></span> <span data-ttu-id="aacf8-106">Une fois démarré, l’expert analyse le fichier de capture à l’aide de plusieurs fonctions de cadre d’experts.</span><span class="sxs-lookup"><span data-stu-id="aacf8-106">When started, the expert analyzes the capture file by using several expert frame functions.</span></span>

<span data-ttu-id="aacf8-107">La fonction [**ExpertIndicateStatus**](expertindicatestatus.md) fournit des informations d’état de l’expert.</span><span class="sxs-lookup"><span data-stu-id="aacf8-107">The [**ExpertIndicateStatus**](expertindicatestatus.md) function provides status information from the expert.</span></span> <span data-ttu-id="aacf8-108">Lorsque vous exécutez un expert avec Moniteur réseau, la fenêtre d’affichage de l’état des experts affiche des informations d’État mises à jour régulièrement (de 0 à 100% de la progression).</span><span class="sxs-lookup"><span data-stu-id="aacf8-108">When you run an expert with Network Monitor, the Expert Status View window displays periodically updated status information (from 0 to 100 percent completion).</span></span>

![fenêtre d’affichage de l’État expert](images/exview.png)

<span data-ttu-id="aacf8-110">L’expert est actif jusqu’à ce que les données se terminent par le fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="aacf8-110">The expert is active until the data completes its pass though the capture file.</span></span> <span data-ttu-id="aacf8-111">Une fois la passe terminée, une fenêtre de observateur d’événements s’affiche.</span><span class="sxs-lookup"><span data-stu-id="aacf8-111">When the pass is complete, an Event Viewer window appears.</span></span> <span data-ttu-id="aacf8-112">Les informations contenues dans cette fenêtre dépendent du type d’expert qui a analysé les données.</span><span class="sxs-lookup"><span data-stu-id="aacf8-112">The information in this window depends on the type of expert that analyzed the data.</span></span> <span data-ttu-id="aacf8-113">L’illustration suivante montre une vue de l’expert distribution de propriétés, qui résume les données de frame analysées par l’expert.</span><span class="sxs-lookup"><span data-stu-id="aacf8-113">The following illustration shows a Property Distribution Expert view, which summarizes the frame data that the expert analyzed.</span></span>

![vue expert distribution de propriété](images/exview1.png)

<span data-ttu-id="aacf8-115">Un deuxième rapport (non affiché) résume les résultats de l’expert de retransmission TCP (Transmission Control Protocol).</span><span class="sxs-lookup"><span data-stu-id="aacf8-115">A second report (not shown), summarizes the results of the Transmission Control Protocol (TCP) Retransmit expert.</span></span>

<span data-ttu-id="aacf8-116">Vous pouvez également :</span><span class="sxs-lookup"><span data-stu-id="aacf8-116">You can also:</span></span>

-   <span data-ttu-id="aacf8-117">Créez une entrée pour une page de référence d’événement qui conseille l’utilisateur de problèmes ou de conditions détectés (comme indiqué dans la fenêtre d’analyse).</span><span class="sxs-lookup"><span data-stu-id="aacf8-117">Create an entry for an event reference page (ERP) that advises the user of detected conditions or problems (as shown in the Analysis window).</span></span>
-   <span data-ttu-id="aacf8-118">Créez des entrées pour les corrections suggérées ou des données explicatives qui fournissent des informations supplémentaires (comme indiqué dans la fenêtre de résolution).</span><span class="sxs-lookup"><span data-stu-id="aacf8-118">Create entries for suggested fixes or explanatory data that provide additional information (as shown in the Resolution window).</span></span>

<span data-ttu-id="aacf8-119">Une fois que l’expert a terminé sa tâche, Moniteur réseau supprime l’expert de la mémoire active.</span><span class="sxs-lookup"><span data-stu-id="aacf8-119">After the expert completes its task, Network Monitor removes the expert from active memory.</span></span> <span data-ttu-id="aacf8-120">Les experts doivent utiliser les fonctions de mémoire protégée incluses dans le kit de développement logiciel (SDK) de la plateforme. ces fonctions nettoient la mémoire si les experts échouent au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="aacf8-120">Experts should use the protected memory functions included in the Platform Software Development Kit (SDK); these functions clean up memory if the experts fail during run time.</span></span>

 

 



