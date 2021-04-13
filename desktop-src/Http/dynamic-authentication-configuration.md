---
title: Configuration de l’authentification dynamique
description: Les applications peuvent modifier les configurations d’authentification sur un groupe d’URL ou une session de serveur à tout moment.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c68daf04d870d4aa50596397f4f021ac1729af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309489"
---
# <a name="dynamic-authentication-configuration"></a><span data-ttu-id="fbfc3-103">Configuration de l’authentification dynamique</span><span class="sxs-lookup"><span data-stu-id="fbfc3-103">Dynamic Authentication Configuration</span></span>

<span data-ttu-id="fbfc3-104">Par défaut, l’API du serveur HTTP n’effectue pas d’authentification, sauf si l’application l’active spécifiquement.</span><span class="sxs-lookup"><span data-stu-id="fbfc3-104">By default, the HTTP Server API does not perform authentication unless the application specifically enables it.</span></span> <span data-ttu-id="fbfc3-105">Les applications peuvent modifier les configurations d’authentification sur un groupe d’URL ou une session de serveur à tout moment.</span><span class="sxs-lookup"><span data-stu-id="fbfc3-105">Applications can change authentication configurations on a URL Group or server session at any time.</span></span> <span data-ttu-id="fbfc3-106">Les modifications apportées à la configuration de l’authentification n’affectent pas les requêtes qui sont déjà authentifiées ou distribuées à l’application</span><span class="sxs-lookup"><span data-stu-id="fbfc3-106">Changes to the authentication configuration do not affect requests that are already authenticated or being dispatched to the application</span></span>

<span data-ttu-id="fbfc3-107">Pour les schémas d’authentification où plusieurs séries de protocoles de transfert sont nécessaires, l’API du serveur HTTP supprime le protocole de transfert d’authentification si le schéma actuel n’est plus pris en charge en raison des modifications de configuration apportées à l’application.</span><span class="sxs-lookup"><span data-stu-id="fbfc3-107">For authentication schemes where multiple rounds of handshake are required, the HTTP Server API drops the authentication handshake if the current scheme is no longer supported due to configuration changes from the application.</span></span> <span data-ttu-id="fbfc3-108">Par exemple, si l’application active Negotiate et désactive NTLM, et que l’API du serveur HTTP se trouve dans le protocole de transfert d’authentification intermédiaire pour NTLM, la négociation pour NTLM est ignorée et la demande est transmise à l’application.</span><span class="sxs-lookup"><span data-stu-id="fbfc3-108">For example, if the application enables Negotiate and disables NTLM, and the HTTP Server API is in the intermediate authentication handshake for NTLM, the handshake for NTLM is discarded and the request is passed to the application.</span></span> <span data-ttu-id="fbfc3-109">L’application envoie une demande d’authentification 401 avec les nouveaux types d’authentification spécifiés dans l’en-tête WWW-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="fbfc3-109">The application sends a 401 authentication challenge with the new authentication types specified in the WWW-Authenticate header.</span></span>

 

 




