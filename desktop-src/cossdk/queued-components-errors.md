---
description: Erreurs de composants en file d’attente
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Erreurs de composants en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514122"
---
# <a name="queued-components-errors"></a>Erreurs de composants en file d’attente

Lorsqu’un appel à un composant en file d’attente échoue, soit parce qu’il n’a pas pu être transmis au serveur (échec côté client), soit parce qu’il n’a pas pu s’exécuter lorsqu’il est arrivé (échec côté serveur), le message d' [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) correspondant est appelé *message incohérent*.

Le service COM+ Queued Components gère les messages incohérents à l’aide d’une série de files d’attente de nouvelles tentatives. Après plusieurs tentatives, le message est déplacé vers une file d’attente Rest finale. Les messages restent dans la file d’attente Rest jusqu’à ce qu’ils soient déplacés manuellement à l’aide de l’utilitaire de déplacement de messages des composants en file d’attente. Pour plus d’informations sur l’utilisation du Data Mover, consultez [gestion des erreurs](handling-errors-in-queued-components.md).

Vous trouverez des descriptions détaillées de la séquence d’événements qui se produit pour différents types d’erreurs dans les rubriques décrites dans le tableau suivant.



| Rubrique                                                                             | Description                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Erreurs côté serveur](server-side-errors.md)<br/>                           | Décrit en détail la réponse du service COM+ Queued Components à une défaillance côté serveur.<br/>             |
| [Erreurs côté client](client-side-errors.md)<br/>                           | Décrit en détail la réponse du service COM+ Queued Components à une défaillance côté client.<br/>             |
| [Échecs de Client-Side persistant](persistent-client-side-failures.md)<br/> | Décrit dans les détails la réponse du service des composants en file d’attente COM+ aux défaillances répétées côté client.<br/> |



 

 

 




