---
description: Concepts des composants en file d’attente COM+
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Concepts des composants en file d’attente COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545769"
---
# <a name="com-queued-components-concepts"></a><span data-ttu-id="012a6-103">Concepts des composants en file d’attente COM+</span><span class="sxs-lookup"><span data-stu-id="012a6-103">COM+ Queued Components Concepts</span></span>

<span data-ttu-id="012a6-104">En fonction des services de [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) , le service de composants en file d’attente com+ offre un moyen simple d’appeler et d’exécuter des composants de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="012a6-104">Based on [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) services, the COM+ queued components service provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="012a6-105">Le traitement peut se produire sans tenir compte de la disponibilité ou de l’accessibilité de l’expéditeur ou du destinataire.</span><span class="sxs-lookup"><span data-stu-id="012a6-105">Processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

<span data-ttu-id="012a6-106">En termes COM, une *file d’attente* est une zone de stockage qui enregistre les messages en vue d’une récupération ultérieure.</span><span class="sxs-lookup"><span data-stu-id="012a6-106">In COM terms, a *queue* is a storage area that saves messages for later retrieval.</span></span> <span data-ttu-id="012a6-107">La mise en file d’attente fournit un mécanisme de communication sans connexion.</span><span class="sxs-lookup"><span data-stu-id="012a6-107">Queuing provides a mechanism for connectionless communication.</span></span> <span data-ttu-id="012a6-108">Autrement dit, l’expéditeur et le destinataire ne sont pas connectés directement et communiquent uniquement par le biais de files d’attente.</span><span class="sxs-lookup"><span data-stu-id="012a6-108">That is, the sender and receiver are not connected directly and communicate only through queues.</span></span> <span data-ttu-id="012a6-109">La mise en file d’attente permet de conserver les informations jusqu’à ce que le récepteur soit prêt à l’obtenir.</span><span class="sxs-lookup"><span data-stu-id="012a6-109">Queuing provides a way to hold the information until the receiver is ready to obtain it.</span></span> <span data-ttu-id="012a6-110">L’expéditeur et le destinataire communiquent indirectement afin que chacun puisse fonctionner indépendamment, ce qui n’est pas affecté par l’autre.</span><span class="sxs-lookup"><span data-stu-id="012a6-110">The sender and receiver are indirectly communicating so that each can operate independently, unaffected by the other.</span></span>

<span data-ttu-id="012a6-111">Dans le passé, une connaissance approfondie du marshaling était nécessaire pour mettre en file d’attente, envoyer et recevoir des messages asynchrones.</span><span class="sxs-lookup"><span data-stu-id="012a6-111">In the past, an in-depth knowledge of marshaling was necessary to queue, send, and receive asynchronous messages.</span></span> <span data-ttu-id="012a6-112">Désormais, à l’aide d’appels de méthode facilement compréhensibles et utilisés par les développeurs de composants, le service de composants en file d’attente COM+ marshale automatiquement les données sous la forme d’un message Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="012a6-112">Now, using method calls that are easily understood and used by component developers, the COM+ queued components service automatically marshals data in the form of a Message Queuing message.</span></span> <span data-ttu-id="012a6-113">Et étant donné que le service Queued Components offre une prise en charge intégrée des transactions, un état incohérent ne peut pas compromettre les données en cas de défaillance du serveur.</span><span class="sxs-lookup"><span data-stu-id="012a6-113">And because the queued components service offers built-in support for transactions, an inconsistent state cannot compromise data if a server failure occurs.</span></span>

<span data-ttu-id="012a6-114">Les rubriques suivantes de cette section contiennent des informations générales sur la conception et l’écriture de composants en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="012a6-114">The following topics in this section contain background information about designing and writing queued components.</span></span>



| <span data-ttu-id="012a6-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="012a6-115">Topic</span></span>                                                                           | <span data-ttu-id="012a6-116">Description</span><span class="sxs-lookup"><span data-stu-id="012a6-116">Description</span></span>                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="012a6-117">Avantages du traitement en file d’attente</span><span class="sxs-lookup"><span data-stu-id="012a6-117">Benefits of Queued Processing</span></span>](benefits-of-queued-processing.md)<br/>   | <span data-ttu-id="012a6-118">Décrit les avantages de la programmation avec des composants en file d’attente COM+.</span><span class="sxs-lookup"><span data-stu-id="012a6-118">Describes the benefits of programming with COM+ queued components.</span></span><br/>                                         |
| [<span data-ttu-id="012a6-119">Architecture des composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="012a6-119">Queued Components Architecture</span></span>](queued-components-architecture.md)<br/> | <span data-ttu-id="012a6-120">Décrit l’architecture du service COM+ Queued Components.</span><span class="sxs-lookup"><span data-stu-id="012a6-120">Describes the architecture of the COM+ queued components service.</span></span><br/>                                          |
| [<span data-ttu-id="012a6-121">Message Queuing transactionnel</span><span class="sxs-lookup"><span data-stu-id="012a6-121">Transactional Message Queuing</span></span>](transactional-message-queuing.md)<br/>   | <span data-ttu-id="012a6-122">Décrit comment les transactions sont gérées par le service de composants en file d’attente COM+.</span><span class="sxs-lookup"><span data-stu-id="012a6-122">Describes how transactions are handled by the COM+ queued components service.</span></span><br/>                              |
| [<span data-ttu-id="012a6-123">Sécurité des composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="012a6-123">Queued Components Security</span></span>](queued-components-security.md)<br/>         | <span data-ttu-id="012a6-124">Décrit les options de stratégie pour l’authentification des messages du client et leurs implications.</span><span class="sxs-lookup"><span data-stu-id="012a6-124">Describes the policy options for authentication of client messages and their implications.</span></span><br/>                 |
| [<span data-ttu-id="012a6-125">Développement de composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="012a6-125">Developing Queued Components</span></span>](developing-queued-components.md)<br/>     | <span data-ttu-id="012a6-126">Décrit les considérations relatives à la programmation lors de l’écriture de composants en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="012a6-126">Describes programming considerations when writing queuable components.</span></span><br/>                                     |
| [<span data-ttu-id="012a6-127">Erreurs de composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="012a6-127">Queued Components Errors</span></span>](queued-components-errors.md)<br/>             | <span data-ttu-id="012a6-128">Décrit les types d’erreurs les plus courants que vous pouvez rencontrer lors de l’utilisation du service de composants en file d’attente COM+.</span><span class="sxs-lookup"><span data-stu-id="012a6-128">Describes the most common types of errors you may encounter when using the COM+ queued components service.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="012a6-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="012a6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="012a6-130">Tâches des composants COM+ en file d’attente</span><span class="sxs-lookup"><span data-stu-id="012a6-130">COM+ Queued Components Tasks</span></span>](com--queued-components-tasks.md)
</dt> </dl>

 

 




