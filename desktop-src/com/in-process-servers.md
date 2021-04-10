---
title: Serveurs In-Process
description: Serveurs In-Process
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196734"
---
# <a name="in-process-servers"></a>Serveurs In-Process

Si vous implémentez une application serveur OLE en tant que serveur in-process, une DLL s’exécutant dans l’espace de processus de l’application conteneur, plutôt qu’en tant que serveur local, un EXE qui s’exécute dans son propre espace de processus, la communication entre le conteneur et le serveur est simplifiée, car la communication entre les deux peut prendre la forme d’appels de fonction normaux. Les appels de procédure distante ne sont pas nécessaires, car les deux applications s’exécutent dans le même espace de processus. Comme vous pouvez vous y attendre, les objets qui gèrent le marshaling des paramètres sont également inutiles, bien qu’ils puissent être agrégés dans la DLL sans interférer avec la communication entre le conteneur et le serveur.

Lorsqu’une application serveur OLE est implémentée en tant que serveur in-process, un gestionnaire d’objets distinct n’est pas nécessaire, car le serveur lui-même réside dans l’espace de processus du client. La principale différence entre un serveur in-process et un gestionnaire d’objets est que le serveur est en mesure de gérer l’objet dans un État en cours d’exécution alors que le gestionnaire ne le peut pas. L’une des conséquences de cette différence est qu’un serveur doit fournir une interface utilisateur pour manipuler l’objet en cours d’exécution, tandis qu’un gestionnaire délègue cette exigence au serveur de l’objet. Lors de la création d’un serveur in-process, vous pouvez effectuer un agrégat sur le gestionnaire OLE par défaut, ce qui lui permet de gérer les tâches de base, telles que l’affichage, le stockage et les notifications, lorsque vous implémentez uniquement les services que le gestionnaire ne fournit pas ou n’implémente pas de la façon dont vous avez besoin.

Pour plus d'informations, voir les rubriques suivantes :

-   [Avantages](advantages.md)
-   [Inconvénients](disadvantages.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Documents composés](compound-documents.md)
</dt> </dl>

 

 




