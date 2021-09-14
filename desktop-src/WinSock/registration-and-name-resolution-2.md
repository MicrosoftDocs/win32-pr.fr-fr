---
description: Windows Sockets 2 est un ensemble de fonctions qui standardise la façon dont les applications accèdent et utilisent les différents services d’attribution de noms de réseau.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Inscription et résolution de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915839"
---
# <a name="registration-and-name-resolution"></a>Inscription et résolution de noms

Windows Sockets 2 est un ensemble de fonctions qui standardise la façon dont les applications accèdent et utilisent les différents services d’attribution de noms de réseau. Lors de l’utilisation de ces fonctions, les applications n’ont pas besoin de distinguer les protocoles les plus différents associés aux services de noms tels que DNS, NIS, X. 500, SAP, etc. pour assurer la compatibilité descendante totale avec les sockets de Windows 1,1, les fonctions de recherche de base de données **getXbyY** et **WSAAsyncGetXbyY** asynchrone existantes continuent d’être prises en charge, mais elles sont implémentées dans l’interface du fournisseur de services de sockets de Windows en termes de nouvelles capacités de résolution de noms. Pour plus d’informations, consultez les fonctions [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) et [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) . consultez également [la résolution de noms Compatible pour TCP/IP dans le SPI Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).

Cette section décrit les fonctionnalités d’inscription et de résolution de noms disponibles pour les développeurs Winsock. La liste suivante décrit les rubriques de cette section :

-   [Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)
-   [résolution de noms Compatible pour TCP/IP dans l’API Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Winsock](about-winsock.md)
</dt> <dt>

[Utilisation de Winsock](using-winsock.md)
</dt> </dl>

 

 



