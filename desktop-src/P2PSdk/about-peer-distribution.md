---
description: L’API de distribution d’homologue, qui prend en charge la fonctionnalité Branch cache dans Windows 7, Windows Server 2008 R2, Windows 8 et Windows Server 2012, offre un ensemble d’API de plateforme qui peuvent augmenter la réactivité du réseau des applications centralisées quand elles sont accessibles à partir de bureaux distants et aident à réduire l’utilisation globale du réseau étendu sans interférer avec les technologies de sécurité
ms.assetid: feb9666e-563a-49f4-ad1c-f166a0faff31
title: À propos de la distribution d’homologue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5b9a99a65ea2cfda6dc8ad9accd4d881529e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865181"
---
# <a name="about-peer-distribution"></a>À propos de la distribution d’homologue

L’API de distribution d’homologue, qui prend en charge la fonctionnalité Branch cache dans Windows 7, Windows Server 2008 R2, Windows 8 et Windows Server 2012, offre un ensemble d’API de plateforme qui peuvent augmenter la réactivité du réseau des applications centralisées quand elles sont accessibles à partir de bureaux distants et aident à réduire l’utilisation globale du réseau étendu sans interférer avec les technologies de sécurité

Le système de distribution d’homologue offre un ensemble d’API de plateforme utilisées par les serveurs de publication qui fournissent du contenu numérique et des consommateurs qui le demandent. Pour distinguer facilement ces rôles, il peut être plus facile de considérer l’éditeur dans un rôle de serveur et le consommateur dans un rôle de client. Là encore, il est important de garder à l’esprit qu’en dehors de ces rôles conceptuels, le service de distribution pair à pair est un véritable système pair, comme indiqué par la capacité de n’importe quel nœud de distribution pair à publier et à consommer du contenu numérique. Les API de plateforme de distribution d’homologue sont exposées aux éditeurs et aux consommateurs par une bibliothèque d’importation Win32 (**PeerDist. lib**).

Le cycle de vie du contenu fourni par un serveur de publication et récupéré par un consommateur avec le service de distribution pair à pair se compose des opérations suivantes :



|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Publication de contenu** | La publication est effectuée pour obtenir une description des informations de contenu de termes de contenu ou des **informations** de **contenu** pour Short. Ces informations de contenu peuvent ensuite être utilisées par une instance du service de distribution d’homologue pour authentifier et reconstruire le contenu. Lorsque le contenu est publié par une application dans le service de distribution d’homologue, qui est conceptuellement une opération côté serveur, ce contenu est associé à l’identité de l’éditeur, qui est basé sur le SID de l’utilisateur associé au jeton d’accès au thread. Cette liaison est effectuée pour limiter l’accès au contenu par des entités non autorisées. Toutefois, il est important de noter que l’accès aux informations de contenu est équivalent à l’accès au contenu proprement dit, car les informations de contenu peuvent être utilisées pour obtenir le contenu à partir d’homologues ou d’un cache hébergé.<br/> Il existe une nouvelle version de la structure de données d’informations de contenu dans Windows 8 ; Toutefois, la version précédente est toujours prise en charge. Pour interagir avec les clients Windows 7, un administrateur peut configurer le service de distribution d’homologues pour utiliser la version précédente de la structure de données d’informations de contenu.<br/> |
| **Récupération du contenu**   | Pour qu’un consommateur récupère du contenu à partir du service de distribution d’homologue, l’accès doit être fourni aux informations de contenu publiées associées à ce contenu. Le service de distribution d’homologue utilisé pour publier le contenu peut fournir les informations de contenu associées. Une fois que le consommateur dispose des informations de contenu, d’autres API de distribution d’homologue peuvent être utilisées pour demander du contenu auprès du service de distribution d’homologue. Le service de distribution d’homologue va tenter de récupérer le contenu à partir du réseau local. Si le contenu n’est pas disponible, l’application cliente est chargée de récupérer le contenu à partir du serveur source.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Suppression de la publication** | Pour les applications qui ont publié du contenu dans le service de distribution d’homologue, la fonction [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish) a été fournie pour permettre l’annulation de la publication du contenu. Une fois que le contenu n’a pas été publié, le service de distribution d’homologue local ne fournit plus les informations de contenu associées à ce contenu.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="asynchronous-completions"></a>Saisie semi-automatique asynchrone

