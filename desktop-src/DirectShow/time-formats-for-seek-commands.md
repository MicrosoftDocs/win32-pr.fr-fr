---
description: Formats d’heure pour les commandes de recherche
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formats d’heure pour les commandes de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857463"
---
# <a name="time-formats-for-seek-commands"></a>Formats d’heure pour les commandes de recherche

La plupart des méthodes de l’interface **IMediaSeeking** ont des paramètres qui expriment les valeurs de position, telles que la position actuelle ou la position d’arrêt. Par défaut, ces paramètres sont exprimés en unités de nanosecondes de 100, également appelées « temps de référence ». Tout filtre pouvant être cherché doit prendre en charge la recherche par temps de référence. Certains filtres peuvent également rechercher à l’aide d’autres unités de temps, telles que la recherche d’un numéro de séquence particulier, ou la recherche d’un décalage d’octet donné dans un flux. Chacune de ces unités de temps est appelée un format d’heure et est définie par un identificateur global unique (GUID). pour obtenir la liste des formats d’heure définis par DirectShow, consultez [**guid Format guid**](time-format-guids.md). Les tiers peuvent également définir des GUID pour des formats d’heure personnalisés.

Pour déterminer si les filtres actuellement dans le graphique de filtre prennent en charge un format d’heure particulier, appelez la méthode [**IMediaSeeking :: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) . La méthode retourne S \_ OK si le format est pris en charge. Sinon, elle retourne S \_ false ou un code d’erreur. Si un format est pris en charge, vous pouvez basculer vers ce format en appelant la méthode [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) . Si la méthode **SetTimeFormat** est réussie, les commandes Seek suivantes sont exprimées à l’aide du nouveau format d’heure.

L’exemple suivant vérifie si le graphique prend en charge la recherche par numéro de frame. Si c’est le cas, il cherche à tramer le numéro 20 :


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



Notez que les formats d’heure s’appliquent uniquement aux commandes Seek. Ils n’affectent pas la lecture des graphiques ou d’autres actions.

 

 



