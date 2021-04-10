---
title: Exemple de code de rendu
description: Exemple de code de rendu
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- visualisations, exemple de code
- visualisations personnalisées, exemple de code
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- Fonction Render, exemple de code
- exemples, fonction Render pour les visualisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029452"
---
# <a name="sample-render-code"></a><span data-ttu-id="0c264-109">Exemple de code de rendu</span><span class="sxs-lookup"><span data-stu-id="0c264-109">Sample Render Code</span></span>

<span data-ttu-id="0c264-110">Voici un exemple de code qui utilise la fonction **Render** pour dessiner une ligne sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="0c264-110">Here is some sample code that uses the **Render** function to draw a line across the screen.</span></span> <span data-ttu-id="0c264-111">La hauteur de la ligne est définie par la valeur de la forme d’onde.</span><span class="sxs-lookup"><span data-stu-id="0c264-111">The height of the line is defined by the waveform value.</span></span>


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



<span data-ttu-id="0c264-112">La fonction **Render** est l’endroit où s’effectue le travail principal de votre code.</span><span class="sxs-lookup"><span data-stu-id="0c264-112">The **Render** function is where the main work of your code takes place.</span></span> <span data-ttu-id="0c264-113">Chaque fois que le lecteur Windows Media prend un instantané de l’audio, il appellera cette fonction et votre code s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="0c264-113">Every time Windows Media Player takes a snapshot of the audio, it will call this function and your code will run.</span></span>

<span data-ttu-id="0c264-114">Ce code effectue les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="0c264-114">This code performs the following tasks.</span></span> <span data-ttu-id="0c264-115">Pour plus d’informations sur des fonctions spécifiques, consultez le kit de développement logiciel (SDK) de plate-forme Microsoft Windows pour Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0c264-115">Refer to the Microsoft Windows Platform SDK for 32-bit Windows for more details about specific functions.</span></span>

## <a name="creating-objects"></a><span data-ttu-id="0c264-116">Création d'objets</span><span class="sxs-lookup"><span data-stu-id="0c264-116">Creating Objects</span></span>

<span data-ttu-id="0c264-117">En général, vous utilisez les fonctions de dessin fournies avec l’interface GDI (Graphical Display Interface) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0c264-117">Usually you will be using the drawing functions that come with the Microsoft Windows Graphical Display Interface (GDI).</span></span> <span data-ttu-id="0c264-118">Vous devez créer des stylets pour dessiner des lignes et des pinceaux pour remplir des zones.</span><span class="sxs-lookup"><span data-stu-id="0c264-118">You need to create pens to draw lines and brushes to fill areas.</span></span>

<span data-ttu-id="0c264-119">Un pinceau noir Uni est créé pour remplir l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="0c264-119">A solid black brush is created to fill in the background.</span></span>

<span data-ttu-id="0c264-120">Un stylet plein est créé pour dessiner une ligne.</span><span class="sxs-lookup"><span data-stu-id="0c264-120">A solid pen is created to draw a line.</span></span> <span data-ttu-id="0c264-121">La couleur sera la couleur de premier plan telle qu’elle est définie par l’apparence qui va afficher la visualisation.</span><span class="sxs-lookup"><span data-stu-id="0c264-121">The color will be the foreground color as defined by the skin that is going to display the visualization.</span></span>

## <a name="adding-the-object-to-the-dc"></a><span data-ttu-id="0c264-122">Ajout de l’objet au contrôleur de l’objet</span><span class="sxs-lookup"><span data-stu-id="0c264-122">Adding the Object to the DC</span></span>

<span data-ttu-id="0c264-123">Vous devez ajouter le stylet au contexte de périphérique (DC).</span><span class="sxs-lookup"><span data-stu-id="0c264-123">You need to add the pen to the device context (DC).</span></span> <span data-ttu-id="0c264-124">Le contrôleur de schéma est la partie de mémoire dans laquelle sont stockées toutes les données et tous les objets de dessin.</span><span class="sxs-lookup"><span data-stu-id="0c264-124">The DC is the portion of memory that all drawing data and objects are stored in.</span></span> <span data-ttu-id="0c264-125">Fondamentalement, le DC est le gestionnaire de trafic de fenêtre qui effectue le suivi de tous les graphiques.</span><span class="sxs-lookup"><span data-stu-id="0c264-125">Essentially the DC is the window traffic manager that keeps track of everything graphical.</span></span>

