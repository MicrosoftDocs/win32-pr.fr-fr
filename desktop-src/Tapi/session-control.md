---
description: Une session ou un appel représente une connexion entre deux adresses ou plus.
ms.assetid: f598c1cd-2b50-4ac6-a05e-4fd8eeb5e3e1
title: Contrôle de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09250a90f978bde9be4f20aad6ee38f5e9766818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760797"
---
# <a name="session-control"></a><span data-ttu-id="8cf18-103">Contrôle de session</span><span class="sxs-lookup"><span data-stu-id="8cf18-103">Session Control</span></span>

<span data-ttu-id="8cf18-104">Une session ou un appel représente une connexion entre deux adresses ou plus.</span><span class="sxs-lookup"><span data-stu-id="8cf18-104">A session or call represents a connection between two or more addresses.</span></span> <span data-ttu-id="8cf18-105">Cette connexion est dynamique et les objets de programmation associés doivent être créés, manipulés et libérés si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8cf18-105">This connection is dynamic, and the associated programming objects must be created, manipulated, and released as needed.</span></span> <span data-ttu-id="8cf18-106">Dans le cas le plus simple, cela signifie créer et déconnecter un appel téléphonique.</span><span class="sxs-lookup"><span data-stu-id="8cf18-106">In the simplest case, this means making and disconnecting a phone call.</span></span> <span data-ttu-id="8cf18-107">Pour les applications avancées, le contrôle de session peut impliquer la gestion de conférences multimédias sur un réseau IP jusqu’au niveau des participants individuels.</span><span class="sxs-lookup"><span data-stu-id="8cf18-107">For advanced applications, session control may involve managing multimedia conferences over an IP network down to the level of individual participants.</span></span>

<span data-ttu-id="8cf18-108">Le contrôle de session implique deux domaines de base :</span><span class="sxs-lookup"><span data-stu-id="8cf18-108">Session control involves two basic areas:</span></span>

-   <span data-ttu-id="8cf18-109">Les [opérations de session](session-operations-ovr.md) sont des contrôles qui initient, maintiennent et mettent fin à une session de communication.</span><span class="sxs-lookup"><span data-stu-id="8cf18-109">[Session Operations](session-operations-ovr.md) are controls that initiate, maintain, and terminate a communications session.</span></span>
-   <span data-ttu-id="8cf18-110">Les [informations de session](session-information-ovr.md) décrivent les données qui peuvent être obtenues concernant une session de communication.</span><span class="sxs-lookup"><span data-stu-id="8cf18-110">[Session Information](session-information-ovr.md) describes data that can be obtained concerning a communications session.</span></span>

<span data-ttu-id="8cf18-111">Les deux types spécialisés de contrôle de session ne sont pas abordés dans cette section.</span><span class="sxs-lookup"><span data-stu-id="8cf18-111">Two specialized types of session control are not covered in this section.</span></span> <span data-ttu-id="8cf18-112">Pour plus d’informations sur les centres de distribution d’appels automatiques, consultez [contrôle de centre d’appels](./call-center-control.md) (TAPI 2. x) ou [à propos des contrôles de centre d’appels](about-call-center-controls.md) (TAPI 3. x).</span><span class="sxs-lookup"><span data-stu-id="8cf18-112">For information on Automatic Call Distribution Centers, see [Call Center Control](./call-center-control.md) (TAPI 2.x) or [About Call Center Controls](about-call-center-controls.md) (TAPI 3.x).</span></span> <span data-ttu-id="8cf18-113">Pour plus d’informations sur la conférence IP, consultez [à propos de la Conférence de téléphonie IP Rendezvous](about-rendezvous-ip-telephony-conferencing.md).</span><span class="sxs-lookup"><span data-stu-id="8cf18-113">For information on IP conferencing, see [About Rendezvous IP Telephony Conferencing](about-rendezvous-ip-telephony-conferencing.md).</span></span>

 

 
