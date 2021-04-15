---
description: L’opération de réponse est une réponse classique des applications à une session de communication proposée. En cas de réussite, cette opération entraîne la transition d’une session dans l’état connecté.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Réponse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529223"
---
# <a name="answer"></a><span data-ttu-id="55f37-104">Réponse</span><span class="sxs-lookup"><span data-stu-id="55f37-104">Answer</span></span>

<span data-ttu-id="55f37-105">L’opération de réponse est une réponse classique d’une application à une session de communication proposée.</span><span class="sxs-lookup"><span data-stu-id="55f37-105">The answer operation is an application's typical response to an offered communications session.</span></span> <span data-ttu-id="55f37-106">En cas de réussite, cette opération entraîne la transition d’une session dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="55f37-106">If successful, this operation causes a session to transition into the connected state.</span></span>

<span data-ttu-id="55f37-107">Dans certains environnements de téléphonie (comme RNIS), où les alertes utilisateur sont séparées de l’offre d’appel, l’application a la possibilité d' [accepter](accept-ovr.md) un appel avant de répondre ou de rejeter ([supprimer](drop-ovr.md)) ou de [Rediriger](redirect-ovr.md) l’appel d' *offre* .</span><span class="sxs-lookup"><span data-stu-id="55f37-107">In some telephony environments (like ISDN), where user alerting is separate from call offering, the application has the option to [accept](accept-ovr.md) a call prior to answering or to reject ([drop](drop-ovr.md)) or [redirect](redirect-ovr.md) the *offering* call.</span></span>

<span data-ttu-id="55f37-108">Si une opération de réponse est effectuée pour une nouvelle session lorsqu’une session est déjà active, l’effet de cette opération sur la session active existante dépend des fonctionnalités du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="55f37-108">If an answer operation is performed for a new session when a session is already active, the effect this has on the existing active session depends on the service provider's capabilities.</span></span> <span data-ttu-id="55f37-109">Le premier appel ne peut pas être affecté, il peut être supprimé automatiquement ou placé automatiquement en attente.</span><span class="sxs-lookup"><span data-stu-id="55f37-109">The first call can be unaffected, it can automatically be dropped, or it can automatically be placed on hold.</span></span> <span data-ttu-id="55f37-110">L’interface TAPI enverra les notifications d’événements appropriées concernant les deux appels.</span><span class="sxs-lookup"><span data-stu-id="55f37-110">TAPI will send the appropriate event notifications concerning both calls.</span></span>

<span data-ttu-id="55f37-111">Dans une situation de pont, si un appel est connecté mais se trouve dans l’état actif, il peut être joint à l’aide de l’opération de réponse.</span><span class="sxs-lookup"><span data-stu-id="55f37-111">In a bridged situation, if a call is connected but in the active state, it can be joined using the answer operation.</span></span>

<span data-ttu-id="55f37-112">L’application a la possibilité d’envoyer des informations sur l’utilisateur au moment de la réponse, si le fournisseur de services la prend en charge.</span><span class="sxs-lookup"><span data-stu-id="55f37-112">The application has the option to send user-user information at the time of the answer, if the service provider supports it.</span></span>

<span data-ttu-id="55f37-113">**TAPI 2. x :** Consultez [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="55f37-113">**TAPI 2.x:** See [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="55f37-114">**TAPI 3. x :** Consultez [**ITBasicCallControl :: Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span><span class="sxs-lookup"><span data-stu-id="55f37-114">**TAPI 3.x:** See [**ITBasicCallControl::Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span></span>

 

 
