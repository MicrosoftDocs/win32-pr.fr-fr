---
description: Le développement d’une infrastructure réseau de haut niveau sécurisée est une priorité pour la plupart des développeurs d’applications réseau. Toutefois, la sécurité de socket est souvent négligée en étant très importante lorsque vous envisagez une solution entièrement sécurisée.
ms.assetid: b37a3e33-65ee-43b1-bc8b-3280db7ebee4
title: Utilisation de SO_REUSEADDR et SO_EXCLUSIVEADDRUSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d58b0249ab19b4c7a1655a1c65130d545d328ef4fba3fd56ae9b05a911cb3fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121143"
---
# <a name="using-so_reuseaddr-and-so_exclusiveaddruse"></a>Utilisation \_ de so REUSEADDR et so \_ EXCLUSIVEADDRUSE

Le développement d’une infrastructure réseau de haut niveau sécurisée est une priorité pour la plupart des développeurs d’applications réseau. Toutefois, la sécurité de socket est souvent négligée en étant très importante lorsque vous envisagez une solution entièrement sécurisée. La sécurité des sockets, en particulier, concerne les processus qui se lient au même port précédemment lié par un autre processus d’application. Dans le passé, il était possible pour une application réseau de « détourner » le port d’une autre application, ce qui pourrait facilement entraîner une attaque par déni de service ou un vol de données.

En général, la sécurité de socket s’applique aux processus côté serveur. Plus précisément, la sécurité de socket s’applique à toute application réseau qui accepte les connexions et reçoit le trafic de datagramme IP. Ces applications sont généralement liées à un port bien connu et sont des cibles communes pour le code réseau malveillant.

Les applications clientes sont moins susceptibles d’être les cibles de telles attaques, pas parce qu’elles sont moins vulnérables, mais parce que la plupart des clients se lient aux ports locaux « éphémères » plutôt qu’aux ports de « service » statiques. Les applications réseau clientes doivent toujours être liées à des ports éphémères (en spécifiant le port 0 dans la structure [**sockaddr**](sockaddr-2.md) désignée par le paramètre *Name* lors de l’appel de la fonction [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) ), à moins qu’il y ait une raison architecturale impérieuse de ne pas le faire. Les ports locaux éphémères sont constitués de ports supérieurs au port 49151. La plupart des applications serveur pour les services dédiés sont liées à un port réservé bien connu qui est inférieur ou égal au port 49151. Ainsi, pour la plupart des applications, il n’y a généralement pas de conflit entre les demandes de liaison entre les applications clientes et serveur.

cette section décrit le niveau de sécurité par défaut sur les différentes plates-formes de Windows Microsoft et la façon dont les options de socket spécifiques **, \_ REUSEADDR** et [ \_ EXCLUSIVEADDRUSE](so-exclusiveaddruse.md) , influencent et affectent la sécurité des applications réseau. une fonctionnalité supplémentaire appelée sécurité de socket améliorée est disponible sur Windows Server 2003 et versions ultérieures. La disponibilité de ces options de socket et de la sécurité de socket améliorée varie selon les versions des systèmes d’exploitation Microsoft, comme indiqué dans le tableau ci-dessous.

| Plateforme            | \_REUSEADDR | \_EXCLUSIVEADDRUSE                  | Sécurité de socket améliorée |
|---------------------|---------------|---------------------------------------|--------------------------|
| Windows 95          | Disponible     | Non disponible                         | Non disponible            |
| Windows 98          | Disponible     | Non disponible                         | Non disponible            |
| Windows J'          | Disponible     | Non disponible                         | Non disponible            |
| Windows NT 4.0      | Disponible     | Disponible dans le Service Pack 4 et versions ultérieures | Non disponible            |
| Windows 2000        | Disponible     | Disponible                             | Non disponible            |
| Windows XP          | Disponible     | Disponible                             | Non disponible            |
| Windows Server 2003 | Disponible     | Disponible                             | Disponible                |
| Windows Vista       | Disponible     | Disponible                             | Disponible                |
| Windows Server 2008 | Disponible     | Disponible                             | Disponible                |
| Windows 7and plus récent  | Disponible     | Disponible                             | Disponible                |

## <a name="using-so_reuseaddr"></a>Utilisation de SO \_ REUSEADDR

