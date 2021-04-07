---
title: Exemple d’art simple
description: Exemple d’art simple
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Apparences du lecteur Windows Media, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les habillages, exemples
- Apparences du lecteur Windows Media, exemples
- Skins, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab7b25dc33da70a627f8b0e126d6797b1bcdd9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672873"
---
# <a name="simple-art-example"></a><span data-ttu-id="5c850-109">Exemple d’art simple</span><span class="sxs-lookup"><span data-stu-id="5c850-109">Simple Art Example</span></span>

<span data-ttu-id="5c850-110">Trois fichiers art sont nécessaires pour créer une apparence simple avec deux boutons.</span><span class="sxs-lookup"><span data-stu-id="5c850-110">Three art files are needed to create a simple skin with two buttons.</span></span> <span data-ttu-id="5c850-111">Une image principale et une image de mappage sont nécessaires, et une autre image fournit à l’utilisateur un signal visuel permettant à l’utilisateur de cliquer sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="5c850-111">A primary image and a mapping image are required, and an alternate image provides a visual cue to the user that a button is clickable.</span></span>

<span data-ttu-id="5c850-112">Ces fichiers art ont été créés dans un programme art qui utilise des couches.</span><span class="sxs-lookup"><span data-stu-id="5c850-112">These art files were created in an art program that uses layers.</span></span> <span data-ttu-id="5c850-113">Grâce aux couches, vous pouvez facilement vous assurer que vos images principales, de mappage et de remplacement sont toutes de la même taille et être alignées les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="5c850-113">Using layers makes it easier to make sure that your primary, mapping, and alternate images are all the same size and line up with each other.</span></span>

<span data-ttu-id="5c850-114">Les instructions détaillées sur la création de l’illustration sont dans le [Guide de création d’apparence](skin-creation-guide.md).</span><span class="sxs-lookup"><span data-stu-id="5c850-114">The detailed instructions on creating the art are in the [Skin Creation Guide](skin-creation-guide.md).</span></span>

## <a name="primary-image"></a><span data-ttu-id="5c850-115">Image principale</span><span class="sxs-lookup"><span data-stu-id="5c850-115">Primary Image</span></span>

<span data-ttu-id="5c850-116">L’image principale est une ellipse jaune simple avec deux boutons, 1 rose pour démarrer le lecteur Windows Media et un bouton violet pour l’arrêter.</span><span class="sxs-lookup"><span data-stu-id="5c850-116">The primary image is a simple yellow oval with two buttons, a pink one to start Windows Media Player and purple button to stop it.</span></span> <span data-ttu-id="5c850-117">L’arrière-plan est légèrement plus sombre que l’ovale.</span><span class="sxs-lookup"><span data-stu-id="5c850-117">The background is a slightly darker yellow than the oval.</span></span> <span data-ttu-id="5c850-118">Cette image est représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="5c850-118">This image is shown in the following illustration.</span></span>

![image principale](images/absam01b.png)

<span data-ttu-id="5c850-120">L’image principale provient des images suivantes, chacune dans une couche distincte.</span><span class="sxs-lookup"><span data-stu-id="5c850-120">The primary image was from the following images, each in a separate layer.</span></span> <span data-ttu-id="5c850-121">Tout d’abord, un ovale a été créé avec un effet biseau et relief de couche.</span><span class="sxs-lookup"><span data-stu-id="5c850-121">First an oval was created with a layer bevel and emboss effect.</span></span> <span data-ttu-id="5c850-122">Cette image est représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="5c850-122">This image is shown in the following illustration.</span></span>

![image ovale](images/absam01s.png)

<span data-ttu-id="5c850-124">Les deux boutons ont été créés, ainsi que les effets de biseau et de relief de couche.</span><span class="sxs-lookup"><span data-stu-id="5c850-124">Then the two buttons were created, also with layer bevel and emboss effects.</span></span> <span data-ttu-id="5c850-125">L'illustration ci-dessous décrit cela.</span><span class="sxs-lookup"><span data-stu-id="5c850-125">This is shown in the following illustration.</span></span>

