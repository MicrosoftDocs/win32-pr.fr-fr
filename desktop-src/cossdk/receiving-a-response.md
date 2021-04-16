---
description: Réception d’une réponse
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: Réception d’une réponse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9e05ec392b7db828ad1efd1360c4d4fb232210
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524180"
---
# <a name="receiving-a-response"></a><span data-ttu-id="0dc53-103">Réception d’une réponse</span><span class="sxs-lookup"><span data-stu-id="0dc53-103">Receiving a Response</span></span>

<span data-ttu-id="0dc53-104">Étant donné que les composants mis en file d’attente sont conçus pour fonctionner de manière asynchrone, les applications clientes ne doivent pas se bloquer en attendant une réponse d’une demande en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="0dc53-104">Because queued components are designed to work asynchronously, client applications should not block while waiting for a response from a queued request.</span></span> <span data-ttu-id="0dc53-105">Néanmoins, il est souvent utile pour l’application cliente ou une application associée sur l’ordinateur client de recevoir une réponse.</span><span class="sxs-lookup"><span data-stu-id="0dc53-105">Nevertheless, it is often useful for the client application or a related application on the client machine to receive a response eventually.</span></span> <span data-ttu-id="0dc53-106">Par exemple, un client peut vouloir être averti lorsqu’une transaction demandée s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0dc53-106">For example, a client may want to be notified when a requested transaction has been completed successfully.</span></span>

<span data-ttu-id="0dc53-107">Un composant mis en file d’attente peut renvoyer une réponse de façon asynchrone à son appelant de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="0dc53-107">There are a variety of ways for a queued component to send a response back to its caller asynchronously.</span></span> <span data-ttu-id="0dc53-108">Par exemple, il peut envoyer un message électronique.</span><span class="sxs-lookup"><span data-stu-id="0dc53-108">For example, it could send an email.</span></span> <span data-ttu-id="0dc53-109">Le serveur peut également publier des événements faiblement couplés auxquels le client peut s’abonner.</span><span class="sxs-lookup"><span data-stu-id="0dc53-109">Alternatively, the server could publish loosely coupled events to which the client could subscribe.</span></span>

<span data-ttu-id="0dc53-110">Une autre façon pour un client d’obtenir une réponse à partir d’un composant mis en file d’attente qui s’exécute sur un serveur est que le client passe la méthode appelée à un objet de notification.</span><span class="sxs-lookup"><span data-stu-id="0dc53-110">Another way for a client to obtain a response from a queued component that runs on a server is for the client to pass the called method a notification object.</span></span> <span data-ttu-id="0dc53-111">Un objet de notification est une instance d’un composant mis en file d’attente qui s’exécute sur le client.</span><span class="sxs-lookup"><span data-stu-id="0dc53-111">A notification object is an instance of a queued component that runs on the client.</span></span> <span data-ttu-id="0dc53-112">Un tel objet de notification peut être assez simple, contenant uniquement un entier qui est utilisé pour représenter une valeur d’erreur, ou il peut être assez complexe, contenant toutes les informations nécessaires à la restauration d’une transaction sur le client.</span><span class="sxs-lookup"><span data-stu-id="0dc53-112">Such a notification object might be quite simple, containing only an integer that is used to represent an error value, or it might be quite complex, containing all the information necessary to roll back a transaction on the client.</span></span> <span data-ttu-id="0dc53-113">Dans les deux cas, le client appelant transmet un objet de notification en tant que paramètre d’entrée lorsqu’il désire une réponse d’un composant en file d’attente qui s’exécute sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="0dc53-113">In either case, the calling client passes a notification object as an input parameter whenever it desires a response from a queued component that runs on a server.</span></span> <span data-ttu-id="0dc53-114">Étant donné que l’objet de notification est mis en file d’attente, le serveur peut appeler sur ses méthodes pour modifier son état, qui peut ensuite être lu par le client.</span><span class="sxs-lookup"><span data-stu-id="0dc53-114">Because the notification object is queued, the server can call on its methods to alter its state, which can subsequently be read out by the client.</span></span> <span data-ttu-id="0dc53-115">Dans ce scénario, le service COM+ Queued Components est utilisé à la fois sur le client et sur le serveur pour autoriser les communications asynchrones dans les deux sens.</span><span class="sxs-lookup"><span data-stu-id="0dc53-115">In this scenario, the COM+ queued components service is used on both the client and the server to allow asynchronous communication in both directions.</span></span>

 

 