L’option de socket **\_ REUSEADDR** permet à un socket de se lier de force à un port utilisé par un autre Socket. Le deuxième Socket appelle [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) avec le paramètre *Nom_option* défini sur **so \_ REUSEADDR** et le paramètre *optval* défini sur une valeur booléenne **true** avant d’appeler [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) sur le même port que le socket d’origine. Une fois le deuxième Socket lié avec succès, le comportement de tous les sockets liés à ce port est indéterminé. Par exemple, si tous les sockets sur le même port fournissent le service TCP, toute demande de connexion TCP entrante sur le port ne peut pas être garantie par le socket approprié ; le comportement est non déterministe. Un programme malveillant peut utiliser par **conséquent \_ REUSEADDR** pour lier de force les sockets déjà utilisés pour les services de protocole réseau standard afin de refuser l’accès à ces services. Aucun privilège spécial n’est requis pour utiliser cette option.

Si une application cliente est liée à un port avant qu’une application serveur puisse se lier au même port, des problèmes peuvent se produire. Si l’application serveur est liée de force à l’aide de l’option de socket **\_ REUSEADDR** sur le même port, le comportement de tous les sockets liés à ce port est indéterminé.

L’exception à ce comportement non déterministe est Sockets multidiffusion. Si deux sockets sont liés à la même interface et au même port et sont membres du même groupe de multidiffusion, les données sont remises aux deux sockets, plutôt qu’à un choix arbitraire.

## <a name="using-so_exclusiveaddruse"></a>Utilisation de SO \_ EXCLUSIVEADDRUSE

Avant l’introduction de l’option de socket **\_ EXCLUSIVEADDRUSE** , il était très peu important pour un développeur d’applications réseau d’empêcher un programme malveillant de se lier au port sur lequel l’application réseau avait ses propres Sockets liés. pour résoudre ce problème de sécurité, Windows sockets a introduit l’option de socket **\_ EXCLUSIVEADDRUSE** , qui est devenue disponible sur Windows NT 4,0 avec Service Pack 4 (SP4) et versions ultérieures.

l’option de socket **\_ EXCLUSIVEADDRUSE** ne peut être utilisée que par les membres du groupe de sécurité administrateurs sur Windows XP et les versions antérieures. les raisons pour lesquelles cette spécification a été modifiée sur Windows Server 2003 et versions ultérieures sont décrites plus loin dans cet article.

L' **option \_ so EXCLUSIVEADDRUSE** est définie en appelant la fonction [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) avec le paramètre *nom_option* défini sur **so \_ EXCLUSIVEADDRUSE** et le paramètre *optval* défini sur une valeur booléenne **true** avant la liaison du Socket. Une fois l’option définie, le comportement des appels de [**liaison**](/windows/win32/api/winsock/nf-winsock-bind) suivants diffère selon l’adresse réseau spécifiée dans chaque appel de **liaison** .

le tableau ci-dessous décrit le comportement qui se produit dans Windows XP et les versions antérieures lorsqu’un deuxième socket tente de se lier à une adresse précédemment liée par un premier socket à l’aide d’options de socket spécifiques.

> [!NOTE]  
> Dans le tableau ci-dessous, « caractère générique » désigne l’adresse générique du protocole donné (par exemple, « 0.0.0.0 » pour IPv4 et «  :: » pour IPv6). « Spécifique » indique qu’une adresse IP spécifique a été attribuée à une interface. Les cellules de tableau indiquent si la liaison est réussie (« Success ») ou si une erreur est retournée (« INUSE » pour l’erreur [WSAEADDRINUSE](windows-sockets-error-codes-2.md) ; « ACCÈS » pour l’erreur [WSAEACCES](windows-sockets-error-codes-2.md) ).

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Premier appel de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>liaison</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Deuxième appel de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>liaison</strong></a></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Default</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td bgcolor="#C0C0C0">Spécifique</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Default</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
        <td>Opération réussie</td>
        <td>Opération réussie</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
        <td>Opération réussie</td>
        <td>Opération réussie</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
        <td>Opération réussie</td>
        <td>Opération réussie</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
        <td>Opération réussie</td>
        <td>Opération réussie</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
</table>

