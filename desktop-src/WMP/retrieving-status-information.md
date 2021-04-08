---
title: Récupération des informations d’État
description: Récupération des informations d’État
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Magasins en ligne du lecteur Windows Media, récupération de l’État
- magasins en ligne, récupération de l’État
- type 2 magasins en ligne, récupération de l’État
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
- récupération de l’État
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674681"
---
# <a name="retrieving-status-information"></a><span data-ttu-id="3307a-113">Récupération des informations d’État</span><span class="sxs-lookup"><span data-stu-id="3307a-113">Retrieving Status Information</span></span>

<span data-ttu-id="3307a-114">Les informations d’État sont mises à jour à l’aide de la minuterie créée dans la fonction **init** .</span><span class="sxs-lookup"><span data-stu-id="3307a-114">Status information is updated using the timer created in the **Init** function.</span></span> <span data-ttu-id="3307a-115">Tous les États sont mis à jour à l’aide du même minuteur.</span><span class="sxs-lookup"><span data-stu-id="3307a-115">All status is updated using the same timer.</span></span> <span data-ttu-id="3307a-116">Le nom de la fonction pour l’événement du minuteur est **OnTimer**.</span><span class="sxs-lookup"><span data-stu-id="3307a-116">The name of the function for the timer event is **OnTimer**.</span></span>

<span data-ttu-id="3307a-117">**OnTimer** détermine les informations à afficher en fonction de la sélection de l’utilisateur, qui est stockée dans la variable globale nommée g \_ oCurrentDLItem.</span><span class="sxs-lookup"><span data-stu-id="3307a-117">**OnTimer** determines the information to display based upon the user selection, which is stored in the global variable named g\_oCurrentDLItem.</span></span> <span data-ttu-id="3307a-118">La fonction teste d’abord si les valeurs de taille ou de progression sont valides et crée une chaîne pour chaque cas.</span><span class="sxs-lookup"><span data-stu-id="3307a-118">The function first tests whether the size or progress values are valid and creates a string for each case.</span></span>


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



<span data-ttu-id="3307a-119">Si une valeur est valide, la chaîne représente le nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="3307a-119">If a value is valid, the string represents the byte count.</span></span> <span data-ttu-id="3307a-120">Si la valeur n’est pas valide, telle que-1, la chaîne fournit un message pour informer l’utilisateur que les informations ne sont pas encore disponibles.</span><span class="sxs-lookup"><span data-stu-id="3307a-120">If the value is not valid, such as -1, the string provides a message to inform the user that the information is not yet available.</span></span>

<span data-ttu-id="3307a-121">Ensuite, un bloc **switch** détermine si le téléchargement de l’élément sélectionné est terminé ou annulé.</span><span class="sxs-lookup"><span data-stu-id="3307a-121">Next, a **switch** block determines whether the download for the selected item is completed or canceled.</span></span> <span data-ttu-id="3307a-122">Si l’un ou l’autre cas est true, la valeur de la taille ou de la progression des variables est mise à jour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="3307a-122">If either case is true, the value of the variables Size or Progress is updated accordingly.</span></span>


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



<span data-ttu-id="3307a-123">Enfin, les informations d’État s’affichent dans l’élément DIV nommé dlstate.</span><span class="sxs-lookup"><span data-stu-id="3307a-123">Finally, the status information is displayed in the DIV element named dlstate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3307a-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3307a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3307a-125">**Utilisation du gestionnaire de téléchargement**</span><span class="sxs-lookup"><span data-stu-id="3307a-125">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




