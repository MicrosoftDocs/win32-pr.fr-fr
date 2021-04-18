---
title: Événements externes
description: Événements externes
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Apparences du lecteur Windows Media, événements externes
- apparences, événements externes
- événements, externes
- écriture de code pour les apparences, événements externes
- événements externes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512275"
---
# <a name="external-events"></a>Événements externes

Lorsque les utilisateurs cliquent sur un bouton ou appuient sur une touche, vous pouvez répondre à leur entrée à l’aide de gestionnaires d’événements. Un gestionnaire d’événements est une section de code qui s’exécute chaque fois que l’événement est déclenché.

Les événements suivants sont pris en charge par les éléments d’apparence :

-   **load**
-   **close**
-   **redimensionner**
-   **minute**
-   **Cliquez sur**
-   **dblclick**
-   **error**
-   **mousedown**
-   **mouseup**
-   **mousemove**
-   **mouseover**
-   **mouseout**
-   **keypress**
-   **keydown**
-   **keyup**

Pour plus d’informations sur les événements spécifiques, consultez la référence sur la programmation de l' [apparence](skin-programming-reference.md) .

Un gestionnaire d’événements externes type nomme l’événement et définit le code qui s’exécute. Par exemple, si vous souhaitez créer du code pour démarrer le lecteur Windows Media quand l’utilisateur clique sur un bouton, vous devez placer la ligne suivante dans votre code de bouton.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



Cela permet de lire le fichier nommé Laure. WMA. Notez que vous ajoutez le mot « on » à des événements spécifiques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des événements**](handling-events.md)
</dt> </dl>

 

 