<span data-ttu-id="0c264-126">Vous devez *effectuer un cast* de l’objet Pen que vous avez créé et le stocker comme un vieux stylet.</span><span class="sxs-lookup"><span data-stu-id="0c264-126">You need to *cast* the pen object you created and store it as an old pen.</span></span> <span data-ttu-id="0c264-127">Utilisez cette technique de codage pour tous les nouveaux stylets.</span><span class="sxs-lookup"><span data-stu-id="0c264-127">Use this coding technique for all new pens.</span></span> <span data-ttu-id="0c264-128">Cette technique est requise pour la programmation 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0c264-128">This technique is required for 32-bit programming.</span></span>

## <a name="filling-in-the-background"></a><span data-ttu-id="0c264-129">Remplissage de l’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="0c264-129">Filling in the Background</span></span>

<span data-ttu-id="0c264-130">Vous êtes maintenant prêt à dessiner.</span><span class="sxs-lookup"><span data-stu-id="0c264-130">You now are ready to draw.</span></span> <span data-ttu-id="0c264-131">La fonction **fillRect** remplit le rectangle de la fenêtre, comme défini par les paramètres de la fonction **Render** .</span><span class="sxs-lookup"><span data-stu-id="0c264-131">The **FillRect** function will fill the rectangle of the window, as defined by the parameters of the **Render** function.</span></span> <span data-ttu-id="0c264-132">Le rectangle est rempli d’un pinceau noir.</span><span class="sxs-lookup"><span data-stu-id="0c264-132">The rectangle is filled with a black brush.</span></span>

## <a name="getting-audio-data"></a><span data-ttu-id="0c264-133">Obtention de données audio</span><span class="sxs-lookup"><span data-stu-id="0c264-133">Getting Audio Data</span></span>

<span data-ttu-id="0c264-134">Ensuite, le code obtient des données audio à partir du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0c264-134">Next the code gets some audio data from Windows Media Player.</span></span> <span data-ttu-id="0c264-135">En utilisant le tableau de forme d’onde, vous pouvez récupérer la valeur actuelle de la puissance audio au moment où la capture instantanée a été prise.</span><span class="sxs-lookup"><span data-stu-id="0c264-135">By using the waveform array, you can get the current value of the audio power at the moment the snapshot was taken.</span></span> <span data-ttu-id="0c264-136">Dans ce cas, vous prenez les données audio du canal de gauche.</span><span class="sxs-lookup"><span data-stu-id="0c264-136">In this case, you are taking the audio data of the left channel.</span></span> <span data-ttu-id="0c264-137">La première valeur du tableau est le premier 1024th de l’instantané d’alimentation audio.</span><span class="sxs-lookup"><span data-stu-id="0c264-137">The first value in the array is the first 1024th of the audio power snapshot.</span></span>

<span data-ttu-id="0c264-138">Ces informations seront utilisées pour afficher une ligne dont la hauteur correspondra à l’instantané d’alimentation audio.</span><span class="sxs-lookup"><span data-stu-id="0c264-138">This information will be used to display a line whose height will match the audio power snapshot.</span></span>

## <a name="draw-the-line"></a><span data-ttu-id="0c264-139">Dessiner la ligne</span><span class="sxs-lookup"><span data-stu-id="0c264-139">Draw the Line</span></span>

<span data-ttu-id="0c264-140">La ligne est dessinée de gauche à droite à l’aide des fonctions GDI **MoveToEx** et **LineTo** .</span><span class="sxs-lookup"><span data-stu-id="0c264-140">The line is drawn from left to right using the **MoveToEx** and **LineTo** GDI functions.</span></span>

<span data-ttu-id="0c264-141">Tout d’abord, vous déplacez le stylet vers le point de départ.</span><span class="sxs-lookup"><span data-stu-id="0c264-141">First you move the pen to the starting point.</span></span> <span data-ttu-id="0c264-142">Dans ce cas, x et y sont utilisés pour définir les valeurs de gauche à droite et de haut en bas que l’utilisateur verra sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="0c264-142">In this case, x and y are used to define the left-to-right and top-to-bottom values the user will see on the screen.</span></span> <span data-ttu-id="0c264-143">X est défini par le rectangle PRC et, plus précisément, par la valeur de PRC->gauche.</span><span class="sxs-lookup"><span data-stu-id="0c264-143">X is defined by the rectangle prc and specifically by the value of prc->left.</span></span> <span data-ttu-id="0c264-144">Y est défini en tant que valeur des données de la forme d’onde à ce moment précis.</span><span class="sxs-lookup"><span data-stu-id="0c264-144">Y is defined as the value of the waveform data at that moment.</span></span>

