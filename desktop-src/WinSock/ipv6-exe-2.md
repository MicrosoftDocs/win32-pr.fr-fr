---
description: Toutes les configurations IPv6 sont effectuées à l’aide de l’outil Ipv6.exe.
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201428"
---
# <a name="ipv6exe"></a>Ipv6.exe

Toutes les configurations IPv6 sont effectuées à l’aide de l’outil Ipv6.exe. Cet outil est principalement utilisé pour l’interrogation et la configuration des interfaces, des adresses, des caches et des itinéraires IPv6. Les sous-commandes IPv6 sont les suivantes :

<dl> <dt>

<span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6 si** \[ que\#\]
</dt> <dd>

Affiche des informations sur les interfaces. Si un numéro d’interface est spécifié, seules les informations relatives à cette interface sont affichées. Dans le cas contraire, des informations sur toutes les interfaces sont affichées. La sortie inclut l’adresse de la couche de liaison de l’interface et la liste des adresses IPv6 affectées à l’interface, y compris l’unité de transmission maximale actuelle de l’interface et la MTU maximale (true) que l’interface peut prendre en charge.

L’interface \# 1 est une pseudo-interface utilisée pour le bouclage. L’interface \# 2 est une pseudo-interface utilisée pour le tunneling configuré, le tunneling automatique et le tunneling 6to4. Les autres interfaces sont numérotées de façon séquentielle dans l’ordre dans lequel elles sont créées. Cet ordre varie d’un ordinateur à un autre.

Les adresses de couche de liaison au format *AA* - *BB* - *CC* - *JJ* - *EE* - *FF* sont des adresses Ethernet. Adresse de couche de liaison dans *un*. *b*. *c*. la forme *d* sont des interfaces 6-sur-4. Pour plus d’informations sur 6-sur-4, consultez la RFC 2529.

Les deux pseudo-interfaces n’utilisent pas la découverte du voisin IPv6.

</dd> <dt>

<span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**IFC IPv6** si \# \[ transfère \] \[ \] \[ des publications-transfère \] \[ -publie les \] \[ octets MTU site \# site \] \[ -identifier\]
</dt> <dd>

Contrôle les attributs d’interface. Les interfaces peuvent être transférées, auquel cas elles transfèrent les paquets avec des adresses de destination non attribuées à l’interface. Les interfaces peuvent être publicitaires, auquel cas elles envoient des publications de routeur. Ces attributs peuvent être contrôlés indépendamment. Une interface envoie les sollicitations de routeur et reçoit les annonces de routeur, ou reçoit les sollicitations de routeur et envoie les annonces de routeur.

Étant donné que les deux pseudo-interfaces n’utilisent pas la découverte de voisins, elles ne peuvent pas être configurées pour envoyer des annonces de routeur.

Les transferts peuvent être abrégés en FORW et publiés comme adv.

L’unité MTU de l’interface peut également être définie. La nouvelle unité de transmission maximale (MTU) doit être inférieure ou égale à l’unité de transmission maximale (true) du lien (comme indiqué par IPv6 si) et supérieure ou égale à l’unité MTU IPv6 minimale (1280 octets).

L’identificateur de site d’une interface peut également être modifié. Les identificateurs de site sont utilisés dans \_ le \_ champ ID d’étendue Sin6 avec des adresses de site local.

</dd> <dt>

<span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IFD IPv6** si\#
</dt> <dd>

Supprime une interface. Les pseudo-interfaces de bouclage et de tunnel ne peuvent pas être supprimées.

</dd> <dt>

<span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**contexte de nommage IPv6** \[ \# \[ adresse if\]\]
</dt> <dd>

Affiche le contenu du cache du voisin. Si un numéro d’interface est spécifié, seul le contenu du cache du voisin de cette interface est affiché. Sinon, le contenu de tous les caches voisins de l’interface est affiché. Si une interface est spécifiée, une adresse IPv6 peut être spécifiée pour afficher uniquement cette entrée de cache du voisin.

Pour chaque entrée de cache du voisin, l’interface, l’adresse IPv6, l’adresse de couche de liaison et l’état d’atteinte sont affichées.

</dd> <dt>

<span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**IPv6 NCF** \[ \# \[ adresse if\]\]
</dt> <dd>

Vide les entrées de cache du voisin spécifiées. Seules les entrées de cache du voisin sans références sont purgées. Étant donné que les entrées du cache d’itinéraire contiennent des références aux entrées de cache du voisin, le cache d’itinéraire doit d’abord être vidé. Les entrées de la table de routage peuvent également contenir des références aux entrées du cache du voisin.

</dd> <dt>

<span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**RC IPv6** \[ \# adresse if\]
</dt> <dd>

Affiche le contenu du cache d’itinéraire. Le cache d’itinéraire est le nom de l’implémentation Microsoft IPv6 pour le cache de destination. Si une interface et une adresse sont spécifiées, l’entrée du cache d’itinéraire pour atteindre l’adresse par le biais de l’interface s’affiche. Dans le cas contraire, toutes les entrées du cache d’itinéraire sont affichées.

Pour chaque entrée du cache d’itinéraire, l’adresse IPv6 et l’interface du saut suivant et l’adresse voisin sont affichées. L’adresse source par défaut à utiliser avec cette destination, la MTU de chemin actuelle pour atteindre cette destination via l’interface et la détermination de l’existence d’une entrée spécifique à l’interface-cache de routage sont également affichées. Toute adresse de précaution (pour la mobilité) pour l’adresse de destination s’affiche également.

Une adresse de destination peut avoir plusieurs entrées de cache d’itinéraires (autant qu’une adresse pour chaque interface sortante). Toutefois, une adresse de destination peut avoir au maximum une entrée du cache d’itinéraire qui n’est pas spécifique à l’interface. Une entrée spécifique à l’interface du cache d’itinéraire est utilisée uniquement si l’application spécifie explicitement cette interface sortante.

</dd> <dt>

<span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**RCF IPv6** \[ \# \[ adresse if\]\]
</dt> <dd>

Vide les entrées du cache d’itinéraire spécifiées.

</dd> <dt>

<span id="ipv6_bc"></span><span id="IPV6_BC"></span>**BC IPv6**
</dt> <dd>

Affiche le contenu du cache de liaison, qui contient les liaisons entre les adresses d’hébergement et les adresses d’hébergement pour Mobile IPv6.

Pour chaque liaison, l’adresse d’hébergement, l’adresse d’hébergement, le numéro de séquence de liaison et la durée de vie sont affichés.

</dd> <dt>

<span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**IPv6 Adu** si \# /address \[ Lifetime VL \[ /pl \] \] \[ anycast \] \[ monodiffusion\]
</dt> <dd>

Ajoute ou supprime une attribution d’adresse monodiffusion ou anycast sur une interface. L’adresse de monodiffusion est traitée si anycast n’est pas spécifié.

La durée de vie est infinie si elle n’est pas spécifiée. Si seule une durée de vie valide est spécifiée, la durée de vie préférée est égale à la durée de vie valide. Une durée de vie infinie peut être spécifiée, ou une valeur finie en secondes. La durée de vie préférée doit être inférieure ou égale à la durée de vie valide. La spécification d’une durée de vie de zéro entraîne la suppression de l’adresse.

Vous pouvez abréger la durée de vie en tant que vie.

Pour les adresses anycast, les seules valeurs de durée de vie valides sont zéro et Infinite.

</dd> <dt>

<span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**SPT IPv6**
</dt> <dd>

Affiche le contenu actuel de la table de préfixe de site.

Pour chaque préfixe de site, la commande affiche le préfixe, l’interface à laquelle le préfixe de site s’applique et la durée de vie du préfixe, en secondes.

Les préfixes de site sont normalement configurés automatiquement à partir des annonces de routeur. Ils sont utilisés dans la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) pour filtrer les adresses locales de site inappropriées.

</dd> <dt>

<span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>préfixe **SPU IPv6** si \# \[ durée de vie L\]
</dt> <dd>

Ajoute, supprime ou met à jour un préfixe dans la table de préfixe de site.

Le préfixe et le numéro d’interface sont requis. La durée de vie du préfixe de site, spécifiée en secondes, est définie par défaut sur Infinite s’il n’est pas spécifié. Si vous spécifiez une durée de vie de zéro, le préfixe de site est supprimé.

Cette commande n’est pas nécessaire pour la configuration normale des ordinateurs hôtes ou routeurs.

</dd> <dt>

<span id="ipv6_rt"></span><span id="IPV6_RT"></span>**RT IPv6**
</dt> <dd>

Affiche le contenu actuel de la table de routage.

Pour chaque entrée de table de routage, la commande affiche le préfixe d’itinéraire, une interface on-Link ou un voisin de saut suivant sur une interface, une valeur de préférence (plus petite est préférable) et une durée de vie en secondes.

Les entrées de la table de routage peuvent également avoir des attributs **Publish** et **Aging** . Par défaut, ils vieillissent (la durée de vie est inférieure à la constante restante) et ne sont pas publiés (ils ne sont pas utilisés dans la construction des publications de routeur).

Sur les ordinateurs hôtes, les entrées de la table de routage sont normalement configurées automatiquement à partir des annonces de routeur.

</dd> <dt>

<span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>préfixe **RTU IPv6** si \# \[ /nexthop \] \[ durée de vie \] \[ de la préférence P \] \[ publication \] \[ âge du \] \[ site-préfixe-longueur\]
</dt> <dd>

Ajoute ou supprime un itinéraire dans la table de routage. Le préfixe d’itinéraire est obligatoire. Le préfixe peut être défini sur un lien vers une interface spécifiée, ou un tronçon suivant, spécifié avec une adresse voisine sur une interface. L’itinéraire peut avoir une durée de vie en secondes, avec la valeur par défaut infinie et une préférence, avec la valeur par défaut zéro ou la plus préférée. Si vous spécifiez une durée de vie de zéro, l’itinéraire est supprimé.

Si la route est spécifiée en tant que publication, indiquant qu’elle sera utilisée dans la construction des publications de routeur, elle n’a pas d’ancienneté. La durée de vie de l’itinéraire n’est pas comptabilisée et est par conséquent infinie, mais la valeur est utilisée dans les annonces de routeur. Si vous le souhaitez, un itinéraire peut être spécifié comme un itinéraire publié qui vieillit également. Par défaut, un itinéraire non publié passe toujours à l’âge.

La sous-option SPL facultative peut être utilisée pour spécifier une longueur de préfixe de site associée à l’itinéraire. La longueur de préfixe de site est utilisée uniquement lors de l’envoi d’annonces de routeur.

La durée de vie peut être abrégée en vie, préférence en tant que préférences et publier en tant que pub.

</dd> </dl>

 

 



