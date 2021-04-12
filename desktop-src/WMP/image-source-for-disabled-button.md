---
title: Source de l’image pour le bouton désactivé
description: Source de l’image pour le bouton désactivé
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Apparences mobiles du lecteur Windows Media, source de l’image du bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379967"
---
# <a name="image-source-for-disabled-button"></a><span data-ttu-id="2f8b6-108">Source de l’image pour le bouton désactivé</span><span class="sxs-lookup"><span data-stu-id="2f8b6-108">Image Source for Disabled Button</span></span>

<span data-ttu-id="2f8b6-109">Vous devez définir la source de l’image que vous souhaitez afficher lorsqu’un bouton est désactivé ou un État qui correspond à OFF.</span><span class="sxs-lookup"><span data-stu-id="2f8b6-109">You must define the source of the image you want to display when a button is disabled or has a state that corresponds to off.</span></span> <span data-ttu-id="2f8b6-110">L’image provient du fichier que vous avez défini comme étant désactivé dans la section bitmaps.</span><span class="sxs-lookup"><span data-stu-id="2f8b6-110">The image comes from the file you defined as Disabled in the Bitmaps section.</span></span> <span data-ttu-id="2f8b6-111">Vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace.</span><span class="sxs-lookup"><span data-stu-id="2f8b6-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="2f8b6-112">Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image que vous souhaitez utiliser dans le fichier bitmap.</span><span class="sxs-lookup"><span data-stu-id="2f8b6-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap file.</span></span> <span data-ttu-id="2f8b6-113">L’emplacement d’affichage de l’image provient des coordonnées définies pour le bouton par rapport à l’image d’arrière-plan, mais l’emplacement à partir duquel elle provient est défini par les deux nombres suivants : « Disabled @ » et est relatif à l’image bitmap désactivée à partir de laquelle vous lisez l’image.</span><span class="sxs-lookup"><span data-stu-id="2f8b6-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image, but the location it comes from is defined by the two numbers following "Disabled @" and is relative to the Disabled bitmap you are reading the image from.</span></span>

<span data-ttu-id="2f8b6-114">Par exemple, pour utiliser une image de la bitmap désactivée qui se trouve dans le fichier désactivé à un emplacement supérieur et gauche de 50, 60 pixels, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="2f8b6-114">For example, to use an image from the Disabled bitmap that is in the Disabled file at a top and left location of 50,60 pixels, use the following code:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="2f8b6-115">Vous devez définir une image bitmap désactivée.</span><span class="sxs-lookup"><span data-stu-id="2f8b6-115">You must define a Disabled bitmap.</span></span> <span data-ttu-id="2f8b6-116">Si vous ne souhaitez pas afficher une image différente, vous pouvez définir la bitmap d’arrière-plan en tant que bitmap désactivé avec un décalage de 0, 0 :</span><span class="sxs-lookup"><span data-stu-id="2f8b6-116">If you do not want to display a different image, you can define the Background bitmap as your Disabled bitmap with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="2f8b6-117">Dans l’exemple précédent, 50, 60 correspond à l’emplacement du bouton que vous utilisez dans le fichier désactivé (dans ce cas, le même emplacement que le bouton sur la bitmap d’arrière-plan).</span><span class="sxs-lookup"><span data-stu-id="2f8b6-117">In the preceding example, 50,60 is the location of the button you are working with in the Disabled file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="2f8b6-118">Toutefois, il est fortement recommandé d’afficher une image désactivée pour tous les boutons afin de fournir à vos utilisateurs une indication visuelle, car de nombreux boutons ne sont pas utilisables dans certaines conditions, par exemple une sélection vide.</span><span class="sxs-lookup"><span data-stu-id="2f8b6-118">However, it is highly recommended that you display a Disabled image for all buttons to give your users a visual indication, because many buttons will not be useable under certain conditions, such as an empty playlist.</span></span> <span data-ttu-id="2f8b6-119">Si les utilisateurs savent qu’un bouton est désactivé, ils n’essaient pas de cliquer dessus ou pensent que votre apparence ne fonctionne pas comme prévu.</span><span class="sxs-lookup"><span data-stu-id="2f8b6-119">If users know a button is disabled, they will not keep trying to click on it or think your skin is not functioning as designed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f8b6-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f8b6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f8b6-121">**Boutons**</span><span class="sxs-lookup"><span data-stu-id="2f8b6-121">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




