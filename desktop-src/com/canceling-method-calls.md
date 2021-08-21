---
title: Annulation des appels de méthode
description: Avec l’introduction d’applications distribuées et basées sur le Web, certains appels de méthode peuvent prendre beaucoup de temps à retourner.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ea089f257527dfd31d7120170c8749a2d1b4d60ba006843c7ff5d43403b352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311083"
---
# <a name="canceling-method-calls"></a>Annulation des appels de méthode

Avec l’introduction d’applications distribuées et basées sur le Web, certains appels de méthode peuvent prendre beaucoup de temps à retourner. La latence de la connexion réseau peut être élevée, l’ordinateur serveur peut servir de nombreux clients ou le composant serveur peut transmettre une grande quantité de données, par exemple un fichier multimédia. Les utilisateurs doivent être en mesure d’annuler une demande qui prend trop de temps et l’application doit être en mesure de gérer les demandes d’annulation et de poursuivre son autre travail. Dans COM, vous pouvez utiliser l’interface [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) pour annuler un appel en attente qui provient d’un cloisonnement à thread unique.

Lorsqu’un appel est marshalé, le proxy crée un objet Cancel, qui implémente l’interface [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) . L’objet Cancel est associé à l’appel et au thread sur lequel l’appel est en attente.

Pour annuler l’appel en attente, le client passe une demande d’annulation via l’objet Cancel, qui gère les détails de la notification à l’objet serveur que l’appel a été annulé. Si la méthode appelée n’a pas été retournée, l’objet serveur, lors de la détection de la demande d’annulation, nettoie toutes les ressources de programme qu’il a allouées et notifie son client, en retournant une valeur **HRESULT** appropriée, qu’il a annulé l’exécution de l’appel. Si la méthode appelée a déjà été retournée, l’objet Cancel avertit le client. Dans les deux cas, le thread client est débloqué et peut continuer le traitement.

La manière dont l’objet serveur répond à une demande d’annulation est à la discrétion de l’implémenteur de serveur, mais le thread appelant sur le client est toujours débloqué et ignore les résultats que le serveur tente de lui passer. Les objets Cancel permettent de demander l’annulation d’une méthode en cours d’exécution, mais il n’existe aucune garantie que l’objet serveur arrête le traitement de l’appel. Par exemple, l’appel peut avoir déjà été retourné, ou l’objet serveur peut ne pas prendre en charge les objets Cancel.

COM fournit automatiquement une implémentation standard d’objets CANCEL pour les objets client et les interfaces qui utilisent le marshaling standard. Pour les objets et les interfaces qui utilisent le marshaling personnalisé, vous devez implémenter votre propre objet d’annulation.

À ce stade, les objets Cancel gèrent uniquement les appels synchrones.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Annulation d’un appel asynchrone](canceling-an-asynchronous-call.md)
</dt> <dt>

[**CoGetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[**CoSetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[**CoTestCancel**](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 