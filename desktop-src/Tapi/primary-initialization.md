---
description: Une application TAPI doit appeler une opération d’initialisation, qui invite une série d’actions à partir de l’interface TAPI et des fournisseurs de services qui configurent l’environnement de communication pour l’application.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Initialisation principale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534030"
---
# <a name="primary-initialization"></a><span data-ttu-id="68d75-103">Initialisation principale</span><span class="sxs-lookup"><span data-stu-id="68d75-103">Primary Initialization</span></span>

<span data-ttu-id="68d75-104">Une application TAPI doit appeler une opération d’initialisation, qui invite une série d’actions à partir de l’interface TAPI et des fournisseurs de services qui configurent l’environnement de communication pour l’application.</span><span class="sxs-lookup"><span data-stu-id="68d75-104">A TAPI application must call an initialization operation, which prompts a series of actions from TAPI and the service providers that set up the communication environment for the application.</span></span>

-   <span data-ttu-id="68d75-105">L’initialisation est synchrone et n’est pas retournée tant que l’opération n’est pas terminée ou a échoué.</span><span class="sxs-lookup"><span data-stu-id="68d75-105">Initialization is synchronous and does not return until the operation is complete or has failed.</span></span>
-   <span data-ttu-id="68d75-106">Si TAPISRV n’est pas déjà en cours d’exécution, TAPI le démarre.</span><span class="sxs-lookup"><span data-stu-id="68d75-106">If TAPISRV is not already running, TAPI starts it.</span></span>
-   <span data-ttu-id="68d75-107">L’interface TAPI configure une connexion au processus TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="68d75-107">TAPI sets up a connection to the TAPISRV process.</span></span>
-   <span data-ttu-id="68d75-108">TAPISVR charge les fournisseurs de services spécifiés dans le registre et les invite à initialiser les appareils qu’ils prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="68d75-108">TAPISVR loads the service providers specified in the registry and prompts them to initialize the devices they support.</span></span>

<span data-ttu-id="68d75-109">**TAPI 2. x :** Les applications effectuent l’initialisation en appelant [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="68d75-109">**TAPI 2.x:** Applications perform initialization by calling [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="68d75-110">**TAPI 3. x :** Les applications appellent [**ITTAPI :: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span><span class="sxs-lookup"><span data-stu-id="68d75-110">**TAPI 3.x:** Applications call [**ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span></span>

 

 
