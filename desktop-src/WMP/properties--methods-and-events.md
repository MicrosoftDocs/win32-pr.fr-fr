---
title: Propriétés, méthodes et événements
description: Propriétés, méthodes et événements
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Windows Media Player, propriétés du modèle d’objet
- Windows Media Player, méthodes pour le modèle objet
- Windows Media Player, événements pour le modèle objet
- Modèle objet du lecteur Windows Media, propriétés
- Modèle objet du lecteur Windows Media, méthodes
- Modèle objet du lecteur Windows Media, événements
- modèle objet, propriétés
- modèle objet, méthodes
- modèle objet, événements
- Contrôle ActiveX du lecteur Windows Media, propriétés du modèle d’objet
- Contrôle ActiveX, propriétés du modèle objet
- Contrôle ActiveX Windows Media Player Mobile, propriétés du modèle d’objet
- Windows Media Player Mobile, propriétés du modèle d’objet
- Contrôle ActiveX du lecteur Windows Media, méthodes pour le modèle objet
- Contrôle ActiveX, méthodes pour le modèle objet
- Windows Media Player Mobile ActiveX, méthodes pour le modèle objet
- Windows Media Player Mobile, méthodes pour le modèle objet
- Contrôle ActiveX du lecteur Windows Media, événements pour le modèle objet
- Contrôle ActiveX, événements pour le modèle objet
- Contrôle ActiveX Windows Media Player Mobile, événements pour le modèle objet
- Windows Media Player Mobile, événements pour le modèle objet
- Propriétés, modèle objet du lecteur Windows Media
- méthodes, modèle objet du lecteur Windows Media
- événements, modèle objet du lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100729"
---
# <a name="properties-methods-and-events"></a>Propriétés, méthodes et événements

Chaque objet possède des méthodes et des propriétés qui vous permettent de programmer le contrôle du lecteur Windows Media. Une méthode est une action que l’objet peut effectuer. Une propriété est une valeur de données que vous pouvez lire ou modifier. Par exemple, la méthode **Play** démarre le contenu en cours de lecture, tandis **que la propriété** Parate indique la fréquence d’images actuelle du contenu en cours de lecture.

En outre, l’objet **Player** déclenche des événements qui vous donnent la possibilité d’effectuer des actions à des moments spécifiques. Vous écrivez du code dans un gestionnaire d’événements qui s’exécutera lorsque le lecteur Windows Media déclenchera l’événement correspondant. Par exemple, vous pouvez écrire du code dans un gestionnaire d’événements **PlayStateChange** qui détermine si la modification de l’État est que le support a pris fin et, dans ce cas, affiche une boîte de dialogue demandant aux utilisateurs s’ils souhaitent relire le support.

> [!Note]  
> Toutes les méthodes du modèle objet du lecteur Windows Media sont asynchrones. Si vous appelez deux méthodes dans la même procédure, la deuxième méthode ne peut pas reposer sur la première méthode ayant terminé son action.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




