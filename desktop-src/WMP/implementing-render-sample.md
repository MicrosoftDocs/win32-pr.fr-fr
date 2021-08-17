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
ms.openlocfilehash: 8c00b57f15655468e5bd0000ccc3b5120e19c2af58d5a1ad6b5493b535c7253f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135572"
---
# <a name="implementing-render-sample"></a>Implémentation de Render, exemple

Le code suivant est utilisé pour implémenter la fonction **Render** :


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



Voici une explication du code :

Une variable nommée *MyColor* est utilisée pour la couleur de l’éclat et est déclarée avec **COLORREF**. Toutes les couleurs doivent utiliser le type de données **COLORREF** .

Une variable nommée *myLevel* est utilisée pour l’instantané de niveau audio Wave. Cette valeur dépend du niveau de puissance réel au moment de l’instantané.

l’instruction **switch** est définie par la présélection que l’utilisateur a choisie sur Lecteur Windows Media. Le choix permet de définir *MyColor* sur la couleur souhaitée (rouge, vert ou bleu). Toutefois, la couleur exacte sera déterminée par le niveau de puissance audio. Par exemple, si la présélection rouge est choisie, la couleur est un rouge fixe, mais il sera plus clair ou plus sombre en fonction de la forme d’onde audio au moment de l’instantané. Veillez à utiliser la macro **RBG** pour créer votre couleur.

un pinceau est créé appelé *hNewBrush* et il est utilisé pour remplir le rectangle *prc* fourni par Lecteur Windows Media. la surface de dessin est le contexte de périphérique *hdc* fourni par Lecteur Windows Media.

Le pinceau est supprimé par **SupprimerObjet**. Veillez à toujours supprimer les stylets ou les pinceaux que vous créez.

une fois le code de **rendu** terminé, Lecteur Windows Media affiche les graphiques *hdc* dans une fenêtre déterminée par l’apparence utilisée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**L’exemple lueur**](the-glow-sample.md)
</dt> </dl>

 

 




