---
title: Utilisation du lecteur
description: Utilisation du lecteur
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Apparences du lecteur Windows Media, attribut Player en JScript
- Skins, attribut Player dans JScript
- attributs, joueur
- attribut Player
- Fichiers JScript pour les apparences, attribut Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380390"
---
# <a name="working-with-the-player"></a>Utilisation du lecteur

Lorsque vous utilisez Microsoft JScript pour accéder aux méthodes et aux propriétés du lecteur Windows Media, vous devez utiliser le nom « Player » pour le nom du contrôle. Par exemple, pour faire référence à la méthode Stop, vous devez taper :


```C++
player.Controls.Stop()

```



L’attribut global **Player** est la clé permettant d’accéder au contrôle du lecteur Windows Media par le biais de scripts d’apparence. Par le biais de cet attribut, tous les objets du contrôle du lecteur Windows Media deviennent accessibles pour la modification au moment de l’exécution par le biais de leurs propriétés et méthodes. En outre, l’élément **Player** est disponible pour vous permettre de spécifier des gestionnaires d’événements et l’attribut **URL** au moment de la conception.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation de JScript**](using-jscript.md)
</dt> </dl>

 

 




