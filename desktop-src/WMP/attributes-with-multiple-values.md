---
title: attributs avec plusieurs valeurs (Lecteur Windows Media SDK)
description: en savoir plus sur les attributs avec plusieurs valeurs dans le kit de développement logiciel (SDK) Lecteur Windows Media. Certains attributs d’éléments multimédias peuvent avoir plusieurs valeurs.
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Lecteur Windows Media, attributs pour les éléments multimédias
- Lecteur Windows Media modèle objet, attributs pour les éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Lecteur Windows Media Mobile, attributs pour les éléments multimédias
- Lecteur Windows Media ActiveX contrôle, attributs pour les éléments multimédias
- Lecteur Windows Media contrôle de ActiveX Mobile, attributs pour les éléments multimédias
- contrôle ActiveX, attributs pour les éléments multimédias
- bibliothèque de Lecteur Windows Media, attributs des éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, valeurs multiples
- valeurs d’attribut multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b029589444525ae3e0ea699cb12c72bcf900b1107556151c01b7b93434a0c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098919"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a>attributs avec plusieurs valeurs (Lecteur Windows Media SDK)

Certains attributs d’éléments multimédias peuvent avoir plusieurs valeurs. par exemple, l' **auteur**, le **wm/Composer** et les attributs **wm/Genre** peuvent avoir plusieurs valeurs. Le type de données de tels attributs est **une chaîne à valeurs multiples**.

dans Lecteur Windows Media, la bibliothèque affiche plusieurs valeurs dans un champ unique, en séparant les valeurs par des points-virgules. toutefois, chaque valeur est en fait un attribut distinct de l’élément multimédia Windows.

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

 

 




