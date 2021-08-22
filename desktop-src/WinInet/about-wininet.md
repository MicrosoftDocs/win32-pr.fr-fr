---
title: À propos de WinINet
description: l’interface de programmation d’applications (API) Windows Internet (WinINet) permet à votre application d’interagir avec les protocoles FTP et HTTP pour accéder aux ressources Internet.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- À propos de wininet wininet
- Wininet wininet, à propos de
- Wininet wininet, page de démarrage
- Windows WinINet Internet
- internet, Windows WinINet internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be38840c33735a1e064e9bdc5e044651130d6e15a6fe22d004a2e8d7c29bf140
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051867"
---
# <a name="about-wininet"></a>À propos de WinINet

> [!NOTE]
> pour les conteneurs d’applications depuis Windows 10, la version 1709, HTTP/2 (voir [RFC7540](https://tools.ietf.org/html/rfc7540)) est activée par défaut.

l’interface de programmation d’applications (API) Windows Internet (WinINet) permet à votre application d’interagir avec les protocoles FTP et HTTP pour accéder aux ressources Internet. À mesure que les normes évoluent, ces fonctions gèrent les modifications apportées aux protocoles sous-jacents, ce qui leur permet de conserver un comportement cohérent.

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Permet également aux applications d’interagir avec Gopher.

Pour plus d'informations, consultez les pages suivantes :

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
