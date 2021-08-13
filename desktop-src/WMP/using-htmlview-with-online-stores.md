---
title: Utilisation de HTMLView avec des magasins en ligne
description: Utilisation de HTMLView avec des magasins en ligne
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Lecteur Windows Media des magasins en ligne, HTMLView
- magasins en ligne, HTMLView
- tapez 1 magasins en ligne, HTMLView
- tapez 2 magasins en ligne, HTMLView
- HTMLView, magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d5e89e2d0eaff2d51f8fa03281bf1ce85878b1863df619c28cdd228beb1eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465889"
---
# <a name="using-htmlview-with-online-stores"></a>Utilisation de HTMLView avec des magasins en ligne

Lecteur Windows Media demande à l’utilisateur l’autorisation d’afficher le contenu HTMLView en **cours de diffusion**. Les magasins en ligne peuvent désactiver cette invite en spécifiant une valeur d’URL de base dans l’élément **HTMLView** du document serviceInfo. lorsque Lecteur Windows Media ouvre une sélection qui spécifie le contenu de HTMLView à afficher, le lecteur compare l’url de base du document ServiceInfo du magasin en ligne actif à l’url de base du contenu HTMLView. s’ils correspondent, Lecteur Windows Media affiche le contenu HTMLView sans demander confirmation à l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**affichage des Pages Web dans les Lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Élément HTMLView**](htmlview-element.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