Lorsque deux sockets sont liés au même numéro de port mais sur des interfaces explicites différentes, il n’y a aucun conflit. Par exemple, dans le cas où un ordinateur a deux interfaces IP, 10.0.0.1 et 10.99.99.99, si le premier appel à [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) est sur 10.0.0.1 avec le port défini sur 5150 et **\_ EXCLUSIVEADDRUSE** spécifié, un deuxième appel à **Bind** sur 10.99.99.99 avec le port est également défini sur 5150 et aucune option spécifiée n’est établie. Toutefois, si le premier Socket est lié à l’adresse générique et au port 5150, tout appel de liaison suivant au port 5150 **avec \_ EXCLUSIVEADDRUSE** défini échoue avec [WSAEADDRINUSE](windows-sockets-error-codes-2.md) ou [WSAEACCES](windows-sockets-error-codes-2.md) retourné par l’opération de **liaison** .

Dans le cas où le premier appel à [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) définit soit **\_ REUSEADDR** , soit aucune option de socket, le deuxième appel de **liaison** « pirate » le port et l’application ne peut pas déterminer lequel des deux sockets ont reçu des paquets spécifiques envoyés au port « partagé ».

Une application classique qui appelle la fonction de [**liaison**](/windows/win32/api/winsock/nf-winsock-bind) n’alloue pas le socket lié pour une utilisation exclusive, à moins que l’option de socket **so \_ EXCLUSIVEADDRUSE** soit appelée sur le socket avant l’appel à la fonction de **liaison** . Si une application cliente est liée à un port éphémère ou à un port spécifique avant qu’une application serveur ne se connecte au même port, des problèmes peuvent se produire. L’application serveur peut être liée de force au même port à l’aide de l’option de socket **so \_ REUSEADDR** sur le socket avant d’appeler la fonction **Bind** , mais le comportement de tous les sockets liés à ce port est alors indéterminé. Si l’application serveur tente d’utiliser l’option de socket **so \_ EXCLUSIVEADDRUSE** pour l’utilisation exclusive du port, la demande échoue.

À l’inverse, un socket avec l' **ensemble \_ EXCLUSIVEADDRUSE, qui** ne peut pas être réutilisé immédiatement après la fermeture du Socket. Par exemple, si un socket d’écoute **avec \_ EXCLUSIVEADDRUSE** défini accepte une connexion et est ensuite fermé, un autre socket (également avec **\_ EXCLUSIVEADDRUSE**) ne peut pas se lier au même port que le premier Socket jusqu’à ce que la connexion d’origine devienne inactive.

Ce problème peut devenir compliqué, car le protocole de transport sous-jacent peut ne pas mettre fin à la connexion même si le socket a été fermé. Même après la fermeture du socket par l’application, le système doit transmettre toutes les données mises en mémoire tampon, envoyer un message de déconnexion approprié à l’homologue et attendre un message de déconnexion approprié de l’homologue. Il est possible que le protocole de transport sous-jacent ne libère jamais la connexion ; par exemple, l’homologue participant à la connexion d’origine peut annoncer une fenêtre de taille nulle ou une autre forme de configuration « attaque ». Dans ce cas, la connexion client reste dans un état actif malgré la demande de la fermer, car les données non acquittées restent dans la mémoire tampon.

Pour éviter cette situation, les applications réseau doivent garantir un arrêt correct en appelant [**Shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) avec l' \_ indicateur SD Send défini, puis attendre dans une boucle [**recv**](/windows/win32/api/winsock/nf-winsock-recv) jusqu’à ce que zéro octet soit renvoyé sur la connexion. Cela garantit que toutes les données sont reçues par l’homologue et confirme de la même manière à l’homologue qu’il a reçu toutes les données transmises, ainsi qu’à éviter le problème de réutilisation des ports susmentionné.

L' \_ option de socket so peut être définie sur un socket pour empêcher le port de passer à un état d’attente « actif »; Toutefois, cela est déconseillé car il peut entraîner des effets souhaités, tels que la réinitialisation des connexions. Par exemple, si les données sont reçues par l’homologue mais qu’elles ne le sont pas, et que l’ordinateur local ferme le socket avec, si tel est le cas \_ , la connexion entre les deux ordinateurs est réinitialisée et les données sans accusé de réception sont ignorées par l’homologue. Il est difficile de choisir un délai d’attente approprié, car une valeur de délai d’expiration plus faible entraîne souvent des interruptions soudaines des connexions, alors que des valeurs de délai d’expiration plus élevées laissent le système vulnérable aux attaques par déni de service (en établissant de nombreuses connexions et en bloquant/bloquant les threads d’application). La fermeture d’un socket qui a une valeur de délai d’attente différente de zéro peut également provoquer le blocage de l’appel [**opération closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) .

