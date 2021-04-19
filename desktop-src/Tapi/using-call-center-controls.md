---
description: Les contrôles de centre d’appels étendent le modèle d’objet TAPI 3 pour prendre en charge les exigences de systèmes ACD (Automatic Call distribution).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Utilisation des contrôles de centre d’appels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531826"
---
# <a name="using-call-center-controls"></a><span data-ttu-id="818b8-103">Utilisation des contrôles de centre d’appels</span><span class="sxs-lookup"><span data-stu-id="818b8-103">Using Call Center Controls</span></span>

<span data-ttu-id="818b8-104">Les contrôles de centre d’appels étendent le modèle d’objet TAPI 3 pour prendre en charge les exigences de systèmes ACD (Automatic Call distribution).</span><span class="sxs-lookup"><span data-stu-id="818b8-104">Call center controls extend the TAPI 3 object model to support the requirements of Automatic Call Distribution (ACD) systems.</span></span> <span data-ttu-id="818b8-105">Un centre d’appels est un lieu avec les agents ou les opérateurs des banques de téléphones qui effectuent des appels téléphoniques sortants ou des champs entrants.</span><span class="sxs-lookup"><span data-stu-id="818b8-105">A call center is a location with agents or operators at banks of telephones either making outgoing telephone calls or fielding incoming ones.</span></span> <span data-ttu-id="818b8-106">Par exemple, une société bancaire ou une société de carte de crédit utilisera un centre d’appels pour traiter les demandes de compte.</span><span class="sxs-lookup"><span data-stu-id="818b8-106">For example, a bank or credit card company will use a call center to process account inquiries.</span></span>

<span data-ttu-id="818b8-107">Les applications de centre d’appels sont divisées en trois types de base :</span><span class="sxs-lookup"><span data-stu-id="818b8-107">Call center applications are divided into three basic types:</span></span>

-   <span data-ttu-id="818b8-108">[Proxy ACD](acd-proxy.md): gère les sessions entrantes ou sortantes sur le serveur, qui peuvent être issues d’un commutateur téléphonique propriétaire vers une passerelle Internet.</span><span class="sxs-lookup"><span data-stu-id="818b8-108">[ACD Proxy](acd-proxy.md): Handles incoming or outgoing sessions at the server, which can be anything from a proprietary telephone switch to an Internet gateway.</span></span>
-   <span data-ttu-id="818b8-109">[Client de l’agent ACD](acd-agent-client.md): services d’un agent individuel recevant ou effectuant des appels.</span><span class="sxs-lookup"><span data-stu-id="818b8-109">[ACD Agent Client](acd-agent-client.md): Services an individual agent who is receiving or making calls.</span></span>
-   <span data-ttu-id="818b8-110">ACD superviseur client : fournit une vue d’ensemble des opérations de l’agent et du ACD.</span><span class="sxs-lookup"><span data-stu-id="818b8-110">ACD Supervisor Client: Provides an overall view of agent and ACD operations.</span></span>

> [!Note]  
> <span data-ttu-id="818b8-111">Pour Windows 2000, la fonctionnalité de proxy est disponible à l’aide de TAPI 2,2, et les fonctions de superviseur ne sont pas implémentées.</span><span class="sxs-lookup"><span data-stu-id="818b8-111">For Windows 2000, proxy functionality is available using TAPI 2.2, and supervisor functions are not implemented.</span></span>

 

<span data-ttu-id="818b8-112">La section Exemples de l’SDK Windows contient des exemples de code ACD sous netds \\ TAPI \\ Tapi2 \\ ACD et netds \\ TAPI \\ Tapi3 \\ ACD.</span><span class="sxs-lookup"><span data-stu-id="818b8-112">The samples section of the Windows SDK contains ACD code samples under Netds\\Tapi\\Tapi2\\Acd and Netds\\Tapi\\Tapi3\\Acd.</span></span>

 

 



