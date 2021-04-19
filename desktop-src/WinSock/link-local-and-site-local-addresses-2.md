---
description: Les adresses IPv6 locales et de site local sont appelées adresses étendues.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Adresses IPv6 locales et de site local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515651"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a>Adresses IPv6 locales et de site local

Les adresses IPv6 locales et de site local sont appelées adresses étendues. L’API Windows Sockets (Winsock) prend en charge le membre d' **\_ \_ ID d’étendue Sin6** dans la structure [**sockaddr \_ in6**](sockaddr-2.md) pour une utilisation avec des adresses délimitées. Pour les adresses IPv6 lien-local (FE80 ::/10 préfixe), le membre de l' **\_ \_ ID d’étendue Sin6** dans la structure **sockaddr \_ in6** est le numéro d’interface. Pour les adresses locales de site IPv6 (préfixe FEC0 ::/10), le membre de l' **\_ \_ ID d’étendue Sin6** dans la structure **\_ in6 sockaddr** est un identificateur de site.

Voici un exemple d’adresse IPv6 de liaison locale sur \# l’interface 5 :

``` syntax
fe80::208:74ff:feda:625c%5
```

La commande suivante est disponible sur Windows XP avec Service Pack 1 (SP1) et versions ultérieures pour interroger et configurer IPv6 sur un ordinateur local :

-   [Netsh.exe](netsh-exe.md)

Les modifications de configuration effectuées à l’aide des commandes Netsh.exe sont permanentes et ne sont pas perdues lors du redémarrage de l’ordinateur ou du protocole IPv6.

Avant Windows XP avec Service Pack 1 (SP1), la configuration et la gestion IPv6 utilisaient plusieurs anciens outils en ligne de commande (Net.exe, Ipv6.exe et Ipsec6.exe) pour configurer et gérer IPv6. À l’aide de ces outils plus anciens, les modifications IPv6 ne sont pas permanentes et sont perdues lorsque l’ordinateur ou le protocole IPv6 a été redémarré. Ces anciens outils en ligne de commande sont uniquement pris en charge sur Windows XP.

Sur Windows XP avec SP1, la commande suivante affiche la liste des interfaces IPv6 sur un ordinateur local, y compris l’index d’interface, le nom de l’interface et diverses autres propriétés de l’interface.

**netsh interface ipv6 show interface**

Sur Windows XP avec SP1, la commande suivante permet de modifier l’identificateur de site associé à un index d’interface.

**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid = valeur**

Sur Windows XP, la commande antérieure suivante remplacera également l’identificateur de site associé à une adresse de site local par 3.

**FEC0 RTU IPv6 ::/10 3**

Si vous envoyez ou vous vous connectez à une adresse délimitée, le membre de l' **\_ \_ ID d’étendue Sin6** dans la structure [**sockaddr \_ in6**](sockaddr-2.md) peut être laissé non spécifié (zéro), ce qui représente une adresse étendue ambiguë. Par exemple, l’adresse lien-local suivante est ambiguë :

``` syntax
fe80::10
```

Si vous effectuez une liaison à une adresse délimitée, le membre de l' **\_ \_ ID d’étendue Sin6** dans la structure [**\_ in6 sockaddr**](sockaddr-2.md) doit contenir une valeur différente de zéro qui spécifie un numéro d’interface valide pour une adresse lien-local ou un identificateur de site pour une adresse de site local.

## <a name="ambiguous-scoped-addresses"></a>Adresses étendues ambiguës

Si vous envoyez ou vous vous connectez à une adresse délimitée et que vous n’avez pas spécifié le membre de l' **\_ \_ ID d’étendue Sin6** dans la structure [**sockaddr \_ in6**](sockaddr-2.md) , l’adresse étendue est ambiguë. Pour résoudre ce comportement, le protocole IPv6 détermine d’abord si vous avez lié le socket à une adresse source. Si c’est le cas, l’adresse source liée résout l’ambiguïté en fournissant un numéro d’interface ou un identificateur de site.