## <a name="enhanced-socket-security"></a>Sécurité de socket améliorée

la sécurité de socket améliorée a été ajoutée avec la version de Windows Server 2003. Dans les versions précédentes du système d’exploitation de serveur Microsoft, la sécurité de socket par défaut permettait facilement de détourner les ports des applications insoupçonnées. dans Windows Server 2003, les sockets ne sont pas dans un état partageable par défaut. Par conséquent, si une application veut permettre à d’autres processus de réutiliser un port sur lequel un socket est déjà lié, elle doit l’activer spécifiquement. Si tel est le cas, le premier socket à appeler [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) sur le port doit avoir **\_ REUSEADDR** défini sur le Socket. La seule exception à ce cas se produit lorsque le deuxième appel de **liaison** est effectué par le même compte d’utilisateur qui a effectué l’appel d’origine à la **liaison**. Cette exception existe uniquement pour assurer la compatibilité descendante.

le tableau ci-dessous décrit le comportement qui se produit dans les systèmes d’exploitation Windows Server 2003 et versions ultérieures lorsqu’un deuxième socket tente de se lier à une adresse précédemment liée par un premier socket à l’aide d’options de socket spécifiques.

> [!NOTE]
> Dans le tableau ci-dessous, « caractère générique » désigne l’adresse générique du protocole donné (par exemple, « 0.0.0.0 » pour IPv4 et «  :: » pour IPv6). « Spécifique » indique qu’une adresse IP spécifique a été attribuée à une interface. Les cellules de tableau indiquent si la liaison est réussie (« Success ») ou si l’erreur retournée (« INUSE » pour l’erreur [WSAEADDRINUSE](windows-sockets-error-codes-2.md) ; « ACCÈS » pour l’erreur [WSAEACCES](windows-sockets-error-codes-2.md) ).
>
> Notez également que dans cette table spécifique, les deux appels de [**liaison**](/windows/win32/api/winsock/nf-winsock-bind) sont effectués sous le même compte d’utilisateur.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Premier appel de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>liaison</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Deuxième appel de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>liaison</strong></a></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Default</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td bgcolor="#C0C0C0">Spécifique</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Default</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td>UTILISÉES</td>
        <td>Succès</td>
        <td>ACCESS</td>
        <td>Succès</td>
        <td>UTILISÉES</td>
        <td>Succès</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td>Succès</td>
        <td>UTILISÉES</td>
        <td>Succès</td>
        <td>ACCESS</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td>UTILISÉES</td>
        <td>Opération réussie</td>
        <td>Opération réussie</td>
        <td>Opération réussie</td>
        <td>UTILISÉES</td>
        <td>Succès</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td>Succès</td>
        <td>UTILISÉES</td>
        <td>Opération réussie</td>
        <td>Opération réussie</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td>UTILISÉES</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>UTILISÉES</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td>Succès</td>
        <td>UTILISÉES</td>
        <td>Succès</td>
        <td>ACCESS</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
</table>

Quelques entrées du tableau ci-dessus méritent une explication.

Par exemple, si le premier appelant définit **\_ EXCLUSIVEADDRUSE** sur une adresse spécifique et que le deuxième appelant tente d’appeler [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) avec une adresse générique sur le même port, le deuxième appel de **liaison** sera effectué. Dans ce cas particulier, le deuxième appelant est lié à toutes les interfaces, à l’exception de l’adresse spécifique à laquelle le premier appelant est lié. Notez que l’inverse de ce cas de figure n’est pas vrai : si le premier appelant définit **so \_ EXCLUSIVEADDRUSE** et appelle **Bind** avec l’indicateur de caractère générique, le deuxième appelant n’est pas en mesure d’appeler **Bind** avec le même port.

