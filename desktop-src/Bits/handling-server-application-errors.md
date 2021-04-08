---
title: Gestion des erreurs d’application serveur
description: Si l’application serveur traite correctement le fichier téléchargé, l’application doit retourner 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671437"
---
# <a name="handling-server-application-errors"></a><span data-ttu-id="b7044-103">Gestion des erreurs d’application serveur</span><span class="sxs-lookup"><span data-stu-id="b7044-103">Handling Server Application Errors</span></span>

<span data-ttu-id="b7044-104">Si l’application serveur traite correctement le fichier téléchargé, l’application doit retourner 200.</span><span class="sxs-lookup"><span data-stu-id="b7044-104">If the server application successfully processes the uploaded file, the application should return 200.</span></span> <span data-ttu-id="b7044-105">Si l’application ne retourne pas 200, le client BITS utilise le code d’erreur pour déterminer si l’erreur est une erreur temporaire ou une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="b7044-105">If the application does not return 200, the BITS client uses the error code to determine if the error is a transient error or fatal error.</span></span>

<span data-ttu-id="b7044-106">Tous les codes d’erreur 3xx sont des erreurs temporaires, à l’exception de 300-305 et 307, qui sont des erreurs irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="b7044-106">All 3xx error codes are transient errors except 300 - 305 and 307, which are fatal errors.</span></span> <span data-ttu-id="b7044-107">Tous les codes d’erreur 4xx sont des erreurs irrécupérables, à l’exception de 408 et 409, qui sont des erreurs temporaires.</span><span class="sxs-lookup"><span data-stu-id="b7044-107">All 4xx error codes are fatal errors except for 408 and 409, which are transient errors.</span></span> <span data-ttu-id="b7044-108">Tous les codes d’erreur 5xx sont des erreurs temporaires, à l’exception de 501 et 505, qui sont des erreurs irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="b7044-108">All 5xx error codes are transient errors except 501 and 505, which are fatal errors.</span></span> <span data-ttu-id="b7044-109">Tous les autres codes HTTP sont considérés comme des erreurs temporaires.</span><span class="sxs-lookup"><span data-stu-id="b7044-109">All other HTTP codes are considered transient errors.</span></span> <span data-ttu-id="b7044-110">Notez qu’un code d’erreur 403 est le seul code d’erreur qui empêche les BITS de publier le fichier de téléchargement vers l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="b7044-110">Note that a 403 error code is the only error code that prevents BITS from posting the upload file to the server application again.</span></span>

<span data-ttu-id="b7044-111">Pour récupérer l’erreur, appelez la méthode [**IBackgroundCopyError :: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) .</span><span class="sxs-lookup"><span data-stu-id="b7044-111">To retrieve the error, call the [**IBackgroundCopyError::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) method.</span></span> <span data-ttu-id="b7044-112">Le contexte d’erreur est l' \_ \_ \_ application distante du contexte d’erreur BG \_ .</span><span class="sxs-lookup"><span data-stu-id="b7044-112">The error context will be BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION.</span></span>

 

 




