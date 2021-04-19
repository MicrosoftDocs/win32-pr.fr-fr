---
title: Super fichiers
description: Super fichiers
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Windows Media Player Mobile Skins, fichiers art
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, fichiers de fichiers Super
- Windows Media Player Mobile Skins, fichiers Super fichiers
- apparences, Super fichiers
- Super fichiers dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513485"
---
# <a name="super-files"></a><span data-ttu-id="b8fc3-110">Super fichiers</span><span class="sxs-lookup"><span data-stu-id="b8fc3-110">Super Files</span></span>

<span data-ttu-id="b8fc3-111">Les fichiers Super sont utilisés pour stocker les images désactivées pour trackbars.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-111">Super files are used to store the Disabled images for trackbars.</span></span> <span data-ttu-id="b8fc3-112">Étant donné que l’image de TrackBar principale est affichée dans le fichier d’arrière-plan et que l’utilisateur appuie sur l’image Thumb, et non sur l’image TrackBar, seule l’image désactivée est nécessaire pour trackbars.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-112">Because the main trackbar image is displayed in the Background file, and the user taps on the thumb image, not the trackbar image, only the Disabled image is needed for trackbars.</span></span> <span data-ttu-id="b8fc3-113">Elle est stockée dans le fichier défini par Super dans la section bitmaps du fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-113">It is stored in the file defined by Super in the Bitmaps section of the skin definition file.</span></span> <span data-ttu-id="b8fc3-114">Un fichier Super peut également stocker les images déplacées et désactivées pour d’autres boutons tels que muet, ce qui ne doit pas nécessairement être un bouton de type d’accès.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-114">A Super file can also store the Pushed and Disabled images for other buttons such as Mute, which is not required to be a hit-type button.</span></span>

> [!Note]  
> <span data-ttu-id="b8fc3-115">Les fichiers Super art ne sont pas utilisés dans les habillages pour Windows Media Player 10 mobile ou version ultérieure, car les images désactivées pour Seek trackbars se trouvent dans le fichier seekthumb.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-115">Super art files are not used in skins for Windows Media Player 10 Mobile or later because the disabled images for seek trackbars are located in the seekthumb file.</span></span>

 

<span data-ttu-id="b8fc3-116">L’image suivante est un fichier Super standard.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-116">The following image is a typical Super file.</span></span>

![Super fichier](images/cesdksup.png)

<span data-ttu-id="b8fc3-118">Cela stocke les images désactivées pour trackbars et le bouton muet.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-118">This stores the disabled images for the trackbars and the mute button.</span></span> <span data-ttu-id="b8fc3-119">Ces images sont décalées comme défini par la section bitmaps.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-119">These images are offset as defined by the Bitmaps section.</span></span>

<span data-ttu-id="b8fc3-120">La zone d’arrière-plan de l’image TrackBar désactivée correspond exactement à la zone correspondante dans le fichier d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-120">The background area of the disabled trackbar image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="b8fc3-121">C’est important, car le rectangle entier défini pour l’image TrackBar désactivée remplace la zone correspondante dans le fichier d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-121">This is important, because the entire rectangle defined for the disabled trackbar image will replace the matching area in the Background file.</span></span> <span data-ttu-id="b8fc3-122">Cela garantit que l’image TrackBar désactivée est mélangée de façon transparente dans l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-122">This ensures that the disabled trackbar image blends seamlessly into the background image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8fc3-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8fc3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8fc3-124">**Fichiers art**</span><span class="sxs-lookup"><span data-stu-id="b8fc3-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




