---
description: Vous pouvez lancer une vue enracinée d’un point de jonction par le biais d’un fichier de raccourci vers ce point de jonction.
title: Comment ouvrir une vue enracinée d’un point de jonction à l’aide d’un fichier de raccourci
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52096f0dbbcebadb60e2612f0304ed497199b2ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581607"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="97fa5-103">Comment ouvrir une vue enracinée d’un point de jonction à l’aide d’un fichier de raccourci</span><span class="sxs-lookup"><span data-stu-id="97fa5-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="97fa5-104">Vous pouvez lancer une vue enracinée d’un point de jonction par le biais d’un [fichier de raccourci](./links.md) vers ce point de jonction.</span><span class="sxs-lookup"><span data-stu-id="97fa5-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="97fa5-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="97fa5-105">Instructions</span></span>


<span data-ttu-id="97fa5-106">Définissez la ligne cible du fichier de raccourci sur Explorer.exe avec un indicateur/root.</span><span class="sxs-lookup"><span data-stu-id="97fa5-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="97fa5-107">La forme exacte de la commande dépend de l’emplacement du point de jonction :</span><span class="sxs-lookup"><span data-stu-id="97fa5-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="97fa5-108">Si le point de jonction est un sous-dossier du bureau, utilisez :</span><span class="sxs-lookup"><span data-stu-id="97fa5-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="97fa5-109">Si le point de jonction est un dossier de système de fichiers, utilisez :</span><span class="sxs-lookup"><span data-stu-id="97fa5-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="97fa5-110">Si le point de jonction est un sous-dossier d’un dossier virtuel système, utilisez :</span><span class="sxs-lookup"><span data-stu-id="97fa5-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="97fa5-111">Les dossiers virtuels système qui peuvent contenir des points de jonction ont les identificateurs de classe suivants (CLSID) :</span><span class="sxs-lookup"><span data-stu-id="97fa5-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    | <span data-ttu-id="97fa5-112">Dossier système</span><span class="sxs-lookup"><span data-stu-id="97fa5-112">System folder</span></span>     | <span data-ttu-id="97fa5-113">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="97fa5-113">Class identifier</span></span>                       |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="97fa5-114">Poste de travail</span><span class="sxs-lookup"><span data-stu-id="97fa5-114">My Computer</span></span>       | <span data-ttu-id="97fa5-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="97fa5-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="97fa5-116">Favoris réseau</span><span class="sxs-lookup"><span data-stu-id="97fa5-116">My Network Places</span></span> | <span data-ttu-id="97fa5-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="97fa5-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="97fa5-118">Control panel</span><span class="sxs-lookup"><span data-stu-id="97fa5-118">Control Panel</span></span>     | <span data-ttu-id="97fa5-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="97fa5-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="97fa5-120">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="97fa5-120">Internet Explorer</span></span> | <span data-ttu-id="97fa5-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="97fa5-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="97fa5-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97fa5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97fa5-123">Spécification de l’emplacement d’une extension d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="97fa5-123">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="97fa5-124">Comment ouvrir une vue enracinée d’un point de jonction dans le registre</span><span class="sxs-lookup"><span data-stu-id="97fa5-124">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
