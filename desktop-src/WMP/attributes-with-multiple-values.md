---
title: Attributs avec plusieurs valeurs (kit de développement logiciel (SDK) Windows Media Player)
description: En savoir plus sur les attributs avec plusieurs valeurs dans le kit de développement logiciel (SDK) du lecteur Windows Media. Certains attributs d’éléments multimédias peuvent avoir plusieurs valeurs.
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Lecteur Windows Media, attributs des éléments multimédias
- Modèle objet du lecteur Windows Media, attributs des éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Windows Media Player Mobile, attributs pour les éléments multimédias
- Contrôle ActiveX du lecteur Windows Media, attributs des éléments multimédias
- Contrôle ActiveX Windows Media Player Mobile, attributs des éléments multimédias
- Contrôle ActiveX, attributs pour les éléments multimédias
- Bibliothèque du lecteur Windows Media, attributs pour les éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, valeurs multiples
- valeurs d’attribut multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16baf4bab47dc972ec7b043980dccb0f2aadd57
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262601"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a>Attributs avec plusieurs valeurs (kit de développement logiciel (SDK) Windows Media Player)

Certains attributs d’éléments multimédias peuvent avoir plusieurs valeurs. Par exemple, l' **auteur**, le **WM/compositeur** et les attributs **WM/genre** peuvent avoir plusieurs valeurs. Le type de données de tels attributs est **une chaîne à valeurs multiples**.

Dans le lecteur Windows Media, la bibliothèque affiche plusieurs valeurs dans un champ unique, en les séparant par des points-virgules. Toutefois, chaque valeur est en fait un attribut distinct de l’élément Windows Media.

Vous pouvez écrire du code qui détermine si un attribut donné a plusieurs valeurs, puis récupérer toutes ces valeurs. Vous devez utiliser le *média*. **getItemInfoByType**. Si vous utilisez le *média*. méthode **getItemInfo** pour récupérer un attribut à valeurs multiples, vous récupérez uniquement la première valeur.

Le dernier exemple de la rubrique [lecture des valeurs d’attribut](reading-attribute-values.md) illustre l’utilisation du *média*. **getAttributeCountByType** et *Media*. méthodes **getItemInfoByType** pour récupérer plusieurs valeurs pour un attribut donné.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs d’élément multimédia**](media-item-attributes.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Lecture des valeurs d’attribut à partir d’un CD ou d’un DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




