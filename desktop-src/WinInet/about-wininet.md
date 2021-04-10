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
# <a name="about-wininet"></a><span data-ttu-id="c1c89-108">À propos de WinINet</span><span class="sxs-lookup"><span data-stu-id="c1c89-108">About WinINet</span></span>

> [!NOTE]
> <span data-ttu-id="c1c89-109">Pour les conteneurs d’applications depuis Windows 10, version 1709, HTTP/2 (voir [RFC7540](https://tools.ietf.org/html/rfc7540)) est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="c1c89-109">For app containers since Windows 10, version 1709, HTTP/2 (see [RFC7540](https://tools.ietf.org/html/rfc7540)) is on by default.</span></span>

<span data-ttu-id="c1c89-110">L’interface de programmation d’applications (API) de Windows Internet (WinINet) permet à votre application d’interagir avec les protocoles FTP et HTTP pour accéder aux ressources Internet.</span><span class="sxs-lookup"><span data-stu-id="c1c89-110">The Windows Internet (WinINet) application programming interface (API) enables your application to interact with FTP and HTTP protocols to access Internet resources.</span></span> <span data-ttu-id="c1c89-111">À mesure que les normes évoluent, ces fonctions gèrent les modifications apportées aux protocoles sous-jacents, ce qui leur permet de conserver un comportement cohérent.</span><span class="sxs-lookup"><span data-stu-id="c1c89-111">As standards evolve, these functions handle the changes in underlying protocols, enabling them to maintain consistent behavior.</span></span>

<span data-ttu-id="c1c89-112">**Windows XP et Windows Server 2003 R2 et versions antérieures :** Permet également aux applications d’interagir avec Gopher.</span><span class="sxs-lookup"><span data-stu-id="c1c89-112">**Windows XP and Windows Server 2003 R2 and earlier:** Also enabled applications to interact with Gopher.</span></span>

<span data-ttu-id="c1c89-113">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="c1c89-113">For more information, see:</span></span>

-   [<span data-ttu-id="c1c89-114">WinINet et WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c1c89-114">WinINet vs. WinHTTP</span></span>](wininet-vs-winhttp.md)
-   [<span data-ttu-id="c1c89-115">Handles HINTERNET</span><span class="sxs-lookup"><span data-stu-id="c1c89-115">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
-   [<span data-ttu-id="c1c89-116">Prise en charge d’IP version 6</span><span class="sxs-lookup"><span data-stu-id="c1c89-116">IP Version 6 Support</span></span>](ip-version-6-support.md)
-   [<span data-ttu-id="c1c89-117">Encodage du contenu \_</span><span class="sxs-lookup"><span data-stu-id="c1c89-117">Content\_Encoding</span></span>](content-encoding.md)
-   [<span data-ttu-id="c1c89-118">Mise en cache</span><span class="sxs-lookup"><span data-stu-id="c1c89-118">Caching</span></span>](caching.md)
-   [<span data-ttu-id="c1c89-119">Fonctions communes</span><span class="sxs-lookup"><span data-stu-id="c1c89-119">Common Functions</span></span>](common-functions.md)
-   [<span data-ttu-id="c1c89-120">Sessions FTP</span><span class="sxs-lookup"><span data-stu-id="c1c89-120">FTP Sessions</span></span>](ftp-sessions.md)
-   [<span data-ttu-id="c1c89-121">Sessions HTTP</span><span class="sxs-lookup"><span data-stu-id="c1c89-121">HTTP Sessions</span></span>](http-sessions.md)
-   [<span data-ttu-id="c1c89-122">Cookies HTTP</span><span class="sxs-lookup"><span data-stu-id="c1c89-122">HTTP Cookies</span></span>](http-cookies.md)
-   [<span data-ttu-id="c1c89-123">Opération asynchrone</span><span class="sxs-lookup"><span data-stu-id="c1c89-123">Asynchronous Operation</span></span>](asynchronous-operation.md)
-   [<span data-ttu-id="c1c89-124">Gestion de l’authentification</span><span class="sxs-lookup"><span data-stu-id="c1c89-124">Handling Authentication</span></span>](handling-authentication.md)
-   [<span data-ttu-id="c1c89-125">Gestion des localisateurs de ressources uniformes</span><span class="sxs-lookup"><span data-stu-id="c1c89-125">Handling Uniform Resource Locators</span></span>](handling-uniform-resource-locators.md)
-   [<span data-ttu-id="c1c89-126">Indications de sécurité \_</span><span class="sxs-lookup"><span data-stu-id="c1c89-126">Security\_Guideline</span></span>](security-guidelines.md)

## <a name="internet-protocols"></a><span data-ttu-id="c1c89-127">Protocoles Internet</span><span class="sxs-lookup"><span data-stu-id="c1c89-127">Internet Protocols</span></span>

<span data-ttu-id="c1c89-128">Les deux principaux protocoles Internet sont FTP et HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1c89-128">The two primary Internet protocols are FTP and HTTP.</span></span> <span data-ttu-id="c1c89-129">Pour plus d’informations sur ces protocoles, consultez les documents RFC (Request for Comments) pour FTP et HTTP :</span><span class="sxs-lookup"><span data-stu-id="c1c89-129">For more information about these protocols, see the Request For Comments (RFC) documents for FTP and HTTP:</span></span>

-   <span data-ttu-id="c1c89-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *protocole FTP (FTP)*.</span><span class="sxs-lookup"><span data-stu-id="c1c89-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.</span></span>
-   <span data-ttu-id="c1c89-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol-HTTP/1.0*.</span><span class="sxs-lookup"><span data-stu-id="c1c89-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol - HTTP/1.0*.</span></span>
-   <span data-ttu-id="c1c89-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol-HTTP/1.1*.</span><span class="sxs-lookup"><span data-stu-id="c1c89-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol - HTTP/1.1*.</span></span>

> [!NOTE]  
> <span data-ttu-id="c1c89-133">(Ces ressources peuvent ne pas être disponibles dans certaines langues et certains pays.)</span><span class="sxs-lookup"><span data-stu-id="c1c89-133">(These resources may not be available in some languages and countries.)</span></span>

<span data-ttu-id="c1c89-134">**Windows XP et Windows Server 2003 R2 et versions antérieures :** Le protocole gopher était également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c1c89-134">**Windows XP and Windows Server 2003 R2 and earlier:** The Gopher protocol was also supported.</span></span> <span data-ttu-id="c1c89-135">Consultez la [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *le protocole Internet Gopher*.</span><span class="sxs-lookup"><span data-stu-id="c1c89-135">See [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *The Internet Gopher Protocol*.</span></span>
