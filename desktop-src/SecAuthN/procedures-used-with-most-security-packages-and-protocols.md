---
description: Le modèle SSPI (Security Support Provider Interface) fournit une interface unique pour une application de transport client/serveur utilisant les différents packages de sécurité disponibles sur un ordinateur ou un réseau.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procédures utilisées avec la plupart des packages de sécurité et des protocoles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525852"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a><span data-ttu-id="6b5c3-103">Procédures utilisées avec la plupart des packages de sécurité et des protocoles</span><span class="sxs-lookup"><span data-stu-id="6b5c3-103">Procedures Used with Most Security Packages and Protocols</span></span>

<span data-ttu-id="6b5c3-104">Le modèle SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) fournit une interface unique pour une application de transport client/serveur utilisant les différents [*packages de sécurité*](../secgloss/s-gly.md) disponibles sur un ordinateur ou un réseau.</span><span class="sxs-lookup"><span data-stu-id="6b5c3-104">The [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) model provides a single interface for a client/server transport application using the various [*security packages*](../secgloss/s-gly.md) available on a computer or network.</span></span> <span data-ttu-id="6b5c3-105">SSPI permet à une application d’utiliser un package de sécurité sans avoir à gérer les [*protocoles de sécurité*](../secgloss/s-gly.md) sous-jacents du package.</span><span class="sxs-lookup"><span data-stu-id="6b5c3-105">SSPI allows an application to use a security package without dealing with the underlying [*security protocols*](../secgloss/s-gly.md) of the package.</span></span> <span data-ttu-id="6b5c3-106">En même temps, SSPI permet également aux applications sophistiquées orientées sécurité de tirer parti des fonctionnalités avancées des packages de sécurité spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6b5c3-106">At the same time, SSPI also allows sophisticated, security-aware applications to take advantage of the advanced capabilities of specific security packages.</span></span>

<span data-ttu-id="6b5c3-107">Les applications initialisent SSPI à l’aide des étapes suivantes pour sécuriser une connexion réseau pour la plupart des packages de sécurité :</span><span class="sxs-lookup"><span data-stu-id="6b5c3-107">Applications initialize SSPI using the following steps to secure a network connection for most security packages:</span></span>

-   [<span data-ttu-id="6b5c3-108">Utilisation de SecBufferDesc et SecBuffer</span><span class="sxs-lookup"><span data-stu-id="6b5c3-108">Using SecBufferDesc and SecBuffer</span></span>](using-secbufferdesc-and-secbuffer.md)
-   [<span data-ttu-id="6b5c3-109">Initialisation de SSPI</span><span class="sxs-lookup"><span data-stu-id="6b5c3-109">Initializing SSPI</span></span>](initializing-sspi.md)
-   [<span data-ttu-id="6b5c3-110">Établissement d’une connexion sécurisée avec authentification</span><span class="sxs-lookup"><span data-stu-id="6b5c3-110">Establishing a Secure Connection with Authentication</span></span>](establishing-a-secure-connection-with-authentication.md)
-   [<span data-ttu-id="6b5c3-111">Garantir l’intégrité des communications pendant l’échange de messages</span><span class="sxs-lookup"><span data-stu-id="6b5c3-111">Ensuring Communication Integrity During Message Exchange</span></span>](ensuring-communication-integrity-during-message-exchange.md)
-   [<span data-ttu-id="6b5c3-112">Fin d’une session SSPI</span><span class="sxs-lookup"><span data-stu-id="6b5c3-112">Ending an SSPI Session</span></span>](ending-an-sspi-session.md)

 

 
