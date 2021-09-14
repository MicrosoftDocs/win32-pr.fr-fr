---
title: Propriétés, méthodes et événements
description: Propriétés, méthodes et événements
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Lecteur Windows Media, propriétés du modèle objet
- Lecteur Windows Media, méthodes pour le modèle objet
- Lecteur Windows Media, événements pour le modèle objet
- Lecteur Windows Media modèle objet, propriétés
- Lecteur Windows Media modèle objet, méthodes
- Lecteur Windows Media modèle objet, événements
- modèle objet, propriétés
- modèle objet, méthodes
- modèle objet, événements
- Lecteur Windows Media ActiveX contrôle, propriétés du modèle objet
- contrôle ActiveX, propriétés du modèle objet
- Lecteur Windows Media contrôle Mobile ActiveX, propriétés du modèle objet
- Lecteur Windows Media Mobile, propriétés du modèle d’objet
- Lecteur Windows Media ActiveX contrôle, méthodes pour le modèle objet
- contrôle ActiveX, méthodes pour le modèle objet
- Lecteur Windows Media contrôle Mobile ActiveX, méthodes pour le modèle objet
- Lecteur Windows Media Mobile, méthodes pour le modèle objet
- Lecteur Windows Media ActiveX contrôle, événements pour le modèle objet
- contrôle ActiveX, événements pour le modèle objet
- Lecteur Windows Media contrôle Mobile ActiveX, événements pour le modèle objet
- Lecteur Windows Media Mobile, événements pour le modèle objet
- propriétés, Lecteur Windows Media modèle objet
- méthodes, Lecteur Windows Media modèle objet
- événements, Lecteur Windows Media modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013242"
---
# <a name="properties-methods-and-events"></a>Propriétés, méthodes et événements

chaque objet possède des méthodes et des propriétés qui vous permettent de programmer le contrôle Lecteur Windows Media. Une méthode est une action que l’objet peut effectuer. Une propriété est une valeur de données que vous pouvez lire ou modifier. Par exemple, la méthode **Play** démarre le contenu en cours de lecture, tandis **que la propriété** Parate indique la fréquence d’images actuelle du contenu en cours de lecture.

En outre, l’objet **Player** déclenche des événements qui vous donnent la possibilité d’effectuer des actions à des moments spécifiques. vous écrivez du code dans un gestionnaire d’événements qui s’exécute quand Lecteur Windows Media déclenche l’événement correspondant. Par exemple, vous pouvez écrire du code dans un gestionnaire d’événements **PlayStateChange** qui détermine si la modification de l’État est que le support a pris fin et, dans ce cas, affiche une boîte de dialogue demandant aux utilisateurs s’ils souhaitent relire le support.

> [!Note]  
> toutes les méthodes dans le modèle objet Lecteur Windows Media sont asynchrones. Si vous appelez deux méthodes dans la même procédure, la deuxième méthode ne peut pas reposer sur la première méthode ayant terminé son action.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




