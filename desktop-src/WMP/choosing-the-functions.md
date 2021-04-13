---
title: Choix des fonctions
description: Choix des fonctions
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Windows Media Player Mobile Skins, fonctions pour l’audio
- Skins, fonctions pour l’audio
- création d’apparences, fonctions pour l’audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380295"
---
# <a name="choosing-the-functions"></a><span data-ttu-id="c3105-106">Choix des fonctions</span><span class="sxs-lookup"><span data-stu-id="c3105-106">Choosing the Functions</span></span>

<span data-ttu-id="c3105-107">L’objectif de cette apparence est de fournir des fonctionnalités de base pour la lecture audio.</span><span class="sxs-lookup"><span data-stu-id="c3105-107">The purpose of this skin is to provide basic functionality for playing audio.</span></span> <span data-ttu-id="c3105-108">Les fonctions suivantes sont utilisées :</span><span class="sxs-lookup"><span data-stu-id="c3105-108">The following functions will be used:</span></span>



| <span data-ttu-id="c3105-109">Fonction</span><span class="sxs-lookup"><span data-stu-id="c3105-109">Function</span></span>                     | <span data-ttu-id="c3105-110">Description</span><span class="sxs-lookup"><span data-stu-id="c3105-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3105-111">PlayPause ou PlayPauseStop\*</span><span class="sxs-lookup"><span data-stu-id="c3105-111">PlayPause or PlayPauseStop\*</span></span> | <span data-ttu-id="c3105-112">Le démarrage de l’élément multimédia est de première importance.</span><span class="sxs-lookup"><span data-stu-id="c3105-112">Starting the media item is of prime importance.</span></span> <span data-ttu-id="c3105-113">Si vous créez une apparence pour Windows Media Player 10 mobile ou version ultérieure, vous devez utiliser PlayPauseStop.</span><span class="sxs-lookup"><span data-stu-id="c3105-113">If you are creating a skin for Windows Media Player 10 Mobile or later, then you should use PlayPauseStop.</span></span> <span data-ttu-id="c3105-114">Si vous utilisez une version antérieure du lecteur Windows Media Mobile, vous devez utiliser PlayPause.</span><span class="sxs-lookup"><span data-stu-id="c3105-114">If you are working with an earlier version of Windows Media Player Mobile, then you must use PlayPause.</span></span> <span data-ttu-id="c3105-115">Les deux fonctions vous offrent les fonctionnalités supplémentaires de pause, mais seules les PlayPauseStop vous permettent d’arrêter une diffusion en direct lorsque la fonctionnalité de pause n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c3105-115">Both functions give you the added functionality of pausing, but only PlayPauseStop allows you to stop a live broadcast when pause functionality is not available.</span></span> |
| <span data-ttu-id="c3105-116">Arrêter</span><span class="sxs-lookup"><span data-stu-id="c3105-116">Stop</span></span>                         | <span data-ttu-id="c3105-117">Vous pouvez ajouter arrêter pour arrêter la diffusion de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c3105-117">You will want to add Stop to stop playing the item.</span></span> <span data-ttu-id="c3105-118">Si vous créez une apparence pour Windows Media Player 10 mobile ou version ultérieure, la fonction PlayPauseStop fournit déjà cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c3105-118">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop function already provides this functionality.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="c3105-119">Suivant</span><span class="sxs-lookup"><span data-stu-id="c3105-119">Next</span></span>                         | <span data-ttu-id="c3105-120">Si vous avez une sélection, vous pouvez choisir l’élément suivant.</span><span class="sxs-lookup"><span data-stu-id="c3105-120">If you have a playlist, you will want to be able to choose the next item.</span></span> <span data-ttu-id="c3105-121">Vous en avez besoin pour une navigation de base sur les médias numériques.</span><span class="sxs-lookup"><span data-stu-id="c3105-121">You need this for basic navigation of digital media.</span></span>                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c3105-122">Précédent</span><span class="sxs-lookup"><span data-stu-id="c3105-122">Prev</span></span>                         | <span data-ttu-id="c3105-123">Si vous pouvez utiliser Next pour parcourir la sélection jusqu’au début, l’ajout de PREV permettra à l’utilisateur de revenir en arrière et de transférer facilement lors de la navigation dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="c3105-123">While you could use Next to cycle through the playlist until you came to the beginning, adding Prev will make it easy for the user to go backward as well as forward when navigating the playlist.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="c3105-124">VolumeUp ou VolumeDown\*</span><span class="sxs-lookup"><span data-stu-id="c3105-124">VolumeUp or VolumeDown\*</span></span>     | <span data-ttu-id="c3105-125">Vous pouvez fournir à l’utilisateur la possibilité d’activer ou de désactiver le volume.</span><span class="sxs-lookup"><span data-stu-id="c3105-125">You will want to provide the user with the ability to turn the volume up or down.</span></span>                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="c3105-126">\*Disponible pour Windows Media Player 10 mobile ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c3105-126">\*Available for Windows Media Player 10 Mobile or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3105-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3105-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3105-128">**Repère d’apparence**</span><span class="sxs-lookup"><span data-stu-id="c3105-128">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




