---
description: La redirection de session permet à une application de dévier une session proposée vers une autre adresse sans répondre à l’appel.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Rediriger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760809"
---
# <a name="redirect"></a><span data-ttu-id="1a866-103">Rediriger</span><span class="sxs-lookup"><span data-stu-id="1a866-103">Redirect</span></span>

<span data-ttu-id="1a866-104">La redirection de session permet à une application de dévier une session proposée vers une autre adresse sans répondre à l’appel.</span><span class="sxs-lookup"><span data-stu-id="1a866-104">Session redirection allows an application to deflect an offered session to another address without answering the call.</span></span> <span data-ttu-id="1a866-105">L’application peut effectuer une redirection appel par appel.</span><span class="sxs-lookup"><span data-stu-id="1a866-105">The application can do redirection on a call-by-call basis.</span></span> <span data-ttu-id="1a866-106">Par exemple, une application peut permettre à un utilisateur de spécifier des redirections différentes en fonction des informations sur l’ID de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="1a866-106">For example, an application might allow a user to specify different redirections based on caller ID information.</span></span> <span data-ttu-id="1a866-107">Une fois qu’un appel a été redirigé avec succès, l’état passe généralement à inactif et les ressources associées doivent être libérées.</span><span class="sxs-lookup"><span data-stu-id="1a866-107">After a call has been successfully redirected, the state typically transitions to idle and associated resources must be released.</span></span>

<span data-ttu-id="1a866-108">La redirection diffère [par rapport à](forward-ovr.md) ce qu’une fois que le transfert a été configuré, l’opération est effectuée par l’interface TAPI, le fournisseur de services ou le commutateur sans intervention supplémentaire de l’application.</span><span class="sxs-lookup"><span data-stu-id="1a866-108">Redirect differs from [forward](forward-ovr.md) in that once forwarding has been set up, the operation is performed by TAPI, the service provider, or the switch without further involvement of the application.</span></span> <span data-ttu-id="1a866-109">La redirection diffère du [transfert](transfer-ovr.md) dans le fait que la redirection ne nécessite pas de réponse préalable à l’appel.</span><span class="sxs-lookup"><span data-stu-id="1a866-109">Redirect differs from [transfer](transfer-ovr.md) in that redirect does not require answering the call first.</span></span>

<span data-ttu-id="1a866-110">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.</span><span class="sxs-lookup"><span data-stu-id="1a866-110">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="1a866-111">**TAPI 2. x :** Consultez [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span><span class="sxs-lookup"><span data-stu-id="1a866-111">**TAPI 2.x:** See [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span></span>

 

 
