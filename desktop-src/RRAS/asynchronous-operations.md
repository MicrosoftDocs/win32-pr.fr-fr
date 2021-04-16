---
title: Opérations asynchrones
description: Lorsque RasDial est appelé en tant qu’opération asynchrone, la fonction retourne immédiatement.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db434b7e6d080933e7e21de056f9af5ea7d57dfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380055"
---
# <a name="asynchronous-operations"></a><span data-ttu-id="b35e9-103">Opérations asynchrones</span><span class="sxs-lookup"><span data-stu-id="b35e9-103">Asynchronous Operations</span></span>

<span data-ttu-id="b35e9-104">Lorsque [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) est appelé en tant qu’opération asynchrone, la fonction retourne immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b35e9-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as an asynchronous operation, the function returns immediately.</span></span> <span data-ttu-id="b35e9-105">En mode asynchrone, l’appel de **rasdial** doit spécifier un [Gestionnaire de notification](notification-handlers.md) que le gestionnaire de connexions d’accès à distance utilise pour informer le client chaque fois que l’opération de connexion change d’État ou qu’une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="b35e9-105">In asynchronous mode, the **RasDial** call must specify a [notification handler](notification-handlers.md) that the Remote Access Connection Manager uses to inform the client whenever the connection operation changes states or an error occurs.</span></span>

<span data-ttu-id="b35e9-106">Le gestionnaire de notification peut être une fenêtre pour la réception de messages, ou une fonction de rappel [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)ou [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) .</span><span class="sxs-lookup"><span data-stu-id="b35e9-106">The notification handler can be a window to receive messages, or a [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1), or [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) callback function.</span></span> <span data-ttu-id="b35e9-107">Le gestionnaire de connexions d’accès à distance effectue ses notifications asynchrones dans le contexte du thread qui a effectué l’appel [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .</span><span class="sxs-lookup"><span data-stu-id="b35e9-107">The Remote Access Connection Manager makes its asynchronous notifications in the context of the thread that made the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call.</span></span> <span data-ttu-id="b35e9-108">Pour cette raison, le thread appelant ne doit se terminer que lorsque l’opération de connexion a été correctement établie ou qu’une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="b35e9-108">For this reason, the calling thread must not terminate until the connection operation has been successfully established or an error occurs.</span></span> <span data-ttu-id="b35e9-109">Comme en mode synchrone, l’application cliente peut se terminer en toute sécurité une fois que la connexion a été établie, et elle doit [arrêter l’opération de connexion](disconnecting.md) si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="b35e9-109">As in synchronous mode, the client application can safely terminate once the connection has been established, and it must [shut down the connection operation](disconnecting.md) if an error occurs.</span></span>

 

 