Le comportement de liaison de socket change lorsque les appels de liaison de socket sont effectués sous des comptes d’utilisateur différents. le tableau ci-dessous spécifie le comportement qui se produit dans les systèmes d’exploitation Windows Server 2003 et versions ultérieures lorsqu’un deuxième socket tente de se lier à une adresse précédemment liée par un premier socket à l’aide d’options de socket spécifiques et d’un autre compte d’utilisateur.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Premier appel de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>liaison</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Deuxième appel de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>liaison</strong></a></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Default</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td bgcolor="#C0C0C0">Spécifique</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Default</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td>UTILISÉES</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>UTILISÉES</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td>Succès</td>
        <td>UTILISÉES</td>
        <td>Succès</td>
        <td>ACCESS</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td>UTILISÉES</td>
        <td>ACCESS</td>
        <td>Opération réussie</td>
        <td>Opération réussie</td>
        <td>UTILISÉES</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td>Succès</td>
        <td>UTILISÉES</td>
        <td>Opération réussie</td>
        <td>Opération réussie</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Caractère générique</td>
        <td>UTILISÉES</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>UTILISÉES</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Spécifique</td>
        <td>Succès</td>
        <td>UTILISÉES</td>
        <td>Succès</td>
        <td>ACCESS</td>
        <td>UTILISÉES</td>
        <td>UTILISÉES</td>
    </tr>
</table>

Notez que le comportement par défaut est différent lorsque les appels de [**liaison**](/windows/win32/api/winsock/nf-winsock-bind) sont effectués sous des comptes d’utilisateur différents. Si le premier appelant ne définit aucune option sur le socket et se lie à l’adresse générique, le deuxième appelant ne peut pas définir l’option **so \_ REUSEADDR** et effectuer une liaison avec le même port. Le comportement par défaut sans option Set retourne également une erreur.

sur Windows Vista et versions ultérieures, vous pouvez créer un socket à double pile qui fonctionne sur IPv6 et IPv4. Lorsqu’un socket à double pile est lié à l’adresse générique, le port donné est réservé sur les piles de mise en réseau IPv4 et IPv6 et les vérifications associées à **so \_ REUSEADDR** et **\_ EXCLUSIVEADDRUSE** (Si défini) sont effectuées. Ces vérifications doivent être exécutées sur les deux piles de mise en réseau. Par exemple, si un socket TCP à double pile **définit \_ EXCLUSIVEADDRUSE** , puis tente d’établir une liaison avec le port 5000, aucun autre socket TCP ne peut être précédemment lié au port 5000 (caractère générique ou spécifique). Dans ce cas, si un socket TCP IPv4 était précédemment lié à l’adresse de bouclage sur le port 5000, l’appel de [**liaison**](/windows/win32/api/winsock/nf-winsock-bind) pour le socket à double pile échouait avec [WSAEACCES](windows-sockets-error-codes-2.md).

## <a name="application-strategies"></a>Stratégies d’application

Lors du développement d’une application réseau qui fonctionne au niveau de la couche de sockets, il est important de prendre en compte le type de sécurité de socket nécessaire. Les applications clientes (applications qui connectent ou envoient des données à un service) requièrent rarement des étapes supplémentaires, car elles sont liées à un port local (éphémère) aléatoire. Si le client requiert une liaison de port local spécifique pour fonctionner correctement, vous devez prendre en compte la sécurité du Socket.

L’option **so \_ REUSEADDR** a très peu d’utilisations dans des applications normales, à l’exception des sockets multidiffusion, où les données sont remises à tous les sockets liés au même port. Dans le cas contraire, toute application qui définit cette option de socket doit être repensée pour supprimer la dépendance, car elle est de plus en plus vulnérable à « le piratage de Sockets ». Tant que l’option de socket **\_ REUSEADDR** peut être utilisée pour détourner potentiellement un port dans une application serveur, l’application doit être considérée comme non sécurisée.

Toutes les applications serveur doivent **définir \_ EXCLUSIVEADDRUSE** pour un niveau élevé de sécurité de Socket. Non seulement il empêche les logiciels malveillants de détourner le port, mais il indique également si une autre application est liée au port demandé. Par exemple, un appel à [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) sur l’adresse générique par un processus avec l’option de socket **\_ EXCLUSIVEADDRUSE** définie échoue si un autre processus est actuellement lié au même port sur une interface spécifique.

enfin, même si la sécurité de socket a été améliorée dans Windows Server 2003, une application doit toujours définir l’option **SO \_ EXCLUSIVEADDRUSE** socket pour s’assurer qu’elle est liée à toutes les interfaces spécifiques que le processus a demandé. la sécurité de socket dans Windows Server 2003 ajoute un niveau accru de sécurité pour les applications héritées, mais les développeurs d’applications doivent toujours concevoir leurs produits avec tous les aspects de la sécurité à l’esprit.
