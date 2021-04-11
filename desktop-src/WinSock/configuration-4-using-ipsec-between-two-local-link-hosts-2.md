---
description: Cette configuration crée une association de sécurité IPsec entre deux hôtes sur le même sous-réseau pour effectuer l’authentification à l’aide de l’en-tête d’authentification (AH) et de l’algorithme de hachage MD5 (Message Digest 5).
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 'Configuration 3 : utilisation d’IPsec entre deux hôtes de liaison locale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994e7a760b6ae1ba87678d6061881e5eb80faf88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113099"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a>Configuration 3 : utilisation d’IPsec entre deux hôtes de liaison locale

Cette configuration crée une association de sécurité IPsec entre deux hôtes sur le même sous-réseau pour effectuer l’authentification à l’aide de l’en-tête d’authentification (AH) et de l’algorithme de hachage MD5 (Message Digest 5). Dans cet exemple, la configuration affichée sécurise tout le trafic entre deux hôtes voisins : l’hôte 1, avec l’adresse lien-local FE80 :: 2AA : FF : FE53 : A92C et l’hôte 2, avec l’adresse lien-local FE80 :: 2AA : FF : FE92 : D0F1.

**Pour utiliser IPsec entre deux hôtes de liaison locale**

1.  Sur l’ordinateur hôte 1, créez des fichiers d’association de sécurité (SAD) et de stratégie de sécurité (SPD) vides à l’aide de la commande Ipsec6 c. Dans cet exemple, la commande Ipsec6.exe est ipsec6 c test. Cela crée deux fichiers pour configurer manuellement les associations de sécurité (test. Sad) et les stratégies de sécurité (test. SPD).
2.  Sur l’ordinateur hôte 1, modifiez le fichier SPD pour ajouter une stratégie de sécurité qui sécurise tout le trafic entre l’hôte 1 et l’ordinateur hôte 2.

    Le tableau suivant montre la stratégie de sécurité ajoutée au fichier test. SPD avant la première entrée pour cet exemple (la première entrée dans le fichier test. SPD n’a pas été modifiée).

    | Nom du champ du fichier SPD | Valeur d'exemple              |
    |---------------------|----------------------------|
    | **Stratégie**          | 2                          |
    | **RemoteIPAddr**    | **FE80 :: 2AA : FF : FE92 : D0F1** |
    | **LocalIPAddr**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protocole**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **AB**                     |
    | **IPSecMode**       | **TRANSPORT**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Sens**       | **Bidirect**               |
    | **Action**          | **APPLIQU**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Placez un point-virgule à la fin de la ligne configuration de cette stratégie de sécurité. Les entrées de stratégie doivent être placées dans un ordre numérique décroissant.

3.  Sur l’ordinateur hôte 1, modifiez le fichier SAD, en ajoutant les entrées SA pour sécuriser tout le trafic entre l’hôte 1 et l’ordinateur hôte 2. Deux associations de sécurité doivent être créées, une pour le trafic vers l’hôte 2 et l’autre pour le trafic à partir de l’hôte 2.

    Le tableau suivant montre la première entrée SA ajoutée au fichier test. sad pour cet exemple (pour le trafic vers l’hôte 2).

    | Nom du champ du fichier SAD | Valeur d'exemple              |
    |---------------------|----------------------------|
    | **Saentry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80 :: 2AA : FF : FE92 : D0F1** |
    | **DestIPAddr**      | **STRATÉGIE**                 |
    | **SrcIPAddr**       | **STRATÉGIE**                 |
    | **Protocole**        | **STRATÉGIE**                 |
    | **DestPort**        | **STRATÉGIE**                 |
    | **SrcPort**         | **STRATÉGIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. Key**               |
    | **Sens**       | **SORTANT**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Placez un point-virgule à la fin de la ligne configuration de cette SA.

    Le tableau suivant montre la seconde entrée d’association de contrôle ajoutée au fichier test. sad pour cet exemple (pour le trafic à partir de l’hôte 2).

    | Nom du champ du fichier SAD | Valeur d'exemple              |
    |---------------------|----------------------------|
    | **Saentry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80 :: 2AA : FF : FE53 : A92C** |
    | **DestIPAddr**      | **STRATÉGIE**                 |
    | **SrcIPAddr**       | **STRATÉGIE**                 |
    | **Protocole**        | **STRATÉGIE**                 |
    | **DestPort**        | **STRATÉGIE**                 |
    | **SrcPort**         | **STRATÉGIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. Key**               |
    | **Sens**       | **ENTRANT**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Placez un point-virgule à la fin de la ligne configuration de cette SA. Les entrées SA doivent être placées dans un ordre numérique décroissant.

4.  Sur l’ordinateur hôte 1, créez un fichier texte qui contient une chaîne de texte utilisée pour authentifier la signature d’accès partagé créée avec l’hôte 2. Dans cet exemple, le fichier test. Key est créé avec le contenu « This is a test ». Vous devez inclure des guillemets doubles autour de la chaîne de clé afin que la clé soit lue par l’outil Ipsec6.

    La version préliminaire de la technologie Microsoft IPv6 prend uniquement en charge les clés configurées manuellement pour l’authentification des associations de sécurité IPsec. Les clés manuelles sont configurées en créant des fichiers texte qui contiennent la chaîne de texte de la touche manuelle. Dans cet exemple, la même clé pour la signature d’accès partagé est utilisée dans les deux directions. Vous pouvez utiliser différentes clés pour la signature d’accès partagé entrante et sortante en créant des fichiers de clé différents et en les référençant avec le champ KeyFile dans le fichier SAD.

