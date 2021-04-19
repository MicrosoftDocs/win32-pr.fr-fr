---
title: Détails de l’implémentation DVC
description: Cette section contient des informations sur l’écriture d’un module client de canal virtuel dynamique (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508972"
---
# <a name="dvc-implementation-details"></a><span data-ttu-id="7290f-103">Détails de l’implémentation DVC</span><span class="sxs-lookup"><span data-stu-id="7290f-103">DVC Implementation Details</span></span>

<span data-ttu-id="7290f-104">Cette section contient des informations sur l’écriture d’un module client de canal virtuel dynamique (DVC).</span><span class="sxs-lookup"><span data-stu-id="7290f-104">This section contains information about how to write a dynamic virtual channel (DVC) client module.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7290f-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7290f-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="7290f-106">Écriture d’un module DVC client</span><span class="sxs-lookup"><span data-stu-id="7290f-106">Writing a Client DVC Module</span></span>](writing-a-client-dvc-component.md)
</dt> <dd>

<span data-ttu-id="7290f-107">Pour écrire un module client de canal virtuel dynamique (DVC), vous devez d’abord implémenter et inscrire un plug-in client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="7290f-107">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="7290f-108">Inscription du plug-in DVC</span><span class="sxs-lookup"><span data-stu-id="7290f-108">DVC plug-in registration</span></span>](dvc-plug-in-registration.md)
</dt> <dd>

<span data-ttu-id="7290f-109">Décrit la syntaxe de l’entrée de plug-in de canal virtuel dynamique (DVC) pour le client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="7290f-109">Describes syntax for the dynamic virtual channel (DVC) plug-in entry for the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="7290f-110">Démarrage d’un écouteur DVC</span><span class="sxs-lookup"><span data-stu-id="7290f-110">Starting a DVC Listener</span></span>](starting-a-dvc-listener.md)
</dt> <dd>

<span data-ttu-id="7290f-111">Pour établir une connexion réussie entre deux modules de canal virtuel dynamique (DVC) qui s’exécutent sur le client et le serveur Connexion Bureau à distance (RDC), un écouteur DVC doit être en cours d’exécution et dans un état d’écoute.</span><span class="sxs-lookup"><span data-stu-id="7290f-111">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

</dd> <dt>

[<span data-ttu-id="7290f-112">Acceptation d’une connexion</span><span class="sxs-lookup"><span data-stu-id="7290f-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> <dd>

<span data-ttu-id="7290f-113">À un moment donné, le client de canal virtuel dynamique (DVC) demande une connexion à l’écouteur DVC.</span><span class="sxs-lookup"><span data-stu-id="7290f-113">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span>

</dd> <dt>

[<span data-ttu-id="7290f-114">Écriture de données à l’aide d’un canal DVC</span><span class="sxs-lookup"><span data-stu-id="7290f-114">Writing Data by Using a DVC Channel</span></span>](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

<span data-ttu-id="7290f-115">L’écriture de données de canal à l’aide d’un canal virtuel dynamique (DVC) est symétrique pour le serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance) et le client.</span><span class="sxs-lookup"><span data-stu-id="7290f-115">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span>

</dd> <dt>

[<span data-ttu-id="7290f-116">Test et débogage</span><span class="sxs-lookup"><span data-stu-id="7290f-116">Testing and Debugging</span></span>](testing-and-debugging.md)
</dt> <dd>

<span data-ttu-id="7290f-117">Il existe un écouteur « Echo » implémenté par le client Connexion Bureau à distance (RDC), qui est toujours présent et à l’écoute des connexions entrantes.</span><span class="sxs-lookup"><span data-stu-id="7290f-117">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span>

</dd> <dt>

[<span data-ttu-id="7290f-118">Exemple de plug-in client DVC</span><span class="sxs-lookup"><span data-stu-id="7290f-118">DVC Client Plug-in Example</span></span>](dvc-client-plug-in-example.md)
</dt> <dd>

<span data-ttu-id="7290f-119">Exemple de code C++ qui montre comment créer un plug-in de canal virtuel dynamique (DVC) de client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="7290f-119">C++ code sample that shows how to create a Remote Desktop Connection (RDC) client dynamic virtual channel (DVC) plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="7290f-120">Exemple de module de serveur DVC</span><span class="sxs-lookup"><span data-stu-id="7290f-120">DVC Server Module Example</span></span>](dvc-server-component-example.md)
</dt> <dd>

<span data-ttu-id="7290f-121">Exemple de code C++ qui montre comment créer le module de canal virtuel dynamique côté serveur (DVC).</span><span class="sxs-lookup"><span data-stu-id="7290f-121">C++ code sample that shows how to create the server-side dynamic virtual channel (DVC) module.</span></span>

</dd> </dl>

 

 




