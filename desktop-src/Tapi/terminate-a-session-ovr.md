---
description: L’arrêt de la session peut provenir d’une demande de l’utilisateur, d’une déconnexion distante par l’autre partie ou pour des raisons spécifiques à l’application.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Terminer une session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531424"
---
# <a name="terminate-a-session"></a><span data-ttu-id="08a60-103">Terminer une session</span><span class="sxs-lookup"><span data-stu-id="08a60-103">Terminate a Session</span></span>

<span data-ttu-id="08a60-104">L’arrêt de la session peut provenir d’une demande de l’utilisateur, d’une déconnexion distante par l’autre partie ou pour des raisons spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="08a60-104">Session termination may originate with a user request, remote disconnection by the other party, or for application-specific reasons.</span></span> <span data-ttu-id="08a60-105">Lorsqu’une session est arrêtée, l' [identificateur de session](session-identifier-ovr.md) reste valide jusqu’à ce qu’il soit publié et peut être utilisé pour collecter des données après la connexion.</span><span class="sxs-lookup"><span data-stu-id="08a60-105">When a session is terminated, the [session identifier](session-identifier-ovr.md) remains valid until specifically released and can be used to gather post-connection data.</span></span>

<span data-ttu-id="08a60-106">L’arrêt de la session est terminé en désallouant et en libérant les ressources associées à la session.</span><span class="sxs-lookup"><span data-stu-id="08a60-106">Session termination is completed by deallocating and releasing the resources associated with the session.</span></span> <span data-ttu-id="08a60-107">Si une session est simplement supprimée ou déconnectée, mais que les ressources ne sont pas libérées, le résultat est une fuite de mémoire dans l’application et éventuellement dans le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="08a60-107">If a session is merely dropped or disconnected but resources are not released, the result is a memory leak in the application and possibly in the service provider as well.</span></span>

<span data-ttu-id="08a60-108">**TAPI 2. x :** Consultez [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span><span class="sxs-lookup"><span data-stu-id="08a60-108">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span></span>

<span data-ttu-id="08a60-109">**TAPI 3. x :** Consultez [**ITBasicCallControl ::D éconnecter**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), effectuez une mise en forme com standard sur le pointeur d’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="08a60-109">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), perform a standard COM release on the Call object pointer.</span></span>

 

 
