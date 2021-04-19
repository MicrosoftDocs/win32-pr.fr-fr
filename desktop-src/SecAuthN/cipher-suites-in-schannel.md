---
description: Une suite de chiffrement est un ensemble d’algorithmes de chiffrement.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Suites de chiffrement dans TLS/SSL (SSP Schannel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa8b47aed266c49ac306adfd2aef78af269a39
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106525812"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a>Suites de chiffrement dans TLS/SSL (SSP Schannel)

Une suite de chiffrement est un ensemble d’algorithmes de chiffrement. L’implémentation du SSP Schannel des protocoles TLS/SSL utilise des algorithmes d’une suite de chiffrement pour créer des clés et chiffrer les informations. Une suite de chiffrement spécifie un algorithme pour chacune des tâches suivantes :

-   Échange de clés
-   Chiffrement en bloc
-   Authentification de message

Les [*algorithmes d’échange de clés*](/windows/desktop/SecGloss/k-gly) protègent les informations requises pour créer des clés partagées. Ces algorithmes sont asymétriques ([*algorithmes de clé publique*](/windows/desktop/SecGloss/p-gly)) et fonctionnent bien pour des quantités de données relativement petites.

Les algorithmes de chiffrement en bloc chiffrent les messages échangés entre les clients et les serveurs. Ces algorithmes sont [*symétriques*](/windows/desktop/SecGloss/s-gly) et fonctionnent correctement pour de grandes quantités de données.

Les algorithmes [d’authentification de message](message-authentication-codes-in-schannel.md) génèrent des [*hachages*](/windows/desktop/SecGloss/h-gly) de message et des signatures qui garantissent l' [*intégrité*](/windows/desktop/SecGloss/i-gly) d’un message.

Les développeurs spécifient ces éléments à l’aide des types de données d' [**\_ ID ALG**](/windows/desktop/SecCrypto/alg-id) . Pour plus d’informations, consultez [spécification des chiffrements Schannel et des niveaux de chiffrement](specifying-schannel-ciphers-and-cipher-strengths.md).

Dans les versions antérieures de Windows, les suites de chiffrement TLS et les courbes elliptiques étaient configurées à l’aide d’une chaîne unique :

![Diagramme qui affiche une chaîne unique pour une suite de chiffrement.](images/tls-cipher-suite.png)

Les différentes versions de Windows prennent en charge différentes suites de chiffrement TLS et ordre de priorité. Consultez la version de Windows correspondante pour l’ordre par défaut dans lequel elles sont choisies par le fournisseur Microsoft Schannel.

**Windows Server 2022 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)

**Windows 10, version 1903 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)

**Windows 10, version 1809 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)

**Windows 10, version 1803 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)

**Windows 10, version 1709 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)

**Windows 10, version 1703 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)

**Windows Server 2016 et Windows 10, version 1607 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)

**Windows 10, version 1511 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 10 v1511 inclut](tls-cipher-suites-in-windows-10-v1511.md)

**Windows 10, version 1507 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 10 V1507](./tls-cipher-suites-in-windows-10--version-1507.md)

**Windows Server 2012 R2 et Windows 8.1 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 8.1](tls-cipher-suites-in-windows-8-1.md)

**Windows Server 2012 et Windows 8 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 8](tls-cipher-suites-in-windows-8.md)

**Windows Server 2008 R2 et Windows 7 :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows 7](tls-cipher-suites-in-windows-7.md)

**Windows Server 2008 et Windows Vista :** Pour plus d’informations sur les suites de chiffrement prises en charge, voir [suites de chiffrement TLS dans Windows Vista](schannel-cipher-suites-in-windows-vista.md)

**Windows Server 2003 et Windows XP :** Pour plus d’informations sur les suites de chiffrement prises en charge, consultez les rubriques suivantes.

| Rubrique                                                                         | Description                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Suites de chiffrement TLS](tls-cipher-suites.md)<br/>                         | Informations sur les suites de chiffrement disponibles avec le protocole TLS dans Windows Server 2003 et Windows XP.<br/>              |
| [Protocole SSL (Secure Sockets Layer)](secure-sockets-layer-protocol.md)<br/> | Informations générales sur les protocoles SSL 2,0 et 3,0, y compris les suites de chiffrement disponibles dans Windows Server 2003 et Windows XP.<br/> |



 

> [!Note]  
> Avant Windows 10, les chaînes de suite de chiffrement étaient ajoutées à la courbe elliptique pour déterminer la priorité de la courbe. Windows 10 prend en charge un paramètre d’ordre de priorité de courbe elliptique, ce qui signifie que le suffixe de courbe elliptique n’est pas obligatoire et est remplacé par le nouvel ordre de priorité de la courbe elliptique, le cas échéant, pour permettre aux organisations d’utiliser la stratégie de groupe pour configurer différentes versions de Windows avec les mêmes suites de chiffrement.

 

