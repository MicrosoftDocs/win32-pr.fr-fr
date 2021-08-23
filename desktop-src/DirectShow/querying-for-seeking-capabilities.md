---
description: Interrogation des fonctionnalités de recherche
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Interrogation des fonctionnalités de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1d4389d9e5fcf1466a039ae48bbffb2c26a41c29281101984f6a7a291789f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747449"
---
# <a name="querying-for-seeking-capabilities"></a>Interrogation des fonctionnalités de recherche

Microsoft® DirectShow® prend en charge la recherche par le biais de l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . le gestionnaire de Graph de filtre expose cette interface, mais la fonctionnalité de recherche est toujours implémentée par des filtres dans le graphique.

Certaines données ne peuvent pas être recherchées. Par exemple, vous ne pouvez pas Rechercher un flux vidéo en direct à partir d’une caméra. Toutefois, si un flux peut faire l’objet d’une recherche, il peut prendre en charge différents types de recherche. Ce sont, entre autres, les suivantes :

-   Recherche d’une position arbitraire dans le flux.
-   Récupération de la durée du flux.
-   Récupération de la position actuelle dans le flux.
-   Lit en sens inverse.

L’interface **IMediaSeeking** définit un jeu d’indicateurs, qui [**recherche des \_ \_ \_ fonctionnalités de recherche**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), qui décrivent les fonctionnalités de recherche possibles. Pour récupérer les fonctionnalités du flux, appelez la méthode [**IMediaSeeking :: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) . La méthode retourne une combinaison d’opérations de bits d’indicateurs. L’application peut les tester à l’aide de l’opérateur & **(and au niveau du** bit). Par exemple, le code suivant vérifie si le graphique peut effectuer une recherche sur une position arbitraire :


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



