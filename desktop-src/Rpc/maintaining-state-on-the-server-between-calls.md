---
title: Conservation de l’État sur le serveur entre les appels
description: Il est souvent nécessaire de conserver l’État sur le serveur entre les appels RPC séparés \ 8212 ; l’utilisation de handles de contexte est la meilleure façon de le faire. Quelques mots sur la façon dont les handles de contexte fonctionnent en interne vous aident à comprendre le fonctionnement optimal des handles de contexte.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- Appel de procédure distante RPC, meilleures pratiques, maintien de l’état entre les appels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670990"
---
# <a name="maintaining-state-on-the-server-between-calls"></a><span data-ttu-id="52a7e-105">Conservation de l’État sur le serveur entre les appels</span><span class="sxs-lookup"><span data-stu-id="52a7e-105">Maintaining State on the Server Between Calls</span></span>

<span data-ttu-id="52a7e-106">Il est souvent nécessaire de conserver l’État sur le serveur entre des appels RPC distincts, l’utilisation de handles de contexte est la meilleure façon de le faire.</span><span class="sxs-lookup"><span data-stu-id="52a7e-106">It is often necessary to maintain state on the server between separate RPC calls—using context handles is the best way to do so.</span></span> <span data-ttu-id="52a7e-107">Quelques mots sur la façon dont les handles de contexte fonctionnent en interne vous aident à comprendre le fonctionnement optimal des handles de contexte.</span><span class="sxs-lookup"><span data-stu-id="52a7e-107">A few words about how context handles operate internally helps in understanding when context handles work best.</span></span>

<span data-ttu-id="52a7e-108">Le client ne reçoit jamais l’État conservé sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="52a7e-108">The client never receives the state kept on the server.</span></span> <span data-ttu-id="52a7e-109">Le plus souvent, l’État sur le serveur est un pointeur vers un bloc de mémoire, et le client ne dispose d’aucune information le concernant.</span><span class="sxs-lookup"><span data-stu-id="52a7e-109">Most often the state on the server is a pointer to a memory block, and the client has no information about it.</span></span> <span data-ttu-id="52a7e-110">Tout le client reçoit un grand nombre unique, avec d’autres informations qui lui sont associées, que le serveur envoie au client et qui représente le descripteur de contexte dans toutes les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="52a7e-110">All the client receives is a large unique number, with other information associated with it, that the server sends to the client and which represents the context handle in all subsequent operations.</span></span> <span data-ttu-id="52a7e-111">Chaque fois que le client fait référence à un descripteur ouvert, il envoie le grand nombre qu’il a reçu du serveur lors de l’ouverture de ce descripteur de contexte.</span><span class="sxs-lookup"><span data-stu-id="52a7e-111">Whenever the client refers to an opened handle, it sends the large number it received from the server when that context handle was opened.</span></span>

<span data-ttu-id="52a7e-112">Le serveur effectue le suivi de tous les nombres importants qu’il envoie à un client.</span><span class="sxs-lookup"><span data-stu-id="52a7e-112">The server keeps track of all large numbers it sends to a client.</span></span> <span data-ttu-id="52a7e-113">Lorsque le serveur reçoit un nombre élevé représentant un handle de contexte, il recherche le nombre dans la collection de handles de contexte valides et en suspens pour ce client et recherche le contexte côté serveur correspondant à un grand nombre donné.</span><span class="sxs-lookup"><span data-stu-id="52a7e-113">When the server receives a large number representing a context handle, it looks up the number in the collection of valid, outstanding context handles for that client, and finds the server-side context corresponding to a given large number.</span></span> <span data-ttu-id="52a7e-114">Cette valeur est transmise à la routine du serveur.</span><span class="sxs-lookup"><span data-stu-id="52a7e-114">This is passed to the server routine.</span></span> <span data-ttu-id="52a7e-115">Si le grand nombre est introuvable, une \_ \_ exception d' \_ incompatibilité de contexte SS RPC X \_ est déclenchée et propagée au client.</span><span class="sxs-lookup"><span data-stu-id="52a7e-115">If the large number is not found, an RPC\_X\_SS\_CONTEXT\_MISMATCH exception is raised and propagated to the client.</span></span>

<span data-ttu-id="52a7e-116">Les rouleaux de cette conception sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="52a7e-116">The corollaries of this design are as follows:</span></span>

-   <span data-ttu-id="52a7e-117">Un handle de contexte est valide uniquement dans le contexte de la session client/serveur existante.</span><span class="sxs-lookup"><span data-stu-id="52a7e-117">A context handle is valid only in the context of the existing client/server session.</span></span> <span data-ttu-id="52a7e-118">Elle ne peut pas être transmise à un autre client.</span><span class="sxs-lookup"><span data-stu-id="52a7e-118">It cannot be passed to another client.</span></span>
-   <span data-ttu-id="52a7e-119">Un descripteur de contexte devient non valide si le serveur est redémarré ou perd sa connexion au client.</span><span class="sxs-lookup"><span data-stu-id="52a7e-119">A context handle becomes invalid if the server is rebooted, or otherwise loses its connection to the client.</span></span>
-   <span data-ttu-id="52a7e-120">Le client ne peut pas interpréter ce que le handle de contexte représente sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="52a7e-120">The client cannot interpret what the context handle represents on the server.</span></span> <span data-ttu-id="52a7e-121">Pour un client, tous les handles de contexte sont simplement des nombres importants.</span><span class="sxs-lookup"><span data-stu-id="52a7e-121">To a client, all context handles are simply large numbers.</span></span>

<span data-ttu-id="52a7e-122">En cas de défaillance du client, le serveur recevra une notification et nettoiera ses descripteurs de contexte à l’aide du mécanisme d’exécution.</span><span class="sxs-lookup"><span data-stu-id="52a7e-122">If the client fails, the server will get a notification and will clean up its context handles using the run-down mechanism.</span></span>

 

 




