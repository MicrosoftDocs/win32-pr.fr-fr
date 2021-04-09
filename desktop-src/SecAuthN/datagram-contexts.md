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
# <a name="datagram-contexts"></a><span data-ttu-id="1a03d-103">Contextes de datagramme</span><span class="sxs-lookup"><span data-stu-id="1a03d-103">Datagram Contexts</span></span>

<span data-ttu-id="1a03d-104">La sémantique pour les contextes de [*datagramme*](/windows/desktop/SecGloss/d-gly), ou sans connexion, diffère légèrement de celles des contextes orientés connexion.</span><span class="sxs-lookup"><span data-stu-id="1a03d-104">The semantics for [*datagram*](/windows/desktop/SecGloss/d-gly), or connectionless, contexts differ slightly from those for connection-oriented contexts.</span></span> <span data-ttu-id="1a03d-105">Dans le [*contexte*](/windows/desktop/SecGloss/c-gly)sans connexion d’un datagramme, un serveur ne peut pas déterminer à quel moment le client s’est arrêté ou a arrêté la connexion.</span><span class="sxs-lookup"><span data-stu-id="1a03d-105">In a datagram's connectionless [*context*](/windows/desktop/SecGloss/c-gly), a server cannot determine when the client has shut down or otherwise terminated the connection.</span></span> <span data-ttu-id="1a03d-106">En d’autres termes, aucune notification d’arrêt n’est transmise à partir de l’application de transport vers le serveur, comme cela se produit dans un contexte orienté connexion.</span><span class="sxs-lookup"><span data-stu-id="1a03d-106">In other words, no termination notice is passed from the transport application to the server as would occur in a connection-oriented context.</span></span>

<span data-ttu-id="1a03d-107">Pour utiliser un contexte de datagramme, un client définit l' \_ indicateur d’ISC req \_ Datagram dans son appel à la fonction [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="1a03d-107">To use a datagram context, a client sets the ISC\_REQ\_DATAGRAM flag in its call to the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a03d-108">Le package [Microsoft Kerberos](microsoft-kerberos.md) ne prend pas en charge les contextes de datagramme en mode utilisateur à utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a03d-108">The [Microsoft Kerberos](microsoft-kerberos.md) package does not support datagram contexts in user-to-user mode.</span></span>

 

<span data-ttu-id="1a03d-109">Pour mieux prendre en charge certains modèles, en particulier les RPC de type DCE, les règles suivantes s’appliquent lorsque le client utilise un contexte de datagramme :</span><span class="sxs-lookup"><span data-stu-id="1a03d-109">To better support some models, particularly DCE-style RPC, the following rules apply when the client uses a datagram context:</span></span>

-   <span data-ttu-id="1a03d-110">Le [*package de sécurité*](/windows/desktop/SecGloss/s-gly) ne produit pas d’objet [*BLOB*](/windows/desktop/SecGloss/b-gly) d’authentification (objet binaire volumineux) lors du premier appel à [**InitializeSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="1a03d-110">The [*security package*](/windows/desktop/SecGloss/s-gly) does not produce an authentication [*BLOB*](/windows/desktop/SecGloss/b-gly) (binary large object) on the first call to [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span> <span data-ttu-id="1a03d-111">Toutefois, le client peut utiliser le contexte de sécurité retourné dans un appel à la fonction [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) pour générer une signature pour un message.</span><span class="sxs-lookup"><span data-stu-id="1a03d-111">However, the client can use the returned security context in a call to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a signature for a message.</span></span>
-   <span data-ttu-id="1a03d-112">Le package de sécurité doit autoriser la réinitialisation du contexte à plusieurs heures pour permettre au serveur de supprimer la connexion sans préavis.</span><span class="sxs-lookup"><span data-stu-id="1a03d-112">The security package must allow for the context to be re-established multiple times to allow the server to drop the connection without notice.</span></span> <span data-ttu-id="1a03d-113">Cela implique que toutes les clés utilisées dans les fonctions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) et [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) peuvent être réinitialisées à un [*État*](/windows/desktop/SecGloss/s-gly)cohérent.</span><span class="sxs-lookup"><span data-stu-id="1a03d-113">This implies that any keys used in the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions can be reset to a consistent [*state*](/windows/desktop/SecGloss/s-gly).</span></span>
-   <span data-ttu-id="1a03d-114">Le package de sécurité permet à l’appelant de spécifier des informations de séquence et fournit les informations de séquence du côté du destinataire.</span><span class="sxs-lookup"><span data-stu-id="1a03d-114">The security package allows the caller to specify sequence information, and provides that sequence information at the receiver side.</span></span> <span data-ttu-id="1a03d-115">Cela s’ajoute aux informations de séquence gérées par le package.</span><span class="sxs-lookup"><span data-stu-id="1a03d-115">This is in addition to any sequence information maintained by the package.</span></span>

<span data-ttu-id="1a03d-116">Un package de sécurité définit l' \_ \_ indicateur de datagramme de l’indicateur SECPKG pour indiquer qu’il prend en charge la sémantique du datagramme.</span><span class="sxs-lookup"><span data-stu-id="1a03d-116">A security package sets the SECPKG\_FLAG\_DATAGRAM flag to indicate that it supports datagram semantics.</span></span>

 

 