L’API de distribution d’homologue prend en charge un modèle d’API asynchrone et, en tant que résultat, les API de distribution d’homologue permettent d’utiliser des ports de terminaison d’e/s ou des événements comme mécanismes de signalisation pour traiter les saisies semi-automatiques des opérations de distribution d’homologue asynchrones. Pour les deux mécanismes, la distribution d’homologue utilise une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . En général, la distribution d’homologue prend la propriété d’une structure **OVERLAPPED** et de tous les paramètres de sortie que le client passe aux fonctions API asynchrones. Le client ne doit pas accéder à ces ressources tant que la fonction asynchrone particulière n’est pas terminée. Dès que les fonctions asynchrones sont terminées, le service de distribution d’homologue n’a plus besoin d’accéder à ces ressources et elles peuvent être réutilisées à mesure que l’application appelante s’affiche.

Il n’y aura pas de saisie semi-automatique asynchrone si la fonction retourne un code d’erreur autre que des **\_ e/s d’erreur \_ en attente**. Le retour d’une valeur autre que l' **erreur d' \_ e/s \_ en attente** signifie que l’appel a échoué de façon synchrone. Si l’API de distribution d’homologue retourne des **\_ e/s d’erreur \_ en attente**, l’appelant doit attendre la fin asynchrone.

Le code d’erreur de la saisie semi-automatique asynchrone peut être récupéré de l’une des deux manières suivantes :

**Achèvement basé sur le port de terminaison d’e/s**

L’utilisateur appelle le mécanisme de port de terminaison d’e/s en fournissant un handle de port d’achèvement et une clé de fin aux fonctions d’API suivantes :

<dl>

[**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)  
[**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)  
[**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)  
[**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)  
</dl>

L’utilisateur crée un port de terminaison en appelant [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport). Ce handle de port d’achèvement peut être utilisé simultanément pour d’autres opérations d’e/s asynchrones, ainsi que pour des opérations spécifiques de distribution d’homologue.

L’appelant doit utiliser la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) pour gérer la saisie semi-automatique asynchrone. Si l’opération asynchrone échoue, la fonction **GetQueuedCompletionStatus** retourne la **valeur false** et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur approprié. L’appelant doit ignorer tous les champs de la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) si le code d’erreur est différent du **\_ succès** de l’erreur. L’opération asynchrone est réussie si la fonction **GetQueuedCompletionStatus** retourne la **valeur true**.

Pour plus d’informations, consultez [ports de terminaison d’e/s](/windows/desktop/FileIO/i-o-completion-ports).

**Achèvement basé sur les événements**

Si l’appelant définit un handle d’événement valide pour le champ *hEvent* de la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , la distribution d’homologue l’utilise pour signaler que l’opération d’e/s asynchrone associée est terminée.

Un appelant de thread peut gérer des opérations avec chevauchement en spécifiant un handle vers l’objet d’événement de réinitialisation manuelle de la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) dans l’une des fonctions d’attente. Une fois l’événement signalé, l’appelant doit appeler [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**) en passant la structure **OVERLAPPED** appropriée. **PeerGetOverlappedResult** retourne la **valeur false** et l’appelant doit appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour récupérer le code d’erreur. L’appelant doit ignorer tous les champs de la structure **OVERLAPPED** si le code d’erreur est différent du **\_ succès** de l’erreur. L’opération asynchrone est réussie si la fonction **PeerGetOverlappedResult** retourne la **valeur true**.

Si l’appelant fournit un port de terminaison avec un événement, l’événement sera utilisé comme mécanisme de terminaison.

**Windows 7 :** Utilisez la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) à la place de [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur l’API de distribution d’homologue](peer-distribution-api-reference.md)
</dt> </dl>

 

