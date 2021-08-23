---
description: Cette rubrique décrit des considérations de programmation spécifiques lors de l’utilisation de l’infrastructure homologue.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Considérations relatives à la programmation (peer-to-peer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d5af967503c216422e3a12572aeeaf91d751473f88d8589c2e125894721b41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518059"
---
# <a name="programming-considerations-peer-to-peer"></a>Considérations relatives à la programmation (peer-to-peer)

Cette rubrique décrit des considérations de programmation spécifiques lors de l’utilisation de l’infrastructure homologue.

Lorsque vous utilisez l’infrastructure homologue pour développer des applications homologues, vous devez prendre en compte les considérations de programmation suivantes :

-   IPv6

    L’infrastructure homologue requiert l’installation et le démarrage D’ipv6 pour permettre aux applications réseau homologues de fonctionner.

-   Ports du pare-feu

    Lorsqu’un pare-feu est utilisé sur un réseau (tel que le pare-feu de connexion Internet IPv6), des ports spécifiques doivent être ouverts pour permettre à l’infrastructure homologue de fonctionner. Les ports suivants doivent être ouverts :

    Port TCP 3587 pour l’infrastructure de regroupement de pairs.

    Port UDP 3540 pour l’infrastructure de représentation graphique des homologues.

    > [!Note]  
    > Les applications qui utilisent l’infrastructure de représentation graphique des pairs sur TCP choisissent leur propre port TCP lors de l’appel de [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Option de socket

    Lorsque vous tentez de vous connecter à d’autres nœuds homologues IPv6 directement (sans utiliser l’infrastructure homologue), assurez-vous que l’option \_ \_ de socket niveau de protection IPv6 est définie sur **niveau de protection non \_ \_ restreint**.

-   Bande passante

    Quand vous utilisez PNRP, une application peut publier un ou plusieurs [noms d’homologues](peer-names.md) qui peuvent être résolus. Pour chaque nom d’homologue inscrit avec PNRP, il y a une augmentation de la bande passante réseau utilisée par PNRP pour publier le nom de l’homologue et le maintenir à la disposition des autres nœuds.

    Pour empêcher l’utilisation d’une bande passante trop importante, les applications doivent éviter d’inscrire un grand nombre de noms d’homologues sur un ordinateur. Par exemple, une application qui publie des images ne doit pas créer de nom d’homologue pour chaque image, mais doit créer un nom d’homologue pour le service qui publie des images et utiliser un protocole différent pour les clients afin d’interroger le service à la recherche d’images spécifiques.

-   Inscription du nom d’homologue

    Certaines applications peuvent être nécessaires pour inscrire le même [nom d’homologue](peer-names.md) sur plusieurs ordinateurs. En général, cela se produit si un nom d’homologue est associé à une personne qui utilise plus d’un ordinateur. Une méthode que vous pouvez utiliser pour enregistrer le même nom d’homologue sur plusieurs ordinateurs consiste à créer un groupe homologue pour la personne et à se connecter à ce groupe à partir de tous les ordinateurs. Une autre méthode consiste à créer une identité d’homologue et un nom d’homologue sur un ordinateur, à exporter l’identité d’homologue à partir de cet ordinateur et à l’importer sur d’autres ordinateurs. Cela permet de créer le même nom d’homologue sécurisé sur tous les ordinateurs qui ont importé l’identité d’homologue.

 

 



