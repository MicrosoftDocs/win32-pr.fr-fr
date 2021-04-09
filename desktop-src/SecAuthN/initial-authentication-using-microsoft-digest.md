---
description: L’authentification initiale a lieu lorsque le serveur reçoit une réponse à une demande d’un client.
ms.assetid: 8a5cf26b-0b2a-4f19-807b-9ec4d533cdd4
title: Authentification initiale à l’aide de Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ed4960d947bbc60df962e6a9b71be755e158c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867861"
---
# <a name="initial-authentication-using-microsoft-digest"></a>Authentification initiale à l’aide de Microsoft Digest

L’authentification initiale a lieu lorsque le serveur reçoit une réponse à une demande d’un client. L’authentification d’une réponse de stimulation implique généralement un minimum de deux serveurs :

-   Le serveur d’origine : reçoit la demande du client et émet une stimulation, puis reçoit la réponse de la stimulation du client qui doit être authentifiée.
-   Serveur d’authentification : reçoit les informations d’autorisation du serveur d’origine et effectue l’authentification. Ce serveur est généralement un contrôleur de domaine qui prend en charge plusieurs serveurs d’origine.

Lorsque le serveur d’origine reçoit une demande avec un en-tête d’autorisation contenant une réponse de stimulation Digest, l’authentification se poursuit comme suit :

-   L’identité du serveur d’origine est vérifiée par rapport au serveur encodé dans la valeur à usage unique de la demande.
-   L’horodatage encodé dans la valeur à usage unique est vérifié. Si la valeur à usage unique a expiré et que les informations de nom d’utilisateur/mot de passe sont valides, le serveur d’origine met fin à l’authentification en émettant une nouvelle demande Digest avec la directive obsolète définie sur « true ». Cela indique que seule la valeur à usage unique était « obsolète » et que le client peut répondre à la nouvelle demande en utilisant le mot de passe utilisé dans la réponse précédente. Si le client reçoit un nouveau défi après l’envoi de la réponse de stimulation pour la demande obsolète, le client doit générer une nouvelle réponse de stimulation.
-   Si la détection de relecture est appliquée, la directive NC (nombre de nonce) est vérifiée par rapport à la base de données de session à usage unique gérée par le serveur.
-   Le serveur d’authentification est identifié et a envoyé les informations d’autorisation du client.
-   Le serveur d’authentification vérifie l’identité du serveur encodé dans la valeur à usage unique par rapport à l’identité du serveur d’origine.
-   Le serveur d’authentification, qui est un contrôleur de domaine, récupère le mot de passe de l’utilisateur.
-   À l’aide des informations d’autorisation, du mot de passe et de l’identification du serveur d’origine, le serveur d’authentification calcule la valeur que le client doit avoir fournie dans la directive de réponse de la réponse de stimulation. Le serveur d’authentification compare la valeur calculée à la réponse du client pour déterminer la réussite ou l’échec de l’authentification.

Si l’authentification réussit, le [*contexte de sécurité*](../secgloss/s-gly.md) de l’utilisateur et une [*clé de session*](../secgloss/s-gly.md) Digest sont retournés au serveur d’origine. Si l’authentification échoue, le serveur d’origine doit générer une réponse d’erreur. Après une authentification réussie, le serveur d’origine retourne la ressource demandée au client.

La clé de session Digest retournée par le serveur d’authentification est mise en cache par le serveur d’origine pour être utilisée lors de l’authentification des demandes ultérieures. Pour plus d’informations, consultez [authentification des demandes suivantes à l’aide de Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

 

 
