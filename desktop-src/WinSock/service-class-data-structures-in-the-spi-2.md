---
description: Quand une nouvelle classe de service est installée, une structure WSASERVICECLASSINFO doit être préparée et fournie. Cette structure se compose également de sous-structures qui contiennent une série de paramètres qui s’appliquent à des espaces de noms spécifiques.
ms.assetid: fb225e0c-a0c7-44e1-80fb-7b924b371afa
title: Structures de données de classe de service dans SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53eb2fd61c5ec6295b65128048bc9fe477ae63f78f89bfba4be73798002ead88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993563"
---
# <a name="service-class-data-structures-in-the-spi"></a>Structures de données de classe de service dans SPI

Quand une nouvelle classe de service est installée, une structure [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) doit être préparée et fournie. Cette structure se compose également de sous-structures qui contiennent une série de paramètres qui s’appliquent à des espaces de noms spécifiques.

![Diagramme montrant la structure WSASERVICECLASSINFO, les sous-structures et les paramètres qui s’appliquent à des espaces de noms spécifiques.](images/ovrvw3-3.png)

Pour chaque classe de service, il existe une seule structure [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . Dans la structure **WSASERVICECLASSINFO** , l’identificateur unique de la classe de service est contenu dans **lpServiceClassId**, et une chaîne d’affichage associée est référencée par **lpServiceClassName**.

Le membre **lpClassInfos** de la structure [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) fait référence à un tableau de structures [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) , chacune d’elles fournissant un paramètre nommé et typé qui s’applique à un espace de noms spécifié. Exemples de valeurs pour le membre **lpszName** : sapid, TCPPORT, UDPPORT, etc. Ces chaînes sont généralement spécifiques à l’espace de noms identifié dans **dwNameSpace**. Les valeurs standard pour **dwValueType** peuvent être reg \_ DWORD, reg \_ SZ, etc. Le membre **dwValueSize** indique la longueur de l’élément de données vers lequel pointe **lpValue**.

L’intégralité de la collection de données représentée dans une structure [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) est fournie à chaque fournisseur d’espace de noms via [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass). Chaque fournisseur d’espace de noms individuel passe ensuite en revue la liste des structures [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) et conserve les informations qui lui sont applicables. Cette architecture permet également d’obtenir l’existence future d’un fournisseur d’espaces de noms spécial qui conservera toutes les informations de schéma de la classe de service pour tous les espaces de noms. L' \_32.dll Ws2 interroge ce fournisseur pour obtenir les données **WSASERVICECLASSINFO** nécessaires pour fournir aux fournisseurs d’espaces de noms lorsque [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) est appelé pour initier une requête, et lorsque [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice) est appelé pour inscrire un service. Le fournisseur d’espaces de noms ne doit pas s’appuyer sur cette fonctionnalité pour le moment et doit disposer d’un moyen spécifique au fournisseur pour obtenir les informations de schéma de classe de service nécessaires. En l’absence d’un fournisseur qui stocke tous les schémas de classe de service pour tous les espaces de noms, le \_32.dll Ws2 utilise [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) pour obtenir ces informations de chaque fournisseur d’espace de noms individuel.

 

 



