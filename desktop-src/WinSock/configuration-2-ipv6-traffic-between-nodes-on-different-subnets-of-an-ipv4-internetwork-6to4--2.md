---
description: 6to4 est une méthode permettant de connecter des hôtes ou des sites IPv6 sur l’infrastructure Internet IPv4 existante.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Configuration 2 : trafic IPv6 entre les nœuds de différents sous-réseaux d’un interréseau IPv4 (6to4)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d976aa3ea21d990ea22f861fbf05a816866e6b0d21502211e23a0e331a2f851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112498"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a>Configuration 2 : trafic IPv6 entre les nœuds de différents sous-réseaux d’un interréseau IPv4 (6to4)

6to4 est une méthode permettant de connecter des hôtes ou des sites IPv6 sur l’infrastructure Internet IPv4 existante. Elle utilise un préfixe d’adresse unique pour fournir aux sites IPv6 isolés leur propre espace d’adressage IPv6. 6to4 est semblable à un « Pseudo-ISP » fournissant une connectivité IPv6. Vous pouvez utiliser 6to4 pour communiquer directement avec d’autres sites 6to4. 6to4 ne requiert pas l’utilisation de routeurs IPv6 et son trafic IPv6 est encapsulé avec un en-tête IPv4.

L’illustration suivante montre la configuration de deux nœuds sur des sous-réseaux distincts à l’aide de 6to4 pour communiquer sur un routeur IPv4.

![les nœuds qui utilisent 6to4 pour communiquer sur un routeur IPv4.](images/v6mig-2.png)

La principale exigence d’utiliser 6to4 est une adresse IPv4 globalement routable pour votre site. Supposons que votre site se compose d’un ensemble d’ordinateurs IPv6 que vous gérez (certains exécutant le protocole Microsoft IPv6 et d’autres implémentations IPv6). Supposons également que tous les ordinateurs IPv6 sont connectés directement via Ethernet ou 6-sur-4. L’adresse IPv4 globalement routable doit être affectée à l’un de vos ordinateurs exécutant le protocole Microsoft IPv6. Cet ordinateur sera votre passerelle 6to4.

