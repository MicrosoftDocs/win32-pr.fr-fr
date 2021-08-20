---
title: Configuration de l’authentification dynamique
description: Les applications peuvent modifier les configurations d’authentification sur un groupe d’URL ou une session de serveur à tout moment.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fda33e150826ed7d84ac45c4ab0771136991aa9aeb2766d5d395a65da270775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014837"
---
# <a name="dynamic-authentication-configuration"></a>Configuration de l’authentification dynamique

Par défaut, l’API du serveur HTTP n’effectue pas d’authentification, sauf si l’application l’active spécifiquement. Les applications peuvent modifier les configurations d’authentification sur un groupe d’URL ou une session de serveur à tout moment. Les modifications apportées à la configuration de l’authentification n’affectent pas les requêtes qui sont déjà authentifiées ou distribuées à l’application

Pour les schémas d’authentification où plusieurs séries de protocoles de transfert sont nécessaires, l’API du serveur HTTP supprime le protocole de transfert d’authentification si le schéma actuel n’est plus pris en charge en raison des modifications de configuration apportées à l’application. Par exemple, si l’application active Negotiate et désactive NTLM, et que l’API du serveur HTTP se trouve dans le protocole de transfert d’authentification intermédiaire pour NTLM, la négociation pour NTLM est ignorée et la demande est transmise à l’application. L’application envoie une demande d’authentification 401 avec les nouveaux types d’authentification spécifiés dans l’en-tête WWW-Authenticate.

 

 




