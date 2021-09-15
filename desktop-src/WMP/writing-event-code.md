---
title: Écriture du code d’événement
description: Écriture du code d’événement
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- apparences de Lecteur Windows Media, écriture de code
- apparences, écrire du code
- événements, écriture de code
- écriture de code pour les habillages, à propos de
- apparences de Lecteur Windows Media, événements
- apparences, événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411620"
---
# <a name="writing-event-code"></a>Écriture du code d’événement

Les événements sont traités de la même façon que les attributs. Vous devez attribuer une valeur à l’événement, et la valeur est le code que vous souhaitez exécuter lorsque l’événement se produit. Le mot « on » est ajouté au début du nom de l’événement ; par exemple, l’événement Click deviendra **OnClick**.

la valeur de l’événement est entre guillemets doubles et commence par le mot JScript suivi d’un signe deux-points. Le code que vous souhaitez exécuter est ensuite suivi d’un point-virgule et des guillemets doubles fermants. Par exemple, pour arrêter la diffusion quand l’utilisateur clique sur un bouton, tapez la commande suivante en tant qu’attribut dans votre code d’élément de **bouton** :


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



Si vous avez un code qui requiert des guillemets, utilisez des guillemets simples. Soyez prudent lorsque vous utilisez des guillemets pour qu’ils soient correctement équilibrés. Voici un exemple d’utilisation des deux types :


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



Vous pouvez également modifier les attributs de votre apparence lors du traitement d’un événement externe. Par exemple, pour fermer une vue nommée myView, vous pouvez taper :


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des événements**](handling-events.md)
</dt> </dl>

 

 




