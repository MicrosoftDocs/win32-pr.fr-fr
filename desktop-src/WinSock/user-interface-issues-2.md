---
description: L’une des modifications les plus évidentes de IPv4 à IPv6 est la taille de l’adresse IP. De nombreuses interfaces utilisateur fournissent des boîtes de dialogue qui permettent à un utilisateur d’entrer une adresse IP, comme illustré dans la figure suivante.
ms.assetid: e2d7fd41-297a-400b-ae59-5d67db2be6f6
title: Problèmes d’interface utilisateur pour les applications Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03305073687cdd77e17c529d70ffe5959df40960
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296623"
---
# <a name="user-interface-issues-for-ipv6-winsock-applications"></a>Problèmes d’interface utilisateur pour les applications Winsock IPv6

L’une des modifications les plus évidentes de IPv4 à IPv6 est la taille de l’adresse IP. De nombreuses interfaces utilisateur fournissent des boîtes de dialogue qui permettent à un utilisateur d’entrer une adresse IP, comme illustré dans la figure suivante.

![zone d’adresse IPv4 commune dans une interface utilisateur](images/portingguide001.jpg)

L’adressage dans IPv6, en raison de nombreux facteurs tels que la longueur, la complexité et l’importance des sections au sein de l’espace d’adressage IPv6, n’est pas propice à la modification ou à la spécification par les utilisateurs. Par conséquent, le besoin de fournir aux utilisateurs la possibilité de spécifier leur propre adresse est réduit. En outre, en raison de la complexité associée à l’adressage IPv6, fournir aux administrateurs la possibilité de spécifier les informations d’adresse IPv6 n’est pas susceptible de se produire en fonction du nœud.

L’affichage d’une adresse IPv6 dans l’interface utilisateur n’est pas inconcevable et, par conséquent, les développeurs doivent prendre en compte la variabilité de la taille d’une adresse IPv6 lors de la modification d’une application pour prendre en charge IPv6.

Le reste de cette section traite de la différence entre la prévisibilité des longueurs d’adresses IPv4 et les considérations relatives à la longueur des adresses IPv6. Cette section suppose que les adresses IPv6 sont affichées dans leur représentation hexadécimale.

La taille des adresses IPv4 est prévisible, car elles suivent de manière rigide la notation décimale séparée par des points, comme l’illustre l’exemple d’adresse suivant :

``` syntax
10.10.256.1
```

Les adresses IPv6 ne sont pas aussi prévisibles, en raison de la Convention d’adresse IPv6 qui permet l’utilisation d’un double deux-points ( ::) pour représenter une série de zéros. Par conséquent, les représentations d’adresses IPv6 suivantes correspondent à la même adresse IPv6 :

``` syntax
1040:0:0:0:0:0:0:1
1040::1
```

La capacité à représenter une série de zéros avec un double deux-points se traduit par une longueur imprévisible pour un IPv6 donné, ce qui oblige les programmeurs à prendre en compte cette fonctionnalité lors de la création d’affichages d’interfaces IPv6. Certes, les développeurs doivent s’assurer que l’interface utilisateur est capable d’afficher des adresses IP qui n’utilisent pas de deux-points pour représenter une série de zéros (première adresse ci-dessous), ainsi que de pouvoir afficher l’adresse IPv6 la plus longue possible (deuxième adresse ci-dessous, avec l’adresse IPv4 incorporée) lors de la création de leur interface utilisateur compatible IPv6. Notez également que l’ajout de l’identificateur d’étendue (ID) à l’adresse suivante augmentera sa longueur de plus de onze caractères :

``` syntax
21DA:00D3:0010:2F3B:02AA:00FF:FE28:9C5A
0000:0000:0000:0000:0000:ffff:123.123.123.123
```

Il est également important de savoir si les adresses basées sur le nom sont plus appropriées que les adresses IPv6 basées sur des nombres. Si les adresses basées sur le nom sont plus appropriées, il convient de tenir compte des conventions d’affectation des noms dans l’interface utilisateur, y compris toute vérification des erreurs d’entrée appropriée pour la tâche.

Il existe d’autres complexités associées à l’affichage des adresses IPv6 que les développeurs doivent prendre en compte lors de la modification de leur application, et lors de la conception des représentations d’interface utilisateur des adresses IPv6. Voici quelques-unes de ces considérations :

