---
title: À propos de l’API du serveur HTTP
description: L’API du serveur HTTP fournit aux développeurs une interface de bas niveau pour le côté serveur de la fonctionnalité HTTP, comme défini dans la norme RFC 2616.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- API serveur HTTP, vue d’ensemble
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e00fcfe6527b77be32a849f00f62222396f42b5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381586"
---
# <a name="about-http-server-api"></a><span data-ttu-id="bb859-104">À propos de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="bb859-104">About HTTP Server API</span></span>

<span data-ttu-id="bb859-105">L’API du serveur HTTP fournit aux développeurs une interface de bas niveau pour le côté serveur de la fonctionnalité HTTP, comme défini dans la [norme RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="bb859-105">The HTTP Server API provides developers with a low-level interface to the server side of the HTTP functionality as defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="bb859-106">L’API permet à une application de recevoir des requêtes HTTP dirigées vers des URL et d’envoyer des réponses HTTP.</span><span class="sxs-lookup"><span data-stu-id="bb859-106">The API enables an application to receive HTTP requests directed to URLs and send HTTP responses.</span></span> <span data-ttu-id="bb859-107">Pour l’envoi de réponses dynamiques, les interfaces ISAPI ou ASP.NET sont recommandées.</span><span class="sxs-lookup"><span data-stu-id="bb859-107">For sending dynamic responses, the ISAPI or ASP.NET interfaces are recommended.</span></span>

<span data-ttu-id="bb859-108">L’API du serveur HTTP permet à plusieurs applications de coexister sur un système, en partageant le même port TCP (par exemple, le port 80 pour HTTP ou le port 443 pour HTTPs) et en desservant différentes parties de l’espace de noms d’URL.</span><span class="sxs-lookup"><span data-stu-id="bb859-108">The HTTP Server API enables multiple applications to coexist on a system, sharing the same TCP port (for example, port 80 for HTTP or port 443 for HTTPS) and serving different parts of the URL namespace.</span></span>

<span data-ttu-id="bb859-109">L’API du serveur HTTP nécessite une connaissance du langage de programmation C et une connaissance de la programmation de l’API Windows.</span><span class="sxs-lookup"><span data-stu-id="bb859-109">The HTTP Server API requires knowledge of the C programming language and a familiarity with Windows API programming.</span></span> <span data-ttu-id="bb859-110">Les applications qui n’ont pas besoin d’un accès de bas niveau à HTTP doivent utiliser les classes ISAPI IIS ou .NET Framework pour les solutions basées sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="bb859-110">Applications that do not require low-level access to HTTP should use the IIS ISAPI or the .NET Framework classes for HTTP-based solutions.</span></span>

 

 




