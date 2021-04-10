---
title: Mise en cache des informations d'identification
description: Mise en cache des informations d'identification
ms.assetid: 6e411333-56fa-455b-a90a-f2b54f3c9545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a139d0cd90495de87f42de08687fd3157acaf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940153"
---
# <a name="credential-caching"></a>Mise en cache des informations d'identification

## <a name="credential-caching-on-ntlm-ka-connections"></a>Mise en cache des informations d’identification sur des connexions KA NTLM

L’API du serveur HTTP met en cache les informations d’identification uniquement sur des connexions Keep-Alive (KA) pour l’authentification NTLM. Par défaut, l’API du serveur HTTP met en cache les informations d’identification obtenues lors de la première demande envoyée sur une connexion KA. Le client peut envoyer des demandes suivantes sur des connexions KA sans en-tête d’autorisation et obtenir l’authentification en fonction du contexte établi précédemment. Dans ce cas, l’API du serveur HTTP envoie le jeton en fonction des informations d’identification mises en cache à l’application. Les informations d’identification pour une demande envoyée par un proxy ne sont pas mises en cache. L’application désactive la mise en cache des informations d’identification NTLM en définissant l’indicateur **DisableNTLMCredentialCaching** dans la structure des [**\_ \_ \_ informations d’authentification du serveur http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) fournie dans les appels à HttpSetServerSessionProperty ou HttpSetUrlGroupProperty. Lorsque la mise en cache des informations d’identification est désactivée, l’API du serveur HTTP ignore les informations d’identification mises en cache et effectue l’authentification pour chaque demande

## <a name="ntlm-credential-caching-for-specific-urls"></a>Mise en cache des informations d’identification NTLM pour des URL spécifiques

L’application détermine si les informations d’identification de la demande retournées par l’API du serveur HTTP sont mises en cache en inspectant le paramètre flags de la structure des informations d’authentification de la \_ requête HTTP \_ \_ . Ce paramètre indique \_ \_ \_ \_ \_ le jeton d’indicateur d’authentification de la requête HTTP pour le \_ cred mis en cache \_ lorsque le jeton NTLM retourné a été récupéré à partir du cache. La mise en cache des informations d’identification est spécifiée sur un groupe d’URL pour toutes les URL du groupe. La mise en cache des informations d’identification par URL n’est pas prise en charge. Toutefois, les applications peuvent déterminer s’il faut accepter ou rejeter les informations d’identification mises en cache par URL en vérifiant le \_ \_ jeton d’indicateur d’authentification de la requête HTTP \_ pour l' \_ \_ \_ indicateur cred mis en cache \_ dans la structure des informations d’authentification de la \_ requête HTTP \_ \_ . L’application rejette les informations d’identification mises en cache en envoyant une demande d’authentification 401 au client. Le client renvoie ensuite la demande avec les en-têtes d’autorisation, en déclenchant une nouvelle négociation d’authentification avec l’API du serveur HTTP.

## <a name="basic-authentication"></a>Authentification de base

Lorsqu’un en-tête d’authentification de base est inclus dans la demande, l’API du serveur HTTP analyse l’en-tête pour obtenir le nom d’utilisateur et le mot de passe. Le nom d’utilisateur est ensuite analysé dans les parties utilisateur et domaine. L’API du serveur HTTP met en cache le jeton d’accès, obtenu pour l’authentification de base, en fonction du nom d’utilisateur et de la clé de domaine. Lorsqu’une nouvelle demande est reçue, l’API du serveur HTTP récupère le jeton d’accès en fonction du nom d’utilisateur et du domaine. Le mot de passe de la demande est ensuite comparé au mot de passe mis en cache. Le jeton d’accès mis en cache est supprimé lorsque la limite de durée de vie (TTL) est atteinte.

 

 




