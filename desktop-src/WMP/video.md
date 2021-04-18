---
title: Vidéo (Windows Media Player SDK)
description: Vidéo
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player Mobile Skins, vidéo
- apparences, vidéo
- référence pour les enveloppes, vidéo
- vidéo dans les apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106512767"
---
# <a name="video-windows-media-player-sdk"></a><span data-ttu-id="3fab8-107">Vidéo (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="3fab8-107">Video (Windows Media Player SDK)</span></span>

<span data-ttu-id="3fab8-108">Un affichage vidéo permet à l’utilisateur d’afficher des fichiers vidéo numériques.</span><span class="sxs-lookup"><span data-stu-id="3fab8-108">A video display allows the user to view digital video files.</span></span> <span data-ttu-id="3fab8-109">La zone d’affichage vidéo est visible uniquement lorsque la vidéo est en mode de diffusion ou en pause.</span><span class="sxs-lookup"><span data-stu-id="3fab8-109">The video display area is only visible when video is playing or paused.</span></span> <span data-ttu-id="3fab8-110">Lorsque vous concevez votre apparence, vous souhaiterez réserver de l’espace dans l’image d’arrière-plan pour contenir l’affichage vidéo.</span><span class="sxs-lookup"><span data-stu-id="3fab8-110">When you design your skin, you will want to reserve space in the Background image to contain the video display.</span></span> <span data-ttu-id="3fab8-111">Si vous ne le faites pas, l’affichage vidéo peut se superposer sur n’importe quelle illustration visible, comme le fichier d’arrière-plan, les boutons et les trackbars, ce qui empêchera l’utilisateur d’utiliser les contrôles sur votre apparence.</span><span class="sxs-lookup"><span data-stu-id="3fab8-111">If you don't, the video display may superimpose itself over any visible art, such as the Background file, buttons, and trackbars, which will keep the user from operating the controls on your skin.</span></span>

<span data-ttu-id="3fab8-112">La section vidéo du fichier de définition d’apparence doit commencer par cette ligne :</span><span class="sxs-lookup"><span data-stu-id="3fab8-112">The Video section of the skin definition file must begin with this line:</span></span>


```C++
[ Video ]

```



<span data-ttu-id="3fab8-113">Vous devez ensuite ajouter une ligne qui spécifie l’emplacement et la taille de la zone d’affichage de la vidéo dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="3fab8-113">You then must add a line that specifies the location and size of the video display area in your skin.</span></span>


```C++
0,38,240,172

```



<span data-ttu-id="3fab8-114">Vous pouvez utiliser le modèle suivant pour la section vidéo de votre fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="3fab8-114">You can use the following template for the Video section of your skin definition file:</span></span>


```C++
//  <Location>
//  ----------

```



<span data-ttu-id="3fab8-115">Les sections suivantes fournissent des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3fab8-115">The following sections provide further details.</span></span>

-   [<span data-ttu-id="3fab8-116">Emplacement de la vidéo</span><span class="sxs-lookup"><span data-stu-id="3fab8-116">Video Location</span></span>](video-location.md)
-   [<span data-ttu-id="3fab8-117">Source de l’image vidéo</span><span class="sxs-lookup"><span data-stu-id="3fab8-117">Video Image Source</span></span>](video-image-source.md)
-   [<span data-ttu-id="3fab8-118">Taille de la vidéo</span><span class="sxs-lookup"><span data-stu-id="3fab8-118">Video Size</span></span>](video-size.md)
-   [<span data-ttu-id="3fab8-119">Exemple de section vidéo</span><span class="sxs-lookup"><span data-stu-id="3fab8-119">Sample Video Section</span></span>](sample-video-section.md)

## <a name="related-topics"></a><span data-ttu-id="3fab8-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3fab8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fab8-121">**Référence d’apparence**</span><span class="sxs-lookup"><span data-stu-id="3fab8-121">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




