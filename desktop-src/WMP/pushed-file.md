---
title: Fichier Push
description: Fichier Push
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Windows Media Player Mobile Skins, fichiers art
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, les fichiers envoyés
- Windows Media Player Mobile Skins, fichiers envoyés
- apparences, fichiers envoyés
- Fichiers faisant l’objet d’un push dans des habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380025"
---
# <a name="pushed-file"></a><span data-ttu-id="fe83c-110">Fichier Push</span><span class="sxs-lookup"><span data-stu-id="fe83c-110">Pushed File</span></span>

<span data-ttu-id="fe83c-111">Le fichier faisant l’objet d’un push contient les images qui seront affichées lorsque l’utilisateur appuie sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="fe83c-111">The Pushed file contains the images that will be displayed when the user taps on a button.</span></span> <span data-ttu-id="fe83c-112">Vous pouvez également inclure les images normales et faisant l’objet d’un push pour l’état de pause du bouton PlayPause.</span><span class="sxs-lookup"><span data-stu-id="fe83c-112">You can also include the normal and pushed images for the pause state of the PlayPause button.</span></span>

<span data-ttu-id="fe83c-113">L’image suivante est un fichier Push type.</span><span class="sxs-lookup"><span data-stu-id="fe83c-113">The following image is a typical Pushed file.</span></span>

![fichier Push](images/cesdkpus.png)

<span data-ttu-id="fe83c-115">Cela permet de stocker les images qui seront affichées lorsque les boutons de type d’accès sont frappés.</span><span class="sxs-lookup"><span data-stu-id="fe83c-115">This stores the images that will be displayed when the hit-type buttons are tapped.</span></span> <span data-ttu-id="fe83c-116">Également stocké dans ce fichier sont les images normales et Push de l’image suspendue du bouton PlayPause.</span><span class="sxs-lookup"><span data-stu-id="fe83c-116">Also stored in this file are the normal and pushed images for the paused image of the PlayPause button.</span></span> <span data-ttu-id="fe83c-117">À l’exception des images secondaires PlayPause sur la droite, les autres images de bouton sont alignées avec l’image d’arrière-plan, à l’aide de l’offset défini dans la section bitmaps du fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="fe83c-117">Except for the PlayPause secondary images on the right, the other button images line up with the Background image, using the offset defined in the Bitmaps section of the skin definition file.</span></span>

<span data-ttu-id="fe83c-118">Notez que l’arrière-plan de l’image de bouton correspond exactement à la zone correspondante dans le fichier d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="fe83c-118">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="fe83c-119">Cela est important, car quand l’utilisateur appuie sur un bouton de type d’accès, le rectangle entier défini pour l’image Push remplace la zone correspondante dans le fichier d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="fe83c-119">This is important, because when the user taps a hit-type button, the entire rectangle defined for the pushed image will replace the matching area in the Background file.</span></span> <span data-ttu-id="fe83c-120">Conservez le graphique cohérent avec l’image d’arrière-plan pour vous assurer que seules les parties du bouton que vous souhaitez voir apparaître varient.</span><span class="sxs-lookup"><span data-stu-id="fe83c-120">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe83c-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe83c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe83c-122">**Fichiers art**</span><span class="sxs-lookup"><span data-stu-id="fe83c-122">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




