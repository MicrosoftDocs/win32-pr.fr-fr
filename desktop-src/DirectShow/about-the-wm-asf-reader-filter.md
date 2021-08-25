---
description: À propos du filtre du Lecteur WM ASF
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: À propos du filtre du Lecteur WM ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b71d0b25070c446ebff88f18785df7b55ba7bbcc7b1bcaa1dcf21995185252ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873699"
---
# <a name="about-the-wm-asf-reader-filter"></a>À propos du filtre du Lecteur WM ASF

La lecture des fichiers ASF est gérée par le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) . Lorsque le lecteur ASF WM lit un fichier, il crée automatiquement une broche de sortie pour chaque flux, y compris les flux Web, les flux de commandes de script et tout autre type de flux arbitraire. Dans le cas de plusieurs fichiers à vitesse de transmission, les codes confidentiels sont créés uniquement pour les flux actuellement sélectionnés. Pour lire un fichier ASF avec le filtre de lecteur ASF WM, appelez [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

le lecteur ASF WM prend en charge l’interface DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , qui permet aux applications d’effectuer une recherche temporelle dans le fichier. Toutefois, la lecture à des vitesses autres que 1,0 (comme spécifié dans [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)sesente) n’est pas prise en charge.

le filtre de lecteur ASF WM expose également plusieurs interfaces Windows Media Format SDK, comme décrit dans le tableau suivant. ces interfaces sont documentées dans la documentation du kit de développement logiciel (SDK) Windows Media Format.



| Interface                                             | Exposition                                 | Commentaires                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Via **IServiceProvider** sur le filtre. | Fourni pour les applications qui doivent lire du contenu protégé par des Rights Management numériques (DRM).                             |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** sur le filtre.           | Fourni pour permettre aux applications de lire les attributs de fichier et de contenu, ainsi que les informations de marqueur et de script et les métadonnées.     |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** sur le filtre.           | Partiellement implémenté sur le filtre afin que les applications puissent accéder aux méthodes d’information sur l’objet WM Reader.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** sur le filtre.           | Partiellement implémenté sur le filtre afin que les applications puissent accéder aux méthodes d’information sur l’objet de lecteur du kit de développement logiciel (SDK) de format. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture des fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



