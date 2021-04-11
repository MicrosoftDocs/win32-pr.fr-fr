---
description: Dans certains environnements, un utilisateur n’est pas automatiquement averti d’un appel d’offre, par exemple par sonnerie ou par message sur l’écran de l’ordinateur.
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: Accepter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd23d8ca1ed483b23d1b56fe98721b9fc53fb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201346"
---
# <a name="accept"></a><span data-ttu-id="cbeac-103">Accepter</span><span class="sxs-lookup"><span data-stu-id="cbeac-103">Accept</span></span>

<span data-ttu-id="cbeac-104">Dans certains environnements, un utilisateur n’est pas automatiquement averti d’un appel d’offre, par exemple par sonnerie ou par message sur l’écran de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cbeac-104">In some environments, a user is not automatically alerted to an offering call, such as by ringing or by a message on their computer screen.</span></span> <span data-ttu-id="cbeac-105">L’opération d’acceptation commence le processus d’alerte (généralement de sonnerie) et l’opération de [réponse](answer-ovr.md) a lieu après.</span><span class="sxs-lookup"><span data-stu-id="cbeac-105">The accept operation starts the process of alerting (usually ringing), and the [answer](answer-ovr.md) operation takes place afterward.</span></span> <span data-ttu-id="cbeac-106">L’application peut [supprimer](drop-ovr.md) la session, la [Rediriger](redirect-ovr.md) ou l’accepter.</span><span class="sxs-lookup"><span data-stu-id="cbeac-106">The application may [drop](drop-ovr.md) the session, [redirect](redirect-ovr.md) it, or accept it.</span></span>

<span data-ttu-id="cbeac-107">Si le fournisseur de services actuel le prend en charge, l’application a la possibilité d’envoyer des informations utilisateur-utilisateur au moment de l’acceptation.</span><span class="sxs-lookup"><span data-stu-id="cbeac-107">If the current service provider supports it, the application has the option to send user-user information at the time of the accept.</span></span> <span data-ttu-id="cbeac-108">Il n’y a aucune garantie que le réseau remet ces informations au tiers appelant.</span><span class="sxs-lookup"><span data-stu-id="cbeac-108">There is no guarantee that the network will deliver this information to the calling party.</span></span>

<span data-ttu-id="cbeac-109">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.</span><span class="sxs-lookup"><span data-stu-id="cbeac-109">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="cbeac-110">**TAPI 2. x :** Consultez [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span><span class="sxs-lookup"><span data-stu-id="cbeac-110">**TAPI 2.x:** See [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span></span>

 

 
