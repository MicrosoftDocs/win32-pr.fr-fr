---
title: Implémentation de Render, exemple
description: Implémentation de Render, exemple
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- visualisations, exemple d’éclat
- visualisations personnalisées, exemple d’éclat
- Guide de programmation, visualisations
- exemples, visualisation lumineuse
- Exemple de visualisation lumineuse
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- Render (fonction), exemple d’éclat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabc816283113a82c1d5d677dfc0ca8e8887d344
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508277"
---
# <a name="implementing-render-sample"></a><span data-ttu-id="89a04-111">Implémentation de Render, exemple</span><span class="sxs-lookup"><span data-stu-id="89a04-111">Implementing Render Sample</span></span>

<span data-ttu-id="89a04-112">Le code suivant est utilisé pour implémenter la fonction **Render** :</span><span class="sxs-lookup"><span data-stu-id="89a04-112">The following code is used to implement the **Render** function:</span></span>


```C++
STDMETHODIMP CGlow::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    COLORREF mycolor;
    int mylevel = pLevels->waveform[0][0];
    
    switch (m_nPreset)
    {
    case PRESET_RED:
        {
        mycolor = RGB( mylevel, 0, 0);    
        }
        break;
    case PRESET_GREEN:
        {
        mycolor = RGB( 0, mylevel, 0);        
        }
        break;
    case PRESET_BLUE:
        {
        mycolor = RGB( 0, 0, mylevel);        
        }
        break;
    }

     HBRUSH hNewBrush = ::CreateSolidBrush( mycolor );
    ::FillRect( hdc, prc, hNewBrush );

    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }

    return S_OK;
}

```



<span data-ttu-id="89a04-113">Voici une explication du code :</span><span class="sxs-lookup"><span data-stu-id="89a04-113">Here is an explanation of the code:</span></span>

<span data-ttu-id="89a04-114">Une variable nommée *MyColor* est utilisée pour la couleur de l’éclat et est déclarée avec **COLORREF**.</span><span class="sxs-lookup"><span data-stu-id="89a04-114">A variable named *mycolor* is used for the color of the glow and is declared with **COLORREF**.</span></span> <span data-ttu-id="89a04-115">Toutes les couleurs doivent utiliser le type de données **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="89a04-115">All colors should use the **COLORREF** data type.</span></span>

<span data-ttu-id="89a04-116">Une variable nommée *myLevel* est utilisée pour l’instantané de niveau audio Wave.</span><span class="sxs-lookup"><span data-stu-id="89a04-116">A variable named *mylevel* is used for the audio waveform level snapshot.</span></span> <span data-ttu-id="89a04-117">Cette valeur dépend du niveau de puissance réel au moment de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="89a04-117">This value will depend on the actual power level at the moment of the snapshot.</span></span>

<span data-ttu-id="89a04-118">L’instruction **switch** est définie par la présélection que l’utilisateur a choisie sur le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="89a04-118">The **switch** statement is set by the preset that the user has chosen on Windows Media Player.</span></span> <span data-ttu-id="89a04-119">Le choix permet de définir *MyColor* sur la couleur souhaitée (rouge, vert ou bleu).</span><span class="sxs-lookup"><span data-stu-id="89a04-119">The choice will set *mycolor* to the desired color (red, green, or blue).</span></span> <span data-ttu-id="89a04-120">Toutefois, la couleur exacte sera déterminée par le niveau de puissance audio.</span><span class="sxs-lookup"><span data-stu-id="89a04-120">However, the exact color will be determined by the audio power level.</span></span> <span data-ttu-id="89a04-121">Par exemple, si la présélection rouge est choisie, la couleur est un rouge fixe, mais il sera plus clair ou plus sombre en fonction de la forme d’onde audio au moment de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="89a04-121">For example, if the red preset is chosen, the color will be a solid red, but it will be lighter or darker depending on the audio waveform at the moment of the snapshot.</span></span> <span data-ttu-id="89a04-122">Veillez à utiliser la macro **RBG** pour créer votre couleur.</span><span class="sxs-lookup"><span data-stu-id="89a04-122">Be sure to use the **RBG** macro to create your color.</span></span>

<span data-ttu-id="89a04-123">Un pinceau est créé appelé *hNewBrush* et il est utilisé pour remplir le rectangle *PRC* fourni par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="89a04-123">A brush is created called *hNewBrush*, and it is used to fill the *prc* rectangle provided by Windows Media Player.</span></span> <span data-ttu-id="89a04-124">La surface de dessin est le contexte de périphérique *HDC* fourni par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="89a04-124">The drawing surface is the *hdc* device context provided by Windows Media Player.</span></span>

<span data-ttu-id="89a04-125">Le pinceau est supprimé par **SupprimerObjet**.</span><span class="sxs-lookup"><span data-stu-id="89a04-125">The brush is deleted by **DeleteObject**.</span></span> <span data-ttu-id="89a04-126">Veillez à toujours supprimer les stylets ou les pinceaux que vous créez.</span><span class="sxs-lookup"><span data-stu-id="89a04-126">Always be sure to delete any pens or brushes you create.</span></span>

<span data-ttu-id="89a04-127">Une fois le code de **rendu** terminé, le lecteur Windows Media affiche les graphiques *HDC* dans une fenêtre déterminée par l’apparence utilisée.</span><span class="sxs-lookup"><span data-stu-id="89a04-127">Once the **Render** code is finished, Windows Media Player will display the *hdc* graphics in a window determined by the skin being used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89a04-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89a04-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89a04-129">**L’exemple lueur**</span><span class="sxs-lookup"><span data-stu-id="89a04-129">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