<span data-ttu-id="0c264-145">Ensuite, vous dessinez une ligne à l’autre extrémité de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0c264-145">Then you draw a line to the other side of the window.</span></span> <span data-ttu-id="0c264-146">Le point sur lequel vous dessinez la ligne est une valeur x, y.</span><span class="sxs-lookup"><span data-stu-id="0c264-146">The point you draw the line to is again an x, y value.</span></span> <span data-ttu-id="0c264-147">X est défini par le rectangle PRC, mais cette fois par PRC->droit.</span><span class="sxs-lookup"><span data-stu-id="0c264-147">X is defined by the rectangle prc, but this time by prc->right.</span></span> <span data-ttu-id="0c264-148">Y est toujours défini par les données de forme d’onde et est le même que le point à partir duquel vous avez commencé, car vous dessinez une ligne droite de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="0c264-148">Y is still defined by the waveform data and is the same as the point you started from, because you are drawing a straight line from left to right.</span></span>

## <a name="clean-up-everything"></a><span data-ttu-id="0c264-149">Tout nettoyer</span><span class="sxs-lookup"><span data-stu-id="0c264-149">Clean up Everything</span></span>

<span data-ttu-id="0c264-150">Vous devez supprimer les objets que vous créez.</span><span class="sxs-lookup"><span data-stu-id="0c264-150">You must delete the objects you create.</span></span> <span data-ttu-id="0c264-151">En particulier, vous devez supprimer tous les pinceaux et les stylets que vous créez.</span><span class="sxs-lookup"><span data-stu-id="0c264-151">Specifically you must delete any and all brushes and pens you create.</span></span> <span data-ttu-id="0c264-152">Il est conseillé de supprimer des stylets et des pinceaux lorsque vous avez fini de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="0c264-152">It is good practice to delete pens and brushes when you finish using them.</span></span>

<span data-ttu-id="0c264-153">Si vous ne les supprimez pas avant de terminer l’implémentation de la fonction **Render** , votre visualisation se bloquera dans une minute ou moins.</span><span class="sxs-lookup"><span data-stu-id="0c264-153">If you do not delete them before finishing your implementation of the **Render** function, your visualization will crash in a minute or less.</span></span> <span data-ttu-id="0c264-154">Vous devez tenir compte de vos stylets et de vos pinceaux et détruire chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="0c264-154">You must keep a count of your pens and brushes and destroy every single one.</span></span> <span data-ttu-id="0c264-155">Veillez à ne pas créer de stylets à l’intérieur d’une boucle de code.</span><span class="sxs-lookup"><span data-stu-id="0c264-155">Be especially careful not to create pens inside a code loop.</span></span>

<span data-ttu-id="0c264-156">Utilisez la technique de codage donnée dans l’exemple pour détruire vos stylets et pinceaux.</span><span class="sxs-lookup"><span data-stu-id="0c264-156">Use the coding technique given in the example to destroy your pens and brushes.</span></span>

-   <span data-ttu-id="0c264-157">**Important** Détruisez vos stylets et vos brosses !</span><span class="sxs-lookup"><span data-stu-id="0c264-157">**Important** Destroy your pens and brushes!</span></span>

<span data-ttu-id="0c264-158">Une fois le nettoyage terminé, veillez à retourner S \_ OK pour que le lecteur Windows Media sache que vous avez terminé le dessin.</span><span class="sxs-lookup"><span data-stu-id="0c264-158">When you have finished cleaning up, be sure to return S\_OK so that Windows Media Player knows you are finished drawing.</span></span> <span data-ttu-id="0c264-159">Une fois que vous avez terminé, votre dessin sera transféré dans la fenêtre, un autre instantané sera pris, le **rendu** demandera à votre code de dessiner, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="0c264-159">Once you finish, your drawing will be transferred to the window, another snapshot will be taken, **Render** will ask your code to draw again, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c264-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c264-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c264-161">**Implémentation du rendu**</span><span class="sxs-lookup"><span data-stu-id="0c264-161">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




