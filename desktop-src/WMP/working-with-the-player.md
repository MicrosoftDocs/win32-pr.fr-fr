---
title: Utilisation du lecteur
description: Utilisation du lecteur
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Lecteur Windows Media skins, attribut Player dans JScript
- Skins, attribut Player dans JScript
- attributs, joueur
- attribut Player
- fichiers JScript pour les apparences, attribut player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411622"
---
# <a name="working-with-the-player"></a>Utilisation du lecteur

lorsque vous utilisez Microsoft JScript pour accéder aux méthodes et aux propriétés d’Lecteur Windows Media, vous devez utiliser le nom "Player" pour le nom du contrôle. Par exemple, pour faire référence à la méthode Stop, vous devez taper :


```C++
player.Controls.Stop()

```



l’attribut global **player** est la clé permettant d’accéder au contrôle Lecteur Windows Media par le biais de scripts d’apparence. par le biais de cet attribut, tous les objets du contrôle Lecteur Windows Media deviennent accessibles pour la modification au moment de l’exécution via leurs propriétés et méthodes. En outre, l’élément **Player** est disponible pour vous permettre de spécifier des gestionnaires d’événements et l’attribut **URL** au moment de la conception.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation de JScript**](using-jscript.md)
</dt> </dl>

 

 