-   L’adresse doit-elle contenir toutes les séquences de zéros ou utiliser la notation à deux-points ?
-   Est-il plus approprié d’utiliser une représentation d’adresse basée sur des nombres ou une représentation basée sur un nom ?
-   L’utilisateur s’intéresse-t-il à un certain aspect du schéma d’adressage, tel que le préfixe de sous-réseau, l’identificateur de portée ou d’autres sous-champs ?
-   L’utilisateur souhaite-t-il déterminer d’autres aspects de l’adresse, tels que l’identificateur TLA, l’identificateur NLA ou l’identificateur du contrat SLA ?
-   Votre interface utilisateur sera-t-elle en mesure de discerner les adresses IPv6 incorporées et, le cas échéant, comment seront-elles gérées et affichées ? Allez-vous discerner les adresses compatibles IPv4 et les adresses IPv6 mappées IPv4 lors de l’affichage des informations d’adresse à l’utilisateur ?

Il y a également d’autres considérations et les développeurs doivent prendre en compte soigneusement leurs clients lors du développement d’interfaces utilisateur d’adresse IP.

Bonnes pratiques

-   Les développeurs doivent prendre en compte l’approche appropriée pour chaque interface utilisateur lors de la modification de leur application pour prendre en charge IPv6. S’assurer que l’interface utilisateur contient suffisamment de longueur pour afficher les adresses IPv6 est impérative, tout comme détermine si cette adresse est basée sur un nombre ou un nom.
-   Dans la mesure du possible, utilisez les fonctions d’assistance Winsock et IP existantes lors de l’utilisation d’adresses IPv6 au lieu de réimplémenter cette logique. Par exemple, les fonctions [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa), [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw), [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)et [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) peuvent être utilisées pour effectuer une conversion entre des adresses IPv6 et des représentations sous forme de chaîne de ces adresses IPv6.

Code pour éviter

-   Les éléments d’interface utilisateur qui dépendent d’une adresse de taille IPv4 doivent être examinés et une partie de cette vérification doit inclure si les informations que vous fournissez (sous IPv4) sont appropriées pour IPv6.
-   La possibilité de spécifier une adresse IP doit également dépendre de l’utilisation de IPv4 ou D’ipv6. Si IPv6 est disponible, est-il approprié de spécifier des adresses (hexadécimales) basées sur des nombres ou des adresses basées sur des noms ?

Tâches de codage

**Pour réviser votre base de code existante de IPv4 à IPv4 et IPv6-interopérabilité**

1.  Effectuer un examen visuel de l’interface utilisateur, en recherchant tout élément qui dépend d’une longueur spécifique pour la chaîne d’adresse IP. Les contrôles avec la notation décimale à quatre sections facilement identifiée sont faciles à repérer, contrairement à d’autres. Il peut y avoir des endroits où des adresses IP peuvent être affichées, par exemple dans des boîtes de dialogue, dans lesquelles une adresse IPv6 peut manquer d’espace d’affichage.
2.  Lors de la recherche de l’un de ces contrôles, examinez s’il est approprié d’afficher l’adresse lors de l’utilisation du protocole IPv6. S’il est possible que IPv4 ou IPv6 soit en cours d’utilisation, assurez-vous que l’interface utilisateur peut prendre en charge l’une ou l’autre. Remplacez ou augmentez tous les contrôles avec des contrôles d’interface utilisateur qui peuvent afficher une adresse IPv6 entière.
3.  Suivi du test de l’interface utilisateur pour vérifier que les modifications qui activent l’affichage de l’adresse IPv6 maintiennent la convivialité prévue lors de l’utilisation d’adresses IPv4. Testez également les emplacements d’affichage des adresses de protocole, tels que les boîtes de dialogue d’information, pour vous assurer qu’ils gèrent correctement les adresses IPv6.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide IPv6 pour les Applications Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modification des structures de données pour IPv6 Winsock appications](changing-data-structures-2.md)
</dt> <dt>

[Sockets à double pile pour les applications Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Appels de fonction pour les applications Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Utilisation d’adresses IPv4 codées en dur](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Protocoles sous-jacents pour les applications Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
