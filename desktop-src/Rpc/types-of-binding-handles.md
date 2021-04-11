---
title: Types de handles de liaison
description: Les handles de liaison peuvent être automatiques, implicites ou explicites.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029572"
---
# <a name="types-of-binding-handles"></a><span data-ttu-id="2374d-103">Types de handles de liaison</span><span class="sxs-lookup"><span data-stu-id="2374d-103">Types of Binding Handles</span></span>

<span data-ttu-id="2374d-104">Les handles de liaison peuvent être automatiques, implicites ou explicites.</span><span class="sxs-lookup"><span data-stu-id="2374d-104">Binding handles can be automatic, implicit, or explicit.</span></span> <span data-ttu-id="2374d-105">Elles diffèrent dans la quantité de contrôle que l’application a sur le processus de liaison.</span><span class="sxs-lookup"><span data-stu-id="2374d-105">They differ in the amount of control the application has over the binding process.</span></span> <span data-ttu-id="2374d-106">Comme son nom l’indique, les poignées de liaison automatique automatisent la liaison.</span><span class="sxs-lookup"><span data-stu-id="2374d-106">As the name suggests, automatic binding handles automate binding.</span></span> <span data-ttu-id="2374d-107">Les applications client et serveur n’ont pas besoin de code pour gérer le processus de liaison.</span><span class="sxs-lookup"><span data-stu-id="2374d-107">The client and server applications do not need code to handle the binding process.</span></span> <span data-ttu-id="2374d-108">Les handles de liaison implicite permettent aux programmes clients de configurer le handle de liaison avant que la liaison ait lieu.</span><span class="sxs-lookup"><span data-stu-id="2374d-108">Implicit binding handles allow client programs to configure the binding handle before the binding takes place.</span></span> <span data-ttu-id="2374d-109">Une fois que le client a établi une liaison, la bibliothèque Runtime RPC gère le reste.</span><span class="sxs-lookup"><span data-stu-id="2374d-109">After the client establishes a binding, the RPC run-time library handles the rest.</span></span> <span data-ttu-id="2374d-110">Les handles de liaison explicites déplacent le contrôle total sur le processus de liaison dans le code source des programmes du client et du serveur.</span><span class="sxs-lookup"><span data-stu-id="2374d-110">Explicit binding handles move complete control over the binding process into the source code of the client and the server programs.</span></span> <span data-ttu-id="2374d-111">Avec ce contrôle, la complexité est accrue.</span><span class="sxs-lookup"><span data-stu-id="2374d-111">With this control comes increased complexity.</span></span> <span data-ttu-id="2374d-112">Votre application doit appeler des fonctions RPC pour gérer la liaison.</span><span class="sxs-lookup"><span data-stu-id="2374d-112">Your application must call RPC functions to manage the binding.</span></span> <span data-ttu-id="2374d-113">Elle ne se produit pas automatiquement.</span><span class="sxs-lookup"><span data-stu-id="2374d-113">It does not happen automatically.</span></span> <span data-ttu-id="2374d-114">Les handles de liaison explicites sont recommandés.</span><span class="sxs-lookup"><span data-stu-id="2374d-114">Explicit binding handles are recommended.</span></span>

<span data-ttu-id="2374d-115">Le diagramme suivant illustre les différences entre les handles de liaison automatiques, implicites et explicites.</span><span class="sxs-lookup"><span data-stu-id="2374d-115">The following diagram illustrates the differences between automatic, implicit, and explicit binding handles.</span></span>

![différences entre les handles de liaison automatiques, implicites et explicites](images/bhand.png)

<span data-ttu-id="2374d-117">En outre, chaque descripteur de liaison est de type primitif ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2374d-117">In addition, every binding handle is either primitive or custom.</span></span> <span data-ttu-id="2374d-118">Chaque type de descripteur de liaison est abordé dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="2374d-118">Each type of binding handle is discussed in the following topics:</span></span>

-   [<span data-ttu-id="2374d-119">Handles de liaison automatiques</span><span class="sxs-lookup"><span data-stu-id="2374d-119">Automatic Binding Handles</span></span>](automatic-binding-handles.md)
-   [<span data-ttu-id="2374d-120">Handles de liaison implicites</span><span class="sxs-lookup"><span data-stu-id="2374d-120">Implicit Binding Handles</span></span>](implicit-binding-handles.md)
-   [<span data-ttu-id="2374d-121">Handles de liaison explicites</span><span class="sxs-lookup"><span data-stu-id="2374d-121">Explicit Binding Handles</span></span>](explicit-binding-handles.md)
-   [<span data-ttu-id="2374d-122">Handles de liaison primitifs et personnalisés</span><span class="sxs-lookup"><span data-stu-id="2374d-122">Primitive and Custom Binding Handles</span></span>](primitive-and-custom-binding-handles.md)

 

 




