---
description: Après l’établissement d’un contexte de sécurité, l’application peut utiliser les fonctions de prise en charge des messages pour transmettre des messages résistants aux falsifications.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Garantir l’intégrité des communications pendant la Exchange des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394f78fcc1e5becf4bdfc7c67db52e1af177a7f3aa427d1c6182a080f0ae87bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008257"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a>Garantir l’intégrité des communications pendant la Exchange des messages

Après l’établissement d’un [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) , l’application peut utiliser les fonctions de [prise en charge des messages](authentication-functions.md) pour transmettre des messages résistants aux falsifications.

Le client ou le serveur transmet le contexte de sécurité et un message à la fonction [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) pour générer une signature sécurisée qui empêche la modification du message en cours de transit. Le récepteur du message appelle la fonction [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) . **VerifySignature** utilise les informations de la signature pour vérifier que le message reçu n’a pas été modifié lors de la transmission. Le client et le serveur peuvent également échanger des messages chiffrés à l’aide de [**EncryptMessage (général)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) et [**DecryptMessage (général)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).

Le serveur dans une connexion authentifiée peut également établir des connexions avec d’autres ordinateurs distants dans le nom du client après avoir appelé [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).

 

 
