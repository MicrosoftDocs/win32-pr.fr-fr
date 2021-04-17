---
description: Le service de composants en file d’attente COM+ améliore le modèle de programmation COM en fournissant un environnement dans lequel un composant peut être appelé de façon synchrone (en temps réel) ou asynchrone (en file d’attente).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Architecture des composants en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104561736"
---
# <a name="queued-components-architecture"></a><span data-ttu-id="97f1a-103">Architecture des composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="97f1a-103">Queued Components Architecture</span></span>

<span data-ttu-id="97f1a-104">Le service de composants en file d’attente COM+ améliore le modèle de programmation COM en fournissant un environnement dans lequel un composant peut être appelé de façon synchrone (en temps réel) ou asynchrone (en file d’attente).</span><span class="sxs-lookup"><span data-stu-id="97f1a-104">The COM+ queued components service enhances the COM programming model by providing an environment in which a component can be invoked either synchronously (real-time) or asynchronously (queued).</span></span> <span data-ttu-id="97f1a-105">Un composant n’a pas besoin de savoir s’il est utilisé dans un contexte en temps réel ou en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="97f1a-105">A component need not be aware of whether it is employed in a real-time or a queued context.</span></span>

<span data-ttu-id="97f1a-106">Les applications de messagerie sont similaires aux transactions par courrier électronique entre les programmes.</span><span class="sxs-lookup"><span data-stu-id="97f1a-106">Messaging applications are like email transactions between programs.</span></span> <span data-ttu-id="97f1a-107">Le demandeur envoie un message au serveur ; Lorsque le serveur s’y trouve, le message est traité.</span><span class="sxs-lookup"><span data-stu-id="97f1a-107">The requester sends a message to the server; when the server gets to it, the message is processed.</span></span> <span data-ttu-id="97f1a-108">À l’instar de la messagerie électronique, un système de messagerie doit gérer les détails du réseau et s’assurer que le message est déplacé du client vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="97f1a-108">Like email, a messaging system must handle the network details and ensure that the message moves from the client to the server.</span></span> <span data-ttu-id="97f1a-109">Dans l’infrastructure des composants en file d’attente, Message Queuing en est responsable.</span><span class="sxs-lookup"><span data-stu-id="97f1a-109">In the queued components framework, Message Queuing is responsible for this.</span></span>

<span data-ttu-id="97f1a-110">Le service COM+ Queued Components se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="97f1a-110">The COM+ queued components service consists of the following parts:</span></span>

-   <span data-ttu-id="97f1a-111">Enregistreur (pour le client ou le côté envoi)</span><span class="sxs-lookup"><span data-stu-id="97f1a-111">Recorder (for the client or send side)</span></span>
-   <span data-ttu-id="97f1a-112">Écouteur (pour le serveur ou le côté réception)</span><span class="sxs-lookup"><span data-stu-id="97f1a-112">Listener (for the server or receive side)</span></span>
-   <span data-ttu-id="97f1a-113">Player (pour le serveur ou le côté réception)</span><span class="sxs-lookup"><span data-stu-id="97f1a-113">Player (for the server or receive side)</span></span>

