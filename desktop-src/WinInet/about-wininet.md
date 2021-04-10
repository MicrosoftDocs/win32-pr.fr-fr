---
title: À propos de WinINet
description: L’interface de programmation d’applications (API) de Windows Internet (WinINet) permet à votre application d’interagir avec les protocoles FTP et HTTP pour accéder aux ressources Internet.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- À propos de wininet wininet
- Wininet wininet, à propos de
- Wininet wininet, page de démarrage
- WinINet Windows Internet
- Internet, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103940720"
---
# <a name="about-wininet"></a>À propos de WinINet

> [!NOTE]
> Pour les conteneurs d’applications depuis Windows 10, version 1709, HTTP/2 (voir [RFC7540](https://tools.ietf.org/html/rfc7540)) est activé par défaut.

L’interface de programmation d’applications (API) de Windows Internet (WinINet) permet à votre application d’interagir avec les protocoles FTP et HTTP pour accéder aux ressources Internet. À mesure que les normes évoluent, ces fonctions gèrent les modifications apportées aux protocoles sous-jacents, ce qui leur permet de conserver un comportement cohérent.

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Permet également aux applications d’interagir avec Gopher.

Pour plus d’informations, consultez :

-   [WinINet et WinHTTP](wininet-vs-winhttp.md)
-   [Handles HINTERNET](appendix-a-hinternet-handles.md)
-   [Prise en charge d’IP version 6](ip-version-6-support.md)
-   [Encodage du contenu \_](content-encoding.md)
-   [Mise en cache](caching.md)
-   [Fonctions communes](common-functions.md)
-   [Sessions FTP](ftp-sessions.md)
-   [Sessions HTTP](http-sessions.md)
-   [Cookies HTTP](http-cookies.md)
-   [Opération asynchrone](asynchronous-operation.md)
-   [Gestion de l’authentification](handling-authentication.md)
-   [Gestion des localisateurs de ressources uniformes](handling-uniform-resource-locators.md)
-   [Indications de sécurité \_](security-guidelines.md)

## <a name="internet-protocols"></a>Protocoles Internet

Les deux principaux protocoles Internet sont FTP et HTTP. Pour plus d’informations sur ces protocoles, consultez les documents RFC (Request for Comments) pour FTP et HTTP :

-   [RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *protocole FTP (FTP)*.
-   [RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol-HTTP/1.0*.
-   [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol-HTTP/1.1*.

> [!NOTE]  
> (Ces ressources peuvent ne pas être disponibles dans certaines langues et certains pays.)

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Le protocole gopher était également pris en charge. Consultez la [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *le protocole Internet Gopher*.
