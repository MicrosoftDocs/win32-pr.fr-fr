---
description: À propos du rendu vidéo dans DirectShow
ms.assetid: 3b064758-2ae5-4441-801c-5400e4ef3790
title: À propos du rendu vidéo dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699e8ecf133f362e699e6b9d650d11da5bf43347
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846746"
---
# <a name="about-video-rendering-in-directshow"></a>À propos du rendu vidéo dans DirectShow

DirectShow fournit plusieurs filtres qui restituent la vidéo :

-   Filtre de [convertisseur vidéo](video-renderer-filter.md) . Ce filtre est disponible pour toutes les plateformes qui prennent en charge DirectX et n’a aucune configuration système requise particulière. Le convertisseur vidéo utilise DirectDraw chaque fois que cela est possible pour afficher la vidéo ; dans le cas contraire, il utilise GDI. Ce filtre est le convertisseur vidéo par défaut sur les plateformes antérieures à Windows XP.
-   [Filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 est disponible sur Windows XP, où il s’agit du convertisseur vidéo par défaut. VMR-7 utilise toujours DirectDraw 7 pour le rendu. Il fournit de nombreuses fonctionnalités puissantes qui ne sont pas disponibles dans l’ancien filtre de convertisseur vidéo, y compris un modèle de plug-in dans lequel l’application contrôle les surfaces DirectDraw utilisées pour le rendu.
-   [Filtre de convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9). VMR-9 est une version plus récente du convertisseur de mixage vidéo qui utilise Direct3D 9 pour le rendu. Elle est disponible pour toutes les plateformes qui prennent en charge DirectX. Toutefois, ce n’est pas le convertisseur par défaut, car il a une configuration système plus élevée que le filtre de convertisseur vidéo.
-   Le filtre de [mixage de superposition](overlay-mixer-filter.md) est conçu spécifiquement pour la vidéo de lecture et de diffusion de DVD. Il prend également en charge les extensions de port vidéo (VPEs), ce qui lui permet de fonctionner avec des décodeurs matériels MPEG-2 ou des tuners TV analogiques qui envoient des vidéos directement à la carte graphique.
-   Le filtre EVR ( [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) ) est disponible à partir de Windows Vista. Il offre des performances vidéo améliorées par rapport aux convertisseurs vidéo antérieurs, en particulier lorsque la composition du bureau Windows Vista est activée.

En règle générale, le EVR est préféré pour les applications qui ciblent Windows Vista ou version ultérieure, et VMR-9 est préféré pour les applications qui s’exécutent sur des versions antérieures de Windows. Pour plus d’informations sur l’utilisation des filtres VMR-7 et VMR-9, consultez [utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md).

Mode fenêtre et mode sans fenêtre

Un convertisseur vidéo DirectShow peut fonctionner en mode *fenêtre* ou *sans fenêtre* .

-   En mode fenêtre, le convertisseur crée sa propre fenêtre pour afficher la vidéo. En règle générale, cette fenêtre est l’enfant d’une fenêtre d’application. Pour plus d’informations, consultez [utilisation du mode fenêtre](using-windowed-mode.md).
-   En mode sans fenêtre, le convertisseur dessine la vidéo directement dans une fenêtre d’application. Elle ne crée pas sa propre fenêtre. Pour plus d’informations sur ce mode, consultez [utilisation du mode sans fenêtre](using-windowless-mode.md).

Le filtre de convertisseur vidéo prend en charge uniquement le mode fenêtre. Les filtres VMR-7 et VMR-9 prennent en charge les deux modes. Ils sont par défaut en mode fenêtre pour des raisons de compatibilité descendante, mais le mode sans fenêtre est préféré. EVR prend en charge le mode sans fenêtre uniquement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu vidéo](video-rendering.md)
</dt> </dl>

 

 



