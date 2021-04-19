---
title: Gestionnaires COM
description: L’objectif des gestionnaires COM est de fournir certains \ 0034 ; intelligent \ 0034 ; code dans l’espace d’adressage du client qui peut optimiser les appels entre un client et un serveur. Les gestionnaires peuvent remplacer certaines interfaces tout en déléguant les autres directement au serveur (via le proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510391"
---
# <a name="com-handlers"></a><span data-ttu-id="86a7a-104">Gestionnaires COM</span><span class="sxs-lookup"><span data-stu-id="86a7a-104">COM Handlers</span></span>

<span data-ttu-id="86a7a-105">L’objectif des gestionnaires COM est de fournir un code « intelligent » dans l’espace d’adressage du client qui peut optimiser les appels entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="86a7a-105">The purpose of COM handlers is to provide some "smart" code in the client address space that can optimize calls between a client and server.</span></span> <span data-ttu-id="86a7a-106">Les gestionnaires peuvent remplacer certaines interfaces tout en déléguant les autres directement au serveur (via le proxy).</span><span class="sxs-lookup"><span data-stu-id="86a7a-106">Handlers can override some interfaces while delegating others directly to the server (through the proxy).</span></span>

<span data-ttu-id="86a7a-107">Il existe deux types de gestionnaires COM :</span><span class="sxs-lookup"><span data-stu-id="86a7a-107">There are two types of COM handlers:</span></span>

-   <span data-ttu-id="86a7a-108">[Le gestionnaire OLE](the-ole-handler.md) est une dll lourde qui fournit des services importants pour la liaison et l’incorporation.</span><span class="sxs-lookup"><span data-stu-id="86a7a-108">[The OLE handler](the-ole-handler.md) is a heavyweight DLL that provides important services for linking and embedding.</span></span> <span data-ttu-id="86a7a-109">Il est généralement créé avant que le serveur ne soit lancé et initialisé afin que le serveur soit activé lorsque l’objet incorporé passe à l’État en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="86a7a-109">It is usually created before the server is launched and is initialized so that the server is activated when the embedded object enters the running state.</span></span>
-   <span data-ttu-id="86a7a-110">[Le gestionnaire léger côté client](the-lightweight-client-side-handler.md) peut être créé à n’importe quel effet, peut être très petit et ne peut pas être créé avant le serveur.</span><span class="sxs-lookup"><span data-stu-id="86a7a-110">[The lightweight client-side handler](the-lightweight-client-side-handler.md) can be created for any purpose, can be very small, and cannot be created before the server.</span></span>

 

 




