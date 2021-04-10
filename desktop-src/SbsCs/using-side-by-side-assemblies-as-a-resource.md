---
description: Utilisation d’assemblys côte à côte en tant que ressource
ms.assetid: f7963d37-93c4-49d6-af7d-fc692f632894
title: Utilisation d’assemblys côte à côte en tant que ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b97265b48f4ce8f3c87a87ec4ca9ea2b8252819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951092"
---
# <a name="using-side-by-side-assemblies-as-a-resource"></a>Utilisation d’assemblys côte à côte en tant que ressource

Vous pouvez ajouter un manifeste à une application en tant que ressource dans le fichier d’en-tête binaire de l’application. La valeur de l’ID de ressource de manifeste \_ \_ détermine la façon dont les dépendances d’assembly côte à côte décrites dans le manifeste sont utilisées par le chargeur.

Si vous affectez \_ à l' \_ ID de ressource de manifeste la valeur 1, le chargeur utilise les dépendances d’assembly côte à côte spécifiées dans le manifeste en tant que processus par défaut. Tous les plug-ins utilisent également ce processus par défaut.

Le tableau suivant résume la façon dont le chargeur utilise le manifeste pour les différentes valeurs de \_ l’ID de ressource de manifeste \_ lorsque l’application est compilée avec l’indicateur compatible-DISOLATION \_ \_ . Notez que les valeurs 1-16 sont réservées à une utilisation par Windows XP. Un développeur peut utiliser d’autres valeurs s’il souhaite gérer les contextes d’activation à l’aide des fonctions décrites dans la [référence de contexte d’activation](activation-context-reference.md).



| Valeur de l' \_ ID de ressource de manifeste \_ | Le manifeste spécifie la valeur par défaut du processus ? | Utiliser pour les importations statiques ? | Utiliser pour un EXE ? | Utiliser pour une DLL ? | Utilise la version côte à côte des assemblys si la prise en charge de-DISOLATION est \_ \_ activée ? |
|---------------------------------|-----------------------------------------|-------------------------|-----------------|----------------|---------------------------------------------------------------------------------------|
| 1                               | Oui                                     | Oui                     | Oui             | Non             | Oui                                                                                   |
| 2                               | Non                                      | Oui                     | Oui             | Oui            | Oui                                                                                   |
| 3                               | Non                                      | Non                      | Oui             | Oui            | Oui                                                                                   |



 

L' \_ \_ ID de ressource de manifeste 1 doit être utilisé pour les applications qui n’hébergent pas de plug-ins. Utilisez \_ \_ l’ID de ressource de manifeste 1 lorsque toutes les parties de l’application doivent utiliser la version de l’assembly côte à côte spécifié dans le manifeste. Pour plus d’informations, consultez [activation d’un assembly dans une application sans extensions](enabling-an-assembly-in-an-application-without-extensions.md).

L' \_ \_ ID de ressource de manifeste 2 doit être utilisé pour les applications qui hébergent des contrôles ou des plug-ins tiers. Dans ce cas, le manifeste affecte tous les assemblys côte à côte chargés par le chargement statique, les appels à DllMain et les appels redirigés par-DISOLATION prenant en charge \_ \_ . Pour plus d’informations, consultez [activation d’un assembly dans une application hébergeant une dll, une extension ou le panneau de configuration](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

\_ \_ L’ID de ressource de manifeste 3 doit être utilisé pour la redirection des appels \_ prenant en charge DISOLATION \_ uniquement. Le chargement par d’autres méthodes n’est pas affecté.

 

 



