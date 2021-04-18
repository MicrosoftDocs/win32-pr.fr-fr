---
title: Enregistrement des erreurs dans l'API du serveur HTTP
description: Certains types d’erreurs sont gérés par l’API du serveur HTTP au lieu d’être retransmis à une application pour la gestion, car la fréquence de ces erreurs pourrait autrement saturer un journal des événements ou un gestionnaire d’applications.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API serveur HTTP, journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512026"
---
# <a name="error-logging-in-the-http-server-api"></a><span data-ttu-id="63a7f-104">Enregistrement des erreurs dans l'API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="63a7f-104">Error Logging in the HTTP Server API</span></span>

<span data-ttu-id="63a7f-105">Certains types d’erreurs sont gérés par l’API du serveur HTTP au lieu d’être retransmis à une application pour la gestion, car la fréquence de ces erreurs pourrait autrement saturer un journal des événements ou un gestionnaire d’applications.</span><span class="sxs-lookup"><span data-stu-id="63a7f-105">Some kinds of errors are handled by the HTTP Server API rather than being passed back to an application for handling, because the frequency of such errors could otherwise flood an event log or application handler.</span></span>

<span data-ttu-id="63a7f-106">Les trois rubriques suivantes décrivent les différents aspects de la journalisation des erreurs de l’API du serveur HTTP :</span><span class="sxs-lookup"><span data-stu-id="63a7f-106">The following three topics describe the different aspects of the HTTP Server API error logging:</span></span>

-   <span data-ttu-id="63a7f-107">[Configuration](configuring-http-server-api-error-logging.md) de Les paramètres de Registre contrôlent si l’API du serveur HTTP journalise des erreurs, la taille maximale autorisée des fichiers journaux et l’emplacement où les fichiers journaux sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="63a7f-107">[Configuration](configuring-http-server-api-error-logging.md) Registry settings control whether the HTTP Server API logs errors, the maximum allowable size of log files, and where log files are saved.</span></span>
-   <span data-ttu-id="63a7f-108">[Format du fichier journal](format-of-the-http-server-api-error-logs.md) L’API du serveur HTTP crée des fichiers journaux conformes aux conventions des fichiers journaux du World Wide Web Consortium (W3C) et peut être analysée à l’aide d’outils standard.</span><span class="sxs-lookup"><span data-stu-id="63a7f-108">[Log File Format](format-of-the-http-server-api-error-logs.md) The HTTP Server API creates log files that comply with the World Wide Web Consortium (W3C) log file conventions, and can be parsed by using standard tools.</span></span> <span data-ttu-id="63a7f-109">Toutefois, contrairement aux fichiers journaux W3C, les fichiers journaux de l’API du serveur HTTP ne contiennent pas de noms de colonnes.</span><span class="sxs-lookup"><span data-stu-id="63a7f-109">However, unlike W3C log files, HTTP Server API log files do not contain names of the columns.</span></span>
-   <span data-ttu-id="63a7f-110">[Types d’erreurs consignées](types-of-errors-logged-by-the-http-server-api.md) L’API du serveur HTTP enregistre une série d’erreurs courantes.</span><span class="sxs-lookup"><span data-stu-id="63a7f-110">[Types of Errors Logged](types-of-errors-logged-by-the-http-server-api.md) The HTTP Server API logs a variety of common errors.</span></span>

 

 




