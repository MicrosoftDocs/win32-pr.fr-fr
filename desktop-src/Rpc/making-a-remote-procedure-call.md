---
title: Exécution d’un appel de procédure distante
description: Une fois que le programme client des applications distribuées qui utilise des handles de liaison explicites a un handle de liaison, il peut exécuter des procédures distantes.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Appel de procédure distante RPC, tâches, appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670989"
---
# <a name="making-a-remote-procedure-call"></a><span data-ttu-id="e29de-104">Exécution d’un appel de procédure distante</span><span class="sxs-lookup"><span data-stu-id="e29de-104">Making a Remote Procedure Call</span></span>

<span data-ttu-id="e29de-105">Une fois que le programme client des applications distribuées qui utilise des handles de liaison explicites a un handle de liaison, il peut exécuter des procédures distantes.</span><span class="sxs-lookup"><span data-stu-id="e29de-105">Once the client program of distributed applications that uses explicit binding handles has a binding handle, it can execute remote procedures.</span></span>

<span data-ttu-id="e29de-106">Microsoft RPC offre également des handles de liaison personnalisés, des handles de liaison implicites et des handles de liaison automatiques.</span><span class="sxs-lookup"><span data-stu-id="e29de-106">Microsoft RPC also offers custom binding handles, implicit binding handles, and automatic binding handles.</span></span> <span data-ttu-id="e29de-107">Ces handles de liaison offrent aux programmes clients et serveurs différents différents niveaux de contrôle sur le processus d’exécution des procédures distantes.</span><span class="sxs-lookup"><span data-stu-id="e29de-107">These binding handles offer client and server programs different levels of control over the process of executing remote procedures.</span></span> <span data-ttu-id="e29de-108">Pour plus d’informations sur les différents types de handle et la flexibilité qu’ils offrent, consultez [liaison et Handles](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="e29de-108">For details on different handle types and the flexibility they offer, see [Binding and Handles](binding-and-handles.md).</span></span>

<span data-ttu-id="e29de-109">Pour exécuter l’appel de procédure à distance, appelez la fonction stub côté client de la même manière que n’importe quelle fonction C est appelée.</span><span class="sxs-lookup"><span data-stu-id="e29de-109">To execute the procedure call remotely, call the client-side stub function in the same manner any C function is called.</span></span>

 

 




