---
description: Allocateur de surface VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Allocateur de surface VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c586c3ef135722ac259813d918dc4054617b8ae6bfb987083f0a2ceaa986067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071983"
---
# <a name="vbi-surface-allocator"></a>Allocateur de surface VBI

L’allocateur de surface VBI contrôle l’allocation de mémoires tampons VBI dans des graphiques de télévision analogiques avec des scénarios de capture de port vidéo matériel. Avec les appareils tels que le décodeur Bt829, la mémoire tampon de trame peut contenir plusieurs mémoires tampons de capture VBI accessibles via un mécanisme matériel propriétaire connu de manière générique comme un port vidéo. Le filtre allocateur de surface VBI se connecte en aval du filtre de capture et n’a aucune broche de sortie. le filtre fonctionne en étroite collaboration avec la [superposition Mixer](overlay-mixer-filter.md) (par le biais de DirectDraw) pour effectuer des opérations coordonnées sur le port vidéo matériel, en utilisant la même mémoire tampon de trame SVGA limitée.



| Étiquette | Valeur |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Types de média de broche d’entrée                    | \_Vidéo MediaType, MEDIASUBTYPE \_ VPVBI                                               |
| Interfaces pin d’entrée                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| Types de média de broche de sortie                   | MEDIATYPE \_ null, MEDIASUBTYPE \_ null. (Rien n’est jamais connecté à la broche de sortie.) |
| Interfaces de broche de sortie                    | Non applicable.                                                                     |
| CLSID du filtre                             | CLSID \_ VBISurfaces                                                                  |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                   |
| Exécutable                               | vbisurf.ax                                                                          |
| [Mérite](merit.md)                       | MÉRITE \_ normal                                                                       |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