Si vous envoyez ou vous vous connectez à une adresse délimitée et que vous n’avez pas spécifié le membre de l' **\_ \_ ID d’étendue Sin6** ou lié une adresse source, le protocole IPv6 vérifie la table de routage. Par exemple, la commande suivante affiche la table de routage IPv6 sur un ordinateur local :

**netsh interface ipv6 show route**

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

Cela indique que les adresses lien-local sont traitées par défaut en tant que liens sur les interfaces \# 13 et \# 14.

Une ambiguïté se produit lorsqu’un ordinateur local possède plusieurs cartes réseau. Par exemple, la commande **netsh** ci-dessus indique qu’il existe deux interfaces réseau (connexion au réseau local et connexion réseau sans fil). Lorsqu’une application spécifie une adresse lien-local de destination (FE80 :: 10, par exemple) sans ID d’étendue, il n’est pas évident de savoir quel adaptateur utiliser pour envoyer le paquet. Seule une monodiffusion de liaison locale de liaison (FE80 ::/64) ou une adresse de destination IPv6 de multidiffusion d’étendue de liaison (FF00 ::/8) peut être affectée de l’absence d’un ID d’étendue lors de l’envoi d’un paquet.

## <a name="neighbor-discovery"></a>Découverte de voisin

Si vous n’avez pas spécifié le membre de l' **\_ \_ ID de l’étendue Sin6** dans la structure [**\_ in6 sockaddr**](sockaddr-2.md) , que vous n’avez pas lié une adresse source et que vous n’avez pas spécifié d’itinéraire pour les adresses lien-local, le protocole IPv6 essaiera la découverte du voisin pour résoudre l’adresse lien-local de destination. Pour un paquet donné en cours d’envoi, une interface est tentée. Cette première interface qui est tentée est considérée comme l’interface la plus préférée. Si la découverte de voisins ne parvient pas à résoudre l’adresse lien-local sur une interface, le paquet à envoyer est supprimé et le système se souvient que l’adresse lien-local de destination n’est pas accessible sur cette interface. Sur le paquet suivant à envoyer dans les mêmes conditions, une interface différente est tentée pour la découverte de voisins. Ce processus continue à traverser chacune des interfaces sur un ordinateur local pour chaque nouveau paquet jusqu’à ce que la découverte du voisin réponde pour l’adresse lien-local de destination ou que toutes les interfaces possibles aient été essayées et échouées. Chaque fois qu’une tentative de résolution du voisin échoue, une interface est supprimée pour ce voisin.

Si l’adresse lien-local de destination est résolue, cette interface est utilisée pour envoyer le paquet actuel. Cette interface est également utilisée pour tous les paquets de portée ambiguë suivants qui sont envoyés à la même adresse de destination lien-local.

Si la découverte de voisins ne parvient pas à résoudre l’adresse lien-local de destination sur toutes les interfaces, le système tente alors d’envoyer le paquet sur l’interface la plus préférée (la première interface essayée). La pile réseau continue de tenter de résoudre l’adresse lien-local de destination sur l’interface la plus préférée. Après un certain laps de temps après l’échec de la découverte de voisins sur toutes les interfaces, la pile réseau redémarre le processus et tente de résoudre l’adresse lien-local de destination sur toutes les interfaces. Actuellement, cet intervalle de temps pendant lequel la découverte du voisin est de nouveau effectuée sur toutes les interfaces est de 60 secondes. Toutefois, cet intervalle de temps peut changer sur les versions de Windows et ne doit pas être utilisé par une application.

> [!Note]  
> Si une application lie la même adresse lien-local à une autre interface après que la découverte du voisin a résolu l’adresse lien-local, cela ne remplace pas l’interface par l’adresse de destination lien-local renvoyée par la découverte de voisins.

 

Pour plus d’informations sur la découverte de voisins pour IP version 6, consultez [RFC4861](https://tools.ietf.org/html/rfc4861) publié par l’IETF.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Préfixes de site IPv6](site-prefixes-2.md)
</dt> <dt>

[Ipv6.exe](ipv6-exe-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> <dt>

[Utilisation d'une adresse IPv6](using-ipv6-2.md)
</dt> </dl>

 

 



