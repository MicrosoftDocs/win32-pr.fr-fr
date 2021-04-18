---
description: Il est possible de développer une application qui effectue des opérations qui requièrent des privilèges d’administrateur, mais qui s’exécute en tant qu’utilisateur standard.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Développement d’applications nécessitant des privilèges d’administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526187"
---
# <a name="developing-applications-that-require-administrator-privilege"></a><span data-ttu-id="6ad21-103">Développement d’applications nécessitant des privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="6ad21-103">Developing Applications that Require Administrator Privilege</span></span>

<span data-ttu-id="6ad21-104">Il est possible de développer une application qui effectue des opérations qui requièrent des privilèges d’administrateur, mais qui s’exécute en tant qu’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="6ad21-104">It is possible to develop an application that performs operations that require administrator privilege yet runs as a standard user.</span></span>

<span data-ttu-id="6ad21-105">Pour ce faire, il existe plusieurs modèles.</span><span class="sxs-lookup"><span data-stu-id="6ad21-105">There are several models for accomplishing this.</span></span>



| <span data-ttu-id="6ad21-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="6ad21-106">Topic</span></span>                                                                | <span data-ttu-id="6ad21-107">Description</span><span class="sxs-lookup"><span data-stu-id="6ad21-107">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ad21-108">Modèle de tâche avec élévation de privilèges</span><span class="sxs-lookup"><span data-stu-id="6ad21-108">Elevated Task Model</span></span>](elevated-task-model.md)                       | <span data-ttu-id="6ad21-109">Une application s’exécutant en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en démarrant une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="6ad21-109">An application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>                                                                     |
| [<span data-ttu-id="6ad21-110">Modèle de service du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6ad21-110">Operating System Service Model</span></span>](operating-system-service-model.md) | <span data-ttu-id="6ad21-111">Une application s’exécutant en tant qu’utilisateur standard communique avec un service exécuté en tant que **système** à l’aide d’un [appel de procédure distante](/windows/desktop/Rpc/rpc-start-page) (RPC).</span><span class="sxs-lookup"><span data-stu-id="6ad21-111">An application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>                                              |
| [<span data-ttu-id="6ad21-112">Modèle de Broker administrateur</span><span class="sxs-lookup"><span data-stu-id="6ad21-112">Administrator Broker Model</span></span>](administrator-broker-model.md)         | <span data-ttu-id="6ad21-113">L’application est divisée en deux programmes.</span><span class="sxs-lookup"><span data-stu-id="6ad21-113">The application is divided into two programs.</span></span> <span data-ttu-id="6ad21-114">L’un des programmes s’exécute en tant qu’utilisateur standard et l’autre s’exécute avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="6ad21-114">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>                                                          |
| [<span data-ttu-id="6ad21-115">Modèle d’objet COM administrateur</span><span class="sxs-lookup"><span data-stu-id="6ad21-115">Administrator COM Object Model</span></span>](administrator-com-object-model.md) | <span data-ttu-id="6ad21-116">Une application s’exécutant en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en créant un objet de [modèle d’objet de composant](/windows/desktop/com/component-object-model--com--portal) avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="6ad21-116">An application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> |



 

 

 
