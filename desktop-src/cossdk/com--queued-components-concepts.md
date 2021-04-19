---
description: Concepts des composants en file d’attente COM+
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Concepts des composants en file d’attente COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545769"
---
# <a name="com-queued-components-concepts"></a>Concepts des composants en file d’attente COM+

En fonction des services de [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) , le service de composants en file d’attente com+ offre un moyen simple d’appeler et d’exécuter des composants de manière asynchrone. Le traitement peut se produire sans tenir compte de la disponibilité ou de l’accessibilité de l’expéditeur ou du destinataire.

En termes COM, une *file d’attente* est une zone de stockage qui enregistre les messages en vue d’une récupération ultérieure. La mise en file d’attente fournit un mécanisme de communication sans connexion. Autrement dit, l’expéditeur et le destinataire ne sont pas connectés directement et communiquent uniquement par le biais de files d’attente. La mise en file d’attente permet de conserver les informations jusqu’à ce que le récepteur soit prêt à l’obtenir. L’expéditeur et le destinataire communiquent indirectement afin que chacun puisse fonctionner indépendamment, ce qui n’est pas affecté par l’autre.

Dans le passé, une connaissance approfondie du marshaling était nécessaire pour mettre en file d’attente, envoyer et recevoir des messages asynchrones. Désormais, à l’aide d’appels de méthode facilement compréhensibles et utilisés par les développeurs de composants, le service de composants en file d’attente COM+ marshale automatiquement les données sous la forme d’un message Message Queuing. Et étant donné que le service Queued Components offre une prise en charge intégrée des transactions, un état incohérent ne peut pas compromettre les données en cas de défaillance du serveur.

Les rubriques suivantes de cette section contiennent des informations générales sur la conception et l’écriture de composants en file d’attente.



| Rubrique                                                                           | Description                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Avantages du traitement en file d’attente](benefits-of-queued-processing.md)<br/>   | Décrit les avantages de la programmation avec des composants en file d’attente COM+.<br/>                                         |
| [Architecture des composants en file d’attente](queued-components-architecture.md)<br/> | Décrit l’architecture du service COM+ Queued Components.<br/>                                          |
| [Message Queuing transactionnel](transactional-message-queuing.md)<br/>   | Décrit comment les transactions sont gérées par le service de composants en file d’attente COM+.<br/>                              |
| [Sécurité des composants en file d’attente](queued-components-security.md)<br/>         | Décrit les options de stratégie pour l’authentification des messages du client et leurs implications.<br/>                 |
| [Développement de composants en file d’attente](developing-queued-components.md)<br/>     | Décrit les considérations relatives à la programmation lors de l’écriture de composants en file d’attente.<br/>                                     |
| [Erreurs de composants en file d’attente](queued-components-errors.md)<br/>             | Décrit les types d’erreurs les plus courants que vous pouvez rencontrer lors de l’utilisation du service de composants en file d’attente COM+.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches des composants COM+ en file d’attente](com--queued-components-tasks.md)
</dt> </dl>

 

 




