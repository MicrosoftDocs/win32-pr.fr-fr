---
title: Liste d’écoutes IP
description: Les API de serveur HTTP ne sont pas liées à une adresse IP et à des paires de ports TCP tant qu’un utilisateur n’a pas inscrit un UrlPrefix.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940288"
---
# <a name="ip-listen-list"></a><span data-ttu-id="af769-103">Liste d’écoutes IP</span><span class="sxs-lookup"><span data-stu-id="af769-103">IP Listen List</span></span>

<span data-ttu-id="af769-104">Les API de serveur HTTP ne sont pas liées à une adresse IP et à des paires de ports TCP tant qu’un utilisateur n’a pas inscrit un UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="af769-104">The HTTP Server APIs do not bind to any IP address and TCP port pairs until a user registers a UrlPrefix.</span></span> <span data-ttu-id="af769-105">Par défaut, une fois qu’une inscription est entrée dans la file d’attente des demandes, l’API du serveur HTTP est liée au port spécifié dans le UrlPrefix (par exemple, le port 80) pour toutes les adresses IP (inadr \_ any ou INADDR6 \_ any) disponibles sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="af769-105">By default, once a registration is entered in the request queue, the HTTP Server API binds to the port specified in the UrlPrefix (for example port 80) for all IP addresses (INADDR\_ANY or INADDR6\_ANY) available on the machine.</span></span> <span data-ttu-id="af769-106">Des problèmes surviennent lorsque des applications tierces (qui n’utilisent pas les API du serveur HTTP) sont liées à l’adresse IP et aux paires port 80 sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="af769-106">Problems arise when third party applications (not using the HTTP Server APIs) bind to IP address and port 80 pairs on the machine.</span></span> <span data-ttu-id="af769-107">L’API du serveur HTTP permet de configurer la liste des adresses IP qu’elle lie et résout ce problème de coexistence.</span><span class="sxs-lookup"><span data-stu-id="af769-107">The HTTP Server API provides a way to configure the list of IP addresses that it binds and solves this coexistence issue.</span></span> <span data-ttu-id="af769-108">L’administrateur système appelle la fonction [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) avec le paramètre *ConfigId* défini sur la valeur HttpServiceConfigIPListenList pour spécifier la liste d’écoutes IP.</span><span class="sxs-lookup"><span data-stu-id="af769-108">The system administrator calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the *ConfigId* parameter set to the HttpServiceConfigIPListenList value to specify the IP listen list.</span></span> <span data-ttu-id="af769-109">Les adresses IPv4 et IPv6 peuvent être ajoutées à la liste.</span><span class="sxs-lookup"><span data-stu-id="af769-109">Both IPv4 and IPv6 addresses can be added to the list.</span></span> <span data-ttu-id="af769-110">Les adresses IP entrées s’appliquent à toutes les applications sur l’ordinateur à l’aide de l’API du serveur HTTP et sont conservées entre les redémarrages de la machine.</span><span class="sxs-lookup"><span data-stu-id="af769-110">The IP addresses entered apply to all applications on the machine using the HTTP Server API and persist across reboots of the machine.</span></span> <span data-ttu-id="af769-111">Toutefois, les modifications apportées à la configuration de la liste d’écoutes IP n’ont pas lieu de manière dynamique. dans la plupart des cas, un redémarrage du système peut être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="af769-111">However, any changes to the IP listen list configuration do not take place dynamically; in most cases, a system reboot may be necessary.</span></span>

 

 