si vous disposez d’une adresse IPv4 qui fait partie de l’espace d’adressage privé (10.0.0.0/8, 172.16.0.0/12 ou 192.168.0.0/16) ou de l’espace d’adressage APIPA (automatic private IP addressing) de 169.254.0.0/16 utilisé par Windows 2000, elle n’est pas globalement routable. Dans le cas contraire, il s’agit probablement d’une adresse IP publique qui est globalement routable. Pour plus d’informations sur la prise en charge de 6to4, consultez la rubrique [débogage de la configuration 6to4](#debugging-6to4-configuration) dans ce document.

## <a name="the-6to4cfgexe-tool"></a>Outil 6to4cfg.exe

L’outil 6to4cfg.exe automatise la configuration 6to4, découvre automatiquement votre adresse IPv4 globalement routable et crée un préfixe 6to4. Il effectue la configuration directement ou il peut écrire un script de configuration que vous pouvez inspecter et exécuter ultérieurement.

La syntaxe de la commande 6to4cfg.exe de base est la suivante.

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span id="_filename_"></span><span id="_FILENAME_"></span>\[*extension*\]
</dt> <dd>

Écrit le script de configuration dans un fichier, si vous spécifiez un nom de fichier. Le script de configuration utilise Ipv6.exe.

Vous pouvez spécifier con pour le nom de fichier pour écrire le script de configuration dans la sortie de la console, ce qui est utile pour voir ce que 6to4cfg.exe fera dans un scénario de test.

Si vous ne spécifiez pas de nom de fichier, 6to4cfg.exe met directement à jour la configuration IPv6 sur votre ordinateur.

</dd> <dt>

<span id="-r"></span><span id="-R"></span>-r
</dt> <dd>

Devient un routeur de passerelle 6to4 pour votre réseau local, ce qui permet le routage sur toutes vos interfaces et les préfixes de sous-réseau affectés.

</dd> <dt>

<span id="-s"></span><span id="-S"></span>-s
</dt> <dd>

Active l’adressage local du site dans votre site 6to4. Cette commande est utile uniquement lorsqu’elle est utilisée conjointement avec-r.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>-u
</dt> <dd>

Spécifie que la configuration 6to4 doit être inversée. Par conséquent, 6to4cfg-u inverse l’effet de 6to4cfg et 6to4cfg-r-u inverse l’effet de 6to4cfg-r, et ainsi de suite.

</dd> <dt>

<span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *Relay*
</dt> <dd>

Spécifie le nom ou l’adresse IPv4 d’un routeur relais 6to4. Le nom par défaut est 6to4.ipv6.microsoft.com, le routeur relais 6to4 sur Internet.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>-b
</dt> <dd>

Spécifie que 6to4cfg.exe sélectionne la « meilleure » adresse de relais au lieu du premier.

</dd> <dt>

<span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *adresse*
</dt> <dd>

Spécifie l’adresse IPv4 locale pour le préfixe 6to4.

</dd> </dl>

## <a name="manual-6to4-configuration"></a>Configuration 6to4 manuelle

Dans cet exemple, l’adresse de la passerelle 6to4 est 172.31.42.239. Vous avez besoin de votre propre adresse IPv4 globalement routable pour utiliser 6to4.

> [!Note]  
> L’adresse IP 172.31.42.239 est utilisée à titre d’exemple uniquement. Il s’agit d’une adresse privée qui n’est pas routable globalement sur Internet.

 

L’adresse IPv4 à routage global 32 bits est combinée au préfixe 16 bits 2002 ::/16 pour former un préfixe d’adresse IPv6 de 48 bits pour votre site. Dans cet exemple, le préfixe de site 6to4 est 2002 : ac1f : 2aef ::/48. Notez que ac1f : 2aef est l’encodage hexadécimal de 172.31.42.239 (bien sûr, vous allez utiliser un préfixe différent basé sur votre propre adresse IPv4 routable globalement). À l’aide du préfixe de site 6to4, vous pouvez affecter des adresses et des préfixes de sous-réseau à l’intérieur de votre site.

Cet exemple part du principe que vous utilisez le sous-réseau 0 pour configurer manuellement une adresse 6to4 sur votre ordinateur de passerelle 6to4 et que vous utilisez le sous-réseau 1 pour configurer automatiquement les adresses sur votre segment de réseau Ethernet. Toutefois, d’autres options sont possibles.

1.  Utilisez Ipv6.exe pour activer 6to4 sur votre ordinateur de passerelle 6to4 :

    **RTU IPv6 2002 ::/16 2**

    La commande **IPv6 RTU** effectue une mise à jour de la table de routage. Il peut être utilisé pour ajouter, supprimer ou mettre à jour un itinéraire. Dans ce cas, il active 6to4.

    L’argument 2002 ::/16 est le préfixe de l’itinéraire, en spécifiant le préfixe 6to4 unique.

    L’argument 2 spécifie l’interface sur lien pour ce préfixe. \#L’interface 2 est la « pseudo-interface » utilisée pour les tunnels configurés, le tunneling automatique et 6to4. Quand une adresse de destination IPv6 correspond au préfixe 2002 ::/16, les 32 bits qui suivent le préfixe dans l’adresse de destination sont extraits pour former une adresse de destination IPv4. Le paquet est encapsulé avec un en-tête IPv4 et envoyé à l’adresse de destination IPv4.

2.  Configurez une adresse 6to4 sur votre ordinateur de passerelle 6to4 :

    **IPv6 Adu 2/2002 : ac1f : 2aef :: ac1f : 2aef**

    La commande **IPv6 Adu** effectue une mise à jour d’adresse. Il peut être utilisé pour ajouter, supprimer ou mettre à jour une adresse sur une interface. Dans ce cas, il configure l’adresse 6to4 de l’ordinateur.

    L’argument 2/2002 : ac1f : 2aef :: ac1f : 2aef spécifie à la fois l’interface et l’adresse. Il requiert la configuration de l’adresse 2002 : ac1f : 2aef :: ac1f : 2aef sur l’interface \# 2. L’adresse est créée à l’aide du préfixe de site 2002 : ac1f : 2aef ::/48, sous-réseau 0 pour fournir un préfixe de sous-réseau : ac1f : 2aef ::/64 et un identificateur d’interface 64 bits. La Convention présentée utilise l’adresse IPv4 de l’ordinateur pour l’identificateur d’interface pour les adresses affectées à l’interface \# 2. Pour votre utilisation, ac1f : 2aef doit être remplacé par le codage hexadécimal de votre propre adresse IPv4 routable globalement.

Les deux commandes précédentes sont suffisantes pour permettre la communication avec d’autres sites 6to4. Par exemple, vous pouvez essayer d’exécuter une commande ping sur le site Microsoft 6to4 :

**ping6 2002:836b : 9820 :: 836b : 9820**

Pour activer la communication avec 6bone, vous devez créer un tunnel configuré par défaut vers un relais 6to4. Vous pouvez utiliser le routeur Microsoft 6to4 Relay, 131.107.152.32 :

**RTU IPv6 ::/0 2/ :: 131.107.152.32 pub Life 1800**

La commande **IPv6 RTU** effectue une mise à jour de la table de routage, en établissant, dans cette instance, un itinéraire par défaut vers le relais 6to4.

L’argument ::/0 est le préfixe d’itinéraire. Le préfixe de longueur zéro indique qu’il s’agit d’un itinéraire par défaut.

L’argument 2/ :: 131.107.152.32 spécifie le voisin de saut suivant pour ce préfixe. Elle nécessite que les paquets correspondant au préfixe soient transmis à address :: 131.107.152.32 à l’aide de l’interface \# 2. Le transfert d’un paquet vers :: 131.107.152.32 sur l’interface \# 2 provoque l’encapsulation d’un paquet avec un en-tête V4 et son envoi à 131.107.152.32.

L’argument pub rend cet itinéraire publié. Étant donné que cela ne concerne que les routeurs, il n’a aucun effet tant que le routage n’est pas activé. De même, la durée de vie de 30 minutes concerne uniquement si le routage est activé.

Vous devez être en mesure d’accéder aux sites 6bone et aux sites 6to4. Pour tester cela, vous pouvez utiliser la commande suivante :

**ping6 3FFE : 1cff : 0 : F5 :: 1**

La dernière étape consiste à activer le routage sur votre passerelle 6to4. Cet exemple suppose que l’interface \# 3 sur votre ordinateur de passerelle est une interface Ethernet et que l’interface \# 4 est 6-sur-4. Votre ordinateur peut numéroter ses interfaces différemment. Les deux commandes suivantes affectent des préfixes de sous-réseau aux deux liens. Les préfixes de sous-réseau sont dérivés du préfixe 6to4 de site 2002 : ac1f : 2aef ::/48 :

**IPv6 RTU 2002 : ac1f : 2aef : 1 ::/64 3 pub Life 1800**

**IPv6 RTU 2002 : ac1f : 2aef : 2 ::/64 4 pub Life 1800**

La commande **IPv6 RTU** spécifie que le préfixe 2002 : ac1f : 2aef : 1 ::/64 est sur liaison avec l’interface \# 3. Il configure le premier préfixe de sous-réseau sur l’interface Ethernet. L’itinéraire est publié avec une durée de vie de 30 minutes.

De même, le préfixe 2002 : ac1f : 2aef : 2 ::/64 est configuré sur l’interface 6-sur-4.

Les trois commandes suivantes permettent à l’ordinateur de passerelle 6to4 de fonctionner en tant que routeur :

**FORW IPv6 IFC 2**

**IPv6 IFC 3 FORW ADV**

**IFC IPv6 FORW ADV**

La commande **IPv6 IFC** contrôle les attributs d’une interface. Un routeur transfère les paquets et envoie les annonces de routeur. Dans l’implémentation Microsoft IPv6, ces attributs par interface sont contrôlés séparément.

L’interface \# 2 n’est pas nécessaire pour la publication, car il s’agit d’une pseudo-interface.

Si votre ordinateur possède des interfaces supplémentaires, celles-ci doivent également être configurées pour le transfert et la publication.

Après l’exécution de ces commandes, le protocole IPv6 de Microsoft configure automatiquement les adresses sur \# les interfaces 3 et \# 4 à l’aide des préfixes de sous-réseau respectifs et les deux interfaces commencent à envoyer des publications de routeur entre 3 et 10 minutes environ.

Les hôtes recevant ces annonces de routeur se configurent automatiquement avec un itinéraire par défaut et une adresse 6to4 dérivée du préfixe de sous-réseau de leur lien. Ils auront une communication avec d’autres sites 6to4 et le 6bone via l’ordinateur passerelle.

## <a name="debugging-6to4-configuration"></a>Débogage de la configuration 6to4

**Pour déboguer votre configuration 6to4**

1.  Vérifiez votre connectivité IPv4 au routeur relais 6to4 :

    **ping 6to4.ipv6.microsoft.com**

    En cas d’échec, vous ne disposez pas d’une connectivité Internet globale.

2.  Vérifiez l’encapsulation IPv6 à l’aide du tunneling automatique :

    **ping6 :: 131.107.152.32**

    En cas d’échec, vous pouvez avoir un pare-feu ou un traducteur d’adresses réseau (NAT) entre votre ordinateur et Internet. Si cette opération réussit, votre connexion Internet peut prendre en charge 6to4.

3.  Vérifiez l’affichage de la commande IPv6 RT. Un itinéraire 2002 ::/16-> 2 doit s’afficher. Vérifiez l’affichage de la commande IPv6 si 2. Vous devez voir une adresse par défaut avec un préfixe 2002 ::/16.

> [!Note]  
> L’adresse IPv4 du routeur de relais Microsoft 6to4 de 131.107.152.32 est susceptible d’être modifiée. Si l’étape 2 ci-dessus ne fonctionne pas, vérifiez la sortie de la commande ping à l’étape 1 pour vérifier l’adresse IPv4 du routeur Microsoft 6to4 Relay.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configurations recommandées pour IPv6](recommended-configurations-2.md)
</dt> <dt>

[Sous-réseau unique avec adresses lien-local](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Utilisation d’IPsec entre deux hôtes de liaison locale](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



