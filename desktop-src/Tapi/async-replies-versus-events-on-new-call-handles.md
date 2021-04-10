---
description: TSPI comprend un certain nombre d’opérations qui démarrent la durée de vie d’un handle d’appel.
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: Réponses Async et événements sur les nouveaux handles d’appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866602"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a><span data-ttu-id="01a8b-103">Réponses Async et événements sur les nouveaux handles d’appel</span><span class="sxs-lookup"><span data-stu-id="01a8b-103">Async Replies versus Events on New Call Handles</span></span>

<span data-ttu-id="01a8b-104">TSPI comprend un certain nombre d’opérations qui démarrent la durée de vie d’un handle d’appel.</span><span class="sxs-lookup"><span data-stu-id="01a8b-104">TSPI includes a number of operations that start the lifetime of a call handle.</span></span> <span data-ttu-id="01a8b-105">Si le fournisseur de services retourne une réussite pour une telle opération, il doit remplir le handle opaque de type **HDRVCALL**, qu’il utilise pour le nouvel appel avant qu’il ne soit retourné.</span><span class="sxs-lookup"><span data-stu-id="01a8b-105">If the service provider returns SUCCESS for such an operation, it must fill in the opaque handle of type **HDRVCALL**, which it uses for the new call before it returns.</span></span> <span data-ttu-id="01a8b-106">L’interface TAPI n’effectue jamais d’opérations sur l’appel avant la réception de la [*\_ procédure d’achèvement*](/windows/win32/api/tspi/nc-tspi-async_completion) correspondante.</span><span class="sxs-lookup"><span data-stu-id="01a8b-106">TAPI never performs operations on the call before the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) has been received.</span></span> <span data-ttu-id="01a8b-107">Si le fournisseur de services retourne un échec, le descripteur devient automatiquement non valide (autrement dit, sans [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span><span class="sxs-lookup"><span data-stu-id="01a8b-107">If the service provider returns FAILURE, the handle automatically becomes invalid (that is, without [**TSPI\_lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span></span> <span data-ttu-id="01a8b-108">En effet, l’interface TAPI traite le descripteur comme « pas encore valide » jusqu’à la fin asynchrone.</span><span class="sxs-lookup"><span data-stu-id="01a8b-108">In effect, TAPI treats the handle as "not yet valid" until the asynchronous completion.</span></span>

<span data-ttu-id="01a8b-109">Le fournisseur de services doit également traiter le descripteur comme « pas encore valide » tant que la [*\_ procédure d’achèvement*](/windows/win32/api/tspi/nc-tspi-async_completion) correspondante n’a pas été reçue.</span><span class="sxs-lookup"><span data-stu-id="01a8b-109">The service provider must also treat the handle as "not yet valid" until after the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) is received.</span></span> <span data-ttu-id="01a8b-110">En d’autres termes, il ne doit pas émettre de fonctions d' [*\_ événement de ligne*](/windows/win32/api/tspi/nc-tspi-lineevent) pour le nouvel appel ou l’inclure dans le nombre d’appels dans les messages ou les structures de données d’État pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="01a8b-110">In other words, it must not issue any [*Line\_Event*](/windows/win32/api/tspi/nc-tspi-lineevent) functions for the new call or include it in call counts in messages or status data structures for the line.</span></span>

<span data-ttu-id="01a8b-111">Le niveau TAPI est également conforme à ces restrictions de cycle de vie. un nouveau descripteur d’appel n’est pas retourné ou valide jusqu’au message de [**\_ réponse**](./line-reply.md) de la ligne correspondante, et aucun événement pour le nouvel appel n’est remis à l’application tant que le message de réponse de ligne n’a pas été envoyé \_ .</span><span class="sxs-lookup"><span data-stu-id="01a8b-111">The TAPI level also conforms to these life cycle restrictions; a new call handle is not returned or valid until the matching [**LINE\_REPLY**](./line-reply.md) message, and no events for the new call are delivered to the application until after the LINE\_REPLY message.</span></span>

<span data-ttu-id="01a8b-112">Les opérations TSPI auxquelles ce principe de « durée de vie de départ » s’applique sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="01a8b-112">The TSPI operations to which this "start lifetime" principle applies are the following:</span></span>

-   [<span data-ttu-id="01a8b-113">**TSPI \_ lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="01a8b-113">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="01a8b-114">**TSPI \_ lineForward**</span><span class="sxs-lookup"><span data-stu-id="01a8b-114">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="01a8b-115">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="01a8b-115">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="01a8b-116">**TSPI \_ linePickup**</span><span class="sxs-lookup"><span data-stu-id="01a8b-116">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="01a8b-117">**TSPI \_ linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="01a8b-117">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="01a8b-118">**TSPI \_ lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="01a8b-118">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="01a8b-119">**TSPI \_ lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="01a8b-119">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="01a8b-120">**TSPI \_ lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="01a8b-120">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
