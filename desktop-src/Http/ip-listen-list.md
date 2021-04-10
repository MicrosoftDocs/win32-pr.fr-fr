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
# <a name="ip-listen-list"></a>Liste d’écoutes IP

Les API de serveur HTTP ne sont pas liées à une adresse IP et à des paires de ports TCP tant qu’un utilisateur n’a pas inscrit un UrlPrefix. Par défaut, une fois qu’une inscription est entrée dans la file d’attente des demandes, l’API du serveur HTTP est liée au port spécifié dans le UrlPrefix (par exemple, le port 80) pour toutes les adresses IP (inadr \_ any ou INADDR6 \_ any) disponibles sur l’ordinateur. Des problèmes surviennent lorsque des applications tierces (qui n’utilisent pas les API du serveur HTTP) sont liées à l’adresse IP et aux paires port 80 sur l’ordinateur. L’API du serveur HTTP permet de configurer la liste des adresses IP qu’elle lie et résout ce problème de coexistence. L’administrateur système appelle la fonction [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) avec le paramètre *ConfigId* défini sur la valeur HttpServiceConfigIPListenList pour spécifier la liste d’écoutes IP. Les adresses IPv4 et IPv6 peuvent être ajoutées à la liste. Les adresses IP entrées s’appliquent à toutes les applications sur l’ordinateur à l’aide de l’API du serveur HTTP et sont conservées entre les redémarrages de la machine. Toutefois, les modifications apportées à la configuration de la liste d’écoutes IP n’ont pas lieu de manière dynamique. dans la plupart des cas, un redémarrage du système peut être nécessaire.

 

 




