---
title: Configuration HTTP requise pour les téléchargements BITS
description: BITS prend en charge les téléchargements HTTP et HTTPs, ainsi que les chargements et requiert que le serveur prenne en charge le protocole HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462070"
---
# <a name="http-requirements-for-bits-downloads"></a><span data-ttu-id="ab9ec-103">Configuration HTTP requise pour les téléchargements BITS</span><span class="sxs-lookup"><span data-stu-id="ab9ec-103">HTTP Requirements for BITS Downloads</span></span>

<span data-ttu-id="ab9ec-104">BITS prend en charge les téléchargements HTTP et HTTPs, ainsi que les chargements et requiert que le serveur prenne en charge le protocole HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-104">BITS supports HTTP and HTTPS downloads and uploads and requires that the server supports the HTTP/1.1 protocol.</span></span> <span data-ttu-id="ab9ec-105">Pour les téléchargements, la méthode **Head** du serveur http doit retourner la taille du fichier et sa méthode d' **extraction** doit prendre en charge les en-têtes Content-Range et Content-Length.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-105">For downloads, the HTTP server's **Head** method must return the file size and its **Get** method must support the Content-Range and Content-Length headers.</span></span> <span data-ttu-id="ab9ec-106">Par conséquent, BITS transfère uniquement le contenu du fichier statique et génère une erreur si vous tentez de transférer du contenu dynamique, à moins que le script ASP, ISAPI ou CGI ne prenne en charge les en-têtes Content-Range et Content-Length.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-106">As a result, BITS only transfers static file content and generates an error if you try to transfer dynamic content, unless the ASP, ISAPI, or CGI script supports the Content-Range and Content-Length headers.</span></span>

<span data-ttu-id="ab9ec-107">BITS peut utiliser un serveur HTTP/1.0, à condition qu’il réponde aux exigences de la méthode **Head** et de la méthode d' **extraction** .</span><span class="sxs-lookup"><span data-stu-id="ab9ec-107">BITS can use an HTTP/1.0 server as long as it meets the **Head** and **Get** method requirements.</span></span>

<span data-ttu-id="ab9ec-108">Pour prendre en charge le téléchargement des plages d’un fichier, le serveur doit prendre en charge les exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="ab9ec-108">To support downloading ranges of a file, the server must support the following requirements:</span></span>

-   <span data-ttu-id="ab9ec-109">Autorisez les en-têtes MIME à inclure les en-têtes standard content-Range et Content-type, plus un maximum de 180 octets d’autres en-têtes.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-109">Allow MIME headers to include the standard Content-Range and Content-Type headers, plus a maximum of 180 bytes of other headers.</span></span>
-   <span data-ttu-id="ab9ec-110">Autorisez un maximum de deux CR/LFs entre les en-têtes HTTP et la première chaîne de limite.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-110">Allow a maximum of two CR/LFs between the HTTP headers and the first boundary string.</span></span>

 

 




