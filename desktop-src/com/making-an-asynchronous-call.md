---
title: Exécution d’un appel asynchrone
description: 'La procédure de création d’un appel synchrone est simple : le client obtient un pointeur d’interface sur l’objet serveur et appelle des méthodes via ce pointeur. L’appel asynchrone implique un objet d’appel, donc il implique quelques étapes supplémentaires.'
ms.assetid: ab65d38d-836a-48d4-87c1-8812cbc8ff92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a153b826e570920fca2a92f5b53ed2079c561cbcda899b793cef1f39473bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755989"
---
# <a name="making-an-asynchronous-call"></a>Exécution d’un appel asynchrone

La procédure de création d’un appel synchrone est simple : le client obtient un pointeur d’interface sur l’objet serveur et appelle des méthodes via ce pointeur. L’appel asynchrone implique un objet d’appel, donc il implique quelques étapes supplémentaires.

Pour chaque méthode sur une interface synchrone, l’interface asynchrone correspondante implémente deux méthodes. Ces méthodes attachent les préfixes Begin \_ et Finish \_ au nom de la méthode synchrone. Par exemple, si une interface nommée ISimpleStream a une méthode Read, l’interface AsyncISimpleStream aura une méthode de lecture Begin \_ Read et Finish \_ . Pour commencer un appel asynchrone, le client appelle la \_ méthode Begin.

**Pour commencer un appel asynchrone**

1.  Interrogez l’objet serveur pour l’interface [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) . Si [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) retourne E \_ nointerface, l’objet serveur ne prend pas en charge l’appel asynchrone.

2.  Appelez [**ICallFactory :: createCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) pour créer un objet d’appel correspondant à l’interface de votre choix, puis relâchez le pointeur vers [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory).

3.  Si vous n’avez pas demandé de pointeur vers l’interface asynchrone à partir de l’appel à [**createCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), interrogez l’objet d’appel pour l’interface asynchrone.

4.  Appelez la méthode Begin appropriée \_ .

L’objet serveur est en train de traiter l’appel asynchrone et le client est libre d’effectuer d’autres tâches jusqu’à ce qu’il ait besoin des résultats de l’appel.

Un objet d’appel ne peut traiter qu’un seul appel asynchrone à la fois. Si le même ou un deuxième client appelle une \_ méthode Begin avant la fin d’un appel asynchrone en attente, la \_ méthode Begin retourne l' \_ appel E RPC E \_ \_ en attente.

Si le client n’a pas besoin des résultats de la \_ méthode Begin, il peut libérer l’objet Call à la fin de cette procédure. COM détecte cette condition et nettoie l’appel. La \_ méthode Finish n’est pas appelée et le client n’obtient pas de paramètres de sortie ou de valeur de retour.

Lorsque l’objet serveur est prêt à retourner à partir de la \_ méthode Begin, il signale l’objet d’appel qu’il a effectué. Lorsque le client est prêt, il vérifie si l’objet d’appel a été signalé. Dans ce cas, le client peut terminer l’appel asynchrone.

Le mécanisme de cette signalisation et de la vérification entre le client et le serveur est l’interface [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) sur l’objet d’appel. L’objet d’appel implémente normalement cette interface en agrégeant un objet de synchronisation fourni par le système. L’objet de synchronisation encapsule un handle d’événement, que le serveur signale juste avant de retourner à partir de la \_ méthode Begin en appelant [**ISynchronize :: signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal).

**Pour effectuer un appel asynchrone**

1.  Interrogez l’objet d’appel pour l’interface [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) .

2.  Appelez [**ISynchronize :: wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait).

3.  Si [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) retourne \_ \_ un délai d’attente RPC E, la \_ méthode Begin n’a pas terminé le traitement. Le client peut continuer à exécuter d’autres tâches et appeler de nouveau **Wait** ultérieurement. Elle ne peut pas appeler la \_ méthode Finish tant que **Wait** n’a pas la valeur \_ OK.

    Si [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) retourne \_ la valeur OK, la \_ méthode Begin est retournée. Appelez la méthode Finish appropriée \_ .

La \_ méthode Finish transmet les paramètres out au client. Le comportement des méthodes asynchrones, y compris la valeur de retour de la \_ méthode Finish, doit correspondre exactement à celui de la méthode synchrone correspondante.

Le client peut libérer l’objet d’appel dès que la méthode Finish est \_ retournée, ou il peut contenir un pointeur vers l’objet d’appel pour effectuer des appels supplémentaires. Dans les deux cas, le client est responsable de la libération de l’objet d’appel lorsque l’objet n’est plus nécessaire.

Si vous appelez une \_ méthode Finish alors qu’aucun appel n’est en cours, la méthode retournera l’appel de RPC \_ E \_ \_ Complete.

> [!Note]  
> Si les objets client et serveur se trouvent dans le même cloisonnement, la réussite des appels à [**ICallFactory :: createCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) n’est pas garantie. Si l’objet serveur ne prend pas en charge l’appel asynchrone sur une interface particulière, la tentative de création d’un objet d’appel échoue et le client doit utiliser l’interface synchrone.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Annulation d’un appel asynchrone](canceling-an-asynchronous-call.md)
</dt> <dt>

[Sécurité du client pendant un appel asynchrone](client-security-during-an-asynchronous-call.md)
</dt> <dt>

[Emprunt d’identité et appels asynchrones](impersonation-and-asynchronous-calls.md)
</dt> </dl>

 

 