---
description: La sémantique pour les contextes de datagramme, ou sans connexion, diffère légèrement de celles des contextes orientés connexion.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Contextes de datagramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113811"
---
# <a name="datagram-contexts"></a>Contextes de datagramme

La sémantique pour les contextes de [*datagramme*](/windows/desktop/SecGloss/d-gly), ou sans connexion, diffère légèrement de celles des contextes orientés connexion. Dans le [*contexte*](/windows/desktop/SecGloss/c-gly)sans connexion d’un datagramme, un serveur ne peut pas déterminer à quel moment le client s’est arrêté ou a arrêté la connexion. En d’autres termes, aucune notification d’arrêt n’est transmise à partir de l’application de transport vers le serveur, comme cela se produit dans un contexte orienté connexion.

Pour utiliser un contexte de datagramme, un client définit l' \_ indicateur d’ISC req \_ Datagram dans son appel à la fonction [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .

> [!IMPORTANT]
> Le package [Microsoft Kerberos](microsoft-kerberos.md) ne prend pas en charge les contextes de datagramme en mode utilisateur à utilisateur.

 

Pour mieux prendre en charge certains modèles, en particulier les RPC de type DCE, les règles suivantes s’appliquent lorsque le client utilise un contexte de datagramme :

-   Le [*package de sécurité*](/windows/desktop/SecGloss/s-gly) ne produit pas d’objet [*BLOB*](/windows/desktop/SecGloss/b-gly) d’authentification (objet binaire volumineux) lors du premier appel à [**InitializeSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta). Toutefois, le client peut utiliser le contexte de sécurité retourné dans un appel à la fonction [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) pour générer une signature pour un message.
-   Le package de sécurité doit autoriser la réinitialisation du contexte à plusieurs heures pour permettre au serveur de supprimer la connexion sans préavis. Cela implique que toutes les clés utilisées dans les fonctions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) et [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) peuvent être réinitialisées à un [*État*](/windows/desktop/SecGloss/s-gly)cohérent.
-   Le package de sécurité permet à l’appelant de spécifier des informations de séquence et fournit les informations de séquence du côté du destinataire. Cela s’ajoute aux informations de séquence gérées par le package.

Un package de sécurité définit l' \_ \_ indicateur de datagramme de l’indicateur SECPKG pour indiquer qu’il prend en charge la sémantique du datagramme.

 

 