![Diagramme qui montre le chemin d’accès du client au serveur : client, enregistreur, file d’attente, écouteur, lecteur, serveur.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a><span data-ttu-id="97f1a-115">Enregistreur</span><span class="sxs-lookup"><span data-stu-id="97f1a-115">The Recorder</span></span>

<span data-ttu-id="97f1a-116">Dans un scénario de composants en file d’attente standard, le client appelle un composant mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="97f1a-116">In a typical queued components scenario, the client calls a queued component.</span></span> <span data-ttu-id="97f1a-117">L’appel est fait à l’enregistreur des composants en file d’attente, qui le place dans le cadre d’un message sur le serveur et le place dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="97f1a-117">The call is made to the queued components recorder, which packages it as part of a message to the server and puts it in a queue.</span></span> <span data-ttu-id="97f1a-118">L’enregistreur marshale le contexte de sécurité du client dans le message et enregistre tous les appels de méthode du client.</span><span class="sxs-lookup"><span data-stu-id="97f1a-118">The recorder marshals the client's security context into the message and records all of the client's method calls.</span></span> <span data-ttu-id="97f1a-119">Dans son rôle en tant que proxy pour le composant serveur, l’enregistreur sélectionne les interfaces à partir des interfaces de mise en file d’attente dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="97f1a-119">In its role as proxy for the server component, the recorder selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

<span data-ttu-id="97f1a-120">Une représentation de l’enregistrement est envoyée à Message Queuing sous la forme d’un message à envoyer à un serveur.</span><span class="sxs-lookup"><span data-stu-id="97f1a-120">A representation of the recording is sent to Message Queuing as a message to be sent to a server.</span></span> <span data-ttu-id="97f1a-121">Lorsque le paramètre d’attribut de transaction du composant en file d’attente est obligatoire ou pris en charge, Message Queuing accepte la remise du message uniquement si la transaction côté client est validée et que la file d’attente Message Queuing est transactionnelle, ce qui correspond à la valeur par défaut normalement établie.</span><span class="sxs-lookup"><span data-stu-id="97f1a-121">When the queued component has the transaction attribute setting of Required or Supported, Message Queuing accepts delivery of the message only if the client-side transaction commits and the Message Queuing queue is transactional, which is the default normally established.</span></span> <span data-ttu-id="97f1a-122">Lorsque le paramètre d’attribut de transaction requiert New, Message Queuing peut accepter le message même si la transaction côté client est abandonnée.</span><span class="sxs-lookup"><span data-stu-id="97f1a-122">When the transaction attribute setting is Requires New, Message Queuing can accept the message even if the client-side transaction aborts.</span></span> <span data-ttu-id="97f1a-123">Pour plus d’informations sur les transactions, consultez [Message Queuing transactionnelles](transactional-message-queuing.md).</span><span class="sxs-lookup"><span data-stu-id="97f1a-123">For more information on transactions, see [Transactional Message Queuing](transactional-message-queuing.md).</span></span>

## <a name="the-listener"></a><span data-ttu-id="97f1a-124">L’écouteur</span><span class="sxs-lookup"><span data-stu-id="97f1a-124">The Listener</span></span>

<span data-ttu-id="97f1a-125">L’écouteur de composants en file d’attente récupère le message de la file d’attente et le transmet au lecteur des composants en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="97f1a-125">The queued components listener retrieves the message from the queue and passes it to the queued components player.</span></span>

## <a name="the-player"></a><span data-ttu-id="97f1a-126">Le lecteur</span><span class="sxs-lookup"><span data-stu-id="97f1a-126">The Player</span></span>

<span data-ttu-id="97f1a-127">Le lecteur démarshale le contexte de sécurité du client côté serveur, puis appelle le composant serveur et effectue les mêmes appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="97f1a-127">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="97f1a-128">Les appels de méthode ne sont pas lus par le joueur jusqu’à ce que le composant client se termine et que la transaction qui a enregistré la méthode appelle valids.</span><span class="sxs-lookup"><span data-stu-id="97f1a-128">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

## <a name="the-message-mover"></a><span data-ttu-id="97f1a-129">Le message Mover</span><span class="sxs-lookup"><span data-stu-id="97f1a-129">The Message Mover</span></span>

<span data-ttu-id="97f1a-130">Le gestionnaire de messages des composants en file d’attente est un utilitaire qui déplace tous les messages d’échec Message Queuing d’une file d’attente vers une autre, afin qu’ils puissent être retentés.</span><span class="sxs-lookup"><span data-stu-id="97f1a-130">The queued components message mover is a utility that moves all failed Message Queuing messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="97f1a-131">L’utilitaire de déplacement de messages est un objet Automation qui peut être appelé à l’aide d’un script VBScript. Pour plus d’informations, consultez [gestion des erreurs](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="97f1a-131">The message mover utility is an Automation object that can be invoked with a VBScript; for more information, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

 

 



