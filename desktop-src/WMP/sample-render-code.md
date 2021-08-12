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
ms.openlocfilehash: 51265191ba7fd8b5eb9e4b1140990a7713eba08356d01c58097c727ec2fe533e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569785"
---
# <a name="sample-render-code"></a>Exemple de code de rendu

Voici un exemple de code qui utilise la fonction **Render** pour dessiner une ligne sur l’écran. La hauteur de la ligne est définie par la valeur de la forme d’onde.


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



La fonction **Render** est l’endroit où s’effectue le travail principal de votre code. chaque fois que Lecteur Windows Media prend un instantané de l’audio, il appellera cette fonction et votre code s’exécutera.

Ce code effectue les tâches suivantes. pour plus d’informations sur des fonctions spécifiques, consultez le kit de développement logiciel (SDK) de plateforme Microsoft Windows pour 32 bits Windows.

## <a name="creating-objects"></a>Création d'objets

en général, vous utilisez les fonctions de dessin fournies avec l’Interface GDI (graphical Display Interface) de Microsoft Windows. Vous devez créer des stylets pour dessiner des lignes et des pinceaux pour remplir des zones.

Un pinceau noir Uni est créé pour remplir l’arrière-plan.

Un stylet plein est créé pour dessiner une ligne. La couleur sera la couleur de premier plan telle qu’elle est définie par l’apparence qui va afficher la visualisation.

## <a name="adding-the-object-to-the-dc"></a>Ajout de l’objet au contrôleur de l’objet

Vous devez ajouter le stylet au contexte de périphérique (DC). Le contrôleur de schéma est la partie de mémoire dans laquelle sont stockées toutes les données et tous les objets de dessin. Fondamentalement, le DC est le gestionnaire de trafic de fenêtre qui effectue le suivi de tous les graphiques.

Vous devez *effectuer un cast* de l’objet Pen que vous avez créé et le stocker comme un vieux stylet. Utilisez cette technique de codage pour tous les nouveaux stylets. Cette technique est requise pour la programmation 32 bits.

## <a name="filling-in-the-background"></a>Remplissage de l’arrière-plan

Vous êtes maintenant prêt à dessiner. La fonction **fillRect** remplit le rectangle de la fenêtre, comme défini par les paramètres de la fonction **Render** . Le rectangle est rempli d’un pinceau noir.

## <a name="getting-audio-data"></a>Obtention de données audio

ensuite, le code obtient des données audio de Lecteur Windows Media. En utilisant le tableau de forme d’onde, vous pouvez récupérer la valeur actuelle de la puissance audio au moment où la capture instantanée a été prise. Dans ce cas, vous prenez les données audio du canal de gauche. La première valeur du tableau est le premier 1024th de l’instantané d’alimentation audio.

Ces informations seront utilisées pour afficher une ligne dont la hauteur correspondra à l’instantané d’alimentation audio.

## <a name="draw-the-line"></a>Dessiner la ligne

La ligne est dessinée de gauche à droite à l’aide des fonctions GDI **MoveToEx** et **LineTo** .

Tout d’abord, vous déplacez le stylet vers le point de départ. Dans ce cas, x et y sont utilisés pour définir les valeurs de gauche à droite et de haut en bas que l’utilisateur verra sur l’écran. X est défini par le rectangle PRC et, plus précisément, par la valeur de PRC->gauche. Y est défini en tant que valeur des données de la forme d’onde à ce moment précis.

Ensuite, vous dessinez une ligne à l’autre extrémité de la fenêtre. Le point sur lequel vous dessinez la ligne est une valeur x, y. X est défini par le rectangle PRC, mais cette fois par PRC->droit. Y est toujours défini par les données de forme d’onde et est le même que le point à partir duquel vous avez commencé, car vous dessinez une ligne droite de gauche à droite.

## <a name="clean-up-everything"></a>Tout nettoyer

Vous devez supprimer les objets que vous créez. En particulier, vous devez supprimer tous les pinceaux et les stylets que vous créez. Il est conseillé de supprimer des stylets et des pinceaux lorsque vous avez fini de les utiliser.

Si vous ne les supprimez pas avant de terminer l’implémentation de la fonction **Render** , votre visualisation se bloquera dans une minute ou moins. Vous devez tenir compte de vos stylets et de vos pinceaux et détruire chacun d’eux. Veillez à ne pas créer de stylets à l’intérieur d’une boucle de code.

Utilisez la technique de codage donnée dans l’exemple pour détruire vos stylets et pinceaux.

-   **Important** Détruisez vos stylets et vos brosses !

une fois le nettoyage terminé, veillez à retourner S \_ OK afin que Lecteur Windows Media sache que vous avez terminé le dessin. Une fois que vous avez terminé, votre dessin sera transféré dans la fenêtre, un autre instantané sera pris, le **rendu** demandera à votre code de dessiner, et ainsi de suite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation du rendu**](implementing-render.md)
</dt> </dl>

 

 




