---
description: Les documents suivants fournissent des instructions sur l’utilisation de l’interface TAPI pour écrire des applications de communication d’utilisateur final ou de serveur. Ces informations sont également très utiles pour les programmeurs de fournisseurs de services.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: Applications TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521947"
---
# <a name="tapi-applications"></a><span data-ttu-id="8c81f-104">Applications TAPI</span><span class="sxs-lookup"><span data-stu-id="8c81f-104">TAPI Applications</span></span>

<span data-ttu-id="8c81f-105">Les documents suivants fournissent des instructions sur l’utilisation de l’interface TAPI pour écrire des applications de communication d’utilisateur final ou de serveur.</span><span class="sxs-lookup"><span data-stu-id="8c81f-105">The following material provides guidelines on using TAPI to write end-user or server communications applications.</span></span> <span data-ttu-id="8c81f-106">Ces informations sont également très utiles pour les programmeurs de fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="8c81f-106">This information is also highly relevant to service provider programmers.</span></span>

<span data-ttu-id="8c81f-107">La première décision qu’un programmeur doit effectuer dans à l’aide de l’interface TAPI est le niveau de service requis.</span><span class="sxs-lookup"><span data-stu-id="8c81f-107">The first decision a programmer needs to make in using TAPI is the level of service required.</span></span> <span data-ttu-id="8c81f-108">Par exemple, si une application nécessite une sélection de menu qui peut composer un numéro de téléphone, une application TAPI complète n’est probablement pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8c81f-108">For example, if an application requires a menu selection that can dial a phone number, a full TAPI application is probably not required.</span></span> <span data-ttu-id="8c81f-109">La téléphonie assistée peut activer cette option rapidement et simplement.</span><span class="sxs-lookup"><span data-stu-id="8c81f-109">Assisted Telephony can enable this option quickly and simply.</span></span> <span data-ttu-id="8c81f-110">Pour plus d’informations sur la distinction entre les applications TAPI complètes et la téléphonie assistée, consultez [niveaux de service TAPI](tapi-levels-of-service.md) .</span><span class="sxs-lookup"><span data-stu-id="8c81f-110">Please see [TAPI Levels of Service](tapi-levels-of-service.md) for more information on the distinction between full TAPI applications and Assisted Telephony.</span></span>

<span data-ttu-id="8c81f-111">La deuxième décision importante est d’utiliser TAPI 2. x, l’API basée sur C ou TAPI 3. x, qui est basé sur COM.</span><span class="sxs-lookup"><span data-stu-id="8c81f-111">The second important decision is whether to use TAPI 2.x, the C-based API, or TAPI 3.x, which is based on COM.</span></span> <span data-ttu-id="8c81f-112">Pour plus d’informations sur les considérations importantes à utiliser, consultez [TAPI 3. x et TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) .</span><span class="sxs-lookup"><span data-stu-id="8c81f-112">Please see [TAPI 3.x vs. TAPI 2.x](tapi-3-x-versus-tapi-2-x.md) for a discussion of important considerations in deciding which one to use.</span></span>

<span data-ttu-id="8c81f-113">Le diagramme suivant illustre les blocs de construction de base d’une application TAPI complète.</span><span class="sxs-lookup"><span data-stu-id="8c81f-113">The following diagram illustrates the basic building blocks of a full TAPI application.</span></span> <span data-ttu-id="8c81f-114">TAPI 2. x et TAPI 3. x sont tous deux traités dans ces sections.</span><span class="sxs-lookup"><span data-stu-id="8c81f-114">TAPI 2.x and TAPI 3.x are both addressed in these sections.</span></span> <span data-ttu-id="8c81f-115">Les documents qui sont très spécifiques à un élément sont traités dans les sections de vue d’ensemble pour TAPI 2. x ou TAPI 3. x.</span><span class="sxs-lookup"><span data-stu-id="8c81f-115">Material that is highly specific to one is addressed in the overview sections for TAPI 2.x or TAPI 3.x.</span></span>

![blocs de construction d’une application TAPI](images/tapior3.png)

<span data-ttu-id="8c81f-117">Les liens suivants fournissent du contenu qui correspond aux chiffres de l’image ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="8c81f-117">The following links provide content that corresponds to the figures in the above image:</span></span>

| <span data-ttu-id="8c81f-118">Configuration</span><span class="sxs-lookup"><span data-stu-id="8c81f-118">Figure</span></span> | <span data-ttu-id="8c81f-119">Documentation</span><span class="sxs-lookup"><span data-stu-id="8c81f-119">Documentation</span></span>                                                                    |
|--------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8c81f-120">1</span><span class="sxs-lookup"><span data-stu-id="8c81f-120">1</span></span>      | [<span data-ttu-id="8c81f-121">Initialisation TAPI</span><span class="sxs-lookup"><span data-stu-id="8c81f-121">TAPI Initialization</span></span>](tapi-initialization.md)                                   |
| <span data-ttu-id="8c81f-122">2</span><span class="sxs-lookup"><span data-stu-id="8c81f-122">2</span></span>      | [<span data-ttu-id="8c81f-123">Contrôle de session</span><span class="sxs-lookup"><span data-stu-id="8c81f-123">Session Control</span></span>](session-control.md)                                           |
| <span data-ttu-id="8c81f-124">3</span><span class="sxs-lookup"><span data-stu-id="8c81f-124">3</span></span>      | [<span data-ttu-id="8c81f-125">Contrôle de l’appareil</span><span class="sxs-lookup"><span data-stu-id="8c81f-125">Device Control</span></span>](device-control.md)                                             |
| <span data-ttu-id="8c81f-126">4</span><span class="sxs-lookup"><span data-stu-id="8c81f-126">4</span></span>      | [<span data-ttu-id="8c81f-127">Contrôle multimédia</span><span class="sxs-lookup"><span data-stu-id="8c81f-127">Media Control</span></span>](media-control.md)                                               |
| <span data-ttu-id="8c81f-128">5</span><span class="sxs-lookup"><span data-stu-id="8c81f-128">5</span></span>      | [<span data-ttu-id="8c81f-129">À propos des contrôles de centre d’appels</span><span class="sxs-lookup"><span data-stu-id="8c81f-129">About Call Center Controls</span></span>](about-call-center-controls.md)                     |
| <span data-ttu-id="8c81f-130">6</span><span class="sxs-lookup"><span data-stu-id="8c81f-130">6</span></span>      | [<span data-ttu-id="8c81f-131">Conférence de téléphonie IP Rendezvous</span><span class="sxs-lookup"><span data-stu-id="8c81f-131">Rendezvous IP Telephony Conferencing</span></span>](rendezvous-ip-telephony-conferencing.md) |
| <span data-ttu-id="8c81f-132">7</span><span class="sxs-lookup"><span data-stu-id="8c81f-132">7</span></span>      | [<span data-ttu-id="8c81f-133">Arrêt de l’interface TAPI</span><span class="sxs-lookup"><span data-stu-id="8c81f-133">TAPI Shutdown</span></span>](tapi-shutdown.md)                                               |



 

 

 



