---
description: Fonctionnalités de la source réseau
ms.assetid: a4e20ecb-c145-4823-ae59-f6fc88593d86
title: Fonctionnalités de la source réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a06b945f82093d5ff235eef306768e68b9f9771a2816df9a4580adab2d8dde8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871886"
---
# <a name="network-source-features"></a>Fonctionnalités de la source réseau

La source réseau fournit l’implémentation de base pour la diffusion en continu des fichiers multimédias et expose l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . L’implémentation spécifique de la source réseau dépend du protocole utilisé pour ouvrir la source, par exemple RTSP ou HTTP. Les sources réseau spécifiques au protocole étendent les fonctionnalités réseau de base. Pour plus d’informations sur les schémas et les protocoles pris en charge, consultez [protocoles pris en charge](supported-protocols.md).

La source réseau :

-   Implémente des fonctionnalités telles que la mise en cache, la détection de proxy et la reconnexion automatique.
-   Convertit les appels indépendants du protocole du programme de résolution source en appels spécifiques au protocole.
-   Interagit avec la couche de socket et le système d’exploitation. Analyse la description SDP et l’utilise comme données de configuration, puis lit les données de flux à partir de la couche de sockets sous-jacente. Lors de la réception, la source réseau est responsable de la réorganisation et de la demande de retransmission des paquets.

## <a name="network-source-creation"></a>Création de la source réseau

La création d’une source de média pour une source à partir du réseau n’est pas différente d’une source de média pour un fichier local. L’application passe l’URL pour les méthodes de programme de [résolution](source-resolver.md) source aux sources comme [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) ou [**IMFSourceResolver :: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) et spécifie l' \_ indicateur MEDIASOURCE de résolution MF \_ . Pour plus d’informations sur l’utilisation de cet indicateur, consultez [utilisation du programme de résolution source](using-the-source-resolver.md).

Selon le schéma fourni par l’application, le programme de résolution source charge l’objet gestionnaire de schéma approprié, qui expose l’interface [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) . L’application peut également utiliser le gestionnaire de schéma directement pour créer la source réseau en appelant [**IMFSchemeHandler :: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject).

