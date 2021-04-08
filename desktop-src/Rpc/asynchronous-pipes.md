---
title: Canaux asynchrones
description: L’utilisation de paramètres de canal avec RPC asynchrone vous permet de transmettre des données de façon incrémentielle, dès qu’elles sont disponibles, sans lier le client et le serveur.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729429"
---
# <a name="asynchronous-pipes"></a><span data-ttu-id="da3cc-103">Canaux asynchrones</span><span class="sxs-lookup"><span data-stu-id="da3cc-103">Asynchronous Pipes</span></span>

<span data-ttu-id="da3cc-104">L’utilisation de paramètres de [canal](/windows/desktop/Midl/pipe) avec RPC asynchrone vous permet de transmettre des données de façon incrémentielle, dès qu’elles sont disponibles, sans lier le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="da3cc-104">Using [pipe](/windows/desktop/Midl/pipe) parameters with asynchronous RPC allows you to transmit data incrementally, as it becomes available, without tying up the client and server.</span></span> <span data-ttu-id="da3cc-105">Cela s’avère particulièrement utile lorsque vous avez une grande quantité de données à transférer, combiné avec un client lent, un serveur lent ou un réseau lent.</span><span class="sxs-lookup"><span data-stu-id="da3cc-105">This is particularly useful when you have a large amount of data to transfer, combined with a slow client, a slow server, or a slow network.</span></span> <span data-ttu-id="da3cc-106">Si vous utilisez un canal dans un appel de fonction asynchrone, il s’agit, par définition, d’un canal asynchrone.</span><span class="sxs-lookup"><span data-stu-id="da3cc-106">If you use a pipe in an asynchronous function call, it is, by definition, an asynchronous pipe.</span></span> <span data-ttu-id="da3cc-107">Les canaux synchrones ne sont pas pris en charge conjointement avec les fonctions asynchrones.</span><span class="sxs-lookup"><span data-stu-id="da3cc-107">Synchronous pipes are not supported in conjunction with asynchronous functions.</span></span>

<span data-ttu-id="da3cc-108">Contrairement aux canaux conventionnels (synchrones) où le serveur gère tous les détails de l’envoi et de la réception des données de canal, les canaux asynchrones sont symétriques.</span><span class="sxs-lookup"><span data-stu-id="da3cc-108">Unlike conventional (synchronous) pipes where the server handles all the details of sending and receiving pipe data, asynchronous pipes are symmetrical.</span></span> <span data-ttu-id="da3cc-109">Autrement dit, le client et le serveur peuvent à la fois pousser et extraire des données via le canal.</span><span class="sxs-lookup"><span data-stu-id="da3cc-109">That is, both the client and the server can push and pull data through the pipe.</span></span>

> [!Note]  
> <span data-ttu-id="da3cc-110">Les paramètres de canal peuvent uniquement être passés par référence.</span><span class="sxs-lookup"><span data-stu-id="da3cc-110">Pipe parameters can only be passed by reference.</span></span> <span data-ttu-id="da3cc-111">Même si le fichier IDL affiche des paramètres de [canal](/windows/desktop/Midl/pipe) passés par valeur, les stubs générés acceptent les paramètres de canal par référence uniquement.</span><span class="sxs-lookup"><span data-stu-id="da3cc-111">Even if the IDL file shows [pipe](/windows/desktop/Midl/pipe) parameters being passed by value, the generated stubs will accept pipe parameters by reference only.</span></span>

 

<span data-ttu-id="da3cc-112">Dans la discussion suivante sur les canaux asynchrones, il est supposé que vous connaissez le constructeur du type de canal.</span><span class="sxs-lookup"><span data-stu-id="da3cc-112">In the following discussion of asynchronous pipes, familiarity with the pipe type constructor is assumed.</span></span> <span data-ttu-id="da3cc-113">Pour plus d’informations sur les procédures de canal décrites dans ces rubriques, consultez [canaux](pipes.md).</span><span class="sxs-lookup"><span data-stu-id="da3cc-113">For more information on the pipe procedures described in these topics, see [Pipes](pipes.md).</span></span>

 

 