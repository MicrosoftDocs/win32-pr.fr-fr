---
title: Démarrage des téléchargements
description: Démarrage des téléchargements
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Windows Media Player Online stores, démarrage des téléchargements
- magasins en ligne, démarrage des téléchargements
- tapez 2 magasins en ligne, à partir de téléchargements
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
- démarrage des téléchargements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380325"
---
# <a name="starting-the-downloads"></a><span data-ttu-id="91af5-113">Démarrage des téléchargements</span><span class="sxs-lookup"><span data-stu-id="91af5-113">Starting the Downloads</span></span>

<span data-ttu-id="91af5-114">Le téléchargement démarre lorsque l’utilisateur clique sur **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="91af5-114">The downloading starts when the user clicks **Download**.</span></span> <span data-ttu-id="91af5-115">Ce bouton est nommé btnDownload dans le code et la fonction du gestionnaire d’événements pour l’événement **OnClick** est nommée « OnDownload ».</span><span class="sxs-lookup"><span data-stu-id="91af5-115">This button is named btnDownload in the code and the event handler function for the **onClick** event is named "OnDownload".</span></span>

<span data-ttu-id="91af5-116">« OnDownload » crée d’abord un nouvel objet **DownloadCollection** vide et l’assigne à une variable locale.</span><span class="sxs-lookup"><span data-stu-id="91af5-116">"OnDownload" first creates a new empty **DownloadCollection** object and assigns it to a local variable.</span></span>


```C++
oDLC = g_oManager.createDownloadCollection();

```



<span data-ttu-id="91af5-117">Ensuite, la fonction démarre chacun des cinq éléments qui sont téléchargés et stocke l’objet **DownloadItem** retourné dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="91af5-117">Next, the function starts each of the five items downloading and stores the returned **DownloadItem** object in an array.</span></span>


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



<span data-ttu-id="91af5-118">Le code met ensuite à jour les éléments de l’interface utilisateur avec les informations relatives à la collection de téléchargements et à ses éléments de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="91af5-118">The code then updates the user interface elements with the information about the download collection and its download items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91af5-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91af5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91af5-120">**Utilisation du gestionnaire de téléchargement**</span><span class="sxs-lookup"><span data-stu-id="91af5-120">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




