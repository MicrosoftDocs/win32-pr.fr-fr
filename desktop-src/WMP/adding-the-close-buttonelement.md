---
title: Ajout du BUTTONELEMENT étroit
description: Ajout du BUTTONELEMENT étroit
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- créer des apparences, BUTTONELEMENT, élément
- Apparences du lecteur Windows Media, BUTTONELEMENT, élément
- Skins, BUTTONELEMENT, élément
- fichiers de définition d’apparence, élément BUTTONELEMENT
- Élément BUTTONELEMENT
- éléments, BUTTONELEMENT
- création d’apparences, boutons Fermer
- Apparences du lecteur Windows Media, boutons de fermeture
- apparences, boutons Fermer
- fichiers de définition d’apparence, boutons Fermer
- Boutons Fermer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196869"
---
# <a name="adding-the-close-buttonelement"></a><span data-ttu-id="59ade-114">Ajout du BUTTONELEMENT étroit</span><span class="sxs-lookup"><span data-stu-id="59ade-114">Adding the Close BUTTONELEMENT</span></span>

<span data-ttu-id="59ade-115">Le bouton Fermer est similaire au concept de bouton de lecture, mais il a des codes et des couleurs différents.</span><span class="sxs-lookup"><span data-stu-id="59ade-115">The Close button is similar in concept to the Play button, but has different codes and colors.</span></span>

<span data-ttu-id="59ade-116">Placez le code **BUTTONELEMENT** étroit après le crochet pointu fermant du **BUTTONELEMENT** Play.</span><span class="sxs-lookup"><span data-stu-id="59ade-116">Put the Close **BUTTONELEMENT** code after the closing angle bracket of the Play **BUTTONELEMENT**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



<span data-ttu-id="59ade-117">Les attributs suivants sont utilisés pour définir **BUTTONELEMENT** pour le bouton Fermer :</span><span class="sxs-lookup"><span data-stu-id="59ade-117">The following attributes are used to define the **BUTTONELEMENT** for the Close button:</span></span>

<span data-ttu-id="59ade-118">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="59ade-118">**mappingColor**</span></span>

<span data-ttu-id="59ade-119">Il s’agit de la valeur de couleur de la région dans le fichier art de mappage que vous avez créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="59ade-119">This is the color value of the region in the mapping art file you created before.</span></span> <span data-ttu-id="59ade-120">Dans ce cas, il s’agit de la couleur rouge unie.</span><span class="sxs-lookup"><span data-stu-id="59ade-120">In this case it is the solid red color.</span></span> <span data-ttu-id="59ade-121">Cet attribut est obligatoire pour tout **BUTTONELEMENT**.</span><span class="sxs-lookup"><span data-stu-id="59ade-121">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="59ade-122">En définissant cette couleur, vous indiquez au lecteur Windows Media d’associer cette zone de couleur au code XML de ce bouton.</span><span class="sxs-lookup"><span data-stu-id="59ade-122">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="59ade-123">**Info-bulle**</span><span class="sxs-lookup"><span data-stu-id="59ade-123">**upToolTip**</span></span>

<span data-ttu-id="59ade-124">Définit le texte qui s’affiche lorsque l’utilisateur pointe la souris sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="59ade-124">This defines the text that will be displayed when the user hovers the mouse over the button.</span></span> <span data-ttu-id="59ade-125">C’est le même que le bouton de lecture, sauf qu’il est étiqueté « Close » (fermer).</span><span class="sxs-lookup"><span data-stu-id="59ade-125">This is the same as the Play button except that it is labeled "Close".</span></span>

<span data-ttu-id="59ade-126">**onClick**</span><span class="sxs-lookup"><span data-stu-id="59ade-126">**onClick**</span></span>

<span data-ttu-id="59ade-127">Cela définit l’événement qui se produit lorsque la souris clique sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="59ade-127">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="59ade-128">La valeur de cet attribut d’événement est appelée gestionnaire d’événements et sera soit une ligne de code Microsoft JScript, soit une fonction JScript dans un fichier texte externe qui est chargée par l’attribut **loadScript** d’une **vue**.</span><span class="sxs-lookup"><span data-stu-id="59ade-128">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="59ade-129">Dans ce cas, le code JScript appelle la méthode **Close** de l’élément **View** à l’aide de la **vue** global Attribute, qui ferme la vue et arrête le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="59ade-129">In this case, the JScript code calls the **close** method of the **VIEW** element using the global attribute **view**, which closes the view and shuts down Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59ade-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59ade-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59ade-131">**Création du fichier de définition d’apparence**</span><span class="sxs-lookup"><span data-stu-id="59ade-131">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




