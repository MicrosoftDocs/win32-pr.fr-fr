---
description: Développement de composants en file d’attente
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Développement de composants en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519341"
---
# <a name="developing-queued-components"></a>Développement de composants en file d’attente

Le service COM+ Queued Components requiert que toutes les méthodes d’application contiennent uniquement \[ des \] paramètres in, sans aucune valeur de retour. Étant donné que l’objet serveur n’est pas nécessairement disponible lorsque le client effectue l’appel, les résultats du serveur peuvent être retournés en envoyant un message qui crée un autre objet. De cette façon, la communication bidirectionnelle ne se produit pas dans tous les cas, mais uniquement lorsqu’elle est requise, par une série de messages unidirectionnels entre objets.

Pour utiliser le service de composants en file d’attente COM+, le service de [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) doit déjà être installé. Message Queuing n’est pas installé automatiquement. Vous devez sélectionner les Message Queuing au cours de l’installation du système d’exploitation ou à l’aide d' **Ajout/suppression de programmes**. Un certificat de Message Queuing interne est créé automatiquement à l’ouverture de session.

Les rubriques décrites dans le tableau suivant fournissent des considérations supplémentaires pour les situations plus spécialisées.



| Rubrique                                                                                           | Description                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Passage d’objets en tant que paramètre](passing-objects-as-parameters.md)s<br/>                   | Décrit comment passer des objets en tant que \[ \] paramètres in à des composants en file d’attente.<br/>                    |
| [Limitations de sécurité en mode groupe de travail](security-limitations-in-workgroup-mode.md)<br/> | Décrit les limitations relatives à l’utilisation de l’authentification Message Queuing en mode groupe de travail.<br/>       |
| [Considérations relatives aux threads](threading-considerations.md)<br/>                             | Décrit les problèmes spécifiques liés au passage de pointeurs d’interface d’enregistreur entre les threads.<br/> |
| [Réception d’une réponse](receiving-a-response.md)<br/>                                     | Décrit comment construire une réponse à un appel de composant mis en file d’attente.<br/>                           |



 

 

 




