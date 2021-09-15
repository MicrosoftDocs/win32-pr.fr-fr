---
description: Après l’établissement d’un contexte de sécurité, l’application peut utiliser les fonctions de prise en charge des messages pour transmettre des messages résistants aux falsifications.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Garantir l’intégrité des communications pendant la Exchange des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70545abf11a933cd3bb6d0c32f3312637fcccbe2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237918"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a>Garantir l’intégrité des communications pendant la Exchange des messages

Après l’établissement d’un [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) , l’application peut utiliser les fonctions de [prise en charge des messages](authentication-functions.md) pour transmettre des messages résistants aux falsifications.

Le client ou le serveur transmet le contexte de sécurité et un message à la fonction [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) pour générer une signature sécurisée qui empêche la modification du message en cours de transit. Le récepteur du message appelle la fonction [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) . **VerifySignature** utilise les informations de la signature pour vérifier que le message reçu n’a pas été modifié lors de la transmission. Le client et le serveur peuvent également échanger des messages chiffrés à l’aide de [**EncryptMessage (général)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) et [**DecryptMessage (général)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).

Le serveur dans une connexion authentifiée peut également établir des connexions avec d’autres ordinateurs distants dans le nom du client après avoir appelé [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).

 

 
