---
description: Erreurs de Client-Side
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Erreurs de Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513926"
---
# <a name="client-side-errors"></a><span data-ttu-id="222e4-103">Erreurs de Client-Side</span><span class="sxs-lookup"><span data-stu-id="222e4-103">Client-Side Errors</span></span>

<span data-ttu-id="222e4-104">Les défaillances côté client sont gérées d’une manière similaire aux défaillances côté serveur.</span><span class="sxs-lookup"><span data-stu-id="222e4-104">Client-side failures are handled in a way that is similar to server-side failures.</span></span> <span data-ttu-id="222e4-105">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) pouvez déplacer un message vers sa file d’attente de destination si, par exemple, le message ne peut pas être déplacé du client vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="222e4-105">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) can move a message to its destination queue if, for example, the message cannot be moved from client to server.</span></span> <span data-ttu-id="222e4-106">Dans ce cas, le message est déplacé vers la file d’attente de lettres mortes côté client.</span><span class="sxs-lookup"><span data-stu-id="222e4-106">In this case, the message is moved to the client-side dead letter queue.</span></span>

<span data-ttu-id="222e4-107">Le service composants en file d’attente COM+ analyse la file d’attente de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="222e4-107">The COM+ queued components service monitors the dead letter queue.</span></span> <span data-ttu-id="222e4-108">Si des messages ont été déplacés, le service Queued Components crée une instance de la classe exception et appelle [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour demander [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span><span class="sxs-lookup"><span data-stu-id="222e4-108">If messages have been moved, the queued components service creates an instance of the exception class and calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to request [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span></span> <span data-ttu-id="222e4-109">En cas de réussite, le moniteur de file d’attente de lettres mortes appelle [**IPlaybackControl :: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span><span class="sxs-lookup"><span data-stu-id="222e4-109">If this is successful, the dead letter queue monitor invokes [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span></span>

<span data-ttu-id="222e4-110">L’objet peut entreprendre une action pour inverser l’effet d’une transaction antérieure.</span><span class="sxs-lookup"><span data-stu-id="222e4-110">The object can take some action to reverse the effect of a prior transaction.</span></span> <span data-ttu-id="222e4-111">Si la lecture est validée, le message est supprimé de la file d’attente de lettres mortes Xact.</span><span class="sxs-lookup"><span data-stu-id="222e4-111">If the playback commits, the message is removed from the Xact dead letter queue.</span></span> <span data-ttu-id="222e4-112">Si la lecture échoue ou si le CLSID et l’interface requis ne sont pas disponibles, le message reste dans la file d’attente de lettres mortes Xact.</span><span class="sxs-lookup"><span data-stu-id="222e4-112">If the playback fails or the required CLSID and interface are not available, the message remains on the Xact dead letter queue.</span></span>

<span data-ttu-id="222e4-113">Si vous devez intervenir dans le processus décrit ci-dessus ou si vous devez déplacer un message incohérent hors de sa file d’attente Rest finale, utilisez l’utilitaire de déplacement de messages.</span><span class="sxs-lookup"><span data-stu-id="222e4-113">If you need to intervene in the process described above or if you need to move a poison message out of its final resting queue, use the message mover utility.</span></span> <span data-ttu-id="222e4-114">Pour plus d’informations sur l’utilitaire de déplacement de messages, consultez [gestion des erreurs](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="222e4-114">For more information on the message mover utility, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="222e4-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="222e4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="222e4-116">Échecs de Client-Side persistant</span><span class="sxs-lookup"><span data-stu-id="222e4-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)
</dt> <dt>

[<span data-ttu-id="222e4-117">Erreurs côté serveur</span><span class="sxs-lookup"><span data-stu-id="222e4-117">Server-Side Errors</span></span>](server-side-errors.md)
</dt> </dl>

 

 
