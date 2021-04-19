---
title: Proxy
description: Un proxy réside dans l’espace d’adressage du processus appelant et agit comme un substitut pour l’objet distant.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11257dd060f51bef118a4afc0cc35acf995c111
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "106538416"
---
# <a name="proxy"></a>Proxy

Un proxy réside dans l’espace d’adressage du processus appelant et agit comme un substitut pour l’objet distant. Du point de vue de l’objet appelant, le proxy est l’objet. En règle générale, le rôle du proxy consiste à empaqueter les paramètres d’interface pour les appels aux méthodes dans ses interfaces d’objet. Le proxy transmet les paramètres dans une mémoire tampon de messages et passe la mémoire tampon sur le canal, qui gère le transport entre les processus. Le proxy est implémenté sous la forme d’un objet d’agrégation, ou composite. Il contient une partie fournie par le système, appelée gestionnaire proxy et un ou plusieurs composants spécifiques à l’interface appelés proxys d’interface. Le nombre de proxys d’interface est égal au nombre d’interfaces d’objets qui ont été exposées à ce client particulier. Pour le client qui respecte le modèle d’objet de composant, le proxy semble être l’objet réel.

> [!Note]  
> Avec le marshaling personnalisé, le proxy peut être implémenté de la même façon ou il peut communiquer directement avec l’objet sans utiliser de stub.

 

Chaque proxy d’interface est un objet de composant qui implémente le code de marshaling pour l’une des interfaces de l’objet. Le proxy représente l’objet pour lequel il fournit le code de marshaling. Chaque proxy implémente également l’interface [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) . Bien que l’interface d’objet représentée par le proxy soit publique, l’implémentation de **IRpcProxyBuffer** est privée et est utilisée en interne dans le proxy. Le gestionnaire proxy effectue le suivi des proxies d’interface et contient également l’implémentation publique de l’interface de contrôle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pour l’agrégat. Chaque proxy d’interface peut exister dans une DLL distincte qui est chargée lorsque l’interface qu’il prend en charge est matérialisée au client.

## <a name="structure-of-the-proxy"></a>Structure du proxy

Le diagramme suivant illustre la structure d’un proxy qui prend en charge le marshaling standard de paramètres appartenant à deux interfaces : IA1 et IA2. Chaque proxy d’interface implémente [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) pour la communication interne entre les éléments d’agrégation. Lorsque le proxy est prêt à passer ses paramètres marshalés à travers la limite de processus, il appelle des méthodes dans l’interface [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) , qui est implémentée par le canal. Le canal transfère à son tour l’appel à la bibliothèque Runtime RPC afin qu’il puisse atteindre sa destination dans l’objet.

![Diagramme qui montre la structure du proxy.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Communication entre les objets](inter-object-communication.md)
</dt> <dt>

[Détails du marshaling](marshaling-details.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Talon](stub.md)
</dt> </dl>

 

 