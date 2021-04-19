---
description: Utilisation de la capture WDDM dans DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Utilisation de la capture WDDM dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528208"
---
# <a name="using-wddm-capture-in-directshow"></a>Utilisation de la capture WDDM dans DirectShow

Cette rubrique s’applique à Windows Vista et versions ultérieures.

Certaines cartes vidéo possèdent une fonctionnalité de capture vidéo intégrée. Sur ces cartes, les images capturées sont placées dans la mémoire vidéo (VRAM). Avant Windows Vista, il n’existait pas de mécanisme standard pour le traitement des frames pendant qu’ils étaient restés dans VRAM. Au lieu de cela, les données devaient être copiées dans la mémoire système, traitées, puis recopiées dans VRAM pour s’afficher. Dans Windows Vista, DirectShow prend désormais en charge un mécanisme de conservation des images vidéo dans la mémoire VRAM dans tout le pipeline de traitement, de la capture à l’affichage.

Le filtre KsProxy détermine si le pilote prend en charge la capture de la surface VRAM en interrogeant le pilote pour la \_ propriété de surface de capture par défaut KSPROPERTY \_ \_ . (Cette propriété est documentée dans la documentation du kit de pilotes Windows.) Si le pilote prend en charge la capture de la surface VRAM, KsProxy alloue un type spécial d’exemple de média qui contient un pointeur vers une surface Direct3D.

Ensuite, KsProxy détermine si le filtre en aval prend en charge l’accélération vidéo DirectX (DXVA) 2,0, comme suit :

1.  KsProxy interroge la broche d’entrée en aval pour l’interface **IMFGetService** .
2.  Si le code PIN expose **IMFGetService**, ksproxy appelle **IMFGetService :: GetService** pour l’interface **IDirect3DDeviceManager** . Le service identier est un \_ service d’accélération vidéo de m \_ \_ .

Ces deux interfaces sont documentées dans la documentation du kit de développement logiciel (SDK) Media Foundation.

Si le filtre en aval ne prend pas en charge DXVA 2,0, KsProxy alloue une mémoire tampon système supplémentaire. Elle utilise cette mémoire tampon pour copier les images vidéo de la mémoire VRAM vers la mémoire système. La méthode [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) de l’exemple de média retourne un pointeur vers cette mémoire tampon système.

Toutefois, si le filtre en aval ne prend pas en charge DXVA 2,0, KsProxy n’alloue pas de mémoire tampon système. Dans ce cas, la méthode **GetPointer** retourne E \_ NOTIMPL. Au lieu de cela, le filtre en aval est supposé accéder directement à la surface Direct3D de l’exemple. Il existe deux façons pour le filtre en aval d’obtenir un pointeur vers la surface, les deux équivalentes :

-   Interrogez l’exemple pour l’interface **IMFGetService** et appelez **GetService** pour l’interface **IDirect3DSurface9** . L’identificateur de service est un \_ service de mémoire tampon Mr \_ .
-   Interrogez l’exemple pour l’interface [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) et appelez [**IMediaSample2Config :: GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> </dl>

 

 



