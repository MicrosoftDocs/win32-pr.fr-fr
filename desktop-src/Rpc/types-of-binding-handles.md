---
title: Types de handles de liaison
description: Les handles de liaison peuvent être automatiques, implicites ou explicites.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a3db77f01bf0228623efe9d3dca5fbeb023d97fbe00e5da4d4ba070f323ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011071"
---
# <a name="types-of-binding-handles"></a>Types de handles de liaison

Les handles de liaison peuvent être automatiques, implicites ou explicites. Elles diffèrent dans la quantité de contrôle que l’application a sur le processus de liaison. Comme son nom l’indique, les poignées de liaison automatique automatisent la liaison. Les applications client et serveur n’ont pas besoin de code pour gérer le processus de liaison. Les handles de liaison implicite permettent aux programmes clients de configurer le handle de liaison avant que la liaison ait lieu. Une fois que le client a établi une liaison, la bibliothèque Runtime RPC gère le reste. Les handles de liaison explicites déplacent le contrôle total sur le processus de liaison dans le code source des programmes du client et du serveur. Avec ce contrôle, la complexité est accrue. Votre application doit appeler des fonctions RPC pour gérer la liaison. Elle ne se produit pas automatiquement. Les handles de liaison explicites sont recommandés.

Le diagramme suivant illustre les différences entre les handles de liaison automatiques, implicites et explicites.

![différences entre les handles de liaison automatiques, implicites et explicites](images/bhand.png)

En outre, chaque descripteur de liaison est de type primitif ou personnalisé. Chaque type de descripteur de liaison est abordé dans les rubriques suivantes :

-   [Handles de liaison automatiques](automatic-binding-handles.md)
-   [Handles de liaison implicites](implicit-binding-handles.md)
-   [Handles de liaison explicites](explicit-binding-handles.md)
-   [Handles de liaison primitifs et personnalisés](primitive-and-custom-binding-handles.md)

 

 




