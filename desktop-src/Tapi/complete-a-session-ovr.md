---
description: Les opérations d’achèvement permettent à une application de spécifier la manière dont elle souhaite gérer une session lorsque des facteurs tels qu’une destination occupée empêchent une connexion normale.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Terminer une session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533613"
---
# <a name="complete-a-session"></a><span data-ttu-id="90554-103">Terminer une session</span><span class="sxs-lookup"><span data-stu-id="90554-103">Complete a Session</span></span>

<span data-ttu-id="90554-104">Les opérations d’achèvement permettent à une application de spécifier la manière dont elle souhaite gérer une session lorsque des facteurs tels qu’une destination occupée empêchent une connexion normale.</span><span class="sxs-lookup"><span data-stu-id="90554-104">Completion operations allow an application to specify how it wants to handle a session when factors such as a busy destination prevent normal connection.</span></span>

<span data-ttu-id="90554-105">Les [ \_ constantes LINECALLCOMPLMODE](./linecallcomplmode--constants.md) définissent les options possibles qu’une application peut avoir, en fonction des fonctionnalités du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="90554-105">The [LINECALLCOMPLMODE\_ Constants](./linecallcomplmode--constants.md) define the possible options an application might have, depending on service provider capabilities.</span></span>

<span data-ttu-id="90554-106">Plusieurs demandes d’achèvement d’appel peuvent être en attente pour une adresse donnée à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="90554-106">Multiple call completion requests might be outstanding for a given address at any one time.</span></span> <span data-ttu-id="90554-107">Pour identifier des demandes individuelles, l’implémentation retourne un [identificateur de saisie semi-automatique](completion-id-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="90554-107">To identify individual requests, the implementation returns a [completion identifier](completion-id-ovr.md).</span></span> <span data-ttu-id="90554-108">L’annulation d’une demande d’achèvement d’appel en cours utilise également cet identificateur d’achèvement d’appel.</span><span class="sxs-lookup"><span data-stu-id="90554-108">Canceling a call completion request in progress also uses this call completion identifier.</span></span>

<span data-ttu-id="90554-109">**TAPI 2. x :** Consultez [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span><span class="sxs-lookup"><span data-stu-id="90554-109">**TAPI 2.x:** See [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span></span>

<span data-ttu-id="90554-110">**TAPI 3. x :** Consultez [**ITBasicCallControl :: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl ::D éconnecter**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="90554-110">**TAPI 3.x:** See [**ITBasicCallControl::Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
