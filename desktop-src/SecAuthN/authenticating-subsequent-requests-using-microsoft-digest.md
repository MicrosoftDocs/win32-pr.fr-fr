---
description: Le serveur envoie au client une référence à son contexte de sécurité partagé à l’aide de la directive opaque de la stimulation Digest.
ms.assetid: 543c4bed-b224-4da7-9746-12c9993a40af
title: Authentification des demandes suivantes avec Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eecccc3be68fb541994e63cdfc5035187e04aa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758398"
---
# <a name="authenticating-subsequent-requests-with-microsoft-digest"></a>Authentification des demandes suivantes avec Microsoft Digest

Le serveur envoie au client une référence à son [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) partagé à l’aide de la directive opaque de la stimulation Digest. Après une authentification réussie, le client doit spécifier cette valeur dans les demandes suivantes adressées au serveur cible. L’inclusion de la valeur opaque dans les demandes de ressources accessibles à l’aide du contexte de sécurité existant évite d’avoir à s’authentifier à nouveau sur le contrôleur de domaine. Ces requêtes sont ré-authentifiées sur le serveur, à l’aide de la [*clé de session*](/windows/desktop/SecGloss/s-gly) Digest mise en cache après l’authentification initiale.

Le diagramme suivant illustre les étapes effectuées par le client et le serveur lors d’une demande ultérieure de ressources protégées par accès.

![authentification des demandes ultérieures à l’aide de Microsoft Digest](images/digest2.png)

Pour demander des ressources supplémentaires après une authentification réussie, le client appelle la fonction Microsoft Digest [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) pour générer une réponse de stimulation Digest. La valeur opaque est incluse dans la directive opaque de la réponse de stimulation envoyée au serveur sous la forme d’un en-tête d’autorisation (indiqué sous forme de requête HTTP).

Le serveur appelle la fonction [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) pour déterminer s’il existe un [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) pour le client. Lorsqu’un contexte existant est trouvé, la fonction retourne SEC \_ E \_ Completed \_ pour indiquer que le serveur doit ensuite appeler la fonction [**CompleteAuthToken**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) . Cette fonction effectue l’authentification du client à l’aide de la [*clé de session*](/windows/desktop/SecGloss/s-gly) Digest mise en cache lors de l' [authentification initiale](initial-authentication-using-microsoft-digest.md) au lieu de réauthentifier sur le contrôleur de domaine.

 

 
