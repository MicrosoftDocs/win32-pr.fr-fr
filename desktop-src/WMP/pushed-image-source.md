---
title: Source de l’image Push
description: Source de l’image Push
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Apparences mobiles du lecteur Windows Media, source de l’image du bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673902"
---
# <a name="pushed-image-source"></a><span data-ttu-id="1969e-108">Source de l’image Push</span><span class="sxs-lookup"><span data-stu-id="1969e-108">Pushed Image Source</span></span>

<span data-ttu-id="1969e-109">Vous devez définir la source de l’image que vous souhaitez afficher lorsque l’utilisateur exécute un push sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="1969e-109">You must define the source of the image you want to display when the user pushes a button.</span></span> <span data-ttu-id="1969e-110">L’image provient du fichier que vous avez défini comme faisant l’objet d’un push dans la section bitmaps.</span><span class="sxs-lookup"><span data-stu-id="1969e-110">The image comes from the file you defined as Pushed in the Bitmaps section.</span></span> <span data-ttu-id="1969e-111">Vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace.</span><span class="sxs-lookup"><span data-stu-id="1969e-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="1969e-112">Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées supérieure et gauche (en pixels) de l’image que vous souhaitez utiliser dans le fichier d’image faisant l’objet d’un push.</span><span class="sxs-lookup"><span data-stu-id="1969e-112">You must then enter two positive integers that define the top and left coordinates (in pixels) of the image you want to use inside the Pushed image file.</span></span> <span data-ttu-id="1969e-113">L’emplacement d’affichage de l’image provient des coordonnées définies pour le bouton par rapport à l’image d’arrière-plan. Toutefois, l’emplacement à partir duquel il provient est défini par les deux nombres suivants « push @ » et est relatif à l’image Poussée à partir de laquelle vous lisez l’image.</span><span class="sxs-lookup"><span data-stu-id="1969e-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image; but the location it comes from is defined by the two numbers following "Pushed @" and is relative to the Pushed image you are reading the image from.</span></span>

<span data-ttu-id="1969e-114">Par exemple, pour utiliser une image de l’image faisant l’objet d’un push qui se trouve dans le fichier ayant fait l’objet d’un push dont l’emplacement en haut à gauche est de 50, 60, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="1969e-114">For example, to use an image from the Pushed image that is in the Pushed file whose top-left location is 50,60 you would use the following code:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="1969e-115">Si vous ne souhaitez pas afficher une autre image, vous pouvez définir la bitmap d’arrière-plan en tant que bitmap push.</span><span class="sxs-lookup"><span data-stu-id="1969e-115">If you do not want to display a different image, you can define the Background bitmap as your Pushed bitmap.</span></span> <span data-ttu-id="1969e-116">Pour ce faire, spécifiez le fichier d’arrière-plan comme fichier faisant l’objet d’un push et spécifiez le décalage vers l’angle supérieur gauche du bouton :</span><span class="sxs-lookup"><span data-stu-id="1969e-116">To do this, specify the Background file as your pushed file and specify the offset to the top-left corner of the button:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="1969e-117">Si vous procédez ainsi, aucun de vos boutons ne peut afficher une image faisant l’objet d’un push.</span><span class="sxs-lookup"><span data-stu-id="1969e-117">If you do this, none of your buttons can display a Pushed image.</span></span> <span data-ttu-id="1969e-118">Nous vous recommandons d’afficher une image Push pour tous les boutons pour donner une indication visuelle à votre utilisateur, car il n’est pas toujours évident de savoir si un TAP produit un résultat, en particulier lorsque la musique est jouée ou que le bruit de frappe est désactivé.</span><span class="sxs-lookup"><span data-stu-id="1969e-118">We recommend that you display a Pushed image for all buttons to give your user a visual indication, because it is not always clear whether a tap produces a result, especially when music is playing or the tapping sound is turned off.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1969e-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1969e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1969e-120">**Boutons**</span><span class="sxs-lookup"><span data-stu-id="1969e-120">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




