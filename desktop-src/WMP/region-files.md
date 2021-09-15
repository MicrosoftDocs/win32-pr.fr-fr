---
title: Fichiers de région
description: Fichiers de région
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Lecteur Windows Media Skins mobiles, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, les fichiers de région
- Lecteur Windows Media Skins mobiles, fichiers de région
- apparences, fichiers de région
- Fichiers de région dans les apparences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518360"
---
# <a name="region-files"></a>Fichiers de région

Les fichiers de région sont requis si vous utilisez n’importe quel type de bouton d’accès (2PushHit, PushHit ou ToggleHit).

Les fichiers de région sont utilisés pour définir des zones qui répondent à un TAP, également appelé « hit », sur un bouton spécifique. Pour chaque bouton d’accès, une zone de la bitmap de région reçoit une couleur Web spécifique (telle que \# FF0000, qui est la valeur du rouge plein). Le numéro de couleur est spécifié dans la définition du bouton de la région. Lorsque l’utilisateur affiche l’apparence, l’image du bouton est superposée sur l’arrière-plan à l’aide des coordonnées de la zone dans la bitmap de la région.

Par exemple, vous pouvez dessiner un cercle rouge à l’emplacement correspondant à l’emplacement du bouton suivant et le colorer en rouge ( \# FF0000). Ensuite, dans la définition du bouton, vous pouvez affecter une valeur RVB d’accès de 255, 0, 0 (qui est l’équivalent RVB de \# FF0000). Dans ce cas, le bouton suivant répond uniquement aux pressions (correspondances) à l’intérieur du cercle rouge.

Les boutons d’accès sont utilisés lorsque vous souhaitez définir des formes autres que des rectangles. Vous devez toujours définir les coordonnées de chaque bouton afin que les images secondaires, telles que Push et Disabled, puissent être localisées correctement. Dans la pratique, chaque bouton est délimité par un rectangle, et ces rectangles de limites imaginaires ne doivent pas se chevaucher.

> [!Note]  
> les fichiers d’art de région ne sont pas nécessaires dans Lecteur Windows Media 10 habillages mobiles, car les types de boutons ne sont pas pris en charge dans Lecteur Windows Media 10 mobile ou version ultérieure.

 

L’image suivante est un fichier de région classique.

![fichier de région](images/cesdkreg.png)

Ce fichier définit les parties de l’apparence pour chaque bouton de type d’accès. Chaque couleur est identifiée par son numéro de couleur dans la section boutons du fichier de définition d’apparence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichiers art**](art-files-mobile.md)
</dt> </dl>

 

 