![deux boutons](images/absam01p.png)

<span data-ttu-id="5c850-127">Ensuite, l’arrière-plan de l’image a été créé.</span><span class="sxs-lookup"><span data-stu-id="5c850-127">Next the image background was created.</span></span> <span data-ttu-id="5c850-128">Un jaune légèrement plus sombre a été choisi afin que tout anticrénelage entre l’ovale et l’arrière-plan ne soit pas remarqué.</span><span class="sxs-lookup"><span data-stu-id="5c850-128">A slightly darker yellow was chosen so that any anti-aliasing between the oval and the background will not be noticed.</span></span> <span data-ttu-id="5c850-129">La valeur de couleur est \# CCCC00.</span><span class="sxs-lookup"><span data-stu-id="5c850-129">The color value is \#CCCC00.</span></span> <span data-ttu-id="5c850-130">Cette image est représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="5c850-130">This image is shown in the following illustration.</span></span>

![image d’arrière-plan](images/absam01y.png)

<span data-ttu-id="5c850-132">Les couches qui contiennent ces images ont été rendues visibles et enregistrées sous forme de copie au format bitmap, créant ainsi l’image principale.</span><span class="sxs-lookup"><span data-stu-id="5c850-132">The layers that contained these images were made visible and saved as a copy in bitmap format, creating the primary image.</span></span> <span data-ttu-id="5c850-133">L’image composite principale sera utilisée par l’attribut **BackgroundImage** de l’élément **View** .</span><span class="sxs-lookup"><span data-stu-id="5c850-133">The primary composite image will be used by the **backgroundImage** attribute of the **VIEW** element.</span></span>

## <a name="mapping-image"></a><span data-ttu-id="5c850-134">Image de mappage</span><span class="sxs-lookup"><span data-stu-id="5c850-134">Mapping Image</span></span>

<span data-ttu-id="5c850-135">Une image de mappage est nécessaire pour spécifier quand et où un clic est effectué sur une apparence.</span><span class="sxs-lookup"><span data-stu-id="5c850-135">A mapping image is needed to specify when and where a skin is clicked.</span></span> <span data-ttu-id="5c850-136">Une image de mappage a été créée avec une zone rouge et une zone verte.</span><span class="sxs-lookup"><span data-stu-id="5c850-136">A mapping image was created with a red area and a green area.</span></span> <span data-ttu-id="5c850-137">Cette image est représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="5c850-137">This image is shown in the following illustration.</span></span>

![image de mappage](images/absam01m.png)

<span data-ttu-id="5c850-139">La zone verte sera utilisée pour identifier la zone de l’apparence qui démarrera le lecteur Windows Media et la zone rouge sera utilisée pour l’arrêter.</span><span class="sxs-lookup"><span data-stu-id="5c850-139">The green area will be used to identify the area on the skin that will start Windows Media Player and the red area will be used to stop it.</span></span> <span data-ttu-id="5c850-140">L’image de mappage a la même taille que l’image principale.</span><span class="sxs-lookup"><span data-stu-id="5c850-140">The mapping image is the same size as the primary image.</span></span>

