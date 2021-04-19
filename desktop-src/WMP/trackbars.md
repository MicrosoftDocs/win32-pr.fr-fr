---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Windows Media Player Mobile Skins, trackbars
- habillages, trackbars
- informations de référence sur les habillages, trackbars
- trackbars dans les habillages, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511445"
---
# <a name="trackbars"></a><span data-ttu-id="49ba5-107">Trackbars</span><span class="sxs-lookup"><span data-stu-id="49ba5-107">Trackbars</span></span>

<span data-ttu-id="49ba5-108">Un TrackBar affiche une image qui change par petits incréments.</span><span class="sxs-lookup"><span data-stu-id="49ba5-108">A trackbar displays an image that changes in small increments.</span></span> <span data-ttu-id="49ba5-109">Les Trackbars sont utilisés pour les contrôles de volume et les contrôles de position de lecture.</span><span class="sxs-lookup"><span data-stu-id="49ba5-109">Trackbars are used for volume controls and playback position controls.</span></span> <span data-ttu-id="49ba5-110">Vous pouvez utiliser trackbars pour afficher des informations sur l’élément multimédia en cours ou pour permettre à l’utilisateur de modifier les paramètres ou la position de lecture.</span><span class="sxs-lookup"><span data-stu-id="49ba5-110">You can use trackbars to display information about the current media item or to allow the user to change settings or playback position.</span></span> <span data-ttu-id="49ba5-111">Par exemple, vous pouvez utiliser un TrackBar pour permettre à l’utilisateur d’ajuster le volume, et un autre TrackBar qui peut montrer à l’utilisateur la position de lecture actuelle.</span><span class="sxs-lookup"><span data-stu-id="49ba5-111">For example, you can use a trackbar to enable the user to adjust the volume, and another trackbar that can show the user the current playback position.</span></span> <span data-ttu-id="49ba5-112">Trackbars ont une image Thumb qui définit le paramètre actuel de la valeur TrackBar.</span><span class="sxs-lookup"><span data-stu-id="49ba5-112">Trackbars have a thumb image that defines the current setting of the trackbar value.</span></span>

<span data-ttu-id="49ba5-113">La section Trackbars du fichier de définition d’apparence doit commencer par cette ligne :</span><span class="sxs-lookup"><span data-stu-id="49ba5-113">The Trackbars section of the skin definition file must begin with this line:</span></span>


```C++
[ Trackbars ]

```



<span data-ttu-id="49ba5-114">Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur chacun des trackbars dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="49ba5-114">You then must add one or more lines that contain information about each of the trackbars in your skin.</span></span>


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



<span data-ttu-id="49ba5-115">Vous pouvez utiliser le modèle suivant pour la section Trackbars de votre fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="49ba5-115">You can use the following template for the Trackbars section of your skin definition file:</span></span>


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



<span data-ttu-id="49ba5-116">Vous devez utiliser l’ordre suivant pour les informations de TrackBar pour chaque ligne dans la section Trackbars (chaque partie de la ligne est requise) :</span><span class="sxs-lookup"><span data-stu-id="49ba5-116">You must use the following order for trackbar information for each line in the Trackbars section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="49ba5-117">TrackBar, type</span><span class="sxs-lookup"><span data-stu-id="49ba5-117">Trackbar Type</span></span>](trackbar-type.md)
2.  [<span data-ttu-id="49ba5-118">Emplacement de la barre de TrackBar</span><span class="sxs-lookup"><span data-stu-id="49ba5-118">Trackbar Location</span></span>](trackbar-location.md)
3.  [<span data-ttu-id="49ba5-119">Source de l’image pour le TrackBar désactivé</span><span class="sxs-lookup"><span data-stu-id="49ba5-119">Image Source for Disabled Trackbar</span></span>](image-source-for-disabled-trackbar.md)
4.  [<span data-ttu-id="49ba5-120">Source de l’image Thumb</span><span class="sxs-lookup"><span data-stu-id="49ba5-120">Thumb Image Source</span></span>](thumb-image-source.md)
5.  [<span data-ttu-id="49ba5-121">Taille de curseur</span><span class="sxs-lookup"><span data-stu-id="49ba5-121">Thumb Size</span></span>](thumb-size.md)

<span data-ttu-id="49ba5-122">Pour obtenir un exemple de code Trackbars, consultez la [section exemple de Trackbars](sample-trackbars-section.md).</span><span class="sxs-lookup"><span data-stu-id="49ba5-122">For an example of Trackbars code, see [Sample Trackbars Section](sample-trackbars-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="49ba5-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49ba5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49ba5-124">**Référence d’apparence**</span><span class="sxs-lookup"><span data-stu-id="49ba5-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




