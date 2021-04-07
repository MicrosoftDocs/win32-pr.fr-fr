---
description: Développement de composants en file d’attente
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Développement de composants en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748044"
---
# <a name="developing-queued-components"></a><span data-ttu-id="a15b9-103">Développement de composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="a15b9-103">Developing Queued Components</span></span>

<span data-ttu-id="a15b9-104">Le service COM+ Queued Components requiert que toutes les méthodes d’application contiennent uniquement \[ des \] paramètres in, sans aucune valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a15b9-104">The COM+ queued components service requires all application methods to contain only \[in\] parameters, with no return values.</span></span> <span data-ttu-id="a15b9-105">Étant donné que l’objet serveur n’est pas nécessairement disponible lorsque le client effectue l’appel, les résultats du serveur peuvent être retournés en envoyant un message qui crée un autre objet.</span><span class="sxs-lookup"><span data-stu-id="a15b9-105">Because the server object is not necessarily available when the client makes the call, server results can be returned by sending a message that creates another object.</span></span> <span data-ttu-id="a15b9-106">De cette façon, la communication bidirectionnelle ne se produit pas dans tous les cas, mais uniquement lorsqu’elle est requise, par une série de messages unidirectionnels entre objets.</span><span class="sxs-lookup"><span data-stu-id="a15b9-106">In this way, two-way communication occurs not in every case but only when it is required, by a series of one-way messages between objects.</span></span>

<span data-ttu-id="a15b9-107">Pour utiliser le service de composants en file d’attente COM+, le service de [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) doit déjà être installé.</span><span class="sxs-lookup"><span data-stu-id="a15b9-107">To use the COM+ queued components service, you must have the [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) service already installed.</span></span> <span data-ttu-id="a15b9-108">Message Queuing n’est pas installé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a15b9-108">Message Queuing is not installed automatically.</span></span> <span data-ttu-id="a15b9-109">Vous devez sélectionner les Message Queuing au cours de l’installation du système d’exploitation ou à l’aide d' **Ajout/suppression de programmes**.</span><span class="sxs-lookup"><span data-stu-id="a15b9-109">Message Queuing must be selected during the operating system setup or by using **Add/Remove programs**.</span></span> <span data-ttu-id="a15b9-110">Un certificat de Message Queuing interne est créé automatiquement à l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="a15b9-110">An internal Message Queuing certificate is created automatically at logon.</span></span>

<span data-ttu-id="a15b9-111">Les rubriques décrites dans le tableau suivant fournissent des considérations supplémentaires pour les situations plus spécialisées.</span><span class="sxs-lookup"><span data-stu-id="a15b9-111">The topics described in the following table provide additional considerations for more specialized situations.</span></span>



| <span data-ttu-id="a15b9-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a15b9-112">Topic</span></span>                                                                                           | <span data-ttu-id="a15b9-113">Description</span><span class="sxs-lookup"><span data-stu-id="a15b9-113">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a15b9-114">[Passage d’objets en tant que paramètre](passing-objects-as-parameters.md)s</span><span class="sxs-lookup"><span data-stu-id="a15b9-114">[Passing Objects as Parameter](passing-objects-as-parameters.md)s</span></span><br/>                   | <span data-ttu-id="a15b9-115">Décrit comment passer des objets en tant que \[ \] paramètres in à des composants en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="a15b9-115">Describes how to pass objects as \[in\] parameters to queued components.</span></span><br/>                    |
| [<span data-ttu-id="a15b9-116">Limitations de sécurité en mode groupe de travail</span><span class="sxs-lookup"><span data-stu-id="a15b9-116">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)<br/> | <span data-ttu-id="a15b9-117">Décrit les limitations relatives à l’utilisation de l’authentification Message Queuing en mode groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="a15b9-117">Describes limitations on the use of Message Queuing authentication in workgroup mode.</span></span><br/>       |
| [<span data-ttu-id="a15b9-118">Considérations relatives aux threads</span><span class="sxs-lookup"><span data-stu-id="a15b9-118">Threading Considerations</span></span>](threading-considerations.md)<br/>                             | <span data-ttu-id="a15b9-119">Décrit les problèmes spécifiques liés au passage de pointeurs d’interface d’enregistreur entre les threads.</span><span class="sxs-lookup"><span data-stu-id="a15b9-119">Describes specific concerns related to passing recorder interface pointers between threads.</span></span><br/> |
| [<span data-ttu-id="a15b9-120">Réception d’une réponse</span><span class="sxs-lookup"><span data-stu-id="a15b9-120">Receiving a Response</span></span>](receiving-a-response.md)<br/>                                     | <span data-ttu-id="a15b9-121">Décrit comment construire une réponse à un appel de composant mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="a15b9-121">Describes how to construct a response to a queued component call.</span></span><br/>                           |



 

 

 




