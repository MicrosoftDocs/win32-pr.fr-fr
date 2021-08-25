---
title: Couches ALE
description: L’application de la couche application (ALE) est constituée de plusieurs couches de filtrage et de nombreuses couches de rejet correspondantes.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9d13c7b5493171caa7216e8f2991e0350b79dd46dca612f241c9446cafa39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901009"
---
# <a name="ale-layers"></a>Couches ALE

L’application de la couche application (ALE) est constituée de plusieurs couches de filtrage et de nombreuses couches de rejet correspondantes. toutes les couches du moteur de filtrage de la plateforme de filtrage Windows (WFP), y compris ALE, sont décrites dans [**filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md). Cette rubrique contient une description plus détaillée des couches de filtrage qui font partie de ALE.

## <a name="resource_assignment"></a>attribution de ressources \_

Un filtre a été mis en correspondance pour les opérations de liaison réseau, explicites ou implicites, au niveau de la couche [**FWPM \_ allocation de ressources ALE de la couche \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) .

Si un filtre à cette couche est mis en correspondance pour autoriser la création de sockets bruts, l’indicateur de condition fwp est défini sur indicateur de [**\_ point de \_ \_ \_ \_ terminaison brut**](filtering-condition-flags-.md) .

Si un filtre de cette couche est mis en correspondance pour autoriser la réception du mode de proximité, le champ du [**\_ \_ \_ \_ mode de proximité ALE de condition fwp**](filtering-condition-identifiers-.md) est défini sur SIO \_ RCVALL. Pour obtenir une description de SIO \_ RCVALL, consultez [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).

> [!Note]  
> Il s’agit de la seule couche dans laquelle le mode de proximité peut être filtré.

 

Si aucun port n’est spécifié lors de la **liaison ()**, autrement dit, si le port est défini sur 0 (zéro), la pile TCP/IP sélectionne un port de la plage de ports dynamiques (19152 – 65535). Le port sélectionné sera classé à cette couche avec l’indicateur de [**condition fwp est un indicateur de \_ \_ \_ \_ \_ liaison de caractères génériques**](filtering-condition-flags-.md) .

Si l’adresse locale n’est pas spécifiée dans l’appel [**Bind ()**](/windows/desktop/api/winsock/nf-winsock-bind) , le champ adresse locale a la [**valeur \_ fwp vide**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).

## <a name="auth_listen"></a>écoute d’authentification \_

Un filtre au niveau de la couche FWPM d’écoute de l' [**\_ \_ écouteur d’authentification ALE de la couche \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) est mis en correspondance pour les appels d' [**écoute TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-listen) .

## <a name="auth_recv_accept"></a>acceptation de l’autorisation \_ recv \_

Un filtre au niveau de la couche [**FWPM d' \_ authentification ALE de la couche ALE est \_ \_ \_ \_ accepté \_ \|**](management-filtering-layer-identifiers-.md) pour les appels TCP [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) , pour les premiers paquets UDP (monodiffusion) à partir d’une adresse distante unique/d’un tuple de port, et pour les premiers messages ICMP non-erreur entrante (monodiffusion) avec un type, un code et un ID ICMP uniques.

> [!Note]  
> Les protocoles qui ne sont pas TCP ou ICMP sont traités comme UDP.

 

Les paquets TCP reçus par les sockets bruts sont gérés de la même façon que le trafic UDP. Autrement dit, seul le premier TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) et le premier TCP [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) sur des sockets bruts seront filtrés.

## <a name="auth_connect"></a>connexion d’authentification \_

Un filtre au niveau de la couche [**FWPM d' \_ \_ authentification ALE de couche ALE \_ \_ \_ \|**](management-filtering-layer-identifiers-.md) est mis en correspondance pour les appels TCP [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) , pour les premiers paquets UDP envoyés à une adresse distante et un TUPLE de port uniques, et pour les premiers messages ICMP non-erreur sortants avec un type, un code et un ID ICMP uniques.

> [!Note]  
> Les protocoles qui ne sont pas TCP ou ICMP sont traités comme UDP.

 

Les paquets TCP envoyés par les sockets bruts sont gérés de la même façon que le trafic UDP. Autrement dit, seul le premier TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) et le premier TCP [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) sur des sockets bruts seront filtrés.

## <a name="flow_established"></a>FLOW \_ établi

Un filtre au niveau de la couche FWPM de la couche [**\_ \_ ALE \_ \_ établie \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) est mis en correspondance après la réussite d’une négociation TCP triple. Pour le trafic non-TCP, le filtre est mis en correspondance immédiatement après la mise en correspondance des filtres des couches d’authentification/d' **authentification \_** des **autorisations de \_ réception \_ d’authentification** .

Un filtre au niveau de cette couche ne doit pas retourner de bloc ou d’autorisation.

cette couche est utilisée par les pilotes de légende pour suivre l’état de la connexion, décrite en détail dans la documentation du [Kit de pilotes Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .

## <a name="resource_release"></a>version de la ressource \_

Un filtre au niveau de la couche FWPM de la mise à jour de la [**\_ ressource ALE de la couche \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) est mis en correspondance après la libération des ressources allouées via l' **\_ attribution de ressources** .

## <a name="endpoint_closure"></a>fermeture du point de terminaison \_

Un filtre au niveau de la couche [**FWPM de clôture du point de terminaison ALE de la \_ couche \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) est mis en correspondance lorsqu’un protocole TCP connecté ou un point de terminaison de sockets UDP est fermé.

## <a name="connect_redirect"></a>\_rediriger la connexion

Un filtre au niveau de la couche [**FWPM \_ redirection de la connexion ALE de la couche \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) permet la modification des adresses et des ports distants. La connexion sortante est redirigée pour la durée de cette connexion.

## <a name="bind_redirect"></a>redirection de liaison \_

Un filtre au niveau de la couche [**FWPM de \_ redirection de liaison ALE de la couche \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) permet de modifier l’adresse locale et les ports du Socket sous-jacent. Le socket local sera redirigé pendant la durée de vie du socket

## <a name="ale-discard-layers"></a>Couches de rejet ALE

Pour chaque couche ALE décrite ci-dessus, le moteur de filtrage contient une couche correspondante à ignorer. Les couches de rejet ALE sont utilisées par les légendes à des fins de journalisation. Les paquets et les indications qui ont été ignorés dans l’une des couches de filtrage ALE sont indiqués dans la couche de suppression ALE correspondante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Application de la couche application (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Filtrage avec état ALE](ale-stateful-filtering.md)
</dt> <dt>

[Trafic de diffusion/multidiffusion ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Réautorisation ALE](ale-re-authorization.md)
</dt> <dt>

[personnalisation de la Flow ALE](ale-flow-customization.md)
</dt> <dt>

[Flux de paquets TCP](tcp-packet-flows.md)
</dt> <dt>

[Flux de paquets UDP](udp-packet-flows.md)
</dt> <dt>

[Fonctions Winsock](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[**Indicateurs de condition de filtrage**](filtering-condition-flags-.md)
</dt> <dt>

[**Conditions de filtrage disponibles pour chaque couche de filtrage**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 