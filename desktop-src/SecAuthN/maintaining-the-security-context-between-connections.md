---
description: Pour réduire le trafic des contrôleurs de domaine et améliorer les performances, le côté client de Microsoft Digest met en cache les informations reçues après une authentification réussie avec un serveur.
ms.assetid: cd928266-889a-494c-a94b-4ea7b1dcc241
title: Maintien du contexte de sécurité entre les connexions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb450dde789f17f46397cb56fe74b94adcf8ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319834"
---
# <a name="maintaining-the-security-context-between-connections"></a>Maintien du contexte de sécurité entre les connexions

Pour réduire le trafic des contrôleurs de domaine et améliorer les performances, le côté client de Microsoft Digest met en cache les informations reçues après une authentification réussie avec un serveur. Les applications clientes doivent uniquement mettre en cache le handle du [*contexte de sécurité*](../secgloss/s-gly.md) qui a été établi. Le tableau suivant décrit les informations mises en cache par le package de sécurité.



| Information                                                       | Description                                                                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom du serveur                                                       | Serveur qui a créé avec succès un contexte de sécurité pour l’utilisateur.                                                                           |
| Domaine/domaine                                                      | Nom de domaine utilisé dans l’authentification réussie.                                                                                              |
| [*Unique*](../secgloss/n-gly.md) | Une valeur à usage unique de serveur associée à la réussite de l’authentification.                                                                               |
| Nombre de nonce                                                       | Nombre de fois où le client a inclus la valeur à usage unique dans les demandes adressées au serveur. Utilisé pour la détection de relecture.                                 |
| Valeur opaque                                                      | Valeur retournée pour la directive opaque après une authentification réussie. Cette valeur contient une référence au contexte de sécurité de l’utilisateur. |



 

Lorsqu’un client envoie un message à un serveur, le serveur doit déterminer si le client dispose d’un contexte de sécurité existant. Pour ce faire, le serveur passe chaque demande du client à la fonction [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Cette fonction extrait la valeur de la directive opaque de la demande, le cas échéant, et l’utilise pour rechercher le contexte de sécurité du client. Si le contexte de sécurité est trouvé, le handle du contexte est retourné au serveur. Pour obtenir des informations connexes, consultez [authentification des demandes suivantes](authenticating-subsequent-requests-using-microsoft-digest.md).

Pour détecter les attaques d’usurpation et de relecture, le client appelle la fonction [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) qui utilise un contexte de sécurité pour signer un message. Lorsque les messages sont protégés à l’aide de la fonction **MakeSignature** , le serveur utilise la fonction [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) avec le contexte mis en cache pour vérifier l’origine et l' [*intégrité*](../secgloss/i-gly.md)du message. Pour plus d’informations, consultez [protection des messages](protecting-messages-using-microsoft-digest.md).

 

 
