---
title: Détails de l’implémentation EAP
description: Les points d’accès, tels que le service d’accès à distance (RAS), interagissent avec les implémentations EAP via l’utilisation d’appels de fonction qui doivent être exportés par la DLL EAP tierce.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314885"
---
# <a name="eap-implementation-details"></a><span data-ttu-id="928a5-103">Détails de l’implémentation EAP</span><span class="sxs-lookup"><span data-stu-id="928a5-103">EAP Implementation Details</span></span>

<span data-ttu-id="928a5-104">Les points d’accès, tels que le service d’accès à distance (RAS), interagissent avec les implémentations EAP via l’utilisation d’appels de fonction qui doivent être exportés par la DLL EAP tierce.</span><span class="sxs-lookup"><span data-stu-id="928a5-104">Access Points (APs), such as Remote Access Service (RAS), interact with EAP implementations through the use of function calls that must be exported by the third-party EAP DLL.</span></span> <span data-ttu-id="928a5-105">En d’autres termes, EAP est une API de fournisseur, ce qui signifie que les plug-ins ou les dll implémentent du code pour devenir un fournisseur EAP, mais ne doivent pas appeler les API EAP elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="928a5-105">In other words, EAP is a provider API, meaning that plug-ins or DLLs implement code to become an EAP provider, but must not call the EAP APIs themselves.</span></span> <span data-ttu-id="928a5-106">Par exemple, un programmeur d’une DLL EAP crée du code pour une routine d’initialisation EAP et place ce code dans la fonction prédéfinie EAP [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="928a5-106">For example, a programmer of an EAP DLL creates code for an EAP initialization routine and places this code in the EAP predefined function [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span></span> <span data-ttu-id="928a5-107">Ensuite, au moment de l’exécution, le gestionnaire de connexions AP appelle la fonction **RasEapInitialize** , qui contient le code, pour initialiser l’implémentation EAP.</span><span class="sxs-lookup"><span data-stu-id="928a5-107">Then at run-time, the AP connection manager calls the **RasEapInitialize** function, which contains the code, to initialize the EAP implementation.</span></span>

<span data-ttu-id="928a5-108">Les rubriques suivantes détaillent cette interaction :</span><span class="sxs-lookup"><span data-stu-id="928a5-108">The following topics detail this interaction:</span></span>

-   [<span data-ttu-id="928a5-109">Initialisation du point d’accès du protocole EAP</span><span class="sxs-lookup"><span data-stu-id="928a5-109">Access Point Initialization of EAP</span></span>](ras-initialization-of-eap.md)
-   [<span data-ttu-id="928a5-110">Initialisation du protocole d’authentification</span><span class="sxs-lookup"><span data-stu-id="928a5-110">Authentication Protocol Initialization</span></span>](authentication-protocol-initialization.md)
-   [<span data-ttu-id="928a5-111">Interaction du protocole d’authentification et du point d’accès</span><span class="sxs-lookup"><span data-stu-id="928a5-111">Access Point and Authentication Protocol Interaction</span></span>](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [<span data-ttu-id="928a5-112">Fin de la session d’authentification</span><span class="sxs-lookup"><span data-stu-id="928a5-112">Completion of the Authentication Session</span></span>](completion-of-the-authentication-session.md)

 

 