5.  Sur l’ordinateur hôte 2, créez des fichiers d’association de sécurité (SAD) et de stratégie de sécurité (SPD) vides à l’aide de la commande Ipsec6 c. Dans cet exemple, la commande Ipsec6.exe est ipsec6 c test. Cela crée deux fichiers avec des entrées vides pour la configuration manuelle des associations de sécurité (test. Sad) et des stratégies de sécurité (test. SPD).

    Pour simplifier l’exemple, les mêmes noms de fichiers pour les fichiers SAD et SPD sont utilisés sur l’hôte 2. Vous pouvez choisir d’utiliser des noms de fichiers différents sur chaque ordinateur hôte.

6.  Sur l’ordinateur hôte 2, modifiez le fichier SPD pour ajouter une stratégie de sécurité qui sécurise tout le trafic entre l’hôte 2 et l’ordinateur hôte 1.

    Le tableau suivant indique l’entrée de stratégie de sécurité ajoutée avant la première entrée au fichier test. SPD pour cet exemple (la première entrée dans le fichier test. SPD n’a pas été modifiée).

    | Nom du champ du fichier SPD | Valeur d'exemple              |
    |---------------------|----------------------------|
    | **Stratégie**          | 2                          |
    | **RemoteIPAddr**    | **FE80 :: 2AA : FF : FE53 : A92C** |
    | **LocalIPAddr**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protocole**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **AB**                     |
    | **IPSecMode**       | **TRANSPORT**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Sens**       | **Bidirect**               |
    | **Action**          | **APPLIQU**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Placez un point-virgule à la fin de la ligne configuration de cette stratégie de sécurité. Les entrées de stratégie doivent être placées dans un ordre numérique décroissant.

7.  Sur l’hôte 2, modifiez le fichier SAD, en ajoutant les entrées SA pour sécuriser tout le trafic entre l’hôte 2 et l’ordinateur hôte 1. Deux associations de sécurité doivent être créées : une pour le trafic vers l’hôte 1 et l’autre pour le trafic à partir de l’hôte 1.

    Le tableau suivant indique la première association de contrôle d’accès (SA) ajoutée au fichier test. sad pour cet exemple (pour le trafic provenant de l’hôte 1).

    | Nom du champ du fichier SAD | Valeur d'exemple              |
    |---------------------|----------------------------|
    | **Saentry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80 :: 2AA : FF : FE92 : D0F1** |
    | **DestIPAddr**      | **STRATÉGIE**                 |
    | **SrcIPAddr**       | **STRATÉGIE**                 |
    | **Protocole**        | **STRATÉGIE**                 |
    | **DestPort**        | **STRATÉGIE**                 |
    | **SrcPort**         | **STRATÉGIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. Key**               |
    | **Sens**       | **ENTRANT**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Placez un point-virgule à la fin de la ligne configuration de cette SA.

    Le tableau suivant montre la seconde entrée d’association de contrôle ajoutée au fichier test. sad pour cet exemple (pour le trafic vers l’hôte 1).

    | Nom du champ du fichier SAD | Valeur d'exemple              |
    |---------------------|----------------------------|
    | **Saentry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80 :: 2AA : FF : FE53 : A92C** |
    | **DestIPAddr**      | **STRATÉGIE**                 |
    | **SrcIPAddr**       | **STRATÉGIE**                 |
    | **Protocole**        | **STRATÉGIE**                 |
    | **DestPort**        | **STRATÉGIE**                 |
    | **SrcPort**         | **STRATÉGIE**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. Key**               |
    | **Sens**       | **SORTANT**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Placez un point-virgule à la fin de la ligne configuration de cette SA. Les entrées SA doivent être placées dans un ordre numérique décroissant.

8.  Sur l’hôte 2, créez un fichier texte qui contient une chaîne de texte utilisée pour authentifier la SAP créée avec l’hôte 1. Dans cet exemple, le fichier test. Key est créé avec le contenu « This is a test ». Vous devez inclure des guillemets doubles autour de la chaîne de clé afin que la clé soit lue par l’outil Ipsec6.
9.  Sur l’ordinateur hôte 1, ajoutez les stratégies de sécurité et les associations de sécurité configurées à partir des fichiers SPD et SAD à l’aide de la commande Ipsec6 a. Dans cet exemple, la commande Ipsec6 a test est exécutée sur l’hôte 1.
10. Sur l’ordinateur hôte 2, ajoutez les stratégies de sécurité et les associations de sécurité configurées à partir des fichiers SPD et SAD à l’aide de la commande Ipsec6 a. Dans cet exemple, la commande Ipsec6 a test est exécutée sur l’hôte 2.
11. Exécutez une commande ping sur l’hôte 1 à partir de l’hôte 2 avec la commande ping6.

    Si vous capturez le trafic à l’aide d’Moniteur réseau Microsoft ou d’un autre renifleur de paquets, vous devez voir l’échange des messages de demande d’écho et de réponse à écho ICMPv6 avec un en-tête d’authentification entre l’en-tête IPv6 et l’en-tête ICMPv6.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configurations recommandées pour IPv6](recommended-configurations-2.md)
</dt> <dt>

[Sous-réseau unique avec adresses lien-local](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Trafic IPv6 entre les nœuds de différents sous-réseaux d’un interréseau IPv4 (6to4)](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



