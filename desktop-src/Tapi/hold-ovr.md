---
description: L’opération de blocage permet à une seule adresse de gérer plusieurs sessions de communication.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Mise en attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863230"
---
# <a name="hold"></a><span data-ttu-id="411aa-103">Mise en attente</span><span class="sxs-lookup"><span data-stu-id="411aa-103">Hold</span></span>

<span data-ttu-id="411aa-104">L’opération de blocage permet à une seule adresse de gérer plusieurs sessions de communication.</span><span class="sxs-lookup"><span data-stu-id="411aa-104">The hold operation allows a single address to handle multiple communications sessions.</span></span> <span data-ttu-id="411aa-105">Le fait de placer une session sur un blocage forcé libère la ligne/l’adresse de l’utilisateur pour effectuer d’autres appels.</span><span class="sxs-lookup"><span data-stu-id="411aa-105">Placing a session on a hard hold frees the user's line/address to make other calls.</span></span> <span data-ttu-id="411aa-106">En règle générale, un appel en attente ne peut pas être transféré ou inclus dans un appel de conférence, mais un appel de consultation peut.</span><span class="sxs-lookup"><span data-stu-id="411aa-106">A call on hard hold typically cannot be transferred or included in a conference call, but a consultation call can.</span></span> <span data-ttu-id="411aa-107">Les appels de consultation sont initiés à l’aide d’opérations de [Conférence](conference-ovr.md) ou de [transfert](transfer-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="411aa-107">Consultation calls are initiated using [conference](conference-ovr.md) or [transfer](transfer-ovr.md) operations.</span></span>

<span data-ttu-id="411aa-108">Une fois qu’un appel a été correctement mis en attente, l’état de l’appel passe généralement à l’État onHold.</span><span class="sxs-lookup"><span data-stu-id="411aa-108">After a call has been successfully placed on hold, the call state typically transitions to the onhold state.</span></span> <span data-ttu-id="411aa-109">Lorsqu’un appel est en attente, l’application peut recevoir des messages sur les modifications d’état de l’appel en attente.</span><span class="sxs-lookup"><span data-stu-id="411aa-109">While a call is on hold, the application can receive messages about state changes of the held call.</span></span> <span data-ttu-id="411aa-110">Par exemple, si le tiers détenu raccroche, l’état de l’appel peut passer à déconnecté.</span><span class="sxs-lookup"><span data-stu-id="411aa-110">For example, if the held party hangs up, the call state can transition to disconnected.</span></span>

<span data-ttu-id="411aa-111">Dans une situation de pont, l’opération de maintien peut ne pas réellement placer l’appel en attente.</span><span class="sxs-lookup"><span data-stu-id="411aa-111">In a bridged situation, the hold operation may not actually place the call on hold.</span></span> <span data-ttu-id="411aa-112">L’état des autres stations de l’appel peut régir (par exemple, la tentative de « conservation » d’un appel lorsque d’autres stations participantes n’est pas possible); au lieu de cela, l’appel peut simplement être remplacé par l’état inactif alors qu’il reste connecté sur d’autres stations.</span><span class="sxs-lookup"><span data-stu-id="411aa-112">The status of other stations on the call can govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call can simply be changed to the inactive state while it remains connected at other stations.</span></span>

<span data-ttu-id="411aa-113">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.</span><span class="sxs-lookup"><span data-stu-id="411aa-113">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="411aa-114">**TAPI 2. x :** Consultez [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span><span class="sxs-lookup"><span data-stu-id="411aa-114">**TAPI 2.x:** See [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span></span>

<span data-ttu-id="411aa-115">**TAPI 3. x :** Consultez [**ITBasicCallControl :: Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span><span class="sxs-lookup"><span data-stu-id="411aa-115">**TAPI 3.x:** See [**ITBasicCallControl::Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span></span>

 

 
