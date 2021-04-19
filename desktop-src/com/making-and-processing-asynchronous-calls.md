---
title: Établissement et traitement des appels asynchrones
description: Les objets COM peuvent prendre en charge l’appel asynchrone.
ms.assetid: bf7f9f8e-66ce-41a4-854c-62dbe840a89e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059f55cc64a70f130e7fb654426803edbe8b7209
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509064"
---
# <a name="making-and-processing-asynchronous-calls"></a>Établissement et traitement des appels asynchrones

Les objets COM peuvent prendre en charge l’appel asynchrone. Lorsqu’un client effectue un appel asynchrone, le contrôle retourne immédiatement au client. Pendant que le serveur traite l’appel, le client est libre d’effectuer d’autres tâches. Lorsque le client ne peut plus continuer sans les résultats de l’appel, il peut obtenir les résultats de l’appel à ce moment-là.

Par exemple, une demande pour un jeu d’enregistrements volumineux ou complexe peut prendre du temps. Un client peut demander le Recordset par un appel asynchrone, puis effectuer un autre travail. Lorsque l’ensemble d’enregistrements est disponible, le client peut l’obtenir rapidement sans blocage.

Les clients n’effectuent pas d’appels asynchrones directement sur l’objet serveur. Au lieu de cela, ils obtiennent un objet d’appel qui implémente une version asynchrone d’une interface synchrone sur l’objet serveur. L’interface asynchrone de l’objet d’appel a un nom de la forme Async *NomInterface*. Par exemple, si un objet serveur implémente une interface synchrone nommée IMyInterface, il y aura un objet d’appel qui implémente une interface asynchrone nommée AsyncIMyInterface.

> [!Note]  
> La prise en charge asynchrone n’est pas disponible pour **IDispatch** ou pour les interfaces qui héritent de **IDispatch**.

 

Les objets serveur qui prennent en charge les appels asynchrones implémentent l’interface [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) . Cette interface expose une méthode unique, [**createCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), qui crée une instance d’un objet d’appel spécifié. Les clients peuvent interroger **ICallFactory** pour déterminer si un objet prend en charge l’appel asynchrone.

Pour chaque méthode sur une interface synchrone, l’interface asynchrone correspondante implémente deux méthodes. Ces méthodes attachent les préfixes Begin \_ et Finish \_ au nom de la méthode synchrone. Par exemple, si une interface nommée ISimpleStream a une méthode Read, l’interface AsyncISimpleStream aura une méthode de lecture Begin \_ Read et Finish \_ . Pour commencer un appel asynchrone, le client appelle la \_ méthode Begin.

Lorsque vous implémentez un objet serveur, il n’est pas nécessaire de fournir un objet d’appel pour chaque interface que l’objet implémente. Si l’objet serveur implémente l’interface [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) et utilise le marshaling standard, un client marshalé peut toujours obtenir un objet proxy d’appel, même s’il n’y a aucun objet d’appel côté serveur. Ce proxy marshale la \_ méthode Begin comme un appel synchrone, le serveur traite l’appel de façon synchrone et le client peut obtenir les paramètres out en appelant la méthode Finish \_ .

À l’inverse, si un client effectue un appel synchrone marshalé sur une interface pour laquelle il existe un objet d’appel côté serveur, le serveur traite toujours l’appel de manière asynchrone. Ce comportement ne sera pas visible pour le client, car le client recevra les mêmes paramètres de sortie et la même valeur de retour que celle qu’il aurait reçue de la méthode synchrone.

Dans les deux cas, l’interaction entre le client et le serveur est marshalée comme si l’appel était synchrone : la sortie des proxies synchrones et asynchrones ne peut pas être distinguée, comme c’est le cas de la sortie des stubs correspondants. Ce comportement simplifie grandement le modèle de programmation à la fois des clients et des serveurs. Si un objet serveur implémente [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory), un client marshalé n’a pas à tenter de créer un objet d’appel qui n’est peut-être pas disponible : pour le client, un objet d’appel est toujours disponible.

Lorsque le client et le serveur se trouvent dans le même cloisonnement, l’objet serveur traite l’appel que le client effectue. Si un objet d’appel n’est pas disponible, le client doit obtenir explicitement l’interface synchrone et effectuer un appel synchrone.

Pour plus d'informations, voir les rubriques suivantes :

-   [Exécution d’un appel asynchrone](making-an-asynchronous-call.md)
-   [Annulation d’un appel asynchrone](canceling-an-asynchronous-call.md)
-   [Annulation des appels de méthode](canceling-method-calls.md)
-   [Synchronisation des appels](call-synchronization.md)

 

 