<span data-ttu-id="5c850-141">L’image de mappage a été créée en copiant la couche de bouton sur une nouvelle couche et en désactivant l’effet de biseau et de relief.</span><span class="sxs-lookup"><span data-stu-id="5c850-141">The mapping image was created by copying the button layer to a new layer and turning off the bevel and emboss effect.</span></span> <span data-ttu-id="5c850-142">Les images plates sont nécessaires pour le mappage, car le lecteur Windows Media recherche des valeurs de couleur unique dans chaque zone.</span><span class="sxs-lookup"><span data-stu-id="5c850-142">Flat images are needed for mapping because Windows Media Player will be looking for single color values in each area.</span></span> <span data-ttu-id="5c850-143">Elle peut uniquement Rechercher une couleur que vous définissez, telle que le rouge ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="5c850-143">It can only search for a color you define, such as red (\#FF0000).</span></span> <span data-ttu-id="5c850-144">Si votre image a un biseau ou un autre effet, ce n’est pas tout ce dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="5c850-144">If your image has a bevel or other effect, not all of it will be the exact red you need.</span></span>

<span data-ttu-id="5c850-145">Pour que les boutons de mappage aient une couleur facile à mémoriser, les images ont été remplies avec du rouge pur et du vert pur, mais toute couleur peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="5c850-145">To make the mapping buttons an easy color to remember, the images were filled with pure red and pure green, but any color can be used.</span></span> <span data-ttu-id="5c850-146">Vous devez mémoriser les numéros de couleur de votre mappage afin qu’ils puissent être entrés dans le fichier de définition d’apparence XML.</span><span class="sxs-lookup"><span data-stu-id="5c850-146">You will need to remember the color numbers in your map so that they can be entered in the XML skin definition file.</span></span> <span data-ttu-id="5c850-147">Dans ce cas, Red est \# FF0000 et Green est \# 00FF00.</span><span class="sxs-lookup"><span data-stu-id="5c850-147">In this case, red is \#FF0000 and green is \#00FF00.</span></span>

<span data-ttu-id="5c850-148">Ensuite, lorsque seule la nouvelle couche est visible, l’image a été enregistrée en tant que copie dans un fichier BMP.</span><span class="sxs-lookup"><span data-stu-id="5c850-148">Then, with only the new layer visible, the image was saved as a copy to a BMP file.</span></span> <span data-ttu-id="5c850-149">Elle est appelée par l’attribut **mappingImage** de l’élément **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="5c850-149">It will be called by the **mappingImage** attribute of the **BUTTONGROUP** element.</span></span>

## <a name="alternate-image"></a><span data-ttu-id="5c850-150">Image de remplacement</span><span class="sxs-lookup"><span data-stu-id="5c850-150">Alternate Image</span></span>

<span data-ttu-id="5c850-151">Les autres images ne sont pas requises, mais elles sont très utiles pour fournir des signaux visuels à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5c850-151">Alternate images are not required but are very useful to give visual cues to the user.</span></span> <span data-ttu-id="5c850-152">Dans ce cas, il est recommandé d’utiliser une image de survol afin que l’utilisateur sache quelles zones peuvent être cliquées.</span><span class="sxs-lookup"><span data-stu-id="5c850-152">In this case, a hover image is recommended so that the user knows what areas can be clicked on.</span></span>

<span data-ttu-id="5c850-153">Une image de remplacement a été créée avec deux boutons jaunes.</span><span class="sxs-lookup"><span data-stu-id="5c850-153">An alternate image was created with two yellow buttons.</span></span> <span data-ttu-id="5c850-154">L'illustration ci-dessous décrit cela.</span><span class="sxs-lookup"><span data-stu-id="5c850-154">This is shown in the following illustration.</span></span>

![image de survol](images/absam01h.png)

<span data-ttu-id="5c850-156">L’image de remplacement a été créée en copiant la couche de bouton d’origine sur une nouvelle couche, puis en remplaçant la couleur de remplissage par jaune.</span><span class="sxs-lookup"><span data-stu-id="5c850-156">The alternate image was created by copying the original button layer to a new layer and then changing the fill color to yellow.</span></span> <span data-ttu-id="5c850-157">L’effet de biseau et de relief était conservé.</span><span class="sxs-lookup"><span data-stu-id="5c850-157">The bevel and emboss effect was kept.</span></span> <span data-ttu-id="5c850-158">Une nouvelle couche a été créée et des images ont été ajoutées : la flèche indique « Play » et le carré indique « stop ».</span><span class="sxs-lookup"><span data-stu-id="5c850-158">Then a new layer was created and images were added: the arrow indicates "play" and the square indicates "stop".</span></span> <span data-ttu-id="5c850-159">Ensuite, avec uniquement les nouveaux boutons jaunes et les couches de type visibles, l’image a été enregistrée en tant que copie dans un fichier bitmap.</span><span class="sxs-lookup"><span data-stu-id="5c850-159">Then, with only the new yellow button and type layers visible, the image was saved as a copy to a bitmap file.</span></span>

<span data-ttu-id="5c850-160">Le résultat est que lorsque la souris pointe sur une zone définie par l’image de mappage, l’image de survol s’affiche et avertit le lecteur que s’il clique sur cet endroit, il peut lire ou arrêter le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5c850-160">The result is that when the mouse hovers over an area defined by the mapping image, the hover image will be displayed, alerting the reader that if they click on that spot, they can play or stop Windows Media Player.</span></span>

## <a name="final-image"></a><span data-ttu-id="5c850-161">Image finale</span><span class="sxs-lookup"><span data-stu-id="5c850-161">Final Image</span></span>

<span data-ttu-id="5c850-162">Voici l’image finale de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="5c850-162">Here is the final image of the skin.</span></span>

![image finale](images/absam01f.png)

<span data-ttu-id="5c850-164">Il s’agit de l’image que vous verrez si vous pointez sur le bouton rose à droite.</span><span class="sxs-lookup"><span data-stu-id="5c850-164">And this is the image you will see if you hover over the pink button on the right.</span></span>

![bouton pointer sur la droite](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a><span data-ttu-id="5c850-166">Code XML pour l’exemple de motif</span><span class="sxs-lookup"><span data-stu-id="5c850-166">XML Code for the Art Example</span></span>

<span data-ttu-id="5c850-167">Les détails de l’écriture de code XML sont fournis dans le [Guide de création d’apparence](skin-creation-guide.md), mais pour montrer la quantité de code nécessaire pour créer une apparence de travail, voici le code de l’illustration dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="5c850-167">The details of how to write XML code are given in the [Skin Creation Guide](skin-creation-guide.md), but to show how little code is needed to create a working skin, here is the code for the artwork in this example.</span></span>

<span data-ttu-id="5c850-168">Les boutons prédéfinis sont utilisés pour les fonctions de lecture et d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5c850-168">Predefined buttons are used for the play and stop functions.</span></span> <span data-ttu-id="5c850-169">Vous devez charger un fichier ou une sélection à partir de l’ancre Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5c850-169">You must load a file or playlist from the Windows Media anchor.</span></span> <span data-ttu-id="5c850-170">Lorsque le lecteur Windows Media passe en mode apparence, une petite zone s’affiche dans le coin inférieur droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="5c850-170">When Windows Media Player changes to skin mode, a small box appears in the lower-right corner of the screen.</span></span> <span data-ttu-id="5c850-171">Cette zone est appelée « ancre ».</span><span class="sxs-lookup"><span data-stu-id="5c850-171">This box is called the "anchor".</span></span> <span data-ttu-id="5c850-172">Le fait de cliquer sur l’ancre vous donne les fonctionnalités minimales nécessaires, au cas où une apparence ne permet pas de revenir au mode complet du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5c850-172">Clicking the anchor gives you the minimum functionality needed, in case a skin does not provide a way to return to the full mode of Windows Media Player.</span></span> <span data-ttu-id="5c850-173">L’utilisateur peut basculer entre les modes en utilisant le menu **affichage** en mode complet ou en cliquant sur le point d’ancrage en mode apparence.</span><span class="sxs-lookup"><span data-stu-id="5c850-173">The user can switch between modes by using the **View** menu if in full mode, or by clicking the anchor if in skin mode.</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a><span data-ttu-id="5c850-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c850-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c850-175">**Fichiers art**</span><span class="sxs-lookup"><span data-stu-id="5c850-175">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 