Pour plus d’informations, consultez [gestionnaires de modèles et gestionnaires de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

Media Foundation ne prend pas en charge les flux d’octets pour les sources réseau. L’objet de flux d’octets est pris en charge uniquement dans le scénario de contenu téléchargé. Toutes les données sont transmises aussi rapidement que possible afin qu’elles puissent être enregistrées sous la forme d’un fichier sur l’ordinateur local. les serveurs Web fournissent des données téléchargées. Il n’y a aucune communication entre le client et le serveur une fois le téléchargement démarré. Dans ce cas, le protocole de téléchargement HTTP est utilisé.

Si l’application demande au programme de résolution de la source de créer un objet de flux d’octets pour les schémas « http : », « MMS : » ou « RTSP : », l’appel échoue avec l' \_ \_ erreur de schéma non pris en charge MF E \_ .

> [!Note]  
> dans Windows 7, la source réseau prend en charge les fichiers de Station Windows Media (. NSC). Ces fichiers sont utilisés dans la diffusion en continu de contenu multimédia sur un réseau. Pour créer la source réseau pour un spécifié. Fichier NSC, l’application doit utiliser le programme de résolution source.

 

Si l’application utilise le gestionnaire de schémas, l’appel asynchrone ignore le paramètre *dwFlags* et retourne un pointeur vers la source réseau à l’achèvement.

L’illustration suivante montre le flux de données pour la diffusion multimédia en continu à l’aide de la source réseau.

![Organigramme présentant les chemins d’accès de l’application au serveur de diffusion en continu, avec une boucle entre la source réseau et la session multimédia](images/3f9186ea-53ed-4a31-a097-92f39fa08624.gif)

## <a name="network-source-configuration"></a>Configuration de la source réseau

Cette rubrique décrit les fonctionnalités prises en charge par la source réseau et les options de configuration associées. Une application peut configurer la source réseau lors de la création de l’objet source réseau. Ces options sont stockées dans un objet **IPropertyStore** , que l’application doit transmettre dans le paramètre *pProps* des méthodes de résolution source ou [**IMFSchemeHandler :: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject).

### <a name="auto-reconnect"></a>Reconnexion automatique

La fonctionnalité de reconnexion automatique de la source réseau permet à un client de se reconnecter automatiquement au serveur multimédia lorsque la connexion TCP au serveur échoue ou que le client ne reçoit pas de paquets. En cas d’échec de la connexion, la source réseau tente de se reconnecter au serveur multimédia à l’aide de la même configuration que celle utilisée dans la connexion précédente. Le processus de reconnexion est asynchrone. La source réseau déclenche l’événement [MEReconnectStart](mereconnectstart.md) lorsqu’elle commence la reconnexion et l’événement [MEReconnectEnd](mereconnectend.md) lorsque la reconnexion réussit ou échoue.

Si le nombre de tentatives de reconnexion dépasse la valeur maximale spécifiée par la propriété [**MFNETSOURCE \_ AUTORECONNECTLIMIT**](mfnetsource-autoreconnectlimit-property.md) , l’opération de reconnexion est annulée. Le nombre de tentatives de reconnexion est stocké dans la propriété [**MFNETSOURCE \_ AUTORECONNECTPROGRESS**](mfnetsource-autoreconnectprogress-property.md) .

La reconnexion automatique permet une lecture fluide du contenu multimédia, même lorsque la connexion TCP au serveur multimédia échoue. Pour une expérience de lecture sans heurts, le client doit disposer de données suffisantes, au moins 1 à 2 minutes, dans son cache pour continuer la lecture jusqu’à la reconnexion. La quantité maximale de données que la source réseau peut mettre en mémoire tampon peut être définie dans la propriété [**MFNETSOURCE \_ MAXBUFFERTIMEMS**](mfnetsource-maxbuffertimems-property.md) .

### <a name="fast-streaming"></a>Streaming rapide

Le client source réseau demande au serveur de diffuser une partie des données au début du contenu à un rythme plus rapide que celui spécifié par la vitesse de transmission du contenu. Si le *démarrage rapide* est activé sur le serveur, le serveur envoie un flux à vitesse de transmission accélérée afin que le client puisse mettre en mémoire tampon une quantité de données suffisante plus rapidement que en temps réel. Cela améliore l’expérience utilisateur en réduisant les délais de mise en mémoire tampon initiaux, ce qui peut être dû à plusieurs facteurs tels que la lenteur de l’ordinateur client ou du réseau, ainsi que la bande passante disponible.

Pour spécifier la quantité de données de streaming rapide que le client peut demander, définissez la propriété [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) . Si la source réseau utilise UDP comme protocole de transport, spécifiez la quantité maximale de données de streaming rapide en définissant la propriété [**MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION**](mfnetsource-maxudpacceleratedstreamingduration-property.md) à la place.

La diffusion rapide sur le client est également possible via la fonction de *mise en cache rapide* , qui diffuse le contenu à la demande plus rapidement que le temps réel et met en cache les données sur le cache local du client. Pour utiliser ce type de diffusion rapide, le cache rapide doit être activé sur la source réseau, et le serveur doit le prendre en charge. Lorsque le client demande du contenu à partir du serveur, la source réseau vérifie d’abord si le contenu se trouve déjà dans le cache du client. Si le contenu se trouve dans le cache local du client et n’a pas expiré, il est rendu. Si le contenu n’est pas dans le cache local ou a déjà expiré, le contenu est diffusé et mis en cache, et la source réseau la lit à partir du cache local. Dans les demandes suivantes, pour les sélections, seules les entrées manquantes sont mises en cache, puis lues. Si une entrée de sélection se trouve déjà dans le cache local du client, elle est lue à partir de là et n’est pas mise en cache.

Par défaut, le cache rapide est activé sur le client source réseau. Toutefois, les facteurs suivants déterminent également si la fonctionnalité est utilisée :

-   Le client doit disposer d’une bande passante supplémentaire pour télécharger et mettre en cache le contenu plus rapidement que la vitesse normale.
-   Le client doit disposer d’un espace disque suffisant. Si le client dispose de moins de 100 Mo d’espace disque disponible après la mise en cache du contenu à la demande demandé, il n’est pas mis en cache, mais est diffusé et rendu simultanément.

La fonctionnalité de mise en cache rapide est contrôlée par la propriété [**MFNETSOURCE \_ CACHEENABLED**](mfnetsource-cacheenabled-property.md) .

### <a name="buffer-management"></a>Gestion des tampons

La source réseau fournit une gestion de mémoire tampon efficace qui surveille l’état de la mémoire tampon sur le client. Par défaut, la source réseau met en mémoire tampon 5 secondes de données au démarrage. Cette valeur peut être configurée en définissant la propriété [**MFNETSOURCE \_ BUFFERINGTIME**](mfnetsource-bufferingtime-property.md) . Sur la base de cette valeur de propriété, la source réseau calcule la taille de la mémoire tampon qui est suffisante pour garantir une lecture fluide et ininterrompue du contenu multimédia. Si cette propriété a la valeur 0, la gestion de la mémoire tampon est désactivée. Lorsque la quantité de contenu de la mémoire tampon est faible, la source réseau démarre la mise en mémoire tampon et déclenche l’événement [MEBufferingStarted](mebufferingstarted.md) pour indiquer que la mise en mémoire tampon a commencé. Lors de la réception de cet événement, le pipeline arrête le rendu. Lorsque la mise en mémoire tampon est terminée, la source réseau déclenche l’événement [MEBufferingStopped](mebufferingstopped.md) , et le client peut redémarrer le rendu.

Le client démarre le rendu du contenu une fois qu’il a accumulé la quantité de données indiquée par la taille de la mémoire tampon du premier échantillon. Si cette valeur est inférieure à la taille de la mémoire tampon calculée, la lecture démarre immédiatement. Ce comportement est très similaire à la fonctionnalité de démarrage rapide.

La propriété [**MFNETSOURCE \_ MAXBUFFERTIMEMS**](mfnetsource-maxbuffertimems-property.md) stocke la quantité maximale de données pouvant être mises en mémoire tampon.

### <a name="bandwidth-selection"></a>Sélection de la bande passante

Lorsqu’un client se connecte au serveur multimédia, dans le cadre de la configuration de la connexion, la source réseau effectue *une mesure statique de paires de paquets* pour estimer la bande passante de liaison initiale entre le client et le serveur. En fonction du résultat de cette mesure, le client peut sélectionner des flux audio et vidéo qui tiennent dans la bande passante estimée. Cela garantit une lecture fluide du contenu multimédia de diffusion en continu.

Pendant la phase de démarrage rapide, la mesure *dynamique de paire de paquets* est exécutée. Dans ce processus, le client reçoit de grandes quantités de données, qui peuvent être plusieurs paquets ou échantillons.

Le résultat de la mesure dynamique des paires de paquets est plus précis que l’estimation de la bande passante de liaison retournée par la mesure statique de paires de paquets, car le processus de paire de paquets statiques envoie un seul paquet de taille fixe, ce qui peut ne pas produire des résultats exacts pour les réseaux à bande passante élevée.

L’application peut récupérer la bande passante estimée à l’aide de la propriété [**MFNETSOURCE \_ PPBANDWIDTH**](mfnetsource-ppbandwidth-property.md) .

Les conditions réseau peuvent changer de manière dynamique, provoquant ainsi des problèmes de lecture de la source réseau. La source réseau peut modifier la sélection du flux initial du client en fonction de la vitesse de réception et de l’état de la mémoire tampon. Par exemple, le client peut basculer vers une vitesse de transmission inférieure pendant la congestion du réseau et revenir à une vitesse de transmission supérieure lorsque le trafic réseau a été amélioré et que le client a accumulé un volume de contenu mis en mémoire tampon suffisant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



