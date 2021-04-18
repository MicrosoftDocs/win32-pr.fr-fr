---
title: Ajout d’une vidéo
description: Ajout d’une vidéo
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- création d’apparences, vidéo
- Apparences du lecteur Windows Media, vidéo
- apparences, vidéo
- vidéo dans les apparences, ajout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509194"
---
# <a name="adding-video"></a><span data-ttu-id="07f45-107">Ajout d’une vidéo</span><span class="sxs-lookup"><span data-stu-id="07f45-107">Adding Video</span></span>

<span data-ttu-id="07f45-108">Vous pouvez ajouter une vidéo à votre fichier en utilisant simplement l’élément **Video** et en définissant l’emplacement où vous souhaitez placer la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="07f45-108">You can add a video to your file by simply using the **VIDEO** element and defining where you want the video window to be placed.</span></span>

<span data-ttu-id="07f45-109">Utilisez le même code que celui que vous avez fait dans la section choix des fichiers ; il vous suffit d’ajouter l’élément **vidéo** avec les attributs haut, gauche, largeur et hauteur.</span><span class="sxs-lookup"><span data-stu-id="07f45-109">Use the same code as you did in the Choosing Files section; all you need to do is add the **VIDEO** element with the top, left, width, and height attributes.</span></span>


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



<span data-ttu-id="07f45-110">Ensuite, lorsque vous lisez une vidéo, elle s’affiche dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="07f45-110">Then when you play a video, it will be displayed in the window.</span></span> <span data-ttu-id="07f45-111">L’illustration de l’exemple de vidéo a été modifiée pour obtenir une apparence légèrement plus grande.</span><span class="sxs-lookup"><span data-stu-id="07f45-111">The art for the video sample was modified to make a slightly larger skin.</span></span> <span data-ttu-id="07f45-112">Comme les couches étaient utilisées dans Photoshop, les boutons étaient facilement déplacés et un nouvel ensemble a été créé très rapidement.</span><span class="sxs-lookup"><span data-stu-id="07f45-112">Because layers were used in Photoshop, the buttons were easily moved around and a new set was created very quickly.</span></span> <span data-ttu-id="07f45-113">Seule l’image d’arrière-plan a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="07f45-113">Only the background image was changed.</span></span> <span data-ttu-id="07f45-114">Un remplissage a été utilisé dans une couche vide et un effet de biseau et de relief a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="07f45-114">A fill was used in a blank layer and a bevel and emboss effect was added.</span></span>

<span data-ttu-id="07f45-115">Vous pouvez voir une apparence de vidéo similaire dans la section exemple du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="07f45-115">You can see a similar working video skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07f45-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07f45-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07f45-117">**Guide de création d’apparence**</span><span class="sxs-lookup"><span data-stu-id="07f45-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




